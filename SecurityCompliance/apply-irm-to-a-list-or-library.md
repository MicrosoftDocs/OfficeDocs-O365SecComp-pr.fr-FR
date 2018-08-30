---
title: Appliquer des Information Rights Management (IRM) à une liste ou une bibliothèque
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1
description: Information Rights Management (IRM) permet de contrôler et protéger les fichiers qui sont téléchargés à partir de listes ou des bibliothèques.
ms.openlocfilehash: 5a48abf13841716d4dba34311d69ca2e6a5ea422
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528032"
---
# <a name="apply-information-rights-management-irm-to-a-list-or-library"></a>Appliquer des Information Rights Management (IRM) à une liste ou une bibliothèque

Information Rights Management (IRM) permet de contrôler et protéger les fichiers qui sont téléchargés à partir de listes ou des bibliothèques.
  
## <a name="before-you-begin"></a>Avant de commencer

- Le service d’Azure Rights Management (RMS Azure) à partir de la Protection des informations Azure et l’équivalent local, Active Directory Rights Management Services (AD RMS), prend en charge l’Information Rights Management pour les sites. Aucune installation distincte ou supplémentaires n’est nécessaires.
    
- Avant d’appliquer IRM à une liste ou une bibliothèque, il doit tout d’abord être activé par un administrateur de votre site.
    
- Pour appliquer IRM à une liste ou une bibliothèque, vous devez disposer des autorisations d’administrateur pour cette liste ou bibliothèque.
    
- Si vous utilisez SharePoint Online, vos utilisateurs peuvent rencontrer des délais d’attente lors du téléchargement de fichiers protégés par IRM plus volumineux. Dans ce cas, puis appliquer la protection IRM à l’aide de vos programmes Office et stocker des fichiers volumineux dans une bibliothèque SharePoint qui n’utilise pas d’IRM.
    
> [!NOTE]
> Si vous utilisez SharePoint Server 2013, un administrateur de serveur doit installer des logiciels de protection sur tous les serveurs Web frontaux pour chaque type de fichier que les personnes dans votre organisation souhaitent protéger à l’aide d’IRM. 
  
## <a name="apply-irm-to-a-list-or-library"></a>Appliquer IRM à une liste ou une bibliothèque
<a name="__toc256598179"> </a>

![Paramètres de gestion des droits de l’information](media/1b708102-9c90-42b0-b255-ef0e72d0be88.png)
  
1. Accédez à la liste ou la bibliothèque pour laquelle vous souhaitez configurer IRM.
    
2. Dans le ruban, cliquez sur l’onglet **bibliothèque** , puis cliquez sur **Paramètres de la bibliothèque**. (Si vous travaillez dans une liste, cliquez sur l’onglet **liste** , puis cliquez sur **Paramètres de la liste**).
    
    ![Boutons du ruban de paramètres de la bibliothèque SharePoint](media/cdf718fa-d792-40fc-8026-00c3b80b9e05.png)
  
3. Sous **autorisations et gestion**, cliquez sur **Gestion des droits**. Si le lien Information Rights Management n’apparaît pas, IRM ne peut pas être activé pour votre site. Contactez votre administrateur système pour voir s’il est possible d’activer IRM pour votre site. Le lien Information Rights Management n’apparaît pas pour les bibliothèques d’images.
    
4. Dans la page **Paramètres de gestion des droits d’informations** , activez la case à cocher **limiter l’accès aux documents de cette bibliothèque au téléchargement** à appliquer des autorisations restreintes aux documents qui sont téléchargés à partir de cette liste ou bibliothèque. 
    
5. Dans la zone **créer un titre de stratégie d’autorisation** , tapez un nom descriptif pour la stratégie que vous pouvez utiliser ultérieurement pour différencier cette stratégie des autres stratégies. Par exemple, vous pouvez taper **Confidentiel** si vous appliquez une autorisation restreinte à une liste ou bibliothèque qui contiendra les documents confidentiels de l’entreprise. 
    
6. Dans la zone **Ajouter une description de stratégie d’autorisation** , tapez une description qui s’affichera pour les personnes qui utilisent cette liste ou bibliothèque expliquant comment gérer les documents dans cette liste ou bibliothèque. Par exemple, vous pouvez taper **discuter du contenu de ce document avec d’autres employés uniquement** si vous souhaitez restreindre l’accès aux informations de ces documents aux employés internes. 
    
7. Pour appliquer des restrictions supplémentaires aux documents de cette liste ou bibliothèque, cliquez sur **Afficher les Options**et effectuez l’une des options suivantes :
    
|**Pour ce faire, procédez comme suit :**|**Procédez comme suit :**|
|:-----|:-----|
|Autoriser les utilisateurs à imprimer des documents à partir de cette liste ou bibliothèque  <br/> |Activez la case à cocher **Autoriser les utilisateurs à imprimer** .  <br/> |
|Autoriser les personnes possédant au moins l’autorisation Afficher les éléments à exécuter du code incorporé ou des macros dans un document.  <br/> |Activez la case à cocher **permettre aux visionneuses d’exécuter le script et écran lecteur pour fonctionner sur des documents téléchargés** .  <br/> Si vous sélectionnez cette option, les utilisateurs peuvent exécuter du code pour extraire le contenu d’un document.           |
|Nécessitent aux utilisateurs de vérifier leurs informations d’identification à des intervalles spécifiques.  <br/> Sélectionnez cette option si vous souhaitez restreindre l’accès au contenu à une période de temps spécifiée. Si vous sélectionnez cette option, licences d’émission les pour accéder au contenu expire après que le nombre de jours et les personnes spécifié doit renvoyer au serveur afin de vérifier leurs informations d’identification et télécharger une nouvelle copie.  <br/> |Sélectionnez le **les utilisateurs doivent vérifier leurs informations d’identification à l’aide de cet intervalle (jours)** case à cocher, puis spécifiez le nombre de jours pour lesquels vous souhaitez que le document soit visible.  <br/> |
| Empêcher des personnes de télécharger des documents qui ne prennent pas en charge IRM à cette liste ou bibliothèque.  <br/>  Si vous sélectionnez cette option, personnes ne sera pas en mesure de télécharger un des types de fichiers suivants :  <br/>  Types de fichiers qui n’ont pas installée sur tous les serveurs Web frontaux de protection IRM correspondant.  <br/>  Types de fichiers SharePoint Server 2010 ne peut pas déchiffrer.  <br/>  Types de fichiers qui sont protégés par IRM dans un autre programme  <br/> |Activez la case à cocher **ne pas autoriser les utilisateurs à télécharger des documents qui ne prennent pas en charge IRM** .  <br/> |
|Supprimer les autorisations restreintes de cette liste ou bibliothèque à une date spécifique.  <br/> |Activez la case à cocher **Arrêter la restriction de l’accès à la bibliothèque à** , puis sélectionnez la date à laquelle vous souhaitez.  <br/> |
|Contrôle l’intervalle que les informations d’identification sont mis en cache pour le programme qui possède une licence pour ouvrir le document.  <br/> |Dans **définir du groupe de protection et un intervalle d’informations d’identification**, entrez theinterval pour la mise en cache des informations d’identification en nombre de jours.  <br/> |
|Autoriser le groupe de protection afin que les utilisateurs peuvent partager avec les membres du même groupe.  <br/> |Sélectionnez **Autoriser la protection par groupe**, puis entrez le nom du groupe pour le partage.  <br/> |
   
8. Après avoir sélectionné les options souhaitées, cliquez sur **OK**.
  
## <a name="what-is-information-rights-management"></a>Nouveautés d’Information Rights Management ?
<a name="__toc256598175"> </a>

Information Rights Management (IRM) vous permet de limiter les actions que les utilisateurs peuvent effectuer sur les fichiers qui ont été téléchargés à partir de listes ou des bibliothèques. IRM chiffre les fichiers téléchargés et limite l’ensemble des utilisateurs et des programmes autorisés à déchiffrer ces fichiers. IRM peut également limiter les droits des utilisateurs autorisés à lire les fichiers, afin qu’ils ne peuvent pas effectuer des actions telles que l’impression des fichiers ou copier du texte.
  
Vous pouvez utiliser IRM sur des listes ou bibliothèques pour limiter la diffusion de contenu sensible. Par exemple, si vous créez une bibliothèque de documents pour partager des informations sur les produits à venir avec agents marketing sélectionnés, vous pouvez utiliser IRM pour empêcher ces personnes de partager ce contenu avec d’autres employés de la société.
  
Sur un site, IRM est appliqué à un ensemble de la liste ou une bibliothèque, et non aux fichiers individuels. Cela facilite assurer un niveau cohérent de protection pour un ensemble de documents ou des fichiers. IRM peut donc aider votre organisation d’appliquer des stratégies d’entreprise qui régissent l’utilisation et la diffusion d’informations confidentielles ou propriétaires.
  
> [!NOTE]
> Les informations sur cette page concernant Information Rights Management remplace tous les termes qui font référence à « Information Rights Management » dans les accords de termes de licence Microsoft SharePoint Server 2013 et SharePoint Server 2016. 
  
### <a name="how-irm-can-help-protect-content"></a>Comment IRM peut contribuer à protéger le contenu
<a name="__toc256598176"> </a>

IRM permet de protéger le contenu de la manière suivante :
  
- Empêche un utilisateur autorisé à partir de la copie, modification, l’impression, télécopie, copier-coller le contenu pour une utilisation non autorisée
    
- Empêche un utilisateur autorisé de copier le contenu à l’aide de la fonctionnalité impression écran dans Microsoft Windows
    
- Permet d’empêcher un utilisateur non autorisé de visualiser le contenu s’il est envoyé par courrier électronique après son téléchargement à partir du serveur
    
- Limite l’accès au contenu à une période de temps, après lequel les utilisateurs doivent vérifier leurs informations d’identification et téléchargez de nouveau le contenu spécifié
    
- Permet d’appliquer des stratégies d’entreprise qui régissent l’utilisation et la diffusion de contenu au sein de votre organisation
    
### <a name="how-irm-cannot-help-protect-content"></a>Comment IRM ne peut pas protéger le contenu
<a name="__toc256598177"> </a>

IRM ne peut pas protéger le contenu dans les éléments suivants :
  
- Effacement, vol, capture ou transmission par des programmes malveillants tels que des chevaux de Troie, enregistreur de frappe et certains types de logiciels espions
    
- Perte ou corruption suite aux actions de virus sur l’ordinateur
    
- Copie manuelle ou refrappe de contenu à partir de l’affichage sur un écran
    
- Numérique ou d’un film photographie du contenu qui est affiché à l’écran
    
- Copie au moyen de programmes de capture d’écran tiers
    
- Copie de métadonnées de contenu (valeurs de colonne) à l’aide de programmes de capture d’écran tiers ou action de copier et coller
    
[Appliquer la Gestion des droits relatifs à l'information à une liste ou une bibliothèque](https://support.office.com/article/6714cfe3-ef39-43b0-bb65-a887726bb63c)
  
## <a name="how-irm-works-for-lists-and-libraries"></a>Fonctionnement d’IRM pour les listes et bibliothèques
<a name="__toc256598178"> </a>

Protection IRM est appliquée aux fichiers au niveau de la liste ou la bibliothèque. Lorsqu’IRM est activé pour une bibliothèque, gestion des droits s’applique à tous les fichiers dans cette bibliothèque. Lorsqu’IRM est activé pour une liste, gestion des droits s’applique uniquement aux fichiers qui sont joints à des éléments de liste, pas les éléments de liste proprement dite.
  
Lorsque les utilisateurs téléchargent des fichiers dans une IRM activé une liste ou une bibliothèque, les fichiers sont chiffrés afin que seules les personnes autorisées puissent les consulter. Chaque fichier géré par des droits contient aussi une licence d’émission qui impose des restrictions sur les personnes qui permet d’afficher le fichier. Restrictions habituelles consistent un fichier en lecture seule, désactivation de la copie de texte, empêcher l’enregistrement d’une copie locale et de l’impression du fichier. Les programmes clients qui peuvent lire des types de fichiers pris en charge IRM utilisent la licence d’émission dans le fichier géré par des droits pour appliquer ces restrictions. Voici comment un fichier géré par des droits conserve sa protection même après son téléchargement à partir du serveur.
  
Les types de restrictions qui sont appliquées à un fichier lorsqu’il est téléchargé à partir d’une liste ou une bibliothèque sont basés sur les autorisations de l’utilisateur sur le site qui contient le fichier. Le tableau suivant explique comment les autorisations sur les sites correspondent aux autorisations IRM.
  
|**Autorisations**|**Autorisations IRM**|
|:-----|:-----|
|Gérer les autorisations, gérer le Site Web  <br/> |**Contrôle total** (tel que défini par le programme client) : cette autorisation permet généralement à un utilisateur de lire, modifier, copier, enregistrer et modifier les autorisations de contenu géré par des droits.  <br/> |
|Modifier les éléments, gérer les listes, ajouter et personnaliser des Pages  <br/> |**Modifier**, **Copier**et **Enregistrer**: un utilisateur peut imprimer un fichier uniquement si la case à cocher **Autoriser les utilisateurs à imprimer des documents** est sélectionnée dans la page Paramètres de gestion des droits des informations pour la liste ou bibliothèque.  <br/> |
|Afficher les éléments  <br/> |**Lecture**: un utilisateur peut lire le document, mais ne peut pas copier ou modifier son contenu. Un utilisateur peut imprimer uniquement si la case à cocher **Autoriser les utilisateurs à imprimer des documents** est sélectionnée dans la page Paramètres de gestion des droits des informations pour la liste ou bibliothèque.<br/> |
|Autre  <br/> |Aucune autre autorisation ne correspondre directement aux autorisations IRM.  <br/> |
   
Lorsque vous activez IRM pour une liste ou une bibliothèque dans SharePoint Server 2013, vous pouvez protéger uniquement les types de fichier dans la liste ou la bibliothèque pour laquelle un logiciel de protection est installé sur tous les serveurs Web frontaux. Un logiciel de protection est un programme qui contrôle le chiffrement et déchiffrement des fichiers gérés par des droits d’un format de fichier spécifique. SharePoint inclut des logiciels de protection pour les types de fichier suivants :
  
- Formulaires Microsoft Office InfoPath
    
- Les formats de fichiers 97-2003 pour les programmes Microsoft Office suivants : Word, Excel et PowerPoint
    
- Les Formats Office Open XML pour les programmes Microsoft Office suivants : Word, Excel et PowerPoint
    
- Le format XML Paper Specification (XPS)
    
Si votre organisation envisage d’utiliser IRM pour protéger des autres types de fichiers en plus de ceux répertoriés ci-dessus, votre administrateur de serveur doit installer des logiciels de protection de ces formats de fichiers supplémentaires.
  

