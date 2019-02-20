---
title: Déployer le contrôle d'application d'accès conditionnel pour les applications Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Procédez comme suit pour configurer les applications Azure AD Office 365 qui seront contrôlées par le contrôle d'application d'accès conditionnel à Office 365 Cloud App Security.
ms.openlocfilehash: ba3980615815fa45b1385a67560cc635506e2c22
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103289"
---
# <a name="deploy-conditional-access-app-control-for-office-365-apps"></a>Déployer le contrôle d'application d'accès conditionnel pour les applications Office 365

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étape suivante](ocas-session-policies.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |

Procédez comme suit pour configurer les applications Azure AD Office 365 qui seront contrôlées par le contrôle d'application d'accès conditionnel à Office 365 Cloud App Security.

**Étape 1: [créer une stratégie de test d'accès conditionnel Azure ad](#step-1-create-an-azure-ad-conditional-access-test-policy)**

**Étape 2: [se connecter avec un utilisateur étendu à la stratégie dans les applications](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**

**Étape 3: Si vous n'avez pas sélectionné de stratégie de sécurité d'application Cloud intégrée dans Azure AD ou si vous souhaitez appliquer la stratégie à une application non proposée, conFigurez les [contrôles avancés dans le portail de sécurité des applications Cloud](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal) .**

**Étape 4: [tester le déploiement](#step-4-test-the-deployment)**

> [!IMPORTANT]
> pour déployer le contrôle d'application d'accès conditionnel pour les applications office 365, vous avez besoin d'une [licence valide pour Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) , ainsi qu'une licence de sécurité d'application Cloud office 365.

## <a name="step-1-create-an-azure-ad-conditional-access-test-policy"></a>Étape 1: créer une stratégie de test d'accès conditionnel Azure AD 

1. Dans Azure Active Directory, sous **sécurité**, cliquez sur **accès conditionnel**.

2. Cliquez sur **nouvelle stratégie** et créez une stratégie.

3. Dans la stratégie de TEST, sous **utilisateurs**, affectez un utilisateur ou un utilisateur test qui peut être utilisé pour une authentification et une vérification initiales.

4. Dans la stratégie de TEST, sous **application Cloud**, affectez les applications que vous souhaitez contrôler avec le contrôle d'application d'accès conditionnel.

5. Sous **session**, définissez la stratégie pour qu'elle utilise l'une des stratégies intégrées, **analyse uniquement** ou **bloquer les téléchargements**. Ou sélectionnez **utiliser une stratégie** personnalisée pour définir une stratégie avancée dans le portail de sécurité des applications Cloud.

6. Ajoutez les attributions de **condition**applicables ou les **contrôles** d'octroi (facultatif).

> ![Accès conditionnel Azure AD](media/image1.png)

## <a name="step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps"></a>Étape 2: se connecter avec un utilisateur étendu à la stratégie dans les applications 

Une fois que vous avez créé la stratégie, connectez-vous à chaque application configurée dans cette stratégie. Vérifiez que vous vous connectez à l'aide d'un utilisateur configuré dans la stratégie. Veillez à vous déconnecter d'abord des sessions existantes.

La sécurité des applications Cloud synchronisera les détails de votre stratégie avec ses serveurs pour chaque nouvelle application à laquelle vous vous connectez. Cette opération peut prendre jusqu'à une minute.

## <a name="step-3-configure-advanced-controls-in-the-cloud-app-security-portal"></a>Étape 3: configurer des contrôles avancés dans le portail de sécurité des applications Cloud 

Les instructions ci-dessus vous ont permis de créer une stratégie de sécurité d'application Cloud intégrée pour les applications proposées directement dans Azure AD.

pour configurer une stratégie avancée, créez une stratégie d' [accès](ocas-access-policies.md) ou une [stratégie](ocas-session-policies.md) de session dans le portail de sécurité des applications Cloud Office 365.

### <a name="to-identify-devices-using-client-certificates-this-is-optional"></a>Pour identifier les appareils utilisant des certificats clients (facultatif):

1. Accédez à l'COG paramètres, puis choisissez identification de l' **appareil**.

2. Téléchargez un ou plusieurs certificats racines ou intermédiaires.

3. Une fois le certificat téléchargé, vous pouvez créer des stratégies d'accès et des stratégies de session basées sur la **baliSe Device** et le **certificat client valide**.

![ID de périphérique de contrôle d'application d'accès conditionnel](media/image2.png)

> [!NOTE]
> Un certificat est uniquement demandé à un utilisateur si la session correspond à une stratégie qui utilise le filtre de certificat client valide.
> 
## <a name="step-4-test-the-deployment"></a>Étape 4: tester le déploiement 

1. Première déconnexion des sessions existantes. Ensuite, essayez de vous connecter à chaque application qui a été déployée avec succès. Connectez-vous à l'aide d'un utilisateur correspondant à la stratégie configurée dans Azure AD.

2. Dans le portail de sécurité des applications Cloud, sous **examiner**, sélectionnez **Journal d'activité**, puis assurez-vous que les activités de connexion sont capturées pour chaque application.

3. Vous pouvez filtrer en cliquant sur **avancé**, puis le filtrage à l'aide de la **source est égal à contrôle d'accès**.

4. Il est recommandé de vous connecter à des applications mobiles et de bureau à partir d'appareils gérés et non gérés. Cela permet de s'assurer que les activités sont correctement capturées dans le journal d'activité. Pour vérifier que l'activité est correctement capturée, cliquez sur une activité d'ouverture de session unique pour qu'elle ouvre le tiroir d'activité. Assurez-vous que la balise de l' **agent utilisateur**reflète correctement si le périphérique est un client natif (c'est-à-dire une application mobile ou de bureau) ou si l'appareil est un appareil géré (conforme, joint à un domaine ou un certificat client valide).

> [!NOTE]
> Une fois déployée, vous ne pouvez pas supprimer une application à partir de la page de contrôle d'application Access conditionnelle. Tant que vous ne définissez pas une session ou une stratégie d'accès sur l'application, le contrôle d'application d'accès conditionnel ne modifie aucun comportement pour l'application.

## <a name="next-steps"></a>Étapes suivantes

- [En savoir plus sur les stratégies de session dans Office 365 Cloud App Security](ocas-session-policies.md)

- [En savoir plus sur les stratégies d'accès dans Office 365 Cloud App Security](ocas-access-policies.md) 

- [Grouper vos adresses IP pour simplifier la gestion dans la sécurité des applications cloud Office 365](group-your-ip-addresses-in-ocas.md)