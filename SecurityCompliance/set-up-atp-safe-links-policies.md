---
title: Configuration des stratégies de liens approuvés Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 02/26/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
ms.collection:
- M365-security-compliance
description: Configurez des stratégies de liens fiables pour protéger votre organisation contre les liens malveillants dans les fichiers Word, Excel, PowerPoint et Visio, ainsi que dans les messages électroniques.
ms.openlocfilehash: fd67562955e14bf5d94280ad6bc8afcd72bcbeb5
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077230"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Configuration des stratégies de liens approuvés Office 365 ATP

> [!IMPORTANT]
> Cet article est destiné aux clients Office 365 entreprise. Si vous utilisez Outlook.com, Office 365 Home ou Office 365 Personal, et que vous recherchez des informations sur les liens fiables dans Outlook, consultez [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Les [liens fiables ATP](atp-safe-links.md), une fonctionnalité d' [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), peuvent vous aider à protéger votre organisation contre les liens malveillants utilisés dans le hameçonnage et les autres attaques. Si vous disposez des [autorisations nécessaires pour le centre de sécurité &amp; conformité Office 365](permissions-in-the-security-and-compliance-center.md), vous pouvez configurer des stratégies de liens fiables ATP afin de vous assurer que lorsque des utilisateurs cliquent sur des adresses Web (URL), votre organisation est protégée. Vos stratégies de liens fiables ATP peuvent être configurées pour analyser les URL dans les messages électroniques et les URL des documents Office.
  
De [nouvelles fonctionnalités sont continuellement ajoutées à](office-365-atp.md#new-features-in-office-365-atp)la protection avancée contre les menaces. À mesure que de nouvelles fonctionnalités sont ajoutées, vous devrez peut-être apporter des modifications à vos stratégies de liens approuvés pour l’ATP existantes.

## <a name="what-to-do"></a>Procédure 
  
1. Passez en revue les conditions préalables.
    
2. Passez en revue et modifiez la stratégie de liens approuvés par défaut ATP qui s’applique à tout le monde. Par exemple, vous pouvez [configurer votre liste d’URL bloquées personnalisées pour les liens fiables ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md).
    
3. Ajouter ou modifier des stratégies pour des destinataires de messagerie spécifiques, y compris [la configuration de votre liste d’URL «ne pas réécrire» personnalisée pour les liens fiables ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
4. Découvrez les options de stratégie de liens approuvés ATP (dans cet article), y compris les paramètres pour les modifications récentes.
    
## <a name="step-1-review-the-prerequisites"></a>Étape 1: vérifier les conditions préalables

- Assurez-vous que votre organisation dispose de la [protection avancée contre les menaces d’Office 365](office-365-atp.md).
    
- Assurez-vous que vous disposez des autorisations nécessaires. Pour définir (ou modifier) des stratégies ATP, vous devez disposer d’un rôle approprié. Certains exemples sont décrits dans le tableau suivant: <br>

    |Role  |WHERE/How Assigned  |
    |---------|---------|
    |Administrateur général Office 365 |La personne qui s’inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d’administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
    |Administrateur de sécurité |Centre d’administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()|
    |Gestion de l’organisation Exchange Online |Centre d’administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>ou <br>  Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

    Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations &amp; dans le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).

- Assurez-vous que les clients Office sont configurés pour utiliser [l’authentification moderne](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) (il s’agit de la protection des liens fiables ATP dans les documents Office).
    
- [En savoir plus sur les options de stratégie de liens fiables ATP](#step-4-learn-about-atp-safe-links-policy-options) (dans cet article). 

- Attendez jusqu’à 30 minutes que votre stratégie nouvelle ou mise à jour se propage à tous les centres de mises à jour Office 365.
    
## <a name="step-2-define-or-review-the-atp-safe-links-policy-that-applies-to-everyone"></a>Étape 2: définition (ou révision) de la stratégie de liens approuvés ATP qui s’applique à tout le monde

Lorsque vous disposez de la [protection avancée contre les menaces Office 365](office-365-atp.md), vous disposez d’une stratégie de liens approuvés par défaut disponible pour tous les membres de votre organisation. Vérifiez et, si nécessaire, modifiez votre stratégie par défaut.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire. 
    
2. Dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez **liens approuvés**de **stratégie \> ** .
    
3. Dans la section **stratégies qui s’appliquent à l’ensemble de l’organisation** , sélectionnez **par défaut**, puis **modifier** (le bouton modifier ressemble à un crayon).<br/>![Cliquez sur modifier pour modifier votre stratégie par défaut pour la protection des liens fiables.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Dans la section **bloquer les URL suivantes** , spécifiez une ou plusieurs URL pour lesquelles vous souhaitez empêcher les personnes de votre organisation de se visiter. (Voir [configurer une liste d’URL bloquées personnalisées à l’aide de liens fiables ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md).)
    
5. Dans la section **paramètres qui s’appliquent au contenu à l’exception de la messagerie** , activez (ou désactivez) les options que vous souhaitez utiliser. (Nous vous recommandons de sélectionner toutes les options.) 
    
6. Choisissez **Enregistrer**.
    
## <a name="step-3-add-or-edit-atp-safe-links-policies-that-apply-to-specific-email-recipients"></a>Étape 3: ajouter (ou modifier) des stratégies de liens fiables ATP qui s’appliquent à des destinataires de messagerie spécifiques

Une fois que vous avez révisé (ou modifié) la stratégie de liens approuvés ATP par défaut qui s’applique à tout le monde, l’étape suivante consiste à définir des stratégies supplémentaires qui s’appliqueront à des destinataires spécifiques. Par exemple, vous pouvez spécifier des exceptions à votre stratégie par défaut en définissant une stratégie supplémentaire. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire. 
    
2. Dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez **stratégie**.
    
3. Choisissez **liens fiables**.
    
4. Dans la section **stratégies qui s’appliquent à des destinataires spécifiques** , sélectionnez **nouveau** (le nouveau bouton ressemble à **+** un signe plus ()).<br/>![Sélectionnez nouveau pour ajouter une stratégie de liens fiables à des destinataires de messagerie spécifiques.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Indiquez un nom, une description et des paramètres pour votre stratégie.<br/>**Exemple:** Pour configurer une stratégie appelée «pas de clics directs» qui n’autorise pas les personnes appartenant à un certain groupe dans votre organisation à cliquer sur un site Web spécifique sans protection contre les liaisons fiables ATP, vous pouvez spécifier les paramètres recommandés suivants: 
    
  - Dans la zone **nom** , tapez pas de clic direct.
    
  - Dans la zone **Description** , tapez une description telle que, empêche les personnes de certains groupes de cliquer sur un site Web sans la vérification des liens fiables ATP.
    
  - Dans la section **Sélectionnez l’action** , choisissez **activé**.
    
  - Sélectionnez **utiliser les pièces jointes approuvées pour analyser le contenu**téléchargeable.
    
  - Si cette option est disponible, sélectionnez **appliquer les liens fiables aux messages envoyés au sein de l’organisation**.
    
  - Sélectionnez **ne pas autoriser l’utilisateur à cliquer vers l’URL d’origine**.
    
  - (Cette option est facultative) Dans la section **ne pas réécrire les URL suivantes** , spécifiez une ou plusieurs URL considérées comme sûres pour votre organisation. (Voir [configurer une liste d’URL «ne pas réécrire» personnalisée à l’aide des liens fiables ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - Dans la section **appliqué à** , choisissez **le destinataire est membre de**, puis choisissez le ou les groupes que vous souhaitez inclure dans votre stratégie. Choisissez **Ajouter**, puis choisissez **OK**.
    
6. Choisissez **Enregistrer**.
    
## <a name="step-4-learn-about-atp-safe-links-policy-options"></a>Étape 4: en savoir plus sur les options de stratégie de liens approuvés ATP

Lorsque vous configurez ou modifiez vos stratégies de liens fiables ATP, plusieurs options sont disponibles. Si vous vous demandez ce que vous devez faire, le tableau suivant décrit chacun d’entre eux et son effet. N’oubliez pas qu’il existe deux types principaux de stratégies de liens fiables ATP à définir ou modifier:
- une [stratégie par défaut](#default-policy-options) qui s’applique à tous les utilisateurs; les  
- [stratégies supplémentaires pour des destinataires spécifiques](#policies-that-apply-to-specific-email-recipients) 

### <a name="default-policy-options"></a>Options de stratégie par défaut

Les options de stratégie par défaut s’appliquent à tous les membres de votre organisation.

|Cette option  |Effectue cette action  |
|---------|---------|
| **Bloquer les URL suivantes** <br/>    | Permet à votre organisation d’avoir une liste personnalisée d’URL qui sont automatiquement bloquées. Lorsque les utilisateurs cliquent sur une URL de cette liste, ils sont dirigés vers une [page d’avertissement](atp-safe-links-warning-pages.md) expliquant pourquoi l’URL est bloquée. Pour plus d’informations, consultez [la rubrique Configurer une liste d’URL bloquées personnalisées à l’aide des liens de sécurité ATP Office 365](set-up-a-custom-blocked-urls-list-wtih-atp.md). |
| **Office 365 ProPlus, Office pour iOS et Android** <br/>    | Lorsque cette option est sélectionnée, la protection des liens fiables ATP est appliquée aux URL dans les fichiers Word, Excel et PowerPoint sur Windows ou Mac OS, les documents Office sur iOS ou les appareils Android, Visio 2016 sur Windows et Office Online (Word Online, PowerPoint Online, Excel Online, et OneNote Online), à condition que l’utilisateur s’est connecté à Office 365. |
| **Ne pas suivre lorsque les utilisateurs cliquent sur les liens fiables ATP** <br/>  | Lorsque cette option est sélectionnée, les données des URL dans les documents Word, Excel, PowerPoint et Visio ne sont pas stockées.  <br/> |
|**Ne pas autoriser les utilisateurs à cliquer sur les liens fiables ATP vers l’URL d’origine** <br/> |Lorsque cette option est sélectionnée, les utilisateurs ne peuvent pas passer une [page d’avertissement](atp-safe-links-warning-pages.md) à une URL qui est considérée comme malveillante.  <br/> |

### <a name="policies-that-apply-to-specific-email-recipients"></a>Stratégies qui s’appliquent à des destinataires de messagerie spécifiques

|Cette option  |Effectue cette action  |
|---------|---------|
|**Désactivé** <br/> |N’analyse pas les URL dans les messages électroniques.  <br/> Vous permet de définir une règle d’exception, telle qu’une règle qui n’analyse pas les URL dans les messages électroniques pour un groupe spécifique de destinataires.  <br/> |
|**On** <br/> |Réécrit les URL pour acheminer les utilisateurs via la protection de liens fiables ATP lorsque les utilisateurs cliquent sur les URL dans les messages électroniques.  <br/> Vérifie une URL lorsque vous cliquez sur une liste d’URL bloquées ou malveillantes.  <br/> |
|**Utiliser les pièces jointes fiables pour analyser le contenu téléchargeable** <br/> |Lorsque cette option est sélectionnée, les URL qui pointent vers du contenu téléchargeable sont analysées.  <br/> |
|**Appliquer des liens fiables aux messages envoyés au sein de l’Organisation** <br/> | Lorsque cette option est disponible et sélectionnée, la protection des liens fiables ATP est appliquée aux messages électroniques envoyés entre les personnes de votre organisation, à condition que les comptes de messagerie soient hébergés dans Office 365.  <br/> |
|**Ne pas suivre les clics des utilisateurs** <br/> |Lorsque cette option est sélectionnée, les données des URL des expéditeurs externes ne sont pas stockées. URL le suivi des liens dans les messages électroniques envoyés au sein de l’organisation n’est pas pris en charge actuellement.  <br/> |
|**Ne pas autoriser les utilisateurs à cliquer vers l’URL d’origine** <br/> |Lorsque cette option est sélectionnée, les utilisateurs ne peuvent pas passer une [page d’avertissement](atp-safe-links-warning-pages.md) à une URL qui est considérée comme malveillante.  <br/> |
|**Ne pas réécrire les URL suivantes** <br/> |Laisse les URL telles quelles. Conserve une liste personnalisée d’URL sûres qui n’ont pas besoin d’être analysées pour un groupe spécifique de destinataires de messagerie dans votre organisation.  Pour plus d’informations, reportez-vous à [la rubrique Configurer une liste d’URL «ne pas réécrire» personnalisée à l’aide de liens fiables ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) , y compris les modifications récentes de la prise en charge des astérisques génériques (\*).  <br/> |
   
## <a name="next-steps"></a>Étapes suivantes

Une fois vos stratégies de liens fiables ATP en place, vous pouvez voir le fonctionnement de la protection avancée contre les menaces pour votre orgnization en affichant des rapports. Pour en savoir plus, consultez les ressources suivantes:

- [Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)

- [Utiliser l’Explorateur dans le &amp; Centre de sécurité conformité](use-explorer-in-security-and-compliance.md)

Restez au fait des nouvelles fonctionnalités disponibles dans la protection avancée contre les menaces. consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) et découvrez les [nouvelles fonctionnalités qui sont ajoutées à](office-365-atp.md#new-features-in-office-365-atp)la protection avancée contre les menaces.