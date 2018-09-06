---
title: Gérer les messages mis en quarantaine et les fichiers en tant qu’administrateur dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
description: 'En tant qu’administrateur, vous pouvez afficher, version et signaler un faux positif mis en quarantaine dans Office 365. Vous pouvez définir des stratégies afin que le filtrage des messages Office 365 et l’envoie à mettre en quarantaine pour plusieurs raisons : car ils ont été identifiés comme du courrier indésirable, en bloc, l’hameçonnage, les logiciels malveillants ou car il correspondant à une règle de flux de messagerie. '
ms.openlocfilehash: be6384d8937e25aec55d82d8212c49d25b64b9a1
ms.sourcegitcommit: d85fc77cba3a17d5ddf215e2f506f61b499e0cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839098"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator-in-office-365"></a>Gérer les messages mis en quarantaine et les fichiers en tant qu’administrateur dans Office 365

En tant qu’administrateur, vous pouvez afficher, version et supprimer les messages mis en quarantaine et les messages mis en quarantaine rapport faux positifs dans Office 365. Vous pouvez également afficher, télécharger et supprimer les fichiers mis en quarantaine capturés par avance Threat Protection (DAV) pour SharePoint Online, OneDrive pour les entreprises et Teams Microsoft. Vous pouvez définir des stratégies afin que le filtrage des messages Office 365 et l’envoie à mettre en quarantaine pour plusieurs raisons : car ils ont été identifiés comme courrier indésirable, courrier en nombre, courrier hameçonnage, contenant des programmes malveillants, ou parce qu’il correspondant à une règle de flux de messagerie.
  
Par défaut, Office 365 envoie les messages de hameçonnage et les messages contenant des programmes malveillants directement en quarantaine. Autres messages filtrés sont envoyées au dossier de courrier indésirable des utilisateurs, sauf si vous définissez une stratégie pour les envoyer au contrôle.
  
Vous devez disposer des autorisations d’administrateur dans Office 365 pour travailler avec des messages mis en quarantaine qui ont été envoyés à d’autres utilisateurs et pour travailler avec les fichiers mis en quarantaine.
  
> [!IMPORTANT]
> Par défaut, le courrier indésirable, en bloc, logiciels malveillants, hameçonnage et les messages qui ont été mis en quarantaine car ils correspondant à une règle de flux de messagerie sont conservés dans la mise en quarantaine pendant 30 jours. Vous pouvez personnaliser l’heure de mise en quarantaine dans les paramètres de blocage du courrier indésirable de la sécurité &amp; centre de conformité. Lorsque Office 365 supprime un message de mise en quarantaine, vous ne pouvez pas le récupérer. Si vous le souhaitez, vous pouvez modifier la période de rétention des messages mis en quarantaine dans vos stratégies de filtrage de blocage du courrier indésirable. Pour plus d’informations, voir [définition de la période de rétention de mise en quarantaine](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) dans cet article. 
  
## <a name="view-your-organizations-quarantined-messages"></a>Afficher les messages mis en quarantaine de votre organisation

1. À l’aide d’un compte professionnel ou de l’école ayant des privilèges d’administrateur global dans votre organisation Office 365, connectez-vous à Office 365 et [accédez au centre de conformité et de sécurité](go-to-the-securitycompliance-center.md).
    
2. Dans la liste de gauche, développez **Threat Management**, sélectionnez **révision**, puis **mise en quarantaine**.
    
    > [!TIP]
    > Pour accéder directement à la page **mise en quarantaine** dans la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
    Par défaut, la sécurité &amp; centre de conformité affiche tous les messages électroniques qui ont été mis en quarantaine en tant que courrier indésirable. Les messages sont triés de la plus récente à la plus ancienne en fonction de la **Date** du message a été reçu. **L’expéditeur**, **l’objet**et la date d’expiration (sous **date d’expiration** ) sont également affichées pour chaque message. Vous pouvez trier sur un champ en cliquant sur l’en-tête de colonne correspondant ; Cliquez sur un en-tête de colonne une deuxième fois afin d’inverser l’ordre de tri. 
    
3. Vous pouvez afficher une liste de tous les messages mis en quarantaine, ou vous pouvez réduire le jeu de résultats par le filtrage. Vous pouvez uniquement effectuer des opérations en bloc sur jusqu'à 100 éléments, afin que le filtrage permet également de réduire votre jeu de résultats si vous disposez de plusieurs qui. Vous pouvez rapidement filtrer les messages pour une raison unique en choisissant une option dans le filtre en haut de la page. Les options sont les suivantes :
    
  - Messages identifiés comme courrier indésirable
    
  - Messages mis en quarantaine parce qu’il correspondait à une stratégie définie par une règle de flux de messagerie (également appelée une règle de transport)
    
  - Courrier électronique identifié comme courrier indésirable
    
  - Courrier électronique identifié comme courrier hameçonnage
    
  - Messages mis en quarantaine parce qu’il contient des programmes malveillants
    
En outre, en tant qu’administrateur, vous pouvez choisir filtrer tous les messages pour votre organisation ou uniquement les messages envoyés. Mettre fin à des utilisateurs peut uniquement afficher et travailler avec les messages envoyés.
  
Vous pouvez également filtrer les résultats pour rechercher des messages spécifiques. Pour obtenir des conseils, voir [pour filtrer les résultats et de rechercher des fichiers et des messages mis en quarantaine](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) dans cet article. 
  
Après avoir trouvé un message en quarantaine spécifique, cliquez sur le message pour afficher les détails et effectuer des actions, comme libérer le message à la boîte de réception d’une personne.
  
## <a name="view-your-organizations-quarantined-files"></a>Afficher les fichiers mis en quarantaine de votre organisation

1. À l’aide d’un compte professionnel ou de l’école ayant des privilèges d’administrateur global dans votre organisation Office 365, connectez-vous à Office 365 et [accédez au centre de conformité et de sécurité](go-to-the-securitycompliance-center.md).
    
2. Sur la gauche, développez **Threat Management**, sélectionnez **révision**, puis **mise en quarantaine**. 
    
    > [!TIP]
    > Pour accéder directement à la page **mise en quarantaine** dans la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
3. Par défaut, la page affiche les messages électroniques mis en quarantaine. Pour afficher les fichiers mis en quarantaine, définissez les filtres en haut de la page pour afficher les **fichiers**mis en quarantaine en raison de **programmes malveillants**. Vous devez disposer des autorisations d’administrateur dans Office 365 pour travailler avec des fichiers mis en quarantaine. 
    
4. Les fichiers sont triés de la plus récente à la plus ancienne en fonction de la date, que le fichier a été mis en quarantaine. L' **utilisateur** qui a modifié le fichier, le **Service** à laquelle le fichier a été validé, le **Nom de fichier**, **l’emplacement**, la **Taille du fichier**, et la date d’expiration ( **expiration**) sont également répertoriés pour chaque fichier. Vous pouvez trier sur un champ en cliquant sur un en-tête ; Cliquez sur un en-tête de colonne une deuxième fois afin d’inverser l’ordre de tri.
    
Vous pouvez afficher une liste de tous les fichiers mis en quarantaine, ou vous pouvez rechercher des fichiers spécifiques par le filtrage. À l’instar des messages, vous pouvez uniquement effectuer des opérations sur jusqu'à 100 éléments en bloc. Actuellement, la sécurité &amp; centre de conformité permet d’afficher et gérer les fichiers qui se trouvent dans la mise en quarantaine, car ils ont été identifiés comme contenant des programmes malveillants. Pour obtenir des conseils, voir [pour filtrer les résultats et de rechercher des fichiers et des messages mis en quarantaine](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) dans cet article. 
  
## <a name="to-filter-results-and-find-quarantined-messages-and-files"></a>Pour filtrer les résultats et de rechercher des fichiers et des messages mis en quarantaine
<a name="BKMK_AdvSearch"> </a>

En fonction de vos paramètres, il peut être un grand nombre de messages mis en quarantaine et les fichiers. Pour rechercher un message spécifique ou un fichier ou un ensemble de fichiers ou de messages, vous pouvez filtrer les éléments mis en quarantaine en fonction de diverses informations supplémentaires.
  
1. Dans la page **mise en quarantaine** , assurez-vous que la ligne supérieure de filtres est définie pour afficher des messages ou des fichiers selon le cas : 
    
  - Pour rechercher des fichiers, définissez les filtres pour afficher les **fichiers** mis en quarantaine en raison de **programmes malveillants**.
    
    Pour les fichiers mis en quarantaine, la page affiche mis en quarantaine tous les fichiers, pas seulement votre propre, quel que soit vous indiquez informatique à afficher.
    
  - Pour rechercher des messages mis en quarantaine, définir des filtres pour afficher **tout** ou **uniquement mes** **e-mail**. Pour le dernier filtre choisir le type de message en quarantaine que vous recherchez. Vous pouvez rechercher des messages mis en quarantaine qui ont été identifiés comme **courrier indésirable**, les messages qui correspondent à un flux de messagerie ou **règle de transport**, courrier **en nombre** , messagerie **hameçonnage** ou des messages contenant des **programmes malveillants**.
    
2. Sous **trier les résultats par**, sélectionnez l’ou les filtres à utiliser pour rechercher dans les listes déroulantes. Les options varient en fonction de si vous recherchez des fichiers ou des messages. Des caractères génériques ne sont pas pris en charge dans les champs de recherche pour l’instant.
    
    Pour les fichiers et messages, vous pouvez choisir de filtrer par la date du message ou fichier a été mis en quarantaine. Vous pouvez spécifier la date ou une plage de dates, y compris l’heure. Vous pouvez également filtrer vos résultats de recherche à la date d’expiration sur lequel le fichier ou le message sera supprimé de la mise en quarantaine, ou vous pouvez utiliser une combinaison de filtres. Pour effectuer une recherche par date d’expiration, cliquez sur **filtre avancé**. Sous **date d’expiration**, vous pouvez sélectionner les messages seront supprimés de la mise en quarantaine dans les 24 heures ( **aujourd'hui**), dans les 48 heures ( **suivant 2 jours**), au sein de la semaine suivante ( **Next 7 jours**), ou vous pouvez sélectionner un intervalle de temps personnalisé.
    
    Pour les messages, vous disposez des options supplémentaires suivantes :
    
  - **ID de message**. Permet d’identifier un message spécifique lorsque vous connaissez l’ID de message. 
    
    Par exemple, si un message spécifique est envoyé par ou destiné à être, un utilisateur dans votre organisation, mais il n’a jamais atteint sa destination, vous pouvez rechercher pour le message à l’aide d’un suivi des messages (voir [exécuter un suivi des messages et afficher les résultats](https://go.microsoft.com/fwlink/?LinkId=799737)). Si vous découvrez que le message a été mis en quarantaine, peut-être parce qu’il correspondait à une règle de flux de messagerie ou a été identifié comme courrier indésirable, puis retrouver facilement ce message en quarantaine en spécifiant l’ID du message. Veillez à inclure la chaîne d’ID de message complet. Cela peut inclure des signes (\<\>), par exemple :
    
    \<79239079-D95A-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Adresse de messagerie de l’expéditeur**. Choisir de filtrer par une adresse de messagerie unique de l’expéditeur. 
    
  - **Adresse de messagerie destinataire**. Choisir de filtrer par une adresse de messagerie du destinataire unique. 
    
  - **Objet**. Entrez l’objet d’une adresse de messagerie à rechercher. Étant donné que la recherche par caractères génériques n’est pas pris en charge, vous devez utiliser l’ensemble du sujet du message dans l’ordre de la recherche pour renvoyer le message dans les résultats de. La recherche ne respecte pas la casse. 
    
## <a name="view-details-about-quarantined-messages-and-files"></a>Afficher les détails des messages mis en quarantaine et les fichiers
<a name="BKMK_ViewDetails"> </a>

Lorsque vous sélectionnez un élément affiché dans la liste mise en quarantaine, vous verrez un récapitulatif de ses propriétés dans le volet **d’informations** sur le côté droit de la sécurité &amp; centre de conformité. 
  
 **Plus d’informations affichées pour les messages mis en quarantaine**
  
- **ID de message**. Identificateur unique pour le message. 
    
- **Adresse de l’expéditeur**. Qui a envoyé le message. 
    
- **Reçu**. Date et heure de que réception du message. 
    
- **Objet**. Le texte de la ligne objet du message. 
    
- **Type**. Indique si un message a été identifié comme **courrier indésirable**, **en bloc**, **hameçonnage**, correspondait à une règle de flux de messagerie ( **règle de Transport**), ou a été identifié comme contenant des **programmes malveillants**.
    
- **Expire**. La date et l’heure lorsque le message sera automatiquement supprimé de la mise en quarantaine. 
    
- **Publié à**. Toutes les adresses de messagerie (le cas échéant) à laquelle le message a été envoyé. 
    
- **Pas encore publié à**. Toutes les adresses de messagerie (le cas échéant) à laquelle le message n'a pas encore été activée. 
    
 **Plus d’informations affichées pour les fichiers mis en quarantaine**
  
- **Nom de fichier** Le nom du fichier de mise en quarantaine. 
    
- **Chemin d’accès au site** URL qui définit l’emplacement du fichier dans Office 365. 
    
- **Détecté Date / heure** La date et l’heure que du fichier a été mis en quarantaine. 
    
- **Expire** La date lorsque le message sera supprimé de la mise en quarantaine. 
    
- **Détecté par** La méthode utilisée pour détecter les programmes malveillants dans le fichier. Il peut s’agir d’un DAV (protection contre les menaces avancées) ou Microsoft contre les programmes malveillants. 
    
- **Publié** Indique si le fichier a été publié. 
    
- **Nom de programmes malveillants** Famille et le nom du programme malveillant détecté dans le fichier. 
    
- **ID de document** Identificateur unique pour le document. 
    
- **Taille de fichier** La taille du fichier en Ko. 
    
- **Organisation** ID unique de votre organisation dans Office 365. 
    
- **Modifié par** Compte professionnel ou de l’école de l’utilisateur qui a modifié le fichier. 
    
- **Taille de fichier** La taille du fichier en Ko. 
    
- **Hachage SHA256** Le hachage du fichier. Cela permet de rechercher d’autres magasins de réputation vous avez ou étudier où le fichier peut être dans votre environnement. 
    
## <a name="managing-messages-and-files-in-quarantine"></a>Gestion des fichiers et les messages en quarantaine
<a name="BKMK_ManageQuarantinedItem"> </a>

Une fois que vous sélectionnez un message ou un groupe de messages que vous disposez de plusieurs options pour la gestion des messages en quarantaine.
  
- Ne rien faire. Si vous choisissez de ne rien faire, le message sera supprimé par Office 365 automatiquement à expiration. Par défaut, le courrier indésirable, en bloc, logiciels malveillants, hameçonnage et les messages mis en quarantaine parce qu’ils correspondant à une règle de flux de messagerie sont conservés dans la mise en quarantaine pendant 30 jours. Lorsque Office 365 supprime un message de mise en quarantaine, vous ne pouvez pas le récupérer. Si vous le souhaitez, vous pouvez modifier la période de rétention des messages mis en quarantaine en configurant le paramètre **conserver le courrier indésirable de (jours)** dans vos stratégies de blocage du courrier indésirable. Pour plus d’informations, voir [définition de la période de rétention de mise en quarantaine](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) dans cet article. 
    
- **En-tête du message** Cliquez sur ce lien pour afficher le texte d’en-tête de message. Pour analyser l’en-tête de la profondeur, copier le texte d’en-tête de message dans le Presse-papiers, puis cliquez sur **L’analyseur en-tête de Message de Microsoft** pour accéder à l’Analyseur de connectivité à distance (avec le bouton droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Office 365 pour effectuer cette tâche). Coller l’en-tête du message sur la page dans la section analyseur d’en-tête de Message, puis choisissez **analyser les en-têtes**.
    
- **Aperçu du message** Vous permet de voir brute ou versions HTML du texte du corps de message. Dans l’affichage HTML, les liens sont désactivés. 
    
- **Téléchargement des messages** ou **Télécharger le fichier**. Choisissez cette option pour télécharger une copie du message ou du fichier sur votre appareil local. Vous devrez confirmer que vous comprenez les risques liés au téléchargement des éléments à partir de la mise en quarantaine avant de vous serez autorisé à le faire. Les messages sont enregistrés au format .eml dans un dossier que vous spécifiez. Les fichiers mis en quarantaine sont enregistrés dans leur format d’origine.
    
- **Supprimer** Si vous le souhaitez, vous pouvez supprimer immédiatement un élément mis en quarantaine (ou un ensemble d’éléments) au lieu d’attendre la date d’expiration par Office 365. Pour supprimer un message ou un fichier, dans la liste mise en quarantaine, sélectionnez l’élément, puis choisissez **Supprimer**. Pour supprimer plusieurs éléments à la fois, activez la case à cocher à gauche des éléments dans la liste mise en quarantaine, puis, dans la page **actions en bloc** qui s’affiche, cliquez sur **Supprimer les messages sélectionnés** ou **Supprimer des fichiers sélectionnés**.
    
- **Version** Libération d’un élément mis en quarantaine (ou un ensemble d’éléments) et signaler à Microsoft les éléments comme faussement mis en quarantaine (faux positifs). 
    
    Pour libérer et signaler un message unique ou un fichier, dans la liste mise en quarantaine, sélectionnez l’élément, choisissez la **version de fichier** ou la dernière **version du message**. Dans la page suivante, vérifiez que **les messages de rapport à Microsoft pour analyse** ou les **fichiers de rapport à Microsoft pour analyse** est sélectionné. 
    
    Pour libérer plusieurs éléments à la fois, activez la case à cocher à gauche des éléments dans la liste mise en quarantaine, puis, dans la page **actions en bloc** qui s’affiche, sélectionnez **version des fichiers** ou **Débloquer les messages**. Dans la page suivante, vérifiez que **les messages de rapport à Microsoft pour analyse** ou les **fichiers de rapport à Microsoft pour analyse** est sélectionné. 
    
Lorsque vous êtes libération des messages, prenez en compte les éléments suivants :
  
- Lorsque vous exécutez une version en bloc de plusieurs messages à la fois, les messages sont libérées à tous les destinataires identifiés à l’origine. Si vous souhaitez débloquer les messages uniquement à des destinataires spécifiques uniquement, vous devez libérer les messages un à la fois et identifier les destinataires individuellement.
    
- Un message ne peut pas être libéré plusieurs fois au même destinataire.
    
- Lorsque vous êtes publie un message à plusieurs destinataires, seuls les destinataires qui n’ont pas déjà reçu le message seront affiche dans la liste des destinataires potentiels.
    
- Lorsque vous choisissez de signaler les faux positifs, si l’ou les messages que vous relâchiez ont été mis en quarantaine en tant que courrier indésirable, en bloc, l’hameçonnage, ou comme contenant des programmes malveillants, le message sera également communiquée à l’équipe d’analyse de courrier indésirable Microsoft. L’équipe évaluer et analyser le message et, en fonction des résultats de l’analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustés pour autoriser le message.
    
## <a name="setting-the-quarantine-retention-period"></a>Définition de la période de rétention de mise en quarantaine
<a name="BKMK_ModQuarantineTime"> </a>

Vous pouvez configurer la durée messages et fichiers restent en quarantaine avant qu’ils n’expirent. Par défaut, les éléments mis en quarantaine sont conservés pendant 30 jours. Vous configurez ce paramètre pour chaque stratégie que vous créez. Vous pouvez également modifier la valeur de la stratégie par défaut comme décrit dans cet article. 
  
### <a name="to-modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security-and-compliance-center"></a>Pour modifier la période de rétention de mise en quarantaine pour la stratégie de filtrage du courrier indésirable par défaut dans le centre de conformité et de sécurité

1. À l’aide d’un compte professionnel ou de l’école ayant des privilèges d’administrateur global dans votre organisation Office 365, connectez-vous à Office 365 et [accédez au centre de conformité et de sécurité](go-to-the-securitycompliance-center.md).
    
2. Sur la gauche, développez **Threat Management**, sélectionnez **stratégie**, puis **blocage du courrier indésirable**. 
    
    > [!TIP]
    > Pour accéder directement à la page **blocage du courrier indésirable** dans la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)
  
3. Sélectionnez **personnalisé** pour afficher l’onglet **paramètres personnalisés** . 
    
4. Développez la ligne de la **stratégie de filtrage du courrier indésirable par défaut (toujours activé)** . 
    
5. Choisissez **Modifier la stratégie**. Les paramètres de la stratégie de filtrage du courrier indésirable par défaut s’affichent dans une nouvelle page.
    
6. Développez **le courrier indésirable et en bloc des actions**.
    
7. Sous **mise en quarantaine**, dans la zone de texte **conserver le courrier indésirable de (jours)** , entrez la durée pendant laquelle que vous souhaitez Office 365 pour conserver les messages et les fichiers de mise en quarantaine. La valeur par défaut est de 30 jours. C’est également la valeur maximale. 
    
8. Sélectionnez **Enregistrer**.
    

