---
title: Intelligence de flux de messagerie dans Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Administrateurs peuvent en savoir plus sur les codes d’erreur qui sont associés avec la remise du message à l’aide de connecteurs dans Office 365 (également appelé intelligence de flux de messagerie).
ms.openlocfilehash: 9f27dfd4c265eb62028d68c27764183202692ef4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327086"
---
# <a name="mail-flow-intelligence-in-office-365"></a>Intelligence de flux de messagerie dans Office 365

En règle générale, vous utilisez un connecteur pour router les messages électroniques à partir de votre organisation Office 365 à votre environnement de messagerie local. Vous pouvez également utiliser un connecteur pour router les messages à partir d’Office 365 à une organisation partenaire. Lorsque Office 365 ne peut pas remettre les messages via le connecteur, ils sont en file d’attente dans Office 365. Office 365 continuera de nouvelle tentative de remise pour chaque message de 48 heures. Après 48 heures, le message en file d’attente expire, et le message sera renvoyé à l’expéditeur d’origine dans un rapport de non-remise (également appelé un message de rapport de non-remise ou de rebond).

Office 365 génère une erreur lorsqu’un message ne peut pas être remis à l’aide d’un connecteur. Les erreurs les plus courants et leurs solutions sont décrits dans cette rubrique. Collectivement, les erreurs de mise en attente et de notification pour les messages non remis envoyés via des connecteurs est appelé _intelligence de flux de messagerie_.

## <a name="error-code-450-44312-dns-query-failed"></a>Code d'erreur : 450 4.4.312 Échec de la requête DNS

En règle générale, cette erreur signifie Qu'office 365 a essayé de se connecter à l’hôte actif est spécifié dans le connecteur, mais la requête DNS pour rechercher des adresses IP de l’hôte actif a échoué. Les causes possibles de cette erreur sont les suivants :

- Il y a un problème avec le service d'hébergement DNS de votre domaine (la partie qui met à jour les serveurs de noms faisant autorité pour votre domaine).

- Votre domaine a expiré récemment, l'enregistrement MX ne peut donc pas être extrait.

- L'enregistrement MX de votre domaine a récemment été modifié et les serveurs DNS Office 365 disposent toujours des informations DNS précédemment mises en cache pour votre domaine.

### <a name="how-do-i-fix-error-code-450-44312"></a>Comment puis-je corriger le code d’erreur 450 4.4.312 ?

- Utilisation de votre service d’hébergement DNS pour identifier et résoudre le problème avec votre domaine.

- Si l’erreur est à partir de votre organisation partenaire (par exemple, un 3e cloud service fournisseur tiers), contactez votre partenaire pour résoudre le problème.

## <a name="error-code-450-44315-connection-timed-out"></a>Code d'erreur : 450 4.4.315 Délai de connexion dépassé

En règle générale, cela signifie Qu'office 365 ne peuvent pas se connecter au serveur de messagerie de destination. Les détails d’erreur explique le problème. Par exemple :

- Votre serveur de messagerie sur site est inactif.

- Il y a une erreur dans les paramètres d'hôte actif du connecteur, donc Office 365 essaie de se connecter à la mauvaise adresse IP.

### <a name="how-do-i-fix-error-code-450-44315"></a>Comment puis-je corriger le code d’erreur 450 4.4.315 ?

- Trouver le scénario s’applique à vous et apportez les corrections nécessaires. Par exemple, si le flux de messagerie a été fonctionne correctement et que vous n’avez pas modifié les paramètres du connecteur, vous devez vérifier votre environnement de messagerie sur site pour voir si le serveur est arrêté, ou si il y a des modifications apportées à votre infrastructure de réseau (par exemple, vous avez modifié les fournisseurs de services internet, afin que vous avez maintenant des adresses IP différentes).

- Si l’erreur est à partir de votre organisation partenaire (par exemple, un 3e cloud service fournisseur tiers), contactez votre partenaire pour résoudre le problème.

## <a name="error-code-450-44316-connection-refused"></a>Code d'erreur : 450 4.4.316 Connexion refusée.

En règle générale, cette erreur signifie que Office 365 a rencontré une erreur de connexion lorsqu’il a essayé de se connecter au serveur de messagerie de destination. Une cause probable de cette erreur est que votre pare-feu bloque les connexions à partir d’adresses IP de Office 365. Ou bien, cette erreur peut être par leur conception si vous avez migré complètement votre locale système de messagerie vers Office 365 et arrêtez votre environnement de messagerie local.

### <a name="how-do-i-fix-error-code-450-44316"></a>Comment puis-je corriger le code d’erreur 450 4.4.316 ?

- Si vous avez des boîtes aux lettres dans votre environnement local, vous devez modifier vos paramètres de pare-feu pour autoriser les connexions à partir d’adresses IP de Office 365 sur le port TCP 25 pour vos serveurs de messagerie local. Pour obtenir la liste des adresses IP de Office 365, voir [Office 365 URL et plages d’adresses IP](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).

- Si aucun autre message ne doit être remis dans votre environnement local, cliquez sur **Fix now** (Corriger maintenant) dans l'alerte afin qu'Office 365 puisse rejeter immédiatement les messages dont les destinataires ne sont pas valides. Cette action réduira le risque de dépasser le quota de destinataires non valides de votre organisation, ce qui peut avoir des répercussions négatives sur la remise normale des messages. Vous pouvez également suivre les instructions suivantes pour résoudre manuellement le problème :

  - Dans le [Centre d’administration Exchange (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) dans Office 365, désactiver ou supprimer le connecteur messagerie à partir d’Office 365 à votre environnement de messagerie local :

    1. Dans le CAE, accédez à **flux de messagerie** \> **connecteurs**.

    2. Sélectionnez le connecteur avec la valeur **de** **Office 365** et la valeur **au** **serveur de messagerie de votre organisation** , effectuez l’une des opérations suivantes :

       - Supprimez le connecteur en cliquant sur **Supprimer** ![icône de suppression](media/adf01106-cc79-475c-8673-065371c1897b.gif)

       - Désactiver le connecteur en cliquant sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) et annulation de l' **Activer**.

  - Modifier le domaine accepté dans Office 365 associé à votre environnement de messagerie locale à partir de **Relais interne** sur **faisant autorité**. Pour plus d’informations, voir [Gérer les domaines acceptés dans Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).

  **Remarque**: en règle générale, ces modifications prendront entre 30 minutes et une heure prennent effet. Après une heure, vérifiez que vous ne recevez plus l’erreur.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a>Code d'erreur : 450 4.4.317 La connexion au serveur distant a échoué

En règle générale, cette erreur signifie que Office 365 connecté au serveur de messagerie de destination, mais le serveur a renvoyé une erreur d’exécution ou ne répond pas à la configuration requise de connexion. Les détails d’erreur explique le problème. Par exemple :

- Le serveur de messagerie de destination a répondu avec une erreur « Service non disponible », qui indique que le serveur ne parvient pas à maintenir la communication avec Office 365.

- Le connecteur est configuré pour exiger le chiffrement TLS, mais le serveur de messagerie de destination ne prend pas en charge TLS.

### <a name="how-do-i-fix-error-code-450-44317"></a>Comment puis-je corriger le code d’erreur 450 4.4.317 ?

- Vérifiez les paramètres TLS certificats sur vos serveurs de messagerie sur site et les paramètres TLS sur le connecteur.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a>Code d'erreur : 450 4.4.318 La connexion a été interrompue brusquement

En règle générale, cette erreur signifie que Office 365 est des difficultés à communiquer avec votre environnement de messagerie local, afin que la connexion a été supprimée. Les causes possibles de cette erreur sont les suivants :

- Votre pare-feu utilise des règles d'examen de paquet SMTP, lesquelles ne fonctionnent pas correctement.

- Votre serveur de messagerie local n’est pas de travail correctement (par exemple, service blocages, incidents ou manque de ressources système), qui est à l’origine au serveur de délai d’expiration et fermez la connexion à Office 365.

- Il y a des problèmes réseau entre votre environnement local et Office 365.

### <a name="how-do-i-fix-error-code-450-44318"></a>Comment puis-je corriger le code d’erreur 450 4.4.318 ?

- Déterminez le scénario qui vous concerne et apportez les corrections nécessaires.

- Si le problème est dû à des problèmes réseau entre votre environnement local et d’Office 365, contactez votre équipe réseau pour résoudre le problème.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="error-code-450-47320-certificate-validation-failed"></a>Code d'erreur : 450 4.7.320 Échec de la validation du certificat

En règle générale, cette erreur signifie que Office 365 a rencontré une erreur lors de la tentative valider le certificat du serveur de messagerie de destination. Les détails d’erreur explique l’erreur. Par exemple :

- Le certificat est arrivé à expiration.

- Le sujet du certificat ne concorde pas.

- Le certificat n'est plus valide.

### <a name="how-do-i-fix-error-code-450-47320"></a>Comment puis-je corriger le code d’erreur 450 4.7.320 ?

- Corriger le certificat ou les paramètres sur le connecteur de sorte que la file d’attente de messages dans Office 365 peuvent être remis.

- Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l’origine de l’erreur, vous devez contacter votre partenaire afin de résoudre le problème.

## <a name="other-error-codes"></a>Autres codes d'erreur

Office 365 est dans une situation délicate remettre des messages à votre site ou serveur de messagerie de partenaire. Utilisez les informations de **serveur de Destination** de l’erreur pour examiner le problème dans votre environnement, ou modifier le connecteur s’il existe une erreur de configuration. 

Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
