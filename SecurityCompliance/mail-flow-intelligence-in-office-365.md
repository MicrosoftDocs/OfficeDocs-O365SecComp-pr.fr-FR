---
title: Intelligence de flux de messagerie dans Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Les administrateurs peuvent en savoir plus sur les codes d’erreur associés à la remise des messages à l’aide de connecteurs dans Office 365 (également appelés aide au flux de messagerie).
ms.openlocfilehash: 0d7d008699242334f2f77dce28e2f1b7e39cf9bb
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598880"
---
# <a name="mail-flow-intelligence-in-office-365"></a>Renseignements sur le flux de messagerie dans Office 365

En règle générale, vous utilisez un connecteur pour acheminer les messages électroniques de votre organisation Office 365 vers votre environnement de messagerie local. Vous pouvez également utiliser un connecteur pour router les messages d'Office 365 vers une organisation partenaire. Lorsqu'Office 365 ne peut pas remettre ces messages via le connecteur, ils sont mis en file d'attente dans Office 365. Office 365 continue d'essayer de livrer chaque message pendant 48 heures. Après 48 heures, le message mis en file d'attente arrive à expiration et le message est renvoyé à l'expéditeur d'origine dans une notification d'échec de remise (également appelée notification de non-remise).

Office 365 génère une erreur lorsqu'un message ne peut pas être remis à l'aide d'un connecteur. Les erreurs les plus courantes et leurs solutions sont décrites dans cette rubrique. Les erreurs de notification et de mise en file d’attente pour les messages non remis envoyés via des connecteurs sont appelées _intelligence de flux de messagerie_.

## <a name="error-code-450-44312-dns-query-failed"></a>Code d’erreur : 450 4.4.312 Échec de la requête DNS

En règle générale, cette erreur signifie qu’Office 365 a essayé de se connecter à l’hôte actif qui est spécifié dans le connecteur, mais que la requête DNS de recherche des adresses IP de l’hôte actif a échoué. Les causes pouvant être à l'origine de cette erreur sont les suivantes :

- Il y a un problème avec le service d'hébergement DNS de votre domaine (la partie qui met à jour les serveurs de noms faisant autorité pour votre domaine).

- Votre domaine a expiré récemment, l'enregistrement MX ne peut donc pas être extrait.

- L'enregistrement MX de votre domaine a récemment été modifié et les serveurs DNS Office 365 disposent toujours des informations DNS précédemment mises en cache pour votre domaine.

### <a name="how-do-i-fix-error-code-450-44312"></a>Comment corriger le code d’erreur 450 4.4.312 échec?

- Collaborez avec votre service d’hébergement DNS pour identifier et résoudre le problème lié à votre domaine.

- Si l’erreur provient de votre organisation partenaire (par exemple, un fournisseur de services Cloud tiers), contactez votre partenaire pour résoudre le problème.

## <a name="error-code-450-44315-connection-timed-out"></a>Code d’erreur : 450 4.4.315 Délai de connexion dépassé

En règle générale, cela signifie qu’Office 365 ne peut pas se connecter au serveur de messagerie de destination. Les détails de l'erreur expliquent le problème. Par exemple :

- Votre serveur de messagerie local est inactif.

- Il y a une erreur dans les paramètres d'hôte actif du connecteur, donc Office 365 essaie de se connecter à la mauvaise adresse IP.

### <a name="how-do-i-fix-error-code-450-44315"></a>Comment corriger le code d’erreur 450 4.4.315 délai?

- Déterminez le scénario qui vous concerne et apportez les corrections nécessaires. Par exemple, si le flux de messagerie fonctionne correctement et que vous n’avez pas modifié les paramètres du connecteur, vous devez vérifier votre environnement de messagerie local pour déterminer si le serveur est en panne ou s’il y a eu des modifications apportées à votre infrastructure réseau (par exemple, vous avez modifié les fournisseurs de services Internet, de sorte que vous avez à présent des adresses IP différentes.

- Si l’erreur provient de votre organisation partenaire (par exemple, un fournisseur de services Cloud tiers), contactez votre partenaire pour résoudre le problème.

## <a name="error-code-450-44316-connection-refused"></a>Code d’erreur : 450 4.4.316 Connexion refusée.

En règle générale, cette erreur signifie qu’Office 365 a rencontré une erreur de connexion lorsqu’il a essayé de se connecter au serveur de messagerie de destination. Une cause probable de cette erreur est que votre pare-feu bloque les connexions depuis des adresses IP Office 365. Cette erreur peut également être voulue si vous avez entièrement migré votre système de messagerie local vers Office 365 et arrêté votre environnement de messagerie local.

### <a name="how-do-i-fix-error-code-450-44316"></a>Comment corriger le code d’erreur 450 4.4.316?

- Si vous avez des boîtes aux lettres dans votre environnement local, vous devez modifier les paramètres de votre pare-feu pour autoriser les connexions à partir des adresses IP Office 365 sur le port TCP 25 vers vos serveurs de messagerie locaux. Pour obtenir une liste des adresses IP Office 365, consultez l'article [URL et plages d'adresses IP Office 365](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).

- Si aucun autre message ne doit être remis dans votre environnement local, cliquez sur **Fix now** (Corriger maintenant) dans l'alerte afin qu'Office 365 puisse rejeter immédiatement les messages dont les destinataires ne sont pas valides. Cette action réduira le risque de dépasser le quota de destinataires non valides de votre organisation, ce qui peut avoir des répercussions négatives sur la remise normale des messages. Vous pouvez également suivre les instructions suivantes pour résoudre manuellement le problème :

  - Dans le [Centre d’administration Exchange](https://docs.microsoft.com/Exchange/exchange-admin-center) dans Office 365, désactivez ou supprimez le connecteur qui remet le courrier électronique d’Office 365 à votre environnement de messagerie local:

    1. Dans le centre d’administration Exchange, accédez à **connecteurs**de **flux** \> de messagerie.

    2. Sélectionnez le connecteur avec la valeur **à partir d'** **Office 365** et la valeur **pour** le **serveur de messagerie de votre organisation** , puis effectuez l’une des opérations suivantes:

       - Supprimez le connecteur en cliquant sur **supprimer** ![l’icône Supprimer.](media/adf01106-cc79-475c-8673-065371c1897b.gif)

       - Désactivez le connecteur **** ![en cliquant sur](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) modifier l’icône modifier, puis désactivez la case à cocher **activer**.

  - Modifiez le domaine accepté dans Office 365 associé à votre environnement de messagerie local de **relais interne** vers **faisant autorité**. Pour obtenir des instructions, consultez la rubrique [gestion des domaines acceptés dans Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).

  **Remarque**: en règle générale, ces modifications prennent entre 30 minutes et une heure pour prendre effet. Après une heure, vérifiez que vous ne recevez plus l’erreur.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a>Code d’erreur : 450 4.4.317 La connexion au serveur distant a échoué

En règle générale, cette erreur signifie qu’Office 365 est connecté au serveur de messagerie de destination, mais que le serveur a répondu avec une erreur immédiate ou ne répond pas aux exigences de connexion. Les détails de l'erreur expliquent le problème. Par exemple :

- Le serveur de messagerie de destination a répondu avec une erreur «service non disponible», ce qui indique que le serveur ne peut pas maintenir la communication avec Office 365.

- Le connecteur est configuré pour exiger TLS, mais le serveur de messagerie de destination ne prend pas en charge le protocole TLS.

### <a name="how-do-i-fix-error-code-450-44317"></a>Comment corriger le code d’erreur 450 4.4.317?

- Vérifiez les certificats et les paramètres TLS sur vos serveurs de messagerie locaux, ainsi que les paramètres TLS sur le connecteur.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a>Code d’erreur : 450 4.4.318 La connexion a été interrompue brusquement

En règle générale, cette erreur signifie qu’Office 365 rencontre des difficultés pour communiquer avec votre environnement de messagerie local, de sorte que la connexion a été abandonnée. Les causes pouvant être à l'origine de cette erreur sont les suivantes :

- Votre pare-feu utilise des règles d'examen de paquet SMTP, lesquelles ne fonctionnent pas correctement.

- Votre serveur de messagerie local ne fonctionne pas correctement (par exemple, blocage du service, blocage ou ressources système faibles), ce qui entraîne l’expiration du serveur et la fermeture de la connexion à Office 365.

- Il y a des problèmes réseau entre votre environnement local et Office 365.

### <a name="how-do-i-fix-error-code-450-44318"></a>Comment corriger le code d’erreur 450 4.4.318 la?

- Déterminez le scénario qui vous concerne et apportez les corrections nécessaires.

- Si le problème est dû à des problèmes de réseau entre votre environnement local et Office 365, contactez votre équipe réseau pour résoudre le problème.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="error-code-450-47320-certificate-validation-failed"></a>Code d’erreur : 450 4.7.320 Échec de la validation du certificat

En règle générale, cette erreur signifie qu’Office 365 a rencontré une erreur lors de la tentative de validation du certificat du serveur de messagerie de destination. Les détails de l'erreur expliquent cette dernière. Par exemple :

- Le certificat est arrivé à expiration.

- Le sujet du certificat ne concorde pas.

- Le certificat n'est plus valide.

### <a name="how-do-i-fix-error-code-450-47320"></a>Comment corriger le code d’erreur 450 4.7.320 échec?

- Corrigez le certificat ou les paramètres sur le connecteur afin que les messages en file d’attente dans Office 365 puissent être remis.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="other-error-codes"></a>Autres codes d’erreur

Office 365 rencontre des problèmes lors de la remise de messages à votre serveur de messagerie local ou partenaire. Utilisez les informations sur le **serveur de destination** dans l'erreur afin d'examiner le problème dans votre environnement ou modifiez le connecteur en cas d'erreur de configuration. 

Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
