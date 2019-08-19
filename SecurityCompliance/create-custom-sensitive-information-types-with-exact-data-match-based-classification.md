---
title: Créer des types d’informations sensibles personnalisés à l’aide du classifieur Exact Data Match
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Créer des types d’informations sensibles personnalisés à l’aide d’une classification Exact Data Match.
ms.openlocfilehash: a937d5ccc947ee9322c5796cf49e9a8ff3eead16
ms.sourcegitcommit: d4acce11a26536b9d6ca71ba4933fc95136198a4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/15/2019
ms.locfileid: "36407906"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification"></a>Créez des types d’informations sensibles personnalisés à l’aide d’une classification Exact Data Match.

## <a name="overview"></a>Vue d’ensemble

Les [types d’informations sensibles personnalisés](https://docs.microsoft.com/fr-FR/office365/securitycompliance/custom-sensitive-info-types)  vous aident à empêcher le partage involontaire ou inapproprié d’informations sensibles. En tant qu’administrateur, vous pouvez utiliser le  [Centre de sécurité et conformité](https://docs.microsoft.com/fr-FR/office365/securitycompliance/create-a-custom-sensitive-information-type)  ou  [PowerShell](https://docs.microsoft.com/fr-FR/office365/securitycompliance/create-a-custom-sensitive-information-type-in-scc-powershell)  pour définir un type d’informations sensibles personnalisé basé sur des modèles, des preuves (mots clés tels que  *employé*,  *badge*,  *ID*, etc.), la proximité de caractère (dans un modèle particulier) et des niveaux de confiance. De tels types d’informations sensibles personnalisés répondent aux besoins métier de nombreuses organisations.

Mais que se passe-t-il si vous voulez utiliser un type d’informations sensibles personnalisé qui utilise des valeurs de données exactes au lieu d’établir une concordance avec des modèles génériques ? Une classification Exact Data Match (EDM) vous permet de créer un type d’informations sensibles personnalisé conçu pour :

- être dynamique et actualisable ;
- être plus évolutif ;
- entraîner moins de faux positifs ;
- utiliser des données sensibles structurées ;
- gérer les informations sensibles de façon plus sécurisée, et
- être utilisé avec plusieurs services de cloud computing de Microsoft.

![Classification EDM](media/EDMClassification.png)

La classification EDM vous permet de créer des types d’informations sensibles personnalisés qui font référence à des valeurs exactes dans une base de données d’informations sensibles. La base de données peut être actualisée quotidiennement ou hebdomadairement, et peut contenir jusqu’à 10 millions lignes de données. À mesure que des employés, patients ou clients vont et viennent, et que les enregistrements changent, vos types d’informations sensibles personnalisés restent à jour et valides. Vous pouvez également utiliser une classification EDM avec des stratégies, par exemple, de  [protection contre la perte de données](https://docs.microsoft.com/fr-FR/office365/securitycompliance/data-loss-prevention-policies)  (DLP) ou les stratégies de fichier de  [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies).

## <a name="required-licenses-and-permissions"></a>Licences et autorisations requises

Pour effectuer les tâches décrites dans cet article, vous devez être un administrateur général, un administrateur de conformité ou un administrateur Exchange Online. Pour en avoir plus sur les autorisations DLP, voir  [Autorisations](https://docs.microsoft.com/fr-FR/office365/securitycompliance/data-loss-prevention-policies#permissions).

Dès qu’elle généralement disponible, la classification EDM sera incluse dans les abonnements suivants

- Office 365 E5
- Microsoft 365 E5
- Conformité et protection des informations Microsoft 365
- Conformité avancée Office 365

## <a name="the-work-flow-at-a-glance"></a>Flux de travail en un clin d’œil

|Phase  |De quoi ai-je besoin ?  |
|---------|---------|
|[Partie 1: configurer la classification EDM](#part-1-set-up-edm-based-classification)<br/><br/>(selon vos besoins)<br/>- [Modifier le schéma de base de données](#editing-the-schema-for-edm-based-classification) <br/>- [Supprimer le schéma](#removing-the-schema-for-edm-based-classification) |-Accès en lecture aux données sensibles<br/>-Schéma de base de données au format. XML (fourni en exemple)<br/>-Package de règles au format. XML (fourni en exemple)<br/>-Autorisations d’administrateur sur le centre de sécurité & conformité (à l’aide de PowerShell) |
|[Partie 2: indexer et télécharger les données sensibles](#part-2-index-and-upload-the-sensitive-data)<br/><br/>(selon vos besoins)<br/>[Actualiser les données](#refreshing-your-sensitive-information-database) |-Groupe de sécurité personnalisé et compte d’utilisateur<br/>-Accès administrateur local à l’ordinateur à l’aide de l’agent de téléchargement EDM<br/>-Accès en lecture aux données sensibles<br/>-Processus et planification pour l’actualisation des données|
|[Partie 3: utiliser la classification EDM avec vos services Cloud Microsoft](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |- Abonnement Office 365 avec DLP<br/>- Fonctionnalité de classification EDM activée |

### <a name="part-1-set-up-edm-based-classification"></a>Partie 1 : configurer la classification EDM

La préparation et la configuration de la classification EDM impliquent d’enregistrer des données sensibles au format. csv, de définir un schéma pour votre base de données d’informations sensibles, de créer un package de règles, puis de télécharger le schéma et le package de règles.

#### <a name="define-the-schema-for-your-database-of-sensitive-information"></a>Définir le schéma de votre base de données d’informations sensibles

1. Identifiez les informations sensibles que vous voulez utiliser. Exportez les données vers une application, telle que Microsoft Excel, puis enregistrez le fichier au format. csv. Le fichier de données peut inclure au maximum :
      - 10 millions de lignes de données sensibles
      - 32 colonnes (champs) par source de données
      - 5 colonnes (champs) marquées comme pouvant faire l’objet d’une recherche

2. Structurez les données sensibles dans le fichier .csv de telle sorte que la première ligne contienne les noms des champs utilisés pour la classification EDM. Votre fichier .csv contient peut-être des noms de champs, tels que « ssn », « birthdate », « firstname », « lastname », etc. Par exemple, le fichier .csv est appelé  *PatientRecords.csv* et ses colonnes incluent  *PatientID*,  *MRN*,  *LastName*,  *FirstName*,  *SSN* , etc.

3. Définissez le schéma pour la base de données d’informations sensibles dans un fichier XML (comme dans l’exemple ci-dessous). Nommez ce fichier de schéma edm.xml, puis configurez-le de telle sorte que, pour chaque colonne dans la base de données, une ligne utilise la syntaxe \<Field name="" searchable=""/\>.

      - Utilisez des noms de colonne pour les valeurs  *Nom de champ* .
      - Utilisez  *searchable="true"*  pour jusqu’à 5 champs dont vous voulez qu’il puissent faire l’objet d’une recherche. Vous devez spécifier au moins un champ comme pouvant faire l’objet d’une recherche.

Par exemple, le fichier. xml suivant définit le schéma d’une base de données de dossiers de patients, avec cinq champs pouvant faire l’objet d’une recherche :  *PatientID*,  *MRN*,  *SSN*,  *Phone* et  *DOB*

(vous pouvez copier, modifier et utiliser notre exemple).

 ```xml
<EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
      <DataStore name="PatientRecords" description="Schema for patient records" version="1">
            <Field name="PatientID" searchable="true" />
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</EdmSchema>
```

4. [Connectez-vous au Centre de sécurité et conformité Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

5. Pour charger le schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :

```powershell
$edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
```

Vous êtes invité à confirmer comme suit :

> Confirmer
>
> Êtes-vous sûr de vouloir effectuer cette action ?
>
> Un nouveau schéma EDM pour le magasin de données « patientrecords » va être importé.
>
> \[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :

> [!TIP]
> Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 5, utilisez plutôt la cmdlet New-DlpEdmSchema -FileData $edmSchemaXml

> [!NOTE]
> La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes. Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.

À présent que le schéma de votre base de données d’informations sensibles est défini, l’étape suivante consiste à configurer un package de règles. Passez à la section  [Configurer un package de règles](#set-up-a-rule-package).

#### <a name="editing-the-schema-for-edm-based-classification"></a>Modification du schéma pour la classification EDM

Si vous souhaitez modifier votre fichier edm.xml, par exemple pour changer les champs utilisés pour la classification EDM, procédez comme suit :

1. Modifiez votre fichier edm.xml (présenté dans la section  [Définir le schéma](#define-the-schema-for-your-database-of-sensitive-information)  de cet article).

2. [Connectez-vous au Centre de sécurité et conformité Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

3. Pour mettre à jour votre schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :

```powershell
$edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
```

Vous êtes invité à confirmer comme suit :

> Confirmer
>
> Êtes-vous sûr de vouloir effectuer cette action ?
>
> Le schéma EDM pour le magasin de données « patientrecords » va être mis à jour.
>
> \[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :

> [!TIP]
> Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 3, utilisez plutôt la cmdlet Set-DlpEdmSchema -FileData $edmSchemaXml

> [!NOTE]
> La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes. Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.

## <a name="removing-the-schema-for-edm-based-classification"></a>Suppression du schéma pour la classification EDM

(Le cas échéant) Si vous voulez supprimer le schéma que vous utilisez pour la classification EDM, procédez comme suit :

1. [Connectez-vous au Centre de sécurité et conformité Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

2. Exécutez les cmdlets PowerShell suivantes, en remplaçant le nom de magasin de données « patientrecords » par celui que vous voulez supprimer :

```powershell
Remove-DlpEdmSchema -Identity patientrecords
```

Vous êtes invité à confirmer comme suit :

> Confirmer
>
> Êtes-vous sûr de vouloir effectuer cette action ?
>
> Le schéma EDM pour le magasin de données « patientrecords » va être supprimé.
>
> \[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :

> [!TIP]
>  Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 2, utilisez plutôt la cmdlet Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false

### <a name="set-up-a-rule-package"></a>Configurer un package de règles

1. Créez un package de règles dans un fichier .xml (avec codage Unicode) similaire à l’exemple suivant (vous pouvez copier, modifier et utiliser notre exemple).

Lorsque vous configurez votre package de règles, veillez à référencer correctement vos fichier .csv et edm.xml. Vous pouvez copier, modifier et utiliser notre exemple. Dans cet exemple de fichier xml, les champs suivants doivent être personnalisés pour créer votre type sensible d’EDM :

- 
  **RulePack id & ExactMatch id** : utilisez  [New-GUID](https://docs.microsoft.com/fr-FR/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6)  pour générer un GUID.

- **Datastore** : ce champ spécifie le magasin de données de recherche EDM à utiliser. Vous indiquez un nom de source de données ou un schéma EDM configuré.

- **idMatch** : ce champ pointe vers l’élément principal pour EDM.
  - Matches : spécifie le champ à utiliser dans la recherche exacte. Vous fournissez un nom de champ pouvant faire l’objet d’une recherche dans le schéma EDM pour le magasin de données.
  - Classification : ce champ spécifie la correspondance de type sensible qui déclenche la recherche EDM. Vous pouvez fournir le nom ou le GUID d’une classification personnalisée ou prédéfinie existante.

- **Match :** ce champ pointe vers d’autres preuves à proximité d’idMatch.
  - Matches : vous indiquez un nom de champ dans le schéma EDM pour DataStore.
- **Resource :** cette section spécifie le nom et la description du type sensible dans plusieurs paramètres régionaux.
  - idRef : fournissez un GUID pour ExactMatch id.
  - Name & Editing the schema descriptions : personnalisez en fonction des besoins.

```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2018/edm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b11">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care EDM Rulepack</Name>
        <Description>This rule package contains the EDM sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="100">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </ExactMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB371">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">EDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
```

1. Téléchargez le package de règles en exécutant les cmdlets PowerShell suivantes, l’une après l’autre :

```powershell
$rulepack=Get-Content .\\rulepack.xml -Encoding Byte -ReadCount 0
New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack
```

À ce stade, vous avez configuré la classification EDM. L’étape suivante consiste à indexer les données sensibles, puis à charger les données indexées.

Rappelez-vous que la procédure précédente de notre schéma PatientRecords définit cinq champs pouvant faire l’objet d’une recherche :  *PatientID*, *MRN*,  *SSN*,  *Phone* et  *DOB*. Notre exemple de package de règles inclut ces champs et référence le fichier de schéma de base de données (edm.xml), avec un seul élément  *ExactMatch*  par champ pouvant faire l’objet d’une recherche. Prenons l’élément ExactMatch suivant :

```xml
<ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="100">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </ExactMatch>
```

À partir de cet exemple, notez les points suivants :

- Le nom du magasin de données fait référence au fichier .csv que nous avons créé précédemment :  **dataStore = "PatientRecords"**.

- La valeur idMatch fait référence à un champ pouvant faire l’objet d’une recherche figurant dans le fichier de schéma de base de données:  **idMatch matches = "SSN"**.

- La valeur de classification fait référence à un type d’informations sensibles existant ou personnalisé :  **classification = "U.S. Social Security Number (SSN)"** (en l’occurrence, nous utilisons le type d’informations sensibles existant pour le numéro de sécurité sociale aux États-Unis).

> [!NOTE]
> La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes. Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.

### <a name="part-2-index-and-upload-the-sensitive-data"></a>Partie 2 : indexer et télécharger les données sensibles

Au cours de cette phase, vous configurez un groupe de sécurité personnalisé et un compte d’utilisateur, et configurez l’outil de chargement de l’agent EDM. Utilisez ensuite l’outil pour indexer les données sensibles, puis à télécharger les données indexées.

#### <a name="set-up-the-security-group-and-user-account"></a>Configurer les groupe de sécurité personnalisé et compte d’utilisateur

1. En tant qu’administrateur général, accédez au centre d’administration ([https://admin.microsoft.com](https://admin.microsoft.com/)) et  [créez un groupe de sécurité](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) nommé\_DataUploaders.

2. Ajoutez un ou plusieurs utilisateurs au groupe de sécurité  *EDM\_DataUploaders*  (ces utilisateurs peuvent gérer la base de données d’informations sensibles).

3. Assurez-vous que tous les utilisateurs qui gèrent les données sensibles sont un administrateur local sur l’ordinateur utilisé pour l’agent de téléchargement EDM.

#### <a name="set-up-the-edm-upload-agent"></a>Configurer l’agent de chargement EDM

>[!NOTE]
> Avant de commencer cette procédure, assurez-vous que vous êtes membre du groupe de sécurité  *EDM\_DataUploaders*  et administrateur local sur votre ordinateur.

1. Téléchargez et installez l’[agent EDM de chargement](https://go.microsoft.com/fwlink/?linkid=2088639). Par défaut, l’emplacement d’installation doit être C:\\Program Files\\Microsoft\\EdmUploadAgent.

2. Pour autoriser l’agent de téléchargement EDM, ouvrez l’invite de commandes Windows (en tant qu’administrateur), puis exécutez la commande suivante :

    `EdmUploadAgent.exe /Authorize`

3. Connectez-vous à Office 365 à l'aide de votre compte professionnel ou scolaire.

L’étape suivante consiste à utiliser l’agent de téléchargement EDM pour indexer les données sensibles, puis à télécharger les données indexées.

#### <a name="index-and-upload-the-sensitive-data"></a>Indexer et charger les données sensibles

Enregistrez le fichier de données sensibles (notre exemple est  *PatientRecords. csv*) sur le disque local de l’ordinateur (nous avons enregistré notre exemple de fichier  *PatientRecords.csv*  dans C:\\Edm\\Data).

Pour indexer et charger les données sensibles, exécutez la commande suivante dans l’invite de commandes Windows :

`EdmUploadAgent.exe /UploadData /DataStoreName \<DataStoreName\> /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

Exemple : **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\\Edm\\Hash\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**

Pour séparer et exécuter un index de données sensibles dans un environnement isolé, exécutez les étapes d’indexation et de téléchargement séparément.

Pour indexer les données sensibles, exécutez la commande suivante dans l’invite de commandes Windows :

`EdmUploadAgent.exe /CreateHash /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

Exemple : **EdmUploadAgent.exe /CreateHash /DataFile C:\\Edm\\Data\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**

Pour charger les données indexées, exécutez la commande suivante dans l’invite de commandes Windows :

`EdmUploadAgent.exe /UploadHash /DataStoreName \<DataStoreName\> /HashFile \<HashedSourceFilePath\>`

Exemple : **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**

Pour vérifier que vos données sensibles ont été téléchargées, exécutez la commande suivante dans l’invite de commandes Windows :

`EdmUploadAgent.exe /GetDataStore`

La liste des magasins de données apparaît, ainsi que la date de la dernière mise à jour, comme suit :

Poursuivez la configuration de votre processus et planifiez l’ [actualisation de votre base de données d’informations sensibles](#refreshing-your-sensitive-information-database).

À ce stade, vous êtes prêt à utiliser la classification EDM avec vos services de Cloud Computing Microsoft. Par exemple, vous pouvez  [configurer une stratégie DLP à l’aide d’une classification EDM](#to-create-a-dlp-policy-with-edm).

#### <a name="refreshing-your-sensitive-information-database"></a>Actualisation de votre base de données d’informations sensibles

Vous pouvez actualiser quotidiennement ou hebdomadairement votre base de données d’informations sensibles, et l’outil de chargement EDM peut réindexer les données sensibles, puis recharger les données indexées.

1. Déterminez vos processus et leur fréquence (quotidien ou hebdomadaire) pour actualiser la base de données d’informations sensibles.

2. Exportez de nouveau les données vers une application, telle que Microsoft Excel, et enregistrez le fichier au format. csv. Conservez le même nom de fichier et l’emplacement que vous avez utilisé lorsque vous avez suivi les étapes décrites dans  [Indexer et charger les données sensibles](#index-and-upload-the-sensitive-data).

> [!NOTE]
> S’il n’y a pas de modifications apportées à la structure (noms de champs) du fichier .csv, vous n’avez pas besoin d’apporter des modifications à votre fichier de schéma de base de données lorsque vous actualisez les données. Si vous devez apporter des modifications, assurez-vous de modifier le schéma de base de données et votre package de règles en conséquence.

3. Utilisez le  [Planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page)  pour automatiser les étapes 2 et 3 dans la procédure  [Indexer et charger les données sensibles](#index-and-upload-the-sensitive-data) . Vous pouvez planifier des tâches à l’aide de plusieurs méthodes :

| **Méthode**             | **Procédure**                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Windows PowerShell     | Voir la documentation  [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps)  et l’ [exemple de script PowerShell](#example-powershell-script-for-task-scheduler)  dans cet article |
| API Planificateur de tâches     | Consultez la documentation relative au  [Planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler)                                                                                                                                                                                                                                                                                 |
| Interface utilisateur Windows | Dans Windows, cliquez sur  **Démarrer**, puis tapez Planificateur de tâches. Dans la liste des résultats, cliquez avec le bouton droit sur  **Planificateur de tâches**, puis sélectionnez  **Exécuter en tant qu’administrateur**.                                                                                                                                                                                                                                                                           |

#### <a name="example-powershell-script-for-task-scheduler"></a>Exemple de script PowerShell pour le planificateur de tâches

Cette section inclut un exemple de script PowerShell que vous pouvez utiliser pour planifier vos tâches d’indexation et de chargement des données indexées :

##### <a name="to-schedule-index-and-upload-in-a-combined-step"></a>Pour planifier un index et le charger dans une étape combinée

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$uploadDataArgs = '/UploadData /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ‘ /HashLocation’ + $hashLocation
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadDataArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```

#### <a name="to-schedule-index-and-upload-as-separate-steps"></a>Pour planifier un index et le charger en tant qu’étapes distinctes

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
$hashFile = "$fileLocation\\$dataStoreName$edmext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash' + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```

### <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a>Partie 3 : utiliser la classification EDM avec vos services de cloud computing Microsoft

Les stratégies DLP Office 365 pour Exchange Online (e-mail), OneDrive Entreprise (fichiers), Microsoft Teams (conversations) et DLP Microsoft Cloud App Security prendront en charge les types d’informations sensibles EDM.

Les types d’informations sensibles EDM pour les scénarios suivants sont en cours de développement, mais pas encore disponibles :

- DLP Office 365 pour SharePoint (fichiers)
- Classification automatique des étiquettes de confidentialité et étiquettes de rétention

#### <a name="to-create-a-dlp-policy-with-edm"></a>Pour créer une stratégie DLP avec EDM

1. Accédez au Centre de sécurité et conformité ([https://protection.office.com](https://protection.office.com/)).

2. Cliquez sur  **Protection contre la perte de données** \> **Stratégie**.

3. Sélectionnez  **Créer une stratégie** \> **Personnaliser** \> **Suivant**.

4. Sous l’onglet  **Nommez votre stratégie** , spécifiez un nom et une description, puis sélectionnez  **Suivant**.

5. Dans le volet  **Choisir des emplacements** , sélectionnez  **Me laisser choisir des emplacements spécifiques**, puis cliquez sur  **Suivant**.

6. Dans la colonne  **État** , sélectionnez  **courrier Exchange, Comptes OneDrive, Messages de conversation et de canal de Teams** , puis  **Suivant** (EDM n’est actuellement pas pris en charge dans les sites SharePoint et la stratégie DLP ne détecte pas les fichiers dans SharePoint pour EDM).

7. Sous l’onglet  **Paramètres de stratégie** , sélectionnez  **Utiliser les paramètres avancés**, puis  **Suivant**.

8. Sélectionnez  **+ Nouvelle règle**.

9. Dans la section **Nom** , spécifiez un nom et une description pour la règle.

10. Dans la section  **Conditions** , dans la liste  **+ Ajouter une condition** , sélectionnez  **Le contenu contient un type sensible**.<br/>![Le contenu contient des types d’informations sensibles](media/edm-dlp-newrule-conditions.png)<br/>

11. Recherchez le type d’informations sensibles que vous avez créé lorsque vous avez configuré votre package de règles, puis sélectionnez  **+ Ajouter**.  
    Ensuite, sélectionnez  **Terminé**.

12. Achevez de sélectionner les options applicables à votre règle, telles que  **Notifications à l’utilisateur**, **Remplacements par l’utilisateur**,  **Rapports d’incident** et autres, puis sélectionnez **Enregistrer**.

13. Sous l’onglet  **Paramètres de stratégie** , examinez vos règles, puis sélectionnez  **Suivant**.

14. Indiquez si vous voulez activer la stratégie immédiatement, la tester ou la maintenir désactivée. Ensuite, choisissez  **Suivant**.

15. Sous l’onglet  **Examiner vos paramètres** , révisez votre stratégie. Apportez les modifications nécessaires. Lorsque vous avez terminé, sélectionnez  **Créer**.

> [!NOTE]
> Comptez environ une heure avant que votre nouvelle stratégie DLP soit appliquée à l’ensemble de votre centre de données.

## <a name="related-articles"></a>Articles connexes


  [Obtenir la liste des types d’informations sensibles intégrés et ce qu’ils recherchent](https://docs.microsoft.com/fr-FR/office365/securitycompliance/what-the-sensitive-information-types-look-for)


  [Types d’informations sensibles personnalisés](https://docs.microsoft.com/fr-FR/office365/securitycompliance/custom-sensitive-info-types)


  [Vue d’ensemble des stratégies DLP](https://docs.microsoft.com/fr-FR/office365/securitycompliance/data-loss-prevention-policies)

[Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)


  [New-DlpEdmSchema](https://docs.microsoft.com/fr-FR/powershell/module/exchange/policy-and-compliance-dlp/new-dlpedmschema?view=exchange-ps)

## <a name="feedback"></a>Commentaires
Les commentaires sur GitHub sont activés, mais l’ajout de problèmes n’est possible que sur le site public.
