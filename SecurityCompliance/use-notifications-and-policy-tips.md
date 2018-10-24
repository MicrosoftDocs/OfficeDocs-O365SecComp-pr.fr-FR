---
title: Envoyer des notifications par courrier électronique et afficher les conseils de stratégie pour les stratégies DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleNotifyUser
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 87496bc5-9601-4473-8021-cb05c71369c1
description: 'Un Conseil de stratégie est une notification ou avertissement qui s’affiche lorsqu’une personne fonctionne avec le contenu qui est en conflit avec une stratégie DLP. Vous pouvez utiliser les notifications par courrier électronique et les conseils de stratégie pour sensibiliser et aider à former les utilisateurs sur les stratégies de votre organisation. Vous pouvez également permettent d’être affichées aux personnes cette option pour remplacer la stratégie, afin qu’ils ne sont pas bloqués s’ils disposent d’une entreprise valide ou si la stratégie détecte un faux positif. '
ms.openlocfilehash: f95e392cc6cced6da29d34abfcab0fa0c3add069
ms.sourcegitcommit: 3ac6452ab77a761d06122c35c5f4a76da4472990
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2018
ms.locfileid: "25769913"
---
# <a name="send-email-notifications-and-show-policy-tips-for-dlp-policies"></a>Envoyer des notifications par courrier électronique et afficher les conseils de stratégie pour les stratégies DLP

Vous pouvez utiliser une stratégie de protection contre la perte données pour identifier, analyser et protection des informations sensibles dans Office 365. Vous souhaitez que les personnes de votre organisation qui travaillent avec ces informations sensibles restent conformes à vos stratégies DLP, mais vous ne voulez pas empêcher les inutilement effectuer leur travail. Il s’agit où les notifications par courrier électronique et les conseils de stratégie peuvent aider.
  
![La barre des messages affiche le conseil de stratégie dans Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Un Conseil de stratégie est une notification ou avertissement qui s’affiche lorsqu’une personne fonctionne avec le contenu qui est en conflit avec une stratégie DLP — par exemple, de contenu comme un classeur Excel sur un site d’entreprise qui contient des informations d’identification personnelle (PII) et est OneDrive partagé avec un utilisateur externe.
  
Vous pouvez utiliser les notifications par courrier électronique et les conseils de stratégie pour sensibiliser et aider à former les utilisateurs sur les stratégies de votre organisation. Vous pouvez également permettent d’être affichées aux personnes cette option pour remplacer la stratégie, afin qu’ils ne sont pas bloqués s’ils disposent d’une entreprise valide ou si la stratégie détecte un faux positif.
  
De sécurité Office 365 &amp; centre de conformité, lorsque vous créez une stratégie DLP, vous pouvez configurer les notifications de l’utilisateur à :
  
- Envoyer une notification par courrier électronique aux personnes vous choisissez qui décrit le problème.
    
- Afficher un Conseil de stratégie pour le contenu qui est en conflit avec la stratégie DLP :
    
  - Pour le courrier électronique dans Outlook sur le web et d’Outlook 2013 et versions ultérieures, le Conseil de stratégie s’affiche en haut d’un message au-dessus de destinataires pendant que le message est en cours composé.
    
  - Pour les documents dans un compte professionnel ou un site SharePoint Online OneDrive, le Conseil de stratégie est indiqué par une icône d’avertissement qui s’affiche sur l’élément. Pour afficher plus d’informations, vous pouvez sélectionner un élément et puis cliquez sur **informations**![icône d’Information volet](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) dans le coin supérieur droit de la page pour ouvrir le volet d’informations. 
    
  - Pour Excel 2016, 2016 PowerPoint et des documents Word 2016 qui sont stockés sur un site de l’entreprise ou un site SharePoint Online qui est inclus dans la stratégie DLP OneDrive, le Conseil de stratégie apparaît dans la barre des messages et le mode Backstage (menu **fichier** \> ** Info**).
    
## <a name="add-user-notifications-to-a-dlp-policy"></a>Ajouter des notifications de l’utilisateur à une stratégie DLP

Lorsque vous créez une stratégie DLP, les notifications par courrier électronique et les conseils de stratégie sont une partie de la section **notifications de l’utilisateur** . 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école. Vous êtes maintenant dans la sécurité Office 365 &amp; centre de conformité.
    
3. Dans la sécurité &amp; centre de conformité \> barre de navigation gauche \> **prévention des pertes de données** \> **stratégie** \> **+ créer une stratégie**.
    
    ![Créer un bouton de la stratégie](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Choisissez le modèle de stratégie DLP qui protège les types d’informations sensibles que vous devez \> **suivant**.
    
    Pour démarrer avec un modèle vide, sélectionnez **personnalisé** \> **stratégie personnalisée** \> **suivant**.
    
5. Nom de la stratégie \> **suivant**.
    
6. Pour choisir les emplacements que vous voulez que la stratégie DLP protéger, effectuez l’une des opérations suivantes :
    
  - Choisissez **tous les emplacements dans Office 365** \> **suivant**.
    
  - Sélectionnez **me laisser choisir les emplacements spécifiques** \> **suivant**.
    
    Pour inclure ou exclure un emplacement complet tel que tout le courrier Exchange ou tous les comptes de OneDrive, activer ou désactiver la l' **état** de cet emplacement. 
    
    Pour inclure uniquement certains sites SharePoint ou les comptes de OneDrive, changer l' **état** , puis cliquez sur les liens sous **inclure** à choisir des comptes ou des sites spécifiques. 
    
7. Choisissez **d’utiliser les paramètres avancés** \> **suivant**.
    
8. Choisissez **+ nouvelle règle**.
    
9. Dans l’éditeur de règle, sous **notifications utilisateur**, basculez le statut.
    
    ![Section de notifications d’utilisateur de l’éditeur de règle](media/47705927-c60b-4054-a072-ab914f33d15d.png)
  
## <a name="options-for-configuring-email-notifications"></a>Options de configuration des notifications par courrier électronique

Pour chaque règle d’une stratégie DLP, vous pouvez :
  
- Envoyer la notification aux personnes de votre choix. Celles-ci peuvent inclure le propriétaire du contenu, la personne qui a modifié le contenu en dernier, le propriétaire du site sur lequel est stocké le contenu ou un utilisateur spécifique.
    
- Personnaliser le texte qui est inclus dans la notification à l’aide de code HTML ou les jetons. Voir la section ci-dessous pour plus d’informations.
    
> [!NOTE]
>  Notifications par courrier électronique peuvent être envoyées uniquement à des destinataires — pas les groupes ou les listes de distribution. > Nouveau contenu ne déclenche une notification par courrier électronique. Modification de contenu existant déclenche les conseils de stratégie, mais pas une notification par courrier électronique. 
  
![Options de notification de messagerie](media/4e7b9500-2a78-44e6-9067-09f4bfd50301.png)
  
### <a name="default-email-notification"></a>Notification par courrier électronique par défaut

Notifications ont une ligne d’objet commence par l’action effectuée, tel que « Notification », « Message bloqué » pour le courrier électronique, ou « Accès bloqué » pour les documents. Si la notification est sur un document, le corps du message de notification inclut un lien qui vous dirige vers le site où le document de stockées et ouvre le Conseil de stratégie pour le document, où vous pouvez résoudre les problèmes (voir la section ci-dessous sur les conseils de stratégie). Si la notification est sur un message, la notification inclut en pièce jointe le message qui correspond à une stratégie DLP.
  
![Message de notification](media/35813d40-5fd8-425f-9624-55655e74fa6b.png)
  
Par défaut, les notifications affichent un texte semblable au suivant pour un élément sur un site. Le texte des notifications est configuré séparément pour chaque règle, afin que le texte qui s’affiche varie en fonction de la règle mise en correspondance.
  
| |
|**Si la règle de stratégie DLP...**|**Puis la notification par défaut pour SharePoint ou OneDrive pour les documents d’entreprise indique ceci...**|**Puis la notification par défaut pour les messages Outlook indique que ceci...**|
|:-----|:-----|:-----|
|Envoie une notification, mais ne permet pas de substitution  <br/> |Cet élément est en conflit avec une stratégie de votre organisation.  <br/> |Votre courrier électronique message est en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. Si vous ne pas résoudre le conflit, accéder à ce fichier peut être bloqué.  <br/> |Votre courrier électronique message est en conflit avec une stratégie de votre organisation. Le message n’a pas été remis à tous les destinataires.  <br/> |
|Bloque l’accès et envoie une notification  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. L’accès à cet élément est bloqué pour tous les utilisateurs, à l’exception de son propriétaire, de l’utilisateur ayant effectué la dernière modification et l’administrateur de la collection de sites principale.  <br/> |Votre courrier électronique message est en conflit avec une stratégie de votre organisation. Le message n’a pas été remis à tous les destinataires.  <br/> |
   
### <a name="custom-email-notification"></a>Notification de message électronique personnalisé

Vous pouvez créer une notification de message électronique personnalisé au lieu d’envoyer la notification par courrier électronique par défaut pour vos utilisateurs finaux ou les administrateurs. La notification de message électronique personnalisé prend en charge HTML et a une limite de 5 000 caractères. Vous pouvez utiliser le HTML pour inclure des images, la mise en forme et les autres marques dans la notification.
  
Vous pouvez également utiliser les jetons suivants vous aideront à personnaliser la notification par courrier électronique. Ces jetons sont des variables qui sont remplacés par des informations spécifiques dans la notification est envoyée.
  
| |
|**Émission de jeton**|**Description**|
|:-----|:-----|
|%% AppliedActions %%  <br/> |Les actions appliquées au contenu.  <br/> |
|%% ContentURL %%  <br/> |L’URL du document sur le site SharePoint Online ou OneDrive pour le site de l’entreprise.  <br/> |
|%% MatchedConditions %%  <br/> |Les conditions qui ont été filtrées par le contenu. Utilisez ce jeton pour informer les utilisateurs des problèmes possibles avec le contenu.  <br/> |
   
![Message de notification indiquant où apparaissent les jetons](media/cd3f36b3-40db-4f30-99e4-190750bd1955.png)
  
## <a name="options-for-configuring-policy-tips"></a>Options de configuration des conseils de stratégie

Pour chaque règle d’une stratégie DLP, vous pouvez configurer des conseils de stratégie pour :
  
- Simplement notifier la personne que le contenu est en conflit avec une stratégie DLP, afin qu’ils peuvent prendre des mesures pour résoudre le conflit. Vous pouvez utiliser le texte par défaut (voir les tableaux ci-dessous) ou entrez le texte personnalisé sur les stratégies spécifiques de votre organisation.
    
- Autoriser la personne à remplacer la stratégie DLP. Si vous le souhaitez, vous pouvez :
    
  - Exiger de la personne à entrer une justification du remplacement de la stratégie. Cette information est enregistrée et vous pouvez l’afficher dans les rapports DLP dans la section **rapports** de la sécurité &amp; centre de conformité. 
    
  - Autoriser la personne à signaler un faux positif et remplacer la stratégie DLP. Cette information est également journalisée pour la création de rapports, afin que vous puissiez utiliser les faux positifs pour affiner vos règles.
    
![Options de Conseil de stratégie](media/0d2f2c68-028a-4900-afe6-1d9fce5303ef.png)
  
Par exemple, avoir une stratégie DLP appliquée à OneDrive pour les sites qui détecte les informations d’identification personnelle (PII), et cette stratégie a trois règles :
  
1. Première règle : si moins de cinq instances de ces informations sensibles sont détectées dans un document et que le document est partagé avec des personnes au sein de l’organisation, l’action **Envoyer une notification** affiche un conseil de stratégie. Pour les conseils de stratégie, aucune option de remplacement n’est nécessaire car cette règle avertit simplement les utilisateurs et ne bloque pas l’accès. 
    
2. Seconde règle : si elle est supérieure à cinq instances de ces informations sensibles détectés dans un document et le document est partagé avec des personnes à l’intérieur de l’organisation, l’action **Bloquer l’accès au contenu** restreint les autorisations pour le fichier et le ** Envoyer une notification** action permet aux utilisateurs de remplacer les actions de cette règle en fournissant une justification. Entreprise de votre organisation requiert parfois des personnes internes de partager des données personnelles, et vous ne voulez pas que votre stratégie DLP pour bloquer ce travail. 
    
3. Troisième règle : Si plus de cinq instances de ces informations sensibles sont détectées dans un document et que le document est partagé avec des personnes extérieures à l’organisation, l’action **Bloquer l’accès au contenu** restreint les autorisations pour le fichier et l’action **Envoyer une notification** ne permet pas aux utilisateurs de remplacer les actions de cette règle car les informations sont partagées en externe. En aucun cas les membres de votre organisation ne doivent être autorisés à partager des données PII en dehors de l’organisation. 
    
Voici quelques notions précises à comprendre à propos de l’utilisation d’un conseil de stratégie pour remplacer une règle :
  
- Cette option pour remplacer est par la règle, et il remplace toutes les actions de la règle (à l’exception de l’envoi d’une notification, qui ne peut pas être substituée).
    
- Il est possible de contenu pour la correspondance de plusieurs règles dans une stratégie DLP, mais s’affichera uniquement le Conseil de stratégie à partir de la plus restrictive, la priorité de la règle. Par exemple, un Conseil de stratégie à partir d’une règle qui bloque l’accès au contenu s’affichera sur un Conseil de stratégie à partir d’une règle qui envoie une notification. Cela empêche des personnes de voir une cascade de conseils de stratégie.
    
- Si les conseils de stratégie de la règle la plus restrictive autorisent les utilisateurs à remplacer la règle, toute autre règle également mise en correspondance avec le contenu est aussi remplacée.
    
## <a name="policy-tips-on-onedrive-for-business-sites-and-sharepoint-online-sites"></a>Conseils de stratégie sur les sites OneDrive Entreprise et les sites SharePoint Online

Lorsqu’un document sur un site de l’entreprise ou un site SharePoint Online OneDrive correspond à une règle dans une stratégie DLP, et cette règle utilise les conseils de stratégie, les conseils de stratégie affichent les icônes spéciales sur le document :
  
1. Si la règle envoie une notification sur le fichier, l’icône d’avertissement s’affiche.
    
2. Si la règle bloque l’accès au document, l’icône de blocage s’affiche.
    
![Icônes de Conseil de stratégie sur les documents dans un compte OneDrive](media/d3e9f772-03f9-4d28-82f8-3064784332a2.png)
  
Pour effectuer une action sur un document, vous pouvez sélectionner un élément \> choisissez **informations**![icône d’Information volet](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) dans le coin supérieur droit de la page pour ouvrir le volet d’informations \> **Conseil de stratégie d’affichage**.
  
Le conseil de stratégie répertorie les problèmes rencontrés avec le contenu, et s’ils sont configurés avec ces options, vous pouvez choisir de les **résoudre**, puis de **remplacer** le conseil de stratégie ou de **signaler** un faux positif. 
  
![Conseil de stratégie affichant des informations volet](media/0a191e70-80f0-4702-90f4-7a5b7aabcaab.png)
  
![Conseil de stratégie avec l’option de remplacement](media/e250bff9-41d5-4ce4-82ea-1dc2d043fab1.png)
  
Les stratégies DLP sont synchronisées avec les sites et le contenu est évalué par rapport à ces stratégies régulièrement et de manière asynchrone. Vous pouvez donc constater un bref délai entre le moment de la création de la stratégie DLP et celui où vous commencez à voir les conseils de stratégie. Un délai similaire peut exister entre le moment où vous résolvez ou remplacez un conseil de stratégie et celui où l’icône disparaît pour le document sur le site.
  
### <a name="default-text-for-policy-tips-on-sites"></a>Texte par défaut pour les conseils de stratégie sur les sites

Par défaut, les conseils de stratégie affichent un texte semblable à ce qui suit pour un élément sur un site. Le texte des notifications est configuré séparément pour chaque règle, afin que le texte qui s’affiche varie en fonction de la règle mise en correspondance.
  
| |
|**Si la règle de stratégie DLP...**|**Le conseil de stratégie par défaut indique que...**|
|:-----|:-----|
|Envoie une notification, mais ne permet pas de substitution  <br/> |Cet élément est en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. Si vous ne pas résoudre le conflit, accéder à ce fichier peut être bloqué.  <br/> |
|Bloque l’accès et envoie une notification  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. L’accès à cet élément est bloqué pour tous les utilisateurs, à l’exception de son propriétaire, de l’utilisateur ayant effectué la dernière modification et l’administrateur de la collection de sites principale.  <br/> |
   
### <a name="custom-text-for-policy-tips-on-sites"></a>Texte personnalisé pour des conseils de stratégie sur les sites

Vous pouvez personnaliser le texte de conseils de stratégie séparément à partir de la notification par courrier électronique. Contrairement à un texte personnalisé pour les notifications par courrier électronique (voir ci-dessus section), un texte personnalisé pour les conseils de stratégie n’accepte pas HTML ou les jetons. Au lieu de cela, le texte personnalisé pour des conseils de stratégie est en texte brut uniquement avec une limite de 256 caractères.
  
## <a name="policy-tips-in-outlook-on-the-web-and-outlook-2013-and-later"></a>Conseils de stratégie dans Outlook sur le web et Outlook 2013 et versions ultérieures

Lorsque vous composez un nouveau message électronique dans Outlook sur le web et Outlook 2013 et versions ultérieures, vous verrez un Conseil de stratégie si vous ajoutez le contenu qui correspond à une règle dans une stratégie DLP, et cette règle utilise les conseils de stratégie. Le Conseil de stratégie s’affiche en haut du message, au-dessus de destinataires, tandis que le message est en cours composé.
  
![Conseil de stratégie en haut d’un message sont composé](media/9b3b6b74-17c5-4562-82d5-d17ecaaa8d95.png)
  
Les conseils de stratégie de travail si les informations sensibles apparaissent dans le corps du message, ligne d’objet ou encore une pièce jointe du message, comme indiqué ici.
  
![Conseil de stratégie indiquant qu’une pièce jointe est en conflit avec une stratégie DLP](media/59ae6655-215f-47d9-ad1d-39c0d1e61740.png)
  
Si les conseils de stratégie sont configurés pour autoriser le remplacement, vous pouvez choisir **d’Afficher les détails** \> **Remplacer** \> permet d’entrer une justification ou signaler un faux positif \> **Remplacer**.
  
![Conseil de stratégie développé pour afficher l’option de remplacement de message](media/28bfb997-48a6-41f0-8682-d5e62488458a.png)
  
![Boîte de dialogue Stratégie Conseil où vous pouvez substituer le Conseil de stratégie](media/f97e836c-04bd-44b4-aec6-ed9526ea31f8.png)
  
Notez que lorsque vous ajoutez des informations sensibles à un message électronique, il peut y avoir latence entre lors de l’ajout des informations sensibles et lorsque le Conseil de stratégie s’affiche.

### <a name="outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions"></a>Outlook 2013 et versions ultérieures prend en charge affichant les conseils de stratégie pour uniquement certaines conditions

Actuellement, Outlook 2013 et versions ultérieures prend en charge affichant les conseils de stratégie uniquement pour les conditions suivantes :

- Contient le contenu
- Le contenu est partagé

Nous sommes actuellement en train de prise en charge pour l’affichage des conseils de stratégie pour des conditions supplémentaires. Cela inclut :

- Contenu de pièce jointe électronique n’a pas pu être analysé.
- Contenu de pièce jointe électronique n’a pas terminé l’analyse
- Extension de fichier des pièces jointes
- Pièce jointe est protégé par mot de passe
- Propriété de document est
- Domaine du destinataire est
- Adresse IP de l’expéditeur est

Notez que toutes les conditions suivantes fonctionnent dans Outlook, où ils correspondent au contenu et appliquer les mesures de protection du contenu. Mais affichant les conseils de stratégie aux utilisateurs n'est pas encore pris en charge.
  
### <a name="policy-tips-in-the-exchange-admin-center-vs-the-office-365-security-amp-compliance-center"></a>Conseils de stratégie dans le centre d’administration Exchange et la sécurité de 365 Office &amp; centre de conformité

Conseils de stratégie peuvent travailler avec les stratégies DLP et créés dans le centre d’administration Exchange, ou avec des stratégies DLP créées de sécurité Office 365 des règles de flux de messagerie &amp; centre de conformité, mais pas les deux. Il s’agit, car ces stratégies sont stockées dans des emplacements différents, mais les conseils de stratégie peuvent tracer uniquement à partir d’un seul emplacement.
  
Si vous avez configuré les conseils de stratégie dans le centre d’administration Exchange, les conseils de stratégie que vous configurez de sécurité Office 365 &amp; centre de conformité n’apparaîtra pas aux utilisateurs dans Outlook sur le web et Outlook 2013 et versions ultérieures jusqu'à ce que vous désactiviez les conseils fournis dans la version d’Exchange Centre d’administration. Cela garantit que vos règles de transport Exchange en cours continue à fonctionner jusqu'à ce que vous choisissez de basculer vers le Office 365 Security &amp; centre de conformité.
  
Notez que les notifications de messagerie pendant que les conseils de stratégie peuvent tracer uniquement à partir d’un seul emplacement, sont toujours envoyés, même si vous utilisez des stratégies DLP dans Office 365 Security &amp; centre de conformité et le centre d’administration Exchange.
  
### <a name="default-text-for-policy-tips-in-email"></a>Texte par défaut pour les conseils de stratégie dans le message électronique

Par défaut, les conseils de stratégie affichent du texte semblable au suivant pour le courrier électronique.

|**Si la règle de stratégie DLP...**|**Le conseil de stratégie par défaut indique que...**|
|:-----|:-----|
|Envoie une notification, mais ne permet pas de substitution  <br/> |Votre courrier électronique en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Votre courrier électronique en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès et envoie une notification  <br/> |Votre courrier électronique en conflit avec une stratégie de votre organisation.  <br/> |
   
## <a name="policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Conseils de stratégie dans Excel 2016, PowerPoint 2016 et Word 2016

Lorsque les utilisateurs travaillent avec du contenu sensible dans les versions de bureau d’Excel 2016, de PowerPoint 2016 et de Word 2016, les conseils de stratégie peuvent les avertir en temps réel que le contenu est en conflit avec une stratégie DLP. En voici les implications :
  
- Le document Office est stocké sur un site OneDrive Entreprise ou un site SharePoint Online.
    
- Le site est inclus dans une stratégie DLP qui est configurée pour utiliser les conseils de stratégie.
    
Ces applications bureautiques Office 2016 synchroniser automatiquement les stratégies DLP directement à partir d’Office 365 et d’analyser vos documents pour vous assurer qu’ils ne sont en conflit avec vos stratégies DLP et afficher des conseils de stratégie en temps réel.
  
Selon la façon dont vous configurez les conseils de stratégie dans la stratégie DLP, les utilisateurs peuvent choisir d’ignorer simplement le conseil, de remplacer la stratégie avec ou sans justification ou de signaler un faux positif.
  
Les conseils de stratégie apparaissent dans la barre des messages.
  
![La barre des messages affiche le conseil de stratégie dans Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Ils apparaissent également dans le mode Backstage (dans l’onglet **Fichier**). 
  
![Le mode Backstage affiche les conseils de stratégie dans Excel 2016](media/44c561f6-8f3f-4878-b1b0-b7543f8a4120.png)
  
Si les conseils de stratégie dans la stratégie DLP sont configurés avec ces options, vous pouvez choisir de **résoudre** le problème pour **remplacer** un conseil de stratégie ou de **signaler** un faux positif. 
  
![Options relatives aux conseils de stratégie en mode Backstage dans Excel 2016](media/5b3857ba-907e-456e-ae43-888b594c049c.png)
  
Dans chacun de ces programmes de bureau Office 2016, les utilisateurs peuvent choisir de désactiver les conseils de stratégie. Si tel est le cas, les conseils qui sont de simples notifications ne s’affichent pas dans la barre des messages ou le mode Backstage (sur l’onglet **Fichier**). Cependant, les conseils de stratégie sur le blocage et le remplacement apparaissent toujours et la notification par courrier électronique est toujours envoyée. Par ailleurs, la désactivation des conseils de stratégie ne dispense pas le document des stratégies DLP qui lui ont été appliquées. 
  
### <a name="default-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Texte par défaut pour les conseils de stratégie dans Excel 2016, PowerPoint 2016 et Word 2016

Par défaut, les conseils de stratégie affichent un texte semblable à ce qui suit sur la barre des messages et le mode Backstage d’un document ouvert. Le texte des notifications est configuré séparément pour chaque règle, afin que le texte qui s’affiche varie en fonction de la règle mise en correspondance.

|**Si la règle de stratégie DLP...**|**Le conseil de stratégie par défaut indique que...**|
|:-----|:-----|
|Envoie une notification, mais ne permet pas de substitution  <br/> |Ce fichier est en conflit avec une stratégie de votre organisation. Ouvrez le menu **fichier** pour plus d’informations.<br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Ce fichier est en conflit avec une stratégie de votre organisation. Si vous ne pas résoudre le conflit, accéder à ce fichier peut être bloqué. Ouvrez le menu **fichier** pour plus d’informations.<br/> |
|Bloque l’accès et envoie une notification  <br/> |Ce fichier est en conflit avec une stratégie de votre organisation. Si vous ne pas résoudre le conflit, accéder à ce fichier peut être bloqué. Ouvrez le menu **fichier** pour plus d’informations.<br/> |
   
### <a name="custom-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Conseils de texte personnalisé pour la stratégie dans Excel 2016, 2016 PowerPoint et Word 2016

Vous pouvez personnaliser le texte de conseils de stratégie séparément à partir de la notification par courrier électronique. Contrairement à un texte personnalisé pour les notifications par courrier électronique (voir ci-dessus section), un texte personnalisé pour les conseils de stratégie n’accepte pas HTML ou les jetons. Au lieu de cela, le texte personnalisé pour des conseils de stratégie est en texte brut uniquement avec une limite de 256 caractères.
  
## <a name="more-information"></a>Plus d’informations

- [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md)
    
- [Créer une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md)
    
- [Créer une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés](protect-documents-that-have-fci-or-other-properties.md)
    
- [Contenu des modèles de stratégie DLP](what-the-dlp-policy-templates-include.md)
    
- [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
    

