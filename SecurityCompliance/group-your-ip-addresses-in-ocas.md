---
title: Groupe vos adresses IP pour simplifier la gestion de sécurité d’application Office 365 dans le nuage
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Pour facilement identifier les ensembles d’adresses IP que vous utiliserez dans Office 365 Cloud application sécurité, telles que vos adresses IP office physiques, vous pouvez définir des groupes de plages d’adresses IP.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527523"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>Groupe vos adresses IP pour simplifier la gestion de sécurité d’application Office 365 dans le nuage
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](#next-steps) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
Pour facilement identifier les ensembles d’adresses IP que vous utiliserez dans Office 365 Cloud application sécurité, telles que vos adresses IP office physiques, vous pouvez définir des groupes de plages d’adresses IP. Définition permet de ces plages de balise et de les classer et puis vous pouvez utiliser des balises et catégories pour personnaliser la façon dont votre activité de journaux et alertes sont affichés et examinés.
  
Chaque groupe de plages d’adresses IP permettre être marqué avec des noms de balise que vous choisissez, puis les balises peuvent être classées selon une liste par défaut des catégories IP (tels que l’entreprise, d’administration, Risky et VPN). Les adresses IPv4 et IPv6 sont prises en charge.
  
> [!NOTE]
> Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer les procédures dans cet article. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>Pour configurer une plage d’adresses IP dans Office 365 Cloud Application Security

1. En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. (Cela vous amène à la sécurité &amp; centre de conformité.) 
    
2. Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.
    
3. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Dans l’angle supérieur droit de la page, cliquez sur **paramètres** \> **plages d’adresses IP**.
    
    ![Dans O365 Cloud application sécurité, choisissez Paramètres pour accéder à vos paramètres système et des données](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. Cliquez sur le bouton Nouveau, ce qui ressemble à un signe plus ( **+**).
    
6. Dans la fenêtre de la **plage d’adresses IP nouveau** , spécifiez les valeurs suivantes : 
    
|**Champ ou une liste**|**Procédure**|
|:-----|:-----|
|**Nom** <br/> |Ce champ permet de gérer votre plage d’adresses IP et les paramètres. (Vous ne verrez pas cette valeur dans les journaux d’activités).  <br/> |
|**Plages d'adresses IP** <br/> |Spécifiez une plage, en utilisant la notation de préfixe réseau (également appelé la notation CIDR). Par exemple, 192.168.1.0/27 inclut la plage de valeurs 192.168.1.0 via 192.168.1.31 (inclus).  <br/> |
|**Emplacement** et **inscrit le fournisseur de services Internet** <br/> |Pour la plage d’adresses IP, spécifiez l’emplacement et le fournisseur de services (Internet). Ce paramètre remplace les champs publics définis pour les adresses, qui est utile pour les cas, tel qu’une adresse IP est qui est considéré comme publiquement en Irlande mais est réellement aux États-Unis.  <br/> |
|**Tags** <br/> |Utiliser des balises de nommer vos groupes d’adresses IP. (Contrairement au champ nom, vous verrez des balises aux journaux d’activité.) Tapez un mot ou expression que vous souhaitez utiliser pour une balise. Vous pouvez ajouter autant de balises que vous le souhaitez pour chaque plage d’adresses IP. Et si vous avez déjà configuré une balise et que vous souhaitez ajouter cette plage d’adresses IP, sélectionnez-le dans la liste des balises actives qui apparaissent lorsque vous commencez à taper.  <br/> |
|**Catégorie** <br/> | Assigner des catégories à vos balises pour faciliter l’accès à reconnaître les activités qui proviennent des adresses IP. Choisissez parmi les options suivantes :<br/> **D’administration** Toutes les adresses IP de vos administrateurs.  <br/> **Fournisseur de nuage** L’adresse IP de votre serveur proxy dans le nuage.  <br/> **D’entreprise** Toutes l’adresses IP dans votre réseau interne, vos succursales et vos adresses itinérants Wi-Fi.  <br/> **Risquée** Toutes les adresses IP que vous considérez à présenter des risques, tels que des adresses IP suspecte que vous ont indiqué dans le passé, les adresses IP dans les réseaux de vos concurrents et ainsi de suite. Par défaut, les catégories risquées inclut deux balises IP : **proxy anonyme** et **Tor** <br/> **Réseau privé virtuel** Toutes les adresses IP qui utilisent votre travailleurs à distance.  <br/> |
   
7. Sélectionnez **Enregistrer**.
    
Après avoir configuré vos plages d’adresses IP, n’oubliez pas que les événements futurs uniquement sont affectés par ces modifications.
  
## <a name="next-steps"></a>Étapes suivantes

- [Alertes et des stratégies d’activité](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies](anomaly-detection-policies-in-ocas.md)
    
- [Intégrer votre serveur SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Passez en revue et effectuer une action sur les alertes de sécurité pour application Cloud Microsoft Office 365](review-office-365-cas-alerts.md)
    

