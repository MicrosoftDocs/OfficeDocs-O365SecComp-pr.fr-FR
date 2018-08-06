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
# <a name="mail-flow-intelligence-in-office-365"></a>Intelligence de flux de messagerie dans Office 365
  
En règle générale, vous utilisez un connecteur pour router les messages de votre organisation Office 365 vers votre environnement de messagerie local. Vous pouvez également utiliser un connecteur pour router les messages d'Office 365 vers une organisation partenaire. Lorsqu'Office 365 ne peut pas remettre ces messages via le connecteur, ils sont mis en file d'attente dans Office 365. Office 365 continue d'essayer de livrer chaque message pendant 48 heures. Après 48 heures, le message mis en file d'attente arrive à expiration et le message est renvoyé à l'expéditeur d'origine dans une notification d'échec de remise (également appelée notification de non-remise).
  
Office 365 génère une erreur lorsqu'un message ne peut pas être remis à l'aide d'un connecteur. Les erreurs les plus courantes et leurs solutions sont décrites dans cette rubrique. Collectivement, les erreurs de mise en file d'attente et de notification pour les messages non remis envoyés via des connecteurs sont appelées renseignements sur le flux de messagerie.
  
 **Contenu de cette rubrique**
  
- [Code d'erreur : 450 4.4.312 Échec de la requête DNS](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [Code d'erreur : 450 4.4.315 Délai de connexion dépassé](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [Code d'erreur : 450 4.4.316 Connexion refusée.](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [Code d'erreur : 450 4.4.317 La connexion au serveur distant a échoué](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [Code d'erreur : 450 4.4.318 La connexion a été interrompue brusquement](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [Code d'erreur : 450 4.7.320 Échec de la validation du certificat](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a>Code d'erreur : 450 4.4.312 Échec de la requête DNS
<a name="ErrorCode44312"> </a>

En règle générale, cette erreur signifie qu'Office 365 a essayé de se connecter à l'hôte actif qui est spécifié dans le connecteur, mais que la requête DNS permettant de rechercher les adresses IP de l'hôte actif a échoué. Les causes pouvant être à l'origine de cette erreur sont les suivantes :
  
- Il y a un problème avec le service d'hébergement DNS de votre domaine (la partie qui met à jour les serveurs de noms faisant autorité pour votre domaine).
    
- Votre domaine a expiré récemment, l'enregistrement MX ne peut donc pas être extrait.
    
- L'enregistrement MX de votre domaine a récemment été modifié et les serveurs DNS Office 365 disposent toujours des informations DNS précédemment mises en cache pour votre domaine.
    
Vous devez résoudre le problème de DNS en collaborant avec votre service d'hébergement DNS.
  
Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
  
## <a name="error-code-450-44315-connection-timed-out"></a>Code d'erreur : 450 4.4.315 Délai de connexion dépassé
<a name="ErrorCode44315"> </a>

En règle générale, cela signifie qu'Office 365 ne peut pas se connecter au serveur de messagerie de destination. Les détails de l'erreur expliquent le problème. Par exemple :
  
- Votre serveur de messagerie local est arrêté.
    
- Il y a une erreur dans les paramètres d'hôte actif du connecteur, donc Office 365 essaie de se connecter à la mauvaise adresse IP.
    
Déterminez le scénario qui vous concerne et apportez les corrections nécessaires. Par exemple, si le flux de messagerie fonctionne correctement et que vous n'avez pas modifié les paramètres de connecteur, vous devez vérifier dans votre environnement de messagerie local si le serveur est arrêté ou si des modifications ont été apportées à votre infrastructure réseau (par exemple, vous avez changé de fournisseurs de services Internet, donc vous disposez de différentes adresses IP).
  
Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l’origine de l’erreur, vous devez contacter votre partenaire afin de résoudre le problème.
  
## <a name="error-code-450-44316-connection-refused"></a>Code d'erreur : 450 4.4.316 Connexion refusée.
<a name="ErrorCode44316"> </a>

En règle générale, cette erreur signifie qu'Office 365 a rencontré une erreur de connexion lors de la tentative de connexion au serveur de messagerie de destination. Une cause probable de cette erreur est que votre pare-feu bloque les connexions depuis des adresses IP Office 365. Cette erreur peut également être naturelle si vous avez effectué la migration complète de votre système de messagerie local vers Office 365 et éteint votre environnement de messagerie local.
  
- Si vous avez des boîtes aux lettres dans votre environnement local, vous devez modifier vos paramètres de pare-feu pour autoriser les connexions à vos serveurs de messagerie locaux depuis des adresses IP Office 365 sur le port TCP 25. Pour obtenir une liste des adresses IP Office 365, consultez l'article [URL et plages d'adresses IP Office 365](https://go.microsoft.com/fwlink/p/?linkid=228887).
    
- Si aucun autre message ne doit être remis dans votre environnement local, cliquez sur **Fix now** (Corriger maintenant) dans l'alerte afin qu'Office 365 puisse rejeter immédiatement les messages dont les destinataires ne sont pas valides. Cette action réduira le risque de dépasser le quota de destinataires non valides de votre organisation, ce qui peut avoir des répercussions négatives sur la remise normale des messages. Vous pouvez également suivre les instructions suivantes pour résoudre manuellement le problème : 
    
  - Désactivez ou supprimez le connecteur d'Office 365 pour votre environnement local : Centre d'administration Office 365 \> **Centre d'administration** \> **Exchange** \> **Flux de messagerie** \> **Connecteurs** \> sélectionnez le connecteur avec **Office 365** pour valeur **De** et **Serveur de messagerie de votre organisation** pour valeur **À**. Supprimez le connecteur en cliquant sur **Supprimer**![Icône Supprimer](media/ITPro-EAC-DeleteIcon.png) ou désactivez le connecteur en cliquant sur **Modifier**![Icône Modifier](media/ITPro-EAC-EditIcon.png) et en décochant **Activer**.
    
  - Modifiez le domaine accepté dans Office 365 qui est associé à votre environnement de messagerie local en remplaçant **Relais interne** pour **Faisant autorité**. Pour obtenir des instructions, consultez la rubrique [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).
    
    **Remarque**: en règle générale, ces modifications prendront entre 30 minutes et une heure prennent effet. Après une heure, vérifiez que vous ne recevez plus l’erreur.
    
Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a>Code d'erreur : 450 4.4.317 La connexion au serveur distant a échoué
<a name="ErrorCode44317"> </a>

En règle générale, cette erreur signifie qu'Office 365 s'est connecté au serveur de messagerie de destination, mais que le serveur a répondu avec une erreur immédiate ou ne répond pas à la configuration requise en matière de connexion. Les détails de l'erreur expliquent le problème. Par exemple :
  
- Le serveur de messagerie de destination a répondu avec une erreur « Service non disponible », ce qui indique que le serveur ne peut pas maintenir la communication avec Office 365.
    
- Le connecteur est configuré pour exiger TLS, mais le serveur de messagerie de destination ne prend pas en charge ce protocole.
    
Vérifiez les certificats et les paramètres TLS sur vos serveurs de messagerie locaux, ainsi que les paramètres TLS sur le connecteur.
  
Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a>Code d'erreur : 450 4.4.318 La connexion a été interrompue brusquement
<a name="ErrorCode44318"> </a>

En règle générale, cette erreur signifie que la connexion a été coupée car Office 365 a des difficultés à communiquer avec votre environnement de messagerie local. Les causes pouvant être à l'origine de cette erreur sont les suivantes :
  
- Votre pare-feu utilise des règles d'examen de paquet SMTP, lesquelles ne fonctionnent pas correctement.
    
- Votre serveur de messagerie local ne fonctionne pas correctement (par exemple, blocage ou défaillance du service, ou ressources système faibles), ce qui entraîne l'expiration du serveur et la fermeture de la connexion à Office 365.
    
- Il y a des problèmes réseau entre votre environnement local et Office 365. Si le problème persiste, contactez votre équipe réseau pour résoudre le problème.
    
Déterminez le scénario qui vous concerne et apportez les corrections nécessaires.
  
Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
  
## <a name="error-code-450-47320-certificate-validation-failed"></a>Code d'erreur : 450 4.7.320 Échec de la validation du certificat
<a name="ErrorCode47320"> </a>

En règle générale, cette erreur signifie qu'Office 365 a rencontré une erreur lors de la tentative de validation du certificat du serveur de messagerie de destination. Les détails de l'erreur expliquent cette dernière. Par exemple :
  
- Le certificat est arrivé à expiration.
    
- Le sujet du certificat ne concorde pas.
    
- Le certificat n'est plus valide.
    
Corrigez le certificat ou le connecteur afin que les messages mis en file d'attente dans Office 365 puissent être remis.
  
Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
  
## <a name="other-error-codes"></a>Autres codes d'erreur
<a name="sectionSection6"> </a>

Office 365 a des difficultés à remettre des messages à votre serveur de messagerie local ou partenaire. Utilisez les informations sur le **serveur de destination** dans l'erreur afin d'examiner le problème dans votre environnement ou modifiez le connecteur en cas d'erreur de configuration. 
  
Si votre organisation partenaire (par exemple, un fournisseur de services cloud tiers) est à l'origine de l'erreur, vous devez contacter votre partenaire afin de résoudre le problème.
  

