---
title: Simulateur d’attaques dans Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: En tant qu’administrateur général Office 365, vous pouvez utiliser un simulateur d’attaque pour exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle ne touche votre entreprise.
ms.openlocfilehash: e72350fb8ca3ef8d7ed0218934097d2383f5ad53
ms.sourcegitcommit: ff370e93b792204547694139ef99bc0848304570
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36852776"
---
# <a name="attack-simulator-in-office-365"></a>Simulateur d’attaques dans Office 365

**Résumé** Si vous êtes un administrateur général Office 365 ou un administrateur de sécurité et que votre organisation a Office 365 Advanced Threat Protection Plan 2, qui inclut des [fonctionnalités d’enquête et de réponse aux menaces](office-365-ti.md), vous pouvez utiliser un simulateur d’attaque pour exécuter scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle n’influe sur votre ligne de base. Lisez cet article pour en savoir plus.
  
## <a name="the-attacks"></a>Les attaques

Trois types de simulations d’attaques sont actuellement disponibles :
  
- [Nom d’affichage-attaque de Spear Phishing](#display-name-spear-phishing-attack)

- [Attaque par pulvérisation de mot de passe](#password-spray-attack)

- [Attaque de mot de passe en force brute](#brute-force-password-attack)
    
Pour qu’une attaque réussisse, assurez-vous que le compte que vous utilisez pour exécuter des attaques simulées utilise l’authentification multifacteur. En outre, vous devez être un administrateur général Office 365 ou un administrateur de sécurité. (Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de conformité des & de sécurité Office 365](permissions-in-the-security-and-compliance-center.md).)
    
Pour accéder à un simulateur d’attaque &amp; , dans le centre de sécurité conformité, sélectionnez **Threat Management** \> **Attack Simulator**.
  
## <a name="before-you-begin"></a>Avant de commencer...

Assurez-vous que vous et votre organisation remplissez les conditions requises suivantes pour le simulateur d’attaque :
      
- Le courrier électronique de votre organisation est hébergé dans Exchange Online. (Le simulateur d’attaque n’est pas disponible pour les serveurs de messagerie locaux.)
    
- Vous êtes un administrateur général Office 365 ou un administrateur de sécurité
    
- L' [authentification multifacteur/l’accès conditionnel](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide) est activé, pour au moins le compte administrateur général Office 365 et les administrateurs de sécurité qui utiliseront un simulateur d’attaque. (Idéalement, l’accès à plusieurs facteurs/accès conditionnel est activé pour tous les utilisateurs de votre organisation.)
 
- Votre organisation dispose d' [Office 365 Advanced Threat Protection Plan 2](office-365-atp.md), avec un simulateur d’attaque &amp; visible dans le centre de sécurité conformité (allez sur **Threat Management** \> **Attack Simulator**)

    ![Gestion des menaces-simulateur d’attaque](media/ThreatMgmt-AttackSimulator.png)

## <a name="display-name-spear-phishing-attack"></a>Nom d’affichage-attaque de Spear Phishing

Le hameçonnage est un terme générique pour une suite d’attaques classées comme une attaque de style d’ingénierie sociale. Cette attaque est axée sur le Spear Phishing, une attaque plus ciblée, dirigée par un groupe spécifique de personnes ou une organisation. En règle générale, une attaque personnalisée avec une reconnaissance a été effectuée et utilise un nom complet qui générera une approbation dans le destinataire, comme un message électronique qui semble provenir d’un cadre de votre organisation.
  
Cette attaque est axée sur la possibilité de manipuler le nom d’affichage et l’adresse source du message. Lorsque les attaques de Spear Phishing sont réussies, cyberattackers accéder aux informations d’identification des utilisateurs.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>Pour simuler une attaque par hameçonnage (Spear Phishing)

![Composer le corps du message électronique](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Vous pouvez concevoir l’éditeur HTML enrichi directement dans le champ de **corps du message** lui-même ou utiliser la source HTML.
  
1. Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.
    
2. Spécifiez un nom de campagne significatif pour l’attaque ou sélectionnez un modèle. 

    ![Page de démarrage du hameçonnage](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Spécifiez les destinataires cibles. Il peut s’agir d’individus ou de groupes au sein de votre organisation. Chaque destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online pour que l’attaque aboutisse. 

    ![Sélection de destinataires](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Configurez les détails du courrier électronique de hameçonnage. 

    ![Configurer les détails du courrier électronique](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
    
    La mise en forme HTML peut être aussi complexe ou basique que les besoins de votre campagne. Comme le format du message est HTML, vous pouvez insérer des images et du texte pour améliorer la convivialité. Vous avez le contrôle sur ce à quoi ressemblera le message reçu dans le client de messagerie de réception.
    
5. Spécifiez le texte du champ **de (nom)** . Il s’agit du champ qui indique le **nom d’affichage** dans le client de messagerie de réception. 
    
6. Spécifiez le texte ou le champ **de** . Il s’agit du champ qui indique comme adresse de messagerie de l’expéditeur dans le client de messagerie de réception.

    Vous pouvez entrer un espace de noms de messagerie existant dans votre organisation (en procédant ainsi à la résolution de l’adresse de messagerie dans le client de réception, ce qui facilite un modèle d’approbation très élevée) ou vous pouvez entrer une adresse de messagerie externe. L’adresse de messagerie que vous spécifiez n’a pas besoin d’exister réellement, mais elle doit suivre le format d’une adresse SMTP valide, telle `user@domainname.extension`que. 
  
7. À l’aide du sélecteur de liste déroulante, sélectionnez une URL de serveur de connexion d’hameçonnage reflétant le type de contenu que vous aurez au sein de votre attaque. Plusieurs URL à thèmes vous sont proposées, telles que livraison de documents, technique, paie, etc. Il s’agit en fait de l’URL sur laquelle les utilisateurs ciblés sont invités à cliquer.
    
8. Spécifiez une URL de page d’accueil personnalisée. Cette opération permet de rediriger les utilisateurs vers une URL que vous spécifiez à la fin d’une attaque réussie. Si vous avez une formation interne à la sensibilisation, par exemple, vous pouvez spécifier cela ici.
    
9. Spécifiez le texte du champ **Subject** . Il s’agit du champ qui indique le **nom** de l’objet dans le client de messagerie de réception. 
    
10. Composez le **corps du message électronique** que la cible recevra. 

    `${username}`insère le nom des cibles dans le corps du message électronique. 

    `${loginserverurl}`insère l’URL sur laquelle les utilisateurs cibles doivent cliquer 
    
11. Choisissez **suivant,** puis **Terminer** pour lancer l’attaque. Le message électronique de Spear Phishing est remis aux boîtes aux lettres de vos destinataires cibles. 
    
## <a name="password-spray-attack"></a>Attaque par pulvérisation de mot de passe

Une attaque par pulvérisation de mot de passe contre une organisation est généralement utilisée après qu’un acteur incorrect a réussi à acquérir une liste d’utilisateurs valides du client. L’acteur incorrect connaît les mots de passe courants que les personnes utilisent. Il s’agit d’une attaque très utilisée, car il s’agit d’une attaque bon marché à exécuter et plus difficile à détecter que les approches en force.
  
Cette attaque est axée sur la possibilité de spécifier un mot de passe commun pour un grand nombre d’utilisateurs cibles.
  
### <a name="to-simulate-a-password-spray-attack"></a>Pour simuler une attaque par pulvérisation de mot de passe

1. Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.
    
2. Spécifiez un nom de campagne significatif pour l’attaque.
    
3. Spécifiez les destinataires cibles. Il peut s’agir d’individus ou de groupes au sein de votre organisation. Un destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online pour que l’attaque réussisse.
    
4. Spécifiez un mot de passe à utiliser pour l’attaque. Par exemple, vous pouvez essayer un mot de passe courant et `Summer2019`pertinent. Un autre peut `Fall2019`être ou `Password1`.
    
5. Cliquez sur **Terminer** pour lancer l’attaque. 
    
## <a name="brute-force-password-attack"></a>Attaque de mot de passe en force brute

Une attaque de mot de passe en force contre une organisation est généralement utilisée après qu’un acteur incorrect a réussi à acquérir une liste d’utilisateurs clés auprès du client. Cette attaque consiste à essayer un ensemble de mots de passe sur le compte d’un seul utilisateur.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>Pour simuler une attaque de mot de passe en force brute

1. Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.
    
2. Spécifiez un nom de campagne significatif pour l’attaque.
    
3. Spécifiez le destinataire cible. Un destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online pour que l’attaque réussisse.
    
4. Spécifiez un ensemble de mots de passe à utiliser pour l’attaque. Pour ce faire, vous pouvez utiliser un fichier texte (. txt) pour votre liste de mots de passe. Le fichier texte ne peut pas dépasser 10 Mo dans la taille du fichier. Utilisez un mot de passe par ligne et assurez-vous d’inclure un retour à la ligne après le dernier mot de passe de votre liste.
    
5. Cliquez sur **Terminer** pour lancer l’attaque. 
    
## <a name="new-features-in-attack-simulator"></a>Nouvelles fonctionnalités dans un simulateur d’attaque

De nouvelles fonctionnalités ont récemment été ajoutées au simulateur d’attaques. Ces approches sont les suivantes :

- Fonctionnalités de création de rapports avancées. La possibilité d’afficher des données telles que le temps le plus rapide (ou le plus lent) pour ouvrir un message électronique de simulation d’attaque, le temps le plus rapide (ou le plus lent) de cliquer sur un lien dans le message, ainsi que davantage de visualisations.

- Éditeur de modèles de courrier électronique. La possibilité de créer un modèle de courrier électronique personnalisé réutilisable que vous pouvez utiliser pour les simulations d’attaque ultérieures.

- Importation de destinataires CSV. La possibilité d’utiliser un fichier. csv pour importer votre liste de destinataires cible au lieu d’utiliser le sélecteur de carnet d’adresses.

De nouvelles fonctionnalités sont bientôt disponibles pour les simulateurs d’attaques. Ces approches sont les suivantes :

- Simulation d’hameçonnage de la charge utile des pièces jointes. Possibilité d’utiliser une pièce jointe comme charge utile pour la simulation de hameçonnage à la place d’une URL.

Consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) pour découvrir les éléments en cours de développement, le déploiement et les fonctionnalités déjà lancées.

## <a name="see-also"></a>Voir aussi

[Description du service Office 365 - Protection avancée contre les menaces](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)

[Office 365 protection avancée contre les menaces](office-365-atp.md)



