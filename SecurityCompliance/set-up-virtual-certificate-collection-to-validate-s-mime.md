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
description: s administrateur client que vous devrez configurer une collection virtuelle de certificat qui sera utilisée pour valider des certificats S/MIME.
ms.openlocfilehash: 88d12b3c1d5f36c58f278cf304237a569a8b92c4
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003033"
---
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a>Configuration d'une collection de certificats virtuelle pour la validation des certificats S/MIME

En tant qu'administrateur client, vous devrez configurer une collection de certificats virtuelle qui sera utilisée pour valider les certificats S/MIME. Cette collection de certificats virtuelle est configurée comme un type de fichier de magasin de certificats avec une extension de nom de fichier SST. Le fichier SST contient tous les certificats racine et intermédiaires utilisés lors de la validation d'un certificat S/MIME.
  
## <a name="create-and-save-an-sst"></a>Créer et enregistrer un fichier SST
<a name="sectionSection0"> </a>

Vous pouvez uniquement utiliser l'environnement de ligne de commande Exchange Management Shell pour effectuer cette tâche. Pour apprendre à ouvrir l'environnement de ligne de commande Environnement de ligne de commande Exchange Management Shell dans votre organisation Exchange locale, reportez-vous à **Open the Shell**. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
  
En tant qu'administrateur, vous pouvez créer ce fichier SST en exportant les certificats à partir d'un ordinateur approuvé à l'aide de la cmdlet  `Export-Certificate` et en indiquant SST pour le type. Pour plus d'informations sur la cmdlet  `Export-Certificate`, consultez la rubrique de référence [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx). 
  
Une fois le fichier SST généré, utilisez la cmdlet  `Set-Smimeconfig` pour l'enregistrer dans le magasin de certificats virtuel à l'aide du paramètre  _-SMIMECertificateIssuingCA_. Par exemple :  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`
  
## <a name="ensuring-a-certificate-is-valid"></a>S'assurer de la validité d'un certificat
<a name="sectionSection1"> </a>

Exchange 2013 SP1 recherche en premier lieu le fichier SST et valide le certificat. Si la validation échoue, il examinera le magasin de certificats de l’ordinateur local pour valider le certificat. Ce comportement est nouveau pour Exchange 2013 SP1 et diffère des versions précédentes d’Exchange. Dans Exchange Online, seul le fichier SST sera utilisé pour la validation.
  
## <a name="more-information"></a>Plus d’informations
<a name="sectionSection2"> </a>

[S/MIME pour la signature et le chiffrement des messages](s-mime-for-message-signing-and-encryption.md)
  
[Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  

