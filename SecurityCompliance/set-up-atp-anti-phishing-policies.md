---
title: Configurer des stratégies anti-hameçonnage d’Office 365 DAV
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578
description: DAV protection anti-hameçonnage, composant d’Office 365 avancée contre les menaces, peut aider à protéger votre organisation contre les attaques malveillantes hameçonnage basée sur l’emprunt d’identité et autres hameçonnage. Si vous êtes un administrateur de sécurité ou d’Office 365 entreprise globale, vous pouvez configurer les stratégies anti-hameçonnage DAV. Hameçonnage attaques entrent dans diverses formes contre les attaques de marchandise sonde ciblé phishing ou baleine. À la complexité, il est difficile de même un œil formé à identifier certains de ces attaques sophistiquées. Heureusement, contre les menaces avancées Office 365 peut vous aider. Vous pouvez configurer une stratégie d’anti-hameçonnage DAV pour vous assurer que votre organisation est protégée contre les attaques de ce type.
ms.openlocfilehash: 2f2258c4059d17410fd040782d7ee9dfca12576d
ms.sourcegitcommit: 4c6c937ec51e8b754332e4c1c8d286e73e197e2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "23827078"
---
# <a name="set-up-office-365-atp-anti-phishing-policies"></a>Configurer des stratégies anti-hameçonnage d’Office 365 DAV

[Protection anti - hameçonnage DAV](atp-anti-phishing.md) , composant d' [Office 365 avancée protection contre les menaces](office-365-atp.md), peuvent aider à protéger votre organisation contre les attaques malveillantes hameçonnage basée sur l’emprunt d’identité et autres hameçonnage. Si vous êtes un administrateur de sécurité ou d’Office 365 entreprise globale, vous pouvez configurer les stratégies anti-hameçonnage DAV. Hameçonnage attaques entrent dans diverses formes contre les attaques de marchandise sonde ciblé phishing ou baleine. À la complexité, il est difficile de même un œil formé à identifier certains de ces attaques sophistiquées. Heureusement, contre les menaces avancées Office 365 peut vous aider. Vous pouvez configurer une stratégie d’anti-hameçonnage DAV pour vous assurer que votre organisation est protégée contre les attaques de ce type.
  
> [!NOTE]
> DAV anti-hameçonnage est uniquement disponible en avancée contre les menaces, disponible avec Office 365 entreprise E5. Si votre organisation utilise un autre abonnement Office 365 pour entreprises, contre les menaces avancées peut être acheté comme module complémentaire. (Comme un administrateur global, dans le centre d’administration Office 365, choisissez **facturation** \> **abonnements Add**.) Pour plus d’informations sur les options de plan, voir [comparer toutes les Office 365 pour les Plans d’activité](https://go.microsoft.com/fwlink/?linkid=844053). Assurez-vous que votre organisation utilise la dernière version d’Office 365 ProPlus sur Windows pour tirer pleinement parti de protection anti-hameçonnage DAV. 
  
Procédure à suivre :
  
1. [Passez en revue les conditions préalables](#review-the-prerequisites)
    
2. [En savoir plus sur les options de stratégie anti-hameçonnage DAV](#learn-about-atp-anti-phishing-policy-options)
    
3. [Configurer une stratégie d’anti-hameçonnage DAV](#set-up-an-atp-anti-phishing-policy)
    
## <a name="review-the-prerequisites"></a>Passez en revue les conditions préalables

- Assurez-vous que vous êtes membre du groupe de rôles **administrateurs de l’entreprise** ou **administrateurs de sécurité** . 
    
- [Découvrez les options de stratégie anti-hameçonnage DAV](set-up-atp-anti-phishing-policies.md#phishpolicyoptions) (dans cet article). 
    
- Vous allez probablement définir plusieurs stratégies d’anti-hameçonnage DAV pour votre organisation. Office 365 applique ces stratégies dans l’ordre d’apparition dans la page **DAV anti-hameçonnage** dans la sécurité &amp; centre de conformité. Une fois que vous avez passé en revue les options de stratégie, prendre un certain temps pour déterminer le nombre de stratégies que vous avez besoin et la priorité pour chacun. 
    
- Plan de consacrer environ 5 à 15 minutes pour définir votre stratégie d’anti-hameçonnage premier DAV.
    
- Autoriser jusqu'à 30 minutes pour votre stratégie de nouveau ou mis à jour pour se propager sur tous les centres de données Office 365.
    
## <a name="set-up-an-atp-anti-phishing-policy"></a>Configurer une stratégie d’anti-hameçonnage DAV

Vous ajouter, modifier et supprimer des stratégies d’anti-hameçonnage DAV de sécurité Office 365 &amp; centre de conformité.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. De sécurité Office 365 &amp; centre de conformité, dans le volet de navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie**.
    
3. Dans la page **stratégie** , choisissez **DAV anti-hameçonnage**.
    
4. Dans la page **Anti-hameçonnage** , effectuez l’une des options suivantes : 
    
  - Pour ajouter une nouvelle stratégie sélectionnez **+ créer**.
    
  - Pour modifier une stratégie existante, sélectionnez le nom de stratégie dans la liste affichée dans la page **Anti-hameçonnage** . Dans la page qui apparaît, choisissez **Modifier la stratégie**.
    
    Un Assistant démarre vous guider dans la définition de votre stratégie anti-hameçonnage.
    
5. Spécifiez le nom, description et paramètres de votre stratégie. Pour plus d’informations, consultez la rubrique [en savoir plus sur les options de stratégie anti-hameçonnage DAV](#learn-about-atp-anti-phishing-policy-options) . 
    
6. Une fois vous avez vérifié vos paramètres, choisissez **créer cette stratégie** ou **Enregistrer** comme il convient. 
    
## <a name="learn-about-atp-anti-phishing-policy-options"></a>En savoir plus sur les options de stratégie anti-hameçonnage DAV

En tant que vous configurer ou modifiez vos stratégies anti-hameçonnage DAV, vous pouvez choisir parmi plusieurs options, comme décrit dans le tableau suivant :
  
|**Ce paramètre**|**Effectue cette action**|**À utiliser lorsque vous souhaitez :**|
|:-----|:-----|:-----|
|**Ajouter des utilisateurs à protéger** <br/> |Définit les adresses de messagerie sont protégées par la stratégie. Vous pouvez ajouter jusqu'à 60 adresses internes et externes que vous souhaitez protéger contre l’emprunt d’identité.  <br/> |Lorsque vous souhaitez vous assurer que les messages depuis l’extérieur de votre organisation n’est pas un emprunt d’identité de l’un des utilisateurs dans la liste des utilisateurs que vous protégez. Exemples d’utilisateurs que vous souhaitez peut-être protéger sont les cadres supérieurs, les responsables d’entreprise, membres externes et ainsi de suite.<br/> Cette liste d’utilisateurs protégés est différente de la liste des utilisateurs auxquels la stratégie s’applique, ou plutôt, pour laquelle la stratégie est appliquée. Vous définissez le s’applique à la liste dans la section **s’applique aux** options de stratégie.<br/> Par exemple, si vous ajoutez Mary Smith \<marys@contoso.com\> en tant qu’utilisateur pour protéger, puis appliquer la stratégie pour le groupe « tous les utilisateurs ». Cela garantie qu’un message qui s’affiche pour emprunter l’identité « Mary Smith » est envoyé à un utilisateur dans le groupe « Tous les utilisateurs » serait effectuée par la stratégie.<br/> |
|**Ajouter des domaines à protéger** <br/> |Vous permet de choisir les domaines que vous souhaitez protéger contre l’emprunt d’identité. Vous pouvez spécifier que la stratégie inclut tous vos domaines personnalisés, une liste des domaines séparés par des virgules ou une combinaison des deux. Si vous choisissez **d’inclure automatiquement des domaines dont vous êtes propriétaire**, et vous ajoutez ultérieurement un domaine à votre organisation Office 365, cette stratégie anti-hameçonnage sera en place pour le nouveau domaine.<br/> |Chaque fois que vous voulez vous assurer que les messages depuis l’extérieur de votre organisation n’est pas un emprunt d’identité de l’un des domaines définis dans votre liste de domaines vérifiés ou celui d’un domaine partenaire.  <br/> |
|**Choisissez actions** <br/> |Choisissez l’action à effectuer lorsqu’Office 365 détecte une tentative d’emprunt d’identité contre les utilisateurs et les domaines que vous avez ajouté à la stratégie. Vous pouvez choisir des actions différentes pour les utilisateurs et les domaines dans la même stratégie anti-hameçonnage. Les actions suivantes s’appliquent à tout le courrier électronique entrant qui a été identifié par Office 365 comme l’emprunt d’identité d’un compte d’utilisateur ou d’un domaine qui se trouve sous la protection de cette stratégie anti-hameçonnage.<br/> **Message de quarantaine** E-mail sera envoyé à la mise en quarantaine d’Office 365. Lorsque vous choisissez cette option, le courrier électronique n’est pas envoyé au destinataire d’origine.<br/> **Rediriger le message vers une autre adresse de messagerie** Message électronique sera envoyé à l’adresse de messagerie que vous spécifiez. Vous pouvez spécifier plusieurs adresses de messagerie. Lorsque vous choisissez cette option, le courrier électronique n’est pas envoyé au destinataire d’origine.<br/> **Déplacer le message vers le dossier courrier indésirable de destinataires** Message électronique sera envoyé vers le dossier de courrier indésirable de destinataires. Lorsque vous choisissez cette option, le courrier électronique est toujours envoyé au destinataire d’origine, mais n’est pas placé dans la boîte de réception du destinataire.<br/> **Remettre le message et ajouter d’autres adresses à la ligne Cci** Courrier électronique est remis au destinataire d’origine. En outre, les utilisateurs que vous identifiez seront ajoutés à la ligne Cci du message avant sa remise. Lorsque vous choisissez cette option, le message est toujours envoyé à la boîte de réception du destinataire d’origine.<br/> **N’appliquez pas n’importe quelle action** Courrier électronique est remis à la boîte de réception du destinataire d’origine. Aucune autre action ne sera entreprise sur le message électronique.<br/> **Activer les conseils de protection anti-hameçonnage** Permet de conseils de sécurité anti-hameçonnage dans le message électronique.  <br/> |Lorsque vous souhaitez effectuer une action sur les messages Office 365 a déterminé un emprunt d’identité d’un utilisateur ou un domaine défini dans la stratégie.  <br/> |
|**Activer l’aide à la décision de boîte aux lettres** <br/> |Active ou désactive l’aide à la décision de boîte aux lettres pour cette stratégie. Vous ne pouvez activer aide à la décision de boîte aux lettres en nuage comptes, autrement dit, comptes de boîte aux lettres est hébergée intégralement dans Office 365.  <br/> |Lorsque vous souhaitez améliorer les résultats de l’emprunt d’identité pour les utilisateurs en fonction de feuille de route de chaque utilisateur individuel de l’expéditeur. Aide à la décision de boîte aux lettres repose sur les personnes vous envoyez et recevez des messages depuis. Cette aide à la décision permet à Office 365 personnaliser la stratégie de l’emprunt d’identité au niveau de l’utilisateur afin de mieux gérer les faux résultats positifs.  <br/> |
|**Ajouter des domaines et des expéditeurs approuvés** <br/> |Définit les adresses de messagerie et les domaines qui ne seront pas considérées comme des emprunts d’identité par cette stratégie. Messages des domaines et les adresses de messagerie de l’expéditeur ajouter en tant qu’expéditeurs approuvés et domaines ne jamais être considérés comme une attaque basée sur l’emprunt d’identité. Par conséquent, les actions et les paramètres de cette stratégie ne seront pas appliquées aux messages de ces expéditeurs et de domaines.  <br/> |Lorsque les utilisateurs interagissent avec les domaines ou les utilisateurs qui déclenchent l’emprunt d’identité, mais sont considérés comme sécurisés. Par exemple, si un partenaire a le même/similaire affichage nom ou nom de domaine en tant qu’utilisateur défini dans la liste.  <br/> |
|**Appliqué à** <br/> |Définit les destinataires dont les messages électroniques entrants seront soumis aux règles de la stratégie. Vous pouvez créer des conditions et exceptions pour les destinataires associés à la stratégie.  <br/> Par exemple, vous pouvez créer une stratégie globale pour votre organisation en appliquant la règle à tous les destinataires dans votre domaine.  <br/> Vous pouvez également créer des règles d’exception, par exemple une règle qui n’analyse pas les messages électroniques pour un groupe spécifique de destinataires.  <br/> |Chaque stratégie doit être associé à un ensemble d’utilisateurs, par exemple, les utilisateurs dans un domaine ou un groupe particulier.  <br/> |
|**Seuils de hameçonnage avancées** <br/> |Définit le niveau de paramètres pour le traitement des messages de phishing.  <br/> **Standard** Courrier électronique semble pour être hameçonnage est géré dans la méthode standard.  <br/> **Agressif** Courrier électronique semble pour être hameçonnage avec un niveau élevé ou très élevé de confiance sont gérés par le système de la même manière.  <br/> **Plus efficaces** Courrier électronique susceptibles d’être hameçonnage avec un moyen, élevé, ou très haut niveau de confiance sont gérés par le système de la même manière.  <br/> **Plus agressif** Courrier électronique semble pour être hameçonnage avec un niveau faible, moyen, élevé ou très élevé de confiance sont gérés par le système de la même manière.  <br/> |Lorsque vous souhaitez être plus efficaces dans le traitement des messages d’hameçonnage potentiellement dans Office 365. Par exemple, avec une probabilité très élevé d’être hameçonnage les messages aura les plus élevées actions effectuées sur les messages avec une probabilité faible ont moins agressives actions effectuées sur ceux-ci. Ce paramètre affecte également les autres composants du système de filtrage qui combinent les signaux. La possibilité de déplacer des messages augmente comme le niveau d’à l’augmentation de paramètres.  <br/> |
   
Une fois que votre organisation a configuré les stratégies anti-hameçonnage DAV, vous pouvez voir comment le service fonctionne en [affichant des rapports de protection contre les menaces avancées](view-reports-for-atp.md).
  
## <a name="example-anti-phishing-policy-to-protect-a-user-and-a-domain"></a>Exemple : Anti-hameçonnage de stratégie pour protéger un utilisateur et un domaine

Cet exemple montre comment définir une stratégie appelée « Domaine et CEO » qui offre une protection de l’emprunt d’identité utilisateur et de domaine, puis comment appliquer la stratégie dans tous les messages reçus par les utilisateurs dans le domaine `contoso.com`. L’administrateur de sécurité a déterminé que la stratégie doit répondre à ces besoins :
  
- La stratégie doit fournir une protection pour du directeur général compte et l’intégralité du domaine de messagerie.
    
- Messages qui sont déterminés à l’emprunt d’identité tentatives contre le compte d’utilisateur du PDG doivent être redirigés vers l’adresse de messagerie de l’administrateur de la sécurité.
    
- Les messages qui sont déterminés à l’emprunt d’identité tentatives par rapport au domaine sont moins urgentes et doivent être mis en quarantaine pour les consulter plus tard.
    
L’administrateur de sécurité chez Contoso peut utiliser des valeurs, comme ci-dessous afin de créer une stratégie anti-hameçonnage qui répond à ces besoins.
  
|||
|:-----|:-----|
|**Paramètre ou option** <br/> |**Exemple** <br/> |
|Name  <br/> |Domaine et PDG  <br/> |
|Description  <br/> |Assurez-vous que le PDG et notre domaine ne sont pas empruntées.  <br/> |
|Ajouter des utilisateurs à protéger  <br/> |Adresse de messagerie du PDG au minimum.  <br/> |
|Ajouter des domaines à protéger  <br/> |Le domaine d’organisation qui inclut le bureau du PDG.  <br/> |
|Choisissez actions  <br/> |Si le message électronique est envoyé par un compte d’utilisateur : cliquez sur **rediriger le message vers une autre adresse de messagerie** et tapez l’adresse de messagerie de l’administrateur de la sécurité, par exemple, `securityadmin@contoso.com`.  <br/> Si le message électronique est envoyé par un domaine d’emprunt d’identité : choisissez **message de quarantaine**.  <br/> |
|Aide à la décision de boîte aux lettres  <br/> |Par défaut, l’aide à la décision de boîte aux lettres est activée lorsque vous créez une nouvelle stratégie anti-hameçonnage. Laissez ce paramètre **sur** pour obtenir de meilleurs résultats.<br/> |
|Ajouter des domaines et des expéditeurs approuvés  <br/> |Cet exemple, ne définissez pas les substitutions.  <br/> |
|Appliqué à  <br/> |Sélectionnez **le domaine du destinataire**. Sous **une de ces**, sélectionnez **Choisir**. Sélectionnez **+ Ajouter**. Activez la case à cocher en regard du nom du domaine, par exemple, `contoso.com`, puis sélectionnez **Ajouter**dans la liste. Cliquez sur **terminé**.<br/> |
   
## <a name="delete-an-atp-anti-phishing-policy"></a>Supprimer une stratégie d’anti-hameçonnage DAV

Vous pouvez ajouter ou modifier des stratégies de sécurité &amp; centre de conformité. Nous recommandons l’utilisation de la sécurité &amp; centre de conformité pour consulter ou modifier un de vos stratégies DAV.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **une stratégie**.
    
3. Dans la page **stratégie** , choisissez **DAV anti-hameçonnage**.
    
4. Dans la page **Anti-hameçonnage** , sélectionnez le nom de stratégie dans la liste affichée dans la page **Anti-hameçonnage** . Dans la page qui s’affiche, cliquez sur **Supprimer la stratégie**. Autoriser jusqu'à 30 minutes pour que vos modifications à répartir pour tous les centres de données Office 365.
    
## <a name="related-topics"></a>Voir aussi

[Protection de Microsoft Office 365 menace avancées](office-365-atp.md)
  
[Protection anti-hameçonnage dans Office 365](anti-phishing-protection.md)
  
[Fonctionnalités anti-hameçonnage de DAV dans Office 365](atp-anti-phishing.md)
  
[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
  
[Définir des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)
  
[Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)
  

