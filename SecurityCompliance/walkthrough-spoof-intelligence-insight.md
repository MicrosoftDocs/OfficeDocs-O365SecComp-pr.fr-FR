---
title: Présentation des usurpations d’identité
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 7/30/2018
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
ms.collection:
- M365-security-compliance
description: Découvrez comment fonctionne la nouvelle usurpation d’aide à la décision.
ms.openlocfilehash: f9e9ba03f69703060a34ae3142607550b5ccee90
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598420"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>Procédure pas à pas: usurpation d’aide

En utilisant l’aide à la décision, vous pouvez déterminer rapidement les expéditeurs qui envoient de manière légitime votre courrier électronique non authentifié. En leur permettant d’envoyer des messages falsifiés, vous pouvez réduire le risque de faux positifs pour vos utilisateurs.
  
En outre, vous pouvez également utiliser le contrôle d’aide à la décision et gérer les paires de domaines autorisées pour fournir une couche de sécurité supplémentaire et empêcher les messages non sécurisés d’arriver dans votre organisation.
  
Vous pouvez utiliser la fonction d’aide à la décision &amp; dans le centre de sécurité conformité si votre compte scolaire ou professionnel dispose des autorisations d’administrateur général d’Office 365, d’administrateur de sécurité ou de lecteur de sécurité. Pour plus d’informations, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).
  
Si vous débutez avec des [rapports et des informations dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md), il peut vous aider à naviguer dans un tableau de bord jusqu’à une vue d’analyse et des actions recommandées.
  
Vous pouvez afficher le centre d’aide à la décision à partir de plusieurs tableaux &amp; de bord dans le centre de sécurité conformité. Quel que soit le tableau de bord que vous examinez, le détail fournit les mêmes détails et vous permet d’effectuer rapidement les mêmes tâches.
  
Il s’agit de l’une des nombreuses procédures pas &amp; à pas pour le centre de sécurité conformité. Pour savoir comment naviguer dans les rapports et les informations, consultez les procédures pas à pas dans la section Rubriques connexes.
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>Accès à l’aide à la décision dans le &amp; Centre de sécurité conformité

1. Pour commencer, vous devez [accéder au centre de &amp; sécurité conformité](go-to-the-securitycompliance-center.md).
    
2. Dans le centre &amp; de sécurité conformité, accédez au **tableau de bord** **gestion** \> des menaces.
    
3. Dans la ligne **Insights** , recherchez la vue d’aide à la décision. Si vous avez activé l’aide à l’usurpation d’identité, l’analyse porte **sur les domaines usurpés dont l’authentification a échoué au cours des 30 derniers jours**. Si vous n’avez pas activé la protection contre les falsifications, l’aperçu vous invitera à le faire en utilisant le titre **activer la protection contre**les falsifications. 
    
## <a name="about-the-insight-on-the-dashboard"></a>À propos du tableau de bord

La vue d’analyse du tableau de bord vous montre des informations comme celles-ci.
  
![Capture d’écran d’un aperçu d’aide à la décision](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
Cette vue comprend deux modes:
  
 **Mode aperçu**. Si aucune stratégie de falsification n’est activée, le service d’aide à la décision indique le nombre de messages ayant été affectés par nos capacités d’aide à la falsification au cours des 30 derniers jours. 
  
 **Mode d’action**. Si aucune stratégie de falsification n’est activée, le service d’aide à la décision indique le nombre de messages qui *auraient* été affectés par nos capacités d’aide à la falsification au cours des 30 derniers jours. 
  
Dans les deux cas, les domaines usurpés affichés dans la vue sont séparés en deux catégories; paires de domaines suspectes et paires de domaines non suspectes. Ces catégories sont encore subdivisées en trois compartiments différents que vous pouvez examiner. 
  
Une *paire de domaine* est une combinaison de l’adresse «de:» et de l’infrastructure d’envoi. 
  
- L’adresse «de» est l’adresse de l’expéditeur par votre application de messagerie. Cette adresse identifie l’auteur du message. C’est-à-dire, la boîte aux lettres de la personne ou du système responsable de l’écriture du message. Elle est parfois appelée adresse 5322.From.
    
- L’infrastructure d’envoi, ou expéditeur, est le domaine de l’organisation de l’enregistrement PTR de l’adresse IP d’envoi. Si l’adresse IP d’envoi n’a pas d’enregistrement PTR, l’expéditeur est identifié par l’adresse IP d’envoi avec le masque de sous-réseau 255.255.255.0 dans la notation CIDR (/24). Par exemple, si l’adresse IP est 192.168.100.100, l’adresse IP complète de l’expéditeur est 192.168.100.100/24.
    
 Les **paires de domaines suspectes** sont les suivantes: 
  
- **Usurpation de confiance élevée**. Office 365 a reçu des signaux forts que ces domaines sont suspects, selon les modèles d’envoi historique et le score de réputation des domaines. Office 365 est très sûr que les domaines usurpent l’identité et que les messages envoyés à partir de ces domaines sont moins susceptibles d’être légitimes. 
    
- **Usurpation de confiance modérée**. Office 365 a reçu des signaux modérés que ces domaines sont suspects, en fonction des modèles d’envoi historiques et du score de réputation des domaines. Office 365 est modérément convaincu que les domaines sont des usurpations et que les messages envoyés à partir de ces domaines sont légitimes. Ce compartiment a plus de chances de contenir des faux positifs (FPs) que le compartiment d’usurpation de confiance élevée. 
    
 **Les paires de domaines non suspectes** incluent l' **usurpation d’identité**. Une usurpation de secours est un domaine dont les vérifications d’authentification explicites ont échoué ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)) mais qui ont transmis nos vérifications d’authentification étendues. Par conséquent, Office 365 a récupéré le courrier en votre nom et aucune action de détection d’usurpation d’identité n’a été effectuée sur le courrier. 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>Afficher des informations détaillées sur les paires de domaines suspectes à partir de l’aide à la décision

1. Sur la vue d’aide à la décision, cliquez sur l’une des paires de domaines (élevée, modérée ou de récupération).
  
La page **usurpation** d’aide s’affiche, indiquant la liste des expéditeurs qui envoient des messages non authentifiés dans votre organisation. Les informations contenues dans cette page vous permettent de déterminer si des messages falsifiés sont autorisés ou non, ou si vous devez effectuer des actions supplémentaires. Vous pouvez trier les informations par nombre de messages, la date de la dernière détection de l’usurpation, et bien plus encore. (Cliquez sur les en-têtes de colonne, par exemple **nombre de messages** ou **Dernière vue**, par exemple). 
    
2. Sélectionnez un élément dans le tableau pour ouvrir un volet de détails qui contient des informations détaillées sur la paire de domaines, notamment la raison pour laquelle nous l’avons détectée, ce que vous devez faire, un résumé de domaine, des données WhoIs sur l’expéditeur et des e-mails similaires que nous avons vus dans votre client du même expéditeur. À partir de là, vous pouvez également choisir d’ajouter ou de supprimer la paire de domaine de la liste des expéditeurs approuvés **AllowedToSpoof** . 
  
![Capture d’écran d’un domaine dans le volet d’informations d’aide à la décision](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>Ajouter ou supprimer un domaine de la liste des expéditeurs approuvés AllowedToSpoof

Vous ajoutez ou supprimez un domaine de la liste des expéditeurs approuvés AllowedToSpoof tout en vérifiant la paire de domaines dans le volet d’informations de la vue d’aide à la décision. Définissez simplement le bouton bascule en conséquence.
  
Cela modifie la combinaison de paires de domaines unique du domaine usurpé et de l’infrastructure d’envoi et ne fournit pas de couverture pour l’ensemble du domaine usurpé ou l’infrastructure d’envoi isolée. Par exemple, si vous ajoutez la paire de domaines suivante à la liste verte de l’expéditeur «AllowedToSpoof»: *domaine usurpé* «gmail.com» et l' *infrastructure d’envoi* «TMS *. mx.com»,* seul le courrier de cette paire de domaines sera autorisé à usurper. Les autres expéditeurs qui tentent d’usurper «gmail.com» et d’autres domaines que «tms.mx.com» tentent d’usurper continueront à être protégés par l’intelligence des usurpations d’identité. 
  
## <a name="related-topics"></a>Sujets associés

[En savoir plus sur l’usurpation d’identité](learn-about-spoof-intelligence.md)
  
[Protection anti-usurpation dans Office 365](anti-spoofing-protection.md)
  
[Procédure pas à pas. D’un tableau de bord à un aperçu](from-a-dashboard-to-an-insight.md)
  
[Procédure pas à pas. D’un rapport détaillé à un aperçu](from-a-detailed-report-to-an-insight.md)
  
[Procédure pas à pas. D’un aperçu à un rapport détaillé](from-an-insight-to-a-detailed-report.md)
  

