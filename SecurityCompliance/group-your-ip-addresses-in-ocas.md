---
title: Grouper vos adresses IP pour simplifier la gestion dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Pour identifier facilement les ensembles d'adresses IP que vous utiliserez dans Office 365 Cloud App Security, comme vos adresses IP de bureau physiques, vous pouvez configurer des groupes de plages d'adresses IP.
ms.openlocfilehash: b8f5c1dd46b2e3990d53a65881d12ca8f3961b16
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220444"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>Grouper vos adresses IP pour simplifier la gestion dans la sécurité des applications cloud Office 365
  
|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étapes suivantes](#next-steps) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
Pour identifier facilement les ensembles d'adresses IP que vous utiliserez dans Office 365 Cloud App Security, comme vos adresses IP de bureau physiques, vous pouvez configurer des groupes de plages d'adresses IP. La définition de ces plages vous permet de baliser et de classer celles-ci, puis vous pouvez utiliser des balises et des catégories pour personnaliser l'affichage et l'analyse des journaux d'activité et des alertes.
  
Chaque groupe de plages d'adresses IP peut être balisé avec des noms de balises que vous choisissez, puis les balises peuvent être classées en fonction d'une liste de catégories IP par défaut (par exemple, entreprise, administratif, risqué et VPN). Les adresses IPv4 et IPv6 sont prises en charge.
  
> [!NOTE]
> Vous devez être un administrateur général ou un administrateur de sécurité pour effectuer les procédures décrites dans cet article. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>Pour configurer une plage d'adresses IP dans Office 365 Cloud App Security

1. En tant qu'administrateur général ou administrateur de sécurité, accédez au portail de sécurité des[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)applications Cloud () et connectez-vous.
    
2. En haut à droite de la page, cliquez sur **plages d'adresses IP**des **paramètres** \> .<br>![Dans la sécurité des applications Cloud Office 365, sélectionnez les paramètres permettant d'accéder aux paramètres du système et des données.](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)<br>
  
3. Cliquez sur le bouton nouveau, qui ressemble à un signe plus **+**().
    
4. Dans la fenêtre **nouvelle plage d'adresses IP** , spécifiez les valeurs suivantes: 
    
|**Champ ou liste**|**Procédure**|
|:-----|:-----|
|**Nom** <br/> |Utilisez ce champ pour gérer votre plage d'adresses IP et vos paramètres. (Cette valeur ne s'affiche pas dans les journaux des activités.)  <br/> |
|**Plages d'adresses IP** <br/> |Spécifiez une plage à l'aide de la notation de préfixe réseau (également appelée notation CIDR). Par exemple, 192.168.1.0/27 inclut la plage de valeurs 192.168.1.0 à 192.168.1.31 (inclus).  <br/> |
|**Emplacement** et **fournisseur de services Internet inscrit** <br/> |Spécifiez l'emplacement et le fournisseur de services Internet (ISP) pour la plage d'adresses IP. Cela remplace les champs publics définis pour les adresses, ce qui est utile dans les cas, par exemple une adresse IP est considérée comme publique pour être en Irlande, mais en réalité aux États-Unis.  <br/> |
|**Tags** <br/> |Utilisez des balises pour nommer vos groupes d'adresses IP. (Contrairement au champ nom, des balises s'affichent dans les journaux d'activité.) Tapez un mot ou une expression que vous souhaitez utiliser pour une balise. Vous pouvez ajouter autant de balises que vous le souhaitez pour chaque plage d'adresses IP. Si vous avez déjà configuré une balise et que vous souhaitez y ajouter cette plage d'adresses IP, sélectionnez-la dans la liste des balises actuelles qui apparaissent lorsque vous commencez à taper.  <br/> |
|**Catégorie** <br/> | Affecter des catégories à vos balises pour faciliter la reconnaissance des activités provenant de certaines adresses IP. Choisissez l'une des options suivantes:<br/> **Administrative** Toutes les adresses IP de vos administrateurs.  <br/> **Fournisseur de Cloud** Adresse IP de votre proxy dans le Cloud.  <br/> **Entreprise** Toutes les adresses IP de votre réseau interne, de vos succursales et de vos adresses d'itinérance Wi-Fi.  <br/> **Risqué** Toutes les adresses IP que vous considérez comme risquées, telles que les adresses IP suspectes que vous avez vues dans le passé, les adresses IP des réseaux de vos concurrents, et ainsi de suite. Par défaut, les catégories à risque incluent deux balises IP: **proxy anonyme** et **TDR** <br/> **VPN** Toutes les adresses IP que vos employés distants utilisent.  <br/> |
   
7. Sélectionnez **Save (Enregistrer)**.
    
Une fois que vous avez configuré vos plages d'adresses IP, gardez à l'esprit que seuls les événements futurs sont affectés par ces modifications.
  
## <a name="next-steps"></a>Étapes suivantes

- [Stratégies d'activité et alertes](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies](anomaly-detection-policies-in-ocas.md)
    
- [Intégration de votre serveur SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365](review-office-365-cas-alerts.md)
    

