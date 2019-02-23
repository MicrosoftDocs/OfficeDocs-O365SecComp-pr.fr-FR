---
title: Créer des alertes d'activité dans le centre &amp; de sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/7/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- BCS160
- MET150
ms.assetid: 72bbad69-035b-4d33-b8f4-549a2743e97d
description: Ajoutez et gérez les alertes d'activité dans &amp; le centre de sécurité conformité afin qu'Office 365 vous envoie des notifications par courrier électronique lorsque les utilisateurs effectuent des activités spécifiques dans Office 365.
ms.openlocfilehash: 25262105332b5317ddf29d49e0364faed57f3d3a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214904"
---
# <a name="create-activity-alerts-in-the-office-365-security-amp-compliance-center"></a>Créer des alertes d'activité dans le centre &amp; de sécurité conformité Office 365

Vous pouvez créer une alerte d'activité qui vous enverra une notification par courrier électronique lorsque les utilisateurs effectuent des activités spécifiques dans Office 365. Les alertes d'activité sont semblables à la recherche d'événements dans le journal d'audit Office 365, sauf que vous recevrez un message électronique lorsqu'un événement pour une activité pour laquelle vous avez créé une alerte se produit. 
  
 **Pourquoi utiliser des alertes d'activité au lieu de rechercher dans le journal d'audit?** Il peut y avoir certains types d'activité ou d'activité réalisés par des utilisateurs spécifiques que vous voulez vraiment connaître. Au lieu de se souvenir de rechercher dans le journal d'audit de ces activités, vous pouvez utiliser des alertes d'activité pour qu'Office 365 vous envoie un message électronique lorsque les utilisateurs effectuent ces activités. Par exemple, vous pouvez créer une alerte activité pour vous avertir lorsqu'un utilisateur supprime des fichiers dans SharePoint ou vous pouvez créer une alerte pour vous avertir lorsqu'un utilisateur supprime définitivement des messages de leur boîte aux lettres. La notification par courrier électronique qui vous a été envoyée inclut des informations sur l'activité qui a été effectuée et sur l'utilisateur qui l'a exécutée. 

> [!NOTE]
> Nous vous recommandons de commencer à utiliser les stratégies d'alerte dans le centre de sécurité & Compliance Center au lieu de créer des alertes d'activité. Les stratégies d'alerte fournissent des fonctionnalités supplémentaires, telles que la création d'une stratégie d'alerte qui déclenche une alerte lorsqu'un utilisateur effectue une activité spécifique et affiche des alertes sur la page **afficher les alertes** dans le centre de sécurité _AMP_ Compliance Center. Pour plus d'informations, consultez [la rubrique Alert Policies in &amp; the Office 365 Security Compliance Center](alert-policies.md).
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez disposer du rôle configuration de l'organisation dans le &amp; Centre de sécurité conformité pour gérer les alertes d'activité. Par défaut, ce rôle est affecté aux groupes de rôles Administrateur de conformité et gestion de l'organisation. Pour plus d'informations sur l'ajout de membres à des groupes de rôles, consultez [la rubrique accorder &amp; aux utilisateurs l'accès au centre de sécurité conformité Office 365](grant-access-to-the-security-and-compliance-center.md).
    
- Vous (ou un autre administrateur) devez d'abord activer la journalisation d'audit pour votre organisation avant de pouvoir commencer à utiliser les alertes d'activité. Pour ce faire, cliquez simplement sur Démarrer l'enregistrement des activités de l' **utilisateur et** de l'administrateur dans la page **alertes d'activité** . (Si vous ne voyez pas ce lien, l'audit a déjà été activé pour votre organisation.) Vous pouvez également activer l'audit sur la page **recherche du journal d'audit** dans le &amp; Centre de sécurité conformité (accéder à recherche dans le \> **Journal d'audit**de la **recherche &amp; ** ). Vous ne devez effectuer cette opération qu'une seule fois pour votre organisation.
  
- Vous pouvez créer des alertes pour les mêmes activités que celles que vous pouvez rechercher dans le journal d'audit Office 365. Consultez la section [more information](#more-information) pour obtenir la liste des scénarios courants (et l'activité spécifique à surveiller) pour lesquels vous pouvez créer des alertes. 
    
- Vous pouvez utiliser la page **alertes d'activité** du centre &amp; de sécurité conformité pour créer des alertes uniquement pour les activités effectuées par les utilisateurs répertoriés dans le carnet d'adresses de votre organisation. Vous ne pouvez pas utiliser cette page pour créer des alertes pour les activités effectuées par des utilisateurs externes qui ne sont pas mentionnés dans le carnet d'adresses. 
    
## <a name="create-an-activity-alert"></a>Créer une alerte d'activité

1. Accédez à la page [https://protection.office.com/#/managealerts](https://protection.office.com/#/managealerts).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Sur la **page alertes d'activité** , ![cliquez sur](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) ajouter une icône **nouveau**.

   La page de menu volant pour créer une alerte d'activité s'affiche.

    
    ![Créer une alerte d'activité](media/53888bd5-9fa2-4398-8ccc-1a9dc72517ac.png)
  
4. Complétez les champs suivants pour créer une alerte d'activité:
    
    a. **nom** -entrez un nom pour l'alerte. Les noms d'alerte doivent être uniques au sein de votre organisation.
    
    b. **Description** (facultatif): Décrivez l'alerte, par exemple les activités et les utilisateurs suivis, ainsi que les utilisateurs auxquels sont envoyées les notifications par courrier électronique. Les descriptions offrent un moyen rapide et facile de décrire l'objectif de l'alerte aux autres administrateurs.
    
    c. **type d'alerte** : Assurez-vous que l'option **personnalisée** est sélectionnée. 

    d. **Envoyer cette alerte quand** -cliquer sur **Envoyer cette alerte quand** , puis configurer ces deux champs:
    
    - **Activités** : cliquez sur la liste déroulante pour afficher les activités pour lesquelles vous pouvez créer une alerte. Il s'agit de la même liste d'activités que celle qui s'affiche lorsque vous recherchez dans le journal d'audit Office 365. Vous pouvez sélectionner une ou plusieurs activités spécifiques ou cliquer sur le nom du groupe d'activités pour sélectionner toutes les activités du groupe. Pour obtenir une description de ces activités, reportez-vous à la section «activités auditées» dans la rubrique [Search the Audit Log in the Office 365 Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities). Lorsqu'un utilisateur effectue une des activités que vous avez ajoutées à l'alerte, une notification par courrier électronique est envoyée. 
    
     - **Utilisateurs** : cliquez sur cette zone, puis sélectionnez un ou plusieurs utilisateurs. Si les utilisateurs de cette zone exécutent les activités que vous avez ajoutées à la zone **activités** , une alerte est envoyée. Laissez la zone **utilisateurs** vide pour envoyer une alerte lorsqu'un utilisateur de votre organisation effectue les activités spécifiées par l'alerte. 

    e. **Envoyer cette alerte en** cliquant sur **Envoyer cette alerte**, puis cliquez dans la zone **destinataires** et tapez un nom pour ajouter des utilisateurs qui recevront une notification par courrier électronique lorsqu'un utilisateur (spécifié dans la zone **utilisateurs** ) effectue une activité (spécifiée dans le Zone **activités** ). Notez que vous êtes ajouté à la liste des destinataires par défaut. Vous pouvez supprimer votre nom de cette liste.
    
5. Cliquez sur **Enregistrer** pour créer l'alerte. 
    
    La nouvelle alerte est affichée dans la liste sur la page **alertes d'activité** . 
    
    ![Une liste d'alertes s'affiche sur la page alertes d'activité dans le &amp; Centre de sécurité et de conformité](media/02b774f2-1719-41de-bbc9-5e5b7576f335.png)
  
    L'état de l'alerte est **activé**. Notez que les destinataires qui recevront une notification par courrier électronique lors de l'envoi d'une alerte sont également répertoriés. 
  
## <a name="turn-off-an-activity-alert"></a>Désactiver une alerte d'activité

Vous pouvez désactiver une alerte d'activité de sorte qu'aucune notification par courrier électronique ne soit envoyée. Une fois que vous avez désactivé l'alerte d'activité, celle-ci apparaît toujours dans la liste des alertes d'activité de votre organisation et vous pouvez toujours afficher ses propriétés.
  
1. Accédez à la page [https://protection.office.com/#/managealerts](https://protection.office.com/#/managealerts).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans la liste des alertes d'activité pour votre organisation, cliquez sur l'alerte que vous souhaitez désactiver.
    
4. Sur la **page modifier l'alerte** , cliquez **** sur le bouton basculer pour définir l'État sur **désactivé**, puis cliquez sur **Enregistrer**.
    
    L'état de l'alerte sur la page **alertes d'activité** est **désactivé**. 
    
Pour réactiver une alerte activité, répétez ces étapes et cliquez sur **** le bouton bascule inactif pour définir l'État sur **activé**.
  
## <a name="more-information"></a>Plus d’informations

- Voici un exemple de notification par courrier électronique envoyée aux utilisateurs qui sont spécifiés dans le champ envoyé cette alerte à (et répertoriés sous destinataires de la page **alertes d'activité** ) dans le &amp; Centre de sécurité et de conformité. **** 
    
    ![Exemple d'un message électronique notifcation envoyé pour une alerte d'activité](media/a5f91611-fae6-4fe9-82f5-58521a2e2541.png)
  
- Voici quelques activités de documents et de messagerie courantes pour lesquelles vous pouvez créer des alertes d'activité. Les tableaux décrivent l'activité, le nom de l'activité pour laquelle créer une alerte et le nom du groupe d'activités dans lequel l'activité est répertoriée dans la liste déroulante **activités** . Pour afficher la liste complète des activités pour lesquelles vous pouvez créer des alertes d'activité, reportez-vous à la section «activités auditées» dans la rubrique [Search the Audit Log in the Office 365 Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities).
    
    > [!TIP]
    > Vous pouvez créer une alerte d'activité pour une seule activité effectuée par un utilisateur. Vous pouvez également créer une alerte activité qui effectue le suivi de plusieurs activités effectuées par un ou plusieurs utilisateurs. 
  
    Le tableau suivant répertorie certaines activités courantes liées aux documents dans SharePoint ou OneDrive entreprise.
    
    |**Lorsqu'un utilisateur effectue cette opération...**|**Créer une alerte pour cette activité**|**Groupe d'activités**|
    |:-----|:-----|:-----|
    |Affiche un document sur un site.  <br/> |Fichier accédé  <br/> |Activités de fichiers et de dossiers  <br/> |
    |Modifie ou modifie un document.  <br/> |Fichier modifié  <br/> |Activités de fichiers et de dossiers  <br/> |
    |Partage un document avec un utilisateur en dehors de votre organisation.  <br/> |Partager un fichier, un dossier ou un site  <br/> Et  <br/> Invitation de partage créée  <br/> Pour plus d'informations, reportez-vous à [la rubrique utiliser l'audit de partage dans le journal d'audit Office 365](use-sharing-auditing.md).  <br/> |Activités de partage et d'accès aux demandes  <br/> |
    |Charge ou télécharge un document.  <br/> |Fichier téléchargé  <br/> Et/ou  <br/> Fichier téléchargé  <br/> |Activités de fichiers et de dossiers  <br/> |
    |Modifie les autorisations d'accès à un site.  <br/> |Autorisations de site modifiées  <br/> |Activités d'administration de site  <br/> |

    Le tableau suivant répertorie certaines activités courantes liées aux courriers électroniques dans Exchange Online.

    |**Lorsqu'un utilisateur effectue cette opération...**|**Créer une alerte pour cette activité**|**Groupe d'activités**|
    |:-----|:-----|:-----|
    |Supprime définitivement un message électronique de sa boîte aux lettres.  <br/> |Messages supprimés de la boîte aux lettres  <br/> | Activités de boîte aux lettres Exchange  <br/> |
    |Envoie un message électronique à partir d'une boîte aux lettres partagée.  <br/> |Message envoyé à l'aide des autorisations Envoyer en tant que  <br/> Et  <br/> Message envoyé à l'aide des autorisations Envoyer de la part de  <br/> | Activités de boîte aux lettres Exchange  <br/> |
   
- Vous pouvez également utiliser les cmdlets **New-ActivityAlert** et **Set-ActivityAlert** dans le &amp; Centre de sécurité conformité PowerShell pour créer et modifier des alertes d'activité. Gardez les éléments suivants à l'esprit si vous utilisez ces cmdlets pour créer ou modifier des alertes d'activité: 
    
  - Si vous utilisez une applet de commande pour ajouter une activité à l'alerte qui n'est pas répertoriée dans la liste déroulante **activités** , un message s'affiche dans sur la page de propriétés de l'alerte indiquant «cette alerte comporte des opérations personnalisées qui ne sont pas répertoriées dans le sélecteur». 
    
  - Une bonne raison d'utiliser les applets de commande pour créer ou modifier une alerte activité consiste à envoyer des notifications par courrier électronique à une personne extérieure à votre organisation. Cet utilisateur externe sera répertorié dans la liste des destinataires de l'alerte. Toutefois, si vous supprimez cet utilisateur externe de l'alerte, il ne peut pas être ajouté à nouveau à l'alerte en utilisant la page Modifier &amp; l' **alerte** du centre de sécurité et de conformité. Vous devrez rajouter l'utilisateur externe à l'aide de la cmdlet **Set-ActivityAlert** ou utiliser l'applet de commande **New-ActivityAlert** pour ajouter le même utilisateur (ou un autre) à une nouvelle alerte. 
    
  

