---
title: Appliquer automatiquement une étiquette sensibilité au contenu
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
description: Lorsque vous créez une étiquette de critère de diffusion, vous pouvez affecter automatiquement une étiquette à un document ou message électronique ou vous pouvez inviter les utilisateurs pour sélectionner l’étiquette que vous recommandez.
ms.openlocfilehash: 5165e9c7bd674046f6a3f3a9d1f1eeedc35f931e
ms.sourcegitcommit: 44cea06d4b007988cadc1e9de2d5ef601f1b3863
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "29760765"
---
# <a name="apply-a-sensitivity-label-to-content-automatically"></a>Appliquer automatiquement une étiquette sensibilité au contenu

Lorsque vous créez une étiquette de sensibilité, vous pouvez affecter automatiquement une étiquette à un document ou message électronique ou vous pouvez inviter les utilisateurs pour sélectionner l’étiquette que vous recommandez.

La possibilité d’appliquer automatiquement des étiquettes à du contenu est importante pour les raisons suivantes :

- Vous n’avez pas besoin de former les utilisateurs concernant l’ensemble de vos classifications.

- Vous n’avez pas à dépendre des utilisateurs pour classer correctement tout le contenu.

- Les utilisateurs n’ont plus à connaître les stratégies de gouvernance des données : à la place, ils peuvent se concentrer sur leur travail.

> [!NOTE]
> La capacité à appliquer automatiquement des étiquettes nécessite un abonnement Azure Information Protection P2. Pour utiliser cette fonctionnalité, vous devez [télécharger et installer le client Azure Information Protection unifié étiquetage](https://docs.microsoft.com/fr-FR/azure/information-protection/rms-client/install-unifiedlabelingclient-app). Nous travaillons à la prise en charge native pour cette fonctionnalité dans les applications Office, afin qu’elle n’exige pas que le client Azure Information Protection unifié création d’étiquettes. Par ailleurs, le client de création d’étiquettes unifié ne s’exécute que sur Windows, afin que cette fonctionnalité ne soit pas encore prise en charge sur Mac, iOS et Android.

![Options pour les étiquettes de la sensibilité d’étiquetage automatique](media/Sensitivity_labels_Auto_labeling_options.png)

## <a name="apply-a-sensitivity-label-automatically-based-on-conditions"></a>Application d’une étiquette automatiquement en fonction des conditions

L’une des fonctionnalités les plus puissantes des étiquettes de sensibilité est la possibilité de les appliquer automatiquement au contenu qui remplit certaines conditions. Dans ce cas, les membres de votre organisation ne doivent pas appliquer ces étiquettes de sensibilité: Office 365 s’en charge à leur place.
   
Vous pouvez choisir d’appliquer automatiquement des étiquettes de sensibilité au contenu quand celui-ci inclut des types spécifiques d’informations sensibles. Lorsque vous configurez une étiquette de sensibilité à être appliquée automatiquement, vous voyez la même liste de types d’informations sensibles comme lorsque vous créez une stratégie prévention contre la perte de données. Par conséquent vous pouvez, par exemple, appliquer automatiquement une étiquette hautement confidentielle à tout contenu qui contient des informations d’identification personnelle des clients (PII) telles que les numéros de sécurité sociale ou carte bancaire. 

![Nombre d’instances et options de précision des résultats](media/Sensitivity_labels_instance_count_match_accuracy.png)

Après avoir choisi vos types d’informations sensibles sections, vous pouvez affiner votre condition en modifiant le nombre d’instances ou précision de correspondance. Pour plus d’informations, voir [Optimisation des règles afin de les rendre plus facile ou plus difficile pour correspondre à](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).

De plus, vous pouvez choisir si une condition doit détecter les types sensibles relatifs ou simplement l’un d’eux. Et pour rendre vos conditions plus flexible ou complexes, vous pouvez ajouter des groupes et utiliser les opérateurs logiques entre les groupes. Pour plus d’informations, voir [Opérateurs logiques et regroupement](data-loss-prevention-policies.md#grouping-and-logical-operators).

Lorsqu’une étiquette de critère de diffusion est automatiquement appliquée, l’utilisateur voit une notification dans leur application Office. Ils peuvent choisir **OK**pour fermer la notification.

![Notification dont un document disposait d’une étiquette appliquée automatiquement](media/sensitivity_labels_msg_doc_was_auto_labeled.PNG)

## <a name="recommend-that-the-user-apply-a-sensitivity-label"></a>Recommandé que l’utilisateur applique une étiquette de critère de diffusion

Si vous préférez, au lieu d’appliquer une étiquette sensibilité automatiquement au contenu, vous pouvez recommander à vos utilisateurs qu’elles s’appliquent à l’étiquette. Cette option permet à vos utilisateurs d’accepter la classification et toute protection associée ou faire disparaitre la valeur recommandée si l’étiquette n’est pas appropriée à leur document ou message électronique.

Notez que les étiquettes recommandées sont prises en charge dans Word, PowerPoint et Excel (et requièrent que l’étiquette client Proteciton Informations Azure unifiée soit bien installée). Nous travaillons à la prise en charge pour les étiquettes recommandées dans Outlook.

![Option pour recommander une étiquette de la sensibilité à des utilisateurs](media/Sensitivity_labels_Recommended_label_option.png)

Voici un exemple d’une invite de commandes lorsque vous configurez une condition à appliquer une étiquette comme action recommandée avec un Conseil de stratégie personnalisé. Vous pouvez choisir quel texte s’affiche dans le Conseil de stratégie.

![Invite à appliquer une étiquette recommandée](media/Sensitivity_label_Prompt_for_required_label.png)

## <a name="how-automatic-or-recommended-labels-are-applied"></a>Comment les étiquettes automatiques ou recommandées sont appliquées

- L’étiquetage automatique s’applique à Word, Excel et PowerPoint lorsque les documents sont enregistrés et dans Outlook lorsque des messages électroniques sont envoyés. Ces conditions détectent les informations sensibles dans le corps de texte dans des documents et messages électroniques et aux en-têtes et pieds de page, mais pas dans la ligne d’objet ou des pièces jointes de message électronique.

- Vous ne pouvez pas utiliser la classification automatique pour les documents et messages électroniques qui ont été précédemment intitulés manuellement ou précédemment automatiquement libellés avec une classification une version ultérieure. N’oubliez pas, un document ou un courrier électronique peut avoir uniquement une seul niveau de confidentialité étiquette (outre une étiquette unique rétention).

- La classification recommandée s’applique à Word, Excel et PowerPoint lorsque les documents sont enregistrés. Nous travaillons sur la prise en charge d’étiquetage recommandée dans Outlook.

- Vous ne pouvez pas utiliser la classification recommandée pour les documents qui ont été précédemment libellés avec une classification une version ultérieure. Dans ce cas, lorsque le contenu est déjà libellé avec une classification supérieure, l’utilisateur ne verra pas l’invite de commandes avec la recommandation et le conseil de stratégie.

## <a name="how-multiple-conditions-are-evaluated-when-they-apply-to-more-than-one-label"></a>Comment plusieurs conditions sont évaluées lorsqu’elles s’appliquent à plus d’une étiquette

Les étiquettes sont classées pour évaluation en fonction de leur position que vous spécifiez dans la stratégie: l’étiquette positionné a tout d’abord la position la plus basse (au moins sensible) et l’étiquette positionnée a dernière position plus élevée (plus sensible). Pour plus d’informations sur la priorité, voir [Priorité étiquettes (ordre aspects importants)](sensitivity-labels.md#label-priority-order-matters).