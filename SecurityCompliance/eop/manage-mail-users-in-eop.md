---
title: Gestion des utilisateurs de messagerie dans EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP).
ms.openlocfilehash: b0093c64a0fcb5997b474e7bd491c0915164b77e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341025"
---
# <a name="manage-mail-users-in-eop"></a>Gestion des utilisateurs de messagerie dans EOP

La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP). Vous pouvez gérer les utilisateurs de différentes manières dans EOP.
  
- Utiliser la synchronisation d'annuaires pour gérer les utilisateurs de messagerie: Si votre société dispose de comptes d'utilisateur existants dans un environnement Active Directory local, vous pouvez synchroniser ces comptes avec Azure Active Directory (AD), où une copie des comptes est stockée dans le Cloud. Lorsque vous synchronisez vos comptes d'utilisateur existants avec Azure Active Directory, vous pouvez afficher ces utilisateurs **** dans le volet destinataires du centre d'administration Exchange. Il est recommandé d'utiliser la synchronisation d'annuaires. 
    
- Utilisation du CAE pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie directement dans le CAE. Il s'agit du moyen le plus facile pour ajouter des utilisateurs de messagerie et cette méthode est également utile pour ajouter un utilisateur à la fois.
    
- Utiliser Windows PowerShell à distance pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie en exécutant Windows PowerShell à distance. Cette méthode est utile pour ajouter plusieurs enregistrements et pour la création de scripts.
    
> [!NOTE]
> Vous pouvez ajouter des utilisateurs dans le Centre d'administration Office 365, mais ces utilisateurs ne peuvent pas être utilisés comme destinataires de courrier. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Les procédures décrites dans cette rubrique requièrent des autorisations spécifiques. Consultez chaque procédure pour savoir quelles autorisations sont nécessaires.
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013**Raccourcis clavier dans le Centre d'administration Exchange**.
    
> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a>Utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie

Cette section fournit des informations sur la gestion des utilisateurs de messagerie électronique à l'aide de la synchronisation d'annuaires.
  
> [!IMPORTANT]
> Si vous utilisez la synchronisation d'annuaires pour gérer vos destinataires, vous pouvez toujours ajouter et gérer les utilisateurs dans le Centre d'administration Office 365, mais ils ne seront pas synchronisés avec votre annuaire Active Directory sur site. En effet, la synchronisation d'annuaires ne synchronise que les destinataires de votre annuaire Active Directory sur site vers le nuage. 
  
> [!TIP]
>  Il est recommandé d'utiliser la synchronisation d'annuaires avec les fonctionnalités suivantes: > **Outlook Safe sender and blocked sender lists** -lors de la synchronisation avec le service, ces listes prévalent sur le filtrage du courrier indésirable dans le service. Cela permet aux utilisateurs de gérer leurs propres listes d'expéditeurs autorisés et bloqués au niveau de chaque utilisateur ou domaine. **blocage du périmètre basé sur l'annuaire > (DBEB)** : pour plus d'informations sur DBEB, consultez la rubrique [use Directory based Edge blockIng to Reject messages sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx). **mise en quarantaine du courrier** indésirable de l'utilisateur final >: pour accéder à la mise en quarantaine du courrier indésirable de l'utilisateur final, les utilisateurs finaux doivent posséder un ID d'utilisateur et un mot de passe Office 365 valides. Les clients EOP qui protègent les boîtes aux lettres locales doivent être des utilisateurs de messagerie valides. **règles de flux de messagerie** >: lorsque vous utilisez la synchronisation d'annuaires, vos utilisateurs et groupes Active Directory existants sont automatiquement téléchargés dans le Cloud, puis vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) qui ciblent des utilisateurs spécifiques et/ou ou des groupes sans avoir à les ajouter manuellement via le centre d'administration Exchange ou Exchange Online Protection PowerShell. Notez que les [groupes de distribution dynamique](https://go.microsoft.com/fwlink/?LinkId=507569) ne peuvent pas être synchronisés via la synchronisation d'annuaires. 
  
 **Avant de commencer**
  
Obtenez les autorisations nécessaires et préparez la synchronisation d'annuaires, comme décrit dans la rubrique [Préparer la synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308908).
  
### <a name="to-synchronize-user-directories"></a>Pour synchroniser les annuaires d'utilisateurs

1. Activez la synchronisation d'annuaires, comme décrit dans la rubrique [Activer la synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308909).
    
2. Configurez votre ordinateur de synchronisation d'annuaires, comme décrit dans la rubrique [Configurer votre ordinateur de synchronisation d'annuaires](http://go.microsoft.com/fwlink/p/?LinkId=308911).
    
3. Synchronisez vos annuaires, comme décrit dans la rubrique [Utiliser l'Assistant Configuration pour synchroniser vos annuaires](http://go.microsoft.com/fwlink/?LinkId=308912).
    
    > [!IMPORTANT]
    > Après exécution de l'Assistant Configuration de l'outil de synchronisation Azure Active Directory, le compte **MSOL_AD_SYNC** est créé dans votre forêt Active Directory. Ce compte permet de lire et de synchroniser vos informations Active Directory sur site. Pour que la synchronisation d'annuaires fonctionne correctement, assurez-vous que le port TCP 443 est ouvert sur votre serveur de synchronisation d'annuaires sur site. 
  
4. Activez les utilisateurs synchronisés, comme décrit dans la rubrique [Activer les utilisateurs synchronisés](http://go.microsoft.com/fwlink/p/?LinkId=308913).
    
5. Gérez la synchronisation d'annuaires, comme décrit dans la rubrique [Gérer la synchronisation d'annuaires](http://go.microsoft.com/fwlink/p/?LinkId=308915).
    
6. Vérifiez qu'EOP effectue la synchronisation correctement. Dans le CAE, accédez à **Destinataires** \> **Contacts** et vérifiez que la liste des utilisateurs a été correctement synchronisée à partir de votre environnement local. 
    
## <a name="use-the-eac-to-manage-mail-users"></a>Utilisation du CAE pour gérer les utilisateurs de messagerie

Cette section fournit des informations sur l'ajout et la gestion des utilisateurs de messagerie directement dans le CAE.
  
 **Avant de commencer**
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).
  
### <a name="to-add-a-mail-user-in-the-eac"></a>Pour ajouter un utilisateur de messagerie dans le CAE

1. Créez un utilisateur de messagerie électronique en accédant à **Destinataires** \> **Contacts** dans le CAE, puis cliquez sur **Nouveau +**.
    
2. Sur la page **Nouvel utilisateur de messagerie**, saisissez les informations de l'utilisateur, notamment les éléments suivants : 
    
   ****

|**Propriété d'utilisateur de messagerie**|**Description**|
|:-----|:-----|
|**Prénom**, **Initiales** et **Nom de famille** <br/> |Dans les zones appropriées, saisissez le nom de l'utilisateur.  <br/> |
|**Nom complet** <br/> |Saisissez le nom (64 caractères maximum). Par défaut, cette zone est renseignée avec les noms que vous avez entrés dans les champs **Prénom**, **Initiales** et **Nom de famille**, le cas échéant. Le nom complet est requis.  <br/> |
|**Alias** <br/> |Saisissez un alias unique pour l'utilisateur (64 caractères maximum). L'alias est obligatoire.  <br/> |
|**Adresse de messagerie externe** <br/> |Saisissez l'adresse de messagerie électronique externe de l'utilisateur.  <br/> |
|**ID utilisateur** <br/> |Saisissez le nom que l'utilisateur de messagerie utilisera pour se connecter au service. Le nom de connexion de l'utilisateur est constitué du nom d'utilisateur à gauche du symbole (@) et d'un suffixe à droite. Généralement, le suffixe est le nom du domaine dans lequel le compte d'utilisateur réside.  <br/> |
|**Nouveau mot de passe** <br/> |Saisissez le mot de passe que l'utilisateur de messagerie utilisera pour se connecter au service. Assurez-vous que le mot de passe que vous saisissez est conforme aux exigences de longueur, de complexité et d'historique de mot de passe du domaine dans lequel vous créez le compte d'utilisateur.  <br/> |
|**Confirmer le mot de passe** <br/> |Ressaisissez le mot de passe pour le confirmer.  <br/> |
   
3. Cliquez sur **Nouveau** pour créer l'utilisateur de messagerie. Le nouvel utilisateur doit apparaître dans la liste des utilisateurs. 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a>Pour modifier ou supprimer un utilisateur de messagerie dans le CAE

- Dans le centre d'administration Exchange **** \> , accédez à **contacts**des destinataires. Dans la liste des utilisateurs, cliquez sur l'utilisateur que vous souhaitez afficher ou modifier, puis sélectionnez **modifier** ![l'icône](../media/ITPro-EAC-EditIcon.gif) modifier pour mettre à jour les paramètres utilisateur selon vos besoins. Vous pouvez modifier le nom, l'alias ou les informations de contact de l'utilisateur, et vous pouvez enregistrer des informations détaillées sur le rôle de l'utilisateur dans l'organisation. Vous pouvez également sélectionner un utilisateur, puis cliquer sur **supprimer**![l'](../media/ITPro-EAC-RemoveIcon.gif) icône Supprimer pour le supprimer. 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a>Utiliser Windows PowerShell à distance pour gérer les utilisateurs de messagerie

Cette section fournit des informations sur l'ajout et la gestion des utilisateurs de messagerie à l'aide de Windows PowerShell à distance.
  
 **Avant de commencer**
  
- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).
    
- Gardez à l'esprit que lorsque vous créez des utilisateurs de messagerie à l'aide de cmdlets PowerShell à distance, vous pouvez être confronté à des limitations.
    
- Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.
    
- Pour découvrir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online Protection à l'aide d'une session PowerShell distante](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).
    
 **Pour ajouter un utilisateur de messagerie à l'aide de PowerShell à distance**
  
Cet exemple illustre la création d'un compte d'utilisateur à extension messagerie avec la cmdlet [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) pour l'utilisateur Jeffrey Zeng, avec les informations suivantes : 
  
- Le prénom est Jeffrey et le nom est Zeng.
    
- Le nom est Jeffrey et le nom d'affichage est Jeffrey Zeng.
    
- L'alias est jeffreyz.
    
- L'adresse de messagerie externe est jzeng@tailspintoys.com.
    
- Le nom de connexion à Office 365 est jeffreyz@contoso.onmicrosoft.com.
    
- Le mot de passe est Pa$$word1.
    
```
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 **Pour vérifier que cela a fonctionné**
  
Exécutez la cmdlet [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) comme suit pour afficher les informations relatives au nouvel utilisateur de messagerie Jeffrey Zeng : 
  
```
Get-User "Jeffrey Zeng"

```

 **Pour modifier les propriétés d'un utilisateur de messagerie à l'aide de PowerShell à distance**
  
Utilisez les cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) et [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) pour afficher et modifier les propriétés des utilisateurs de messagerie. 
  
Cet exemple illustre la configuration de l'adresse de messagerie externe pour Pilar Pinilla.
  
```
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

Cet exemple illustre la définition de la propriété Company sur Contoso pour tous les utilisateurs de messagerie.
  
```
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 **Pour vérifier que cela a fonctionné**
  
Dans l'exemple précédent où nous avons modifié les propriétés de l'utilisateur de messagerie nommé Pilar Pinilla, utilisez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) pour vérifier les modifications. (Vous pouvez afficher plusieurs propriétés pour plusieurs contacts de messagerie.) 
  
```
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

Dans l'exemple précédent où la propriété Company a été définie sur Contoso pour tous les utilisateurs de messagerie, exécutez la commande suivante pour vérifier les modifications :
  
```
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles. 
  
 **Pour supprimer un utilisateur de messagerie à l'aide de PowerShell à distance**
  
Cet exemple utilise la cmdlet [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) pour supprimer l'utilisateur Jeffrey Zeng : 
  
```
Remove-EOPMailUser -Identity Jeffrey
```

 **Pour vérifier que cela a fonctionné**
  
Exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) comme suit. Vous devriez obtenir un message d'erreur car l'utilisateur n'existe plus. 
  
```
Get-Recipient Jeffrey | fl
```


