---
title: Synchronisation des certificats utilisateur vers Office 365 pour S/MIME
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
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: Pour qu'une personne puisse envoyer des messages protégés par S/MIME, les certificats appropriés doivent être configurés. Pour envoyer des messages chiffrés par Exchange Online, le programme de messagerie de l'expéditeur utilise le certificat public du destinataire pour chiffrer le message. Ce certificat X.509 public doit être publié sur Office 365.
ms.openlocfilehash: 452b538b4515bdbcd5fcbdedad17f0450c04207a
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002372"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a>Synchronisation des certificats utilisateur vers Office 365 pour S/MIME

Pour qu'une personne puisse envoyer des messages protégés par S/MIME, les certificats appropriés doivent être configurés. Pour envoyer des messages chiffrés par Exchange Online, le programme de messagerie de l'expéditeur utilise le certificat public du destinataire pour chiffrer le message. Ce certificat X.509 public doit être publié sur Office 365.
  
## <a name="to-sync-certificates-that-support-smime"></a>Synchronisation de certificats prenant en charge S/MIME

Commencez la configuration de S/MIME en émettant des certificats et en les publiant dans votre service de domaine Active Directory local. Pour plus d'informations sur la gestion des certificats dans Exchange 2013, consultez la rubrique [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).
  
Une fois vos certificats publiés, utilisez l'Outil de synchronisation Windows Azure Active Directory pour synchroniser les données utilisateur depuis votre environnement Exchange local sur Office 365. Pour plus d'informations sur ce processus, consultez la rubrique [DirSync : Historique des versions de l'outil de synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=392587).
  
En plus de la synchronisation d'autres données d'annuaire, à des fins de protection S/MIME, l'outil synchronisera les attributs  `userCertificate` et  `userSMIMECertificate` pour chaque objet utilisateur afin que les données puissent être utilisées pour signer et chiffrer les messages. 
  
## <a name="more-information"></a>Plus d'informations

[S/MIME pour la signature et le chiffrement des messages](s-mime-for-message-signing-and-encryption.md)
  
[Outil de synchronisation Windows Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkId=392587).
  

