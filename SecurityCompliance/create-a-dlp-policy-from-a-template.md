---
title: Création d'une stratégie DLP à partir d'un modèle
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'La plus simple et la plus courante pour prendre en main les stratégies DLP consiste à utiliser un des modèles inclus dans Office 365. '
ms.openlocfilehash: 4e3a5d731538e4998858b5f9f7a296c43e6774ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528156"
---
# <a name="create-a-dlp-policy-from-a-template"></a>Création d'une stratégie DLP à partir d'un modèle

La plus simple et la plus courante pour prendre en main les stratégies DLP consiste à utiliser un des modèles inclus dans Office 365. Vous pouvez utiliser une de ces modèles est, ou personnaliser les règles pour répondre aux exigences de conformité spécifiques de votre organisation.
  
Office 365 comprend plus de 40 modèles prêts à l’emploi qui peuvent vous aider à répondre à toute une variété de besoins réglementaires et professionnels courants en matière de stratégies. Par exemple, il existe des modèles de stratégie DLP pour :
  
- La loi Gramm-Leach-Bliley Act (GLBA)
    
- La norme Payment Card Industry Data Security Standard (PCI-DSS)
    
- Les informations d’identification personnelle aux États-Unis (U.S. PII)
    
- La loi Health Insurance Act (HIPAA) aux États-Unis
    
Vous pouvez affiner un modèle en modifiant les règles existantes ou en ajoutant de nouvelles règles. Par exemple, vous pouvez ajouter de nouveaux types d’informations sensibles à une règle, modifier les décomptes dans une règle pour rendre son déclenchement plus facile ou plus difficile, permettre aux utilisateurs de remplacer les actions d’une règle en fournissant une justification ou modifier les destinataires des notifications et des rapports d’incident. Un modèle de stratégie DLP est un point de départ flexible pour de nombreux scénarios de conformité courants.
  
Vous pouvez également choisir le modèle personnalisé, sans règle par défaut, et configurer votre stratégie DLP de A à Z, pour répondre aux exigences de conformité spécifiques de votre organisation.
  
## <a name="example-identify-sensitive-information-across-all-onedrive-for-business-sites-and-restrict-access-for-people-outside-your-organization"></a>Exemple : Identifier les informations sensibles sur OneDrive tous les sites de commerce et restreindre l’accès des personnes extérieures à votre organisation

OneDrive entreprise comptes facilitent des personnes dans votre organisation de collaborer et de partager des documents. Mais un intérêt commun pour les responsables de la conformité est que les informations sensibles stockées dans OneDrive pour les comptes de l’entreprise peuvent être partagées par inadvertance avec des personnes extérieures à votre organisation. Une stratégie DLP permet de réduire le risque.
  
Dans cet exemple, vous allez créer une stratégie DLP qui identifie les données PII US, qui inclut les numéros de passeport individuels contribuable Identification numéros (ITIN), les numéros de sécurité sociale et US. Vous aidera à l’aide d’un modèle, puis vous allez modifier le modèle pour répondre aux exigences de conformité de votre organisation, en particulier, vous devez :
  
- Ajoutez deux types de numéros de compte bancaire sensibles information—U.S. et licence de permis de conduire américain, afin que la stratégie DLP protège davantage de vos données sensibles.
    
- Rendre plus élevé, la stratégie de sorte qu’une seule occurrence d’informations sensibles soit suffisant pour restreindre l’accès des utilisateurs externes.
    
- Autoriser les utilisateurs à remplacer les actions en fournissant une justification ou un faux positif de création de rapports. De cette manière, votre stratégie DLP ne sont pas empêcher des personnes dans votre organisation d’accéder à leur travail, pourvu qu’ils disposent d’un motif valide pour le partage des informations sensibles.
    
### <a name="create-a-dlp-policy-from-a-template"></a>Création d'une stratégie DLP à partir d'un modèle

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école. Vous êtes maintenant dans la sécurité Office 365 &amp; centre de conformité.
    
3. Dans la sécurité &amp; centre de conformité \> barre de navigation gauche \> **prévention des pertes de données** \> **stratégie** \> **+ créer une stratégie**.
    
    ![Créer un bouton de la stratégie](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Choisissez le modèle de stratégie DLP qui protège les types d’informations sensibles que vous devez \> **suivant**.
    
    Dans cet exemple, vous devez sélectionner **confidentialité** \> **US personnellement identifiables informations personnelles données** parce qu’il inclut déjà la plupart des types d’informations sensibles que vous souhaitez protéger, vous ajouterez plus tard quelques. 
    
    Lorsque vous sélectionnez un modèle, vous pouvez lire la description sur la droite pour en savoir plus qui protège les types d’informations sensibles le modèle.
    
    ![Page choix d’un modèle de stratégie DLP](media/775266f6-ad87-4080-8d7c-97f2e7403b30.png)
  
5. Nom de la stratégie \> **suivant**.
    
6. Pour choisir les emplacements que vous voulez que la stratégie DLP protéger, effectuez l’une des opérations suivantes :
    
  - Choisissez **tous les emplacements dans Office 365** \> **suivant**.
    
  - Sélectionnez **me laisser choisir les emplacements spécifiques** \> **suivant**. Cet exemple, choisissez cette option.
    
    Pour inclure ou exclure un emplacement complet tel que tout le courrier Exchange ou tous les comptes de OneDrive, activer ou désactiver la l' **état** de cet emplacement. 
    
    Pour inclure uniquement certains sites SharePoint ou OneDrive pour les comptes d’entreprise, activer l' **état** , puis cliquez sur les liens sous **inclure** à choisir des comptes ou des sites spécifiques. Lorsque vous appliquez une stratégie à un site, les règles configurées dans cette stratégie sont automatiquement appliqués à tous les sous-sites de ce site. 
    
    ![Options pour les emplacements dans lesquels une stratégie DLP peut être appliquée](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
    Dans cet exemple, pour protéger les informations sensibles stockées dans tous les OneDrive for Business des comptes, désactiver l' **état** de **messagerie Exchange** et **les sites SharePoint**et conservez l' **état** sur pour les **comptes OneDrive**.
    
7. Choisissez **d’utiliser les paramètres avancés** \> **suivant**.
    
8. Un modèle de stratégie DLP contient des règles prédéfinies avec des conditions et actions pour détecter et agissent sur des types spécifiques d’informations sensibles. Vous pouvez modifier, supprimer, ou désactiver les règles existantes ou ajouter de nouveaux. Lorsque vous avez terminé, cliquez sur **suivant**.
    
    ![Règles d’étendue dans le modèle de stratégie nous PII](media/3bc9f1b6-f8ad-4334-863a-24448bb87687.png)
  
    Dans cet exemple, le modèle de données d’identification personnelle US comprend deux règles prédéfinies :
    
  - **Faible volume de contenu détecté PII US** Cette règle recherche les fichiers contenant entre 1 et 10 occurrences de chacun des trois types d’informations sensibles (ITIN, SSN et US numéros de passeport), où les fichiers sont partagés avec des personnes en dehors de l’organisation. Si trouvée, la règle envoie une notification par courrier électronique à l’administrateur de collection de site principal, propriétaire du document, et la dernière personne à avoir modifié le document. 
    
  - **Un volume important de contenu détecté PII US** Cette règle recherche les fichiers contenant au moins 10 occurrences de chacun des mêmes trois types d’informations sensibles, où les fichiers sont partagés avec des personnes en dehors de l’organisation. Si trouvé, cette action envoie également une notification par courrier électronique, ainsi que sa limite l’accès au fichier. Pour le contenu dans un compte professionnel OneDrive, cela signifie que les autorisations pour le document sont réservées pour tout le monde sauf les administrateur de collection de sites principal, le propriétaire du document et la personne qui a modifié le document. 
    
    Pour répondre aux besoins spécifiques de votre organisation, vous souhaiterez peut-être faciliter les règles déclencheur, afin qu’une seule occurrence d’informations sensibles est suffisante pour bloquer l’accès des utilisateurs externes. Après avoir examiné ces règles, comprendre que vous n’avez pas besoin de règles du nombre élevé et faible, vous avez besoin qu’une seule règle qui bloque l’accès si toutes les occurrences d’informations sensibles sont trouvée.
    
    Afin que vous développez la règle nommée **faible volume de contenu détecté PII US** \> **Supprimer la règle**.
    
    ![Supprimer une règle](media/bc36f7d2-0fae-4af1-92e8-95ba51077b12.png)
  
9. Maintenant, dans cet exemple, vous devez pour ajouter les deux types d’informations sensibles (numéros de compte bancaire US et les numéros de licence de permis de conduire américain), autoriser les utilisateurs de remplacer une règle et modifier le nombre de n’importe quelle occurrence. Vous pouvez faire tout cela de modifier une règle, sélectionnez **un volume important de contenu détecté PII US** \> **Modifier la règle**.
    
    ![Modifier une règle](media/eaf54067-4945-4c98-8dd6-fb2c5d6de075.png)
  
10. Pour ajouter un type d’informations sensibles, dans la section **Conditions** \> **Ajouter ou modifier des types**. Ensuite, sous **Ajouter ou modifier des types** \> , choisissez **Ajouter** \> sélectionner le **Numéro de compte bancaire US** et **Numéro de permis de conduire américain** \> **Ajouter** \> **terminé**.
    
    ![Permet d’ajouter ou modifier des types](media/c6c3ae86-f7db-40a8-a6e4-db11692024be.png)
  
    ![Ajouter ou modifier le volet types](media/fdbb96af-b914-4a6c-a97b-bbd014689965.png)
  
11. Pour modifier le nombre (le nombre d’instances d’informations sensibles nécessaire pour déclencher la règle), sous le **nombre d’instances** \> choisir la valeur **minimale** pour chaque type de \> entrez 1. Le nombre minimal ne peut pas être vide. Le nombre maximal peut être vide ; une valeur vide **max** convertir **n’importe quel**.
    
    Lorsque vous avez terminé, le nombre minimum de tous les types d’informations sensibles doit être **1** et le nombre maximal doit être **n’importe quel**. En d’autres termes, toutes les occurrences de ce type d’informations sensibles répondront à cette condition.
    
    ![Compteurs d’instance pour les types d’informations sensibles](media/5c6e08cb-59a9-4558-b54b-d899836d4737.png)
  
12. Pour la personnalisation finale, vous ne voulez pas que vos stratégies DLP pour empêcher les personnes de leur travail lorsqu’ils ont une justification valide ou que vous rencontrent un faux positif, afin que vous voulez la notification utilisateur incluent des options pour remplacer l’action de blocage.
    
    Dans la section **notifications d’utilisateur** , vous pouvez voir que les notifications par courrier électronique et les conseils de stratégie sont allumés par défaut de cette règle dans le modèle. 
    
    Dans la section **substitutions par l’utilisateur** , vous pouvez voir que substitutions pour justifier sont activées, mais substitutions à signaler faux positifs ne sont pas. Choisissez **Remplacer la règle automatiquement si elles signalement comme faux positif**.
    
    ![Section de notifications par utilisateur et l’utilisateur remplace la section](media/62720e7a-a939-4c03-b414-67748f3d64a0.png)
  
13. En haut de l’éditeur de règle, modifiez le nom de cette règle par défaut **un volume important de contenu détecté US PII** à **n’importe quel contenu détecté avec US PII** car il est désormais déclenché par toutes les occurrences de types d’informations sensibles. 
    
14. En bas de l’éditeur de règles \> **Enregistrer**.
    
15. Passez en revue les conditions et les actions de cette règle \> **suivant**.
    
    Sur la droite, notez **l’état** basculer de la règle. Si vous désactivez une stratégie entière, toutes les règles contenues dans la stratégie sont également désactivés. Toutefois, ici vous pouvez désactiver une règle spécifique sans désactiver entièrement. Cela peut être utile lorsque vous avez besoin d’une règle qui génère un grand nombre de faux positifs étudier la question. 
    
16. Dans la page suivante, lire et comprendre les points suivants, puis choisissez s’il faut activer la règle ou tester extraire au préalable \> **suivant**.
    
     Avant de créer vos stratégies DLP, vous devez envisager de les déployer progressivement pour évaluer leur impact et tester leur efficacité avant de vous les appliquer pleinement. Par exemple, vous ne voulez pas qu’une nouvelle stratégie DLP involontairement bloquer l’accès à des milliers de documents qui nécessitent des personnes afin d’effectuer leur travail. 
    
    Si vous créez des stratégies DLP ayant un impact potentiel volumineux, nous vous recommandons de cet ordre :
    
17. Démarrez en mode test sans conseil de stratégie, puis utilisez les rapports DLP pour évaluer l’impact. Vous pouvez utiliser les rapports DLP pour connaître le nombre, l’emplacement, le type et la gravité des correspondances de stratégie. En fonction des résultats, vous pouvez affiner les règles, si nécessaire. En mode test, les stratégies DLP n’auront aucun impact sur la productivité des personnes qui travaillent dans votre organisation. 
    
18. Passez en mode test avec notifications et conseils de stratégie pour commencer à faire découvrir vos stratégies de conformité aux utilisateurs et les préparer pour les règles qui vont être appliquées. À ce stade, vous pouvez également demander aux utilisateurs de signaler les faux positifs afin d’affiner les règles.
    
19. Activer les stratégies afin que les règles sont appliquées et le contenu de le protégé. Continuez à surveiller les rapports DLP et tous les rapports d’incidents ou notifications pour vous assurer que les résultats sont ce que vous prévoyez. 
    
    ![Options pour l’utilisation du mode de test et l’activation de la stratégie](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
20. Passez en revue vos paramètres de cette stratégie \> choisissez **créer**.
    
Après avoir créé et activer une stratégie DLP, il est déployé sur les sources de contenu qui inclut, tels que des sites SharePoint Online ou OneDrive pour les comptes de l’entreprise, dont la stratégie commence automatiquement appliquer ses règles sur ce contenu.
  
## <a name="view-the-status-of-a-dlp-policy"></a>Affichage de l’état d’une stratégie DLP

À tout moment, vous pouvez afficher l’état de vos stratégies DLP dans la page de **stratégie** dans la section de **prévention des pertes de données** de la sécurité &amp; centre de conformité. Vous trouverez ici des informations importantes, telles que si une stratégie a été correctement activée ou désactivée, ou si la stratégie est en mode test. 
  
Voici les différents états et leur signification.
  
|**État**|**Explication**|
|:-----|:-----|
|**Activation en cours...** <br/> |La stratégie est déployée pour les sources de contenu qu’elle contient. La stratégie n’est pas encore appliquée sur toutes les sources.  <br/> |
|**Test en cours, avec notifications** <br/> |La stratégie est en mode test. Les actions dans une règle ne sont pas appliquées, mais les correspondances de stratégie sont collectées et peuvent être consultées à l’aide des rapports DLP. Les notifications sur les correspondances de stratégie sont envoyées aux destinataires spécifiés.  <br/> |
|**Test en cours, sans notifications** <br/> |La stratégie est en mode test. Les actions dans une règle ne sont pas appliquées, mais les correspondances de stratégie sont collectées et peuvent être consultées à l’aide des rapports DLP. Les notifications sur les correspondances de stratégie ne sont pas envoyées aux destinataires spécifiés.  <br/> |
|**Activé** <br/> |La stratégie est appliquée et active. La stratégie a été correctement déployée sur toutes ses sources de contenu.  <br/> |
|**Désactivation en cours...** <br/> |La stratégie est supprimée des sources de contenu qu’elle contient. La stratégie peut être toujours active et appliquée sur certaines sources. La désactivation d’une stratégie peut prendre jusqu’à 45 minutes.  <br/> |
|**Désactivé** <br/> |La stratégie n’est pas active et n’est pas appliquée. Les paramètres de la stratégie (sources, mots clés, durée, etc.) sont enregistrés.  <br/> |
|**Suppression…** <br/> |La stratégie est en cours de suppression. La stratégie n’est pas active et n’est pas appliquée.  <br/> |
   
## <a name="turn-off-a-dlp-policy"></a>Désactivation d’une stratégie DLP

Vous pouvez modifier ou désactiver une stratégie DLP à tout moment. Désactivation d’une stratégie désactive toutes les règles dans la stratégie.
  
Pour modifier ou désactiver une stratégie DLP, dans la page **stratégie** \> sélectionnez la stratégie \> **Modifier la stratégie**.
  
![Modifier le bouton de la stratégie](media/ce319e92-0519-44fe-9507-45a409eaefe4.png)
  
En outre, vous pouvez désactiver chaque règle individuellement en modifiant la stratégie et en basculant sur Désactiver l' **état** de la règle, comme indiqué ci-dessus. 
  
## <a name="more-information"></a>Plus d'informations

- [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md)
    
- [Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md)
    
- [Création d’une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés](protect-documents-that-have-fci-or-other-properties.md)
    
- [Ce qu’incluent les modèles de stratégie DLP](what-the-dlp-policy-templates-include.md)
    
- [Inventaire des types d'informations sensibles](what-the-sensitive-information-types-look-for.md)
    

