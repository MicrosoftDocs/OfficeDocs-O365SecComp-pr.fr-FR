---
title: Synchronisation des certificats utilisateur vers Office 365 pour S/MIME
ms.author: chrisda
author: chrisda
manager: Serdars
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: Pour qu'une personne puisse envoyer des messages protégés par S/MIME, les certificats appropriés doivent être configurés. Pour envoyer des messages chiffrés par Exchange Online, le programme de messagerie de l'expéditeur utilise le certificat public du destinataire pour chiffrer le message. Ce certificat X.509 public doit être publié sur Office 365.
ms.openlocfilehash: 35de3ba34be48a8553c7034f646576e4fca8b870
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30294997"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a><span data-ttu-id="b76a2-105">Synchronisation des certificats utilisateur vers Office 365 pour S/MIME</span><span class="sxs-lookup"><span data-stu-id="b76a2-105">Sync user certificates to Office 365 for S/MIME</span></span>

<span data-ttu-id="b76a2-p102">Pour qu'une personne puisse envoyer des messages protégés par S/MIME dans Exchange Online, les certificats appropriés doivent être configurés. Pour envoyer des messages chiffrés via Exchange Online, l'application de messagerie de l'expéditeur utilise le certificat public du destinataire pour chiffrer le message. Ce certificat X. 509 public doit être publié vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="b76a2-p102">Before anyone can send S/MIME-protected messages in Exchange Online, the appropriate certificates must be set up. To send encrypted messages through Exchange Online, the sender's email app uses the public certificate of the recipient to encrypt the message. This public X.509 certificate has to be published to Office 365.</span></span>

## <a name="to-sync-certificates-that-support-smime"></a><span data-ttu-id="b76a2-109">Synchronisation de certificats prenant en charge S/MIME</span><span class="sxs-lookup"><span data-stu-id="b76a2-109">To Sync certificates that support S/MIME</span></span>

<span data-ttu-id="b76a2-p103">Commencez la configuration de S/MIME en émettant des certificats et en les publiant dans votre service de domaine Active Directory local. Pour plus d'informations sur la gestion des certificats dans Exchange Server, consultez la rubrique [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span><span class="sxs-lookup"><span data-stu-id="b76a2-p103">Begin setting up S/MIME by issuing certificates and publishing them in your local Active Directory Domain Service. For more information about managing certificates in Exchange Server, see [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span></span>

<span data-ttu-id="b76a2-p104">Une fois vos certificats publiés, utilisez l'Outil de synchronisation Windows Azure Active Directory pour synchroniser les données utilisateur depuis votre environnement Exchange local sur Office 365. Pour plus d'informations sur ce processus, consultez la rubrique [DirSync : Historique des versions de l'outil de synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span><span class="sxs-lookup"><span data-stu-id="b76a2-p104">After your certificates are published, use the Azure Active Directory Sync tool to synchronize user data from your on-premises Exchange environment to Office 365. For more information on this process, see [DirSync: Directory Sync Tool Version Release History](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span></span>

<span data-ttu-id="b76a2-114">En plus de synchroniser d'autres données d'annuaire, pour des raisons de S/MIME, l'outil synchronisera les attributs **userCertificate** et **userSMIMECertificate** pour chaque objet utilisateur afin que les données puissent être utilisées pour signer et chiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="b76a2-114">Along with synchronizing other directory data, for S/MIME purposes, the tool will synchronize the  **userCertificate** and **userSMIMECertificate** attributes for each user object so the data can be used to sign and encrypt messages.</span></span>

## <a name="more-information"></a><span data-ttu-id="b76a2-115">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="b76a2-115">More Information</span></span>

[<span data-ttu-id="b76a2-116">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="b76a2-116">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

<span data-ttu-id="b76a2-117">[Outil de synchronisation Windows Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span><span class="sxs-lookup"><span data-stu-id="b76a2-117">[Azure Active Directory Sync tool](https://go.microsoft.com/fwlink/p/?LinkId=392587)</span></span>
