---
title: Configuration d'une collection de certificats virtuelle pour la validation des certificats S/MIME
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: s un administrateur client vous devrez configurer une collection de certificats virtuels qui sera utilisée pour valider les certificats S/MIME.
ms.openlocfilehash: 0e8226ca35e872cd8c7da16ba353bf8b99a6954d
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091056"
---
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a><span data-ttu-id="a7bb6-103">Configuration d'une collection de certificats virtuelle pour la validation des certificats S/MIME</span><span class="sxs-lookup"><span data-stu-id="a7bb6-103">Set up virtual certificate collection to validate S/MIME</span></span>

<span data-ttu-id="a7bb6-p101">En tant qu'administrateur client, vous devrez configurer une collection de certificats virtuelle qui sera utilisée pour valider les certificats S/MIME. Cette collection de certificats virtuelle est configurée comme un type de fichier de magasin de certificats avec une extension de nom de fichier SST. Le fichier SST contient tous les certificats racine et intermédiaires utilisés lors de la validation d'un certificat S/MIME.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-p101">As a tenant administrator you will need to configure a virtual certificate collection that will be used to validate S/MIME certificates. This virtual certificate collection is set up as a certificate store file type with an SST filename extension. The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>
  
## <a name="create-and-save-an-sst"></a><span data-ttu-id="a7bb6-107">Créer et enregistrer un fichier SST</span><span class="sxs-lookup"><span data-stu-id="a7bb6-107">Create and save an SST</span></span>
<span data-ttu-id="a7bb6-108"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="a7bb6-108"></span></span>

<span data-ttu-id="a7bb6-p102">Vous pouvez uniquement utiliser l'environnement de ligne de commande Exchange Management Shell pour effectuer cette tâche. Pour apprendre à ouvrir l'environnement de ligne de commande Environnement de ligne de commande Exchange Management Shell dans votre organisation Exchange locale, reportez-vous à **Open the Shell**. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="a7bb6-p102">You can only use the Shell to perform this procedure. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
<span data-ttu-id="a7bb6-p103">En tant qu'administrateur, vous pouvez créer ce fichier SST en exportant les certificats à partir d'un ordinateur approuvé à l'aide de la cmdlet  `Export-Certificate` et en indiquant SST pour le type. Pour plus d'informations sur la cmdlet  `Export-Certificate`, consultez la rubrique de référence [Export-Certificate](https://docs.microsoft.com/en-us/powershell/module/pkiclient/export-certificate?view=win10-ps).</span><span class="sxs-lookup"><span data-stu-id="a7bb6-p103">As an administrator, you can create this SST file by exporting the certificates from a trusted machine using the  `Export-Certificate` cmdlet and specifying the type as SST. For more information the  `Export-Certificate` cmdlet, see the [Export-Certificate](https://docs.microsoft.com/en-us/powershell/module/pkiclient/export-certificate?view=win10-ps) reference topic.</span></span> 
  
<span data-ttu-id="a7bb6-p104">Une fois le fichier SST généré, utilisez la cmdlet  `Set-Smimeconfig` pour l'enregistrer dans le magasin de certificats virtuel à l'aide du paramètre  _-SMIMECertificateIssuingCA_. Par exemple :  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span><span class="sxs-lookup"><span data-stu-id="a7bb6-p104">Once the SST file is generated, use the  `Set-Smimeconfig` cmdlet to save it in the virtual certificate store by using the  _-SMIMECertificateIssuingCA_ parameter. For example:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span></span>
  
## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="a7bb6-116">S'assurer de la validité d'un certificat</span><span class="sxs-lookup"><span data-stu-id="a7bb6-116">Ensuring a certificate is valid</span></span>
<span data-ttu-id="a7bb6-117"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="a7bb6-117"></span></span>

<span data-ttu-id="a7bb6-p105">Exchange 2013 SP1 recherche en premier lieu le fichier SST et valide le certificat. Si la validation échoue, il examinera le magasin de certificats de l’ordinateur local pour valider le certificat. Ce comportement est nouveau pour Exchange 2013 SP1 et diffère des versions précédentes d’Exchange. Dans Exchange Online, seul le fichier SST sera utilisé pour la validation.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-p105">Exchange 2013 SP1 first checks for the SST file and validates the certificate. If the validation fails, it will look at the local machine certificate store to validate the certificate. This behavior is new for Exchange 2013 SP1 and different from prior versions of Exchange. In Exchange Online only the SST will be used for validation.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="a7bb6-122">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a7bb6-122">More Information</span></span>
<span data-ttu-id="a7bb6-123"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="a7bb6-123"></span></span>

[<span data-ttu-id="a7bb6-124">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="a7bb6-124">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="a7bb6-125">Get-SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="a7bb6-125">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  

