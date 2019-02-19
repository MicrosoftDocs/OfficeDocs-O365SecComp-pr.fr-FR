---
title: Conservation, suppression et destruction de données dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Vue d'ensemble des stratégies de Microsoft pour Office 365 relatives à la rétention, la suppression et la destruction des données.
ms.openlocfilehash: 8a773ebafba0d7cdd36b9da30878dcc487685846
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "24961570"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Conservation, suppression et destruction de données dans Office 365

Microsoft propose une stratégie standard de gestion des données pour Office 365 qui spécifie la durée de conservation des données client après leur suppression. Il existe généralement deux scénarios dans lesquels les données client sont supprimées:

- **Suppression active** -le client a un abonnement actif et un utilisateur supprime des données, ou les données fournies par un utilisateur sont supprimées par l'administrateur.
- **Suppression passive** -l'abonnement client prend fin.

## <a name="data-retention"></a>RéTention des données

Pour chacun de ces scénarios de suppression, le tableau suivant indique la période maximale de rétention des données, par catégorie de données et par classification:

| Catégorie de données | Classification des données | Description | Exemples | Période de réTention |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Données client | Contenu client| Contenu fourni/créé directement par les administrateurs et les utilisateurs <br><br> Cela inclut l'ensemble du texte, du son, de la vidéo, des fichiers image et des logiciels créés et stockés dans les centres de données Microsoft lors de l'utilisation des services dans Office 365 | Exemples des applications Office 365 les plus couramment utilisées qui permettent aux utilisateurs de créer des données, notamment Word, Excel, PowerPoint, Outlook et OneNote <br><br> Le contenu du client inclut également les secrets fournis par le client (mots de passe, certificats, clés de chiffrement, clés de stockage). | **Scénario de suppression active:** au plus 30 jours <br><br> **Scénario de suppression passive:** au plus 180 jours |
| Données client | Informations identifiables de l'utilisateur final (EUII) | Données qui identifient ou peuvent être utilisées pour identifier l'utilisateur d'un service Microsoft. EUII ne contient pas de contenu client | Nom d'utilisateur ou nom d'affichage (domaine\nom_utilisateur) <br><br> Nom d'utilisateur principal (nom @ domaine) <br><br>  Adresses IP spécifiques de l'utilisateur | **Scénario de suppression active:** au plus 180 jours (seule une action de l'administrateur client) <br><br> **Scénario de suppression passive:** au plus 180 jours |
| Données personnelles <br> (données non incluses dans les données client) | Identificateurs de pseudonyme de l'utilisateur final (EUPI) | Identificateur créé par Microsoft et lié à l'utilisateur d'un service Microsoft. Lorsque EUPI est combiné à d'autres informations, telles qu'une table de mappage, il identifie l'utilisateur final. <br><br> EUPI ne contient pas les informations chargées ou créées par le client. | GUID d'utilisateur, PUIDs ou sid <br><br> ID de session | **Scénario de suppression active:** au plus 30 jours <br><br> **Scénario de suppression passive:** au plus 180 jours |

## <a name="subscription-retention"></a>RéTention d'abonnement

À tout moment pendant le terme d'un abonnement actif, un abonné peut accéder aux données client stockées dans Office 365, les extraire ou les supprimer. Si un abonnement payant se termine ou est terminé, Microsoft conservera les données client stockées dans Office 365 dans un compte à fonction limitée pendant 90 jours pour permettre à l'abonné d'extraire les données. Une fois la période de rétention de 90 jours terminée, Microsoft désactive le compte et supprime les données client. Pas plus de 180 jours après l'expiration ou la résiliation d'un abonnement à Office 365, Microsoft désactive le compte et supprime toutes les données client du compte. Une fois que la période de rétention maximale de toutes les données s'est écoulée, les données sont rendues irrécupérables.

Dans le cas d'une version d'évaluation gratuite, votre compte passe à un état de grâce pour 30 jours dans la plupart des pays et régions. Pendant cette période de grâce, vous avez la possibilité d'acheter Office 365. Si vous décidez de ne pas acheter Office 365, vous pouvez annuler votre version d'évaluation ou laisser la période de grâce expirer, et les informations et les données de votre compte d'évaluation seront supprimées.

## <a name="expedited-deletion"></a>Suppression accélérée
À tout moment pendant la durée d'un abonnement, un abonné peut contacter le support Microsoft et demander l'annulation de la mise en service de l'abonnement. Dans ce processus, toutes les données utilisateur, y compris les données dans SharePoint Online, Exchange Online pouvant être bloquées ou stockées dans des boîtes aux lettres inactives, sont supprimées trois jours après que l'administrateur a entré le code de verrouillage fourni par Microsoft. Pour plus d'informations sur la mise en service accélérée, consultez la rubrique [Annuler Office 365](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a).

## <a name="related-links"></a>Liens connexes
- [Destruction de données](office-365-data-destruction.md)
- [Immuabilité dans Office 365](office-365-data-immutability.md)
- [Suppression de données Exchange Online](office-365-exchange-online-data-deletion.md)
- [Suppression de données SharePoint Online](office-365-sharepoint-online-data-deletion.md)
- [Suppression des données Skype Entreprise](office-365-skype-data-deletion.md)