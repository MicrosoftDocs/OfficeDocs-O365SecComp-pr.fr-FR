---
title: Stratégies d’accès dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 Cloud App les stratégies d'accès de sécurité activent la surveillance en temps réel et le contrôle de l'accès aux applications Cloud en fonction de l'utilisateur, de l'emplacement, du périphérique et de l'application. Vous pouvez créer des stratégies d'accès pour n'importe quel appareil, y compris des appareils qui ne sont pas joints à un domaine, et qui ne sont pas gérés par Windows Intune en déployant des certificats clients sur des appareils gérés ou à l'aide de certificats existants, tels que des certificats MDM tiers. Par exemple, vous pouvez déployer des certificats clients sur des appareils gérés, puis bloquer l'accès à partir d'appareils sans certificat.
ms.openlocfilehash: 5e8b8fa293420bc9ff3616daf288b8e02a2eb768
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263002"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a>Stratégies d’accès dans la sécurité des applications cloud Office 365

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étape suivante](group-your-ip-addresses-in-ocas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |

Office 365 Cloud App les stratégies d'accès de sécurité activent la surveillance en temps réel et le contrôle de l'accès aux applications Cloud en fonction de l'utilisateur, de l'emplacement, du périphérique et de l'application. Vous pouvez créer des stratégies d'accès pour n'importe quel appareil, y compris des appareils qui ne sont pas joints à un domaine, et qui ne sont pas gérés par Windows Intune en déployant des certificats clients sur des appareils gérés ou à l'aide de certificats existants, tels que des certificats MDM tiers. Par exemple, vous pouvez déployer des certificats clients sur des appareils gérés, puis bloquer l'accès à partir d'appareils sans certificat.

Au lieu d'autoriser ou de bloquer entièrement l'accès, avec des [stratégies](ocas-session-policies.md) de session, vous pouvez autoriser l'accès tout en surveillant la session et/ou en limitant les activités de session spécifiques.

## <a name="prerequisites-to-using-access-policies"></a>Conditions préalables à l'utilisation des stratégies d'accès

- Licence Azure AD Premium P1

- Les applications appropriées doivent être [déployées avec le contrôle d'application d'accès conditionnel](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)

-  une [stratégie d'accès conditionnel Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)doit être mise en place pour rediriger les utilisateurs vers Office 365 Cloud App Security, comme décrit ci-dessous.

## <a name="create-an-azure-ad-conditional-access-policy"></a>Créer une stratégie d'accès conditionnel Azure AD

Les stratégies d'accès conditionnel Azure Active Directory et les stratégies de session de sécurité des applications Cloud fonctionnent en tandem pour examiner chaque session utilisateur et prendre des décisions de stratégie pour chaque application. Pour configurer une stratégie d'accès conditionnel dans Azure AD, procédez comme suit:

1. Configurez une  [stratégie d'accès conditionnel Azure ad](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)avec des affectations pour un utilisateur ou un groupe d'utilisateurs et l'application que vous souhaitez contrôler avec un contrôle d'application d'accès conditionnel.<br>Remarque: seules les applications qui ont été déployées  [avec le contrôle d'application d'accès conditionnel](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)seront affectées par cette stratégie.

2. acheminer les utilisateurs vers Office 365 Cloud app Security en sélectionnant les  **restrictions utiliser le contrôle d'application d'accès conditionnel**sous **Session**.

## <a name="create-a-cloud-app-security-access-policy"></a>Créer une stratégie d'accès de sécurité d'application Cloud

Pour créer une stratégie d'accès, procédez comme suit:

1. Dans le portail, sélectionnez **contrôle** suivi de **stratégies**.

2. Dans la page **stratégies** , cliquez sur **créer une stratégie** , puis sélectionnez **stratégie d'accès**.

3. Dans la fenêtre **stratégie** d'accès, attribuez un nom à votre stratégie, par exemple *bloquer l'accès à partir d'appareils non gérés*.

4. Dans les **activités correspondant à toutes les sections suivantes** , sous **source d'activité**, sélectionnez filtres d'activité supplémentaires à appliquer à la stratégie. Les filtres incluent les options suivantes:
    
    - **Balises de périphérique**: utilisez ce filtre pour identifier les appareils non gérés.
    
    - **Emplacement**: utilisez ce filtre pour identifier les emplacements inconnus (et par conséquent).
    
    - **Adresse IP**: utilisez ce filtre pour filtrer par adresse IP ou utiliser les balises d'adresses IP précédemment attribuées.
    
    - **Balise de l'agent utilisateur**: utilisez ce filtre pour activer l'heuristique afin d'identifier les applications mobiles et de bureau. Ce filtre peut être défini sur égal ou différent de. Les valeurs doivent être testées par rapport à vos applications mobiles et de bureau pour chaque application Cloud.

5. Sous **actions**, sélectionnez l'une des options suivantes:
    
    - **Autoriser**: définissez cette action pour autoriser l'accès de manière explicite en fonction des filtres de stratégie que vous définissez.
    
    - **Bloquer**: définissez cette action pour bloquer explicitement l'accès en fonction des filtres de stratégie que vous avez définis.

6. Vous pouvez **créer une alerte pour chaque événement correspondant à l'aide de la gravité de la stratégie**et définir une limite d'alerte, puis indiquer si vous souhaitez l'alerte sous forme de message électronique, de texte ou les deux.

## <a name="next-steps"></a>Étapes suivantes

- [Grouper vos adresses IP pour simplifier la gestion dans la sécurité des applications cloud Office 365](group-your-ip-addresses-in-ocas.md)