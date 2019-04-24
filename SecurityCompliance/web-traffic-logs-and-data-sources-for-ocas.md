---
title: Historique de trafic web et sources de données pour la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: La sécurité des applications Cloud Office 365 fonctionne avec les journaux de trafic Web provenant d'un large éventail de fournisseurs. Lisez cet article pour en savoir plus sur les journaux du trafic Web et les sources de données prises en charge pour Office 365 Cloud App Security.
ms.openlocfilehash: 67246ded0e3d39c81b5b906f753b91298309d1d8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32266849"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Historique de trafic web et sources de données pour la sécurité des applications cloud Office 365
  
|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étapes suivantes](#next-steps) <br/> |
  
Vous pouvez utiliser une large gamme de fichiers journaux de trafic Web et de sources de données avec Office 365 Cloud App Security. Toutefois, les fichiers journaux de votre trafic Web doivent inclure des informations spécifiques et être mis en forme d'une certaine façon afin qu'ils fonctionnent avec les rapports de découverte d'application de sécurité Cloud App Office 365 et le tableau de bord de découverte du Cloud. Utilisez cet article comme guide de référence pour les journaux de trafic Web et les sources de données que vous utiliserez avec la sécurité des applications Cloud Office 365.
  
> [!NOTE]
> Vous devez être un administrateur général, un administrateur de sécurité ou un lecteur de sécurité pour &amp; accéder au centre de sécurité conformité et à Office 365 Cloud App Security Portal. Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="web-traffic-log-requirements"></a>Exigences en matière de journal de trafic Web

Office 365 Cloud App Security utilise des données dans vos journaux de trafic Web pour vous aider à comprendre les applications utilisées par les personnes de votre organisation. Plus le nombre de détails inclus dans les fichiers journaux est important, plus l'activité de l'utilisateur sera meilleure.
  
Les sections suivantes répertorient les attributs nécessaires et les exigences supplémentaires pour les journaux de trafic Web afin qu'ils fonctionnent correctement avec la sécurité des applications Cloud Office 365.

### <a name="attributes"></a>Attributs

Office 365 Cloud App Security ne peut pas afficher ou analyser les attributs qui ne sont pas inclus dans vos journaux de trafic Web. Par exemple, le format de journal standard du pare-feu ASA Cisco n'a pas le nombre d'octets téléchargés par transaction, le nom d'utilisateur ou une URL cible (adresse IP cible uniquement). Par conséquent, ces attributs ne sont pas affichés dans les données de découverte de Cloud et la visibilité dans les applications Cloud est limitée. Pour les pare-feu ASA Cisco, le niveau d'information doit être défini sur 6. 

Les journaux de votre trafic Web doivent inclure les attributs suivants:

- Date de la transaction
- Adresse IP source
- Utilisateur source (fortement recommandé)
- Adresse IP de destination
- URL de destination (recommandé; Les URL offrent une plus grande précision pour la détection d'applications Cloud que les adresses IP.
- Quantité totale de données (recommandé; les informations de données sont très utiles)
- Quantité de données téléchargées ou transférées (recommandé; présentation des modèles d'utilisation de l'application Cloud)
- Action entreprise (autorisée ou bloquée)

### <a name="additional-requirements"></a>Autres conditions requises 

Outre les attributs répertoriés plus haut dans cet article, les journaux de votre trafic Web doivent répondre aux exigences suivantes:

- La source de données pour les fichiers journaux doit être prise en charge.
- Le format que les fichiers journaux utilisent doivent respecter le format standard. Une fois le fichier téléchargé, la découverte d'application vérifie cela.
- Les événements dans le journal doivent avoir eu lieu plus de 90 jours.
- Le fichier journal doit inclure les informations de trafic sortant pouvant être analysées pour l'activité réseau.
  
## <a name="data-attributes-for-different-vendors"></a>Attributs de données pour différents fournisseurs

Le tableau suivant récapitule les informations contenues dans les journaux du trafic Web de différents fournisseurs. **Veillez à vérifier auprès de votre fournisseur les informations les plus récentes.**


|                 Source de données                  |    URL de l'application cible    |    ADRESSE IP de l'application cible     |       Nom d’utilisateur       |      ADRESSE IP d'origine       |    Trafic total     |    Octets téléchargés    |
|----------------------------------------------|----------------------|----------------------|----------------------|----------------------|----------------------|----------------------|
|                  Barracuda                   | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |          Non          |          Non          |
|                  Couche bleue                   | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                  Point                  |          Non          | <strong>Oui</strong> |          Non          | <strong>Oui</strong> |          Non          |          Non          |
|              Cisco ASA (syslog)              |          Non          | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> |          Non          |
|           Cisco ASA avec un niveau de puissance           | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                  Cisco FWSM                  |          Non          | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> |          Non          |
|              Cisco IronPort WSA              | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                 Cisco Meraki                 | <strong>Oui</strong> | <strong>Oui</strong> |          Non          | <strong>Oui</strong> |          Non          |          Non          |
|           Clavister NGFW (syslog)            | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                SonicWall (anciennement Dell)                | <strong>Oui</strong> | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|            Arts numériques i-filtre             | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                  FortiGate                   |          Non          | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                 Genévriers SRX                  |          Non          | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                 Juniper SSG                  |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                  McAfee SWG                  | <strong>Oui</strong> |          Non          |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                    MS TMG                    | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|              Réseaux Palo Alto              |          Non          | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                    Sophos                    | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |          Non          |
|                Squid (commun)                | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> |          Non          | <strong>Oui</strong> |
|                Squid (natif)                | <strong>Oui</strong> |          Non          | <strong>Oui</strong> | <strong>Oui</strong> |          Non          | <strong>Oui</strong> |
| WebSens-rapport détaillé d'enquête (CSV) | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|    WebSense-journal d'activité Internet (CEF)    | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
|                   Zscaler                    | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> | <strong>Oui</strong> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>Pare-feu et proxys de fournisseur pris en charge

La sécurité des applications Cloud Office 365 prend en charge les proxys et les pare-feu suivants.
  
- Barracuda-Web App Firewall (W3C)  
- Journal d'accès SG pour proxy d'enrobage bleu (W3C)
- Point de contrôle
- Pare-feu ASA Cisco (veillez à définir le niveau d'informations sur 6)
- Cisco ASA avec un niveau de puissance   
- Cisco IronPort WSA
- Cisco ScanSafe
- Merkai de Cisco-URL
- Clavister NGFW (syslog)
- Arts numériques i-filtre
- Fortinet FortiGate
- Passerelle Cloud iboss sécurisée
- Genévriers SRX
- Juniper SSG
- McAfee Secure Web Gateway
- Microsoft Forefront Threat Management Gateway (W3C)
- Pare-feu Palo Alto Series
- SonicWALL (anciennement Dell)   
- Sophos SG
- Sophos XG
- Sophos Cyberoam
- Squid (commun)
- Squid (natif)
- WebSense-solutions de sécurité Web-rapport détaillé d'enquête (CSV)
- WebSense-solutions de sécurité Web-Journal d'activité Internet (CEF)
- Zscaler
    
> [!NOTE]
> Si une source de données que vous souhaitez utiliser n'est pas incluse ici, vous pouvez demander qu'elle soit ajoutée à la découverte d'application. Pour ce faire, lorsque vous créez un rapport, sélectionnez **autre** pour la **source de données**. Tapez ensuite le nom de la source de données que vous essayez de télécharger. Nous allons examiner le journal et vous indiquer si nous ajoutons la prise en charge de ce type de journal. Vous pouvez également [définir un analyseur personnalisé](https://docs.microsoft.com/cloud-app-security/custom-log-parser) correspondant à votre format. 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>Résoudre les erreurs lorsque les fichiers journaux sont téléchargés

Une fois que vous avez téléchargé les fichiers journaux du trafic Web, consultez le journal de gouvernance pour voir s'il y a eu des erreurs. S'il existe des erreurs, utilisez les informations du tableau ci-dessous pour résoudre ces erreurs.
  
|**Error**|**Description**|**Solution**|
|:-----|:-----|:-----|
|Type de fichier non pris en charge  <br/> |Le fichier téléchargé n'est pas un fichier journal valide. Par exemple, un fichier image.  <br/> |Téléchargez un fichier texte, zip ou gzip qui a été directement exporté à partir de votre pare-feu ou de votre proxy.  <br/> |
|Erreur interne  <br/> |Une défaillance de ressource interne a été détectée.  <br/> |Cliquez **** sur Réessayer pour réexécuter la tâche.  <br/> |
|Le format du journal ne correspond pas  <br/> |Le format de journal que vous avez téléchargé ne correspond pas au format de journal attendu pour cette source de données.  <br/> |
Vérifiez que le journal n'est pas endommagé. Comparez et associez le format du fichier journal au format d'exemple indiqué sur la page de chargement. |
|Les transactions sont datant de plus de 90 jours  <br/> |Toutes les transactions ont plus de 90 jours et sont donc ignorées.  <br/> |ExPortez un nouveau journal avec les événements récents et téléchargez-le à nouveau.  <br/> |
|Aucune transaction pour cataloguer les applications Cloud  <br/> |Aucune transaction n'est trouvée dans le journal pour les applications Cloud reconnues.  <br/> |Vérifiez que le journal contient des informations de trafic sortant.  <br/> |
|Type de journal non pris en charge  <br/> |Lorsque vous sélectionnez **Data source = Other (non pris en charge)**, le journal n'est pas analysé. Au lieu de cela, il est envoyé à la révision à l'équipe technique de [sécurité des applications Cloud de Microsoft](https://aka.ms/whatiscas) .  <br/> |L'équipe technique de [sécurité des applications Cloud de Microsoft](https://aka.ms/whatiscas) crée un analyseur dédié pour chaque source de données. Les sources de données les plus populaires sont déjà prises en charge. Lorsqu'une source de données non prise en charge est chargée, elle est examinée et ajoutée à la liste des nouveaux analyseurs de sources de données potentiels.  <br/> Lorsqu'un nouveau parseur est ajouté à la fonctionnalité, une notification est incluse dans les notes de publication de la sécurité des applications Cloud de Microsoft.  <br/> |
   
## <a name="next-steps"></a>Étapes suivantes

- [Passer en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Créer des rapports de découverte d'application](create-app-discovery-reports-in-ocas.md)
    
- [Examen des résultats de la découverte des applications](review-app-discovery-findings-in-ocas.md)
    
- [Examiner vos activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    

