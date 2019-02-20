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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: ConFigurez des stratégies de vérification de surveillance pour capturer les communications des employés à des fins de révision.
ms.openlocfilehash: dee9f21d4b88338a092a64538cca33b41cc481c4
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090956"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Configurer des stratégies de surveillance pour votre organisation

Utilisez des stratégies de surveillance pour capturer les communications des employés à des fins d'examen par des relecteurs internes ou externes. Pour plus d'informations sur la façon dont les stratégies de surveillance peuvent vous aider à surveiller les communications au sein de votre organisation, consultez la rubrique [surveillance des stratégies dans Office 365](supervision-policies.md).

> [!NOTE]
> Les utilisateurs surveillés par des stratégies de surveillance doivent disposer d'une licence Office 365 entreprise E3 avec le complément de conformité avancé ou être inclus dans un abonnement Office 365 entreprise E5. Si vous ne disposez pas d'un plan entreprise E5 existant et que vous souhaitez essayer de contrôler, vous pouvez vous [inscrire pour obtenir une version d'évaluation d'Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
Procédez comme suit pour configurer et utiliser la surveillance dans votre organisation Office 365:
  
- **Étape 1 (facultatif)** - [configurer des groupes pour la surveillance](configure-supervision-policies.md#exampledist)

    Avant de commencer à utiliser la surveillance, déterminez qui aura ses communications et qui effectueront ces révisions. Si vous souhaitez commencer avec quelques utilisateurs seulement pour voir le fonctionnement de la surveillance, vous pouvez ignorer la configuration des groupes pour le moment.

- **Étape 2 (obligatoire)** - [rendez la surveillance disponible dans votre organisation](configure-supervision-policies.md#MakeAvailable)

    Ajoutez-vous au groupe de rôles examen de surveillance afin de pouvoir configurer des stratégies. Tous les utilisateurs auxquels ce rôle est attribué peuvent accéder à la page **surveillance** sous **gouvernance des données** dans le centre de sécurité & Compliance Center. Si le courrier électronique à vérifier est hébergé sur Exchange Online, chaque réviseur doit également disposer [d'un accès à PowerShell à distance à Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

- **Étape 3 (facultatif)** - [configurer des types d'informations sensibles personnalisés ou des dictionnaires/lexiques de mots clés personnalisés](configure-supervision-policies.md#sensitiveinfo)

    Si vous devez utiliser un type d'informations sensibles personnalisé ou un dictionnaire de mots clés personnalisé pour votre stratégie de surveillance, vous devez le créer avant de démarrer l'Assistant surveillance.

- **Étape 4 (obligatoire)** - [configurer une stratégie de surveillance](configure-supervision-policies.md#setupsuper)

    Vous allez créer des stratégies de surveillance dans le centre de sécurité & Compliance Center. Ces stratégies définissent les communications qui font l'objet d'un examen dans votre organisation et spécifie qui doit effectuer des révisions. Les communications incluent le courrier électronique et les communications Microsoft Teams, ainsi que les communications de plateformes tierces (par exemple, Facebook, Twitter, etc.)

- **Étape 5-(facultatif)** [Tester votre nouvelle stratégie de surveillance](configure-supervision-policies.md#TestPolicy)

    Le test de votre stratégie de surveillance pour vous assurer qu'elle fonctionne comme vous le souhaitez est une partie importante de la façon de s'assurer que votre stratégie de conformité répond à vos normes.

- **Étape 6-(facultatif)** [Configurer le complément Outlook pour les relecteurs qui ne souhaitent pas utiliser le tableau de bord de surveillance Office 365 ou OWA pour consulter les communications surveillées](configure-supervision-policies.md#UseOutlook)

    Le complément de supervision pour Outlook accorde aux réviseurs l'accès à la fonctionnalité de surveillance directement dans le client Outlook afin qu'ils puissent évaluer et catégoriser chaque élément.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>Étape 1: configurer des groupes pour la surveillance (facultatif)

 Lorsque vous créez une stratégie de surveillance, vous déterminez les personnes auxquelles les communications seront vérifiées et qui effectueront ces révisions. Dans la stratégie, vous utiliserez des adresses de messagerie pour identifier des individus ou des groupes de personnes. Pour simplifier votre configuration, créez des groupes pour les personnes dont la communication est vérifiée et les groupes pour les personnes qui examineront ces communications. Si vous utilisez des groupes, vous aurez peut-être besoin de plusieurs, par exemple, si vous souhaitez surveiller les communications entre deux groupes distincts de personnes ou si vous souhaitez spécifier un groupe qui n'est pas supervisé. Pour plus d'informations sur le fonctionnement, consultez l' [exemple de groupes de distribution](configure-supervision-policies.md#GroupExample) .
  
Pour superviser les communications entre les groupes de votre organisation ou au sein de celle-ci, configurez **** \> des groupes de distribution dans le centre d'administration Exchange (accédez à **groupes**de destinataires). Pour plus d'informations sur la configuration des groupes de distribution, consultez la rubrique [Manage distribution Groups](http://go.microsoft.com/fwlink/?LinkId=613635) .
  
> [!NOTE]
> Vous pouvez également utiliser des groupes de distribution dynamique ou des groupes de sécurité pour la supervision si vous le souhaitez. Pour vous aider à déterminer si cela correspond mieux aux besoins de votre organisation, consultez la rubrique [gérer les groupes de sécurité à extension messagerie](http://go.microsoft.com/fwlink/?LinkId=627033)et [gérer les groupes de distribution dynamique](http://go.microsoft.com/fwlink/?LinkId=627058).
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>Exemple de groupes de distribution

Cet exemple inclut un groupe de distribution qui a été configuré pour une organisation financière appelée Contoso Financial international.
  
Chez Contoso Financial International, un échantillonnage des communications entre les courtiers aux États-Unis doit être effectué. Toutefois, les responsables de la mise en conformité au sein de ce groupe ne doivent pas être surveillés. Dans cet exemple, nous pouvons créer les groupes suivants :
  
|**Configuration de ce groupe de distribution**|**Adresse de groupe (alias)**|**Description**|
|:-----|:-----|:-----|
|Tous les courtiers des États-Unis | US_Brokers@Contoso.com | Ce groupe contient les adresses de messagerie de tous les courtiers basés aux États-Unis qui travaillent pour Contoso. |
| Tous les responsables de la mise en conformité des États-Unis | US_Compliance@Contoso.com  | Ce groupe inclut des adresses de messagerie pour tous les responsables de la mise en conformité américains qui travaillent pour contoso. Étant donné que ce groupe est un sous-ensemble de tous les courtiers basés aux États-Unis, vous pouvez utiliser cet alias pour exempter les responsables de la conformité d'une stratégie de surveillance. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>Étape 2-faire en sorte que la supervision soit disponible dans votre organisation (obligatoire)

Pour que la **surveillance** soit disponible sous la forme d'une option de menu dans le centre de sécurité & conformité, vous devez disposer du rôle d'administrateur examen de surveillance.
  
Pour ce faire, vous pouvez vous ajouter en tant que membre du groupe de rôles examen de surveillance ou créer un nouveau groupe de rôles.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Ajouter des membres au groupe de rôles examen de surveillance

1. Connectez- [https://protection.office.com](https://protection.office.com) vous à l'aide des informations d'identification d'un compte d'administrateur dans votre organisation Office 365.

2. Dans le centre de sécurité & conformité, accédez à **autorisations**.

3. Sélectionnez le groupe de rôles **examen de surveillance** , puis cliquez sur l'icône modifier.

4. Dans la section **membres** , ajoutez les personnes dont vous souhaitez gérer la surveillance pour votre organisation.

### <a name="create-a-new-role-group"></a>Créer un groupe de rôles

1. Connectez- [https://protection.office.com](https://protection.office.com) vous à l'aide des informations d'identification d'un compte d'administrateur dans votre organisation Office 365.

2. Dans le centre de sécurité & conformité, accédez à **autorisations** , puis cliquez sur**+** ajouter ().

3. Dans la section **rôles** , cliquez sur Ajouter**+**() et faites défiler vers le bas jusqu'à administrateur de la **vérification de surveillance**. Ajoutez ce rôle au groupe de rôles.

4. Dans la section **membres** , ajoutez les personnes dont vous souhaitez gérer la surveillance pour votre organisation.

Pour plus d'informations sur les groupes de rôles et les autorisations, consultez [la rubrique &amp; autorisations dans le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>Activer l'accès à PowerShell à distance pour les relecteurs (si le courrier électronique est hébergé sur Exchange Online)

1. Suivez les instructions [pour activer ou désactiver l'accès à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>Étape 3-créer des types d'informations sensibles personnalisés ou des dictionnaires personnels de mots clés personnalisés (facultatif)

Pour sélectionner des types d'informations sensibles personnalisés ou des dictionnaires personnels de mots clés personnalisés dans l'Assistant stratégie de surveillance, vous devez d'abord créer ces éléments si nécessaire.

### <a name="create-custom-sensitive-information-types"></a>Créer des types d'informations sensibles personnalisés

1. Créez un nouveau type d'informations sensibles dans le centre de sécurité & de la sécurité d'Office 365. Naviguez **** \> jusqu'à types d' **informations sensibles** sur les classifications et suivez les étapes de l' **Assistant Nouveau type d'informations sensibles**. Ici, vous allez:

    - Définir un nom et une description pour le type d'informations sensibles
    - Définir les éléments de proximité, de niveau de confiance et de modèle principal
    - Vérifier vos sélections et créer le type d'informations sensibles

    Pour plus d'informations, consultez [la rubrique créer un type d'informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).

### <a name="create-custom-keyword-dictionarylexicon"></a>Créer un dictionnaire/Lexique de mots clés personnalisé

1. À l'aide d'un éditeur de texte (comme le bloc-notes), créez un nouveau fichier incluant les termes de mots clés que vous souhaitez surveiller dans une stratégie de surveillance. Assurez-vous que chaque terme se trouve sur une ligne distincte et enregistrez le fichier au format **Unicode/UTF-16 (Little endian)** .
2. ImPortez le fichier de mots clés dans votre client Office 365 à l'aide de PowerShell. Pour vous connecter à Office 365 avec PowerShell, consultez [la rubrique Connect to office 365 Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

    Une fois que vous êtes connecté à Office 365 avec PowerShell, exécutez les commandes suivantes pour importer votre dictionnaire de mots clés:

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    Pour plus d'informations, consultez [la rubrique créer un dictionnaire de mots clés](create-a-keyword-dictionary.md).

3. Créez un nouveau type d'informations sensibles dans le centre de sécurité & de la sécurité d'Office 365. Naviguez **** \> jusqu'à types d' **informations sensibles** sur les classifications et suivez les étapes de l' **Assistant Nouveau type d'informations sensibles**. Ici, vous allez:

    - Définir un nom et une description pour le type d'informations sensibles
    - Ajouter votre dictionnaire personnalisé comme condition requise pour l'élément correspondant
    - Vérifier vos sélections et créer le type d'informations sensibles

    Une fois le dictionnaire/lexique personnalisé créé, vous pouvez afficher les mots clés configurés à l'aide de la cmdlet [Get-dlpkeyworddictionary permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) ou ajouter et supprimer des termes à l'aide de la cmdlet [Set-dlpkeyworddictionary permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) .

    Pour plus d'informations, consultez [la rubrique créer un type d'informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>Étape 4: configurer une stratégie de surveillance (obligatoire)
  
1. Connectez- [https://protection.office.com](https://protection.office.com) vous à l'aide des informations d'identification d'un compte d'administrateur dans votre organisation Office 365.

2. Dans le centre de sécurité & Compliance Center, sélectionnez **supervision**.
  
3. Sélectionnez **créer** , puis suivez l'Assistant pour configurer les pages suivantes de la stratégie. À l'aide de l'Assistant, vous allez:

    - Donnez un nom et une description à la stratégie.
    - Choisissez les utilisateurs ou les groupes à superviser, y compris le choix des utilisateurs ou des groupes que vous souhaitez exclure.
    - Définir les conditions de la stratégie de surveillance.
    - Choisissez si vous souhaitez inclure des types d'informations sensibles. C'est ici que vous pouvez sélectionner les types d'informations sensibles par défaut et personnalisés.
    - Définir le pourcentage de communications à réviser.
    - Choisissez les relecteurs de la stratégie. Les relecteurs peuvent être des utilisateurs individuels ou des [groupes de sécurité à extension messagerie](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group).
    - Examinez vos sélections de stratégie et créez la stratégie.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>Étape 5: test de votre stratégie de supervision (facultatif)

Une fois que vous avez créé une stratégie de surveillance, il est recommandé de tester les conditions que vous avez définies de façon appropriée. Vous pouvez également [tester vos stratégies de protection contre la perte de données (DLP)](create-test-tune-dlp-policy.md) si vos stratégies de surveillance incluent des types d'informations sensibles. Suivez les étapes ci-dessous pour tester votre stratégie de surveillance:

1. Ouvrez un client de messagerie ou Microsoft teams connecté en tant qu'utilisateur supervisé défini dans la stratégie que vous souhaitez tester.
2. Envoyez un message électronique ou une conversation Microsoft teams qui répond aux critères que vous avez définis dans la stratégie de supervision. Il peut s'agir d'un mot clé, d'une taille de pièce jointe, d'un domaine, etc. Assurez-vous de déterminer si vos paramètres conditionnels configurés dans la stratégie sont trop restrictifs ou trop stricts.

    > [!Note]
    > Les E-mails soumis à des stratégies définies sont traités en temps réel et peuvent être testés immédiatement après la configuration de la stratégie. Les conversations dans Microsoft teams peuvent prendre jusqu'à 24 heures pour être entièrement traitées dans une stratégie. 

3. Connectez-vous à votre client Office 365 en tant que réviseur désigné dans la stratégie de supervision. Accédez à **surveillance** > de*votre stratégie* > **** personnalisée pour afficher le rapport de la stratégie.

<a name="UseOutlook"> </a>

## <a name="step-6---set-up-outlook-add-in-for-reviewers-optional"></a>Étape 6: configurer le complément Outlook pour les relecteurs (facultatif)

Les relecteurs qui souhaitent utiliser Outlook au lieu d'utiliser le tableau de bord de supervision dans Office 365 ou Outlook sur le Web pour examiner les communications doivent installer le complément de supervision pour leur client Outlook.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Étape 1: Copiez l'adresse de la boîte aux lettres de supervision

Pour installer le complément pour le bureau Outlook, vous aurez besoin de l'adresse de la boîte aux lettres de surveillance créée dans le cadre de la configuration de la stratégie de supervision.
  
> [!NOTE]
> Si une autre personne a créé la stratégie, vous devez obtenir cette adresse auprès de celle-ci pour installer le complément.

 **Pour Rechercher l'adresse de la boîte aux lettres de supervision**
  
1. Connectez-vous [au &amp; Centre de sécurité conformité](https://protection.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation Office 365.

2. Accédez à **surveillance**.

3. Cliquez sur la stratégie de surveillance qui rassemble les communications que vous souhaitez examiner.

4. Dans la fenêtre mobile détails de la stratégie, sous **boîte aux lettres de supervision**, copiez l'adresse.<br/>![La section «boîte aux lettres de surveillance» d'une fenêtre de détails de la stratégie de supervision indiquant l'adresse de la supervision sélectionnée](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Étape 2: configuration de la boîte aux lettres de supervision pour l'accès Bureau à Outlook

Ensuite, les relecteurs doivent exécuter des commandes PowerShell Exchange Online pour pouvoir connecter Outlook à la boîte aux lettres de supervision.
  
1. Connectez-vous à Exchange Online PowerShell. [Comment procéder?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. Exécutez les commandes suivantes, où *SupervisoryReview {GUID} @domain. onmicrosoft.com* est l'adresse que vous avez copiée à l'étape 1 ci-dessus, et *utilisateur* est le nom du réviseur qui se connectera à la boîte aux lettres de supervision à l'étape 3.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. Patientez au moins une heure avant de passer à l'étape 3 ci-dessous.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Étape 3: créer un profil Outlook pour se connecter à la boîte aux lettres de supervision

Pour la dernière étape, les relecteurs devront créer un profil Outlook pour se connecter à la boîte aux lettres de supervision.

> [!NOTE]
> Pour créer un nouveau profil Outlook, vous devez utiliser les paramètres de messagerie dans le panneau de configuration de Windows. Le chemin d'accès à ces paramètres peut dépendre du système d'exploitation Windows (Windows 7, Windows 8 ou Windows 10) que vous utilisez et de la version d'Outlook installée.
  
1. Ouvrez le panneau de configuration et, dans la zone de **recherche** en haut de la fenêtre, tapez **courrier**.<br/>(Vous ne savez pas comment accéder au panneau de configuration? Voir [où est le panneau de configuration?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)
  
2. Ouvrez l'application de **messagerie** .

3. Dans **configuration de la messagerie-Outlook**, cliquez sur **afficher les profils**.<br/>![Boîte de dialogue «Configuration de la messagerie-Outlook» avec le bouton «afficher les profils» mis en évidence](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. Dans **courrier**, cliquez sur **Ajouter**. Ensuite, dans **nouveau profil**, entrez un nom pour la boîte aux lettres de supervision (par exemple, **surveillance**).<br/>![Boîte de dialogue «Nouveau profil» affichant le nom «surveillance» dans la zone «Nom du profil»](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. Dans **connecter Outlook à Office 365**, cliquez sur **se connecter à un autre compte**.<br/>![Message «connexion d'Outlook à Office 365» avec le lien «se connecter à un autre compte» mis en surbrillance](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Dans **configuration de compte automatique**, choisissez **installation manuelle ou types de serveurs supplémentaires**, puis cliquez sur **suivant**.

7. Dans **choisir votre type de compte**, choisissez **Office 365**. Ensuite, dans la zone **adresse de messagerie** , entrez l'adresse de la boîte aux lettres de supervision que vous avez copiée précédemment.<br/>![La page «Choisissez votre type de compte» de la boîte de dialogue «Ajouter un compte» dans Outlook affichant la case «adresse de messagerie» en surbrillance.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Lorsque vous y êtes invité, entrez vos informations d'identification Office 365.

9. Si elle réussit, vous verrez le dossier ** \<surveillance\> -nom** de la stratégie répertorié dans la liste des dossiers dans Outlook.

## <a name="powershell-reference"></a>Référence PowerShell

Si nécessaire, vous pouvez créer et gérer des stratégies de surveillance à l'aide des applets de commande PowerShell suivantes:

- [New-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [Get-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [Set-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [Remove-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [Get-SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [Get-SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)