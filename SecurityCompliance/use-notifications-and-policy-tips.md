---
title: Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/14/2019
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleNotifyUser
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 'Un Conseil de stratégie est une notification ou un avertissement qui s’affiche lorsqu’un utilisateur travaille avec du contenu qui entre en conflit avec une stratégie DLP. Vous pouvez utiliser des notifications par courrier électronique et des conseils de stratégie pour sensibiliser les utilisateurs aux stratégies de votre organisation. Vous pouvez également donner aux utilisateurs la possibilité de remplacer la stratégie, afin qu’ils ne soient pas bloqués s’ils ont un besoin opérationnel valide ou si la stratégie détecte un faux positif. '
ms.openlocfilehash: 4de22c8ad8a45cf1489e72516d30f078889774e3
ms.sourcegitcommit: 9df5bf99c1860ace0c5cc90647733d075be412ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2019
ms.locfileid: "34948902"
---
# <a name="send-email-notifications-and-show-policy-tips-for-dlp-policies"></a>Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP

Vous pouvez utiliser une stratégie de protection contre la perte de données (DLP) pour identifier, surveiller et protéger les informations sensibles dans Office 365. Vous souhaitez que les personnes de votre organisation qui travaillent avec ces informations sensibles soient conformes à vos stratégies DLP, mais que vous ne voulez pas les bloquer inutilement. C’est ici que les notifications par courrier électronique et les conseils de stratégie peuvent vous aider.
  
![La barre des messages affiche le conseil de stratégie dans Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Un Conseil de stratégie est une notification ou un avertissement qui s’affiche lorsqu’un utilisateur travaille avec du contenu qui entre en conflit avec une stratégie DLP (par exemple, du contenu tel qu’un classeur Excel sur un site OneDrive entreprise qui contient des informations d’identification personnelle et qui est partagé avec un utilisateur externe.
  
Vous pouvez utiliser des notifications par courrier électronique et des conseils de stratégie pour sensibiliser les utilisateurs aux stratégies de votre organisation. Vous pouvez également donner aux utilisateurs la possibilité de remplacer la stratégie, afin qu’ils ne soient pas bloqués s’ils ont un besoin opérationnel valide ou si la stratégie détecte un faux positif.
  
Dans le centre de sécurité &amp; conformité Office 365, lorsque vous créez une stratégie DLP, vous pouvez configurer les notifications utilisateur de la façon suivante:
  
- Envoyer une notification par courrier électronique aux personnes que vous avez choisies qui décrivent le problème.
    
- Afficher un Conseil de stratégie pour le contenu qui est en conflit avec la stratégie DLP:
    
  - Pour le courrier électronique dans Outlook sur le Web et Outlook 2013 et versions ultérieures, le Conseil de stratégie apparaît en haut d’un message au-dessus des destinataires lors de la composition du message.
    
  - Pour les documents dans un compte OneDrive entreprise ou un site SharePoint Online, le Conseil de stratégie est indiqué par une icône d’avertissement qui apparaît sur l’élément. Pour afficher plus d’informations, vous pouvez sélectionner un élément, puis **** ![choisir volet informations sur](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) les informations dans le coin supérieur droit de la page pour ouvrir le volet d’informations. 
    
  - Pour les documents Excel, PowerPoint et Word stockés sur un site OneDrive entreprise ou un site SharePoint Online inclus dans la stratégie DLP, le Conseil de stratégie s’affiche dans la barre des messages et le mode Backstage ( \> **informations**du menu **fichier** ).
    
## <a name="add-user-notifications-to-a-dlp-policy"></a>Ajouter des notifications utilisateur à une stratégie DLP

Lorsque vous créez une stratégie DLP, les notifications par courrier électronique et les conseils de stratégie font partie de la section notifications de l' **utilisateur** . 
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel. Vous êtes maintenant dans le centre de sécurité &amp; conformité Office 365.
    
3. Dans le centre &amp; \> de sécurité conformité, \> **stratégie** \> de **protection contre** \> la perte de données gauche **+ créer une stratégie**.
    
    ![Bouton créer une stratégie](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Choisissez le modèle de stratégie DLP qui protège les types d’informations sensibles dont vous \> **** avez besoin.
    
    Pour commencer avec un modèle vide, sélectionnez **** \> **stratégie** \> personnalisée personnalisée **suivant**.
    
5. Nommez la \> stratégie **suivante**.
    
6. Pour choisir les emplacements que la stratégie DLP doit protéger, effectuez l’une des opérations suivantes:
    
  - Choisissez **tous les emplacements dans Office 365** \> ****.
    
  - Choisissez **me laisser choisir des emplacements** \> **** spécifiques.
    
    Pour inclure ou exclure un emplacement entier, tel que tous les messages électroniques Exchange ou tous les comptes OneDrive, activez ou désactivez l' **État** de cet emplacement. 
    
    Pour inclure uniquement des sites SharePoint spécifiques ou des comptes OneDrive, changez l' **État** en activé, puis cliquez sur les liens sous **inclure** pour choisir des sites ou des comptes spécifiques. 
    
7. Sélectionnez **utiliser les paramètres** \> avancés **suivant**.
    
8. Sélectionnez **+ nouvelle règle**.
    
9. Dans l’éditeur de règles, sous **notifications utilisateur**, changez l’état de.
    
    ![Section notifications utilisateur de l’éditeur de règles](media/47705927-c60b-4054-a072-ab914f33d15d.png)

> [!NOTE]
> Les stratégies DLP s’appliquent à tous les documents qui correspondent à la stratégie, qu’ils soient nouveaux ou existants. Toutefois, une notification par courrier électronique est générée uniquement lorsque le nouveau contenu correspond à une stratégie DLP existante. Le contenu existant est protégé, mais ne génère pas de notification d’utilisateur par courrier électronique.
  
## <a name="options-for-configuring-email-notifications"></a>Options de configuration des notifications par courrier électronique

Pour chaque règle d’une stratégie DLP, vous pouvez:
  
- Envoyer la notification aux personnes que vous choisissez. Ces personnes peuvent inclure le propriétaire du contenu, la personne qui a modifié le contenu en dernier, le propriétaire du site où le contenu est stocké, ou un utilisateur spécifique.
    
- Personnaliser le texte inclus dans la notification à l’aide de code HTML ou de jetons. Pour plus d’informations, consultez la section ci-dessous.
    
> [!NOTE]
>  Les notifications par courrier électronique ne peuvent être envoyées qu’à des destinataires individuels, et non à des groupes ou à des listes de distribution. Seul le nouveau contenu déclenchera une notification par courrier électronique. La modification d’un contenu existant déclenche des conseils de stratégie, mais pas de notification par courrier électronique. 
  
![Options de notification par courrier électronique](media/4e7b9500-2a78-44e6-9067-09f4bfd50301.png)
  
### <a name="default-email-notification"></a>Notification par courrier électronique par défaut

Les notifications ont une ligne d’objet qui commence par l’action entreprise, telle que «notification», «message bloqué» pour le courrier électronique ou «accès bloqué» pour les documents. Si la notification concerne un document, le corps du message de notification inclut un lien qui vous dirige vers le site où le document est stocké et ouvre le Conseil de stratégie pour le document, où vous pouvez résoudre les problèmes (voir la section ci-dessous à propos des conseils de stratégie). Si la notification concerne un message, la notification inclut comme pièce jointe le message qui correspond à une stratégie DLP.
  
![Message de notification](media/35813d40-5fd8-425f-9624-55655e74fa6b.png)
  
Par défaut, les notifications s’affichent sous une forme semblable à la suivante pour un élément sur un site. Le texte de notification est configuré séparément pour chaque règle, de sorte que le texte affiché diffère en fonction de la règle mise en correspondance.

|**Si la règle de stratégie DLP effectue cette opération...**|**La notification par défaut pour les documents SharePoint ou OneDrive entreprise indique ceci...**|**La notification par défaut pour les messages Outlook indique ceci...**|
|:-----|:-----|:-----|
|Envoie une notification, mais n’autorise pas le remplacement  <br/> |Cet élément est en conflit avec une stratégie de votre organisation.  <br/> |Votre message électronique est en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. Si vous ne résolvez pas ce conflit, l’accès à ce fichier peut être bloqué.  <br/> |Votre message électronique est en conflit avec une stratégie de votre organisation. Le message n’a pas été remis à tous les destinataires.  <br/> |
|Bloque l’accès et envoie une notification  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. L’accès à cet élément est bloqué pour tout le monde sauf son propriétaire, le dernier modificateur et l’administrateur principal de la collection de sites.  <br/> |Votre message électronique est en conflit avec une stratégie de votre organisation. Le message n’a pas été remis à tous les destinataires.  <br/> |
   
### <a name="custom-email-notification"></a>Notification par courrier électronique personnalisée

Vous pouvez créer une notification par courrier électronique personnalisée au lieu d’envoyer la notification par défaut à vos utilisateurs finaux ou administrateurs. La notification par courrier électronique personnalisée prend en charge le format HTML et présente une limite de 5 000 caractères. Vous pouvez utiliser du code HTML pour inclure des images, une mise en forme et d’autres personnalisations dans la notification.
  
Vous pouvez également utiliser les jetons suivants pour vous aider à personnaliser la notification par courrier électronique. Ces jetons sont des variables qui sont remplacées par des informations spécifiques dans la notification envoyée.

|**Jeton**|**Description**|
|:-----|:-----|
|%% AppliedActions%%  <br/> |Actions appliquées au contenu.  <br/> |
|%% ContentURL%%  <br/> |URL du document sur le site SharePoint Online ou OneDrive entreprise.  <br/> |
|%%MatchedConditions%%  <br/> |Conditions qui ont été mises en correspondance avec le contenu. Utilisez ce jeton pour informer les personnes de problèmes possibles liés au contenu.  <br/> |
   
![Message de notification indiquant où les jetons apparaissent](media/cd3f36b3-40db-4f30-99e4-190750bd1955.png)
  
## <a name="options-for-configuring-policy-tips"></a>Options de configuration des conseils de stratégie

Pour chaque règle d’une stratégie DLP, vous pouvez configurer des conseils de stratégie pour:
  
- Informez simplement la personne que le contenu est en conflit avec une stratégie DLP, afin qu’ils puissent prendre des mesures pour résoudre le conflit. Vous pouvez utiliser le texte par défaut (voir les tableaux ci-dessous) ou entrer du texte personnalisé sur les stratégies spécifiques de votre organisation.
    
- Autoriser la personne à remplacer la stratégie DLP. Si vous le souhaitez, vous pouvez:
    
  - Demander à la personne d’entrer une justification professionnelle pour remplacer la stratégie. Ces informations sont consignées dans le journal et vous pouvez les afficher dans **** les rapports DLP dans la &amp; section rapports du centre de sécurité et de conformité. 
    
  - Autoriser la personne à signaler un faux positif et remplacer la stratégie DLP. Ces informations sont également consignées pour la création de rapports, afin que vous puissiez utiliser des faux positifs pour affiner vos règles.
    
![Options du Conseil de stratégie](media/0d2f2c68-028a-4900-afe6-1d9fce5303ef.png)
  
Par exemple, vous pouvez avoir une stratégie DLP appliquée aux sites OneDrive entreprise qui détecte des informations d’identification personnelle, et cette stratégie comporte trois règles:
  
1. Première règle: si moins de cinq instances de ces informations sensibles sont détectées dans un document et que le document est partagé avec des personnes au sein de l’organisation, l’action **Envoyer une notification** affiche un Conseil de stratégie. Pour les conseils de stratégie, aucune option de remplacement n’est nécessaire, car cette règle avertit simplement les personnes et ne bloque pas l’accès. 
    
2. Deuxième règle: si plus de cinq instances de ces informations sensibles sont détectées dans un document et que le document est partagé avec des personnes au sein de l’organisation, l’action **bloquer l’accès au contenu** limite les autorisations du fichier et le ** Envoyer une** action de notification permet aux utilisateurs de remplacer les actions de cette règle en fournissant une justification professionnelle. Les activités professionnelles de votre organisation nécessitent parfois des personnes internes pour partager des données personnelles, et vous ne voulez pas que votre stratégie DLP bloque ce travail. 
    
3. Troisième règle: si plus de cinq instances de ces informations sensibles sont détectées dans un document et que le document est partagé avec des personnes extérieures à l’organisation, l’action **bloquer l’accès au contenu** limite les autorisations du fichier, et le ** Envoyer une** action de notification ne permet pas aux utilisateurs de remplacer les actions de cette règle car les informations sont partagées en externe. En aucun cas, les membres de votre organisation ne doivent être autorisés à partager les données des données personnelles à l’extérieur de l’organisation. 
    
Voici quelques points précis pour comprendre l’utilisation d’un Conseil de stratégie pour remplacer une règle:
  
- L’option de remplacement est par règle et elle remplace toutes les actions de la règle (à l’exception de l’envoi d’une notification, qui ne peut pas être remplacée).
    
- Il est possible que le contenu corresponde à plusieurs règles dans une stratégie DLP, mais seul le Conseil de stratégie de la règle de priorité la plus restrictive s’affiche. Par exemple, un Conseil de stratégie provenant d’une règle qui bloque l’accès au contenu sera affiché sur un Conseil de stratégie à partir d’une règle qui envoie simplement une notification. Cela empêche les personnes de voir une cascade de conseils de stratégie.
    
- Si les conseils de stratégie de la règle la plus restrictive permettent aux utilisateurs de remplacer la règle, la substitution de cette règle remplace également toutes les autres règles que le contenu correspond.
    
## <a name="policy-tips-on-onedrive-for-business-sites-and-sharepoint-online-sites"></a>Conseils de stratégie sur les sites OneDrive entreprise et SharePoint Online

Lorsqu’un document sur un site OneDrive entreprise ou un site SharePoint Online correspond à une règle dans une stratégie DLP et que cette règle utilise des conseils de stratégie, les conseils de stratégie affichent des icônes spéciales dans le document:
  
1. Si la règle envoie une notification sur le fichier, l’icône d’avertissement s’affiche.
    
2. Si la règle bloque l’accès au document, l’icône bloqué apparaît.
    
![Icônes de Conseil de stratégie sur les documents dans un compte OneDrive](media/d3e9f772-03f9-4d28-82f8-3064784332a2.png)
  
Pour effectuer une action sur un document, vous pouvez sélectionner un \> élément **** ![choisir un volet informations](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) sur l’icône dans le coin supérieur droit de la page pour ouvrir le \> **Conseil de stratégie afficher**le volet d’informations.
  
Le Conseil de stratégie répertorie les problèmes liés au contenu et, si les conseils de stratégie sont configurés avec ces options, vous pouvez choisir **résoudre**, puis **remplacer** le Conseil de stratégie ou **signaler** un faux positif. 
  
![Volet d’informations affichant le Conseil de stratégie](media/0a191e70-80f0-4702-90f4-7a5b7aabcaab.png)
  
![Conseil de stratégie avec l’option de remplacement](media/e250bff9-41d5-4ce4-82ea-1dc2d043fab1.png)
  
Les stratégies DLP sont synchronisées avec les sites et le contenu est évalué régulièrement et de manière asynchrone, de sorte qu’il peut y avoir un court délai entre le moment où vous créez la stratégie DLP et l’heure à laquelle vous commencez à consulter les conseils de stratégie. Il peut y avoir un délai similaire entre le moment où vous résolvez ou le remplacement d’un Conseil de stratégie et le moment où l’icône du document sur le site est supprimée.
  
### <a name="default-text-for-policy-tips-on-sites"></a>Texte par défaut pour les conseils de stratégie sur les sites

Par défaut, les conseils de stratégie affichent du texte similaire à ce qui suit pour un élément sur un site. Le texte de notification est configuré séparément pour chaque règle, de sorte que le texte affiché diffère en fonction de la règle mise en correspondance.

|**Si la règle de stratégie DLP effectue cette opération...**|**Le Conseil de stratégie par défaut indique alors...**|
|:-----|:-----|
|Envoie une notification, mais n’autorise pas le remplacement  <br/> |Cet élément est en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. Si vous ne résolvez pas ce conflit, l’accès à ce fichier peut être bloqué.  <br/> |
|Bloque l’accès et envoie une notification  <br/> |Cet élément est en conflit avec une stratégie de votre organisation. L’accès à cet élément est bloqué pour tout le monde sauf son propriétaire, le dernier modificateur et l’administrateur principal de la collection de sites.  <br/> |
   
### <a name="custom-text-for-policy-tips-on-sites"></a>Texte personnalisé pour les conseils de stratégie sur les sites

Vous pouvez personnaliser le texte pour les conseils de stratégie indépendamment de la notification par courrier électronique. Contrairement au texte personnalisé pour les notifications par courrier électronique (voir la section ci-dessus), le texte personnalisé pour les conseils de stratégie n’accepte pas les codes HTML ou les jetons. Au lieu de cela, le texte personnalisé pour les conseils de stratégie est uniquement en texte brut avec une limite de 256 caractères.
  
## <a name="policy-tips-in-outlook-on-the-web-and-outlook-2013-and-later"></a>Conseils de stratégie dans Outlook sur le Web et Outlook 2013 et versions ultérieures

Lorsque vous rédigez un nouveau message électronique dans Outlook sur le Web et Outlook 2013 et versions ultérieures, un Conseil de stratégie s’affiche si vous ajoutez du contenu qui correspond à une règle dans une stratégie DLP et que cette règle utilise des conseils de stratégie. Le Conseil de stratégie s’affiche en haut du message, au-dessus des destinataires, tandis que le message est en cours de composition.
  
![Conseil de stratégie en haut d’un message en cours de composition](media/9b3b6b74-17c5-4562-82d5-d17ecaaa8d95.png)
  
Les conseils de stratégie fonctionnent si les informations sensibles apparaissent dans le corps du message, la ligne d’objet ou même une pièce jointe de message, comme indiqué ci-dessous.
  
![Conseil de stratégie montrant qu’une pièce jointe est en conflit avec une stratégie DLP](media/59ae6655-215f-47d9-ad1d-39c0d1e61740.png)
  
Si les conseils de stratégie sont configurés pour autoriser le remplacement, vous pouvez choisir **Afficher** \> **remplacement** \> des détails entrez une justification professionnelle ou signaler \> un **remplacement**positif faux.
  
![Conseil de stratégie dans un message développé pour afficher l’option de remplacement](media/28bfb997-48a6-41f0-8682-d5e62488458a.png)
  
![Boîte de dialogue Conseil de stratégie, dans laquelle vous pouvez remplacer le Conseil de stratégie](media/f97e836c-04bd-44b4-aec6-ed9526ea31f8.png)
  
Notez que lorsque vous ajoutez des informations sensibles à un message électronique, il peut y avoir une latence entre le moment où les informations sensibles sont ajoutées et le Conseil de stratégie.

### <a name="outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions"></a>Outlook 2013 et les versions ultérieures prennent en charge l’affichage de conseils de stratégie pour certaines conditions uniquement

Actuellement, Outlook 2013 et les versions ultérieures prennent en charge l’affichage des conseils de stratégie uniquement pour les conditions suivantes:

- Le contenu contient
- Le contenu est partagé

Nous travaillons actuellement sur la prise en charge de l’affichage des conseils de stratégie pour des conditions supplémentaires. Ces approches sont les suivantes :

- Le contenu d’une pièce jointe de courrier électronique n’a pas pu être analysé
- Le contenu d’une pièce jointe de courrier électronique n’a pas terminé l’analyse
- L’extension de fichier de pièce jointe est
- La pièce jointe est protégée par mot de passe
- La propriété de document est
- Le domaine du destinataire est
- L’adresse IP de l’expéditeur est

Notez que toutes ces conditions fonctionnent dans Outlook, où elles correspondent au contenu et appliquent des actions de protection sur le contenu. Mais l’affichage des conseils de stratégie pour les utilisateurs n’est pas encore pris en charge.
  
### <a name="policy-tips-in-the-exchange-admin-center-vs-the-office-365-security-amp-compliance-center"></a>Conseils de stratégie dans le centre d’administration Exchange et le centre de &amp; sécurité conformité Office 365

Les conseils de stratégie peuvent fonctionner soit avec les stratégies DLP et les règles de flux de messagerie créées dans le centre d’administration Exchange, soit avec les &amp; stratégies DLP créées dans le centre de sécurité conformité Office 365, mais pas dans les deux. Cela est dû au fait que ces stratégies sont stockées à des emplacements différents, mais que les conseils de stratégie ne peuvent tirer qu’à partir d’un seul emplacement.
  
Si vous avez configuré des conseils de stratégie dans le centre d’administration Exchange, tous les conseils de stratégie que vous configurez dans le centre de sécurité &amp; conformité d’Office 365 n’apparaîtront pas pour les utilisateurs dans Outlook sur le Web et Outlook 2013 et les versions ultérieures jusqu’à ce que vous désactiviez les conseils dans l’Exchange Centre d’administration. Cela permet de s’assurer que vos règles de flux de messagerie Exchange actuelles (également appelées règles de transport) continueront de fonctionner jusqu’à ce que vous &amp; choisissiez de basculer vers le centre de sécurité conformité Office 365.
  
Notez que si 365 les conseils de stratégie ne peuvent tirer qu’à partir d’un seul emplacement, les notifications par courrier électronique sont toujours envoyées, même si vous &amp; utilisez les stratégies DLP dans le centre de sécurité et le centre d’administration Exchange.
  
### <a name="default-text-for-policy-tips-in-email"></a>Texte par défaut pour les conseils de stratégie dans les courriers électroniques

Par défaut, les conseils de stratégie affichent un texte semblable à celui ci-dessous pour la messagerie électronique.

|**Si la règle de stratégie DLP effectue cette opération...**|**Le Conseil de stratégie par défaut indique alors...**|
|:-----|:-----|
|Envoie une notification, mais n’autorise pas le remplacement  <br/> |Votre courrier est en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Votre courrier est en conflit avec une stratégie de votre organisation.  <br/> |
|Bloque l’accès et envoie une notification  <br/> |Votre courrier est en conflit avec une stratégie de votre organisation.  <br/> |
   
## <a name="policy-tips-in-excel-powerpoint-and-word"></a>Conseils de stratégie dans Excel, PowerPoint et Word

Lorsque les utilisateurs travaillent avec du contenu sensible dans les versions de bureau d’Excel, PowerPoint et Word, les conseils de stratégie peuvent les informer en temps réel que le contenu est en conflit avec une stratégie DLP. Cela nécessite les éléments suivants:
  
- Le document Office est stocké sur un site OneDrive entreprise ou un site SharePoint Online.
    
- Le site est inclus dans une stratégie DLP configurée pour utiliser les conseils de stratégie.
    
Les programmes de bureau Office synchronisent automatiquement les stratégies DLP directement à partir d’Office 365, puis analysent vos documents pour s’assurer qu’ils ne sont pas en conflit avec vos stratégies DLP et afficher les conseils de stratégie en temps réel.
  
En fonction de la façon dont vous configurez les conseils de stratégie dans la stratégie DLP, les utilisateurs peuvent simplement ignorer le Conseil de stratégie, remplacer la stratégie avec ou sans justification professionnelle ou signaler un faux positif.
  
Les conseils de stratégie s’affichent dans la barre des messages.
  
![La barre des messages affiche le conseil de stratégie dans Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Et les conseils de stratégie apparaissent également dans le mode Backstage (sous l’onglet **fichier** ). 
  
![Le mode Backstage affiche les conseils de stratégie dans Excel 2016](media/44c561f6-8f3f-4878-b1b0-b7543f8a4120.png)
  
Si les conseils de stratégie dans la stratégie DLP sont configurés avec ces options, vous pouvez choisir de **résoudre** le **remplacement** d’un Conseil de stratégie ou **signaler** un faux positif. 
  
![Options relatives aux conseils de stratégie en mode Backstage dans Excel 2016](media/5b3857ba-907e-456e-ae43-888b594c049c.png)
  
Dans chacun de ces programmes de bureau Office, les utilisateurs peuvent choisir de désactiver les conseils de stratégie. Si ce paramètre est désactivé, les conseils de stratégie qui sont des notifications simples n’apparaissent pas dans la barre des messages ou le mode Backstage (sous l’onglet **fichier** ). Toutefois, les conseils de stratégie concernant le blocage et le remplacement continueront d’apparaître, et ils continueront de recevoir la notification par courrier électronique. En outre, la désactivation des conseils de stratégie n’exempte pas le document des stratégies DLP qui lui ont été appliquées. 
  
### <a name="default-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Texte par défaut pour les conseils de stratégie dans Excel 2016, PowerPoint 2016 et Word 2016

Par défaut, les conseils de stratégie affichent du texte similaire à ce qui suit sur la barre des messages et le mode Backstage d’un document ouvert. Le texte de notification est configuré séparément pour chaque règle, de sorte que le texte affiché diffère en fonction de la règle mise en correspondance.

|**Si la règle de stratégie DLP effectue cette opération...**|**Le Conseil de stratégie par défaut indique alors...**|
|:-----|:-----|
|Envoie une notification, mais n’autorise pas le remplacement  <br/> |Ce fichier est en conflit avec une stratégie de votre organisation. Pour plus d’informations, consultez le menu **fichier** .  <br/> |
|Bloque l’accès, envoie une notification et autorise le remplacement  <br/> |Ce fichier est en conflit avec une stratégie de votre organisation. Si vous ne résolvez pas ce conflit, l’accès à ce fichier peut être bloqué. Pour plus d’informations, consultez le menu **fichier** .  <br/> |
|Bloque l’accès et envoie une notification  <br/> |Ce fichier est en conflit avec une stratégie de votre organisation. Si vous ne résolvez pas ce conflit, l’accès à ce fichier peut être bloqué. Pour plus d’informations, consultez le menu **fichier** .  <br/> |
   
### <a name="custom-text-for-policy-tips-in-excel-powerpoint-and-word"></a>Texte personnalisé pour les conseils de stratégie dans Excel, PowerPoint et Word

Vous pouvez personnaliser le texte pour les conseils de stratégie indépendamment de la notification par courrier électronique. Contrairement au texte personnalisé pour les notifications par courrier électronique (voir la section ci-dessus), le texte personnalisé pour les conseils de stratégie n’accepte pas les codes HTML ou les jetons. Au lieu de cela, le texte personnalisé pour les conseils de stratégie est uniquement en texte brut avec une limite de 256 caractères.
  
## <a name="more-information"></a>Plus d’informations

- [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md)
    
- [Création d’une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md)
    
- [Créer une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés](protect-documents-that-have-fci-or-other-properties.md)
    
- [Contenu des modèles de stratégie DLP](what-the-dlp-policy-templates-include.md)
    
- [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
    

