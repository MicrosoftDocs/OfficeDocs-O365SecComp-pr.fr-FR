---
title: Configurer des stratégies de surveillance pour votre organisation
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Configurer une vérification de surveillance des stratégies pour capturer les communications des employés pour la révision.
ms.openlocfilehash: a919d65f5c0967a44ac12b7e02d477dac2113704
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528779"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Configurer des stratégies de surveillance pour votre organisation

Utiliser des stratégies de surveillance pour capturer les communications des employés pour l’examen des réviseurs internes ou externes.
  
> [!NOTE]
> À l’aide de stratégies de surveillance requiert un abonnement à Office 365 E5 pour votre organisation. Si vous n’avez qu’un plan et essayer de surveillance, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Suivez ces étapes pour configurer et utiliser le contrôle de votre organisation Office 365 : 
  
- [Configurer des groupes de surveillance](configure-supervision-policies.md#exampledist)
    
    Avant de commencer à l’aide de surveillance, déterminer qui sera leurs communications révisé et qui effectue les révisions. Si vous souhaitez prendre en main quelques aux utilisateurs de voir le fonctionne de surveillance, vous pouvez ignorer la configuration de groupes pour l’instant.
    
- [Rendre le contrôle disponible dans votre organisation](configure-supervision-policies.md#SRavailable)
    
    Ajoutez-vous au groupe de rôles de supervision afin que vous pouvez définir des stratégies. Toute personne ce rôle a été attribué permettre accéder à la page de **surveillance** sous **La gouvernance des données** de la sécurité &amp; centre de conformité. 
    
- [Définir une stratégie de surveillance](configure-supervision-policies.md#setupsuper)
    
    Vous allez créer des stratégies de surveillance de la sécurité &amp; centre de conformité. Ces stratégies définissent les communications sont sujettes à révision dans votre organisation et indique qui doit effectuer des analyses. Communications incluent la messagerie ainsi que les communications de plateforme 3 rd tiers (tels que Facebook, Twitter, etc.)
    
- [Utiliser Outlook web app pour passer en revue les communications identifiées par une stratégie de surveillance](configure-supervision-policies.md#UseOutlook)
    
    Le complément de contrôle donne relecteurs accès à la fonctionnalité de surveillance dans Outlook web app afin de pouvoir évaluer et classer chaque élément. Prise en charge pour la version de bureau d’Outlook seront prochainement disponibles.
    
- **Exécuter le rapport de surveillance**
    
    Utilisez les rapports de surveillance pour afficher l’activité de révision au niveau de la stratégie et de réviseur. Pour chaque stratégie, vous pouvez également afficher les statistiques live sur l’état actuel de l’activité de révision. Pour plus d’informations, voir [les rapports de surveillance](supervision-reports.md).
    
## <a name="set-up-groups-for-supervision"></a>Configurer des groupes de surveillance
<a name="exampledist"> </a>

 Lorsque vous créez une stratégie de surveillance, vous devez déterminer qui auront leurs communications révisées et qui effectue les révisions. Dans la stratégie, vous allez utiliser des adresses de messagerie pour identifier des utilisateurs individuels ou des groupes de personnes. Pour simplifier votre installation, créez des personnes disposant de leurs communications révisée et les groupes pour les personnes qui validera les communications. Si vous utilisez des groupes, vous devrez peut-être plusieurs — par exemple, si vous souhaitez surveiller les communications entre les deux groupes distincts de personnes, ou si vous souhaitez spécifier un groupe qui n’est pas sur le point d’être surveillés. Pour plus d’informations sur cette procédure, voir [groupes de distribution exemple](configure-supervision-policies.md#GroupExample) . 
  
Pour contrôler les communications entre ou au sein de groupes de votre organisation, configurer des groupes de distribution dans le centre d’administration Exchange (accédez à **destinataires** \> **groupes**). Pour plus d’informations sur la configuration de groupes de distribution, voir [Gérer les groupes de distribution](http://go.microsoft.com/fwlink/?LinkId=613635)
  
> [!NOTE]
> Vous pouvez également utiliser des groupes de distribution dynamique ou de groupes de sécurité de surveillance si vous préférez. Pour vous aider à décider si ces adaptées à votre organisation a besoin, voir [Gérer les groupes de sécurité à extension messagerie](http://go.microsoft.com/fwlink/?LinkId=627033)et [Gérer les groupes de distribution dynamique](http://go.microsoft.com/fwlink/?LinkId=627058). 
  
### <a name="example-distribution-groups"></a>Exemple de groupes de distribution
<a name="GroupExample"> </a>

Cet exemple inclut un groupe de distribution qui a été configuré pour une organisation financière appelée Contoso financières International. 
  
Chez Contoso Financial International, un échantillonnage des communications entre les courtiers aux États-Unis doit être effectué. Toutefois, les responsables de la mise en conformité au sein de ce groupe ne doivent pas être surveillés. Dans cet exemple, nous pouvons créer les groupes suivants :
  
|**Configuration de ce groupe de distribution**|**Adresse de groupe (alias)**|**Description**|
|:-----|:-----|:-----|
|Tous les courtiers des États-Unis  <br/> |US_Brokers@contoso.com  <br/> |Ce groupe contient les adresses de messagerie de tous les courtiers basés aux États-Unis qui travaillent pour Contoso.  <br/> |
|Tous les responsables de la mise en conformité des États-Unis  <br/> |US_Compliance@contoso.com  <br/> |Ce groupe comprend les adresses de messagerie pour tous les responsables de conformité basée aux États-Unis qui travaillent pour Contoso. Ce groupe étant un sous-ensemble de tous les agents basée aux États-Unis, vous pouvez utiliser cet alias pour exemptés de conformité d’une stratégie de surveillance.  <br/> |
   
La section [configurer une stratégie de surveillance](configure-supervision-policies.md#setupsuper) décrit comment vous pouvez utiliser ces groupes lorsque vous configurez la stratégie. 
  
## <a name="make-supervision-available-in-your-organization"></a>Rendre le contrôle disponible dans votre organisation
<a name="SRavailable"> </a>

Pour rendre **surveillance** disponible comme option de menu dans la sécurité &amp; centre de conformité, vous devez posséder le rôle d’administrateur de passer en revue les surveillance. 
  
Pour ce faire, vous pouvez ajouter vous-même en tant que membre du groupe de rôles de supervision, ou vous pouvez créer un nouveau groupe de rôles.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Ajouter des membres au groupe de rôles de supervision

1. Se connecter à [https://protection.office.com](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365. 
    
2. Dans la sécurité &amp; centre de conformité, accédez à **autorisations**.
    
3. Sélectionnez le groupe de rôles **De supervision** , puis cliquez sur l’icône Modifier. 
    
4. Dans la section **membres** , ajoutez les personnes que vous souhaitez gérer la surveillance pour votre organisation. 
    
### <a name="create-a-new-role-group"></a>Créer un nouveau groupe de rôles

1. Se connecter à [https://protection.office.com](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365. 
    
2. Dans la sécurité &amp; centre de conformité, accédez à **autorisations** , puis cliquez sur Ajouter ( **+**).
    
3. Dans la section **rôles** , cliquez sur Ajouter ( **+**) et faites défiler jusqu'à la **Surveillance administrateur de révision**. Ajoutez ce rôle au groupe de rôles.
    
4. Dans la section **membres** , ajoutez les personnes que vous souhaitez gérer la surveillance pour votre organisation. 
    
Pour plus d’informations sur les groupes de rôles et autorisations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité ](permissions-in-the-security-and-compliance-center.md).
  
## <a name="set-up-a-supervision-policy"></a>Définir une stratégie de surveillance
<a name="setupsuper"> </a>

> [!IMPORTANT]
> Avant de créer une stratégie de surveillance, vous devez d’abord supprimer toutes les stratégies de supervision existant. 
  
1. Se connecter à [https://protection.office.com](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365. 
    
2. Dans la sécurité &amp; centre de conformité, accédez à cliquer sur **la gouvernance des données** \> **surveillance**.
    
    > [!NOTE]
    > La version précédente de la fonctionnalité peut afficher dans le volet de navigation gauche en tant que **révision contrôle (le retrait bientôt)**. Cette version sera bientôt désapprouvée et supprimée. La nouvelle version appelée **surveillance** prendra sa place. 
  
3. Cliquez sur **créer** , puis suivez l’Assistant pour configurer les pages suivantes de la stratégie. 
    
### <a name="policy-name-and-description"></a>Description et nom de la stratégie

Entrez un nom et une description pour votre stratégie. À titre d’exemple, nous allons nommez la stratégie Contoso nous courtiers.
  
### <a name="choose-users-to-supervise"></a>Choisir les utilisateurs à contrôler

- Dans la zone **Supervise ces utilisateurs ou groupes** , sélectionnez les utilisateurs ou groupes dont les communications de votre choix pour le contrôle. Utiliser pour Contoso nous courtiers notre exemple, nous allons sélectionner le groupe US_Brokers@Contoso.com ici. 
    
- Si vous avez choisi un groupe pour le contrôle, vous pouvez utiliser la zone **exclure ces utilisateurs** pour choisir les membres du groupe qui sont exemptés de surveillance. À l’aide de l’exemple, nous allons exclure le groupe US_Compliance@Contoso.com ici. 
    
### <a name="choose-communications-to-review"></a>Choisissez communications pour passer en revue
<a name="CommsToReview"> </a>

Par défaut, la condition de **Direction est** s’affiche et ne peut pas être supprimée. Si vous souhaitez que l’étendue de la révision supplémentaire (par exemple, uniquement examen du contenu qui contient des mots ou des expressions), cliquez sur **Ajouter une condition**. Vous pouvez spécifier plusieurs conditions si nécessaire.
  
Les conditions que vous choisissez seront appliquera aux communications à partir de sources de courrier électronique et 3 rd tiers dans votre organisation (par exemple avec Facebook ou échange). Pour plus d’informations sur l’importation des communications partie 3 rd dans votre organisation Office 365, voir [l’archivage des données tierces dans Office 365](https://technet.microsoft.com/EN-US/library/mt621583.aspx).
  
Le tableau suivant explique plus sur chaque condition.
  
|**Condition**|**Comment utiliser cette condition ?**|
|:-----|:-----|
|La direction est  <br/> |Sélectionnez **entrant** pour passer en revue les communications sont envoyées **aux** personnes que vous avez choisi pour le contrôle **de** personnes non inclus dans la stratégie.  <br/> Choisissez **sortant** si vous souhaitez examiner les communications qui sont envoyés **depuis** les personnes que vous avez choisi de surveiller ** à ** personnes non inclus dans la stratégie.  <br/> Choisissez **interne** pour passer en revue les communications envoyées **entre** les personnes que vous avez identifié dans la stratégie.  <br/> |
|Le message contient un de ces mots  <br/> Message ne contient aucun de ces mots  <br/> |Pour appliquer la stratégie des mots ou des expressions incluses ou exclues dans un message, entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez sera appliquée séparément (un seul de ces lignes doit s’appliquer de la stratégie à appliquer au message). Pour plus d’informations sur la saisie des mots ou expressions, consultez la section suivante, [mise en correspondance des mots et expressions pour les messages électroniques ou des pièces jointes](configure-supervision-policies.md#Matchwords).<br/> |
|Pièce jointe contient l’un de ces mots  <br/> Pièce jointe ne contient aucun de ces mots  <br/> |Pour appliquer la stratégie des mots ou des expressions incluses ou exclues dans une pièce jointe du message (par exemple un document Word), entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez sera appliquée séparément (une seule ligne doit s’appliquer de la stratégie à appliquer à la pièce jointe). Pour plus d’informations sur la saisie des mots ou expressions, consultez la section suivante, [mise en correspondance des mots et expressions pour les messages électroniques ou des pièces jointes](configure-supervision-policies.md#Matchwords).<br/> |
|Pièce jointe est une de ces types de fichiers  <br/> Pièce jointe est aucun de ces types de fichier  <br/> |Pour contrôler les communications qui inclure ou exclure des types de pièces jointes spécifiques, entrez les extensions de fichier (par exemple .exe ou .pdf). Si vous souhaitez inclure ou exclure plusieurs extensions de fichier, entrez ces sur des lignes distinctes. Extension qu’une pièce jointe doit correspondre pour appliquer la stratégie.  <br/> |
|La taille du message est supérieure à  <br/> Taille du message n’est pas supérieure  <br/> |Pour passer en revue les messages à partir d’une certaine taille, utilisez ces conditions pour spécifier la taille minimale ou maximale, qu'un message peut être avant d’être soumis à révision. Par exemple, si vous spécifiez la **taille du Message est supérieure à** \> **Mo 1.0**, tous les messages qui sont 1,01 Mo et plus faire l’objet de révision. Vous pouvez choisir d’octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.<br/> |
|Pièce jointe est supérieure à  <br/> Pièce jointe n’est pas supérieure  <br/> |Pour passer en revue les messages en fonction de la taille de leurs pièces jointes, spécifiez la taille minimale ou maximale une pièce jointe peut être avant le message et ses pièces jointes sont soumis à révision. Par exemple, si vous spécifiez la **pièce jointe est supérieure à** \> **Mo 2.0**, tous les messages avec pièces jointes Mo 2.01 et sera plu faire l’objet de révision. Vous pouvez choisir d’octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.<br/> |
   
#### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Correspondance de mots et expressions avec des courriers électroniques ou des pièces jointes
<a name="Matchwords"> </a>

Chaque ligne de mots que vous entrez sera appliquée séparément (une seule ligne doit appliquer pour la condition de stratégie à appliquer au courrier électronique ou pièce jointe). Par exemple, nous allons utiliser la condition, **que le Message contient un de ces mots**, bancaire « mots clés » et « initiés » sur des lignes distinctes. La stratégie s’applique à tous les messages qui inclut le bancaire « word » ou la phrase « initiés ». Un seul de ces mots ou phrases doit se produire pour cette condition de stratégie s’applique. Mots dans le message ou d’une pièce jointe doivent correspondre exactement ce que vous entrez.
  
#### <a name="entering-multiple-conditions"></a>Saisie de plusieurs conditions
<a name="Matchwords"> </a>

Si vous entrez plusieurs conditions, Office 365 utilise conjointement toutes les conditions pour déterminer le moment auquel appliquer la stratégie aux éléments de communication. Lorsque vous configurez plusieurs conditions, ils doivent tous les être remplies pour la stratégie à appliquer, sauf si vous entrez une exception. Par exemple, supposons que vous avez besoin créer une stratégie qui doit s’appliquer si un message contient le mot « Commerce » et est supérieur à 2 Mo. Toutefois, si le message contient également les mots « Approuvé par Contoso financière », la stratégie doit s’applique pas. Par conséquent, dans ce cas, les trois conditions serait comme suit : 
  
- **Le message contient un de ces mots**, avec les mots clés « Commerce »
    
- **Taille du message est supérieure**, avec la valeur 2 Mo
    
- **Message ne contient aucun de ces mots**, avec les mots clés « Approuvé par l’équipe financière Contoso ».
    
### <a name="specify-percentage-to-review"></a>Spécifier le pourcentage pour passer en revue
<a name="CommsToReview"> </a>

Si vous souhaitez réduire la quantité de contenu pour passer en revue, spécifiez un pourcentage. Sélectionnez aléatoire que quantité de contenu à partir du total qui remplissent les conditions que vous avez choisi. Si vous souhaitez que les relecteurs pour passer en revue tous les éléments, entrez **100 %**.
  
### <a name="choose-reviewers"></a>Choisissez relecteurs
<a name="CommsToReview"> </a>

Les utilisateurs et les groupes que vous choisissez utiliser l’application de surveillance dans Outlook web app pour examiner les communications sont renvoyées par cette stratégie. Vous pouvez inclure les adresses de messagerie des relecteurs internes ou externes. 
  
### <a name="review-your-settings"></a>Passez en revue vos paramètres
<a name="CommsToReview"> </a>

Une fois que vous avez terminé toutes les sections de la stratégie de surveillance, passez en revue vos paramètres et puis cliquez sur **Terminer** pour enregistrer votre stratégie. Il peut prendre quelques heures pour la stratégie de commencer la capture des communications. Surveillance offre toutes les communications de révision dans un dossier partagé réviseurs peuvent accéder dans Outlook web app. 
  
## <a name="use-outlook-web-app-to-review-communications-identified-by-a-supervision-policy"></a>Utiliser Outlook web app pour passer en revue les communications identifiées par une stratégie de surveillance
<a name="UseOutlook"> </a>

Relecteurs utilisera le complément de contrôle Outlook web App pour passer en revue les communications. Le complément est installé automatiquement dans Outlook web app pour tous les relecteurs spécifiés dans la stratégie. Prise en charge pour la version de bureau d’Outlook seront prochainement disponibles.
  
 **Examen des communications dans Outlook web app**
  
1. Dans Outlook web app, développez le **surveillance - \<nom de la stratégie\> ** dossier. 
    
2. Dans la ** \<nom de la stratégie\> ** sous-dossier, réviseurs verront toutes les communications identifiées par cette stratégie de surveillance. 
    
    ![Complément de contrôle dans Outlook web app affichant le sous-dossier de stratégie de surveillance sélectionné](media/eef329bf-2bd0-477e-a715-76ca19b3347f.jpg)
  
3. Ouvrez un élément pour passer en revue et cliquez sur le complément de **contrôle** . 
    
4. Utilisez le complément de classer l’élément comme **conforme**, **Non-compatible**, **Questionable** ou **résolu**. Une fois que vous avez classé un élément, il sera déplacé vers le sous-dossier correspondant sous le ** \<nom de la stratégie\> ** dossier. 
    

