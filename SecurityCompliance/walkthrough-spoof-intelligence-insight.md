---
title: Procédure pas à pas présente les aide à la décision usurpation d’identité
ms.author: krowley
author: kccross
ms.date: 7/30/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
description: Découvrez comment fonctionne le mieux d’aide à la décision usurpation d’identité.
ms.openlocfilehash: ca9c4ae6f2d65ef2700a2e02acd5b4f1dfbfe903
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22596093"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>Procédure pas à pas : présente les aide à la décision usurpation d’identité

À l’aide de l’aperçu usurpation d’identité aide à la décision, vous pouvez rapidement déterminer les expéditeurs sont envoyer légitimement que vous non authentifié e-mail. En leur permettant d’envoyer des messages usurpés, vous pouvez réduire le risque de n’importe quel faux positifs accédant à vos utilisateurs.
  
En outre, vous pouvez également utiliser l’analyseur d’aide à la décision usurpation d’identité et gérer les paires de domaines autorisés pour fournir une couche supplémentaire de sécurité et pour empêcher les messages non sécurisés d’arriver dans votre organisation.
  
Vous pouvez utiliser l’aperçu d’aide à la décision usurpation d’identité de la sécurité &amp; centre de conformité si votre compte professionnel ou de l’école a reçu les autorisations de lecture de sécurité, administrateur de sécurité ou administrateur général Office 365. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
  
Si vous utilisez pour [des rapports et des vues d’ensemble de sécurité Office 365 &amp; centre de conformité](reports-and-insights-in-security-and-compliance.md), il peut vous aider à voir comment vous pouvez accéder facilement à partir d’un tableau de bord à un aperçu et les actions recommandées.
  
Vous pouvez afficher l’insight d’aide à la décision usurpation d’identité plus d’un tableau de bord dans la sécurité &amp; centre de conformité. Quel que soit le tableau de bord que vous examinez l’insight fournit les mêmes détails et permet d’effectuer rapidement les mêmes tâches.
  
Il s’agit d’une des procédures pas à pas plusieurs pour la sécurité &amp; centre de conformité. Sur la navigation dans les rapports et les vues d’ensemble, voir les procédures dans la section Rubriques connexes.
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>Obtention de l’aperçu d’aide à la décision usurpation d’identité dans la sécurité &amp; centre de conformité

1. Pour commencer, vous devez [accédez à la sécurité &amp; centre de conformité](go-to-the-securitycompliance-center.md).
    
2. Dans la sécurité &amp; centre de conformité, accédez à la **Gestion des menaces** \> **tableau de bord.**
    
3. Dans la ligne **Insights** , recherchez l’aperçu d’aide à la décision usurpation d’identité. Si vous avez activé les aide à la décision usurpation d’identité, puis l’aperçu est autorisé **Spoofed domaines qui Échec de l’authentification au cours des 30 derniers jours**. Si vous n’avez pas activé la protection d’usurpation d’identité, puis l’insight vous invitera à le faire à l’aide de **l’Activer la Protection contre l’usurpation**de titre. 
    
## <a name="about-the-insight-on-the-dashboard"></a>À propos de l’aperçu du tableau de bord

L’aperçu du tableau de bord affiche des informations comme suit.
  
![Capture d’écran de détail d’aide à la décision usurpation d’identité](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
Cet aperçu offre deux modes :
  
 **En mode Aperçu**. Si vous avez activé toute stratégie d’usurpation d’identité, puis l’aperçu vous montre le nombre de messages électroniques ont été affectés par nos fonctions d’aide à la décision usurpation d’identité au cours des 30 derniers jours. 
  
 **Que se passe-t-il si le mode**. Si vous n’avez pas activé toute stratégie d’usurpation d’identité, puis l’aperçu montre combien e-mails *serait* ont été affectées par nos fonctions d’aide à la décision usurpation d’identité au cours des 30 derniers jours. 
  
Les deux cas, les domaines usurpés affichés dans l’aperçu sont séparés en deux catégories ; les paires de domaine suspects et paires de domaine non suspects. Ces catégories sont subdivisés en trois différents compartiments à examiner. 
  
Une *paire de domaine* est une combinaison de la « à partir de : « adresse et l’infrastructure d’envoi. 
  
- L’adresse « De » est l’adresse affiché comme adresse par votre application de messagerie. Cette adresse identifie l’auteur du message électronique. Autrement dit, la boîte aux lettres de la personne ou le système chargé d’écrire le message. Il est parfois appelée l’adresse 5322.From.
    
- L’infrastructure envoi ou l’expéditeur, est le domaine d’organisation de l’enregistrement PTR de l’adresse IP d’envoi. Si l’adresse IP d’envoi a pas d’enregistrement PTR, alors que l’expéditeur est identifié par l’émetteur IP avec le 255.255.255.0 masque de sous-réseau dans la notation CIDR (/ 24). Par exemple, si l’adresse IP est 192.168.100.100 l’adresse IP complète de l’expéditeur est 192.168.100.100/24.
    
 **Les paires de domaine suspects** sont les suivantes : 
  
- **Usurpation d’identité fiables**. Office 365 a reçu un signal puissant ces domaines sont suspectes, basé sur les modèles d’envoi historiques et le score de réputation des domaines. Office 365 est très convaincu que les domaines sont l’usurpation d’identité et que les messages envoyés à partir de ces domaines sont moins susceptibles d’être légitime. 
    
- **Usurpation d’identité confiance modéré**. Office 365 reçu signaux modérés ces domaines sont suspectes, en fonction des modèles envoi historiques et le score de réputation des domaines. Office 365 est Moyennement certain que les domaines sont l’usurpation d’identité et que les messages envoyés à partir de ces domaines sont légitimes. Ce compartiment a plus de chances de contenant de faux positifs (i/s) à la plage de l’usurpation d’identité fiables. 
    
 **Les paires de domaine suspects-non** inclure **récupéré usurpation d’identité**. Usurpation d’identité récupérée sont des domaines qui ont échoué les vérifications d’authentification explicites ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)) mais transmis vérifie authentification étendue. Par conséquent, Office 365 a récupéré les messages de votre part et aucune action anti-usurpation a été effectuée sur le courrier. 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>Afficher des informations détaillées sur les paires de domaine suspects à partir de l’aperçu d’aide à la décision usurpation d’identité

1. Dans l’aperçu d’aide à la décision usurpation d’identité, cliquez sur une des paires de domaine (élevés, modérés ou récupérés).
  
La page de **Détail d’aide à la décision usurpation d’identité** apparaît avec la liste des expéditeurs qui sont l’envoi du courrier non authentifié dans votre organisation. Les informations sur cette page vous permettent de déterminer si les messages usurpés sont autorisés ou non ou si vous devez prendre des mesures. Vous pouvez trier les informations par le nombre de messages, la date de que dernière détection l’usurpation d’identité, et bien plus encore. (Cliquez sur les en-têtes de colonne, telles que **Message compter** ou **dernière détection**, par exemple.) 
    
2. Sélectionnez un élément dans la table pour ouvrir le volet de détails qui contient des informations complètes sur la paire de domaine, y compris pourquoi nous détecter, ce que vous devez faire un récapitulatif de domaine, les données WhoIs sur l’expéditeur et que nous avons trouvé dans votre client de l’expéditeur même les messages électroniques similaires. À partir de là, vous pouvez également choisir d’ajouter ou de supprimer la paire de domaine de la liste des expéditeurs approuvés **AllowedToSpoof** . 
  
![Capture d’écran d’un domaine dans le volet de détails insight usurpation d’identité aide à la décision](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>Ajouter ou supprimer un domaine de la liste des expéditeurs approuvés AllowedToSpoof

Vous ajoutez ou supprimez un domaine à partir de la liste des expéditeurs approuvés AllowedToSpoof lors de la révision de la paire de domaine dans le volet détails de l’aperçu d’aide à la décision usurpation d’identité. Définissez simplement la bascule en conséquence.
  
Cela modifie la combinaison de paire domaine unique du domaine usurpé et l’infrastructure d’envoi et ne fournit pas de couverture pour l’intégralité du domaine usurpé ou de l’infrastructure d’envoi de manière isolée. Par exemple, si vous ajoutez la paire de domaine suivant à l’expéditeur 'AllowedToSpoof' autoriser liste : *Usurpation de domaine* « gmail.com » et *L’envoi d’une Infrastructure* « mémoires *. mx.com »,* alors que les messages à partir de la paire de ce domaine seront autorisés à usurper. Autres expéditeurs d’essayer d’usurper « gmail.com » et les autres domaines que « tms.mx.com » tentative d’usurpation continuera à être protégées à l’aide à la décision usurpation d’identité. 
  
## <a name="related-topics"></a>Voir aussi

[Pour plus d’informations sur l’aide à la décision usurpation d’identité](learn-about-spoof-intelligence.md)
  
[L’usurpation d’identité contre la protection dans Office 365](anti-spoofing-protection.md)
  
[Procédure pas à pas - à partir d’un tableau de bord pour un aperçu](from-a-dashboard-to-an-insight.md)
  
[Procédure pas à pas - à partir d’un rapport détaillé d’une analyse](from-a-detailed-report-to-an-insight.md)
  
[Procédure pas à pas - à partir d’un aperçu à un rapport détaillé](from-an-insight-to-a-detailed-report.md)
  

