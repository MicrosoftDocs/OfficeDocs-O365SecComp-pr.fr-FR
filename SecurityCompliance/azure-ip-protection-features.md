---
title: Fonctionnalités de protection d’Azure Information Protection présentant aux clients Office 365 existants
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ad6f58e-65d7-4c82-8e65-0b773666634d
description: Pour vous aider avec la première étape de la protection de vos informations, début juillet 2018 tous les clients éligibles de Protection des informations Azure sont ont les fonctionnalités de protection de la Protection des informations Azure activées par défaut. Les fonctionnalités de protection de la Protection des informations Azure ont été anciennement dans Office 365 Rights Management ou RMS Azure. Si votre organisation a un plan de service Office E3 ou un plan de service plus élevé, que vous obtenez un coup de protection des informations par le biais de la Protection des informations Azure lorsque nous déployer ces fonctionnalités.
ms.openlocfilehash: be0200da3032dccbcf54e67f3bdfbac800b65526
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527832"
---
# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>Fonctionnalités de protection d’Azure Information Protection présentant aux clients Office 365 existants

Pour vous aider avec la première étape de la protection de vos informations, début juillet 2018 tous les clients éligibles de Protection des informations Azure sont ont les fonctionnalités de protection de la Protection des informations Azure activées par défaut. Les fonctionnalités de protection de la Protection des informations Azure ont été anciennement dans Office 365 Rights Management ou RMS Azure. Si votre organisation a un plan de service Office E3 ou un plan de service plus élevé, que vous obtenez un coup de protection des informations par le biais de la Protection des informations Azure lorsque nous déployer ces fonctionnalités.
  
## <a name="changes-beginning-july-1-2018"></a>Modifications commençant le 1 juillet 2018

Démarrage 1 juillet 2018, Microsoft activer la fonctionnalité de protection dans Azure la Protection des informations pour tous les clients Office 365 qui ont un des plans d’abonnement suivants :
  
- Office 365, le chiffrement de messages est proposé dans le cadre d’Office 365 E3 et E5, Microsoft E3 et E5, Office 365 A1, A3 et A5 et Office 365 G3 et G5. Vous n’avez pas besoin de licences supplémentaires afin de recevoir les nouvelles fonctionnalités de protection par la Protection des informations Azure. 
    
- Vous pouvez également ajouter des plans recevoir les nouvelles fonctionnalités d’Office 365 Message Encryption Azure informations Protection Plan 1 à la suivante : Exchange Online Plan 1, Exchange Online Plan 2, Office 365 F1, Office 365 entreprise Essentials, Office 365 entreprise Premium, ou Office 365 entreprise E1.
    
- Chaque utilisateur bénéficiant de chiffrement de messages Office 365 doit être sous licence pour être couverts par la fonctionnalité.
    
- Pour obtenir la liste complète consultez les [descriptions du service Exchange Online](https://technet.microsoft.com/library/exchange-online-service-description.aspx) pour Office 365 Message Encryption. 
    
Les administrateurs de clients peuvent vérifier l’état de la protection dans le portail d’administrateur Office 365. 
  
![Capture d’écran montrant que la gestion des droits dans Office 365 est activée.](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>Pourquoi nous faisons ce changement ?

Chiffrement de messages Office 365 exploite les fonctionnalités de protection de la Protection des informations Azure. Au cœur de récentes améliorations apportées au chiffrement de messages Office 365 et nos investissements plus larges pour la protection des informations dans Microsoft 365, nous effectuons ce qui facilite pour les organisations à activer et utiliser ses fonctionnalités de protection, en tant que par le passé, chiffrement technologies ont été difficiles à configurer. En activant les fonctionnalités de protection dans Azure la Protection des informations par défaut, vous pouvez rapidement commencer à protéger vos données sensibles.
  
## <a name="does-this-impact-me"></a>Est l’impact sur moi ?

Si votre organisation Office 365 a acquis une licence Office 365 éligible, votre client est affectée par cette modification.
  
 **IMPORTANT !** Si vous utilisez Active Directory Rights Management Services (AD RMS) dans votre environnement local, vous devez annulations de ce changement immédiatement ou migrer vers la Protection des informations Azure avant que nous déployer cette modification dans les 30 jours. Pour plus d’informations sur la façon d’annulations, consultez la rubrique « utiliser AD RMS, comment choisir les out? » plus loin dans cet article. Si vous souhaitez migrer, voir [migration à partir d’AD RMS pour la Protection des informations Azure.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>Puis-je utiliser la Protection des informations Azure avec Active Directory Rights Management Services (AD RMS) ?

Non. Il ne s’agit pas d’un scénario de déploiement pris en charge. Sans effectuer les étapes annulations supplémentaires, certains ordinateurs peuvent démarrer automatiquement à l’aide du service Azure Rights Management et également vous connecter à votre cluster AD RMS. Ce scénario n’est pas pris en charge et a des résultats non fiables, il est important de refuser cette modification dans les 30 jours avant de nous répercuter ces fonctionnalités. Pour plus d’informations sur la façon d’annulations, consultez la rubrique « utiliser AD RMS, comment choisir les out? » plus loin dans cet article. Si vous souhaitez migrer, voir [migration à partir d’AD RMS pour la Protection des informations Azure.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>Comment savoir si j’utilise AD RMS ?

Utilisez ces instructions de [Préparation de l’environnement pour Azure Rights Management lorsque vous avez également Active Directory Rights Management Services (AD RMS)](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) pour vérifier si vous avez déployé AD RMS : 
  
1. Bien que facultatif, la plupart des déploiements AD RMS publier le point de connexion de service (SCP) dans Active Directory afin que les ordinateurs du domaine peuvent découvrir le cluster AD RMS. 
  
Utilisez l’éditeur ADSI pour vérifier si vous avez un SCP publié dans Active Directory : CN = Configuration [nom du serveur], CN = Services, CN = RightsManagementServices, CN = SCP
    
2. Si vous n’utilisez pas un SCP, les ordinateurs Windows qui se connectent à un cluster AD RMS doivent être configurés pour la détection du service côté client ou de la redirection de gestion des licences à l’aide du Registre Windows : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation ou HKEY_ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
Pour plus d’informations sur ces configurations de Registre, consultez [découverte de service côté client activation à l’aide du Registre Windows](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) et [Gestion des licences redirection le trafic du serveur](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic).
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>Utiliser AD RMS, comment j’exclure ?

Pour refuser les modifications à venir, procédez comme suit :
  
1. À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Exécutez l’applet de commande Set-IRMConfiguration à l’aide de la syntaxe suivante :
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>Quelles que j’attends qu’une fois que cette modification a été effectuée ?

Une fois que cette option est activée, condition que vous n’avez pas choisi, vous pouvez démarrer à l’aide de la nouvelle version d’Office 365 Message Encryption qui a été annoncé à [Microsoft Ignite 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) et tire parti des fonctionnalités de chiffrement et de protection des informations d’Azure Protection. 
  
![Capture d’écran montrant un OME protégés par message dans Outlook sur le web.](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
Pour plus d’informations sur les nouvelles fonctionnalités, voir [Office 365 Message Encryption](ome.md).
  

