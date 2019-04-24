---
title: Intégrer Office 365 Advanced Threat Protection avec Windows Defender protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Intégrer Office 365 Advanced Threat Protection avec Windows Defender protection avancée contre les menaces pour consulter des informations plus détaillées sur la gestion des menaces.
ms.openlocfilehash: 832b9c6bc600366e1ed6b7c6e60442bec8b5002c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254424"
---
# <a name="integrate-office-365-advanced-threat-protection-with-windows-defender-advanced-threat-protection"></a>Intégrer Office 365 Advanced Threat Protection avec Windows Defender protection avancée contre les menaces

Si vous êtes membre de l'équipe de sécurité de votre organisation, vous pouvez intégrer Office 365 Advanced Threat Protection et les fonctionnalités d'enquête et de réponse associées avec Windows Defender Advanced Threat Protection. Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous étudiez les menaces dans Office 365. Par exemple, une fois que l'intégration est activée, vous pouvez voir la liste des ordinateurs utilisés par les destinataires d'un message électronique détecté, ainsi que le nombre d'alertes récentes de protection avancée contre les menaces Windows Defender.
  
L'image suivante montre l'onglet **appareils** qui apparaît lorsque l'intégration de la protection avancée contre les menaces Windows Defender est activée: 
  
![Lorsque l'ATP Windows Defender est activé, vous pouvez voir une liste des ordinateurs avec des alertes.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre appareils et que l'un d'entre eux comporte une alerte. Cliquer sur le lien d'un appareil ouvre sa page dans le portail protection avancée contre les menaces Windows Defender.
  
## <a name="requirements"></a>Configuration requise

- Votre organisation doit avoir Office 365 Advanced Threat Protection Plan 2 (ou Office 365 E5) et Windows Defender ATP.
    
- Vous devez être un administrateur général Office 365 ou disposer d'un rôle d'administrateur de sécurité (tel que administrateur de sécurité) affecté dans le [Centre de sécurité &amp; conformité](https://protection.office.com). (Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md))
    
- Vous devez avoir accès à Office 365 Threat Explorer dans le centre de sécurité & Compliance Center et au portail protection avancée contre les menaces Windows Defender.
    
## <a name="to-integrate-office-365-advanced-threat-protection-with-windows-defender-atp"></a>Pour intégrer Office 365 Advanced Threat Protection avec Windows Defender ATP

L'intégration de la protection avancée contre les menaces Office 365 avec Windows Defender Advanced Threat Protection est configurée à l'aide du centre de sécurité & Compliance Center et du portail de protection avancée contre les menaces Windows Defender.
  
1. En tant qu'administrateur général Office 365 ou administrateur de sécurité, accédez [https://protection.office.com](https://protection.office.com) à et connectez-vous avec votre compte professionnel ou scolaire pour Office 365. 
    
2. Choisissez **** \> **Explorateur**de gestion des menaces.<br>![Explorateur dans le menu gestion des menaces](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. Dans le coin supérieur droit de l'écran, sélectionnez **paramètres WDATP**.
    
4. Dans la boîte de dialogue connexion Windows Defender ATP, activez connexion à Windows ATP.<br>![Connexion ATP Windows Defender](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Activez la connexion dans Windows Defender protection avancée contre les menaces. Voir [utiliser le portail protection avancée contre les menaces Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Voir aussi

[Enquête et réponse aux menaces Office 365](office-365-ti.md)
  
[Office 365-Protection avancée contre les menaces](office-365-atp.md)
  

