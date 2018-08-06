---
title: Use mail flow rules to set the spam confidence level (SCL) in messages
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
description: Vous pouvez créer une règle de transport qui définit le seuil de probabilité de courrier indésirable (SCL) d'un message électronique. Le SCL mesure la probabilité qu'un message soit un courrier indésirable. Le courrier indésirable représente les messages électroniques non sollicités (et généralement indésirables). Le service prend différentes mesures en ce qui concerne le message en fonction de la notation SCL. Par exemple, vous pouvez contourner le filtrage de contenu de courrier indésirable pour les messages envoyés par des membres de votre organisation, car vous pensez qu'un message envoyé en interne par un collègue n'est pas un courrier indésirable. L'utilisation des règles de transport pour définir la valeur SCL d'un message vous offre un contrôle accru en matière de gestion du courrier indésirable.
ms.openlocfilehash: ad89230dac9de668488b40090d70d2b697a86edd
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026731"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a>Use mail flow rules to set the spam confidence level (SCL) in messages

Vous pouvez créer une règle de transport qui définit le seuil de probabilité de courrier indésirable (SCL) d'un message électronique. Le SCL mesure la probabilité qu'un message soit un courrier indésirable. Le courrier indésirable représente les messages électroniques non sollicités (et généralement indésirables). Le service prend différentes mesures en ce qui concerne le message en fonction de la notation SCL. Par exemple, vous pouvez contourner le filtrage de contenu de courrier indésirable pour les messages envoyés par des membres de votre organisation, car vous pensez qu'un message envoyé en interne par un collègue n'est pas un courrier indésirable. L'utilisation des règles de transport pour définir la valeur SCL d'un message vous offre un contrôle accru en matière de gestion du courrier indésirable. 
  
 **Ce qu'il faut savoir avant de commencer**
  
- Durée estimée de la procédure : 10 minutes.
    
- Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez l’entrée « Règles de Transport » dans [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) ou les [autorisations des fonctionnalités dans EOP](eop/feature-permissions-in-eop.md). 
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a>Pour créer une règle de transport définissant la valeur SCL d'un message

1. Dans le Centre d'administration Exchange (CAE), choisissez **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur **Nouveau**![Icône Ajouter](media/ITPro-EAC-AddIcon.png), puis sélectionnez **Créer une règle**.
    
3. Indiquez le nom de la règle.
    
4. Choisissez **Plus d'options** et, sous **Appliquer cette règle si**, indiquez une condition qui déclenchera l'action que vous allez définir pour cette règle (c'est-à-dire la valeur SCL).
    
    Par exemple, vous pouvez définir **L'expéditeur** \> **est interne/externe** et, dans la boîte de dialogue **Sélectionner l'emplacement de l'expéditeur**, choisir **À l'intérieur de l'organisation**, puis cliquer sur **OK**.</br>
    ![Sélectionner l'emplacement de l'expéditeur](media/EOP-ETR-SetSCL-1.jpg)
  
5. Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.
  
6. Dans la boîte de dialogue **spécifier la valeur SCL**, sélectionnez l'une des valeurs suivantes, puis cliquez sur **OK**:
    
  - **Contourner le filtrage du courrier indésirable**: cette option définit la valeur SCL sur -1, ce qui signifie qu'aucun filtrage de contenu ne sera effectué. 
    
  - **0-4**: lorsque vous définissez la valeur SCL sur l'une de ces valeurs, le message est transmis au filtre de contenu en vue d'un traitement supplémentaire. 
    
  - **5, 6**: lorsque vous définissez la valeur SCL sur l'une de ces valeurs, l'action spécifiée pour **Courrier indésirable** dans les stratégies de filtre de contenu applicables est appliquée. Par défaut, l'action consiste à envoyer le message vers le dossier Courrier indésirable du destinataire. 
    
  - **7-9**: lorsque vous définissez la valeur SCL sur l'une de ces valeurs, l'action spécifiée pour **Probabilité élevée de courrier indésirable** dans les stratégies de filtre de contenu applicables est appliquée. Par défaut, l'action consiste à envoyer le message vers le dossier Courrier indésirable du destinataire. 
    
    Pour plus d'informations sur la configuration des stratégies de filtre de contenu, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Pour plus d'informations sur les valeurs SCL du service, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).
    
7. Spécifiez des propriétés supplémentaires pour la règle, puis choisissez **enregistrer**.
    
    > [!TIP]
    > Pour plus d'informations sur les propriétés supplémentaires que vous pouvez sélectionner ou spécifier pour cette règle, voir [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC). 
  
## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vous assurer que cette procédure fonctionne correctement, envoyez un message électronique à un membre de votre organisation et vérifiez que l'action effectuée sur le message correspond à celle prévue. Par exemple, si vous avez **défini le seuil de probabilité de courrier indésirable (SCL)** sur **Contourner le filtrage du courrier indésirable**, le message doit être envoyé vers la boîte de réception du destinataire spécifié. Cependant, si vous avez **défini le seuil de probabilité de courrier indésirable (SCL)** sur **9** et que l'action **Probabilité élevée de courrier indésirable** pour les stratégies de filtre de contenu applicables consiste à déplacer le message vers le dossier Courrier indésirable, le message doit être envoyé vers le dossier Courrier indésirable du destinataire spécifié. 
  

