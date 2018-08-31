---
title: Créer des alertes de l’activité de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/7/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- BCS160
- MET150
ms.assetid: 72bbad69-035b-4d33-b8f4-549a2743e97d
description: Ajouter et gérer les alertes d’activité de la sécurité &amp; centre de conformité afin que Office 365 vous envoyer des notifications par e-mail lorsque les utilisateurs effectuent des activités spécifiques dans Office 365.
ms.openlocfilehash: 409c1ff4c7fdd0d2d071bdb2eab08ec49357ed8a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528495"
---
# <a name="create-activity-alerts-in-the-office-365-security-amp-compliance-center"></a>Créer des alertes de l’activité de sécurité Office 365 &amp; centre de conformité

Vous pouvez créer une alerte d’activité qui vous envoie une notification par courrier électronique lorsque les utilisateurs effectuent des activités spécifiques dans Office 365. Alertes d’activité sont similaires à la recherche pour les événements dans le journal d’audit d’Office 365, sauf que vous allez être envoyé un message électronique lorsqu’un événement d’une activité que vous avez créé une alerte se produit. 
  
 **Pourquoi utiliser des alertes d’activité au lieu de la recherche dans le journal d’audit ?** Il peut y avoir certains types d’activité ou effectuée par des utilisateurs spécifiques que vous souhaitez vraiment savoir à propos de. Au lieu de devoir n’oubliez pas de recherche dans le journal d’audit pour ces activités, vous pouvez utiliser des alertes d’activité pour que Office 365 vous envoyer un message électronique lorsque les utilisateurs effectuent les activités. Par exemple, vous pouvez créer une alerte d’activité pour vous signaler si un utilisateur supprime des fichiers dans SharePoint ou vous pouvez créer une alerte pour vous avertir lorsqu’un utilisateur supprime définitivement des messages à partir de leur boîte aux lettres. La notification par courrier électronique envoyée consacrée des informations sur l’activité qui a été effectuée et que l’utilisateur qui a effectué son. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être affecté au rôle de Configuration de l’organisation dans la sécurité &amp; centre de conformité pour gérer les alertes d’activité. Par défaut, ce rôle est attribué pour les groupes de rôles d’administrateur de la conformité et de gestion de l’organisation. Pour plus d’informations sur l’ajout de membres aux groupes de rôles, consultez la rubrique [donner aux utilisateurs l’accès à l’Office 365 Security &amp; centre de conformité](grant-access-to-the-security-and-compliance-center.md).
    
- Vous (ou un autre administrateur) devez d’abord activer la journalisation d’audit pour votre organisation avant de pouvoir commencer à utiliser les alertes de l’activité. Pour ce faire, cliquez simplement sur **Démarrer l’enregistrement d’utilisateur et des activités d’administration** dans la page **alertes d’activité** . (Si vous ne voyez pas ce lien, l’audit a déjà été activé pour votre organisation.) Vous pouvez également activer l’audit dans la page de **recherche des journaux d’Audit** de sécurité &amp; centre de conformité (atteindre **recherche &amp; enquête** \> **recherche des journaux d’Audit**). Vous ne devez cela qu’une seule fois pour votre organisation.
    
- Vous pouvez utiliser la page **des alertes** de sécurité &amp; centre de conformité pour créer des alertes uniquement pour les activités effectuées par les utilisateurs qui figurent dans le carnet d’adresses de votre organisation. Vous ne pouvez pas utiliser cette page pour créer des alertes pour les activités effectuées par des utilisateurs externes. 
    
- Afficher les [informations plus](#more-information) section pour obtenir la liste des scénarios courants (et l’activité spécifique à surveiller) que vous pouvez créer des alertes pour. 
    
- Vous pouvez créer des alertes pour les mêmes opérations que vous pouvez rechercher dans le journal d’audit d’Office 365. 
    
## <a name="create-an-activity-alert"></a>Créer une alerte de l’activité

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche, cliquez sur **alertes**, puis cliquez sur **Gérer les alertes**.
    
4. Dans la page **alertes d’activité** , cliquez sur **Ajouter une alerte**.
    
    ![Ajout d’une alerte de l’activité](media/53888bd5-9fa2-4398-8ccc-1a9dc72517ac.png)
  
5. Renseignez les champs suivants pour créer une alerte :
    
    a **nom** : tapez le nom de l’alerte. Noms d’alerte doivent être uniques au sein de votre organisation.
    
    b. **Description** (facultatif) : décrire l’alerte, telles que les activités et le suivi est activés, les utilisateurs et les utilisateurs que les notifications de messagerie sont envoyées à. Descriptions fournissent un moyen simple et rapide pour décrire la finalité de l’alerte à d’autres administrateurs.
    
    c. **envoi cette alerte lorsque** - cliquez sur **Envoyer cette alerte quand** , puis configurer ces deux champs :
    
    - **Activités** - cliquez sur la liste déroulante liste pour afficher les activités que vous pouvez créer une alerte. Il s’agit de la même liste des activités qui s’affiche lorsque vous recherchez le journal d’audit de Office 365. Vous pouvez sélectionner une ou plusieurs activités spécifiques ou vous pouvez cliquer sur le nom du groupe activité à sélectionner toutes les activités dans le groupe. Pour obtenir une description de ces activités, consultez la section « Audités activités » de la [recherche, ouvrez une session de l’audit dans la sécurité pour Microsoft Office 365 et le centre de conformité](search-the-audit-log-in-security-and-compliance.md#audited-activities). Lorsqu’un utilisateur effectue une des actions que vous avez ajoutée à l’alerte, une notification par courrier électronique est envoyée. 
    
     - **Utilisateurs** : Activez cette case, puis sélectionnez un ou plusieurs utilisateurs. Si les utilisateurs dans cette zone de réaliser les opérations que vous avez ajouté à la zone **activités** , une alerte est envoyée. Rien dans la zone **utilisateurs** d’envoyer une alerte lorsque tous les utilisateurs de votre organisation exécute les activités de l’alerte. 
    
    d. **Envoyer cette alerte** - cliquez sur **Envoyer cette alerte**, puis cliquez dans la zone de **destinataires** et tapez un nom pour ajouter un utilisateur qui recevront une notification par courrier électronique lorsqu’un utilisateur (spécifié dans la zone **utilisateurs** ) effectue une activité (spécifié dans le Zone **activités** ). Notez que vous êtes ajouté à la liste des destinataires par défaut. Vous pouvez supprimer votre nom de cette liste.
    
6. Cliquez sur **Enregistrer** pour créer l’alerte. 
    
    La nouvelle alerte s’affiche dans la liste dans la page **alertes d’activité** . 
    
    ![Une liste d’alertes s’affiche dans la page d’alertes activité de la sécurité &amp; centre de conformité](media/02b774f2-1719-41de-bbc9-5e5b7576f335.png)
  
    L’état de l’alerte est défini **sur**. Notez que les destinataires qui a reçu une notification par courrier électronique lors de l’envoi d’une alerte sont également répertoriées. 
  
## <a name="turn-off-an-activity-alert"></a>Désactiver une alerte de l’activité

Vous pouvez désactiver une alerte d’activité pour qu’une notification par courrier électronique n’est pas envoyée. Après la désactivation de l’alerte d’activité, il est toujours affiché dans la liste des alertes d’activité pour votre organisation, et vous pouvez toujours afficher ses propriétés.
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche, cliquez sur **alertes**, puis cliquez sur **Gérer les alertes d’activité**.
    
4. Dans la liste des alertes pour votre organisation, cliquez sur l’alerte que vous souhaitez désactiver.
    
5. Dans la page **Modifier l’alerte** , cliquez sur le bouton bascule **sur** pour modifier le statut à **désactiver**, puis cliquez sur **Enregistrer**.
    
    L’état de l’alerte dans les pages d’alertes activité est défini sur **désactivé**. 
    
Pour activer une alerte de l’activité, simplement Répétez ces étapes et cliquez sur le bouton bascule **désactiver** pour modifier l’état **activé**.
  
## <a name="more-information"></a>Plus d'informations

- Voici un exemple de la notification de courrier électronique est envoyé aux utilisateurs qui sont spécifiés dans le Sent cette alerte au champ (et répertoriés sous **destinataires** dans la page **alertes d’activité** ) dans la sécurité &amp; centre de conformité. 
    
    ![Exemple d’une notifications de courrier électronique envoyée par une alerte de l’activité](media/a5f91611-fae6-4fe9-82f5-58521a2e2541.png)
  
- Vous trouverez ici des alertes pour des activités courantes de document et au courrier électronique que vous pouvez créer une activité. Les tableaux décrit l’activité et le nom de l’activité pour créer une alerte pour le nom du groupe d’activités répertorié sous l’activité dans la liste déroulante des **activités** . Pour afficher une liste complète des activités que vous pouvez créer des alertes d’activité pour, consultez la section « Audités activités » de la [recherche, ouvrez une session de l’audit dans la sécurité pour Microsoft Office 365 et le centre de conformité](search-the-audit-log-in-security-and-compliance.md#audited-activities).
    
    > [!TIP]
    > Vous pouvez souhaiter créer une alerte de l’activité pour qu’une activité réalisée par les utilisateurs. Ou vous pouvez souhaiter créer une alerte de l’activité qui effectuent le suivi de plusieurs activités effectuées par parents ou d’un utilisateur. 
  
    Le tableau suivant répertorie certaines activités liées aux documents courants dans SharePoint ou OneDrive for Business.
    
    |**Lorsqu’un utilisateur effectue ceci...**|**Créer une alerte pour cette activité**|**Groupe d’activités**|
    |:-----|:-----|:-----|
    |Affiche un document sur un site.  <br/> |Accès aux fichiers  <br/> |Activités de fichier et de dossier  <br/> |
    |Modifie ou modifie un document.  <br/> |Fichier modifié  <br/> |Activités de fichier et de dossier  <br/> |
    |Partage un document avec un utilisateur à l’extérieur de votre organisation.  <br/> |Partage de fichier, dossier ou site  <br/> Et  <br/> Invitation de partage créée  <br/> Pour plus d’informations, voir [utiliser le partage d’audit dans le journal d’audit d’Office 365](use-sharing-auditing.md).  <br/> |Activités de demande de partage et d’accès  <br/> |
    |Transfère ou télécharge un document.  <br/> |Fichier téléchargé  <br/> Et/ou  <br/> Fichier téléchargé  <br/> |Activités de fichier et de dossier  <br/> |
    |Modifie les autorisations d’accès à un site.  <br/> |Autorisations de site modifié  <br/> |Activités de l’administration de site  <br/> |

    Le tableau suivant répertorie certaines activités courantes liées à la messagerie dans Exchange Online.

    |**Lorsqu’un utilisateur effectue ceci...**|**Créer une alerte pour cette activité**|**Groupe d’activités**|
    |:-----|:-----|:-----|
    |Définitivement supprime (vide) un message électronique de message à partir de leur boîte aux lettres.  <br/> |Messages purgés de boîte aux lettres  <br/> | Activités de boîte aux lettres Exchange  <br/> |
    |Envoie un message électronique à partir d’une boîte aux lettres partagée.  <br/> |Envoyé le message à l’aide des autorisations Envoyer en tant que  <br/> Et  <br/> Envoyé à l’aide des autorisations Envoyer de la part de message  <br/> | Activités de boîte aux lettres Exchange  <br/> |
   
- Vous pouvez également utiliser les applets de commande **New-ActivityAlert** et **Set-ActivityAlert** de la sécurité &amp; PowerShell du centre de conformité pour créer et modifier des alertes d’activité. Gardez les éléments suivants à l’esprit si vous utilisez ces applets de commande pour créer ou modifier des alertes d’activité : 
    
  - Si vous utilisez une applet de commande pour ajouter une activité à l’alerte qui n’est pas répertorié dans la liste déroulante des **activités** , un message s’affiche dans sur la page de propriétés de l’alerte indiquant « cette alerte a des opérations personnalisées non répertoriées dans le sélecteur de ». 
    
  - Une bonne raison d’utiliser les applets de commande pour créer ou modifier une alerte d’activité consiste à envoyer des notifications par courrier électronique à une personne extérieure à votre organisation. Cet utilisateur externe apparaît dans la liste des destinataires de l’alerte. Mais si vous supprimez cet utilisateur externe à partir de l’alerte, que l’utilisateur ne peut pas être ajouté à l’alerte de nouveau à l’aide de la page **Modifier l’alerte** de sécurité &amp; centre de conformité. Vous allez ont rajouter l’utilisateur externe à l’aide de l’applet de commande **Set-ActivityAlert** , ou utilisez l’applet de commande **New-ActivityAlert** pour ajouter l’utilisateur externe (ou plusieurs) à une alerte. 
    
  

