---
title: Suppression de données en ligne Exchange Office 365
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
description: Comment logicielle et matérielle suppressions de données sont gérées dans Exchange Online.
ms.openlocfilehash: 3a17b09e9c21ae309e00bcb0ddc0b51b93478bc1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527953"
---
# <a name="exchange-online-data-deletion-in-office-365"></a>Suppression de données en ligne Exchange dans Office 365
Dans Exchange Online, il existe deux types de suppressions : suppressions logicielles et les suppressions de disque durs. Cela s’applique aux boîtes aux lettres et éléments dans une boîte aux lettres.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Boîtes aux lettres supprimée et supprimée
Une boîte aux lettres utilisateur récupérable est une boîte aux lettres qui a été supprimé à l’aide du centre d’administration Office 365 ou l’applet de commande Remove-Mailbox et a été toujours dans la Corbeille d’Azure Active Directory moins de 30 jours. Une boîte aux lettres peut devenir récupérable dans une des manières suivantes :
- La boîte aux lettres de l’utilisateur associé du compte d’utilisateur est supprimée de Azure Active Directory (l’objet utilisateur est hors de portée ou dans le conteneur recycle bin).
- Compte d’utilisateur de la boîte aux lettres utilisateur associé Azure Active Directory a été supprimée, mais la boîte aux lettres Exchange Online est sous un litige ou blocage eDiscovery.
- La boîte aux lettres utilisateur associé Azure Active Directory compte d’utilisateur a été purgé au cours des 30 derniers jours ; qui est la longueur maximale de rétention Exchange Online conserver la boîte aux lettres dans un état récupérable avant d’être définitivement supprimés définitivement et irrécupérables.

Une boîte aux lettres utilisateur supprimée est une boîte aux lettres qui a été supprimée d’une des manières suivantes :
- La boîte aux lettres de l’utilisateur a été supprimée pendant plus de 30 jours, et l’utilisateur d’Azure Active Directory associé a été supprimée. Tout le contenu tel que les messages électroniques, des contacts et des fichiers de boîte aux lettres sont définitivement supprimées.
- Le compte d’utilisateur associé à la boîte aux lettres de l’utilisateur a été supprimée d’Azure Active Directory. La boîte aux lettres de l’utilisateur est désormais supprimée dans Exchange Online et reste dans un état récupérable pendant 30 jours. Si la période de 30 jours un nouvel utilisateur d’Azure Active Directory est synchronisé dans le compte du destinataire d’origine avec même **ExchangeGuid** ou **ArchiveGuid**et nouveau compte possède une licence pour Exchange Online, il en résulte une suppression du disque dur la boîte aux lettres utilisateur d’origine. Tout le contenu tel que les messages électroniques, des contacts et des fichiers de boîte aux lettres sont définitivement supprimées.
- Une boîte aux lettres supprimée est supprimé à l’aide de **Remove-Mailbox-PermanentlyDelete**.

Les scénarios de suppression ci-dessus supposent que la boîte aux lettres de l’utilisateur n’est pas dans un des États d’attente, comme en attente pour litige ou blocage eDiscovery. S’il existe un type de blocage sur la boîte aux lettres, la boîte aux lettres ne peut pas être supprimée. Pour tous les types de destinataires de messagerie utilisateur, les paramètres de [blocage](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) sont ignorées et n’ont aucun effet sur disque dur suppressions ou récupérable-suppressions.

## <a name="soft-deleted-and-hard-deleted-items"></a>Éléments supprimés et supprimée
Lorsqu’un utilisateur supprime un élément de boîte aux lettres (tel qu’un message électronique, un contact, un rendez-vous du calendrier ou une tâche), l’élément est déplacé vers le dossier éléments récupérables et dans un sous-dossier nommé suppressions. Il est appelé une suppression logicielle. Supprimé la durée pendant laquelle les éléments sont conservés dans les dossier dépend de la période de rétention des éléments supprimés qui est définie pour la boîte aux lettres de suppressions. Une boîte aux lettres Exchange Online conserve les éléments supprimés pendant 14 jours par défaut, mais les administrateurs Exchange Online peuvent modifier ce paramètre pour augmenter la période jusqu'à un maximum de 30 jours. (Pour obtenir la procédure détaillée augmenter la période de rétention des éléments supprimés pour une boîte aux lettres Exchange Online, voir [les éléments de modification de la durée définitivement supprimée sont conservés pendant une boîte aux lettres Exchange Online](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention)). Les utilisateurs peuvent récupérer ou vider, éléments supprimés avant l’expiration de la durée de rétention d’un élément supprimé. Pour ce faire, ils utilisent la fonctionnalité récupérer les éléments supprimés dans Microsoft Outlook ou Outlook sur le web.

Si un utilisateur supprime un élément supprimé à l’aide de la fonctionnalité récupérer les éléments supprimés dans Outlook ou Outlook sur le web, il s’agit d’une suppression de disque dur. Dans Exchange Online, récupération d’élément unique est activée par défaut lorsqu’une nouvelle boîte aux lettres est créé, afin que l’administrateur peut toujours [récupérer](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages) les éléments supprimés définitivement avant l’expiration de la période de rétention des éléments supprimés. En outre, si un message est modifié par un utilisateur ou un processus, les copies de l’élément d’origine sont conservées également lors de la récupération d’élément unique est activée.

## <a name="page-zeroing"></a>Mise à zéro des pages
*Zeroing* est un mécanisme de sécurité qui écrit des zéros ou un modèle binaire sur les données supprimées afin que les données supprimées sont plus difficiles à récupérer. Dans Exchange Online, bases de données de boîtes aux lettres utilisent *pages* en tant que leur unité de stockage et implémentent un processus de remplacement appelé *page mise à zéro*. Page mise à zéro est activée par défaut, et il ne peut pas être désactivée par les clients ou par Microsoft. Page zéro opérations sont enregistrées dans les fichiers journaux des transactions afin que toutes les copies de base de données donné sont page mise à zéro de la même manière. Une page d’une copie de base de données active de mise à zéro, la page obtenir des mises à zéro sur des copies passives de la base de données.

Page mise à zéro écrase un modèle binaire enregistrements supprimée. Le modèle de page de mise à zéro est spécifique aux opérations du moteur ESE (Extensible Storage) (le nom du moteur de base de données interne utilisé par les serveurs dans Exchange Online), et il est différent pour les opérations d’exécution par rapport à des opérations de maintenance de base de données en arrière-plan. (La maintenance de base de données en arrière-plan est un processus en continu les totaux de contrôle et analyses de chaque base de données. Sa fonction principale est de pages de base de données de somme de contrôle, mais il gère également le nettoyage de l’espace et réinitialisation des enregistrements et des pages qui ont été pas à zéro en raison d’une panne de banque d’informations.)

Le tableau suivant répertorie les schémas de remplissage qui correspondent à des opérations d'exécution particulières.

| Opération d’exécution d’ESE   | Modèle de remplissage |
|--------------------------|--------------|
| Remplacement                  | R            |
| Suppression d'enregistrement/de valeur longue | D            |
| Espace de page libéré         | H            |


Le tableau suivant répertorie les schémas de remplissage correspondant à des opérations spécifiques effectuées pendant une opération de maintenance de base de données ESE en arrière-plan.

| Opération de maintenance de base de données ESE en arrière-plan | Modèle de remplissage |
|-----------------------------------------------|--------------|
| Suppression d’enregistrement                                 | D            |
| Suppression de valeur longue                             | L            |
| Espace libéré sur la page partiellement utilisée       | Z            |
| Espace libéré sur la page inutilisée               | U            |


### <a name="page-zeroing-process"></a>Processus de mise à zéro des pages
Le processus de mise à zéro de la page varie selon le scénario de suppression. Le tableau suivant décrit les scénarios de suppression de base de données, et lorsque des fonctions de zéro des pages se produisent.

| Scénario de suppression de base de données | Processus et délai nécessaire à ESE pour mettre à zéro les données de la base de données |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Élément expire en fonction de la période de rétention des éléments supprimés. | Un thread asynchrone écrit un masque binaire sur les données supprimées. Cette action se produit dans les millisecondes suivant la suppression de l'enregistrement. Si le processus de banque se bloque alors que la tâche de mise à zéro asynchrone est toujours en attente (ou que le nettoyage de la banque des versions est annulé en raison de la croissance de la banque d'informations), la mise à zéro est terminée lorsque la maintenance de base de données en arrière-plan traite cette section de la base de données. |
| Scénario d’affichage : Expiration des éléments à partir d’Outlook/Outlook dans l’affichage des dossiers web (par exemple, affichage de Conversation) | La mise à zéro des données a lieu lorsque la maintenance de base de données en arrière-plan traite cette section de la base de données. |
| Scénario de déplacement/suppression boîte aux lettres : Boîte aux lettres Source supprimée (expiration de la boîte aux lettres supprimée) | La mise à zéro des données a lieu lorsque la maintenance de base de données en arrière-plan traite cette section de la base de données. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Types de données de boîte aux lettres sans mise à zéro des pages
Les types de données de boîtes aux lettres suivantes n’ont aucuns dispositions pour la page mise à zéro :
- **Journaux de transactions de base de données de boîte aux lettres** - lorsque les journaux de transactions sont supprimés dans le cadre d’opérations normales, il n’existe aucun processus de mise à zéro les blocs dans le système de fichiers stockés les fichiers journaux supprimés. Il est probable que le système de fichiers sera rapidement réutiliser cet espace libre pour les nouveaux fichiers journaux, mais il n’existe aucune garantie que cela se produit.
- **Fichiers de catalogue d’index de contenu** - Exchange Online utilise recherche Foundation (également appelé rapide) pour les fonctionnalités d’indexation de recherche. Le catalogue d’indexation de recherche est composé de plusieurs douzaines fichiers stockés sur le même volume que le fichier de base de données de boîtes aux lettres. Lorsqu’un message est supprimée de la base de données de boîte aux lettres, le contenu associé dans le catalogue de recherche n’est pas immédiatement supprimé. Suppression du contenu se produit lorsque Search Foundation effectue une ombre ou fusion principale de fichiers catalogue petite dans un seul fichier plus volumineux. Une fois la fusion principale terminée, les fichiers de catalogue plus petites sont supprimés. Il n’existe aucun processus de mise à zéro les blocs qui stocké les fichiers de catalogue supprimé.

## <a name="continuous-replication"></a>Réplication continue
Réplication continue (également appelé envoi de journaux et de relecture) est la technologie dans Exchange Online qui crée et conserve des copies de chaque base de données de boîtes aux lettres pour fournir une haute disponibilité et résilience de site, la récupération d’urgence. Réplication continue tire parti de la prise en charge de la récupération des blocages Exchange Server de base de données pour fournir la technologie qui effectue la mise à jour asynchrone d’une ou plusieurs copies de base de données de boîtes aux lettres. Chaque serveur de boîtes aux lettres enregistre les mises à jour de base de données sur une base de données active (par exemple, activité de messagerie utilisateur) en tant qu’enregistrements du journal dans un ensemble de fichiers journaux des transactions 1 Mo séquentiel. Cet ensemble de fichiers est appelé flux du journal. Réplication continue, flux du journal sert également mettre à jour de manière asynchrone une ou plusieurs copies de base de données. Cette opération s’effectue en transmettant les journaux vers un emplacement contenant une copie passive de la base de données active et leur relecture puis dans la copie passive de base de données. Si tous les journaux de la base de données active sont relus selon une copie passive de base de données, puis les deux bases de données sont les mêmes, et il est par le biais de ce processus que toute modification physique apportée à une base de données active est répliquée sur toutes les copies passives de cette base de données.

Toute suppression d’une base de données de boîtes aux lettres, si un élément de boîte aux lettres ou d’une boîte aux lettres entière et, si une suppression logicielle ou une suppression définitive, représente une modification physique à la base de données active. Page mise à zéro également implique d’apporter des modifications physiques à la base de données active. Ces modifications sont écrites dans les fichiers journaux via un processus appelé réplication continue et lorsque ces fichiers journaux sont relus copies passives de base de données, les mêmes modifications physiques sont apportées à ces bases de données passives.