---
title: Contrôles de la technologie Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Vue d’ensemble des pratiques de contrôle de la technologie de Microsoft pour Office 365.'
ms.openlocfilehash: 2ef04b558f5fa82075d9aa602b83d437aa4b2ee6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527991"
---
# <a name="office-365-technology-controls"></a>Contrôles de la technologie Office 365 

Microsoft utilise plusieurs outils et technologies pour contrôler, gérer et d’audit de l’accès aux données client dans Exchange Online et SharePoint Online, y compris la zone de sécurité et de zone de sécurité client, l’authentification multifacteur et plus. Yammer Enterprise utilise des contrôles similaires, comme décrit dans les [Contrôles d’accès entreprise Yammer](office-365-yammer-enterprise-access-controls.md).

Ingénieurs d’Office 365 aient zéro permanent un accès aux données des clients Office 365, et ils doivent passer par un processus d’approbation qui inclut Microsoft et – si le client licences la fonctionnalité de zone de sécurité client pour Exchange Online et SharePoint Online – client approbation, avant l’accès aux données client pour les opérations de service peuvent se produire. Lors de l’approbation est accordée, les comptes d’administration spécifiques à un service sont mis en service juste-à-temps avec juste un accès pour effectuer les tâches requises par la demande de service.

## <a name="lockbox-and-customer-lockbox"></a>Zone de sécurité et de la zone de sécurité client
Bien qu’il soit très rare, un client peut demander une assistance de Microsoft, qui peut-être exposer un ingénieur Microsoft pour le contenu du client pour les aider à un problème. Pour contrôler l’accès à Exchange Online (qui inclut tout Skype pour les données métiers stockées dans les boîtes aux lettres des utilisateurs (Skype pour la couverture d’entreprise n’inclut pas Skype réunion diffusion des enregistrements ou le contenu téléchargé à des réunions par les utilisateurs)) et SharePoint Online (qui inclut OneDrive entreprise), Microsoft utilise un système de contrôle d’accès appelé zone de sécurité. Avant tout ingénieur Microsoft permettre accéder aux données ni systèmes Exchange Online ou SharePoint Online, ils doivent envoyer une demande d’accès à l’aide de la zone de sécurité. À l’aide de la zone de sécurité est requis pour tous les accès avec élévation de privilèges à Exchange Online ou SharePoint Online.

Zone de sécurité traite les demandes d’autorisation qui accordent les ingénieurs la possibilité d’exécuter des fonctions opérationnelles et administratives au sein du service. Demandes d’envoi ingénieurs par le biais de zone de sécurité, qui doit être approuvée par un responsable avant l’ingénieur a la possibilité d’accéder aux données client. Lors de l’approbation du responsable, l’ingénieur est limitée dans le temps et limitée à la portée de l’accès aux données client pour travailler sur le problème du client.

Zone de sécurité client pour Office 365 peut vous aider à répondre aux obligations de conformité, telles que celles trouvées dans FedRAMP et HIPAA, si vous avez besoin en place des procédures pour l’autorisation d’accès de données explicites. Dans l’instance rare lorsqu’un technicien du service Microsoft doit accéder à vos données, vous accordez que l’accès uniquement aux données nécessaires pour résoudre le problème et pour une durée limitée. Actions effectuées par l’ingénieur du support technique sont consignées à des fins d’audit et sont accessibles par le biais de l' [API d’activité Office 365 gestion](https://msdn.microsoft.com/library/office/dn707383.aspx) et [sécurité et le centre de conformité](http://protection.office.com/). Zone de sécurité client insère le client dans le processus d’approbation de zone de sécurité et les fournit la capacité à contrôler l’autorisation d’accès de Microsoft à leurs Exchange Online ou SharePoint Online pour les opérations de service.

>**Remarque**: zone de sécurité client est disponible dans [Office 365 entreprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) et comme un achat de module complémentaire, mais manuelle mesures dans le centre d’administration Office 365 (sous paramètres de Service | Client zone de sécurité) pour l’activer. Pour plus d’informations, voir [Demandes de zone de sécurité du client Office 365](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

Toutes les demandes de service pour Exchange Online et SharePoint Online sont gérés par le système de zone de sécurité. Et avec une zone de sécurité client, aucune opération de service nécessitant l’accès à ces services avec l’exposition aux données client passe par le processus d’approbation de zone de sécurité, puis permet au client approuver ou refuser la demande par la suite.
 
*Figure 1 : flux de travail de zone de sécurité client*

Si la demande est rejetée par le client, l’ingénieur Microsoft n’auront pas accès au contenu du client et ne sera pas en mesure d’effectuer l’opération de service. Si la demande est approuvée par le client, l’ingénieur Microsoft sera accès est limité juste-à-temps pour le contenu du client par le biais des interfaces de gestion contrôlée et limitée. Zone de sécurité et zone de sécurité client, tous les accès approuvé sont conforme à un utilisateur unique, rendant ingénieurs responsables de leur gestion des données du client.

## <a name="just-in-time-access"></a>Accès juste-à-temps
Microsoft utilise le principe d’accès juste-à-temps (juste) pour Office 365 pour atténuer les risques d’attaques latérales et de la falsification des informations d’identification. JUSTE supprime un accès administratif permanent aux services et remplace les droits d’accès avec la possibilité d’élever dans ces rôles à la demande. Suppression permanente par des droits d’administrateurs garantit que les informations d’identification sont disponibles uniquement lorsqu’ils sont nécessaires et supprime le risque à l’entreprise en cas de vol d’informations d’identification.

Le modèle d’accès juste nécessite ingénieurs demander des privilèges élevés pour une durée limitée effectuer les tâches d’administration. En outre, OCEs utiliser des comptes temporaires qui sont créés avec des mots de passe complexes générées par ordinateur et accordé uniquement les rôles qui leur permettent d’effectuer les tâches nécessaires. Par exemple, accès administratif accordé par la zone de sécurité est liés au temps, et la durée pendant laquelle l’accès est accordé dépend du rôle demandé. Un technicien spécifie la durée d’accès temps requis lors de la demande au système de zone de sécurité. Le système de zone de sécurité rejette les demandes où l’heure demandée dépasse le maximum autorisé de temps pour l’élévation. Après expiration de la demande l’élévation, accès administratif est supprimé et le compte temporaire a expiré.

Lorsque autorisés et approuvés pour l’accès (par exemple, pour déboguer un système), ingénieurs reçoivent un mot de passe d’administration utilisation unique qui est généré par le système d’autorisation chaque fois qu’une demande d’accès avec des privilèges élevés est approuvée. Ce mot de passe est copié par le technicien dans un mot de passe sécurisé, séparé à partir des informations d’identification de l’ingénieur pour l’environnement d’entreprise de Microsoft et est utile uniquement pour la session pour laquelle avec élévation de privilèges d’accès a été approuvée.

## <a name="constrained-management-interfaces"></a>Interfaces de gestion de contrainte
OCEs utiliser deux interfaces de gestion pour effectuer des tâches d’administration : Bureau à distance par le biais de passerelles de services Terminal Server sécurisés (STG) et PowerShell à distance. Dans la gestion de ces interfaces, il existe des stratégies de logiciel et accéder à des contrôles qui effectuent des restrictions importantes sur les applications peuvent être exécutées et les commandes et les applets de commande sont disponibles. 

Serveurs Office 365 restreindre les sessions simultanées à un administrateur de l’équipe par service de session, par serveur. STG est configurés pour autoriser uniquement une seule session simultanée pour les utilisateurs, et ils n’autorisent pas plusieurs sessions. STG permettre aux administrateurs de l’équipe de service Office 365 se connecter à plusieurs serveurs simultanément, à l’aide d’une seule session par serveur, afin que les administrateurs peuvent exécuter efficacement leurs tâches. Administrateurs de l’équipe de service n’ont pas toutes les autorisations sur les TSG eux-mêmes. Le TSG sert uniquement à appliquer l’authentification multifacteur (MFA) et cryptage. Une fois que l’administrateur de l’équipe de service se connecte à un serveur spécifique via un TSG, le serveur spécifique applique une limite de session d’une par l’administrateur.

Restrictions d’utilisation et de la connexion et la configuration requise pour Office 365 personnel est établis par les stratégies de groupe Active Directory. Ces stratégies incluent les caractéristiques suivantes :
- STG est configurés pour utiliser uniquement [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2 validé chiffrement
- Sessions TSG sont configurées pour déconnecter après 30 minutes d’inactivité
- Sessions TSG sont configurées pour se connecter automatiquement désactiver après 24 heures

Connexions à STG nécessitent également MFA à l’aide d’une carte à puce physique distincte et un compte distinct des informations d’identification d’entreprise de l’ingénieur Microsoft. Ingénieurs sont émis les cartes à puce différents pour les différentes plateformes et plates-formes de gestion de clés secrètes sont utilisées pour garantir un stockage sécurisé des informations d’identification. STG utiliser des stratégies de groupe Active Directory pour contrôler les personnes qui peuvent se connecter à des serveurs distants, le nombre de sessions autorisées et les paramètres de délai d’inactivité. Les stratégies supplémentaires sont mis en place pour limiter l’accès aux applications autorisées et à restreindre l’accès à Internet.

En plus de l’accès à distance à l’aide de STG spécialement configuré, Exchange Online permet aux utilisateurs avec le rôle d’opérations ingénieur de Service accéder à certaines fonctionnalités d’administration sur les serveurs de production à l’aide de PowerShell à distance. Pour ce faire, l’utilisateur doit être autorisé pour l’accès en lecture seule (débogage) dans l’environnement de production d’Office 365. Élévation des privilèges sont activé de la même manière qu’il est activé pour STG à l’aide du processus de la zone de sécurité.

Pour l’accès distant, il est une adresse IP virtuelle à charge équilibrée à chaque centre de données qui sert de point d’accès unique. Les applets de commande PowerShell à distance pouvant être exécutées sont basées sur le niveau de privilège identifié dans la demande d’accès obtenue lors de l’authentification. Ces applets de commande sont les fonctionnalités uniquement d’administration qui sont accessibles et exécutées par les utilisateurs se connectent à l’aide de cette méthode. PowerShell distant est utilisé pour limiter l’étendue des commandes disponibles à l’ingénieur, lequel est basé sur le niveau d’accès accordé par le biais du processus de zone de sécurité. Par exemple, dans Exchange Online, Get-Mailbox est peut-être disponible, mais Set-Mailbox ne serait pas.
