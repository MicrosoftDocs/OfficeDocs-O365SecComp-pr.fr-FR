---
title: Types d’informations sensibles personnalisés pour la protection contre la perte de données (DLP)
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/23/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Obtenez une vue d’ensemble des types d’informations sensibles personnalisés pour la protection contre la perte de données (DLP).
ms.openlocfilehash: 3c3acceb23fe74d22b9e952bf5dc76d9ed6eefd9
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230778"
---
# <a name="custom-sensitive-information-types"></a>Types d’informations sensibles personnalisés

## <a name="overview"></a>Vue d’ensemble

Office 365 inclut différents types d’informations sensibles intégrés prêts à l’emploi, par exemple, pour la [protection contre la perte de données](data-loss-prevention-policies.md) (DLP) ou avec [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security). Les types d’informations sensibles intégrés peuvent aider à identifier et à protéger des numéros de carte de crédit, de compte bancaire, de passeport et autres sur la base de modèles définis par une expression régulière (regex) ou une fonction. Pour en savoir plus, voir [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).

Mais que se passe-t-il si vous devez identifier et protéger un autre type d’informations sensibles, par exemple, des ID d’employé ou des numéros de projet, à l’aide d’un format spécifique de votre organisation ? Vous pouvez créer un type d’informations sensibles personnalisé.

Les éléments fondamentaux d’un type d’informations sensibles personnalisé sont :

- **Modèle principal** : numéros d’identification d’employé, numéros de projet, etc. Cela est généralement identifié par une expression régulière (RegEx) mais il peut aussi s’agir d’une liste de mots clés.

- **Preuves supplémentaires** : supposons que vous recherchez un numéro d’identification d’employé à neuf chiffres. Tous les numéros à neuf chiffres ne sont pas des numéros d’identification d’employé, donc vous pouvez rechercher un texte supplémentaire : les mots clés comme « employé », « badge », « ID » ou d’autres modèles de texte suivant d’autres expressions régulières. Cette preuve (également appelée preuve _justificative_ ou _probante_) augmente la probabilité que le nombre à neuf chiffres trouvé dans le contenu est réellement un numéro d’identification d’employé.

- **Proximité de caractère** : il est logique que plus le modèle principal et la preuve justificative sont proches, plus le contenu détecté a des chances d’être ce que vous recherchez. Vous pouvez spécifier la distance de caractère entre le modèle principal et la preuve justificative (également appelée _fenêtre de proximité_) comme illustré dans le diagramme suivant :

    ![Diagramme de la fenêtre de proximité et de preuves probantes](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- **Niveau de confiance** : plus la preuve que vous possédez est justificative, plus la probabilité qu’un résultat contienne les informations sensibles que vous recherchez est élevée. Vous pouvez affecter des niveaux de confiance supérieurs pour les correspondances détectées en utilisant plus de preuves.

  Lorsqu’il est satisfait, un modèle renvoie un nombre et un niveau de confiance, que vous pouvez utiliser dans les conditions dans votre stratégie DLP. Lorsque vous ajoutez une condition de détection d’un type d’informations sensibles à une stratégie DLP, vous pouvez modifier le nombre et le niveau de confiance comme illustré dans le diagramme suivant :

    ![Nombre d’instances et options de précision de correspondance](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

## <a name="creating-custom-sensitive-information-types"></a>Création de types d’informations sensibles personnalisés

Pour créer des types d’informations sensibles personnalisés dans le Centre de sécurité et conformité, vous disposez des options suivantes :

- **Utiliser EDM** (nouveau) Vous pouvez configurer des types d’informations sensibles personnalisés à l’aide d’une classification de correspondance exacte des données (EDM, Exact Data Match). Cette méthode vous permet de créer un type d’informations sensibles dynamique à l’aide d’une base de données sécurisée que vous pouvez actualiser régulièrement. Voir l’article sur la [création d’un type d’informations sensibles personnalisé à l’aide d’une classification de correspondance exacte des données (préversion)](create-custom-sensitive-info-type-edm.md).

- **Utiliser PowerShell** vous pouvez configurer des types d’informations sensibles personnalisés à l’aide de PowerShell. Bien que cette méthode soit plus complexe que celle de l’interface utilisateur, elle offre davantage d’options de configuration. Voir [Créer un type d’informations sensibles personnalisé dans l’interface PowerShell du Centre de sécurité et conformité](create-a-custom-sensitive-information-type-in-scc-powershell.md).

- **Utiliser l’interface utilisateur** Vous pouvez configurer un type d’informations sensibles personnalisé à l’aide de l’interface utilisateur du Centre de sécurité et de conformité. Cette méthode vous permet d’utiliser des expressions régulières, des mots clés et des dictionnaires de mots clés. Pour en savoir plus, voir [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).



