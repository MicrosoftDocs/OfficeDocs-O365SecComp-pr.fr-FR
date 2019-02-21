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
description: La protection anti-hameçonnage, avec une protection complète dans le cadre d'Office 365 protection avancée contre les menaces et de la protection de base dans Office 365 Exchange Online Protection, peut vous aider à protéger votre organisation contre les attaques de hameçonnage malveillant basées sur l'emprunt d'identité. et d'autres attaques par hameçonnage.
ms.openlocfilehash: 94aa4ca6339ee0e0c250e96b9d8a499c83e964f7
ms.sourcegitcommit: 32cb896aef370764ec6e8f8278ebaf16f1c5ff37
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30123965"
---
# <a name="set-up-office-365-atp-anti-phishing-and-anti-phishing-policies"></a>Configurer des stratégies anti-hameçonnage et anti-hameçonnage Office 365 ATP

La [protection anti-hameçonnage ATP](atp-anti-phishing.md), partie de la [protection avancée contre les menaces d'Office 365](office-365-atp.md), peut vous aider à protéger votre organisation contre les attaques par hameçonnage malveillantes et les attaques par hameçonnage. Si vous êtes un administrateur Office 365 Enterprise global ou un administrateur de sécurité, vous pouvez configurer des stratégies anti-hameçonnage ATP. 

Les attaques par hameçonnage se composent de différentes formes, des attaques basées sur des produits, à un Spear Phishing ou à une baleine ciblée. Avec la complexité croissante, il est difficile d'identifier certaines de ces attaques sophistiquées. Heureusement, Office 365 Advanced Threat Protection peut vous aider. Vous pouvez configurer une stratégie anti-hameçonnage ATP pour vous assurer que votre organisation est protégée contre ces attaques.
  
> [!NOTE]
> L'anti-hameçonnage ATP est disponible uniquement dans la protection avancée contre les menaces (ATP). La protection avancée contre les menaces est incluse dans les abonnements, tels que [microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation a5, etc. Si votre organisation dispose d'un abonnement Office 365 qui n'inclut pas Office 365 ATP, vous pouvez acheter l'ATP en tant que module complémentaire. Pour plus d'informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). Assurez-vous que votre organisation utilise la dernière version d'Office 365 proPlus sur Windows pour tirer pleinement parti de la protection anti-hameçonnage ATP. 

Une stratégie anti-hameçonnage est également disponible pour Office 365 Exchange Online Protection, avec un ensemble limité de protection contre l'usurpation d'identité, destinée à la protection contre les attaques basées sur l'authentification et la déception.
  
Que faire:
  
1. Passez en revue les conditions préalables.
    
2. En savoir plus sur les options de stratégie anti-hameçonnage et de protection contre le hameçonnage.
    
3. ConFigurez une stratégie anti-hameçonnage ou une stratégie anti-hameçonnage ATP.
    
## <a name="review-the-prerequisites"></a>Vérifier les conditions préalables

- Pour définir (ou modifier) des stratégies ATP, vous devez disposer d'un rôle approprié. Certains exemples sont décrits dans le tableau suivant: <br>

    |Rôle  |WHERE/How Assigned  |
    |---------|---------|
    |Administrateur général Office 365 |La personne qui s'inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
    |Administrateur de sécurité |Centre d'administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()|
    |Gestion de l'organisation Exchange Online |Centre d'administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>ou <br>  Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
    Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations &amp; dans le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).

- Vous allez probablement configurer plusieurs stratégies anti-hameçonnage pour votre organisation. Office 365 applique ces stratégies dans l'ordre dans lequel elles sont indiquées sur la **page anti-hameçonnage** et les pages **anti-hameçonnage ATP** dans le centre de &amp; sécurité conformité. Une fois que vous avez examiné vos [options de stratégie](#learn-about-atp-anti-phishing-policy-options), prenez le temps de déterminer le nombre de stratégies requises et la priorité de chacune d'elles. 
    
- Prévoyez de consacrer environ 5-15 minutes à la mise en place de votre première stratégie anti-hameçonnage.
    
- Attendez jusqu'à 30 minutes que votre stratégie nouvelle ou mise à jour se propage à tous les centres de mises à jour Office 365.
    
## <a name="set-up-an-anti-phishing-or-atp-anti-phishing-policy"></a>Configurer une stratégie anti-hameçonnage (anti-hameçonnage) ou de protection avancée contre les menaces

Chaque organisation dans Office 365 a une stratégie anti-hameçonnage par défaut qui s'applique à tous les utilisateurs. Vous pouvez créer plusieurs stratégies anti-hameçonnage personnalisées que vous pouvez étendre à des utilisateurs, des groupes ou des domaines spécifiques au sein de votre organisation. Les stratégies personnalisées que vous créez ont priorité sur la stratégie par défaut. Vous pouvez ajouter, modifier et supprimer des stratégies de détection d'hameçonnage dans le centre de &amp; sécurité conformité d'Office 365.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire. 
    
2. Dans le centre de sécurité &amp; conformité d'Office 365, dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez **stratégie**.
    
3. Sur la page **stratégie** , choisissez **** anti-hameçonnage ou **protection contre le hameçonnage**.
    
4. Sur la **** page anti-hameçonnage ou **protection contre le hameçonnage** , effectuez l'une des opérations suivantes: 
    
    - Pour ajouter une nouvelle stratégie, sélectionnez **+ créer**.
    - Pour modifier une stratégie existante, sélectionnez le nom de la stratégie dans la liste affichée sur la page **anti-hameçonnage** . (Vous pouvez également choisir la **stratégie par défaut** au-dessus de la liste). Sur la page qui s'affiche, sélectionnez **modifier la stratégie**.  
    
5. Spécifiez le nom, la description et les paramètres de votre stratégie. Pour plus d'informations, consultez la rubrique [en savoir plus sur les options de stratégie anti-hameçonnage ATP](#learn-about-atp-anti-phishing-policy-options) . 
    
6. Une fois que vous avez vérifié vos paramètres, choisissez **créer cette stratégie** (ou **Enregistrer**). 
    
## <a name="learn-about-atp-anti-phishing-policy-options"></a>En savoir plus sur les options de stratégie anti-hameçonnage ATP

Lors de la configuration ou de la modification de vos stratégies de protection contre le hameçonnage ATP, vous pouvez choisir parmi plusieurs options offrant la protection la plus sophistiquée et complète, comme décrit dans le tableau suivant:
  
|**Ce paramètre**|**Effectue cette action**|**À utiliser lorsque vous souhaitez:**|
|:-----|:-----|:-----|
|**Ajouter des utilisateurs à protéger** <br/> |Définit les adresses de messagerie qui seront protégées par la stratégie. Vous pouvez ajouter jusqu'à 60 adresses internes et externes que vous souhaitez protéger contre l'emprunt d'identité.  <br/> |Lorsque vous souhaitez vous assurer que les messages provenant de l'extérieur de votre organisation ne sont pas emprunts d'identité de l'un des utilisateurs sur la liste des utilisateurs que vous protégez. Les utilisateurs que vous souhaiterez peut-être protéger sont des cadres de haut niveau, des propriétaires d'entreprise, des membres de conseil externe, etc.<br/> Cette liste d'utilisateurs protégés est différente de la liste des personnes auxquelles la stratégie s'applique, ou non pour laquelle la stratégie est appliquée. Vous définissez la liste s'applique à dans la section **appliqué à** des options de stratégie.<br/> Par exemple, si vous ajoutez `Mary Smith <marys@contoso.com>` en tant qu'utilisateur à protéger, appliquez la stratégie au groupe «tous les utilisateurs». Cela permet de s'assurer qu'un message qui semble emprunter l'identité «Mary Smith» envoyé à un utilisateur dans le groupe «tous les utilisateurs» serait traité par la stratégie.<br/> |
|**Ajouter des domaines à protéger** <br/> |Vous permet de choisir les domaines que vous souhaitez protéger de l'emprunt d'identité. Vous pouvez spécifier que la stratégie inclut tous vos domaines personnalisés, une liste de domaines séparés par des virgules ou une combinaison des deux. Si vous choisissez d' **inclure automatiquement les domaines dont je suis propriétaire**, et que vous ajoutez ultérieurement un domaine à votre organisation Office 365, cette stratégie de blocage du hameçonnage sera mise en place pour le nouveau domaine.<br/> |Chaque fois que vous souhaitez vous assurer que les messages provenant de l'extérieur de votre organisation ne sont pas emprunts d'identité de l'un des domaines définis dans votre liste de domaines vérifiés ou ceux d'un domaine partenaire.  <br/> |
|**Choisir les actions** <br/> |Sélectionnez l'action à effectuer lorsque Office 365 détecte une tentative d'emprunt d'identité par rapport aux utilisateurs et domaines que vous avez ajoutés à la stratégie. Vous pouvez choisir différentes actions pour les utilisateurs et les domaines dans la même stratégie anti-hameçonnage. Ces actions s'appliquent à tout courrier électronique entrant identifié par Office 365 comme empruntant l'identité d'un compte d'utilisateur ou d'un domaine qui est protégé par cette stratégie anti-hameçonnage.<br/> **Mettre en quarantaine le message** Le courrier électronique sera envoyé à la mise en quarantaine Office 365. Lorsque vous choisissez cette option, le courrier électronique n'est pas envoyé au destinataire d'origine.<br/> **Rediriger le message vers une autre adresse de messagerie** Le courrier électronique est envoyé à l'adresse de messagerie que vous spécifiez. Vous pouvez spécifier plusieurs adresses de messagerie. Lorsque vous choisissez cette option, le courrier électronique n'est pas envoyé au destinataire d'origine.<br/> **Déplacer le message vers le dossier** courrier indésirable des destinataires Le courrier électronique sera envoyé vers le dossier courrier inDésirable des destinataires. Lorsque vous choisissez cette option, le courrier électronique est toujours envoyé au destinataire d'origine, mais il n'est pas placé dans la boîte de réception du destinataire.<br/> **Remise du message et ajout d'autres adresses à la ligne CCI** Le courrier électronique sera remis au destinataire d'origine. En outre, les utilisateurs que vous identifiez sont ajoutés à la ligne CCI du message avant qu'il ne soit remis. Lorsque vous choisissez cette option, le courrier électronique est toujours envoyé à la boîte de réception du destinataire d'origine.<br/> **Ne pas appliquer d'action** Le courrier électronique sera remis dans la boîte de réception du destinataire d'origine. Aucune autre action n'est effectuée sur le message électronique.<br/> **Activer les conseils de protection contre le hameçonnage** Active les conseils de sécurité anti-hameçonnage dans les messages électroniques.  <br/> |Lorsque vous souhaitez effectuer une action sur les messages qu'Office 365 a déterminés comme emprunt d'identité d'un utilisateur ou d'un domaine, comme défini dans la stratégie.  <br/> |
|**Activer l'intelligence des boîtes aux lettres** <br/> |Active ou désactive l'intelligence de boîte aux lettres pour cette stratégie. Vous pouvez activer l'intelligence des boîtes aux lettres uniquement pour les comptes en nuage, c'est-à-dire les comptes dont la boîte aux lettres est hébergée entièrement dans Office 365.  <br/> |Lorsque vous souhaitez améliorer les résultats de l'emprunt d'identité pour les utilisateurs en fonction du mappage individuel de chaque utilisateur. La fonctionnalité intelligence des boîtes aux lettres est basée sur les personnes à partir desquelles vous envoyez et recevoir des messages. Cette intelligence permet à Office 365 de personnaliser la stratégie d'emprunt d'identité à un niveau utilisateur afin de mieux gérer les résultats faux positifs.  <br/> |
|**Ajouter des expéditeurs et des domaines approuvés** <br/> |Définit les adresses de messagerie et les domaines qui ne seront pas considérés comme des emprunts d'identité par cette stratégie. Les messages provenant des adresses de messagerie de l'expéditeur et des domaines que vous ajoutez en tant qu'expéditeurs approuvés et domaines ne seront jamais classés comme une attaque basée sur l'emprunt d'identité. Par conséquent, les actions et les paramètres de cette stratégie ne seront pas appliqués aux messages provenant de ces expéditeurs et domaines.  <br/> |Lorsque les utilisateurs interagissent avec des domaines ou des utilisateurs qui déclenchent l'emprunt d'identité mais sont considérés comme sûrs. Par exemple, si un partenaire possède le même nom d'affichage ou nom de domaine que celui d'un utilisateur défini dans la liste.  <br/> |
|**Appliqué à** <br/> |Définit les destinataires dont les messages électroniques entrants seront soumis aux règles de la stratégie. Vous pouvez créer des conditions et des exceptions pour les destinataires associés à la stratégie.  <br/> Par exemple, vous pouvez créer une stratégie globale pour votre organisation en appliquant la règle à tous les destinataires de votre domaine.  <br/> Vous pouvez également créer des règles d'exception, telles qu'une règle qui n'analyse pas les messages électroniques d'un groupe spécifique de destinataires.  <br/> |Chaque stratégie doit être associée à un ensemble d'utilisateurs, par exemple, les utilisateurs d'un groupe ou d'un domaine particulier.  <br/> |
|**Seuils de hameçonnage avancés** <br/> |Définit le niveau de gestion des messages d'hameçonnage.  <br/> **Standard** Le courrier électronique suspect d'être un hameçonnage est géré de manière standard.  <br/> **Agressif** Les E-mails suspectés d'être hameçons avec un degré élevé ou très élevé de confiance sont gérés par le système de la même manière.  <br/> **Plus agressive** Les E-mails suspectés d'être hameçons avec un degré de confiance moyen, élevé ou très élevé sont gérés par le système de la même manière.  <br/> **La plus agressive** Les E-mails suspectés d'être hameçons avec un niveau de confiance faible, moyen, élevé ou très élevé sont gérés par le système de la même manière.  <br/> |Si vous souhaitez être plus agressif dans le traitement des messages potentiellement hameçons dans Office 365. Par exemple, les messages dont la probabilité d'hameçonnage est très élevée sont les actions les plus agressives, tandis que les messages avec une faible probabilité ont des actions moins agressives. Ce paramètre a également un impact sur les autres parties du système de filtrage qui combinent les signaux. Le risque de transfert de messages de qualité augmente à mesure que le niveau de paramètres augmente.  <br/>|
   
## <a name="learn-about-anti-phishing-policy-options"></a>En savoir plus sur les options de stratégie anti-hameçonnage 

Lors de la configuration ou de la modification de votre anti-hameçonnage, vous pouvez choisir parmi plusieurs options, comme décrit dans le tableau suivant: 

|**Ce paramètre**|**Effectue cette action**|**À utiliser lorsque vous souhaitez:**|
|:-----|:-----|:-----|
|**Appliqué à** <br/> |Définit les destinataires dont les messages électroniques entrants seront soumis aux règles de la stratégie. Vous pouvez créer des conditions et des exceptions pour les destinataires associés à la stratégie.  <br/> Par exemple, vous pouvez créer une stratégie globale pour votre organisation en appliquant la règle à tous les destinataires de votre domaine.  <br/> Vous pouvez également créer des règles d'exception, telles qu'une règle qui n'analyse pas les messages électroniques d'un groupe spécifique de destinataires.  <br/> |Chaque stratégie doit être associée à un ensemble d'utilisateurs, par exemple, les utilisateurs d'un groupe ou d'un domaine particulier.  <br/> | 
|**Choisir les actions** <br/> |Sélectionnez l'action à effectuer lorsque Office 365 détecte une tentative d'usurpation d'identité intra-organisation ou d'organisation externe auprès de vos utilisateurs. Ces actions s'appliquent à tous les messages électroniques entrants identifiés par Office 365 comme tentatives d'usurpation d'identité pour les utilisateurs qui sont protégés par cette stratégie anti-hameçonnage.<br/> **Mettre en quarantaine le message** Le courrier électronique sera envoyé à la mise en quarantaine Office 365. Lorsque vous choisissez cette option, le courrier électronique n'est pas envoyé au destinataire d'origine.<br/> **Déplacer le message vers le dossier** courrier indésirable des destinataires Le courrier électronique sera envoyé vers le dossier courrier inDésirable des destinataires. Lorsque vous choisissez cette option, le courrier électronique est toujours envoyé au destinataire d'origine, mais il n'est pas placé dans la boîte de réception du destinataire.<br/> **Ne pas appliquer d'action** Le courrier électronique sera remis dans la boîte de réception du destinataire d'origine. Aucune autre action n'est effectuée sur le message électronique.<br/> |Lorsque vous souhaitez effectuer une action sur les messages qu'Office 365 a déterminé comme étant une tentative d'usurpation de domaines internes ou externes, comme défini dans la stratégie.  <br/>|

Une fois que votre organisation a configuré des stratégies anti-hameçonnage ou des stratégies anti-hameçonnage ATP, vous pouvez voir comment le service fonctionne en [affichant des rapports pour une protection avancée contre les menaces](view-reports-for-atp.md).
  
## <a name="example-anti-phishing-policy-to-protect-a-user-and-a-domain"></a>Exemple: stratégie anti-hameçonnage pour protéger un utilisateur et un domaine

Cet exemple définit une stratégie appelée «Domain and CEO» qui assure à la fois la protection des utilisateurs et des domaines à partir de l'emprunt d'identité, puis applique la stratégie à tous `contoso.com`les messages électroniques reçus par les utilisateurs au sein du domaine. L'administrateur de la sécurité a déterminé que la stratégie doit répondre aux exigences de l'entreprise suivantes:
  
- La stratégie doit assurer la protection du compte de messagerie du PDG et de l'ensemble du domaine.
    
- Les messages qui sont déterminés comme tentatives d'emprunt d'identité contre le compte d'utilisateur du PDG doivent être redirigés vers l'adresse de messagerie de l'administrateur de la sécurité.
    
- Les messages qui sont considérés comme des tentatives d'emprunt d'identité contre le domaine sont moins urgents et doivent être mis en quarantaine pour examen ultérieur.
    
L'administrateur de sécurité de contoso peut utiliser des valeurs similaires à celles-ci pour créer une stratégie anti-hameçonnage qui répond à ces besoins.
  
|||
|:-----|:-----|
|**Paramètre ou option** <br/> |**Exemple** <br/> |
|Nom  <br/> |Domaine et PDG  <br/> |
|Description  <br/> |Assurez-vous que le PDG et notre domaine ne sont pas empruntés.  <br/> |
|Ajouter des utilisateurs à protéger  <br/> |L'adresse de messagerie du PDG au minimum.  <br/> |
|Ajouter des domaines à protéger  <br/> |Le domaine de l'organisation incluant le Bureau du PDG.  <br/> |
|Choisir les actions  <br/> |Si un message électronique est envoyé par un utilisateur représenté: choisissez rediriger le **message vers une autre adresse de messagerie** , puis tapez l'adresse de messagerie de l'administrateur `securityadmin@contoso.com`de sécurité, par exemple.  <br/> Si le courrier électronique est envoyé par un domaine emprunté: choisissez **mettre en quarantaine le message**.  <br/> |
|Intelligence des boîtes aux lettres  <br/> |Par défaut, l'intelligence de boîte aux lettres est activée lorsque vous créez une nouvelle stratégie anti-hameçonnage. Laissez ce paramètre **activé** pour obtenir les meilleurs résultats.<br/> |
|Ajouter des expéditeurs et des domaines approuvés  <br/> |Pour cet exemple, ne définissez aucune substitution.  <br/> |
|Appliqué à  <br/> |Sélectionnez **le domaine du destinataire**. Sous **l'un de ces éléments**, sélectionnez **choisir**. Sélectionnez **+ Ajouter**. Sélectionnez la case à cocher en regard du nom du domaine, par `contoso.com`exemple, dans la liste, puis sélectionnez **Ajouter**. Sélectionnez **Terminer**.<br/> |
   
## <a name="delete-an-anti-phishing-or-atp-anti-phishing-policy"></a>Supprimer une stratégie anti-hameçonnage ou anti-hameçonnage de protection avancée contre les menaces

Vous pouvez supprimer des stratégies personnalisées que vous avez créées à &amp; l'aide du centre de sécurité et de conformité. Vous ne pouvez pas supprimer la stratégie par défaut pour votre organisation. Nous vous recommandons d'utiliser &amp; le centre de sécurité conformité pour consulter ou modifier toutes vos stratégies ATP.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire. 
    
2. Dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez **stratégie**.
    
3. Sur la page **stratégie** , choisissez **** anti-hameçonnage ou **protection contre le hameçonnage**.
    
4. Sur la **** page anti-hameçonnage ou **protection contre le hameçonnage** , sélectionnez le nom de la stratégie dans la liste.

5. Sur la page qui s'affiche, sélectionnez **Supprimer la stratégie**. Autorisez jusqu'à 30 minutes pour que vos modifications soient diffusées sur tous les centres de calcul Office 365.
    

## <a name="next-steps"></a>Étapes suivantes

Une fois que vos stratégies anti-hameçonnage sont en place, vous pouvez voir le fonctionnement de vos fonctionnalités de protection contre les menaces pour votre organisation en affichant des rapports. Pour en savoir plus, consultez les ressources suivantes:
- [Afficher des rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md) ou [afficher des rapports de sécurité de messagerie](view-email-security-reports.md)
- [Utiliser l'Explorateur (également appelé Explorateur de menaces)](use-explorer-in-security-and-compliance.md)

Restez au fait des nouvelles fonctionnalités disponibles dans la protection avancée contre les menaces. consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) et découvrez les [nouvelles fonctionnalités qui sont ajoutées à](office-365-atp.md#new-features-in-office-365-atp)la protection avancée contre les menaces.
 