---
title: Rapport sur les clients SMTP AUTH
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent en savoir plus sur le rapport clients d’authentification SMTP dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center.
ms.openlocfilehash: df0ef74a3ffd7ae8d36e5d1092b3e23304e1df78
ms.sourcegitcommit: e05e83212e7ca4e84f2ddb0de0297895b995338d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2019
ms.locfileid: "33868552"
---
# <a name="smtp-auth-clients-report"></a>Rapport sur les clients SMTP AUTH

Le rapport **clients d’authentification SMTP** met en évidence l’utilisation du protocole de soumission du client SMTP AUTH par les utilisateurs ou les comptes système de votre organisation. Ce protocole hérité (qui utilise le point de terminaison smtp.office365.com) offre uniquement l’authentification de base et est susceptible d’être utilisé par des comptes compromis pour envoyer des courriers électroniques.  Ce rapport vous permet de vérifier l’activité inhabituelle. Il indique également les données d’utilisation TLS pour les clients ou les appareils utilisant l’authentification SMTP.

Le widget affiché dans le tableau de bord du flux de messagerie indique le nombre d’utilisateurs ou de comptes de service qui ont utilisé le protocole SMTP AUTH au cours des 7 derniers jours.

![Rapport sur les clients SMTP AUTH dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center](media/smtp-auth-clients-report-selected.png)

Un clic sur le widget ouvre une fenêtre mobile qui offre une vue agrégée de l’utilisation et des volumes TLS pour la dernière semaine.

![Le menu volant dans le rapport clients SMTP AUTH](media/smtp-auth-clients-flyout.png)

Lorsque vous cliquez sur le lien du **rapport clients d’authentification SMTP** , deux vues de données principales et deux vues de données s’affichent. Les données croisées dynamiques représentent le **volume d’envoi** et l’utilisation de **TLS**. Les vues de données sont le graphique et le tableau des détails.

L’affichage **volume d’envoi** indique le nombre de messages qui ont été envoyés à l’aide de l’authentification SMTP pour la plage de temps spécifiée. Vous pouvez ajuster la plage en cliquant sur **filtres**. Le graphique est organisé par domaine d’expéditeur. Vous pouvez voir les données séparées pour chaque domaine en sélectionnant le domaine dans la liste déroulante **afficher les données** .

![Envoi de volume dans le rapport clients SMTP AUTH](media/smtp-auth-clients-report-sending-volume.png)

Vous pouvez afficher des informations détaillées sur les expéditeurs et le nombre de messages en cliquant sur **afficher la table des détails**. Pour revenir au graphique, cliquez sur **afficher le rapport**.

![Table des détails pour l’envoi de volume dans le rapport clients SMTP AUTH](media/smtp-auth-clients-report-details-sending-volume.png)

Le tableau croisé dynamique d' **utilisation TLS** est important en raison de la désapprobation à venir de TLS 1.0 et TLS 1.1 dans Office 365. De nombreux appareils et applications hérités ne peuvent pas envoyer de courrier électronique s’ils ne peuvent utiliser TLS 1.0 qu’avec l’authentification SMTP. Ce tableau croisé dynamique vous permet d’identifier et de prendre des mesures sur les utilisateurs et les comptes système qui utilisent encore des versions plus anciennes de TLS.

![Utilisation de TLS dans le rapport clients d’authentification SMTP](media/smtp-auth-clients-report-tls-usage.png)

Vous pouvez afficher des informations détaillées sur les expéditeurs, les versions de TLS qu’ils utilisent avec l’authentification SMTP et le nombre de messages en cliquant sur **afficher la table des détails**. Pour revenir au graphique, cliquez sur **afficher le rapport**.

Vous pouvez également télécharger une version plus détaillée du rapport en cliquant sur demander un rapport.

![Table des détails pour l’utilisation de TLS dans le rapport clients SMTP AUTH](media/smtp-auth-clients-report-details-tls-usage.png)

## <a name="see-also"></a>Voir aussi

Pour plus d’informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security _AMP_ Compliance Center](mail-flow-insights-v2.md).
