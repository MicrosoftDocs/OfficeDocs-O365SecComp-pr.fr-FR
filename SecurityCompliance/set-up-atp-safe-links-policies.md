---
title: Définir des stratégies Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
description: Définir des stratégies de liens fiables pour protéger votre organisation contre les liens malveillants dans les fichiers Word, Excel, PowerPoint et Visio, ainsi que dans les messages électroniques.
ms.openlocfilehash: a0c88a81503555417c16501ec9283cf2316c6d09
ms.sourcegitcommit: a8884b9675559018e1fddec1c0cc2de0bc3bdde5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839974"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Définir des stratégies Office 365 DAV fiables liens

[Liens approuvés DAV](atp-safe-links.md) , une fonctionnalité d' [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), peuvent aider à protéger votre organisation à partir des liens malveillants utilisés dans les attaques par hameçonnage et d’autres attaques. Si vous avez nécessaires [autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md), vous pouvez définir des stratégies de liens fiables DAV pour s’assurer que lorsque les utilisateurs cliquent sur les adresses web (URL), votre organisation est protégée. Vos stratégies de liens fiables DAV peuvent être configurées pour analyser les URL dans le message électronique et les URL dans les documents Office.
  
Nouvelles fonctionnalités sont régulièrement ajoutées aux liens fiables DAV :
  
- Dans la liaison tardive octobre 2017, protection liens fiables DAV est étendue pour s’appliquent à l’URL dans le message électronique ainsi que les URL dans les documents Office 365 ProPlus, telles que Word, Excel, PowerPoint sur Windows, périphériques iOS ou Android et les fichiers de Visio sur un ordinateur Windows.
    
- Au début de mars 2018, protection liens fiables DAV est étendue s’appliquent aux messages envoyés entre les personnes dans une organisation.
    
- Au début de fin mars 2018, protection liens fiables DAV est étendue s’appliquent aux URL dans Office Online (Word en ligne, Online Excel, PowerPoint en ligne et OneNote en ligne) et Office 365 ProPlus sur Mac OS.
    
- [Pages d’avertissement](atp-safe-links-warning-pages.md) au début de mai 2018, sont mis à jour avec un nouveau jeu de couleurs, plus de détails et la possibilité de passer à un site malgré ces recommandations donnés. 

Ajout de nouvelles fonctionnalités, vous devrez peut-être ajuster vos stratégies DAV fiables liens existants.

## <a name="what-to-do"></a>Procédure 
  
1. [Passez en revue les composants requis](#review-the-prerequisites).
    
2. [Réviser et modifier la stratégie de liens fiables DAV par défaut qui s’applique à tout le monde](#define-an-atp-safe-links-policy-that-applies-to-everyone). Par exemple, vous pouvez [configurer votre liste des URL bloqué personnalisé pour les liens sécurisés DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md).
    
3. [Ajouter une stratégie pour les destinataires de courriers électroniques spécifique](#add-a-policy-for-specific-email-recipients), y compris [la configuration de votre liste des URL « Pas de rewrite » personnalisé pour les liens sécurisés DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
4. [Découvrez les options de stratégie de liens fiables DAV](#learn-about-atp-safe-links-policy-options) (dans cet article), notamment les paramètres pour les modifications récentes
    
## <a name="review-the-prerequisites"></a>Passez en revue les conditions préalables

- Assurez-vous que votre organisation dispose [d’Office 365 avancée protection contre les menaces](office-365-atp.md).
    
- Assurez-vous que vous avez nécessaires [autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
    
- [Découvrez les options de stratégie de liens fiables DAV](#learn-about-atp-safe-links-policy-options) (dans cet article). 
    
- Autoriser jusqu'à 30 minutes pour votre stratégie de nouveau ou mis à jour pour se propager sur tous les centres de données Office 365.
    
## <a name="define-an-atp-safe-links-policy-that-applies-to-everyone"></a>Définir une stratégie de liens fiables DAV qui s’applique à tout le monde

Lorsque vous avez protection contre les menaces avancées dans Office 365 pour entreprises, vous aurez une stratégie par défaut des liens fiables DAV qui s’applique à tout le monde dans votre organisation. Vous pouvez modifier votre stratégie de sécurité soit &amp; centre de conformité ou le centre d’administration Exchange. **Nous recommandons l’utilisation de la sécurité &amp; centre de conformité pour consulter ou modifier un de vos stratégies DAV**.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie \> ** **Liens fiables**.
    
3. Dans la section **stratégies qui s’appliquent à toute l’organisation** , sélectionnez **par défaut**, puis choisissez **Modifier** (le bouton Modifier ressemble à un crayon). 
    
    ![Cliquez sur Modifier pour modifier votre stratégie par défaut pour la protection des liens fiables](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Dans la section **bloquer les URL suivantes** , spécifiez une ou plusieurs URL que vous souhaitez empêcher les utilisateurs de votre organisation de se connecter. (Voir [configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md)).
    
5. Dans la section **paramètres qui s’appliquent au contenu, à l’exception du courrier électronique** , activez (ou désactivez) les options que vous souhaitez utiliser. (Nous vous conseillons de sélectionner toutes les options.) 
    
6. Sélectionnez **Enregistrer**.
    
## <a name="add-a-policy-for-specific-email-recipients"></a>Ajouter une stratégie pour les destinataires de messages électroniques spécifique

Après avoir consulté la stratégie pour tous les utilisateurs, vous pouvez définir des stratégies supplémentaires pour des groupes spécifiques de destinataires de courriers électroniques. Cela vous permet de spécifier des exceptions à votre stratégie par défaut. Vous pouvez ajouter des stratégies à l’aide de la sécurité de le &amp; centre de conformité (recommandé) ou le centre d’administration Exchange. **Nous recommandons l’utilisation de la sécurité &amp; centre de conformité pour consulter ou modifier un de vos stratégies DAV**.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **une stratégie**.
    
3. Choisissez **les liens sécurisés**.
    
4. Dans la section **stratégies qui s’appliquent à des destinataires spécifiques** , choisissez **Nouveau** (nouveau bouton ressemble à un signe plus ( **+**)).
    
    ![Cliquez sur Nouveau pour ajouter une stratégie de liens sécurisés pour les destinataires de messages électroniques spécifique](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Indiquez un nom, une description et des paramètres pour votre stratégie.
    
    **Exemple :** Pour configurer une stratégie appelée « sans direct par clic » qui n’autorise pas les personnes dans un certain groupe dans votre organisation pour cliquer sur un site Web spécifique sans protection liens fiables DAV, vous pouvez spécifier les éléments suivants de le paramètres recommandés : 
    
  - Dans la zone **nom** , ne tapez aucun direct aux clics publicitaires.
    
  - Dans la zone **Description** , tapez une description comme empêche les personnes à certains groupes provenant du clic par le biais d’un site Web sans la vérification des liens fiables DAV.
    
  - Dans la section **Sélectionnez l’action** , cliquez **sur**.
    
  - Sélectionnez **Les pièces jointes fiables à utiliser pour analyser du contenu téléchargeable**.
    
  - Si cette option est disponible, sélectionnez **Appliquer sans échec des liens vers des messages envoyés au sein de l’organisation**.
    
  - Sélectionnez **ne pas autoriser l’utilisateur de clic vers l’URL d’origine**.
    
  - (Cette étape est facultative) Dans la section **ne pas réécrire les URL suivantes** , spécifiez une ou plusieurs URL sont considérés comme sûrs pour votre organisation. (Voir [configurer une liste d’URL personnalisée du « Pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - Dans la section **Appliquée à** , sélectionnez **le destinataire est un membre du**, puis les groupes que vous souhaitez inclure dans votre stratégie de. Cliquez sur **Ajouter**, puis cliquez sur **OK**.
    
6. Sélectionnez **Enregistrer**.
    
## <a name="learn-about-atp-safe-links-policy-options"></a>En savoir plus sur les options de stratégie de liens fiables DAV

Comme vous configurez ou modifiez une stratégie de liens fiables DAV, verront plusieurs options disponibles. Au cas où vous vous demandez ces options, le tableau suivant décrit chaque option et son effet. Notez qu’il existe deux types principaux de stratégies pour définir ou modifier : une stratégie par défaut qui s’applique à tout le monde et des stratégies supplémentaires qui sont définies pour des destinataires spécifiques.
  
|**Pour cette stratégie.**|**Cette option**|**Effectue cette action**|
|:-----|:-----|:-----|
|Par défaut (une fois définies, la stratégie par défaut s’applique à tout le monde dans l’organisation)  <br/> |**Bloquer les URL suivantes** <br/> |Permet à votre organisation d’avoir une liste personnalisée d’URL qui sont bloqués automatiquement. Lorsque les utilisateurs cliquent sur une URL dans cette liste, il est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md) qui explique pourquoi l’URL est bloquée.<br/> Pour plus de détails, tels que de la prise en charge ajoutée pour trois astérisques générique, consultez [configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md) (\*).  <br/> |
|Par défaut  <br/> |**Office 365 ProPlus, Office pour iOS et Android** <br/> |Lorsque cette option est sélectionnée, les liens sécurisés DAV protection est appliquée aux URL dans les documents qui sont ouvrir dans Office 365 ProPlus (Word, Excel et PowerPoint sous Windows ou Mac OS), des documents Office sur iOS ou Android appareils, 2016 Visio sur Windows et Office Online (Word En ligne, PowerPoint Online, Excel Online et OneNote en ligne), fournies à que l’utilisateur s’est connecté à Office 365. </br></br>Si vous voyez uniquement **2016 Office sur Windows**, puis les mises à jour de la fonctionnalité ne parviennent pas à encore votre environnement Office 365 (et ils sont bientôt disponible). En attendant, protection liens fiables DAV s’applique à Word 2016, 2016 Excel, PowerPoint 2016 ou 2016 Visio en cours d’exécution sur Windows.           |
|Par défaut  <br/> |**Ne suivez pas lorsque les utilisateurs cliquent sur les liens sécurisés DAV** <br/> |Lorsque cette option est sélectionnée, cliquez sur données pour l’URL dans les documents Word, Excel, PowerPoint et Visio n’est pas stocké.  <br/> |
|Par défaut  <br/> |**Ne laissez pas vos utilisateurs cliquez sur par le biais de DAV fiables des liens vers des URL d’origine** <br/> |Lorsque cette option est sélectionnée, les utilisateurs ne peut pas continuer au-delà d’une [page d’avertissement](atp-safe-links-warning-pages.md) à une URL qui est définie comme étant malveillants.  <br/> |
|Une stratégie créée pour les destinataires de messages électroniques spécifique  <br/> |**Off** <br/> |N’analyse pas les URL dans les messages électroniques.  <br/> Vous permet de définir une règle d’exception, par exemple une règle qui n’analyse pas les URL dans les messages électroniques pour un groupe spécifique de destinataires.  <br/> |
|Une stratégie créée pour les destinataires de messages électroniques spécifique  <br/> |**Sur** <br/> |Réécrit URL aux utilisateurs d’itinéraire par le biais de protection des liens fiables DAV lorsque les utilisateurs cliquent sur les URL dans les messages électroniques.  <br/> Vérifie une URL lorsque vous cliquez sur par rapport à une liste d’URL bloquées ou malveillants.  <br/> |
|Une stratégie créée pour les destinataires de messages électroniques spécifique  <br/> |**Pièces jointes fiables permet d’analyser le contenu téléchargeable** <br/> |Lorsque cette option est sélectionnée, les URL qui pointent vers le contenu téléchargeable sont analysés.  <br/> |
|Une stratégie créée pour les destinataires de messages électroniques spécifique  <br/> |**Appliquez les liens sécurisés pour les messages envoyés au sein de l’organisation** <br/> | Lorsque cette option est disponible et activée, protection liens fiables DAV est appliquée pour les messages envoyés entre les personnes dans votre organisation, fournie les comptes de messagerie sont hébergées dans Office 365 les courriers électroniques.  <br/> |
|Une stratégie créée pour les destinataires de messages électroniques spécifique  <br/> |**Ne suivent pas les clics de l’utilisateur** <br/> |Lorsque cette option est sélectionnée, cliquez sur données pour l’URL dans le courrier provenant d’expéditeurs externes n’est pas stocké. Cliquez sur URL de suivi pour les liens dans les messages électroniques envoyés au sein de l’organisation n’est pas actuellement pris en charge.  <br/> |
|Une stratégie créée pour les destinataires de messages électroniques spécifique  <br/> |**Ne pas autoriser les utilisateurs à l’URL d’origine** <br/> |Lorsque cette option est sélectionnée, les utilisateurs ne peut pas continuer au-delà d’une [page d’avertissement](atp-safe-links-warning-pages.md) à une URL qui est définie comme étant malveillants.  <br/> |
|Une stratégie créée pour les destinataires de messages électroniques spécifique  <br/> |**Pas réécrire les URL suivantes** <br/> |Laisse les URL en tant qu’ils reçoivent. Tenir à jour une liste personnalisée d’URL fiables qui n’ont pas besoin d’analyse pour un groupe spécifique de destinataires de courriers électroniques dans votre organisation.  Pour plus d’informations, y compris les modifications récentes apportées pour prendre en charge pour le caractère générique astérisque, consultez [configurer une liste d’URL personnalisée du « Pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) (\*).<br/> |
   
## <a name="related-topics"></a>Voir aussi

[Protection de Microsoft Office 365 menace avancées](office-365-atp.md)
  
[Liens DAV Safe dans Office 365](atp-safe-links.md)
  
[Pièces jointes DAV Safe dans Office 365](atp-safe-attachments.md)
  
[Configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md)
  
[Configurer une liste d’URL personnalisée du « Pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)
  
[Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)

[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)
  

