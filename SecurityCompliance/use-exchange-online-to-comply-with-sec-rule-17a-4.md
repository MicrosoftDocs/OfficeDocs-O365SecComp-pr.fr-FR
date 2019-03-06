---
title: Utiliser Exchange Online et le centre de sécurité et conformité pour se conformer à la règle SEC 17a-4
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: Cohasset Associates a validé que lorsque Exchange Online et le centre de sécurité et conformité sont configurés comme recommandé, ils répondent aux exigences de stockage pertinentes de règle CFTC 1.31(c)-(d), FINRA règle 4511 et SEC règle 17 a-4. Vous pouvez télécharger l’évaluation.
ms.openlocfilehash: b0c2a54aab8f011605a285d4dabfb4091612b17a
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410509"
---
# <a name="use-exchange-online-and-the-security--compliance-center-to-comply-with-sec-rule-17a-4"></a>Utiliser Exchange Online et le centre de sécurité et conformité pour se conformer à la règle SEC 17a-4

Si votre organisation doit respecter les normes réglementaires pour conserver vos données, le Centre de Conformité et Sécurité Office 365 fournit des fonctionnalités pour gérer le cycle de vie de vos données dans Exchange Online. Cela inclut la possibilité de conserver, d’audit, rechercher et exporter vos données. Ces fonctionnalités sont suffisantes pour répondre aux besoins de la plupart des organisations.

Toutefois, certaines organisations dans des secteurs hautement réglementés sont soumises à des exigences réglementaires plus stricts. Par exemple, les institutions financières de tels que les banques ou les courtiers sont soumis aux règle 17 a-4 émis par Securities and Exchange Commission (SEC). La Règle 17 a-4 a des exigences spécifiques pour le stockage de données électroniques, y compris de nombreux aspects de la gestion des enregistrements telles que la durée, le format, la qualité, la disponibilité et la responsabilité de rétention des enregistrements.

Pour aider ces organisations à mieux comprendre comment le Centre de Sécurité et Conformité peut être utilisé pour répondre à leurs obligations légales pour Exchange Online. plus précisément par rapport à la configuration requise relative à la règle 17 a-4, nous avons publié une évaluation en partenariat avec Cohasset Associates.

Cohasset a validé que lorsque Exchange Online et le Centre de Sécurité et Conformité sont configurés comme recommandé, ils répondent aux exigences de stockage pertinentes de règle CFTC 1.31(c)-(d), la FINRA règle 4511 et la SEC règle 17 a-4.  Nous avons ciblé cet ensemble de règles car elles représentent les conseils de la plupart des conseils globalement pour la rétention des enregistrements pour les institutions financières.

## <a name="download-the-cohasset-assessment"></a>Télécharger l’évaluation Cohasset

Vous pouvez [télécharger ici l’évaluation Cohasset](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers).

![La page de titre de l’évaluation téléchargeable par Cohasset Associates](media/cohasset-associates-assessment.png)

## <a name="this-assessment-is-specific-to-exchange-online"></a>Cette évaluation est spécifique à Exchange Online

Notez que cette évaluation est spécifique à Exchange Online. L’évaluation n’inclut pas les autres services Office 365 tels que SharePoint Online ou OneDrive Entreprise, bien que nous envisageons la prise en charge dans ces services par rapport à SEC 17 a-4 à l’avenir.

Il est important de comprendre que Skype Entreprise et Teams stockent également des données dans Exchange Online.  Par conséquent, l’évaluation traite les messages de Skype Entreprise, le canal et les messages de conversation à partir de Teams.

## <a name="using-preservation-lock-is-key-to-the-recommended-configuration"></a>À l’aide de verrouillage de conservation est essentiel pour la configuration recommandée

Les secteurs d’activités hautement rigoureuses ont souvent besoin de stocker les communications électroniques afin de répondre à la configuration requise WORM (plusieurs lectures, écriture une seule fois). La configuration requise WORM dicte une solution de stockage dans lequel un enregistrement doit être :

- Conservée pendant une période de rétention obligatoire qui ne peut pas être raccourcie uniquement augmentée.
- Immuable, ce qui signifie que l’enregistrement ne peut pas être remplacée, supprimée ou modifiée pendant la période de rétention requise.

Dans Exchange Online, lorsqu’une[stratégie de rétention](retention-policies.md) est appliquée à la boîte aux lettres d’un utilisateur, tout contenu de l’utilisateur sera conservée en fonction de critères de la stratégie. En fait, si un utilisateur tente de supprimer ou modifier un message électronique, une copie du message électronique avant la modification est effectuée et conservée dans un emplacement sécurisé, masqué dans la boîte aux lettres de l’utilisateur. Les stratégies de rétention peuvent vous assurer qu’une organisation conserve les communications électroniques, mais ces stratégies peuvent être modifiées.

En plaçant un verrouillage de conservation dans une stratégie de rétention, une organisation garantit que la stratégie ne peut pas être modifiée. En fait, une fois un verrouillage de conservation est appliquée à une stratégie de rétention, les actions suivantes sont limitées :

- La période de rétention de la stratégie peut uniquement être accrue, elle ne raccourcie pas.
- Les utilisateurs peuvent être ajoutés à la stratégie, mais aucun utilisateur ne peut être supprimé.
- La stratégie de rétention ne peut pas être supprimée par un administrateur.

Le verrouillage de conservation peut vous aider à répondre aux exigences réglementaires SEC 17 a-4.

## <a name="how-to-set-up-preservation-lock"></a>Comment configurer le verrouillage de conservation

Vous pouvez verrouiller une stratégie de rétention à l’aide de PowerShell. Pour plus d’informations, voir [Verrouillage d’une stratégie de rétention](retention-policies.md#locking-a-retention-policy).

## <a name="known-limitations"></a>Limitations connues

Nous sommes conscients de quelques limitations importantes dans Exchange Online. Nous travaillons activement sur celles-ci et prévoyons de publier une prise en charge dans ces scénarios en juillet 2019:

- L’audit au niveau de l’élément n’est pas disponible dans les boîtes aux lettres de groupe Office 365.
- Les fils de communications ne sont pas disponibles pour les messages de conversation et le canal équipes.
- Les mentions j’aime ne sont pas conservées pour les messages de conversation et le canal équipes.
