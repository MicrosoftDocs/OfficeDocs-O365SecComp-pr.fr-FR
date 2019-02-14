---
title: Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection: M365-security-compliance
description: Intégrer contre les menaces avancées Office 365 avec Windows Defender avancée protection contre les menaces pour afficher des informations plus détaillées sur la gestion menace.
ms.openlocfilehash: f8f5f50af10fb668aa67b68604e95e8dd19c9e69
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995205"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces

Si vous faites partie de l’équipe de sécurité de votre organisation, vous pouvez intégrer les fonctionnalités Office 365 avancée protection contre les menaces et les menaces contre les menaces avancées Windows Defender. Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous effectuez des recherches sur les menaces dans Office 365. Par exemple, une fois que l’intégration est activée, vous serez en mesure de voir une liste des ordinateurs qui sont utilisés par les destinataires d’un message électronique détecté, ainsi que la manière dont les alertes récentes de ces ordinateurs ont dans Windows Defender avancée protection contre les menaces.
  
L’image suivante montre l’onglet **périphériques** qui apparaît lorsque l’intégration Windows Defender avancée protection contre les menaces activée a été : 
  
![Lorsque Windows Defender DAV est activé, vous pouvez voir une liste des ordinateurs sur lesquels les alertes.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre périphériques et a une alerte. En cliquant sur le lien pour un périphérique, la page s’ouvre dans le portail Windows Defender avancée protection contre les menaces.
  
## <a name="requirements"></a>Configuration requise

- Votre organisation doit avoir des informations sur les menaces Office 365 et Windows Defender DAV.
    
- Vous devez être administrateur Global Office 365 ou avoir un rôle d’administrateur de sécurité (comme administrateur de sécurité) affecté dans le [sécurité &amp; centre de conformité](https://protection.office.com). (Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md))
    
- Vous devez avoir accès à Office 365 menaces et le portail Windows Defender avancée protection contre les menaces.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Pour intégrer des menaces Office 365 avec Windows Defender DAV

Intégrer Office 365 menaces contre les menaces avancées Windows Defender est définie à l’aide de deux & Office 365 sécurité Centre de conformité et le portail Windows Defender avancée protection contre les menaces.
  
1. En tant qu’administrateur global Office 365 ou un administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école pour Office 365. 
    
2. Cliquez sur **Gestion des menaces** \> **Explorer**.<br>![Explorateur de solutions dans le menu Gestion des menaces](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. Dans le coin supérieur droit de l’écran, choisissez **Paramètres WDATP**.
    
4. Dans la boîte de dialogue connexion Windows Defender DAV activer sur se connecter à Windows DAV.<br>![Connexion Windows Defender DAV](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Activer la connexion dans Windows Defender avancée protection contre les menaces. Voir [utilisation du portail Windows Defender avancée protection contre les menaces](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Voir aussi

[Intelligence des menaces d’Office 365](office-365-ti.md)
  
[Protection avancée contre les menaces dans Office 365](office-365-atp.md)
  

