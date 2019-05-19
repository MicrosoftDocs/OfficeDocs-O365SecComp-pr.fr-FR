---
title: Utilisation des règles de flux de courrier pour définir le seuil de probabilité de courrier indésirable (SCL) dans les messages
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à définir la valeur SCL des messages dans Exchange Online Protection.
ms.openlocfilehash: c997f321ed14cddfa430c43e6de42f36934c642b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157966"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a>Utilisation des règles de flux de courrier pour définir le seuil de probabilité de courrier indésirable (SCL) dans les messages

Vous pouvez créer une règle de flux de messagerie (également appelée règle de transport) qui définit le seuil de probabilité de courrier indésirable (SCL) d’un message électronique. Le SCL mesure la probabilité qu'un message soit un courrier indésirable. Le courrier indésirable représente les messages électroniques non sollicités (et généralement indésirables). Le service prend différentes mesures en ce qui concerne le message en fonction de la notation SCL. Par exemple, vous pouvez contourner le filtrage de contenu de courrier indésirable pour les messages envoyés par des membres de votre organisation, car vous pensez qu'un message envoyé en interne par un collègue n'est pas un courrier indésirable. La définition de la valeur SCL d’un message à l’aide de règles de flux de messagerie vous permet de contrôler le traitement du courrier indésirable. 
  
 **Ce qu'il faut savoir avant de commencer**
  
- Durée estimée de la procédure : 10 minutes.
    
- You need to be assigned permissions before you can perform this procedure or procedures. Pour voir les autorisations qui vous sont nécessaires, consultez l’entrée «règles de flux de messagerie» dans [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) ou [autorisations des fonctionnalités dans EOP](eop/feature-permissions-in-eop.md). 
    
- Pour obtenir des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, reportez-vous à l’article **Raccourcis clavier dans le Centre d’administration Exchange**.
    
### <a name="to-create-a-mail-flow-rule-that-sets-the-scl-of-a-message"></a>Pour créer une règle de flux de messagerie qui définit la valeur SCL d’un message

1. Dans le Centre d'administration Exchange (CAE), choisissez **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur **Nouveau**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une règle**.
    
3. Indiquez le nom de la règle.
    
4. Choisissez **Plus d'options** et, sous **Appliquer cette règle si**, indiquez une condition qui déclenchera l'action que vous allez définir pour cette règle (c'est-à-dire la valeur SCL).
    
    Par exemple, vous pouvez définir **L'expéditeur** \> **est interne/externe** et, dans la boîte de dialogue **Sélectionner l'emplacement de l'expéditeur**, choisir **À l'intérieur de l'organisation**, puis cliquer sur **OK**.<br/>
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
    > Pour plus d’informations sur les propriétés supplémentaires que vous pouvez sélectionner ou spécifier pour cette règle, reportez-vous [à la rubrique utiliser le centre d’administration Exchange pour créer des règles de flux de messagerie](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures#use-the-eac-to-create-mail-flow-rules). 
  
## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vous assurer que cette procédure fonctionne correctement, envoyez un message électronique à un membre de votre organisation et vérifiez que l'action effectuée sur le message correspond à celle prévue. Par exemple, si vous avez **défini le seuil de probabilité de courrier indésirable (SCL)** sur **Contourner le filtrage du courrier indésirable**, le message doit être envoyé vers la boîte de réception du destinataire spécifié. Cependant, si vous avez **défini le seuil de probabilité de courrier indésirable (SCL)** sur **9** et que l'action **Probabilité élevée de courrier indésirable** pour les stratégies de filtre de contenu applicables consiste à déplacer le message vers le dossier Courrier indésirable, le message doit être envoyé vers le dossier Courrier indésirable du destinataire spécifié. 
  

