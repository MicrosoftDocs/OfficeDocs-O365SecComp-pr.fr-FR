---
title: Attaque Simulator dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/19/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Découvrez trois différents types d’attaques informatiques que vous pouvez exécuter à l’aide d’attaque Simulator.
ms.openlocfilehash: 364144c0b2f8109c67fb262ce879414088380ebe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527837"
---
# <a name="attack-simulator-in-office-365"></a>Attaque Simulator dans Office 365

Avec attaque Simulator (inclus dans [Office 365 menaces](office-365-ti.md)), si vous êtes membre de l’équipe de sécurité de votre organisation, vous pouvez exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et de rechercher des utilisateurs vulnérables avant une attaque réelle a un impact sur la ligne du bas.
  
## <a name="the-attacks"></a>Attaque

Au niveau de la version d’évaluation, nous vous proposons trois types de simulations attaque que vous pouvez exécuter :
  
- [Afficher l’attaque par hameçonnage de la sonde de nom](attack-simulator.md#spearphish)
    
- [Attaque par mot de passe-Jet](attack-simulator.md#passwordspray)
    
- [Attaque par mot de passe en force brute](attack-simulator.md#bruteforce)
    
Pour une attaque à lancer avec succès, le compte qui exécute l’attaque et ouvert une session doit utiliser l’authentification multifacteur.
  
> [!NOTE]
> Prise en charge pour l’accès conditionnel seront prochainement disponibles. 
  
Pour accéder aux Simulator attaque, dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.
  
## <a name="before-you-begin"></a>Avant de commencer...

Assurez-vous que vous et votre organisation satisfaire les conditions suivantes pour attaque Simulator :
  
- Votre organisation a des [Menaces Office 365](office-365-ti.md)avec attaque Simulator visibles dans la sécurité &amp; centre de conformité (accédez à **gestion de menace** \> **simulator attaque**)
    
- Courrier électronique de votre organisation est hébergée dans Exchange Online. (Attaque Simulator n’est pas disponible pour les serveurs de messagerie sur site).
    
- Vous êtes un administrateur global d’Office 365
    
- Votre organisation utilise [l’authentification multifacteur pour les utilisateurs d’Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="display-name-spear-phishing-attack"></a>Afficher l’attaque par hameçonnage de la sonde de nom

L’hameçonnage est un terme générique pour une vaste gamme d’attaques classés comme une attaque de style d’ingénierie sociale. Cette attaque se concentre sur la tentative de phishing, une attaque ciblée plus qui est destinée à un groupe spécifique d’individus ou d’une organisation. En règle générale, une attaque personnalisée avec certains reconnaissance effectuée et à l’aide d’un nom d’affichage qui génère de confiance dans le destinataire, par exemple un message électronique qui semble provenir d’un responsable au sein de votre organisation.
  
Cette attaque se concentre sur ce qui vous permet de manipuler les le message semble provenir d’en modifiant l’adresse de source et de nom complet. Lorsque les attaques par phishing de la sonde réussissent, cybercriminels accéder aux informations d’identification des utilisateurs.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>Pour simuler une attaque par hameçonnage de la sonde

![Composez le corps du message électronique](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Vous pouvez concevoir l’éditeur HTML enrichi directement dans le champ **corps du message électronique** lui-même ou travailler avec la source HTML. Il existe deux champs importants pour inclusion dans le code HTML : 
  
1. Dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.
    
2. Spécifiez un nom de campagne explicite pour l’attaque ou sélectionnez un modèle.
    
    ![Page de démarrage de hameçonnage](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.
    
    ![Sélectionner les destinataires](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Configurez les détails de messagerie hameçonnage.
    
    ![Configurer les paramètres de messagerie](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    La mise en forme HTML peut être complexe ou base en fonction des besoins votre campagne. Comme c’est HTML, vous pouvez insérer des images et du texte pour améliorer la believability. Vous pouvez contrôler à quoi ressemblera le message reçu dans le client de messagerie de réception.
    
1. Entrez le texte du champ **de (nom)** . Il s’agit le champ qui indique le **Nom complet** dans le client de messagerie de réception. 
    
2. Entrez le texte ou **le champ** . Il s’agit le champ qui indique que l’adresse de messagerie de l’expéditeur dans le client de messagerie de réception. 
    
    > [!IMPORTANT]
    > Vous pouvez entrer un espace de noms de messagerie existant au sein de votre organisation (Cela permettra l’adresse de messagerie résout dans le client du destinataire, emprunter un modèle de confiance très élevé), ou vous pouvez entrer une adresse de messagerie externe. L’adresse de messagerie que vous spécifiez ne doit pas réellement existe, mais il est nécessaire après le format d’une adresse SMTP valide, tel que user@domainname.extension. 
  
3. Le sélecteur de liste déroulante, sélectionnez une URL du serveur de connexion hameçonnage qui reflète le type de contenu que vous aurez au sein de votre attaque. Vous permet de sélectionner, telles que les salaires technique, de documents de remise, etc., plusieurs URL à thème sont fournies. C’est effectivement qui cible les utilisateurs sont invités à cliquer sur l’URL.
    
4. Entrez une URL de page d’accueil personnalisée. L’utilisation de cette redirection des utilisateurs à une URL que vous spécifiez à la fin d’une attaque. Si vous avez des formations internes, par exemple, vous pouvez spécifier qu’ici.
    
5. Entrez le texte pour le champ **objet** . Il s’agit le champ qui indique que le **Nom de l’objet** dans le client de messagerie de réception. 
    
5. Composez le **corps du message électronique** qui sera envoyé à la cible. 
  
 **${nom_utilisateur}** insère le nom de cibles dans le corps 
  
 **${loginserverurl}** insère l’URL que nous voulons cibler les utilisateurs à cliquer sur 
    
6. Cliquez sur **suivant,** puis sur **Terminer** pour lancer l’attaque. Le message électronique de phishing sonde est remis aux boîtes aux lettres des destinataires de votre cible. 
    
## <a name="password-spray-attack"></a>Attaque par mot de passe-Jet

Une attaque par jet de mot de passe par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a énuméré correctement une liste d’utilisateurs valides à partir du client, en utilisant leurs connaissances de mots de passe courants utilisés. Il est utilisé largement tel qu’il s’agit d’une attaque peu coûteuse pour exécuter et plus difficile à détecter que les attaques en force approches.
  
Cette attaque se concentre sur ce qui vous permet de spécifier un mot de passe courants par rapport à une base de grande taille cible des utilisateurs.
  
### <a name="to-simulate-a-password-spray-attack"></a>Pour simuler une attaque par mot de passe-Jet

1. Dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.
    
2. Spécifiez un nom de campagne explicite de l’attaque.
    
3. Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.
    
4. Spécifier un mot de passe à utiliser pour l’attaque. Par exemple, un mot de passe de courantes et pertinent vous pouvez essayer est `Fall2017`. Un autre peut être `Spring2018`, ou `Password1`.
    
5. Cliquez sur **Terminer** pour lancer l’attaque. 
    
## <a name="brute-force-password-attack"></a>Attaque par mot de passe en force brute

Une attaque par mot de passe en force brute par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a énuméré correctement une liste d’utilisateurs clés à partir du client. Cette attaque se concentre sur ce qui vous permet de spécifier un ensemble de mots de passe par rapport à un seul utilisateur.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>Pour simuler une attaque par mot de passe en force brute

1. Dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.
    
2. Spécifiez un nom de campagne explicite de l’attaque.
    
3. Spécifiez le destinataire cible. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.
    
4. Spécifiez un ensemble de mots de passe à utiliser pour l’attaque. Par exemple, un mot de passe de courantes et pertinent vous pouvez essayer est `Fall2017`. Un autre peut être `Spring2018`, ou `Password1`.
    
5. Cliquez sur **Terminer** pour lancer l’attaque. 
    
## <a name="related-topics"></a>Voir aussi

[Intelligence des menaces d’Office 365](office-365-ti.md)
  

