---
title: Configurer des stratégies de surveillance pour votre organisation
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Configurer une vérification de surveillance des stratégies pour capturer les communications des employés pour la révision.
ms.openlocfilehash: 898ef9951ea20dec1e0cc6c28ad1ed6f9a0ded6e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29768035"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Configurer des stratégies de surveillance pour votre organisation

Utiliser des stratégies de surveillance pour capturer les communications des employés pour l’examen des réviseurs internes ou externes. Pour plus d’informations sur comment les stratégies de surveillance peuvent vous aider à contrôler les communications dans votre organisation, voir [stratégies de surveillance dans Office 365](supervision-policies.md).

> [!NOTE]
> Utilisateurs contrôlés par des stratégies de surveillance doivent avoir une licence d’Office 365 entreprise E3 avec le module complémentaire de conformité avancée ou être inclus dans un abonnement à Office 365 entreprise E5. Si vous n’avez un plan d’entreprise E5 existant et essayer de surveillance, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
Suivez ces étapes pour configurer et utiliser le contrôle de votre organisation Office 365 :
  
- **Étape 1 (facultatif)** - [configuré des groupes de surveillance](configure-supervision-policies.md#exampledist)

    Avant de commencer à l’aide de surveillance, déterminer qui sera leurs communications révisé et qui effectue les révisions. Si vous souhaitez prendre en main quelques aux utilisateurs de voir le fonctionne de surveillance, vous pouvez ignorer la configuration de groupes pour l’instant.

- **Étape 2 (requis)** - [rendre disponibles dans votre organisation de surveillance](configure-supervision-policies.md#MakeAvailable)

    Ajoutez-vous au groupe de rôles de supervision afin que vous pouvez définir des stratégies. Toute personne ce rôle a été attribué permettre accéder à la page **surveillance** sous **La gouvernance des données** dans le centre de conformité de & sécurité. Si le courrier électronique à réviser est hébergé sur Exchange Online, chaque réviseur doit également accéder [à distance PowerShell vers Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

- **Étape 3 (facultative)** - [configurer les types d’informations sensibles personnalisés ou des dictionnaires personnalisés de mots clés/lexiques](configure-supervision-policies.md#sensitiveinfo)

    Si vous avez besoin d’utiliser un type d’informations sensibles personnalisé ou un dictionnaire personnalisé de mot clé pour votre stratégie de surveillance, vous devez le créer avant de démarrer l’Assistant de surveillance.

- **Étape 4 (requis)** - [définir une stratégie de surveillance](configure-supervision-policies.md#setupsuper)

    Vous allez créer des stratégies de surveillance dans le centre de conformité de & sécurité. Ces stratégies définissent les communications sont soumis à la révision de votre organisation et spécifie qui doit effectuer des analyses. Communications comprennent e-mail et les communications Microsoft Teams, ainsi que les communications plateforme 3 rd tiers (tels que Facebook, Twitter, etc.)

- **Étape 5 : (facultatif)** [Test de votre nouvelle stratégie de surveillance](configure-supervision-policies.md#TestPolicy)

    Testez votre stratégie de surveillance pour vous assurer qu’il fonctionne comme vous le souhaitez est une part importante de s’assurer que votre stratégie de conformité est normes votre.

- **Étape 6 : (facultatif)** [Installer le complément Outlook pour relecteurs qui ne souhaitez pas utiliser le tableau de bord de surveillance Office 365 ou OWA pour passer en revue les communications contrôlées](configure-supervision-policies.md#UseOutlook)

    Le complément de contrôle pour Outlook donne relecteurs accès à droite de la fonctionnalité de surveillance dans le client Outlook afin qu’ils puissent évaluer et classer chaque élément.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>Étape 1 : configurer des groupes de surveillance (facultatif)

 Lorsque vous créez une stratégie de surveillance, vous devez déterminer qui auront leurs communications révisées et qui effectue les révisions. Dans la stratégie, vous allez utiliser des adresses de messagerie pour identifier des utilisateurs individuels ou des groupes de personnes. Pour simplifier votre installation, créez des personnes disposant de leurs communications révisée et les groupes pour les personnes qui validera les communications. Si vous utilisez des groupes, vous devrez peut-être plusieurs — par exemple, si vous souhaitez surveiller les communications entre les deux groupes distincts de personnes, ou si vous souhaitez spécifier un groupe qui n’est pas sur le point d’être surveillés. Pour plus d’informations sur cette procédure, voir [groupes de distribution exemple](configure-supervision-policies.md#GroupExample) .
  
Pour contrôler les communications entre ou au sein de groupes de votre organisation, configurer des groupes de distribution dans le centre d’administration Exchange (accédez à **destinataires** \> **groupes**). Pour plus d’informations sur la configuration de groupes de distribution, voir [Gérer les groupes de distribution](http://go.microsoft.com/fwlink/?LinkId=613635)
  
> [!NOTE]
> Vous pouvez également utiliser des groupes de distribution dynamique ou de groupes de sécurité de surveillance si vous préférez. Pour vous aider à décider si ces adaptées à votre organisation a besoin, voir [Gérer les groupes de sécurité à extension messagerie](http://go.microsoft.com/fwlink/?LinkId=627033)et [Gérer les groupes de distribution dynamique](http://go.microsoft.com/fwlink/?LinkId=627058).
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>Exemple de groupes de distribution

Cet exemple inclut un groupe de distribution qui a été configuré pour une organisation financière appelée Contoso financières International.
  
Chez Contoso Financial International, un échantillonnage des communications entre les courtiers aux États-Unis doit être effectué. Toutefois, les responsables de la mise en conformité au sein de ce groupe ne doivent pas être surveillés. Dans cet exemple, nous pouvons créer les groupes suivants :
  
|**Configuration de ce groupe de distribution**|**Adresse de groupe (alias)**|**Description**|
|:-----|:-----|:-----|
|Tous les courtiers des États-Unis | US_Brokers@contoso.com | Ce groupe contient les adresses de messagerie de tous les courtiers basés aux États-Unis qui travaillent pour Contoso. |
| Tous les responsables de la mise en conformité des États-Unis | US_Compliance@contoso.com  | Ce groupe comprend les adresses de messagerie pour tous les responsables de conformité basée aux États-Unis qui travaillent pour Contoso. Ce groupe étant un sous-ensemble de tous les agents basée aux États-Unis, vous pouvez utiliser cet alias pour exemptés de conformité d’une stratégie de surveillance. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>Étape 2 : surveillance rendre disponible dans votre organisation (requis)

Pour rendre la **surveillance** disponible sous forme d’une option de menu dans le centre de conformité de & sécurité, vous devez être affecté le rôle d’administrateur de passer en revue les surveillance.
  
Pour ce faire, vous pouvez ajouter vous-même en tant que membre du groupe de rôles de supervision, ou vous pouvez créer un nouveau groupe de rôles.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Ajouter des membres au groupe de rôles de supervision

1. Se connecter à [https://protection.office.com](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365.

2. Dans le centre de conformité & sécurité, accédez à **autorisations**.

3. Sélectionnez le groupe de rôles **De supervision** , puis cliquez sur l’icône Modifier.

4. Dans la section **membres** , ajoutez les personnes que vous souhaitez gérer la surveillance pour votre organisation.

### <a name="create-a-new-role-group"></a>Créer un nouveau groupe de rôles

1. Se connecter à [https://protection.office.com](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365.

2. Dans le centre de conformité & sécurité, accédez à **autorisations** , puis cliquez sur Ajouter (**+**).

3. Dans la section **rôles** , cliquez sur Ajouter (**+**) et faites défiler jusqu'à la **Surveillance administrateur de révision**. Ajoutez ce rôle au groupe de rôles.

4. Dans la section **membres** , ajoutez les personnes que vous souhaitez gérer la surveillance pour votre organisation.

Pour plus d’informations sur les groupes de rôles et autorisations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>Activer l’accès à distance PowerShell pour relecteurs (si la messagerie est hébergée sur Exchange Online)

1. Suivez les instructions de [Activer ou désactiver l’accès à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>Étape 3 : créer des types d’informations sensibles personnalisés ou des dictionnaires personnalisés de mot clé (facultatif)

Afin de choisir parmi les types d’informations sensibles personnalisées existants ou les dictionnaires personnalisés de mot clé dans l’Assistant de la stratégie de surveillance, vous devez d’abord créer ces éléments si nécessaire.

### <a name="create-custom-sensitive-information-types"></a>Créer des types d’informations sensibles personnalisé

1. Créer un nouveau type d’informations sensibles dans les & de sécurité pour Microsoft Office 365 centre de conformité. Accédez à **Classifications** \> **types d’informations sensibles** et suivez les étapes de l' **Assistant nouveau type d’informations sensibles**. Vous allez ici :

    - Définir un nom et une description pour le type d’informations sensibles
    - Définir la proximité, niveau de confiance et des éléments de motif principal
    - Vérifiez vos sélections et créer le type d’informations sensibles

    Pour plus d’informations, voir [créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).

### <a name="create-custom-keyword-dictionarylexicon"></a>Créer le dictionnaire personnalisé de mots clés/lexique

1. À l’aide d’un éditeur de texte (comme le bloc-notes), créez un nouveau fichier qui contient les termes de mot clé que vous souhaitez surveiller dans une stratégie de surveillance. Assurez-vous que chaque terme est sur une ligne distincte et enregistrez le fichier au format **Unicode UTF-16 / (Little Endian)** .
2. Importer le fichier de mots clés dans votre organisation cliente Office 365 à l’aide de PowerShell. Pour vous connecter à Office 365 avec PowerShell, voir [se connecter à Office 365 sécurité & PowerShell du centre de conformité](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

    Une fois que vous êtes connecté à Office 365 avec PowerShell, exécutez les commandes suivantes pour importer le dictionnaire de mots clés :

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    Pour plus d’informations, voir [créer un dictionnaire de mot clé](create-a-keyword-dictionary.md).

3. Créer un nouveau type d’informations sensibles dans les & de sécurité pour Microsoft Office 365 centre de conformité. Accédez à **Classifications** \> **types d’informations sensibles** et suivez les étapes de l' **Assistant nouveau type d’informations sensibles**. Vous allez ici :

    - Définir un nom et une description pour le type d’informations sensibles
    - Ajouter le dictionnaire personnalisé en tant qu’une condition requise pour l’élément correspondant
    - Vérifiez vos sélections et créer le type d’informations sensibles

    Une fois le dictionnaire personnalisé/lexique est créé, vous pouvez afficher des mots clés configurés à l’aide de l’applet de commande [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) ou ajouter ou supprimer des termes à l’aide de l’applet de commande [Set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) .

    Pour plus d’informations, voir [créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>Étape 4 : configurer une stratégie de surveillance (requis)
  
1. Se connecter à [https://protection.office.com](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365.

2. Dans le centre de conformité & sécurité, sélectionnez le **contrôle**.
  
3. Sélectionnez **créer** , puis suivez l’Assistant pour configurer les pages suivantes de la stratégie. À l’aide de l’Assistant, vous pouvez :

    - Donnez un nom et une description à la stratégie.
    - Sélectionnez les utilisateurs ou des groupes à surveiller, y compris le choix des utilisateurs ou des groupes que vous souhaitez exclure.
    - Définir les conditions de stratégie de surveillance.
    - Choisissez si vous souhaitez inclure les types d’informations sensibles. Il s’agit d’où vous pouvez sélectionner les types d’informations sensibles personnalisés et par défaut.
    - Définir le pourcentage de communications pour passer en revue.
    - Choisissez les réviseurs de la stratégie. Relecteurs peuvent être des utilisateurs individuels ou des [groupes de sécurité à extension messagerie](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group).
    - Vérifiez vos sélections de stratégie et créer la stratégie.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>Étape 5 : Test de votre stratégie de surveillance (facultatif)

Après avoir créé une stratégie de surveillance, il est conseillé de tester pour vous assurer que les conditions que vous avez définies sont correctement appliquées par la stratégie. Vous pouvez également pour [tester les règles de protection contre la perte de données](create-test-tune-dlp-policy.md) si vos stratégies de surveillance sont les types d’informations sensibles. Suivez la procédure ci-dessous pour tester votre stratégie de surveillance :

1. Ouvrir un client de messagerie ou Microsoft Teams connecté en tant qu’un utilisateur supervisé défini dans la stratégie que vous souhaitez tester.
2. Envoyer un courrier électronique ou une conversation Teams Microsoft qui répond aux critères que vous avez définie dans la stratégie de surveillance. Il peut s’agir d’un mot clé taille de pièce jointe, domaine, etc.. Assurez-vous de que déterminer si vos paramètres conditionnelle configurés dans la stratégie est trop restrictif ou trop stricte ou non.

    > [!Note]
    > Les messages électroniques soumis aux stratégies définies sont traités dans presque en temps réel et peuvent être testés immédiatement après avoir configuré la stratégie. Salles de conversation dans Microsoft Teams peuvent prendre jusqu'à 24 heures pour traiter entièrement dans une stratégie. 

3. Connectez-vous à votre client Office 365 en tant que réviseur indiqué dans la stratégie de surveillance. Accédez à la **surveillance** > *Votre stratégie personnalisée* > **Open** pour afficher le rapport de la stratégie.

<a name="UseOutlook"> </a>

## <a name="step-6---set-up-outlook-add-in-for-reviewers-optional"></a>Étape 6 : configurer complément Outlook pour relecteurs (facultatif)

Réviseurs want utiliser Outlook au lieu d’utiliser le tableau de bord de surveillance dans Office 365 ou Outlook sur le web pour passer en revue les communications doivent installer le complément de contrôle pour leur client Outlook.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Étape 1 : Copier l’adresse de la boîte aux lettres de surveillance

Pour installer le complément pour Outlook du bureau, vous devez l’adresse pour la boîte aux lettres de surveillance qui a été créé dans le cadre de la configuration de stratégie de surveillance.
  
> [!NOTE]
> Si un autre utilisateur la stratégie, vous devez obtenir cette adresse à partir de celles-ci pour installer le complément.

 **Pour rechercher l’adresse de boîte aux lettres de surveillance**
  
1. Se connecter à la [sécurité &amp; centre de conformité](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365.

2. Accédez à la **surveillance**.

3. Cliquez sur la stratégie de surveillance qui collecte les communications que vous souhaitez examiner.

4. Dans la fenêtre mobile stratégie plus d’informations, sous **boîte aux lettres de surveillance**, copiez l’adresse.<br/>![La section « Boîte aux lettres de surveillance » de volant de détails d’une stratégie de surveillance avec l’adresse de boîte aux lettres de surveillance mis en surbrillance](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Étape 2 : Configurer la boîte aux lettres de contrôle d’accès du bureau d’Outlook

Ensuite, relecteurs vous devrez exécuter deux commandes Exchange Online PowerShell afin qu’ils peuvent connecter Outlook à la boîte aux lettres de surveillance.
  
1. Connexion à Exchange Online PowerShell. [Comment faire ceci ?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. Exécutez les commandes suivantes, où *SupervisoryReview{GUID}@domain.onmicrosoft.com* est l’adresse que vous avez copié à l’étape 1 ci-dessus et *utilisateur* est le nom du relecteur doivent se connecter à la boîte aux lettres de surveillance à l’étape 3.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. Attendez au moins une heure avant de passer à l’étape 3 ci-dessous.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Étape 3 : Créer un profil Outlook pour se connecter à la boîte aux lettres de surveillance

La dernière étape, relecteurs vous devrez créer un profil Outlook pour se connecter à la boîte aux lettres de surveillance.

> [!NOTE]
> Pour créer un nouveau profil Outlook, vous allez utiliser les paramètres de messagerie dans le panneau de configuration Windows. Le chemin d’accès que vous prenez pour accéder à ces paramètres peut-être dépendre d’un système d’exploitation Windows (Windows 7, Windows 8 ou Windows 10) que vous utilisez, et la version d’Outlook est installée.
  
1. Ouvrez le panneau de configuration, et dans la zone de **recherche** en haut de la fenêtre, tapez **Mail**.<br/>(Ne savez pas comment atteindre le panneau de configuration ? Voir [où est le panneau de configuration ?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. Ouvrez l’application de **messagerie** .

3. Dans la **Configuration de la messagerie - Outlook**, cliquez sur **Afficher les profils**.<br/>![La « configuration de la messagerie - Outlook' boîte de dialogue avec le bouton Afficher les profils en surbrillance](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. Dans la **messagerie**, cliquez sur **Ajouter**. Puis, dans le **Nouveau profil**, entrez un nom pour la boîte aux lettres de surveillance (par exemple, **surveillance**).<br/>![La boîte de dialogue « Nouveau profil » l’affichage du nom « Surveillance » dans la zone Nom du profil](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. Dans **Outlook de se connecter à Office 365**, cliquez sur **se connecter à un autre compte**.<br/>![Le message « Outlook de se connecter à Office 365 » avec le lien « Se connecter à un autre compte » en surbrillance](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Dans la **Configuration de compte automatique**, sélectionnez **configuration manuelle ou types de serveurs supplémentaires**, puis cliquez sur **suivant**.

7. **Sélectionnez votre Type de compte**, choisissez **Office 365**. Puis, dans la zone **Adresse de messagerie** , entrez l’adresse de la boîte aux lettres de surveillance que vous avez copié précédemment.<br/>![La page « Choisir votre propre Type de compte de la boîte de dialogue Ajouter un compte dans Outlook affiche la boîte de « Adresse de messagerie » mise en surbrillance.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Lorsque vous y êtes invité, entrez vos informations d’identification d’Office 365.

9. Si elle réussit, vous verrez le **surveillance - \<nom de la stratégie\> ** dossier répertorié dans la vue liste des dossiers dans Outlook.

## <a name="powershell-reference"></a>Référence de PowerShell

Si nécessaire, vous pouvez créer et gérer les stratégies de surveillance à l’aide des applets de commande PowerShell suivantes :

- [Nouvelle SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [Set-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [Nouvelle SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [Get-SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [Get-SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)