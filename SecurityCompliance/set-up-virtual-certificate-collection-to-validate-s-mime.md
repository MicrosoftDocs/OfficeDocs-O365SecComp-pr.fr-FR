---
title: Configurer la collection de certificats virtuels dans Exchange Online pour valider S/MIME
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: Les administrateurs peuvent apprendre à créer une collection de certificats virtuels qui sera utilisée pour valider les certificats S/MIME dans Exchange Online.
ms.openlocfilehash: 15998bce1971952286d8dd4401a92f1e9e47c25d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693553"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a><span data-ttu-id="278de-103">Configurer la collection de certificats virtuels dans Exchange Online pour valider S/MIME</span><span class="sxs-lookup"><span data-stu-id="278de-103">Set up virtual certificate collection in Exchange Online to validate S/MIME</span></span>

<span data-ttu-id="278de-104">En tant qu'administrateur, vous devrez configurer une collection de certificats virtuels dans Exchange Online qui sera utilisée pour valider les certificats S/MIME.</span><span class="sxs-lookup"><span data-stu-id="278de-104">As an admin, you will need to configure a virtual certificate collection in Exchange Online that will be used to validate S/MIME certificates.</span></span> <span data-ttu-id="278de-105">Cette collection de certificats virtuels est configurée en tant que magasin de certificats avec une extension de nom de fichier SST.</span><span class="sxs-lookup"><span data-stu-id="278de-105">This virtual certificate collection is set up as a certificate store with an SST filename extension.</span></span> <span data-ttu-id="278de-106">Le fichier SST contient tous les certificats racine et intermédiaires utilisés lors de la validation d’un certificat S/MIME.</span><span class="sxs-lookup"><span data-stu-id="278de-106">The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>

## <a name="create-and-save-an-sst"></a><span data-ttu-id="278de-107">Créer et enregistrer un fichier SST</span><span class="sxs-lookup"><span data-stu-id="278de-107">Create and save an SST</span></span>

<span data-ttu-id="278de-108">Vous pouvez créer ce fichier de magasin de certificats SST en exportant les certificats à partir d'un ordinateur approuvé à l'aide de la cmdlet **Export-certificat** dans Windows PowerShell et en spécifiant la valeur de _type_ SST.</span><span class="sxs-lookup"><span data-stu-id="278de-108">You can create this SST certificate store file by exporting the certificates from a trusted machine using the **Export-Certificate** cmdlet in Windows PowerShell and specifying the _Type_ value as SST.</span></span> <span data-ttu-id="278de-109">Pour obtenir des instructions, consultez la rubrique [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span><span class="sxs-lookup"><span data-stu-id="278de-109">For instructions, see [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span></span>

<span data-ttu-id="278de-110">Une fois que vous avez le fichier de magasin de certificats SST, utilisez la syntaxe suivante dans Exchange Online PowerShell pour enregistrer le contenu du fichier SST dans le magasin de certificats virtuels Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="278de-110">Once you have the SST certificate store file, use the following syntax in Exchange Online PowerShell to save the SST file contents in the Exchange Online virtual certificate store.</span></span> <span data-ttu-id="278de-111">Pour vous connecter à Exchange Online PowerShell, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="278de-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

<span data-ttu-id="278de-112">Cet exemple importe le fichier SST C:\My Documents\exported Rules Certificate Store. SST.</span><span class="sxs-lookup"><span data-stu-id="278de-112">This example imports the SST file C:\My Documents\Exported Certificate Store.sst.</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

<span data-ttu-id="278de-113">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).</span><span class="sxs-lookup"><span data-stu-id="278de-113">For detailed syntax and parameter information, see [Set-SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).</span></span>

## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="278de-114">S’assurer de la validité d’un certificat</span><span class="sxs-lookup"><span data-stu-id="278de-114">Ensuring a certificate is valid</span></span>

<span data-ttu-id="278de-115">Dans Exchange Online, seul le service SST est utilisé pour la validation des certificats.</span><span class="sxs-lookup"><span data-stu-id="278de-115">In Exchange Online, only the SST is used for certificate validation.</span></span>

## <a name="more-information"></a><span data-ttu-id="278de-116">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="278de-116">More Information</span></span>

[<span data-ttu-id="278de-117">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="278de-117">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

[<span data-ttu-id="278de-118">Get-SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="278de-118">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
