---
title: Simulateur d’attaques dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/09/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: En tant qu’administrateur global Office 365, vous pouvez utiliser attaque Simulator pour exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et de rechercher des utilisateurs vulnérables avant une attaque réelle accède à votre entreprise.
ms.openlocfilehash: 9a7e1fd5327b4a764356df110c46ee7a9f496b53
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706438"
---
# <a name="attack-simulator-in-office-365"></a>Simulateur d’attaques dans Office 365

**Résumé** Si vous êtes un administrateur global d’Office 365 et votre organisation dispose [d’Informations sur les menaces Office 365](office-365-ti.md), vous pouvez utiliser l’attaque Simulator pour exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et de rechercher des utilisateurs vulnérables avant une attaque réelle a un impact sur la ligne du bas. Lisez cet article pour en savoir plus.
  
## <a name="the-attacks"></a>Attaque

Trois types de simulations attaque sont actuellement disponibles :
  
- [Afficher l’attaque par hameçonnage de la sonde de nom](attack-simulator.md#spearphish)
    
- [Attaque par mot de passe-Jet](attack-simulator.md#passwordspray)
    
- [Attaque par mot de passe en force brute](attack-simulator.md#bruteforce)
    
Pour une attaque à lancer avec succès, vous utilisez l’authentification multifacteur sur le compte que vous utilisez pour exécuter des attaques simulés. En outre, vous devez être un administrateur global d’Office 365.
  
> [!NOTE]
> Prise en charge pour l’accès conditionnel seront prochainement disponibles. 
  
Pour accéder aux Simulator attaque, dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.
  
## <a name="before-you-begin"></a>Avant de commencer...

Assurez-vous que vous et votre organisation satisfaire les conditions suivantes pour attaque Simulator :
      
- Courrier électronique de votre organisation est hébergée dans Exchange Online. (Attaque Simulator n’est pas disponible pour les serveurs de messagerie sur site).
    
- Vous êtes un administrateur global d’Office 365
    
- Votre organisation utilise [l’authentification multifacteur pour les utilisateurs d’Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication&view=o365-worldwide)
 
- Votre organisation a des [Menaces Office 365](office-365-ti.md)avec attaque Simulator visibles dans la sécurité &amp; centre de conformité (accédez à **gestion de menace** \> **simulator attaque**)<br/>![Gestion des menaces - Simulator attaque](media/ThreatMgmt-AttackSimulator.png)

    
## <a name="display-name-spear-phishing-attack"></a>Afficher l’attaque par hameçonnage de la sonde de nom

L’hameçonnage est un terme générique pour une vaste gamme d’attaques classés comme une attaque de style d’ingénierie sociale. Cette attaque se concentre sur la tentative de phishing, une attaque ciblée plus qui est destinée à un groupe spécifique d’individus ou d’une organisation. En règle générale, une attaque personnalisée avec certains reconnaissance effectuée et à l’aide d’un nom d’affichage qui génère de confiance dans le destinataire, par exemple un message électronique qui semble provenir d’un responsable au sein de votre organisation.
  
Cette attaque se concentre sur ce qui vous permet de manipuler les le message semble provenir d’en modifiant l’adresse de source et de nom complet. Lorsque les attaques par phishing de la sonde réussissent, cybercriminels accéder aux informations d’identification des utilisateurs.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>Pour simuler une attaque par hameçonnage de la sonde

![Composez le corps du message électronique](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Vous pouvez concevoir l’éditeur HTML enrichi directement dans le champ **corps du message électronique** lui-même ou travailler avec la source HTML. Il existe deux champs importants pour inclusion dans le code HTML : 
  
1. Dans la [sécurité &amp; centre de conformité](https://security.microsoft.com), cliquez sur **Gestion des menaces** \> **simulator attaque**.
    
2. Spécifiez un nom de campagne explicite pour l’attaque ou sélectionnez un modèle. <br/>![Page de démarrage de hameçonnage](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Chaque destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse. <br/>![Sélectionner les destinataires](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Configurez les détails de messagerie hameçonnage. <br/>![Configurer les paramètres de messagerie](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/>La mise en forme HTML peut être complexe ou base en fonction des besoins votre campagne. Comme c’est le format de courrier HTML, vous pouvez insérer des images et du texte pour améliorer la believability. Vous pouvez contrôler à quoi ressemblera le message reçu dans le client de messagerie de réception.
    
5. Spécifier le texte du champ **de (nom)** . Il s’agit le champ qui indique le **Nom complet** dans le client de messagerie de réception. 
    
6. Spécifiez le texte ou **le champ** . Il s’agit le champ qui indique que l’adresse de messagerie de l’expéditeur dans le client de messagerie de réception.<br/>Vous pouvez entrer un espace de noms de messagerie existant au sein de votre organisation (Cela permettra l’adresse de messagerie résout dans le client du destinataire, emprunter un modèle de confiance très élevé), ou vous pouvez entrer une adresse de messagerie externe. L’adresse de messagerie que vous spécifiez ne doit pas réellement existe, mais il est nécessaire après le format d’une adresse SMTP valide, tel que user@domainname.extension. 
  
7. Le sélecteur de liste déroulante, sélectionnez une URL du serveur de connexion hameçonnage qui reflète le type de contenu que vous aurez au sein de votre attaque. Vous permet de sélectionner, telles que les salaires technique, de documents de remise, etc., plusieurs URL à thème sont fournies. C’est effectivement qui cible les utilisateurs sont invités à cliquer sur l’URL.
    
8. Spécifiez une URL de page d’accueil personnalisée. L’utilisation de cette redirection des utilisateurs à une URL que vous spécifiez à la fin d’une attaque. Si vous avez des formations internes, par exemple, vous pouvez spécifier qu’ici.
    
9. Spécifiez le texte pour le champ **objet** . Il s’agit le champ qui indique que le **Nom de l’objet** dans le client de messagerie de réception. 
    
10. Composez le **corps du message électronique** qui sera envoyé à la cible. <br/>`${username}`Insère le nom de cibles dans le corps du courrier électronique. <br/>`${loginserverurl}`Insérer l’URL que nous voulons cibler les utilisateurs à cliquer sur 
    
11. Cliquez sur **suivant,** puis sur **Terminer** pour lancer l’attaque. Le message électronique de phishing sonde est remis aux boîtes aux lettres des destinataires de votre cible. 
    
## <a name="password-spray-attack"></a>Attaque par mot de passe-Jet

Une attaque par jet de mot de passe par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a acquis avec succès une liste d’utilisateurs valides à partir du client. L’acteur mauvaise connaît les mots de passe courants que les employés d’utilisation. Il s’agit d’une attaque largement utilisée, comme il s’agit d’une attaque à exécuter et plus difficiles à détecter que les attaques en force approches peu coûteuse.
  
Cette attaque se concentre sur ce qui vous permet de spécifier un mot de passe courants par rapport à une base de grande taille cible des utilisateurs.
  
### <a name="to-simulate-a-password-spray-attack"></a>Pour simuler une attaque par mot de passe-Jet

1. Dans la [sécurité &amp; centre de conformité](https://security.microsoft.com), cliquez sur **Gestion des menaces** \> **simulator attaque**.
    
2. Spécifiez un nom de campagne explicite de l’attaque.
    
3. Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.
    
4. Spécifier un mot de passe à utiliser pour l’attaque. Par exemple, un mot de passe de courantes et pertinent vous pouvez essayer est `Fall2017`. Un autre peut être `Spring2018`, ou `Password1`.
    
5. Cliquez sur **Terminer** pour lancer l’attaque. 
    
## <a name="brute-force-password-attack"></a>Attaque par mot de passe en force brute

Une attaque par mot de passe en force brute par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a acquis avec succès une liste d’utilisateurs clés à partir du client. Cette attaque se concentre sur la tentative d’un ensemble de mots de passe sur un seul compte d’utilisateur.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>Pour simuler une attaque par mot de passe en force brute

1. Dans la [sécurité &amp; centre de conformité](https://security.microsoft.com), cliquez sur **Gestion des menaces** \> **simulator attaque**.
    
2. Spécifiez un nom de campagne explicite de l’attaque.
    
3. Spécifiez le destinataire cible. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.
    
4. Spécifiez un ensemble de mots de passe à utiliser pour l’attaque. Vous pouvez utiliser un fichier texte (.txt) pour votre liste de mots de passe. Le fichier texte ne peut pas dépasser 10 Mo dans la taille du fichier. Utilisez un mot de passe par ligne et veillez à inclure un retour chariot après le dernier mot de passe dans votre liste.
    
5. Cliquez sur **Terminer** pour lancer l’attaque. 
    
## <a name="new-features-in-attack-simulator"></a>Nouvelles fonctionnalités d’attaque Simulator

Nouvelles fonctionnalités sont ajoutées à une attaque Simulator. Cela inclut :
- **Options avancées de fonctionnalités de création de rapports**. Vous serez en mesure de voir les données telles que l’heure plus rapide (ou plus lent) pour ouvrir un message électronique de simulation attaque, l’heure plus rapide (ou plus lent) à cliquer sur un lien dans le message et bien plus encore.
- **Éditeur de modèle de courrier électronique**. Vous pouvez créer un modèle de courrier électronique personnalisés et réutilisables que vous pouvez utiliser pour les simulations attaque future.

Visitez le site de la [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) pour voir les nouveautés dans le développement et déploiement de ce qui est déjà lancé.



