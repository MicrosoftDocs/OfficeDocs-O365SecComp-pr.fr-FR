---
title: Fonctionnalités de protection dans Azure information protection pour les clients Office 365 existants
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ad6f58e-65d7-4c82-8e65-0b773666634d
ms.collection:
- M365-security-compliance
description: Pour vous aider avec la première étape de la protection de vos informations, à partir du 1er juillet 2018, tous les clients éligibles Azure information protection disposent par défaut des fonctionnalités de protection d'Azure information protection. Les fonctionnalités de protection d'Azure information protection étaient précédemment connues dans Office 365 en tant que gestion des droits ou Azure RMS. Si votre organisation dispose d'un plan de service E3 Office ou d'un plan de service supérieur, vous recevrez maintenant une tête de protection des informations via Azure information protection lors de la mise en route de ces fonctionnalités.
ms.openlocfilehash: 2484f9b335a6698894046aaf429fdad68d82491e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243973"
---
# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>Fonctionnalités de protection dans Azure information protection pour les clients Office 365 existants

Pour vous aider avec la première étape de la protection de vos informations, à partir du 1er juillet 2018, tous les clients éligibles Azure information protection disposent par défaut des fonctionnalités de protection d'Azure information protection. Les fonctionnalités de protection d'Azure information protection étaient précédemment connues dans Office 365 en tant que gestion des droits ou Azure RMS. Si votre organisation dispose d'un plan de service E3 Office ou d'un plan de service supérieur, vous recevrez maintenant une tête de protection des informations via Azure information protection lors de la mise en route de ces fonctionnalités.
  
## <a name="changes-beginning-july-1-2018"></a>Modifications depuis le 1er juillet 2018

À partir du 1er juillet 2018, Microsoft Active la fonctionnalité de protection dans Azure information protection pour tous les clients Office 365 qui ont l'un des plans d'abonnement suivants:
  
- Le chiffrement de messages Office 365 est proposé dans Office 365 E3 et E5, Microsoft E3 et E5, Office 365 a1, a3 et a5, et Office 365 G3 et G5. Vous n'avez pas besoin de licences supplémentaires pour recevoir les nouvelles fonctionnalités de protection optimisées par Azure information protection. 
    
- Vous pouvez également ajouter le plan de protection des informations Azure 1 aux plans suivants pour recevoir les nouvelles fonctionnalités de chiffrement des messages Office 365: Exchange Online plan 1, Exchange Online plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium ou Office 365 entreprise E1.
    
- Chaque utilisateur bénéficiant d'Office 365 le chiffrement de messages doit être concédé sous licence pour être couvert par la fonctionnalité.
    
- Pour obtenir la liste complète, consultez les [descriptions de service Exchange Online](https://technet.microsoft.com/library/exchange-online-service-description.aspx) pour le chiffrement de messages Office 365. 
    
Les administrateurs clients peuvent vérifier le statut de protection dans le portail d'administration d'Office 365. 
  
![Capture d'écran montrant que la gestion des droits dans Office 365 est activée.](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>Pourquoi ce changement?

Le chiffrement de messages Office 365 exploite les fonctionnalités de protection d'Azure information protection. Au cœur des dernières améliorations apportées au chiffrement de messages Office 365 et à nos investissements plus larges en matière de protection des informations dans Microsoft 365, il est plus facile pour les organisations d'activer et d'utiliser les fonctionnalités de protection, telles que le chiffrement. les technologies ont été difficiles à configurer. En activant les fonctionnalités de protection dans Azure information protection par défaut, vous pouvez rapidement prendre en main pour protéger vos données sensibles.
  
## <a name="does-this-impact-me"></a>Cela a-t-il un impact?

Si votre organisation Office 365 a acheté une licence Office 365 éligible, votre client sera affecté par cette modification.
  
 **INDISPENSABLES!** Si vous utilisez les services AD RMS (Active Directory Rights Management Services) dans votre environnement local, vous devez annuler cette modification immédiatement ou migrer vers Azure information protection avant de déployer ces modifications au cours des 30 prochains jours. Pour plus d'informations sur la façon d'annuler l'abonnement, voir «j'utilise AD RMS, comment le désactiver?». » plus loin dans cet article. Si vous préférez effectuer une migration, reportez-vous à la rubrique [migration d'AD RMS vers Azure information protection.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>Puis-je utiliser Azure information protection avec Active Directory Rights Management Services (AD RMS)?

Non. Il ne s'agit pas d'un scénario de déploiement pris en charge. Sans prendre les autres étapes de désabonnement, certains ordinateurs peuvent démarrer automatiquement à l'aide du service Azure Rights Management et se connecter à votre cluster AD RMS. Ce scénario n'est pas pris en charge et présente des résultats peu fiables, c'est pourquoi il est important de désactiver ces modifications au cours des 30 prochains jours avant de déployer ces nouvelles fonctionnalités. Pour plus d'informations sur la façon d'annuler l'abonnement, voir «j'utilise AD RMS, comment le désactiver?». » plus loin dans cet article. Si vous préférez effectuer une migration, reportez-vous à la rubrique [migration d'AD RMS vers Azure information protection.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>Comment savoir si j'utilise AD RMS?

Suivez ces instructions de [la préparation de l'environnement pour Azure Rights Management lorsque vous disposez également des services AD RMS (Active Directory Rights Management Services)](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) pour vérifier si vous avez déployé AD RMS: 
  
1. Bien que facultatif, la plupart des déploiements AD RMS publient le point de connexion de service (SCP) vers Active Directory afin que les ordinateurs du domaine puissent découvrir le cluster AD RMS. 
  
Utiliser ADSI Edit pour voir si vous avez un SCP publié dans Active Directory: CN = Configuration [nom du serveur], CN = Services, CN = RightsManagementServices, CN = SCP
    
2. Si vous n'utilisez pas de SCP, les ordinateurs Windows qui se connectent à un cluster AD RMS doivent être configurés pour la redirection du service côté client ou de la gestion des licences à l'aide du Registre Windows: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation ou HKEY_ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
Pour plus d'informations sur ces configurations de Registre, reportez-vous à [la rubrique activation de la découverte de service côté client à l'aide du Registre Windows](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) et redirection [du trafic du serveur](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic)de gestion des licences.
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>J'utilise AD RMS, comment puis-je désactiver?

Pour désactiver la modification à venir, procédez comme suit:
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Exécutez la cmdlet Set-IRMConfiguration à l'aide de la syntaxe suivante:
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>Que puis-je attendre une fois cette modification apportée?

Une fois cette fonctionnalité activée, si vous n'avez pas encore choisi, vous pouvez commencer à utiliser la nouvelle version d'Office 365 le chiffrement de messages annoncé auprès de [Microsoft enflamme 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) et tirer parti des fonctionnalités de chiffrement et de protection des informations Azure. Protège. 
  
![Capture d'écran illustrant un message protégé par OME dans Outlook sur le Web.](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
Pour plus d'informations sur les nouvelles améliorations, consultez la rubrique [Office 365 message](ome.md)Encryption.
  

