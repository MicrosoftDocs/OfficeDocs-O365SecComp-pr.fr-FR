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
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="00b5d-103">Intelligence de flux de messagerie dans Office 365</span><span class="sxs-lookup"><span data-stu-id="00b5d-103">Mail flow intelligence in Office 365</span></span>

<span data-ttu-id="00b5d-p101">En règle générale, vous utilisez un connecteur pour router les messages électroniques à partir de votre organisation Office 365 à votre environnement de messagerie local. Vous pouvez également utiliser un connecteur pour router les messages à partir d’Office 365 à une organisation partenaire. Lorsque Office 365 ne peut pas remettre les messages via le connecteur, ils sont en file d’attente dans Office 365. Office 365 continuera de nouvelle tentative de remise pour chaque message de 48 heures. Après 48 heures, le message en file d’attente expire, et le message sera renvoyé à l’expéditeur d’origine dans un rapport de non-remise (également appelé un message de rapport de non-remise ou de rebond).</span><span class="sxs-lookup"><span data-stu-id="00b5d-p101">Typically, you use a connector to route email messages from your Office 365 organization to your on-premises email environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>

<span data-ttu-id="00b5d-p102">Office 365 génère une erreur lorsqu’un message ne peut pas être remis à l’aide d’un connecteur. Les erreurs les plus courants et leurs solutions sont décrits dans cette rubrique. Collectivement, les erreurs de mise en attente et de notification pour les messages non remis envoyés via des connecteurs est appelé _intelligence de flux de messagerie_.</span><span class="sxs-lookup"><span data-stu-id="00b5d-p102">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as _mail flow intelligence_.</span></span>

## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="00b5d-112">Code d'erreur : 450 4.4.312 Échec de la requête DNS</span><span class="sxs-lookup"><span data-stu-id="00b5d-112">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="00b5d-p103">En règle générale, cette erreur signifie Qu'office 365 a essayé de se connecter à l’hôte actif est spécifié dans le connecteur, mais la requête DNS pour rechercher des adresses IP de l’hôte actif a échoué. Les causes possibles de cette erreur sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="00b5d-p103">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host's IP addresses failed. The possible causes for this error are:</span></span>

- <span data-ttu-id="00b5d-115">Il y a un problème avec le service d'hébergement DNS de votre domaine (la partie qui met à jour les serveurs de noms faisant autorité pour votre domaine).</span><span class="sxs-lookup"><span data-stu-id="00b5d-115">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>

- <span data-ttu-id="00b5d-116">Votre domaine a expiré récemment, l'enregistrement MX ne peut donc pas être extrait.</span><span class="sxs-lookup"><span data-stu-id="00b5d-116">Your domain has recently expired, so the MX record can't be retrieved.</span></span>

- <span data-ttu-id="00b5d-117">L'enregistrement MX de votre domaine a récemment été modifié et les serveurs DNS Office 365 disposent toujours des informations DNS précédemment mises en cache pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="00b5d-117">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>

### <a name="how-do-i-fix-error-code-450-44312"></a><span data-ttu-id="00b5d-118">Comment puis-je corriger le code d’erreur 450 4.4.312 ?</span><span class="sxs-lookup"><span data-stu-id="00b5d-118">How do I fix error code 450 4.4.312?</span></span>

- <span data-ttu-id="00b5d-119">Utilisation de votre service d’hébergement DNS pour identifier et résoudre le problème avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="00b5d-119">Work with your DNS hosting service to identify and fix the problem with your domain.</span></span>

- <span data-ttu-id="00b5d-120">Si l’erreur est à partir de votre organisation partenaire (par exemple, un 3e cloud service fournisseur tiers), contactez votre partenaire pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-120">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="00b5d-121">Code d'erreur : 450 4.4.315 Délai de connexion dépassé</span><span class="sxs-lookup"><span data-stu-id="00b5d-121">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="00b5d-p104">En règle générale, cela signifie Qu'office 365 ne peuvent pas se connecter au serveur de messagerie de destination. Les détails d’erreur explique le problème. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="00b5d-p104">Typically, this means Office 365 can't connect to the destination email server. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="00b5d-125">Votre serveur de messagerie sur site est inactif.</span><span class="sxs-lookup"><span data-stu-id="00b5d-125">Your on-premises email server is down.</span></span>

- <span data-ttu-id="00b5d-126">Il y a une erreur dans les paramètres d'hôte actif du connecteur, donc Office 365 essaie de se connecter à la mauvaise adresse IP.</span><span class="sxs-lookup"><span data-stu-id="00b5d-126">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>

### <a name="how-do-i-fix-error-code-450-44315"></a><span data-ttu-id="00b5d-127">Comment puis-je corriger le code d’erreur 450 4.4.315 ?</span><span class="sxs-lookup"><span data-stu-id="00b5d-127">How do I fix error code 450 4.4.315?</span></span>

- <span data-ttu-id="00b5d-p105">Trouver le scénario s’applique à vous et apportez les corrections nécessaires. Par exemple, si le flux de messagerie a été fonctionne correctement et que vous n’avez pas modifié les paramètres du connecteur, vous devez vérifier votre environnement de messagerie sur site pour voir si le serveur est arrêté, ou si il y a des modifications apportées à votre infrastructure de réseau (par exemple, vous avez modifié les fournisseurs de services internet, afin que vous avez maintenant des adresses IP différentes).</span><span class="sxs-lookup"><span data-stu-id="00b5d-p105">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises email environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed internet service providers, so you now have different IP addresses).</span></span>

- <span data-ttu-id="00b5d-130">Si l’erreur est à partir de votre organisation partenaire (par exemple, un 3e cloud service fournisseur tiers), contactez votre partenaire pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-130">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="00b5d-131">Code d'erreur : 450 4.4.316 Connexion refusée.</span><span class="sxs-lookup"><span data-stu-id="00b5d-131">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="00b5d-p106">En règle générale, cette erreur signifie que Office 365 a rencontré une erreur de connexion lorsqu’il a essayé de se connecter au serveur de messagerie de destination. Une cause probable de cette erreur est que votre pare-feu bloque les connexions à partir d’adresses IP de Office 365. Ou bien, cette erreur peut être par leur conception si vous avez migré complètement votre locale système de messagerie vers Office 365 et arrêtez votre environnement de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="00b5d-p106">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination email server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises email system to Office 365 and shut down your on-premises email environment.</span></span>

### <a name="how-do-i-fix-error-code-450-44316"></a><span data-ttu-id="00b5d-135">Comment puis-je corriger le code d’erreur 450 4.4.316 ?</span><span class="sxs-lookup"><span data-stu-id="00b5d-135">How do I fix error code 450 4.4.316?</span></span>

- <span data-ttu-id="00b5d-p107">Si vous avez des boîtes aux lettres dans votre environnement local, vous devez modifier vos paramètres de pare-feu pour autoriser les connexions à partir d’adresses IP de Office 365 sur le port TCP 25 pour vos serveurs de messagerie local. Pour obtenir la liste des adresses IP de Office 365, voir [Office 365 URL et plages d’adresses IP](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span><span class="sxs-lookup"><span data-stu-id="00b5d-p107">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises email servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span></span>

- <span data-ttu-id="00b5d-p108">Si aucun autre message ne doit être remis dans votre environnement local, cliquez sur **Fix now** (Corriger maintenant) dans l'alerte afin qu'Office 365 puisse rejeter immédiatement les messages dont les destinataires ne sont pas valides. Cette action réduira le risque de dépasser le quota de destinataires non valides de votre organisation, ce qui peut avoir des répercussions négatives sur la remise normale des messages. Vous pouvez également suivre les instructions suivantes pour résoudre manuellement le problème :</span><span class="sxs-lookup"><span data-stu-id="00b5d-p108">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span>

  - <span data-ttu-id="00b5d-141">Dans le [Centre d’administration Exchange (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) dans Office 365, désactiver ou supprimer le connecteur messagerie à partir d’Office 365 à votre environnement de messagerie local :</span><span class="sxs-lookup"><span data-stu-id="00b5d-141">In the [Exchange admin center (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365, disable or delete the connector that delivers email from Office 365 to your on-premises email environment:</span></span>

    1. <span data-ttu-id="00b5d-142">Dans le CAE, accédez à **flux de messagerie** \> **connecteurs**.</span><span class="sxs-lookup"><span data-stu-id="00b5d-142">In the EAC, go to **Mail flow** \> **Connectors**.</span></span>

    2. <span data-ttu-id="00b5d-143">Sélectionnez le connecteur avec la valeur **de** **Office 365** et la valeur **au** **serveur de messagerie de votre organisation** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b5d-143">Select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server** and do one of the following steps:</span></span>

       - <span data-ttu-id="00b5d-144">Supprimez le connecteur en cliquant sur **Supprimer** ![icône de suppression](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span><span class="sxs-lookup"><span data-stu-id="00b5d-144">Delete the connector by clicking **Delete** ![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span></span>

       - <span data-ttu-id="00b5d-145">Désactiver le connecteur en cliquant sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) et annulation de l' **Activer**.</span><span class="sxs-lookup"><span data-stu-id="00b5d-145">Disable the connector by clicking **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) and unchecking **Turn it on**.</span></span>

  - <span data-ttu-id="00b5d-p109">Modifier le domaine accepté dans Office 365 associé à votre environnement de messagerie locale à partir de **Relais interne** sur **faisant autorité**. Pour plus d’informations, voir [Gérer les domaines acceptés dans Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span><span class="sxs-lookup"><span data-stu-id="00b5d-p109">Change the accepted domain in Office 365 that's associated with your on-premises email environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span></span>

  <span data-ttu-id="00b5d-p110">**Remarque**: en règle générale, ces modifications prendront entre 30 minutes et une heure prennent effet. Après une heure, vérifiez que vous ne recevez plus l’erreur.</span><span class="sxs-lookup"><span data-stu-id="00b5d-p110">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>

- <span data-ttu-id="00b5d-150">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-150">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="00b5d-151">Code d'erreur : 450 4.4.317 La connexion au serveur distant a échoué</span><span class="sxs-lookup"><span data-stu-id="00b5d-151">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="00b5d-p111">En règle générale, cette erreur signifie que Office 365 connecté au serveur de messagerie de destination, mais le serveur a renvoyé une erreur d’exécution ou ne répond pas à la configuration requise de connexion. Les détails d’erreur explique le problème. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="00b5d-p111">Typically, this error means Office 365 connected to the destination email server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="00b5d-155">Le serveur de messagerie de destination a répondu avec une erreur « Service non disponible », qui indique que le serveur ne parvient pas à maintenir la communication avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="00b5d-155">The destination email server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>

- <span data-ttu-id="00b5d-156">Le connecteur est configuré pour exiger le chiffrement TLS, mais le serveur de messagerie de destination ne prend pas en charge TLS.</span><span class="sxs-lookup"><span data-stu-id="00b5d-156">The connector is configured to require TLS, but the destination email server doesn't support TLS.</span></span>

### <a name="how-do-i-fix-error-code-450-44317"></a><span data-ttu-id="00b5d-157">Comment puis-je corriger le code d’erreur 450 4.4.317 ?</span><span class="sxs-lookup"><span data-stu-id="00b5d-157">How do I fix error code 450 4.4.317?</span></span>

- <span data-ttu-id="00b5d-158">Vérifiez les paramètres TLS certificats sur vos serveurs de messagerie sur site et les paramètres TLS sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="00b5d-158">Verify the TLS settings and certificates on your on-premises email servers, and the TLS settings on the connector.</span></span>

- <span data-ttu-id="00b5d-159">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-159">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="00b5d-160">Code d'erreur : 450 4.4.318 La connexion a été interrompue brusquement</span><span class="sxs-lookup"><span data-stu-id="00b5d-160">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="00b5d-p112">En règle générale, cette erreur signifie que Office 365 est des difficultés à communiquer avec votre environnement de messagerie local, afin que la connexion a été supprimée. Les causes possibles de cette erreur sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="00b5d-p112">Typically, this error means Office 365 is having difficulty communicating with your on-premises email environment, so the connection was dropped. The possible causes for this error are:</span></span>

- <span data-ttu-id="00b5d-163">Votre pare-feu utilise des règles d'examen de paquet SMTP, lesquelles ne fonctionnent pas correctement.</span><span class="sxs-lookup"><span data-stu-id="00b5d-163">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>

- <span data-ttu-id="00b5d-164">Votre serveur de messagerie local n’est pas de travail correctement (par exemple, service blocages, incidents ou manque de ressources système), qui est à l’origine au serveur de délai d’expiration et fermez la connexion à Office 365.</span><span class="sxs-lookup"><span data-stu-id="00b5d-164">Your on-premises email server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>

- <span data-ttu-id="00b5d-165">Il y a des problèmes réseau entre votre environnement local et Office 365.</span><span class="sxs-lookup"><span data-stu-id="00b5d-165">There are network issues between your on-premises environment and Office 365.</span></span>

### <a name="how-do-i-fix-error-code-450-44318"></a><span data-ttu-id="00b5d-166">Comment puis-je corriger le code d’erreur 450 4.4.318 ?</span><span class="sxs-lookup"><span data-stu-id="00b5d-166">How do I fix error code 450 4.4.318?</span></span>

- <span data-ttu-id="00b5d-167">Déterminez le scénario qui vous concerne et apportez les corrections nécessaires.</span><span class="sxs-lookup"><span data-stu-id="00b5d-167">Find out which scenario applies to you, and make the necessary corrections.</span></span>

- <span data-ttu-id="00b5d-168">Si le problème est dû à des problèmes réseau entre votre environnement local et d’Office 365, contactez votre équipe réseau pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-168">If the problem is caused by network issues between your on-premises environment and Office 365, contact your network team to troubleshoot the issue.</span></span>

- <span data-ttu-id="00b5d-169">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-169">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="00b5d-170">Code d'erreur : 450 4.7.320 Échec de la validation du certificat</span><span class="sxs-lookup"><span data-stu-id="00b5d-170">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="00b5d-p113">En règle générale, cette erreur signifie que Office 365 a rencontré une erreur lors de la tentative valider le certificat du serveur de messagerie de destination. Les détails d’erreur explique l’erreur. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="00b5d-p113">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination email server. The error details will explain the error. For example:</span></span>

- <span data-ttu-id="00b5d-174">Le certificat est arrivé à expiration.</span><span class="sxs-lookup"><span data-stu-id="00b5d-174">Certificate expired</span></span>

- <span data-ttu-id="00b5d-175">Le sujet du certificat ne concorde pas.</span><span class="sxs-lookup"><span data-stu-id="00b5d-175">Certificate subject mismatch</span></span>

- <span data-ttu-id="00b5d-176">Le certificat n'est plus valide.</span><span class="sxs-lookup"><span data-stu-id="00b5d-176">Certificate is no longer valid</span></span>

### <a name="how-do-i-fix-error-code-450-47320"></a><span data-ttu-id="00b5d-177">Comment puis-je corriger le code d’erreur 450 4.7.320 ?</span><span class="sxs-lookup"><span data-stu-id="00b5d-177">How do I fix error code 450 4.7.320?</span></span>

- <span data-ttu-id="00b5d-178">Corriger le certificat ou les paramètres sur le connecteur de sorte que la file d’attente de messages dans Office 365 peuvent être remis.</span><span class="sxs-lookup"><span data-stu-id="00b5d-178">Fix the certificate or the settings on the connector so that queued messages in Office 365 can be delivered.</span></span>

- <span data-ttu-id="00b5d-179">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l’origine de l’erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="other-error-codes"></a><span data-ttu-id="00b5d-180">Autres codes d'erreur</span><span class="sxs-lookup"><span data-stu-id="00b5d-180">Other error codes</span></span>

<span data-ttu-id="00b5d-p114">Office 365 est dans une situation délicate remettre des messages à votre site ou serveur de messagerie de partenaire. Utilisez les informations de **serveur de Destination** de l’erreur pour examiner le problème dans votre environnement, ou modifier le connecteur s’il existe une erreur de configuration.</span><span class="sxs-lookup"><span data-stu-id="00b5d-p114">Office 365 is having difficulty delivering messages to your on-premises or partner email server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 

<span data-ttu-id="00b5d-183">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="00b5d-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
