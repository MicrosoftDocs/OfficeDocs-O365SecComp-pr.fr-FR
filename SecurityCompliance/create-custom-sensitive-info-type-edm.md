---
title: Créer un type d’informations sensibles personnalisé à l’aide d’une correspondance exacte des données
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 05/15/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Créer un type d’informations sensibles personnalisé à l’aide d’une classification basée sur la correspondance exacte des données.
ms.openlocfilehash: 3b15bf0197918d6bbc3897f9fa578c40b70d3f4e
ms.sourcegitcommit: 4eb4ca899adcf4d86501530f875eb49af8cdaeb7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2019
ms.locfileid: "34083187"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification-preview"></a><span data-ttu-id="77c1d-103">Créer un type d’informations sensibles personnalisé à l’aide d’une correspondance exacte des données (préversion)</span><span class="sxs-lookup"><span data-stu-id="77c1d-103">See Create a custom sensitive information type with Exact Data Match based classification (Preview).</span></span>

## <a name="overview"></a><span data-ttu-id="77c1d-104">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="77c1d-104">Overview</span></span>

<span data-ttu-id="77c1d-105">[Les types d’informations sensibles personnalisés](custom-sensitive-info-types.md) sont utilisés pour empêcher le partage involontaire ou inapproprié d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="77c1d-105">[Custom sensitive information types](custom-sensitive-info-types.md) are used to help prevent inadvertent or inappropriate sharing of sensitive information.</span></span> <span data-ttu-id="77c1d-106">En tant qu’administrateur, vous pouvez utiliser [le centre de sécurité & conformité ](create-a-custom-sensitive-information-type.md)ou[PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) pour définir un type d’informations sensibles personnalisé basé sur des modèles, des preuves (Mots clés tels que *employé*, *badge*,*ID*,etc.),proximité des caractères(comment les preuves sont proches des caractères dans un modèle particulier) et des niveaux de confiance.</span><span class="sxs-lookup"><span data-stu-id="77c1d-106">As an administrator, you can use the [Security & Compliance Center](create-a-custom-sensitive-information-type.md) or [PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) to define a custom sensitive information type based on patterns, evidence (keywords such as *employee*, *badge*, *ID*, and so on), character proximity (how close evidence is to characters in a particular pattern), and confidence levels.</span></span> <span data-ttu-id="77c1d-107">De tels types d’informations sensibles personnalisés répondent aux besoins professionnels de nombreuses organisations.</span><span class="sxs-lookup"><span data-stu-id="77c1d-107">Such custom sensitive information types meet business needs for many organizations.</span></span>

<span data-ttu-id="77c1d-108">Mais que se passe-t-il si vous voulez utiliser un type d’informations sensibles personnalisé qui utilise des valeurs de données exactes au lieu de modèles et de proximité?</span><span class="sxs-lookup"><span data-stu-id="77c1d-108">But what if you wanted a custom sensitive information type that uses exact data values, instead of patterns and proximity?</span></span> <span data-ttu-id="77c1d-109">Avec une classification de correspondance de données exacte (EDM), vous pouvez créer un type d’informations sensibles personnalisé conçu pour:</span><span class="sxs-lookup"><span data-stu-id="77c1d-109">With Exact Data Match (EDM)-based classification, you can create a custom sensitive information type that is designed to:</span></span>
- <span data-ttu-id="77c1d-110">être dynamique et actualisable ;</span><span class="sxs-lookup"><span data-stu-id="77c1d-110">be dynamic and refreshable;</span></span>
- <span data-ttu-id="77c1d-111">être plus évolutif ;</span><span class="sxs-lookup"><span data-stu-id="77c1d-111">be more scalable;</span></span>
- <span data-ttu-id="77c1d-112">entraîner moins de faux positifs ;</span><span class="sxs-lookup"><span data-stu-id="77c1d-112">result in fewer false-positives;</span></span>
- <span data-ttu-id="77c1d-113">utiliser des données sensibles structurées ;</span><span class="sxs-lookup"><span data-stu-id="77c1d-113">work with structured sensitive data;</span></span>
- <span data-ttu-id="77c1d-114">gérer les informations sensibles de façon plus sécurisée, et</span><span class="sxs-lookup"><span data-stu-id="77c1d-114">handle sensitive information more securely; and</span></span>
- <span data-ttu-id="77c1d-115">être utilisé avec plusieurs services de cloud computing de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77c1d-115">be used with several Microsoft cloud services.</span></span>

![Classification basée sur EDM](media/EDMClassification.png)

<span data-ttu-id="77c1d-117">La classification basée sur EDM vous permet de créer des types d’informations sensibles personnalisés qui font référence à des valeurs exactes dans une base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="77c1d-117">EDM-based classification enables you to create custom sensitive information types that refer to exact values in a database of sensitive information.</span></span> <span data-ttu-id="77c1d-118">La base de données peut être actualisée quotidiennement ou hebdomadairement, et peut contenir jusqu’à 10 millions lignes de données.</span><span class="sxs-lookup"><span data-stu-id="77c1d-118">The database can be refreshed daily or weekly, and it can contain up to 10 million rows of data.</span></span> <span data-ttu-id="77c1d-119">À mesure que les employés, patients ou clients arrivent et changent, et que les enregistrements changent, vos types d’informations sensibles personnalisés restent à jour et applicables.</span><span class="sxs-lookup"><span data-stu-id="77c1d-119">So as employees, patients, or clients come and go, and records change, your custom sensitive information types remain current and applicable.</span></span> <span data-ttu-id="77c1d-120">Vous pouvez également utiliser la classification basée sur EDM avec des stratégies, telles [que les stratégies de protection contre la perte de données](data-loss-prevention-policies.md) (DLP) ou [les stratégies de fichier de Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span><span class="sxs-lookup"><span data-stu-id="77c1d-120">And, you can use EDM-based classification with policies, such as [data loss prevention policies](data-loss-prevention-policies.md) (DLP) or [Microsoft Cloud App Security file policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="77c1d-121">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="77c1d-121">Required licenses and permissions</span></span>

- <span data-ttu-id="77c1d-122">Vous devez être un administrateur général, un administrateur de conformité ou un administrateur Exchange Online pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="77c1d-122">You must be a global admin, compliance administrator, or Exchange Online administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="77c1d-123">Pour en avoir plus sur les autorisations DLP, consultez la section[Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="77c1d-123">To learn more about DLP permissions, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

- <span data-ttu-id="77c1d-124">Lorsque la classification basée sur EDM est généralement disponible, elle est incluse dans les abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="77c1d-124">When generally available, EDM-based classification will be included in the following subscriptions:</span></span>
    - <span data-ttu-id="77c1d-125">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="77c1d-125">Office 365 Enterprise E5</span></span>
    - <span data-ttu-id="77c1d-126">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="77c1d-126">Microsoft 365 E5</span></span>
    - <span data-ttu-id="77c1d-127">Conformité et protection des informations Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="77c1d-127">Microsoft 365 Information Protection and Compliance</span></span>
    - <span data-ttu-id="77c1d-128">Conformité avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="77c1d-128">Office 365 Advanced Compliance</span></span>

> [!NOTE]
> <span data-ttu-id="77c1d-129">**La classification basée sur EDM est actuellement en préversion** pour [DLP dans Office 365](data-loss-prevention-policies.md) (avec Exchange Online et Microsoft Teams) et la [sécurité des applications Cloud](https://docs.microsoft.com/cloud-app-security).</span><span class="sxs-lookup"><span data-stu-id="77c1d-129">**EDM-based classification is currently in preview** for [DLP in Office 365](data-loss-prevention-policies.md) (with Exchange Online and Microsoft Teams) and [Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span></span> <span data-ttu-id="77c1d-130">Si votre organisation dispose [de fonctionnalités DLP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc#data-loss-prevention-dlp), vous pouvez essayer la classification basée sur EDM.</span><span class="sxs-lookup"><span data-stu-id="77c1d-130">If your organization has [DLP capabilities](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc#data-loss-prevention-dlp), you can try EDM-based classification.</span></span> <span data-ttu-id="77c1d-131">Si vous ne participez pas déjà à la préversion[, contactez Microsoft](https://resources.office.com/us-landing-spe-contactus.html?LCID=EN-US) pour commencer.</span><span class="sxs-lookup"><span data-stu-id="77c1d-131">If you are not already participating in the preview, [contact Microsoft](https://resources.office.com/us-landing-spe-contactus.html?LCID=EN-US) to get started.</span></span> 

## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="77c1d-132">Flux de travail en un clin d’œil</span><span class="sxs-lookup"><span data-stu-id="77c1d-132">The work flow at a glance</span></span>

|<span data-ttu-id="77c1d-133">Phase</span><span class="sxs-lookup"><span data-stu-id="77c1d-133">Phase</span></span>  |<span data-ttu-id="77c1d-134">De quoi ai-je besoin ?</span><span class="sxs-lookup"><span data-stu-id="77c1d-134">What's needed</span></span>  |
|---------|---------|
|[<span data-ttu-id="77c1d-135">Partie 1: configurer la classification basée sur EDM</span><span class="sxs-lookup"><span data-stu-id="77c1d-135">Part 1: Set up EDM-based classification</span></span>](#part-1-set-up-edm-based-classification)<br/><br/><span data-ttu-id="77c1d-136">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="77c1d-136">(As needed)</span></span><br/><span data-ttu-id="77c1d-137">- [Modifier le schéma de base de données](#editing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="77c1d-137">- [Edit the database schema](#editing-the-schema-for-edm-based-classification)</span></span> <br/><span data-ttu-id="77c1d-138">- [Supprimer le schéma](#removing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="77c1d-138">- [Remove the schema](#removing-the-schema-for-edm-based-classification)</span></span> |<span data-ttu-id="77c1d-139">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-139">- Read access to the sensitive data</span></span><br/><span data-ttu-id="77c1d-140">-Schéma de base de données au format. XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="77c1d-140">- Database schema in .xml format (example provided)</span></span><br/><span data-ttu-id="77c1d-141">-Package de règles au format. XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="77c1d-141">- Rule package in .xml format (example provided)</span></span><br/><span data-ttu-id="77c1d-142">-Autorisations d’administrateur sur le centre de sécurité & conformité (à l’aide de PowerShell)</span><span class="sxs-lookup"><span data-stu-id="77c1d-142">- Admin permissions to the Security & Compliance Center (using PowerShell)</span></span> |
|[<span data-ttu-id="77c1d-143">Partie 2: indexer et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-143">Part 2: Index and upload the sensitive data</span></span>](#part-2-index-and-upload-the-sensitive-data)<br/><br/><span data-ttu-id="77c1d-144">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="77c1d-144">(As needed)</span></span><br/>[<span data-ttu-id="77c1d-145">Actualiser les données</span><span class="sxs-lookup"><span data-stu-id="77c1d-145">Refresh the data</span></span>](#refreshing-your-sensitive-information-database) |<span data-ttu-id="77c1d-146">-Groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="77c1d-146">- Custom security group and user account</span></span><br/><span data-ttu-id="77c1d-147">-Accès administrateur local à l’ordinateur à l’aide de l’agent de téléchargement EDM</span><span class="sxs-lookup"><span data-stu-id="77c1d-147">- Local admin access to machine with EDM Upload Agent</span></span><br/><span data-ttu-id="77c1d-148">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-148">- Read access to the sensitive data</span></span><br/><span data-ttu-id="77c1d-149">-Processus et planification pour l’actualisation des données</span><span class="sxs-lookup"><span data-stu-id="77c1d-149">- Process and schedule for refreshing the data</span></span>|
|[<span data-ttu-id="77c1d-150">Partie 3: utiliser la classification basée sur EDM avec vos services Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="77c1d-150">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |<span data-ttu-id="77c1d-151">-Abonnement Office 365 avec DLP</span><span class="sxs-lookup"><span data-stu-id="77c1d-151">- Office 365 subscription with DLP</span></span><br/><span data-ttu-id="77c1d-152">-Fonctionnalité de classification basée sur EDM activée (en préversion)</span><span class="sxs-lookup"><span data-stu-id="77c1d-152">- EDM-based classification feature enabled (in preview)</span></span> |

## <a name="part-1-set-up-edm-based-classification"></a><span data-ttu-id="77c1d-153">Partie 1: configurer la classification basée sur EDM</span><span class="sxs-lookup"><span data-stu-id="77c1d-153">Part 1: Set up EDM-based classification</span></span>

<span data-ttu-id="77c1d-154">La préparation et la configuration de la classification basée sur EDM impliquent d’enregistrer des données sensibles au format. csv, de définir un schéma pour votre base de données d’informations sensibles, de créer un package de règles, puis de télécharger le schéma et le package de règles.</span><span class="sxs-lookup"><span data-stu-id="77c1d-154">Setting up and configuring EDM-based classification involves saving sensitive data in .csv format, defining a schema for your database of sensitive information, creating a rule package, and then uploading the schema and rule package.</span></span>

### <a name="define-the-schema-for-your-database-of-sensitive-information"></a><span data-ttu-id="77c1d-155">Définir le schéma de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-155">Define the schema for your database of sensitive information</span></span>

1. <span data-ttu-id="77c1d-156">Identifier les informations sensibles que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="77c1d-156">Identify the KPIs that you want to use.</span></span> <span data-ttu-id="77c1d-157">Exporter les données vers une application, telle que Microsoft Excel, et enregistrez le fichier au format. csv.</span><span class="sxs-lookup"><span data-stu-id="77c1d-157">Export the data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="77c1d-158">Le fichier de données peut inclure les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="77c1d-158">The data file can include:</span></span>

    - <span data-ttu-id="77c1d-159">Jusqu’à 10 millions de lignes de données sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-159">Up to 10 million rows of sensitive data</span></span>
    - <span data-ttu-id="77c1d-160">Jusqu’à 32 colonnes (champs) par source de données</span><span class="sxs-lookup"><span data-stu-id="77c1d-160">Up to 32 columns (fields) per data source</span></span>

2. <span data-ttu-id="77c1d-161">Structurer les données sensibles dans le fichier. csv de telle sorte que la première ligne inclut les noms des champs utilisés pour la classification basée sur EDM.</span><span class="sxs-lookup"><span data-stu-id="77c1d-161">Structure the sensitive data in the .csv file such that the first row includes the names of the fields used for EDM-based classification.</span></span> <span data-ttu-id="77c1d-162">Votre fichier. csv contient peut-être des noms de champs, tels que «SSN», «BirthDate», «FirstName», «LastName», etc.</span><span class="sxs-lookup"><span data-stu-id="77c1d-162">In your .csv file, you might have field names, such as "ssn", "birthdate", "firstname", "lastname", and so on.</span></span> <span data-ttu-id="77c1d-163">Par exemple, le fichier. csv est appelé PatientRecords.csvet ses colonnes incluent PatientID, MRN, LastName, FirstName,*SSN*, etc.</span><span class="sxs-lookup"><span data-stu-id="77c1d-163">As an example, our .csv file is called *PatientRecords.csv*, and its columns include *PatientID*, *MRN*, *lastname*, *FirstName*, *SSN* and more.</span></span>

3. <span data-ttu-id="77c1d-164">Définissez le schéma pour la base de données d’informations sensibles au format. XML (comme dans l’exemple ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="77c1d-164">Define the schema for the database of sensitive information in .xml format (similar to our example below).</span></span> <span data-ttu-id="77c1d-165">Nommez ce fichier de schéma`edm.xml` et configurez-le de telle sorte que pour chaque colonne de la base de données, une ligne utilise la syntaxe`<Field name="" unique="" searchable=""/>`.</span><span class="sxs-lookup"><span data-stu-id="77c1d-165">Name this schema file `edm.xml`, and configure it such that for each column in the database, there is a line that uses the syntax `<Field name="" unique="" searchable=""/>`.</span></span> 

    - <span data-ttu-id="77c1d-166">Utilisez les noms de colonne pour les valeurs de *nom de champ*.</span><span class="sxs-lookup"><span data-stu-id="77c1d-166">Use column names for *Field name* values.</span></span>
    - <span data-ttu-id="77c1d-167">Utilisez *unique = "true"* pour les champs qui contiennent des valeurs uniques (numéros d’identification de sécurité sociale, numéros d’identification, etc. ). sinon, utilisez*unique = "false"*.</span><span class="sxs-lookup"><span data-stu-id="77c1d-167">Use *unique="true"* for the fields that contain unique values (Social Security numbers, identification numbers, etc.); otherwise, use *unique="false"*.</span></span>
    - <span data-ttu-id="77c1d-168">Utilisez *searchable="true"* pour les champs que vous voulez rechercher.</span><span class="sxs-lookup"><span data-stu-id="77c1d-168">Use *searchable="true"* for the fields that you want to be searchable.</span></span> <span data-ttu-id="77c1d-169">Ne précisez pas plus de cinq champs par base de données à rechercher.</span><span class="sxs-lookup"><span data-stu-id="77c1d-169">Do not specify more than five fields per database to be searchable.</span></span> <span data-ttu-id="77c1d-170">Tout le reste doit avoir *searchable="false"*.</span><span class="sxs-lookup"><span data-stu-id="77c1d-170">All the rest should have *searchable="false"*.</span></span>  

    <span data-ttu-id="77c1d-171">Par exemple, le fichier. xml suivant définit le schéma d’une base de données de dossiers de patients, avec cinq champs pouvant faire l’objet d’une recherche : *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span><span class="sxs-lookup"><span data-stu-id="77c1d-171">As an example, the following .xml file defines the schema for a patient records database, with five fields specified as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span> 
    
    <span data-ttu-id="77c1d-172">(Vous pouvez copier, modifier et utiliser notre exemple.)</span><span class="sxs-lookup"><span data-stu-id="77c1d-172">(You can copy, modify, and use our example.)</span></span>
    
    <span data-ttu-id="77c1d-173">\`\`\`<?xml version="1.0" encoding="utf-8"?> <EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm"></span><span class="sxs-lookup"><span data-stu-id="77c1d-173"></span></span>
        <span data-ttu-id="77c1d-174"><DataStore name="PatientRecords" description="Schéma pour les dossiers des patients</span><span class="sxs-lookup"><span data-stu-id="77c1d-174"><DataStore name="PatientRecords" description="Schema for patient records</span></span>" version="1">
            <span data-ttu-id="77c1d-175"><Field name="PatientID" unique="false" searchable="true" /> <Field name="MRN" unique="false" searchable="true" /></span><span class="sxs-lookup"><span data-stu-id="77c1d-175"></span></span>
            <Field name="FirstName" unique="false" searchable="false" />
            <Field name="LastName" unique="false" searchable="false" />
            <Field name="SSN" unique="false" searchable="true" />
            <Field name="Phone" unique="false" searchable="true" />
            <Field name="DOB" unique="false" searchable="true" />
            <Field name="Gender" unique="false" searchable="false" />
            <Field name="Address" unique="false" searchable="false" />
        </DataStore>
    </EdmSchema>
    ```

4. [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

5. To upload the database schema, run the following cmdlets, one at a time:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    You will be prompted to confirm, as follows:

       Confirm
       Are you sure you want to perform this action?
       New EDM Schema for the data store 'patientrecords' will be imported.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > If you want your changes to occur without confirmation, in Step 5, use this cmdlet instead: `New-DlpEdmSchema -FileData $edmSchemaXml`
    
Now that the schema for your database of sensitive information is defined, the next step is to set up a rule package. Proceed to the section [Set up a rule package](#set-up-a-rule-package).

#### Editing the schema for EDM-based classification 

(As needed) If you want to make changes to your edm.xml file, such as changing which fields are used for EDM-based classification, follow these steps:

1. Edit your edm.mxl file (this is the file discussed in the [Define the schema](#define-the-schema-for-your-database-of-sensitive-information) section of this article).

2. [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

3. To update your database schema, run the following cmdlets, one at a time:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    You will be prompted to confirm, as follows:

       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be updated.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > If you want your changes to occur without confirmation, in Step 3, use this cmdlet instead: `Set-DlpEdmSchema -FileData $edmSchemaXml`

#### Removing the schema for EDM-based classification

(As needed) If you want to remove the schema you're using for EDM-based classification, follow these steps:

1. [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

2. Run the following PowerShell cmdlet, substituting the data store name of "patientrecords" with the one you want to remove:

    `Remove-DlpEdmSchema -Identity patientrecords`

     You will be prompted to confirm, as follows:
    
       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be removed.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):
    
    > [!TIP]
    > If you want your changes to occur without confirmation, in Step 2, use this cmdlet instead: `Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false`

### Set up a rule package

1. Create a rule package in .xml format (with Unicode encoding), similar to the following example. (You can copy, modify, and use our example.) 

   Recall from the previous procedure that our PatientRecords schema defines five fields as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*. Our example rule package includes those fields and references the database schema file (edm.xml), with one *ExactMatch* items per searchable field. Consider the following ExactMatch item:

   ```
    <span data-ttu-id="77c1d-176"><ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" > <Pattern confidenceLevel="65"> <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" /> </Pattern> </ExactMatch></span><span class="sxs-lookup"><span data-stu-id="77c1d-176"></span></span>
   ```

    In this example, note the following:

    - The dataStore name references the .csv file we created earlier: **dataStore = "PatientRecords"**.
    - The idMatch value references a searchable field that is listed in the database schema file: **idMatch matches = "SSN"**.
    - The classification value references an existing or custom sensitive information type: **classification = "U.S. Social Security Number (SSN)"**. (In this case, we use the existing sensitive information type of U.S. Social Security Number.)

    When you set up your rule package, make sure to correctly reference your .csv file and edm.xml file. (You can copy, modify, and use our example.) 

    ```<?xml version="1.0" encoding="utf-8"?>
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
    
2. <span data-ttu-id="77c1d-177">Téléchargez le package de règles en exécutant les applets de commande PowerShell suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="77c1d-177">Upload the rule package by running the following PowerShell cmdlets, one at a time:</span></span>

    `$rulepack=Get-Content .\rulepack.xml -Encoding Byte -ReadCount 0`

    `New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack`

<span data-ttu-id="77c1d-178">À ce stade, vous avez configuré la classification basée sur EDM.</span><span class="sxs-lookup"><span data-stu-id="77c1d-178">At this point, you have set up EDM-based classification.</span></span> <span data-ttu-id="77c1d-179">L’étape suivante consiste à indexer les données sensibles, puis à télécharger les données indexées.</span><span class="sxs-lookup"><span data-stu-id="77c1d-179">The next step is to index the sensitive data, and then upload the indexed data.</span></span> 

## <a name="part-2-index-and-upload-the-sensitive-data"></a><span data-ttu-id="77c1d-180">Partie 2: indexer et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-180">Part 2: Index and upload the sensitive data</span></span>

<span data-ttu-id="77c1d-181">Au cours de cette phase, vous configurez un groupe de sécurité personnalisé et un compte d’utilisateur, et configurez l’outil de chargement de l’agent EDM.</span><span class="sxs-lookup"><span data-stu-id="77c1d-181">During this phase, you set up a custom security group and user account, and set up the EDM Upload Agent tool.</span></span> <span data-ttu-id="77c1d-182">Utilisez ensuite l’outil pour indexer les données sensibles, puis à télécharger les données indexées.</span><span class="sxs-lookup"><span data-stu-id="77c1d-182">Then, you use the tool to index the sensitive data, and upload the indexed data.</span></span>

### <a name="set-up-the-security-group-and-user-account"></a><span data-ttu-id="77c1d-183">Configurer le groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="77c1d-183">Set up the security group and user account</span></span>

1. <span data-ttu-id="77c1d-184">En tant qu’administrateur général, accédez au centre d’administration ([https://admin.microsoft.com](https://admin.microsoft.com)) et [créez un groupe de sécurité appelé`EDM_DataUploaders`.</span><span class="sxs-lookup"><span data-stu-id="77c1d-184">As a global administrator, go to the admin center ([https://admin.microsoft.com](https://admin.microsoft.com)) and [create a security group](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) called `EDM_DataUploaders`.</span></span> 

2. <span data-ttu-id="77c1d-185">Ajoutez un ou plusieurs utilisateurs au groupe de sécurité*EDM_DataUploaders*.</span><span class="sxs-lookup"><span data-stu-id="77c1d-185">Add one or more users to the *EDM_DataUploaders* security group.</span></span> <span data-ttu-id="77c1d-186">(Ces utilisateurs peuvent gérer la base de données d’informations sensibles.)</span><span class="sxs-lookup"><span data-stu-id="77c1d-186">(These users will manage the database of sensitive information.)</span></span>

3. <span data-ttu-id="77c1d-187">Assurez-vous que tous les utilisateurs qui gèrent les données sensibles sont un administrateur local sur l’ordinateur utilisé pour l’agent de téléchargement EDM.</span><span class="sxs-lookup"><span data-stu-id="77c1d-187">Make sure each user who is managing the sensitive data is a local admin on the machine used for the EDM Upload Agent.</span></span>

### <a name="set-up-the-edm-upload-agent"></a><span data-ttu-id="77c1d-188">Configurer l’agent de téléchargement EDM</span><span class="sxs-lookup"><span data-stu-id="77c1d-188">Set up the EDM Upload Agent</span></span>

> [!NOTE]
> <span data-ttu-id="77c1d-189">Avant de commencer cette procédure, assurez-vous que vous êtes membre du groupe de sécurité *EDM_DataUploaders* et administrateur local sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="77c1d-189">Before you begin this procedure, make sure that you are a member of the *EDM_DataUploaders* security group and a local admin on your machine.</span></span>

1. <span data-ttu-id="77c1d-190">Téléchargez et installez l’agent EDM de chargement sur [https://go.microsoft.com/fwlink/?linkid=2088639](https://go.microsoft.com/fwlink/?linkid=2088639).</span><span class="sxs-lookup"><span data-stu-id="77c1d-190">Download and install the EDM Upload Agent at [https://go.microsoft.com/fwlink/?linkid=2088639](https://go.microsoft.com/fwlink/?linkid=2088639).</span></span> <span data-ttu-id="77c1d-191">Par défaut, l’emplacement d’installation doit être`C:\Program Files\Microsoft\EdmUploadAgent`.</span><span class="sxs-lookup"><span data-stu-id="77c1d-191">By default, the installation location should be `C:\Program Files\Microsoft\EdmUploadAgent`.</span></span> 

2. <span data-ttu-id="77c1d-192">Pour autoriser l’agent de téléchargement EDM, ouvrez l’invite de commandes Windows (en tant qu’administrateur), puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="77c1d-192">To authorize the EDM Upload Agent, open Windows Command Prompt (as an administrator), and then run the following command:</span></span>

    `EdmUploadAgent.exe /Authorize`

3. <span data-ttu-id="77c1d-193">Connectez-vous à Office 365 à l'aide de votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="77c1d-193">Sign in to Office 365 for business with your work or school account.</span></span>

<span data-ttu-id="77c1d-194">L’étape suivante consiste à utiliser l’agent de téléchargement EDM pour indexer les données sensibles, puis à télécharger les données indexées.</span><span class="sxs-lookup"><span data-stu-id="77c1d-194">The next step is to use the EDM Upload Agent to index the sensitive data, and then upload the indexed data.</span></span>

### <a name="index-and-upload-the-sensitive-data"></a><span data-ttu-id="77c1d-195">Indexer et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-195">Index and upload the sensitive data</span></span>

1. <span data-ttu-id="77c1d-196">Enregistrez le fichier de données sensibles (notre exemple est *PatientRecords. csv*) sur le disque local sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="77c1d-196">Save the sensitive data file (recall our example is *PatientRecords.csv*) to the local drive on the machine.</span></span> <span data-ttu-id="77c1d-197">(Nous avons enregistré notre exemple de fichier\*PatientRecords.csv dans.)</span><span class="sxs-lookup"><span data-stu-id="77c1d-197">(We saved our example *PatientRecords.csv* file to `C:\Edm\Data`.)</span></span>

2. <span data-ttu-id="77c1d-198">Pour indexer les données sensibles, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="77c1d-198">To index the sensitive data, run the following command in Windows Command Prompt:</span></span>

    `EdmUploadAgent.exe /CreateHash /DataStoreName <DataStoreName> /DataFile <DataFilePath> /HashLocation <HashedFileLocation>`

    <span data-ttu-id="77c1d-199">Example: **EdmUploadAgent.exe /CreateHash /DataStoreName PatientRecords /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash**</span><span class="sxs-lookup"><span data-stu-id="77c1d-199">Example: **EdmUploadAgent.exe /CreateHash /DataStoreName PatientRecords /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash**</span></span> 

3. <span data-ttu-id="77c1d-200">Pour charger les données indexées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="77c1d-200">To upload the indexed data, run the following command in Windows Command Prompt:</span></span>

    `EdmUploadAgent.exe /UploadHash /DataStoreName <DataStoreName> /HashFile <HashedSourceFilePath>`

    <span data-ttu-id="77c1d-201">Example: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\Edm\Hash\PatientRecords.EdmHash**</span><span class="sxs-lookup"><span data-stu-id="77c1d-201">Example: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\Edm\Hash\PatientRecords.EdmHash**</span></span> 

4. <span data-ttu-id="77c1d-202">Pour vérifier que vos données sensibles ont été téléchargées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="77c1d-202">To verify your sensitive data has been uploaded, run the following command in Windows Command Prompt:</span></span>

    `EdmUploadAgent.exe /GetDataStore`

    <span data-ttu-id="77c1d-203">La liste des magasins de données apparaît, ainsi que la date de la dernière mise à jour, comme suit :</span><span class="sxs-lookup"><span data-stu-id="77c1d-203">You'll see a list of data stores and when they were last updated, similar to the following:</span></span> <br/>![Exemple d’applet de commande GetDataStore et résultats](media/EDM-GetDataStore-example.png)

5. <span data-ttu-id="77c1d-205">Poursuivez la configuration de votre processus et planifiez l’[actualisation de votre base de données d'informations sensibles](#refreshing-your-sensitive-information-database).</span><span class="sxs-lookup"><span data-stu-id="77c1d-205">Proceed to set up your process and schedule for [Refreshing your sensitive information database](#refreshing-your-sensitive-information-database).</span></span>

<span data-ttu-id="77c1d-206">À ce stade, vous êtes prêt à utiliser la classification basée sur EDM avec vos services de Cloud Computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77c1d-206">At this point, you are ready to use EDM-based classification with your Microsoft cloud services.</span></span> <span data-ttu-id="77c1d-207">Par exemple, vous pouvez [configurer une stratégie DLP à l’aide d’une classification basée sur EDM](#to-create-a-dlp-policy-with-edm).</span><span class="sxs-lookup"><span data-stu-id="77c1d-207">For example, you can [set up a DLP policy using EDM-based classification](#to-create-a-dlp-policy-with-edm).</span></span> 

### <a name="refreshing-your-sensitive-information-database"></a><span data-ttu-id="77c1d-208">Actualisation de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="77c1d-208">Refreshing your sensitive information database</span></span>

<span data-ttu-id="77c1d-209">Vous pouvez actualiser quotidiennement ou hebdomadairement votre base de données d’informations sensibles, et l’outil de chargement EDM peut réindexer les données sensibles, puis recharger les données indexées.</span><span class="sxs-lookup"><span data-stu-id="77c1d-209">You can refresh your sensitive information database daily or weekly, and the EDM Upload Tool can reindex the sensitive data and then reupload the indexed data.</span></span> 

1. <span data-ttu-id="77c1d-210">Déterminez vos processus et leur fréquence (quotidien ou hebdomadaire) pour actualiser la base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="77c1d-210">Determine your process and frequency (daily or weekly) for refreshing the database of sensitive information.</span></span>

2. <span data-ttu-id="77c1d-211">Exporter de nouveau les données vers une application, telle que Microsoft Excel, et enregistrez le fichier au format. csv.</span><span class="sxs-lookup"><span data-stu-id="77c1d-211">Re-export the sensitive data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="77c1d-212">Conservez le même nom de fichier et l’emplacement que vous avez utilisé lorsque vous avez suivi les étapes décrites dans[indexez et téléchargez les données sensibles](#index-and-upload-the-sensitive-data).</span><span class="sxs-lookup"><span data-stu-id="77c1d-212">Keep the same file name and location you used when you followed the steps described in [Index and upload the sensitive data](#index-and-upload-the-sensitive-data).</span></span>

    > [!NOTE]
    > <span data-ttu-id="77c1d-213">S’il n’y a pas de modifications apportées à la structure (noms de champs) du fichier. csv, vous n’avez pas besoin d’apporter des modifications à votre fichier de schéma de base de données lorsque vous actualisez les données.</span><span class="sxs-lookup"><span data-stu-id="77c1d-213">If there are no changes to the structure (field names) of the .csv file, you won't need to make any changes to your database schema file when you refresh the data.</span></span> <span data-ttu-id="77c1d-214">Si vous devez apporter des modifications, assurez-vous de modifier le[schéma de base de données](#editing-the-schema-for-edm-based-classification) et votre [package de règles](#set-up-a-rule-package)en conséquence.</span><span class="sxs-lookup"><span data-stu-id="77c1d-214">But if you must make changes, make sure to edit the [database schema](#editing-the-schema-for-edm-based-classification) and your [rule package](#set-up-a-rule-package) accordingly.</span></span>        

3. <span data-ttu-id="77c1d-215">Utilisez [le planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) pour automatiser les étapes 2 et 3 dans la procédure[indexer et télécharger les données sensibles](#index-and-upload-the-sensitive-data).</span><span class="sxs-lookup"><span data-stu-id="77c1d-215">Use [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) to automate steps 2 and 3 in the [Index and upload the sensitive data](#index-and-upload-the-sensitive-data) procedure.</span></span> <span data-ttu-id="77c1d-216">Vous pouvez planifier des tâches à l’aide de plusieurs méthodes :</span><span class="sxs-lookup"><span data-stu-id="77c1d-216">You can schedule tasks using several methods:</span></span>
    
    |<span data-ttu-id="77c1d-217">Méthode</span><span class="sxs-lookup"><span data-stu-id="77c1d-217">Method</span></span>  |<span data-ttu-id="77c1d-218">Procédure</span><span class="sxs-lookup"><span data-stu-id="77c1d-218">What to do</span></span>  |
    |---------|---------|
    |<span data-ttu-id="77c1d-219">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="77c1d-219">Windows PowerShell</span></span>     |<span data-ttu-id="77c1d-220">Consultez la documentation[ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) et l’[exemple de script PowerShell](#example-powershell-script-for-task-scheduler) dans cet article</span><span class="sxs-lookup"><span data-stu-id="77c1d-220">See the [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) documentation and the [example PowerShell script](#example-powershell-script-for-task-scheduler) in this article</span></span>|
    |<span data-ttu-id="77c1d-221">API planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="77c1d-221">Task Scheduler API</span></span> |<span data-ttu-id="77c1d-222">Consultez la documentation relative au [planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler)</span><span class="sxs-lookup"><span data-stu-id="77c1d-222">See the [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) documentation</span></span> |
    |<span data-ttu-id="77c1d-223">Interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="77c1d-223">Windows user interface</span></span>     |<span data-ttu-id="77c1d-224">Dans Windows, cliquez sur **Démarrer**, puis tapez`Task Scheduler`.</span><span class="sxs-lookup"><span data-stu-id="77c1d-224">In Windows, click **Start**, and type `Task Scheduler`.</span></span> <span data-ttu-id="77c1d-225">Dans la liste des résultats, cliquez avec le bouton droit sur**planificateur de tâches**, puis sélectionnez**exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-225">Then, in the list of results, right-click **Task Scheduler**, and choose **Run as administrator**.</span></span>          |

#### <a name="example-powershell-script-for-task-scheduler"></a><span data-ttu-id="77c1d-226">Exemple de script PowerShell pour le planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="77c1d-226">Example PowerShell script for Task Scheduler</span></span>

<span data-ttu-id="77c1d-227">Cette section inclut un exemple de script PowerShell que vous pouvez utiliser pour planifier vos tâches d’indexation et de chargement des données indexées :</span><span class="sxs-lookup"><span data-stu-id="77c1d-227">This section includes an example PowerShell script you can use to schedule your tasks for indexing data and uploading the indexed data:</span></span>

```powershell
param([string]$dataStoreName,[string]$fileLocation)
# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\$env:USERNAME"
$edminstallpath = 'C:\Program Files\Microsoft\EdmUploadAgent\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\$dataStoreName$csvext"
$hashFile = "$fileLocation\$dataStoreName$edmext"
# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=[Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($creds.Password))
# Register the scheduled task
$taskName = 'EDMUpload_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```
## <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a><span data-ttu-id="77c1d-228">Partie 3: utiliser la classification basée sur EDM avec vos services de cloud computing Microsoft</span><span class="sxs-lookup"><span data-stu-id="77c1d-228">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>

<span data-ttu-id="77c1d-229">Vous pouvez également utiliser la classification basée sur EDM avec des fonctionnalités de protection d’informations, telles que les [stratégies Office 365 DLP](data-loss-prevention-policies.md) ou [les stratégies de fichier Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span><span class="sxs-lookup"><span data-stu-id="77c1d-229">You can use EDM-based classification with information protection features, such as [Office 365 DLP policies](data-loss-prevention-policies.md) and [Microsoft Cloud App Security file policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span></span> <span data-ttu-id="77c1d-230">La procédure suivante explique comment utiliser EDM avec une stratégie DLP créée dans le centre de sécurité & conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="77c1d-230">The following procedure describes how to use EDM with a DLP policy that is created in the Office 365 Security & Compliance Center.</span></span>

### <a name="to-create-a-dlp-policy-with-edm"></a><span data-ttu-id="77c1d-231">Pour créer une stratégie DLP avec EDM</span><span class="sxs-lookup"><span data-stu-id="77c1d-231">To create a DLP policy with EDM</span></span>

1. <span data-ttu-id="77c1d-232">Accédez au centre de sécurité & conformité ([https://protection.office.com](https://protection.office.com)).</span><span class="sxs-lookup"><span data-stu-id="77c1d-232">Go to the Security & Compliance Center</span></span>

2. <span data-ttu-id="77c1d-233">Cliquez sur **Protection contre la perte de données** > **(Stratégie)**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-233">Click **Data loss prevention** > **Policy**.</span></span>

3. <span data-ttu-id="77c1d-234">Sélectionnez créer une stratégie\*\* > **personnaliser** > \*\*suivant.</span><span class="sxs-lookup"><span data-stu-id="77c1d-234">Choose **Create a policy** > **Custom** > **Next**.</span></span>

4. <span data-ttu-id="77c1d-235">Sous l'onglet**Nommez votre stratégie**, spécifiez un nom et une description, puis sélectionnez**suivant**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-235">On the **Name your policy** tab, specify a name and description, and then choose **Next**.</span></span>

5. <span data-ttu-id="77c1d-236">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-236">On the **Choose locations** tab, select **Let me choose specific locations**, and then choose **Next**.</span></span><br/><span data-ttu-id="77c1d-237">![Option choisir les emplacements](media/DLP-EDM-newpolicy-chooselocations.png)</span><span class="sxs-lookup"><span data-stu-id="77c1d-237">![Choose locations option](media/DLP-EDM-newpolicy-chooselocations.png)</span></span><br/>

6. <span data-ttu-id="77c1d-238">Dans la colonne**État**, sélectionnez **courrier Exchange** uniquement, puis**suivant**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-238">In the **Status** column, select **Exchange email** only, and then choose **Next**.</span></span> <br/><span data-ttu-id="77c1d-239">![Stratégie EDM avec Exchange uniquement](media/EDM-DLPpolicy-ExchangeOnly.png)</span><span class="sxs-lookup"><span data-stu-id="77c1d-239">![EDM policy with Exchange only](media/EDM-DLPpolicy-ExchangeOnly.png)</span></span><br/>

7. <span data-ttu-id="77c1d-240">Sous l'onglet**paramètres de stratégie**, sélectionnez**utiliser les paramètres avancés**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-240">On the **Policy settings** tab, choose **Use advanced settings**, and then choose **Next**.</span></span><br/><span data-ttu-id="77c1d-241">![Utiliser les paramètres avancés](media/edm-dlp-policy-advancedsettings.png)</span><span class="sxs-lookup"><span data-stu-id="77c1d-241">![Use advanced settings](media/edm-dlp-policy-advancedsettings.png)</span></span><br/>

8. <span data-ttu-id="77c1d-242">Sélectionnez **+ Nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-242">Choose **+ New rule**.</span></span><br/><span data-ttu-id="77c1d-243">![Créer une règle](media/edm-dlp-newrule.png)</span><span class="sxs-lookup"><span data-stu-id="77c1d-243">![Create a crawl rule</span></span><br/>

9. <span data-ttu-id="77c1d-244">Dans la section**Nom**, spécifiez un nom et une description pour la règle.</span><span class="sxs-lookup"><span data-stu-id="77c1d-244">Use the **Name and Description** section to specify a name and description for the category.</span></span><br/><span data-ttu-id="77c1d-245">![Champs nouvelle règle](media/edm-dlp-newruleform.png)</span><span class="sxs-lookup"><span data-stu-id="77c1d-245">![New rule fields](media/edm-dlp-newruleform.png)</span></span><br/>

10. <span data-ttu-id="77c1d-246">Dans la section**conditions**, dans la liste **+ ajouter une condition**, sélectionnez **le contenu contient un type de contenu sensible**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-246">In the **Conditions** section, in the **+ Add a condition** list, choose **Content contains sensitive type**.</span></span><br/><span data-ttu-id="77c1d-247">![Le contenu contient des types d’informations sensibles](media/edm-dlp-newrule-conditions.png)</span><span class="sxs-lookup"><span data-stu-id="77c1d-247">![Content contains sensitive info types](media/edm-dlp-newrule-conditions.png)</span></span><br/>

11. <span data-ttu-id="77c1d-248">Recherchez le type d’informations sensibles que vous avez créé lorsque vous avez configuré votre package de règles, puis sélectionnez **+ ajouter**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-248">Search for the sensitive information type you created when you set up your rule package, and then choose **+ Add**.</span></span><br/><span data-ttu-id="77c1d-249">![Rechercher le type d’informations sensibles](media/edm-dlp-newrulefindsensitiverulepack.png)</span><span class="sxs-lookup"><span data-stu-id="77c1d-249">![Find the sensitive info type](media/edm-dlp-newrulefindsensitiverulepack.png)</span></span><br/><span data-ttu-id="77c1d-250">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-250">Then choose **Done**.</span></span>

12. <span data-ttu-id="77c1d-251">Terminez de sélectionner les options de votre règle, telles que**notifications d’utilisateur**,**remplacements d’utilisateur**, **rapports d’incident**, puis sélectionnez\*\* Enregistrer\*\*.</span><span class="sxs-lookup"><span data-stu-id="77c1d-251">Finish selecting options for your rule, such as **User notifications**, **User overrides**, **Incident reports**, and so on, and then choose **Save**.</span></span>

13. <span data-ttu-id="77c1d-252">Sous l'onglet **paramètres de stratégie**, passez en revue vos règles, puis sélectionnez**suivant**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-252">On the **Policy settings** tab, review your rules, and then choose **Next**.</span></span>

14. <span data-ttu-id="77c1d-253">Indiquez si vous voulez activer la stratégie immédiatement, tester celle-ci ou la maintenir désactivée.</span><span class="sxs-lookup"><span data-stu-id="77c1d-253">Specify whether to turn on the policy right away, test it out, or keep it turned off.</span></span> <span data-ttu-id="77c1d-254">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-254">Then choose **Next**.</span></span>

15. <span data-ttu-id="77c1d-255">Sous l'onglet **Vérifier vos paramètres**, passez en revue votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="77c1d-255">On the **Review your settings** tab, review your policy.</span></span> <span data-ttu-id="77c1d-256">Apportez les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="77c1d-256">Make any needed changes.</span></span> <span data-ttu-id="77c1d-257">Lorsque vous avez terminé, sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="77c1d-257">When you're ready, choose **Create**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="77c1d-258">Laissez environ une heure pour que votre nouvelle stratégie DLP fonctionne de la même manière dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="77c1d-258">Allow approximately one hour for your new DLP policy to work its way through your data center.</span></span>

## <a name="related-articles"></a><span data-ttu-id="77c1d-259">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="77c1d-259">Related articles</span></span>

[<span data-ttu-id="77c1d-260">Obtenir la liste des types d’informations sensibles intégrés et ce qu’ils recherchent</span><span class="sxs-lookup"><span data-stu-id="77c1d-260">Built-in sensitive information types and what they look for</span></span>](what-the-sensitive-information-types-look-for.md)

[<span data-ttu-id="77c1d-261">Types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="77c1d-261">Custom sensitive information types</span></span>](custom-sensitive-info-types.md)

[<span data-ttu-id="77c1d-262">Vue d’ensemble des stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="77c1d-262">Overview of DLP policies</span></span>](data-loss-prevention-policies.md)

[<span data-ttu-id="77c1d-263">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="77c1d-263">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)
