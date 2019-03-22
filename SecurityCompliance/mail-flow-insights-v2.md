---
title: Informations sur le flux de messagerie dans le centre de sécurité & conformité
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: Les administrateurs peuvent en savoir plus sur le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 4af35fea640c1f4c43464d1adf2e4a9f3b4f780d
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30722853"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a>Informations sur le flux de messagerie dans le centre de sécurité & conformité

> [!NOTE]
> Les fonctionnalités décrites dans cette rubrique n'ont pas été déployées sur toutes les organisations Office 365 et peuvent faire l'objet de modifications.

Les administrateurs peuvent utiliser le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center pour découvrir des tendances, des informations et prendre des mesures pour résoudre les problèmes liés au flux de messagerie dans leur organisation Office 365.

Les informations, les rapports et les widgets disponibles dans le tableau de bord du flux de messagerie sont les suivants:

- [Rapport de carte de flux de messagerie](mfi-mail-flow-map-report.md) (Ce rapport est nouveau et est actuellement déployé dans Office 365.)

- [Aperçu](mfi-domain-mail-flow-status-insight.md) de l'état du flux de messagerie du domaine (Cette vue est nouvelle et est actuellement déployée dans Office 365.)

- [Rapport sur les clients SMTP AUTH](mfi-smtp-auth-clients-report.md) (Ce rapport est nouveau et est actuellement déployé dans Office 365.)

- [Aperçu de domaine](mfi-sender-domain-insight.md) de l'expéditeur (Cette vue est nouvelle et est actuellement déployée dans Office 365.)

- [Notification de non-remise](mfi-non-delivery-report.md) (Ce rapport est nouveau et est actuellement déployé dans Office 365.)

- [Rapport de domaine non accepté](mfi-non-accepted-domain-report.md) (Ce rapport est nouveau et est actuellement déployé dans Office 365.)

- [Flux de courrier entrant et sortant](mfi-outbound-and-inbound-mail-flow.md)

- [Alertes de files d’attente et files d’attente](mfi-queue-alerts-and-queues.md)

- [Rapport des messages transférés automatiquement](mfi-auto-forwarded-messages-report.md)

- [Informations sur les boucles de courrier](mfi-mail-loop-insight.md)

- [Informations sur les règles de flux de messagerie lent](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a>Autorisations requises pour afficher le tableau de bord de flux de messagerie

Le tableau de bord de flux de messagerie est disponible pour:

- Membres du rôle d' **administrateur général Office 365** .

- Membres du rôle d' **administrateur Exchange 365 Office** .

- Membres du **rôle administrateur de flux de messagerie** dans le centre de sécurité _AMP_ Compliance Center. Si ce rôle est attribué de manière explicite à un utilisateur qui n'est pas membre des rôles administrateur général ou administrateur Exchange:

  - L'utilisateur doit se connecter au centre de sécurité & Compliance directement à [https://protection.office.com](https://protection.office.com)l'adresse.

  - L'utilisateur disposera uniquement de l'autorisation lecture seule sur le tableau de bord du flux de messagerie.

  - L'utilisateur n'a pas accès au portail d'administration d'Office 365.

Pour plus d'informations sur le rôle d'administrateur général Office 365, voir [à propos des rôles d'administrateur office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).

Pour plus d'informations sur l'attribution de rôles de centre de sécurité & de conformité aux utilisateurs, consultez [la rubrique accorder aux utilisateurs l'accès au centre de sécurité _AMP_ Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).

## <a name="where-to-find-the-mail-flow-dashboard"></a>Où trouver le tableau de bord de flux de messagerie?

1. Accédez au centre de sécurité & Compliance à [https://protection.office.com](https://protection.office.com)l'adresse.

2. Développez **flux de messagerie** , puis sélectionnez **tableau de bord**.

   ![Tableau de bord de flux de messagerie dans le centre de sécurité & Office 365 Security](media/mail-flow-dashboard-v2.png)
