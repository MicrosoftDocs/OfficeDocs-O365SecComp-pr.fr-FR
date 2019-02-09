---
title: Configuration des stratégies anti-hameçonnage ATP d’Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578
description: Protection anti-hameçonnage, avec une protection complète dans le cadre d’Office 365 avancée protection contre les menaces et de protection de base dans Office 365 Exchange Online Protection permet de protéger votre organisation contre les attaques malveillantes hameçonnage basée sur l’emprunt d’identité et autres attaques par hameçonnage.
ms.openlocfilehash: 333176ebef8d6367f5090730386fc820927cf3af
ms.sourcegitcommit: c1c41744c2de89c9e172f817c8f73bb0ada81a58
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792279"
---
# <a name="set-up-office-365-atp-anti-phishing-and-anti-phishing-policies"></a>Configurer des stratégies anti-hameçonnage et anti-hameçonnage d’Office 365 DAV

[Protection anti - hameçonnage DAV](atp-anti-phishing.md), composant d' [Office 365 avancée protection contre les menaces](office-365-atp.md), peuvent aider à protéger votre organisation contre les attaques malveillantes hameçonnage basée sur l’emprunt d’identité et autres hameçonnage. Si vous êtes un administrateur de sécurité ou d’Office 365 entreprise globale, vous pouvez configurer les stratégies anti-hameçonnage DAV. 

Hameçonnage attaques entrent dans diverses formes contre les attaques de marchandise sonde ciblé phishing ou baleine. À la complexité, il est difficile de même un œil formé à identifier certains de ces attaques sophistiquées. Heureusement, contre les menaces avancées Office 365 peut vous aider. Vous pouvez configurer une stratégie d’anti-hameçonnage DAV pour vous assurer que votre organisation est protégée contre les attaques de ce type.
  
> [!NOTE]
> DAV anti-hameçonnage n’est disponible dans Advanced Threat Protection (DAV). DAV est inclus dans les abonnements, tels que [Microsoft 365 pour entreprises](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation A5, etc.. Si votre organisation a un abonnement à Office 365 qui n’inclut pas d’Office 365 DAV, vous pouvez acheter potentiellement DAV comme module complémentaire. Pour plus d’informations, voir [plans Office 365 avancée protection contre les menaces et les prix](https://products.office.com/exchange/advance-threat-protection) et [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). Assurez-vous que votre organisation utilise la dernière version d’Office 365 ProPlus sur Windows pour tirer pleinement parti de protection anti-hameçonnage DAV. 

Une stratégie anti-hameçonnage est également disponible pour Office 365 Exchange Online Protection, avec un ensemble limité de protection anti-l’usurpation d’identité qui est destiné à protéger contre les attaques basées sur la description et l’authentification.
  
Procédure à suivre :
  
1. Passez en revue les composants requis.
    
2. Découvrez les options de stratégie anti-hameçonnage DAV anti-hameçonnage.
    
3. Configurer une stratégie anti-hameçonnage ou une stratégie d’anti-hameçonnage DAV.
    
## <a name="review-the-prerequisites"></a>Passez en revue les conditions préalables

- Pour définir (ou modifier) les stratégies de vente, vous devez posséder un des rôles décrits dans le tableau suivant : <br>

    |Rôle  |Où/procédure affecté  |
    |---------|---------|
    |Administrateur Global d’Office 365 |La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).         |
    |Administrateur de sécurité |Centre d’administration Active Directory Azure ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
    |Gestion de l’organisation en ligne Exchange |Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
    Pour en savoir plus sur les rôles et autorisations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).

- Vous définirez probablement plusieurs stratégies anti-hameçonnage pour votre organisation. Office 365 applique ces stratégies dans l’ordre d’apparition dans les pages de **page Anti-hameçonnage** et **DAV anti-hameçonnage** dans la sécurité &amp; centre de conformité. Une fois que vous avez passé en revue vos [options de stratégie](#learn-about-atp-anti-phishing-policy-options), prendre un certain temps pour déterminer le nombre de stratégies que vous avez besoin et la priorité pour chacun. 
    
- Plan de consacrer environ 5 à 15 minutes pour configurer votre première stratégie anti-hameçonnage.
    
- Autoriser jusqu'à 30 minutes pour votre stratégie de nouveau ou mis à jour pour se propager sur tous les centres de données Office 365.
    
## <a name="set-up-an-anti-phishing-or-atp-anti-phishing-policy"></a>Configurer une stratégie d’anti-hameçonnage de DAV ou d’anti-hameçonnage

Chaque organisation dans Office 365 dispose d’une stratégie par défaut anti-hameçonnage qui s’applique à tous les utilisateurs. Vous pouvez créer plusieurs stratégies anti-hameçonnage personnalisées que vous pouvez limiter l’étendue à des utilisateurs spécifiques, des groupes ou des domaines au sein de votre organisation. Les stratégies personnalisées que vous créez sont prioritaires sur la stratégie par défaut. Vous ajouter, modifier et supprimer des stratégies anti-hameçonnage de sécurité Office 365 &amp; centre de conformité.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. De sécurité Office 365 &amp; centre de conformité, dans le volet de navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie**.
    
3. Dans la page **stratégie** , choisissez **Anti-hameçonnage** ou **DAV anti-hameçonnage**.
    
4. Dans la page **Anti-hameçonnage** ou **DAV anti-hameçonnage** , effectuez l’une des options suivantes : 
    
    - Pour ajouter une nouvelle stratégie sélectionnez **+ créer**.
    - Pour modifier une stratégie existante, sélectionnez le nom de stratégie dans la liste affichée dans la page **Anti-hameçonnage** . (Également, vous pouvez ou sélectionnez **Stratégie par défaut** au-dessus de la liste). Dans la page qui apparaît, choisissez **Modifier la stratégie**.  
    
5. Spécifiez le nom, description et paramètres de votre stratégie. Pour plus d’informations, consultez la rubrique [en savoir plus sur les options de stratégie anti-hameçonnage DAV](#learn-about-atp-anti-phishing-policy-options) . 
    
6. Une fois que vous avez passé en revue vos paramètres, choisissez **créer cette stratégie** (ou **Enregistrer**). 
    
## <a name="learn-about-atp-anti-phishing-policy-options"></a>En savoir plus sur les options de stratégie anti-hameçonnage DAV

Comme vous configurez ou modifiez vos stratégies anti-hameçonnage de DAV, vous pouvez choisir parmi plusieurs options qui fournissent la protection complète et plus sophistiquée, comme décrit dans le tableau suivant :
  
|**Ce paramètre**|**Effectue cette action**|**À utiliser lorsque vous souhaitez :**|
|:-----|:-----|:-----|
|**Ajouter des utilisateurs à protéger** <br/> |Définit les adresses de messagerie sont protégées par la stratégie. Vous pouvez ajouter jusqu'à 60 adresses internes et externes que vous souhaitez protéger contre l’emprunt d’identité.  <br/> |Lorsque vous souhaitez vous assurer que les messages depuis l’extérieur de votre organisation n’est pas un emprunt d’identité de l’un des utilisateurs dans la liste des utilisateurs que vous protégez. Exemples d’utilisateurs que vous souhaitez peut-être protéger sont les cadres supérieurs, les responsables d’entreprise, membres externes et ainsi de suite.<br/> Cette liste d’utilisateurs protégés est différente de la liste des utilisateurs auxquels la stratégie s’applique, ou plutôt, pour laquelle la stratégie est appliquée. Vous définissez le s’applique à la liste dans la section **s’applique aux** options de stratégie.<br/> Par exemple, si vous ajoutez `Mary Smith <marys@contoso.com>` en tant qu’utilisateur pour protéger, puis appliquer la stratégie pour le groupe « tous les utilisateurs ». Cela garantie qu’un message qui s’affiche pour emprunter l’identité « Mary Smith » est envoyé à un utilisateur dans le groupe « Tous les utilisateurs » serait effectuée par la stratégie.<br/> |
|**Ajouter des domaines à protéger** <br/> |Vous permet de choisir les domaines que vous souhaitez protéger contre l’emprunt d’identité. Vous pouvez spécifier que la stratégie inclut tous vos domaines personnalisés, une liste des domaines séparés par des virgules ou une combinaison des deux. Si vous choisissez **d’inclure automatiquement des domaines dont vous êtes propriétaire**, et vous ajoutez ultérieurement un domaine à votre organisation Office 365, cette stratégie anti-hameçonnage sera en place pour le nouveau domaine.<br/> |Chaque fois que vous voulez vous assurer que les messages depuis l’extérieur de votre organisation n’est pas un emprunt d’identité de l’un des domaines définis dans votre liste de domaines vérifiés ou celui d’un domaine partenaire.  <br/> |
|**Choisissez actions** <br/> |Choisissez l’action à effectuer lorsqu’Office 365 détecte une tentative d’emprunt d’identité contre les utilisateurs et les domaines que vous avez ajouté à la stratégie. Vous pouvez choisir des actions différentes pour les utilisateurs et les domaines dans la même stratégie anti-hameçonnage. Les actions suivantes s’appliquent à tout le courrier électronique entrant qui a été identifié par Office 365 comme l’emprunt d’identité d’un compte d’utilisateur ou d’un domaine qui se trouve sous la protection de cette stratégie anti-hameçonnage.<br/> **Message de quarantaine** E-mail sera envoyé à la mise en quarantaine d’Office 365. Lorsque vous choisissez cette option, le courrier électronique n’est pas envoyé au destinataire d’origine.<br/> **Rediriger le message vers une autre adresse de messagerie** Message électronique sera envoyé à l’adresse de messagerie que vous spécifiez. Vous pouvez spécifier plusieurs adresses de messagerie. Lorsque vous choisissez cette option, le courrier électronique n’est pas envoyé au destinataire d’origine.<br/> **Déplacer le message vers le dossier courrier indésirable de destinataires** Message électronique sera envoyé vers le dossier de courrier indésirable de destinataires. Lorsque vous choisissez cette option, le courrier électronique est toujours envoyé au destinataire d’origine, mais n’est pas placé dans la boîte de réception du destinataire.<br/> **Remettre le message et ajouter d’autres adresses à la ligne Cci** Courrier électronique est remis au destinataire d’origine. En outre, les utilisateurs que vous identifiez seront ajoutés à la ligne Cci du message avant sa remise. Lorsque vous choisissez cette option, le message est toujours envoyé à la boîte de réception du destinataire d’origine.<br/> **N’appliquez pas n’importe quelle action** Courrier électronique est remis à la boîte de réception du destinataire d’origine. Aucune autre action ne sera entreprise sur le message électronique.<br/> **Activer les conseils de protection anti-hameçonnage** Permet de conseils de sécurité anti-hameçonnage dans le message électronique.  <br/> |Lorsque vous souhaitez effectuer une action sur les messages Office 365 a déterminé un emprunt d’identité d’un utilisateur ou un domaine défini dans la stratégie.  <br/> |
|**Activer l’aide à la décision de boîte aux lettres** <br/> |Active ou désactive l’aide à la décision de boîte aux lettres pour cette stratégie. Vous ne pouvez activer aide à la décision de boîte aux lettres en nuage comptes, autrement dit, comptes de boîte aux lettres est hébergée intégralement dans Office 365.  <br/> |Lorsque vous souhaitez améliorer les résultats de l’emprunt d’identité pour les utilisateurs en fonction de feuille de route de chaque utilisateur individuel de l’expéditeur. Aide à la décision de boîte aux lettres repose sur les personnes vous envoyez et recevez des messages depuis. Cette aide à la décision permet à Office 365 personnaliser la stratégie de l’emprunt d’identité au niveau de l’utilisateur afin de mieux gérer les faux résultats positifs.  <br/> |
|**Ajouter des domaines et des expéditeurs approuvés** <br/> |Définit les adresses de messagerie et les domaines qui ne seront pas considérées comme des emprunts d’identité par cette stratégie. Messages des domaines et les adresses de messagerie de l’expéditeur ajouter en tant qu’expéditeurs approuvés et domaines ne jamais être considérés comme une attaque basée sur l’emprunt d’identité. Par conséquent, les actions et les paramètres de cette stratégie ne seront pas appliquées aux messages de ces expéditeurs et de domaines.  <br/> |Lorsque les utilisateurs interagissent avec les domaines ou les utilisateurs qui déclenchent l’emprunt d’identité, mais sont considérés comme sécurisés. Par exemple, si un partenaire a le même/similaire affichage nom ou nom de domaine en tant qu’utilisateur défini dans la liste.  <br/> |
|**Appliqué à** <br/> |Définit les destinataires dont les messages électroniques entrants seront soumis aux règles de la stratégie. Vous pouvez créer des conditions et exceptions pour les destinataires associés à la stratégie.  <br/> Par exemple, vous pouvez créer une stratégie globale pour votre organisation en appliquant la règle à tous les destinataires dans votre domaine.  <br/> Vous pouvez également créer des règles d’exception, par exemple une règle qui n’analyse pas les messages électroniques pour un groupe spécifique de destinataires.  <br/> |Chaque stratégie doit être associé à un ensemble d’utilisateurs, par exemple, les utilisateurs dans un domaine ou un groupe particulier.  <br/> |
|**Seuils de hameçonnage avancées** <br/> |Définit le niveau de paramètres pour le traitement des messages de phishing.  <br/> **Standard** Courrier électronique semble pour être hameçonnage est géré dans la méthode standard.  <br/> **Agressif** Courrier électronique semble pour être hameçonnage avec un niveau élevé ou très élevé de confiance sont gérés par le système de la même manière.  <br/> **Plus efficaces** Courrier électronique susceptibles d’être hameçonnage avec un moyen, élevé, ou très haut niveau de confiance sont gérés par le système de la même manière.  <br/> **Plus agressif** Courrier électronique semble pour être hameçonnage avec un niveau faible, moyen, élevé ou très élevé de confiance sont gérés par le système de la même manière.  <br/> |Lorsque vous souhaitez être plus efficaces dans le traitement des messages d’hameçonnage potentiellement dans Office 365. Par exemple, avec une probabilité très élevé d’être hameçonnage les messages aura les plus élevées actions effectuées sur les messages avec une probabilité faible ont moins agressives actions effectuées sur ceux-ci. Ce paramètre affecte également les autres composants du système de filtrage qui combinent les signaux. La possibilité de déplacer des messages augmente comme le niveau d’à l’augmentation de paramètres.  <br/>|
   
## <a name="learn-about-anti-phishing-policy-options"></a>En savoir plus sur les options de stratégie anti-hameçonnage 

En tant que vous configurer ou modifiez votre anti-hameçonnage, vous pouvez choisir parmi plusieurs options, comme décrit dans le tableau suivant : 

|**Ce paramètre**|**Effectue cette action**|**À utiliser lorsque vous souhaitez :**|
|:-----|:-----|:-----|
|**Appliqué à** <br/> |Définit les destinataires dont les messages électroniques entrants seront soumis aux règles de la stratégie. Vous pouvez créer des conditions et exceptions pour les destinataires associés à la stratégie.  <br/> Par exemple, vous pouvez créer une stratégie globale pour votre organisation en appliquant la règle à tous les destinataires dans votre domaine.  <br/> Vous pouvez également créer des règles d’exception, par exemple une règle qui n’analyse pas les messages électroniques pour un groupe spécifique de destinataires.  <br/> |Chaque stratégie doit être associé à un ensemble d’utilisateurs, par exemple, les utilisateurs dans un domaine ou un groupe particulier.  <br/> | 
|**Choisissez actions** <br/> |Choisissez l’action à effectuer lorsqu’Office 365 détecte une tentative d’usurpation d’identité à l’organisation interne ou externe à l’organisation par rapport à vos utilisateurs. Les actions suivantes s’appliquent à tout le courrier électronique entrant qui a été identifié par Office 365 comme une tentative d’usurpation d’identité pour les utilisateurs qui sont sous la protection de cette stratégie anti-hameçonnage.<br/> **Message de quarantaine** E-mail sera envoyé à la mise en quarantaine d’Office 365. Lorsque vous choisissez cette option, le courrier électronique n’est pas envoyé au destinataire d’origine.<br/> **Déplacer le message vers le dossier courrier indésirable de destinataires** Message électronique sera envoyé vers le dossier de courrier indésirable de destinataires. Lorsque vous choisissez cette option, le courrier électronique est toujours envoyé au destinataire d’origine, mais n’est pas placé dans la boîte de réception du destinataire.<br/> **N’appliquez pas n’importe quelle action** Courrier électronique est remis à la boîte de réception du destinataire d’origine. Aucune autre action ne sera entreprise sur le message électronique.<br/> |Lorsque vous souhaitez effectuer une action sur les messages Office 365 a déterminé une tentative d’usurpation des domaines internes ou externes telle que définie dans la stratégie.  <br/>|

Une fois que votre organisation a configuré des stratégies d’anti-hameçonnage ou anti-hameçonnage DAV, vous pouvez voir comment le service fonctionne en [affichant des rapports de protection contre les menaces avancées](view-reports-for-atp.md).
  
## <a name="example-anti-phishing-policy-to-protect-a-user-and-a-domain"></a>Exemple : Anti-hameçonnage de stratégie pour protéger un utilisateur et un domaine

Cet exemple montre comment définir une stratégie appelée « Domaine et CEO » qui offre une protection de l’emprunt d’identité utilisateur et de domaine, puis comment appliquer la stratégie dans tous les messages reçus par les utilisateurs dans le domaine `contoso.com`. L’administrateur de sécurité a déterminé que la stratégie doit répondre à ces besoins :
  
- La stratégie doit fournir une protection pour du directeur général compte et l’intégralité du domaine de messagerie.
    
- Messages qui sont déterminés à l’emprunt d’identité tentatives contre le compte d’utilisateur du PDG doivent être redirigés vers l’adresse de messagerie de l’administrateur de la sécurité.
    
- Les messages qui sont déterminés à l’emprunt d’identité tentatives par rapport au domaine sont moins urgentes et doivent être mis en quarantaine pour les consulter plus tard.
    
L’administrateur de sécurité chez Contoso peut utiliser des valeurs, comme ci-dessous afin de créer une stratégie anti-hameçonnage qui répond à ces besoins.
  
|||
|:-----|:-----|
|**Paramètre ou option** <br/> |**Exemple** <br/> |
|Nom  <br/> |Domaine et PDG  <br/> |
|Description  <br/> |Assurez-vous que le PDG et notre domaine ne sont pas empruntées.  <br/> |
|Ajouter des utilisateurs à protéger  <br/> |Adresse de messagerie du PDG au minimum.  <br/> |
|Ajouter des domaines à protéger  <br/> |Le domaine d’organisation qui inclut le bureau du PDG.  <br/> |
|Choisissez actions  <br/> |Si le message électronique est envoyé par un compte d’utilisateur : cliquez sur **rediriger le message vers une autre adresse de messagerie** et tapez l’adresse de messagerie de l’administrateur de la sécurité, par exemple, `securityadmin@contoso.com`.  <br/> Si le message électronique est envoyé par un domaine d’emprunt d’identité : choisissez **message de quarantaine**.  <br/> |
|Aide à la décision de boîte aux lettres  <br/> |Par défaut, l’aide à la décision de boîte aux lettres est activée lorsque vous créez une nouvelle stratégie anti-hameçonnage. Laissez ce paramètre **sur** pour obtenir de meilleurs résultats.<br/> |
|Ajouter des domaines et des expéditeurs approuvés  <br/> |Cet exemple, ne définissez pas les substitutions.  <br/> |
|Appliqué à  <br/> |Sélectionnez **le domaine du destinataire**. Sous **une de ces**, sélectionnez **Choisir**. Sélectionnez **+ Ajouter**. Activez la case à cocher en regard du nom du domaine, par exemple, `contoso.com`, puis sélectionnez **Ajouter**dans la liste. Cliquez sur **terminé**.<br/> |
   
## <a name="delete-an-anti-phishing-or-atp-anti-phishing-policy"></a>Supprimer une stratégie d’anti-hameçonnage de DAV ou d’anti-hameçonnage

Vous pouvez supprimer des stratégies personnalisées que vous avez créé à l’aide de la sécurité &amp; centre de conformité. Vous ne pouvez pas supprimer la stratégie par défaut pour votre organisation. Nous recommandons l’utilisation de la sécurité &amp; centre de conformité pour consulter ou modifier un de vos stratégies DAV.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **une stratégie**.
    
3. Dans la page **stratégie** , choisissez **Anti-hameçonnage** ou **DAV anti-hameçonnage**.
    
4. Dans la page **Anti-hameçonnage** ou **DAV anti-hameçonnage** , sélectionnez le nom de stratégie dans la liste.

5. Dans la page qui s’affiche, cliquez sur **Supprimer la stratégie**. Autoriser jusqu'à 30 minutes pour que vos modifications à répartir pour tous les centres de données Office 365.
    

## <a name="next-steps"></a>Étapes suivantes

Une fois vos stratégies anti-hameçonnage sont mis en place, vous pouvez voir le fonctionnement des fonctions de protection de menace pour votre organisation en affichant des rapports. Voir les ressources suivantes pour en savoir plus :
- [Afficher les rapports pour Office 365 avancée protection contre les menaces](view-reports-for-atp.md) ou [Afficher les rapports de sécurité de messagerie](view-email-security-reports.md)
- [Utilisez l’Explorateur (également appelé Threat Explorer)](use-explorer-in-security-and-compliance.md)

Maîtriser les nouvelles fonctionnalités en DAV. visitez le site de la [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) et découvrez les [nouvelles fonctionnalités qui sont ajoutées à DAV](office-365-atp.md#new-features-are-continually-being-added-to-atp).
 