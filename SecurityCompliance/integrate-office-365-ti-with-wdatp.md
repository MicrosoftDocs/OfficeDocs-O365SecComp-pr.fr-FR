---
title: Intégrer les menaces d’Office 365 avec Windows Defender avancées de protection contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Intégrer contre les menaces avancées Office 365 avec Windows Defender avancée protection contre les menaces pour afficher des informations plus détaillées sur la gestion menace.
ms.openlocfilehash: 574594d5881853b268713e0bb74444ae80ffcf46
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527811"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Intégrer les menaces d’Office 365 avec Windows Defender avancées de protection contre les menaces

Si vous faites partie de l’équipe de sécurité de votre organisation, vous pouvez intégrer Office 365 avec le module Windows Defender Advanced Threat Protection (DAV). Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous effectuez des recherches sur les menaces dans Office 365. Par exemple, une fois que l’intégration est activée, vous serez en mesure de voir une liste des ordinateurs qui sont utilisés par les destinataires d’un message électronique détecté, ainsi que la manière dont les alertes récentes de ces ordinateurs ont dans Windows Defender DAV.
  
L’image suivante montre l’onglet **périphériques** qui apparaît lorsque l’intégration Windows Defender DAV activée a été : 
  
![Lorsque Windows Defender DAV est activé, vous pouvez voir une liste des ordinateurs sur lesquels les alertes.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre ordinateurs et une a une alerte dans Windows Defender DAV. En cliquant sur le lien vers un ordinateur ouvre la page de l’ordinateur dans Windows Defender DAV dans un nouvel onglet.
  
## <a name="requirements"></a>Configuration requise

- Votre organisation doit avoir des informations sur les menaces Office 365 et Windows Defender DAV.
    
- Vous devez être un administrateur global d’Office 365 ou avoir un rôle d’administrateur de sécurité affecté de la sécurité &amp; centre de conformité. (Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md))
    
- Vous devez avoir accès à Office 365 menaces et le portail Windows Defender DAV.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Pour intégrer des menaces Office 365 avec Windows Defender DAV

Intégration des menaces Office 365 avec Windows Defender DAV est configuré dans Office 365 et dans le portail Windows Defender DAV.
  
1. En tant qu’un global Office 365 ou un administrateur de sécurité, accédez à [https://portal.office.com](https://portal.office.com) et connectez-vous avec votre compte professionnel ou de l’école pour Office 365. 
    
2. Cliquez sur **Gestion des menaces** \> **explorer menace**.
    
3. Dans le menu de **plus** , choisissez **Paramètres WDATP**.
    
4. Sélectionnez **se connecter à Windows DAV**.
    
Une fois que vous avez modifié les paramètres dans Office 365, vous devez activer la connexion à partir de Windows Defender DAV. Pour ce faire, voir [utilisation du portail Windows Defender avancée protection contre les menaces](https://go.microsoft.com/fwlink/?linkid=859690).
  
## <a name="related-topics"></a>Voir aussi

[Intelligence des menaces d’Office 365](office-365-ti.md)
  
[Protection de Microsoft Office 365 menace avancées](office-365-atp.md)
  

