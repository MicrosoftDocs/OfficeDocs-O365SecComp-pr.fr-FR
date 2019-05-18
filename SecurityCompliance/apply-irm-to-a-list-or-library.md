---
title: Appliquer la gestion des droits relatifs à l’information (IRM) à une liste ou une bibliothèque
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1
ms.collection:
- M365-security-compliance
description: Vous pouvez utiliser la gestion des droits relatifs à l’information (IRM) pour contrôler et protéger les fichiers téléchargés à partir de listes ou de bibliothèques.
ms.openlocfilehash: 3c350a3648b77992dd8e86ee47498efc327b2af8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152336"
---
# <a name="apply-information-rights-management-irm-to-a-list-or-library"></a>Appliquer la gestion des droits relatifs à l’information (IRM) à une liste ou une bibliothèque

Vous pouvez utiliser la gestion des droits relatifs à l’information (IRM) pour contrôler et protéger les fichiers téléchargés à partir de listes ou de bibliothèques.
  
## <a name="before-you-begin"></a>Avant de commencer

- Le service Azure Rights Management (Azure RMS) d’Azure information protection et l’équivalent local, AD RMS (Active Directory Rights Management Services), prennent en charge la gestion des droits relatifs à l’information pour les sites. Aucune installation séparée ou supplémentaire n’est requise.
    
- Avant d’appliquer la gestion des droits relatifs à l’information à une liste ou à une bibliothèque, elle doit d’abord être activée par un administrateur de votre site.
    
- Pour appliquer la gestion des droits relatifs à l’information à une liste ou à une bibliothèque, vous devez disposer d’autorisations d’administrateur pour cette liste ou bibliothèque.
    
- Si vous utilisez SharePoint Online, vos utilisateurs peuvent être confronté à des délais d’attente lors du téléchargement de fichiers plus volumineux protégés par IRM. Dans ce cas, appliquez la protection IRM à l’aide de vos programmes Office et stockez des fichiers volumineux dans une bibliothèque SharePoint qui n’utilise pas la gestion des droits relatifs à l’information.
    
> [!NOTE]
> Si vous utilisez SharePoint Server 2013, un administrateur de serveur doit installer des logiciels de protection sur tous les serveurs Web frontaux pour chaque type de fichier que les personnes de votre organisation souhaitent protéger à l’aide d’IRM. 
  
## <a name="apply-irm-to-a-list-or-library"></a>Appliquer la gestion des droits relatifs à l’information à une liste ou à une bibliothèque
<a name="__toc256598179"> </a>

![Paramètres de gestion des droits relatifs à l’information](media/1b708102-9c90-42b0-b255-ef0e72d0be88.png)
  
1. Accédez à la liste ou à la bibliothèque pour laquelle vous souhaitez configurer la gestion des droits relatifs à l’information.
    
2. Dans le ruban, cliquez sur l’onglet **bibliothèque** , puis sur **paramètres**de la bibliothèque. (Si vous utilisez une liste, cliquez sur l’onglet **liste** , puis sur paramètres de la **liste**).
    
    ![Boutons des paramètres de bibliothèque SharePoint sur le ruban](media/cdf718fa-d792-40fc-8026-00c3b80b9e05.png)
  
3. Sous **autorisations et gestion**, cliquez sur **gestion des droits relatifs**à l’information. Si le lien gestion des droits relatifs à l’information n’apparaît pas, il est possible que l’IRM ne soit pas activée pour votre site. Contactez votre administrateur de serveur pour savoir s’il est possible d’activer la gestion des droits relatifs à l’information pour votre site. Le lien gestion des droits relatifs à l’information n’apparaît pas pour les bibliothèques d’images.
    
4. Sur la page **paramètres de gestion des droits relatifs** à l’information, activez la case à cocher **restreindre l’autorisation d’accès aux documents de cette bibliothèque au téléchargement** pour appliquer des autorisations restreintes aux documents téléchargés à partir de cette liste ou bibliothèque. 
    
5. Dans la zone de **titre créer une stratégie d’autorisation** , tapez un nom descriptif pour la stratégie que vous pouvez utiliser ultérieurement pour différencier cette stratégie des autres stratégies. Par exemple, vous pouvez taper **confidentiel société** si vous appliquez des autorisations restreintes à une liste ou une bibliothèque qui contiendra des documents d’entreprise confidentiels. 
    
6. Dans la zone **Ajouter une description** de la stratégie d’autorisation, tapez une description qui s’affichera pour les utilisateurs de cette liste ou bibliothèque qui expliquent comment ils doivent gérer les documents de cette liste ou bibliothèque. Par exemple, vous pouvez taper **discuter du contenu de ce document uniquement avec d’autres employés** si vous souhaitez limiter l’accès aux informations contenues dans ces documents aux employés internes. 
    
7. Pour appliquer des restrictions supplémentaires aux documents de cette liste ou bibliothèque, cliquez sur **afficher les options**, puis effectuez l’une des opérations suivantes:
    
|**Pour ce faire :**|**Procédez comme suit:**|
|:-----|:-----|
|Autoriser les utilisateurs à imprimer des documents à partir de cette liste ou bibliothèque  <br/> |Activez la case à cocher **autoriser les utilisateurs à imprimer** .  <br/> |
|Autorisez les utilisateurs disposant au moins de l’autorisation Afficher les éléments à exécuter du code incorporé ou des macros dans un document.  <br/> |Activez la case à cocher **autoriser les visualiseurs à exécuter le script et le lecteur d’écran pour fonctionner sur les documents téléchargés** .  <br/> Si vous sélectionnez cette option, les utilisateurs peuvent exécuter du code pour extraire le contenu d’un document.           |
|Exiger que les personnes vérifient leurs informations d’identification à intervalles spécifiques.  <br/> Sélectionnez cette option si vous souhaitez restreindre l’accès au contenu à une période de temps spécifiée. Si vous sélectionnez cette option, les licences d’émission de personnes pour accéder au contenu expireront après le nombre de jours spécifié, et les personnes seront obligées de retourner au serveur pour vérifier leurs informations d’identification et télécharger une nouvelle copie.  <br/> |Activez la case à cocher les **utilisateurs doivent vérifier leurs informations d’identification à l’aide de cet intervalle (jours)** , puis spécifiez le nombre de jours pendant lesquels vous souhaitez que le document soit affichable.  <br/> |
| Empêcher les utilisateurs de télécharger des documents qui ne prennent pas en charge IRM sur cette liste ou bibliothèque.  <br/>  Si vous sélectionnez cette option, les utilisateurs ne pourront pas télécharger les types de fichiers suivants:  <br/>  Types de fichiers qui n’ont pas de logiciels de protection IRM correspondant installés sur tous les serveurs Web frontaux.  <br/>  Types de fichiers que SharePoint Server 2010 ne peut pas déchiffrer.  <br/>  Types de fichiers protégés par IRM dans un autre programme  <br/> |Activez la case à cocher **ne pas autoriser les utilisateurs à télécharger des documents qui ne prennent pas en charge IRM** .  <br/> |
|Supprimez les autorisations restreintes de cette liste ou bibliothèque à une date spécifique.  <br/> |Activez la case à cocher **arrêter de restreindre l’accès à la bibliothèque à** , puis sélectionnez la date de votre choix.  <br/> |
|Contrôlez l’intervalle de mise en cache des informations d’identification pour le programme sous licence pour ouvrir le document.  <br/> |Dans l' **intervalle définir la protection de groupe et les informations d’identification**, entrez theinterval pour mettre en cache les informations d’identification en nombre de jours.  <br/> |
|Autoriser la protection de groupe afin que les utilisateurs puissent partager avec les membres du même groupe.  <br/> |Sélectionnez **autoriser la protection du groupe**, puis entrez le nom du groupe pour le partage.  <br/> |
   
8. Une fois que vous avez terminé de sélectionner les options souhaitées, cliquez sur **OK**.
  
## <a name="what-is-information-rights-management"></a>Qu’est-ce que la gestion des droits relatifs à l’information?
<a name="__toc256598175"> </a>

La gestion des droits relatifs à l’information (IRM) vous permet de limiter les actions que les utilisateurs peuvent effectuer sur les fichiers qui ont été téléchargés à partir de listes ou de bibliothèques. IRM chiffre les fichiers téléchargés et limite l’ensemble des utilisateurs et des programmes autorisés à déchiffrer ces fichiers. IRM peut également limiter les droits des utilisateurs qui sont autorisés à lire des fichiers, pour leur interdire par exemple d’effectuer des actions telles qu’imprimer des copies des fichiers ou copier du texte de ceux-ci.
  
Vous pouvez utiliser la gestion des droits relatifs à l’information (IRM) sur des listes ou des bibliothèques pour limiter la diffusion de contenu sensible. Par exemple, si vous créez une bibliothèque de documents pour partager des informations sur les produits à venir avec des délégués marketing sélectionnés, vous pouvez utiliser la gestion des droits relatifs à l’information pour empêcher ces personnes de partager ce contenu avec d’autres employés de l’entreprise.
  
Sur un site, vous appliquez IRM à une liste ou une bibliothèque entière, et non à des fichiers individuels. Cela permet de garantir un niveau de protection cohérent pour l’ensemble des documents ou des fichiers. La gestion des droits relatifs à l’information peut ainsi aider votre organisation à appliquer des stratégies d’entreprise qui régissent l’utilisation et la diffusion d’informations confidentielles ou propriétaires.
  
> [!NOTE]
> Les informations contenues dans cette page relatives à la gestion des droits relatifs à l’information remplacent tous les termes qui font référence à la «gestion des droits relatifs à l’information» dans les accords de termes de licence Microsoft SharePoint Server 2013 et SharePoint Server 2016. 
  
### <a name="how-irm-can-help-protect-content"></a>Comment la gestion des droits relatifs à l’information peut protéger le contenu
<a name="__toc256598176"> </a>

La gestion des droits relatifs à l’information permet de protéger le contenu restreint des manières suivantes:
  
- Empêche une personne autorisée à copier, modifier, imprimer, télécopier ou copier et coller le contenu pour une utilisation non autorisée.
    
- Permet d’empêcher une personne autorisée de copier le contenu à l’aide de la fonctionnalité Impr écran de Microsoft Windows
    
- Empêche un utilisateur non autorisé d’afficher le contenu s’il est envoyé par courrier électronique après avoir été téléchargé à partir du serveur
    
- Limite l’accès au contenu à une période de temps spécifiée, après quoi les utilisateurs doivent confirmer leurs informations d’identification et télécharger de nouveau le contenu
    
- Permet d’appliquer des stratégies d’entreprise qui régissent l’utilisation et la diffusion du contenu au sein de votre organisation
    
### <a name="how-irm-cannot-help-protect-content"></a>Protection du contenu par la gestion des droits relatifs à l’information
<a name="__toc256598177"> </a>

La gestion des droits relatifs à l’information ne peut pas protéger le contenu restreint des éléments suivants:
  
- Effacement, vol, capture ou transmission par des programmes malveillants tels que des chevaux de Troie, des enregistreurs de frappe et certains types de logiciels espions
    
- Perte ou corruption en raison des actions des virus informatiques
    
- Copie manuelle ou Refrappe de contenu à partir de l’affichage sur un écran
    
- Photographie numérique ou cinématographique de contenu affiché à l’écran
    
- Copie à l’aide de programmes de capture d’écran tiers
    
- Copie de métadonnées de contenu (valeurs de colonne) à l’aide de programmes de capture d’écran tiers ou de l’action copier-coller
    
[Appliquer la Gestion des droits relatifs à l'information à une liste ou une bibliothèque](https://support.office.com/article/6714cfe3-ef39-43b0-bb65-a887726bb63c)
  
## <a name="how-irm-works-for-lists-and-libraries"></a>Fonctionnement de la gestion des droits relatifs à l’information pour les listes et les bibliothèques
<a name="__toc256598178"> </a>

La protection IRM est appliquée aux fichiers au niveau de la liste ou de la bibliothèque. Lorsque la gestion des droits relatifs à l’information est activée pour une bibliothèque, Rights Management s’applique à tous les fichiers de cette bibliothèque. Lorsque la gestion des droits relatifs à l’information est activée pour une liste, la gestion des droits s’applique uniquement aux fichiers joints à des éléments de liste, et non aux éléments de liste réels.
  
Lorsque des personnes téléchargent des fichiers dans une liste ou une bibliothèque activée pour IRM, les fichiers sont chiffrés de sorte que seules les personnes autorisées puissent les afficher. Chaque fichier géré par des droits contient également une licence d’émission qui impose des restrictions sur les personnes qui visualisent le fichier. Les restrictions habituelles incluent la création d’un fichier en lecture seule, la désactivation de la copie de texte, l’interdiction de l’enregistrement d’une copie locale et l’interdiction d’impression du fichier. Les programmes clients qui peuvent lire les types de fichiers pris en charge par IRM utilisent la licence d’émission dans le fichier géré par des droits pour appliquer ces restrictions. Voici comment un fichier géré par des droits conserve sa protection même après avoir été téléchargé à partir du serveur.
  
Les types de restrictions appliquées à un fichier lorsqu’il est téléchargé à partir d’une liste ou d’une bibliothèque sont basés sur les autorisations de l’utilisateur individuel sur le site qui contient le fichier. Le tableau suivant explique comment les autorisations sur les sites correspondent aux autorisations IRM.
  
|**Autorisations**|**Autorisations IRM**|
|:-----|:-----|
|Gérer les autorisations, gérer le site Web  <br/> |**Contrôle total** (tel que défini par le programme client): cette autorisation permet généralement à un utilisateur de lire, modifier, copier, enregistrer et modifier des autorisations de contenu géré par des droits.  <br/> |
|Modifier des éléments, gérer des listes, ajouter et personnaliser des pages  <br/> |**Modifier**, **copier**et **Enregistrer**: un utilisateur peut imprimer un fichier uniquement si la case **à cocher Autoriser les utilisateurs à imprimer des documents** est activée sur la page Paramètres de gestion des droits relatifs à l’information pour la liste ou la bibliothèque.  <br/> |
|Afficher les éléments  <br/> |**Lecture**: un utilisateur peut lire le document, mais ne peut pas copier ou modifier son contenu. Un utilisateur ne peut imprimer que si la case à cocher **autoriser les utilisateurs à imprimer des documents** est activée sur la page Paramètres de gestion des droits relatifs à l’information pour la liste ou la bibliothèque.  <br/> |
|Other  <br/> |Aucune autre autorisation ne correspond directement aux autorisations IRM.  <br/> |
   
Lorsque vous activez IRM pour une liste ou une bibliothèque dans SharePoint Server 2013, vous pouvez uniquement protéger les types de fichiers de cette liste ou bibliothèque pour lesquels un logiciel de protection est installé sur tous les serveurs Web frontaux. Un protecteur est un programme qui contrôle le chiffrement et le déchiffrement des fichiers gérés par des droits d’un format de fichier spécifique. SharePoint inclut des logiciels de protection pour les types de fichiers suivants:
  
- Formulaires Microsoft Office InfoPath
    
- Formats de fichiers 97-2003 pour les programmes Microsoft Office suivants: Word, Excel et PowerPoint
    
- Formats Office Open XML pour les programmes Microsoft Office suivants: Word, Excel et PowerPoint
    
- Format XPS (XML Paper Specification)
    
Si votre organisation envisage d’utiliser la gestion des droits relatifs à l’information pour protéger d’autres types de fichiers en plus de ceux mentionnés ci-dessus, votre administrateur de serveur doit installer des logiciels de protection pour ces formats de fichiers supplémentaires.
  

