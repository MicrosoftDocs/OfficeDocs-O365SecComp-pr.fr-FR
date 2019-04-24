---
title: Contrôles de technologie Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: "Résumé: vue d'ensemble des pratiques de contrôle technologique de Microsoft pour Office 365."
ms.openlocfilehash: a8dcb65880fc729fc067b2f2bcf25c7db76dbca9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262336"
---
# <a name="office-365-technology-controls"></a>Contrôles de technologie Office 365 

Microsoft utilise plusieurs outils et technologies pour contrôler, gérer et auditer l'accès aux données client dans Exchange Online et SharePoint Online, y compris la boîte postale scellée et le référentiel sécurisé du client, l'authentification multifacteur, et bien plus encore. Yammer Enterprise utilise des contrôles similaires, comme décrit dans [Yammer Enterprise Access Controls](office-365-yammer-enterprise-access-controls.md).

Les ingénieurs Office 365 disposent d'un accès permanent aux données client d'Office 365 et doivent passer par un processus d'approbation incluant Microsoft et – si le client accorde la fonctionnalité de référentiel sécurisé client pour Exchange Online et SharePoint Online – client approbation, avant l'accès aux données client pour les opérations de service. Lorsque l'approbation est accordée, les comptes d'administration propres au service sont configurés juste-à-temps avec un accès suffisant pour effectuer les tâches requises par la demande de service.

## <a name="lockbox-and-customer-lockbox"></a>Bte post.
Bien qu'il soit extrêmement rare, un client peut demander de l'aide de Microsoft susceptible d'exposer un ingénieur Microsoft sur le contenu du client afin de l'aider à résoudre un problème. Pour contrôler l'accès à Exchange Online (qui inclut toutes les données Skype entreprise stockées dans les boîtes aux lettres des utilisateurs (la couverture Skype entreprise n'inclut pas les enregistrements de diffusion de réunion Skype ni le contenu téléchargé vers les réunions par les utilisateurs)) et SharePoint Online (qui inclut OneDrive entreprise), Microsoft utilise un système de contrôle d'accès appelé Lockbox. Avant de pouvoir accéder à des données ou des systèmes Exchange Online ou SharePoint Online, les ingénieurs Microsoft doivent soumettre une demande d'accès à l'aide de la boîte postale sécurisée. L'utilisation de la boîte postale est requise pour tous les accès élevés à Exchange Online ou SharePoint Online.

Lockbox traite les demandes d'autorisations qui accordent aux ingénieurs la possibilité d'exécuter des fonctions opérationnelles et administratives au sein du service. Les ingénieurs envoient des demandes via la boîte de réception, qui doivent être approuvées par un responsable avant que l'ingénieur ait la possibilité d'accéder aux données client. Lors de l'approbation du responsable, l'ingénieur dispose de l'accès limité au temps et limité à l'étendue aux données client pour fonctionner sur le problème du client.

Le référentiel sécurisé du client pour Office 365 peut vous aider à respecter les obligations de conformité, telles que celles trouvées dans FedRAMP et HIPAA, si vous avez besoin de procédures en place pour l'autorisation explicite de l'accès aux données. Dans l'exemple rare où un ingénieur de service Microsoft a besoin d'accéder à vos données, vous accordez cet accès uniquement aux données requises pour résoudre le problème et pour une durée limitée. Les actions effectuées par l'ingénieur du support technique sont consignées à des fins d'audit et sont accessibles via l' [API activité de gestion d'Office 365](https://msdn.microsoft.com/library/office/dn707383.aspx) et le [Centre de sécurité et de conformité](http://protection.office.com/). Le référentiel sécurisé du client insère le client dans le processus d'approbation de la boîte de réception et lui permet de contrôler l'autorisation de Microsoft Access à son contenu Exchange Online ou SharePoint Online pour les opérations de service.

>**Remarque**: le référentiel sécurisé du client est disponible dans [Office 365 entreprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) et en tant qu'achat de complément, mais une action manuelle doit être effectuée dans le centre d'administration Microsoft 365 (sous paramètres du service | Client Lockbox) pour l'activer. Pour plus d'informations, voir [Demandes Customer Lockbox dans Office 365](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

Toutes les demandes de service pour Exchange Online et SharePoint Online sont gérées par le système bte post. Avec le référentiel sécurisé du client, toute opération de service nécessitant l'accès à ces services avec une exposition aux données client passe par le processus d'approbation de la boîte de réception, puis permet au client d'approuver ou de refuser la demande par la suite.
 
*Figure 1: flux de travail de référentiel sécurisé client*

Si la demande est rejetée par le client, l'ingénieur Microsoft n'aura pas accès au contenu du client et ne pourra pas terminer l'opération de service. Si la demande est approuvée par le client, l'ingénieur Microsoft disposera d'un accès limité en temps réel au contenu du client via des interfaces de gestion contrôlées et restreintes. Avec la zone de gestion des référentiels et le référentiel sécurisé client, tous les accès approuvés sont suivis à un utilisateur unique, ce qui rend les ingénieurs responsables de la gestion des données client.

## <a name="just-in-time-access"></a>Accès juste-à-temps
Microsoft utilise le principe d'accès juste-à-temps (JIT) pour Office 365 afin de réduire davantage le risque de falsification des informations d'identification et les attaques latérales. JIT supprime l'accès administratif permanent aux services et remplace ces droits par la possibilité d'élever ces rôles à la demande. La suppression des droits persistants des administrateurs garantit que les informations d'identification sont disponibles uniquement lorsqu'elles sont nécessaires, et supprime le risque lié à l'entreprise en cas de vol d'informations d'identification.

Le modèle d'accès JIT exige des ingénieurs qui demandent des privilèges élevés pour une période limitée afin d'effectuer des tâches d'administration. En outre, OCEs utilisent des comptes temporaires créés avec des mots de passe complexes générés par l'ordinateur et qui accordent uniquement les rôles leur permettant d'effectuer les tâches nécessaires. Par exemple, l'accès administratif accordé par la boîte de réception est lié au temps et le temps d'accès est accordé dépend du rôle demandé. Un technicien spécifie la durée d'accès requise pendant la demande au système de la boîte postale scellée. Le système de boîte postale scellée rejette les demandes pour lesquelles le temps demandé dépasse le temps maximal autorisé pour l'élévation. Après l'expiration de la demande d'élévation, l'accès administratif est supprimé et le compte temporaire est expiré.

Lorsqu'ils sont autorisés et approuvés pour Access (par exemple, pour déboguer un système), les ingénieurs reçoivent un mot de passe administratif unique qui est généré par le système d'autorisation chaque fois qu'une demande d'accès élevé est approuvée. Ce mot de passe est copié par l'ingénieur dans un mot de passe sécurisé, est différent des informations d'identification de l'ingénieur pour l'environnement d'entreprise Microsoft et n'est valable que pour la session pour laquelle l'accès élevé a été approuvé.

## <a name="constrained-management-interfaces"></a>Interfaces de gestion contraintes
OCEs utilisez deux interfaces de gestion pour effectuer des tâches d'administration: Bureau à distance via des passerelles de service Terminal (TSGs) sécurisées et PowerShell à distance. Dans ces interfaces de gestion, il existe des stratégies logicielles et des contrôles d'accès qui placent des restrictions importantes sur les applications qui peuvent être exécutées, ainsi que sur les commandes et les cmdlets disponibles. 

Les serveurs Office 365 restreignent les sessions simultanées à une session administrateur d'équipe par service, par serveur. Les TSGs sont configurés pour autoriser une seule session simultanée pour les utilisateurs et ils n'autorisent pas plusieurs sessions. TSGs permet aux administrateurs de services Office 365 de se connecter simultanément à plusieurs serveurs, à l'aide d'une seule session par serveur, afin que les administrateurs puissent effectuer efficacement leurs tâches. Les administrateurs d'équipe de service n'ont pas d'autorisations sur le TSGs eux-mêmes. Le TSG est utilisé uniquement pour appliquer les exigences en matière d'authentification multifacteur (MFA) et de chiffrement. Une fois que l'administrateur de l'équipe de service se connecte à un serveur spécifique via un TSG, le serveur spécifique applique une limite de session d'un par administrateur.

Les restrictions d'utilisation et les exigences de connexion et de configuration pour le personnel Office 365 sont établies par les stratégies de groupe Active Directory. Ces stratégies incluent les caractéristiques suivantes:
- TSGs sont configurés pour utiliser uniquement le chiffrement validé [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2
- Les sessions TSG sont configurées pour se déconnecter après 30 minutes d'inactivité
- Les sessions TSG sont configurées pour se déconnecter automatiquement après 24 heures

Les connexions à TSGs nécessitent également l'authentification multiFACTEUR à l'aide d'une carte à puce physique distincte et d'un compte distinct des informations d'identification d'entreprise Microsoft. Les ingénieurs reçoivent différentes cartes à puce pour différentes plateformes et plateformes de gestion de clés secrètes pour garantir le stockage sécurisé des informations d'identification. TSGs utilisez les stratégies de groupe Active Directory pour contrôler qui peut se connecter à des serveurs distants, le nombre de sessions autorisées et les paramètres de délai d'inactivité. Des stratégies supplémentaires sont en place pour limiter l'accès aux applications autorisées et restreindre l'accès à Internet.

En plus de l'accès à distance à l'aide de TSGs spécialement configurés, Exchange Online permet aux utilisateurs disposant du rôle d'ingénieur de service d'accéder à certaines fonctionnalités administratives sur des serveurs de production à l'aide de PowerShell à distance. Pour ce faire, l'utilisateur doit être autorisé à accéder en lecture seule (débogage) à l'environnement de production Office 365. L'escalade des privilèges est activée de la même manière que pour TSGs à l'aide du processus bte post.

Pour l'accès à distance, il existe une adresse IP virtuelle à charge équilibrée sur chaque centre de donnée qui sert de point d'accès unique. Les cmdlets PowerShell disTantes qui peuvent être exécutées sont basées sur le niveau de privilège identifié dans la revendication d'accès obtenue lors de l'authentification. Ces applets de commande sont les seules fonctionnalités d'administration accessibles et exécutées par les utilisateurs qui se connectent à l'aide de cette méthode. Remote PowerShell permet de limiter l'étendue des commandes disponibles pour l'ingénieur, en fonction du niveau d'accès accordé via le processus de la boîte de réception. Par exemple, dans Exchange Online, Get-Mailbox est peut-être disponible, mais Set-Mailbox ne l'est pas.
