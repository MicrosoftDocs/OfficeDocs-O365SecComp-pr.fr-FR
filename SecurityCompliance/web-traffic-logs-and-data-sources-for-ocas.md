---
title: Sources de journaux et de données de trafic Office 365 nuage sécurité des applications Web
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: Office 365 Cloud application sécurité fonctionne avec les journaux de trafic web à partir d’un large éventail de fournisseurs. Lisez cet article pour en savoir plus sur les journaux de trafic web et prise en charge des sources de données Office 365 nuage sécurité des applications.
ms.openlocfilehash: 09b0358e0d8b9a6ed59393d8771237f7eaf8bb98
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528197"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Sources de journaux et de données de trafic Office 365 nuage sécurité des applications Web
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](#next-steps) <br/> |
  
Vous pouvez utiliser un large éventail de sources de données et fichiers journaux de trafic web avec Office 365 Cloud Application Security. Toutefois, vos fichiers journaux de trafic web doivent inclure des informations spécifiques et être mis en forme une certaine façon afin qu’elles fonctionnent avec Office 365 Cloud application sécurité application de rapports de découverte et le tableau de bord de découverte dans le nuage. Utilisez cet article comme un guide de référence pour les journaux de trafic web et les sources de données que vous utiliserez avec Office 365 Cloud Application Security.
  
> [!NOTE]
> Vous devez être un administrateur global, un administrateur de sécurité ou un lecteur de sécurité pour la sécurité d’accès &amp; portail centre de conformité et de sécurité d’application Office 365 dans le nuage. Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="web-traffic-log-requirements"></a>Exigences de journal du trafic Web

À l’aide de données d’utilise Office 365 Cloud application sécurité dans les journaux de trafic web pour vous aider à comprendre les applications de personnes dans votre organisation. Plus de détails sont inclus dans les fichiers journaux, la meilleure visibilité vous aurez activité de l’utilisateur.
  
Le tableau suivant répertorie les conditions requises et les attributs qui sont nécessaires pour les journaux de trafic web fonctionne correctement avec Office 365 Cloud application sécurité :
  
|**Attributs**|**Autres conditions requises **|
|:-----|:-----|
| Date de la transaction  <br/>  Adresse IP source  <br/>  Utilisateur source (recommandé)  <br/>  Adresse IP de destination  <br/>  URL de destination (recommandé : URL fournissent plus précise de détection d’application cloud que les adresses IP)  <br/>  Quantité totale de données (recommandées)  <br/>  Quantité de téléchargement ou transfert de données (recommandé : fournit des modèles d’application d’utilisation détails sur le nuage)  <br/>  Action effectuée (autorisées ou bloquées)  <br/> | La source de données pour les fichiers journaux doit être pris en charge.  <br/>  Le format à qu'utilisent les fichiers journaux doit respecter le format standard. Lorsque le fichier est téléchargé, détection d’application vérifie ce.  <br/>  Les événements dans le journal doivent avoir eu lieu il y a pas plus de 90 jours.  <br/>  Le fichier journal doit inclure les informations de trafic sortant qui peuvent être analysées pour l’activité réseau.  <br/> |
   
Si les attributs ne sont pas inclus dans les journaux sont chargés, sécurité pour application Cloud Microsoft Office 365 ne peuvent pas afficher ou analyser les informations pour vous. Par exemple, format de journal standard du pare-feu Cisco ASA n’inclut pas le nombre d’octets téléchargés par transaction, le nom d’utilisateur ou une URL cible (uniquement une adresse IP cible). Étant donné que ces informations n’est pas dans les fichiers journaux de Cisco, Office 365 Cloud application sécurité ne sont pas l’inclure lors de l’analyse du trafic réseau de votre organisation.
  
> [!NOTE]
> Pour certains types de pare-feu, vous devez définir un niveau d’informations pour les journaux de trafic web inclure les attributs obligatoires. Par exemple, Cisco ASA pare-feu doivent être le niveau d’information définie sur 6. Veillez à vérifier que votre pare-feu est définis pour fournir les informations appropriées dans les journaux de trafic web. 
  
## <a name="data-attributes-for-different-vendors"></a>Attributs pour les différents fournisseurs de données
<a name="BKMK_LogAndData"> </a>

Le tableau suivant récapitule les informations contenues dans les journaux de trafic web à partir de divers fournisseurs. **Vérifiez avec votre fournisseur pour les informations les plus récentes.**
  
|**Source de données**|**URL d’application cible**|**IP d’application cible**|**Username**|**Origine IP**|**Trafic total**|**Octets téléchargés**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Barracuda  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |Non  <br/> |
|REVÊTEMENT bleu  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Point de contrôle  <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |Non  <br/> |
|Cisco ASA  <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |
|Cisco FWSM  <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |
|Cisco Ironport WSA  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Cisco Meraki  <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |Non  <br/> |
|Clavister Conviction (journal système)  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Dell SonicWall  <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Fortigate  <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Juniper SRX  <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Juniper SSG  <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|McAfee SWG  <br/> |**Oui** <br/> |Non  <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Meraki (Cisco)  <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |Non  <br/> |Non  <br/> |
|Microsoft Threat Management Gateway  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Palo Alto Networks  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Sophos  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |
|SqUID (Common)  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |
|SqUID (natif)  <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |**Oui** <br/> |Non  <br/> |**Oui** <br/> |
|Websense - rapport sur le détail investigation (CSV)  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Websense - journal d’activité Internet (format CEF)  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
|Zscaler  <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |**Oui** <br/> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>Pare-feu de fournisseur pris en charge et des proxys
<a name="BKMK_Supported"> </a>

Sécurité d’application Office 365 Cloud prend en charge les proxys et les pare-feu suivants.
  
- Barracuda - pare-feu de l’application Web (W3C)
    
- Bleu revêtement Proxy administratives - journal d’accès (W3C)
    
- Point de vérification
    
- Cisco ASA pare-feu (Notez que vous devez définir le niveau d’informations sur 6)
    
- Cisco IronPort WSA
    
- Cisco ScanSafe
    
- Ouvrez une session Cisco Merkai - URL
    
- Dell Sonicwall
    
- Fortinet Fortigate
    
- Juniper SRX
    
- Juniper SSG
    
- Passerelle Web sécurisée de McAfee
    
- Microsoft Forefront Threat Management Gateway (W3C)
    
- Série Palo Alto pare-feu
    
- Sophos administratives
    
- Sophos Cyberoam
    
- SqUID (Common)
    
- SqUID (natif)
    
- Rapport sur le détail investigation Websense - Solutions de sécurité Web - (CSV)
    
- Journal d’activité Websense - Solutions de sécurité Web - Internet (format CEF)
    
- Zscaler
    
> [!NOTE]
> Si une source de données que vous souhaitez utiliser n’est pas incluse ici, vous pouvez demander à ajouter à la découverte de l’application. Pour cela, lorsque vous créez un rapport, sélectionnez **autre** pour la **source de données**. Puis tapez le nom de la source de données que vous essayez de télécharger. Nous allons consulter le journal et vous permettent de savoir si nous ajoutons prise en charge pour ce type de journal. 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>Résoudre les erreurs lorsque les fichiers journaux sont téléchargés.

Après avoir téléchargé les fichiers journaux du trafic web, consultez le journal de gouvernance pour voir si des erreurs. S’il existe des erreurs, utilisez les informations dans le tableau suivant pour résoudre ces erreurs.
  
|**Erreur**|**Description**|**Résolution**|
|:-----|:-----|:-----|
|Type de fichier non pris en charge  <br/> |Le fichier téléchargé n’est pas un fichier journal valide. Par exemple, un fichier image.  <br/> |Téléchargez un zip, fichier texte ou gzip qui a été exporté directement à partir de votre pare-feu ou votre proxy.  <br/> |
|Erreur interne  <br/> |Un échec de ressource interne a été détecté.  <br/> |Cliquez sur **Réessayer** pour réexécuter la tâche.  <br/> |
|Le format de journal ne correspond pas à  <br/> |Le format de journal que vous avez téléchargé ne correspond pas le format attendu journal pour cette source de données.  <br/> |
Vérifiez que le journal n’est pas endommagé. Comparer et correspond au format de fichier journal à l’exemple de format indiqué dans la page de téléchargement. |
|Les transactions sont plus de 90 jours  <br/> |Toutes les transactions datant de plus de 90 jours et par conséquent, sont ignorées.  <br/> |Exporter un nouveau journal des événements récents et télécharger à nouveau.  <br/> |
|Aucune transaction aux applications dans le nuage de catalogue  <br/> |Aucune transaction à des applications dans le nuage reconnu ne se trouvent dans le journal.  <br/> |Vérifiez que le journal contient des informations sur le trafic sortant.  <br/> |
|Type de journal non pris en charge  <br/> |Lorsque vous sélectionnez **source de données = autres (non pris en charge)**, le journal n’est pas analysé. Au lieu de cela, il est envoyé pour révision à l’équipe technique [Microsoft Cloud Application Security](https://aka.ms/whatiscas) .<br/> |L’équipe technique [Microsoft Cloud Application Security](https://aka.ms/whatiscas) génère un analyseur dédié pour chaque source de données. Sources de données les plus populaires sont déjà pris en charge. Lorsqu’une source de données non pris en charge est téléchargée, il est passé en revue et ajouté à la liste des éventuels nouveaux analyseurs de source de données.<br/> Lorsqu’un nouvel analyseur est ajouté à la fonctionnalité, une notification est incluse dans les notes de publication Microsoft Cloud Application Security.  <br/> |
   
## <a name="next-steps"></a>Étapes suivantes

- [Passez en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Créer des rapports de détection d’application](create-app-discovery-reports-in-ocas.md)
    
- [Passez en revue les résultats de la détection d’application](review-app-discovery-findings-in-ocas.md)
    
- [Passez en revue vos activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)
    

