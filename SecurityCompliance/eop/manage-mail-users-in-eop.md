---
title: Gestion des utilisateurs de messagerie dans EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP).
ms.openlocfilehash: 48d530be17a7e75f6e179a50067b1b9526606cb0
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676714"
---
# <a name="manage-mail-users-in-eop"></a>Gestion des utilisateurs de messagerie dans EOP

La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP). Vous pouvez gérer les utilisateurs de différentes manières dans EOP.
  
- Utilisation de la synchronisation d'annuaires pour gérer les utilisateurs de messagerie : si votre entreprise dispose de comptes d'utilisateur dans un environnement Active Directory local, vous pouvez synchroniser ces comptes sur Azure Active Directory (AD), où des copies des comptes sont stockées dans le nuage. Lorsque vous synchronisez vos comptes d'utilisateur sur Azure Active Directory, vous pouvez consulter ces utilisateurs dans le volet **Destinataires** du Centre d'administration Exchange (CAE). L'utilisation de la synchronisation d'annuaires est recommandée. 

- Utilisation du CAE pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie directement dans le CAE. Il s'agit du moyen le plus facile pour ajouter des utilisateurs de messagerie et cette méthode est également utile pour ajouter un utilisateur à la fois.

- Utiliser Windows PowerShell à distance pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie en exécutant Windows PowerShell à distance. Cette méthode est utile pour ajouter plusieurs enregistrements et pour la création de scripts.

> [!NOTE]
> Vous pouvez ajouter des utilisateurs dans le centre d’administration 365 de Microsoft, mais ces utilisateurs ne peuvent pas être utilisés comme destinataires de courrier.
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).

- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).

- N’oubliez pas que lors de la création d’utilisateurs de messagerie à l’aide des cmdlets PowerShell d’Exchange Online Protection, vous pouvez rencontrer des limitations.

- Les commandes PowerShell de cette rubrique utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes soient visibles.

- Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).

- Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).

> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a>Utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie

Cette section fournit des informations sur la gestion des utilisateurs de messagerie électronique à l’aide de la synchronisation d’annuaires.
  
> [!NOTE]
> Si vous utilisez la synchronisation d’annuaires pour gérer vos destinataires, vous pouvez toujours ajouter et gérer des utilisateurs dans le centre d’administration 365 de Microsoft, mais ils ne seront pas synchronisés avec votre annuaire Active Directory local. En effet, la synchronisation d'annuaires ne synchronise que les destinataires de votre annuaire Active Directory sur site vers le nuage. <br/><br/> La synchronisation d’annuaires est recommandée pour une utilisation avec les fonctionnalités suivantes: <br/><br/>• Listes des expéditeurs autorisés **et des expéditeurs bloqués Outlook**: lorsqu’ils sont synchronisés avec le service, ces listes prévalent sur le filtrage du courrier indésirable dans le service. Cela permet aux utilisateurs de gérer leurs propres listes d’expéditeurs autorisés et bloqués en fonction de l’utilisateur et du domaine. <br/><br/>• **Blocage du périmètre basé sur l’annuaire (DBEB)**: pour plus d’informations sur DBEB, voir [use Directory based Edge Blocking to Reject messages sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx). <br/><br/>• **Mise en quarantaine du courrier**indésirable de l’utilisateur final: pour accéder à la mise en quarantaine du courrier indésirable de l’utilisateur final, les utilisateurs finaux doivent posséder un ID d’utilisateur et un mot de passe Office 365 valide. Les clients qui utilisent EOP pour la protection des boîtes aux lettres locales doivent être des utilisateurs de messagerie électronique valides. <br/><br/>• **Règles de flux de messagerie**: lorsque vous utilisez la synchronisation d’annuaires, vos utilisateurs et groupes Active Directory existants sont automatiquement téléchargés dans le Cloud, puis vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) ciblant des utilisateurs spécifiques et/ou groupes sans avoir à les ajouter manuellement via le centre d’administration Exchange ou Exchange Online Protection PowerShell. Notez que les [groupes de distribution dynamique](https://go.microsoft.com/fwlink/?LinkId=507569) ne peuvent pas être synchronisés via la synchronisation d’annuaires.
  
Obtenez les autorisations nécessaires et préparez la synchronisation d'annuaires, comme décrit dans la rubrique [Préparer la synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308908).
  
### <a name="to-synchronize-user-directories-with-azure-active-directory-connect-aad-connect"></a>Pour synchroniser les annuaires d’utilisateurs avec Azure Active Directory Connect (AAD Connect)

Pour synchroniser les utilisateurs avec Azure Active Directory (AAD), vous devez d’abord **activer la synchronisation**d’annuaires, comme décrit dans la rubrique activation de la [synchronisation](https://go.microsoft.com/fwlink/p/?LinkId=308909)d’annuaires.

Ensuite, l’installation et la configuration d’un ordinateur local pour exécuter AAD Connect (si vous n’avez pas encore besoin de vérifier à l’avance). La rubrique [configuration de AAD Connect, la rubrique relative à la méthode rapide](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express) vous indique comment configurer et synchroniser vos comptes de l’organisation locale vers Azure ad avec AAD Connect.

Mais avant cela, [vous devez vous assurer que vous répondez aux conditions préalables](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites)et [Choisissez votre type d’installation](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation). Le lien précédent est un petit article pour les installations rapides. Vous pouvez également trouver des articles sur les [installations personnalisées](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)ou [l’authentification directe](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start) si elles sont nécessaires.

> [!IMPORTANT]
> Après exécution de l'Assistant Configuration de l'outil de synchronisation Azure Active Directory, le compte **MSOL_AD_SYNC** est créé dans votre forêt Active Directory. Ce compte permet de lire et de synchroniser vos informations Active Directory sur site. Pour que la synchronisation d'annuaires fonctionne correctement, assurez-vous que le port TCP 443 est ouvert sur votre serveur de synchronisation d'annuaires sur site.

Après avoir configuré votre synchronisation, assurez-vous de vérifier que EOP effectue une synchronisation correcte. Dans le CAE, accédez à **Destinataires** \> **Contacts** et vérifiez que la liste des utilisateurs a été correctement synchronisée à partir de votre environnement local.

## <a name="use-the-eac-to-manage-mail-users"></a>Utilisation du CAE pour gérer les utilisateurs de messagerie

Cette section fournit des informations sur l’ajout et la gestion des utilisateurs de messagerie directement dans le CAE.
  
### <a name="use-the-eac-to-add-a-mail-user"></a>Utiliser le centre d’administration Exchange pour ajouter un utilisateur de messagerie

1. Créez un utilisateur de messagerie électronique en accédant à **Destinataires** \> **Contacts** dans le CAE, puis cliquez sur **Nouveau +**.

2. Sur la page **Nouvel utilisateur de messagerie**, saisissez les informations de l'utilisateur, notamment les éléments suivants : 

   ****

   |**Propriété d'utilisateur de messagerie**|**Description**|
   |:-----|:-----|
   |**Prénom**, **Initiales** et **Nom de famille**|Dans les zones appropriées, saisissez le nom de l'utilisateur.|
   |**Nom complet**|Saisissez le nom (64 caractères maximum). Par défaut, cette zone est renseignée avec les noms que vous avez entrés dans les champs **Prénom**, **Initiales** et **Nom de famille**, le cas échéant. Le nom complet est requis.  |
   |**Alias**|Saisissez un alias unique pour l'utilisateur (64 caractères maximum). L'alias est obligatoire.|
   |**Adresse de messagerie externe**|Saisissez l'adresse de messagerie électronique externe de l'utilisateur.|
   |**ID utilisateur**|Saisissez le nom que l'utilisateur de messagerie utilisera pour se connecter au service. Le nom de connexion de l'utilisateur est constitué du nom d'utilisateur à gauche du symbole (@) et d'un suffixe à droite. Généralement, le suffixe est le nom du domaine dans lequel le compte d'utilisateur réside.|
   |**Nouveau mot de passe**|Saisissez le mot de passe que l'utilisateur de messagerie utilisera pour se connecter au service. Assurez-vous que le mot de passe que vous saisissez est conforme aux exigences de longueur, de complexité et d'historique de mot de passe du domaine dans lequel vous créez le compte d'utilisateur.|
   |**Confirmer le mot de passe**|Ressaisissez le mot de passe pour le confirmer.|

3. Cliquez sur **Nouveau** pour créer l'utilisateur de messagerie. Le nouvel utilisateur doit apparaître dans la liste des utilisateurs.

### <a name="use-the-eac-to-edit-or-remove-a-mail-user"></a>Utiliser le centre d’administration Exchange pour modifier ou supprimer un utilisateur de messagerie

- Dans le CAE, accédez à **Destinataires** \> **Contacts**. Dans la liste des utilisateurs, cliquez sur l’utilisateur que vous souhaitez afficher ou modifier, puis sélectionnez **modifier** ![l’icône](../media/ITPro-EAC-EditIcon.gif) modifier pour mettre à jour les paramètres utilisateur selon vos besoins. Vous pouvez modifier le nom, l'alias ou les coordonnées de l'utilisateur et vous pouvez enregistrer des informations détaillées sur le rôle de l'utilisateur dans l'organisation. Vous pouvez également sélectionner un utilisateur, puis cliquer sur **supprimer** ![l'](../media/ITPro-EAC-RemoveIcon.gif) icône Supprimer pour le supprimer. 

## <a name="use-exchange-online-protection-powershell-to-manage-mail-users"></a>Utiliser Exchange Online Protection PowerShell pour gérer les utilisateurs de messagerie

Cette section fournit des informations sur l'ajout et la gestion des utilisateurs de messagerie à l'aide de Windows PowerShell à distance.
  
### <a name="use-eop-powershell-to-add-a-mail-user"></a>Utiliser EOP PowerShell pour ajouter un utilisateur de messagerie
  
Cet exemple illustre la création d'un compte d'utilisateur à extension messagerie avec la cmdlet [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-eopmailuser) pour l'utilisateur Jeffrey Zeng, avec les informations suivantes :
  
- Le prénom est Jeffrey et le nom est Zeng.

- Le nom est Jeffrey et le nom d'affichage est Jeffrey Zeng.

- L'alias est jeffreyz.

- L'adresse de messagerie externe est jzeng@tailspintoys.com.

- Le nom de connexion à Office 365 est jeffreyz@contoso.onmicrosoft.com.

- Le mot de passe est Pa$$word1.

```Powershell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

Pour vérifier qu’elle a fonctionné, exécutez la commande suivante pour afficher les informations sur le nouvel utilisateur de messagerie Jeffrey Zeng:
  
```Powershell
Get-User -Identity "Jeffrey Zeng"
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-User](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-user).

### <a name="use-eop-powershell-to-edit-the-properties-of-a-mail-user"></a>Utiliser EOP PowerShell pour modifier les propriétés d’un utilisateur de messagerie
  
Utilisez les cmdlets [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) et [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopmailuser) pour afficher et modifier les propriétés des utilisateurs de messagerie.
  
Cet exemple illustre la configuration de l'adresse de messagerie externe pour Pilar Pinilla.
  
```Powershell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

Cet exemple illustre la définition de la propriété Company sur Contoso pour tous les utilisateurs de messagerie.
  
```Powershell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}
```
  
Pour vérifier que cela a fonctionné, utilisez la cmdlet [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) pour vérifier les modifications. (Vous pouvez afficher plusieurs propriétés pour plusieurs contacts de messagerie.)
  
```Powershell
Get-Recipient -Identity "Pilar Pinilla" | Format-List
```

Dans l'exemple précédent où la propriété Company a été définie sur Contoso pour tous les utilisateurs de messagerie, exécutez la commande suivante pour vérifier les modifications :
  
```Powershell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.
  
### <a name="use-eop-powershell-to-remove-a-mail-user"></a>Utiliser EOP PowerShell pour supprimer un utilisateur de messagerie
  
Cet exemple utilise la cmdlet [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient/remove-eopmailuser) pour supprimer l'utilisateur Jeffrey Zeng :
  
```Powershell
Remove-EOPMailUser -Identity Jeffrey
```

 **Pour vérifier que cela a fonctionné**
  
Pour vérifier que cela a fonctionné, exécutez la cmdlet [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) pour vérifier que l’utilisateur de messagerie n’existe plus.
  
```Powershell
Get-Recipient Jeffrey | Format-List
```
