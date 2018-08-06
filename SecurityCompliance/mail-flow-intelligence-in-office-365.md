---
title: Intelligence de flux de messagerie dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/27/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 'En règle générale, que vous utilisez un connecteur pour router les messages à partir de votre organisation Office 365 à votre site environnement de messagerie. Vous pouvez également utiliser un connecteur pour router les messages à partir d’Office 365 à une organisation partenaire. Lorsque Office 365 ne peut pas remettre les messages via le connecteur, ils sont en file d’attente dans Office 365. '
ms.openlocfilehash: 495d73524afb3ab3a34fd2f1f5f4cd747481f9d8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027621"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="56698-105">Intelligence de flux de messagerie dans Office 365</span><span class="sxs-lookup"><span data-stu-id="56698-105">Mail flow intelligence in Office 365</span></span>
  
<span data-ttu-id="56698-p102">En règle générale, vous utilisez un connecteur pour router les messages de votre organisation Office 365 vers votre environnement de messagerie local. Vous pouvez également utiliser un connecteur pour router les messages d'Office 365 vers une organisation partenaire. Lorsqu'Office 365 ne peut pas remettre ces messages via le connecteur, ils sont mis en file d'attente dans Office 365. Office 365 continue d'essayer de livrer chaque message pendant 48 heures. Après 48 heures, le message mis en file d'attente arrive à expiration et le message est renvoyé à l'expéditeur d'origine dans une notification d'échec de remise (également appelée notification de non-remise).</span><span class="sxs-lookup"><span data-stu-id="56698-p102">Typically, you use a connector to route messages from your Office 365 organization to your on-premises messaging environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>
  
<span data-ttu-id="56698-p103">Office 365 génère une erreur lorsqu'un message ne peut pas être remis à l'aide d'un connecteur. Les erreurs les plus courantes et leurs solutions sont décrites dans cette rubrique. Collectivement, les erreurs de mise en file d'attente et de notification pour les messages non remis envoyés via des connecteurs sont appelées renseignements sur le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="56698-p103">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as mailflow intelligence.</span></span>
  
 <span data-ttu-id="56698-114">**Contenu de cette rubrique**</span><span class="sxs-lookup"><span data-stu-id="56698-114">**Contents**</span></span>
  
- [<span data-ttu-id="56698-115">Code d'erreur : 450 4.4.312 Échec de la requête DNS</span><span class="sxs-lookup"><span data-stu-id="56698-115">Error code: 450 4.4.312 DNS query failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [<span data-ttu-id="56698-116">Code d'erreur : 450 4.4.315 Délai de connexion dépassé</span><span class="sxs-lookup"><span data-stu-id="56698-116">Error code: 450 4.4.315 Connection timed out</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [<span data-ttu-id="56698-117">Code d'erreur : 450 4.4.316 Connexion refusée.</span><span class="sxs-lookup"><span data-stu-id="56698-117">Error code: 450 4.4.316 Connection refused</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [<span data-ttu-id="56698-118">Code d'erreur : 450 4.4.317 La connexion au serveur distant a échoué</span><span class="sxs-lookup"><span data-stu-id="56698-118">Error code: 450 4.4.317 Cannot connect to remote server</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [<span data-ttu-id="56698-119">Code d'erreur : 450 4.4.318 La connexion a été interrompue brusquement</span><span class="sxs-lookup"><span data-stu-id="56698-119">Error code: 450 4.4.318 Connection was closed abruptly</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [<span data-ttu-id="56698-120">Code d'erreur : 450 4.7.320 Échec de la validation du certificat</span><span class="sxs-lookup"><span data-stu-id="56698-120">Error code: 450 4.7.320 Certificate validation failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="56698-121">Code d'erreur : 450 4.4.312 Échec de la requête DNS</span><span class="sxs-lookup"><span data-stu-id="56698-121">Error code: 450 4.4.312 DNS query failed</span></span>
<span data-ttu-id="56698-122"><a name="ErrorCode44312"> </a></span><span class="sxs-lookup"><span data-stu-id="56698-122"></span></span>

<span data-ttu-id="56698-p104">En règle générale, cette erreur signifie qu'Office 365 a essayé de se connecter à l'hôte actif qui est spécifié dans le connecteur, mais que la requête DNS permettant de rechercher les adresses IP de l'hôte actif a échoué. Les causes pouvant être à l'origine de cette erreur sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="56698-p104">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host IP addresses failed. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="56698-125">Il y a un problème avec le service d'hébergement DNS de votre domaine (la partie qui met à jour les serveurs de noms faisant autorité pour votre domaine).</span><span class="sxs-lookup"><span data-stu-id="56698-125">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>
    
- <span data-ttu-id="56698-126">Votre domaine a expiré récemment, l'enregistrement MX ne peut donc pas être extrait.</span><span class="sxs-lookup"><span data-stu-id="56698-126">Your domain has recently expired, so the MX record can't be retrieved.</span></span>
    
- <span data-ttu-id="56698-127">L'enregistrement MX de votre domaine a récemment été modifié et les serveurs DNS Office 365 disposent toujours des informations DNS précédemment mises en cache pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="56698-127">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>
    
<span data-ttu-id="56698-128">Vous devez résoudre le problème de DNS en collaborant avec votre service d'hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="56698-128">You need to fix the DNS issue by working with your DNS hosting service.</span></span>
  
<span data-ttu-id="56698-129">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-129">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="56698-130">Code d'erreur : 450 4.4.315 Délai de connexion dépassé</span><span class="sxs-lookup"><span data-stu-id="56698-130">Error code: 450 4.4.315 Connection timed out</span></span>
<span data-ttu-id="56698-131"><a name="ErrorCode44315"> </a></span><span class="sxs-lookup"><span data-stu-id="56698-131"></span></span>

<span data-ttu-id="56698-p105">En règle générale, cela signifie qu'Office 365 ne peut pas se connecter au serveur de messagerie de destination. Les détails de l'erreur expliquent le problème. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="56698-p105">Typically, this means Office 365 can't connect to the destination messaging server. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="56698-135">Votre serveur de messagerie local est arrêté.</span><span class="sxs-lookup"><span data-stu-id="56698-135">Your on-premises messaging server is down.</span></span>
    
- <span data-ttu-id="56698-136">Il y a une erreur dans les paramètres d'hôte actif du connecteur, donc Office 365 essaie de se connecter à la mauvaise adresse IP.</span><span class="sxs-lookup"><span data-stu-id="56698-136">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>
    
<span data-ttu-id="56698-p106">Déterminez le scénario qui vous concerne et apportez les corrections nécessaires. Par exemple, si le flux de messagerie fonctionne correctement et que vous n'avez pas modifié les paramètres de connecteur, vous devez vérifier dans votre environnement de messagerie local si le serveur est arrêté ou si des modifications ont été apportées à votre infrastructure réseau (par exemple, vous avez changé de fournisseurs de services Internet, donc vous disposez de différentes adresses IP).</span><span class="sxs-lookup"><span data-stu-id="56698-p106">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises messaging environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed Internet service providers, so you now have different IP addresses).</span></span>
  
<span data-ttu-id="56698-139">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l’origine de l’erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-139">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="56698-140">Code d'erreur : 450 4.4.316 Connexion refusée.</span><span class="sxs-lookup"><span data-stu-id="56698-140">Error code: 450 4.4.316 Connection refused</span></span>
<span data-ttu-id="56698-141"><a name="ErrorCode44316"> </a></span><span class="sxs-lookup"><span data-stu-id="56698-141"></span></span>

<span data-ttu-id="56698-p107">En règle générale, cette erreur signifie qu'Office 365 a rencontré une erreur de connexion lors de la tentative de connexion au serveur de messagerie de destination. Une cause probable de cette erreur est que votre pare-feu bloque les connexions depuis des adresses IP Office 365. Cette erreur peut également être naturelle si vous avez effectué la migration complète de votre système de messagerie local vers Office 365 et éteint votre environnement de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="56698-p107">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination messaging server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises messaging system to Office 365 and shut down your on-premises messaging environment..</span></span>
  
- <span data-ttu-id="56698-p108">Si vous avez des boîtes aux lettres dans votre environnement local, vous devez modifier vos paramètres de pare-feu pour autoriser les connexions à vos serveurs de messagerie locaux depuis des adresses IP Office 365 sur le port TCP 25. Pour obtenir une liste des adresses IP Office 365, consultez l'article [URL et plages d'adresses IP Office 365](https://go.microsoft.com/fwlink/p/?linkid=228887).</span><span class="sxs-lookup"><span data-stu-id="56698-p108">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises messaging servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=228887).</span></span>
    
- <span data-ttu-id="56698-p109">Si aucun autre message ne doit être remis dans votre environnement local, cliquez sur **Fix now** (Corriger maintenant) dans l'alerte afin qu'Office 365 puisse rejeter immédiatement les messages dont les destinataires ne sont pas valides. Cette action réduira le risque de dépasser le quota de destinataires non valides de votre organisation, ce qui peut avoir des répercussions négatives sur la remise normale des messages. Vous pouvez également suivre les instructions suivantes pour résoudre manuellement le problème :</span><span class="sxs-lookup"><span data-stu-id="56698-p109">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span> 
    
  - <span data-ttu-id="56698-p110">Désactivez ou supprimez le connecteur d'Office 365 pour votre environnement local : Centre d'administration Office 365 \> **Centre d'administration** \> **Exchange** \> **Flux de messagerie** \> **Connecteurs** \> sélectionnez le connecteur avec **Office 365** pour valeur **De** et **Serveur de messagerie de votre organisation** pour valeur **À**. Supprimez le connecteur en cliquant sur **Supprimer**![Icône Supprimer](media/ITPro-EAC-DeleteIcon.png) ou désactivez le connecteur en cliquant sur **Modifier**![Icône Modifier](media/ITPro-EAC-EditIcon.png) et en décochant **Activer**.</span><span class="sxs-lookup"><span data-stu-id="56698-p110">Disable or delete the connector from Office 365 to your on-premises environment: Office 365 admin center \> **Admin centers** \> **Exchange** \> **Mail flow** \> **Connectors** \> select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server**. Delete the connector by clicking **Delete**![Delete icon](media/ITPro-EAC-DeleteIcon.png), or disable the connector by clicking **Edit**![Edit icon](media/ITPro-EAC-EditIcon.png) and unchecking **Turn it on**.</span></span>
    
  - <span data-ttu-id="56698-p111">Modifiez le domaine accepté dans Office 365 qui est associé à votre environnement de messagerie local en remplaçant **Relais interne** pour **Faisant autorité**. Pour obtenir des instructions, consultez la rubrique [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span><span class="sxs-lookup"><span data-stu-id="56698-p111">Change the accepted domain in Office 365 that's associated with your on-premises messaging environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span></span>
    
    <span data-ttu-id="56698-p112">**Remarque**: en règle générale, ces modifications prendront entre 30 minutes et une heure prennent effet. Après une heure, vérifiez que vous ne recevez plus l’erreur.</span><span class="sxs-lookup"><span data-stu-id="56698-p112">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>
    
<span data-ttu-id="56698-156">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-156">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="56698-157">Code d'erreur : 450 4.4.317 La connexion au serveur distant a échoué</span><span class="sxs-lookup"><span data-stu-id="56698-157">Error code: 450 4.4.317 Cannot connect to remote server</span></span>
<span data-ttu-id="56698-158"><a name="ErrorCode44317"> </a></span><span class="sxs-lookup"><span data-stu-id="56698-158"></span></span>

<span data-ttu-id="56698-p113">En règle générale, cette erreur signifie qu'Office 365 s'est connecté au serveur de messagerie de destination, mais que le serveur a répondu avec une erreur immédiate ou ne répond pas à la configuration requise en matière de connexion. Les détails de l'erreur expliquent le problème. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="56698-p113">Typically, this error means Office 365 connected to the destination messaging server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="56698-162">Le serveur de messagerie de destination a répondu avec une erreur « Service non disponible », ce qui indique que le serveur ne peut pas maintenir la communication avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="56698-162">The destination messaging server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>
    
- <span data-ttu-id="56698-163">Le connecteur est configuré pour exiger TLS, mais le serveur de messagerie de destination ne prend pas en charge ce protocole.</span><span class="sxs-lookup"><span data-stu-id="56698-163">The connector is configured to require TLS, but the destination messaging server doesn't support TLS.</span></span>
    
<span data-ttu-id="56698-164">Vérifiez les certificats et les paramètres TLS sur vos serveurs de messagerie locaux, ainsi que les paramètres TLS sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="56698-164">Verify the TLS settings and certificates on your on-premises messaging servers, and the TLS settings on the connector.</span></span>
  
<span data-ttu-id="56698-165">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-165">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="56698-166">Code d'erreur : 450 4.4.318 La connexion a été interrompue brusquement</span><span class="sxs-lookup"><span data-stu-id="56698-166">Error code: 450 4.4.318 Connection was closed abruptly</span></span>
<span data-ttu-id="56698-167"><a name="ErrorCode44318"> </a></span><span class="sxs-lookup"><span data-stu-id="56698-167"></span></span>

<span data-ttu-id="56698-p114">En règle générale, cette erreur signifie que la connexion a été coupée car Office 365 a des difficultés à communiquer avec votre environnement de messagerie local. Les causes pouvant être à l'origine de cette erreur sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="56698-p114">Typically, this error means Office 365 is having difficulty communicating with your on-premises messaging environment, so the connection was dropped. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="56698-170">Votre pare-feu utilise des règles d'examen de paquet SMTP, lesquelles ne fonctionnent pas correctement.</span><span class="sxs-lookup"><span data-stu-id="56698-170">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>
    
- <span data-ttu-id="56698-171">Votre serveur de messagerie local ne fonctionne pas correctement (par exemple, blocage ou défaillance du service, ou ressources système faibles), ce qui entraîne l'expiration du serveur et la fermeture de la connexion à Office 365.</span><span class="sxs-lookup"><span data-stu-id="56698-171">Your on-premises messaging server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>
    
- <span data-ttu-id="56698-p115">Il y a des problèmes réseau entre votre environnement local et Office 365. Si le problème persiste, contactez votre équipe réseau pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-p115">There are network issues between your on-premises environment and Office 365. If the problem persists, contact your network team to troubleshoot the issue.</span></span>
    
<span data-ttu-id="56698-174">Déterminez le scénario qui vous concerne et apportez les corrections nécessaires.</span><span class="sxs-lookup"><span data-stu-id="56698-174">Find out which scenario applies to you, and make the necessary corrections.</span></span>
  
<span data-ttu-id="56698-175">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-175">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="56698-176">Code d'erreur : 450 4.7.320 Échec de la validation du certificat</span><span class="sxs-lookup"><span data-stu-id="56698-176">Error code: 450 4.7.320 Certificate validation failed</span></span>
<span data-ttu-id="56698-177"><a name="ErrorCode47320"> </a></span><span class="sxs-lookup"><span data-stu-id="56698-177"></span></span>

<span data-ttu-id="56698-p116">En règle générale, cette erreur signifie qu'Office 365 a rencontré une erreur lors de la tentative de validation du certificat du serveur de messagerie de destination. Les détails de l'erreur expliquent cette dernière. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="56698-p116">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination messaging server. The error details will explain the error. For example:</span></span>
  
- <span data-ttu-id="56698-181">Le certificat est arrivé à expiration.</span><span class="sxs-lookup"><span data-stu-id="56698-181">Certificate expired</span></span>
    
- <span data-ttu-id="56698-182">Le sujet du certificat ne concorde pas.</span><span class="sxs-lookup"><span data-stu-id="56698-182">Certificate subject mismatch</span></span>
    
- <span data-ttu-id="56698-183">Le certificat n'est plus valide.</span><span class="sxs-lookup"><span data-stu-id="56698-183">Certificate is no longer valid</span></span>
    
<span data-ttu-id="56698-184">Corrigez le certificat ou le connecteur afin que les messages mis en file d'attente dans Office 365 puissent être remis.</span><span class="sxs-lookup"><span data-stu-id="56698-184">Please fix the certificate or the connector so that queued messages in Office 365can be delivered.</span></span>
  
<span data-ttu-id="56698-185">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-185">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="other-error-codes"></a><span data-ttu-id="56698-186">Autres codes d'erreur</span><span class="sxs-lookup"><span data-stu-id="56698-186">Other error codes</span></span>
<span data-ttu-id="56698-187"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="56698-187"></span></span>

<span data-ttu-id="56698-p117">Office 365 a des difficultés à remettre des messages à votre serveur de messagerie local ou partenaire. Utilisez les informations sur le **serveur de destination** dans l'erreur afin d'examiner le problème dans votre environnement ou modifiez le connecteur en cas d'erreur de configuration.</span><span class="sxs-lookup"><span data-stu-id="56698-p117">Office 365 is having difficulty delivering messages to your on-premises or partner messaging server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 
  
<span data-ttu-id="56698-190">Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="56698-190">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  

