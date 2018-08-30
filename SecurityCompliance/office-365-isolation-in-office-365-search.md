---
title: Isolation du locataire Office 365 dans Office 365 Search
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
description: 'Résumé : Une explication de l’isolation du locataire dans Office 365 Search.'
ms.openlocfilehash: cc73f3c157ffd20b3891a6b7c58e7d0b2adf4e55
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527500"
---
# <a name="tenant-isolation-in-office-365-search"></a>Isolation du locataire de la recherche Office 365
Recherche SharePoint Online utilise un modèle de séparation de client qui équilibre l’efficacité des structures de données partagées avec protection contre les fuites entre les utilisateurs des informations. Avec ce modèle, nous empêcher les fonctionnalités de recherche à partir de :
- Renvoi des résultats de requête contenant des documents à partir d’autres clients
- Exposition de suffisamment d’informations dans les résultats de requête qu’un utilisateur expérimenté peut en déduire plus d’informations sur les autres clients
- Schéma d’affichage ou les paramètres à partir d’un autre client
- Mélange analytique traitement des informations entre des clients ou des résultats de la banque dans le client incorrect
- À l’aide des entrées de dictionnaire à partir d’un autre client

Pour chaque type de données du client, nous utilisons une ou plusieurs couches de protection dans le code pour empêcher la fuite accidentelle des informations. Les données critiques ont la plupart des couches de protection pour vous assurer qu’un seul défaut ne produit pas fuite d’informations réelles ou perçues.

## <a name="tenant-separation-for-the-search-index"></a>Séparation du client pour l’Index de recherche
L’index de recherche est stockée sur le disque dans les serveurs qui hébergent les composants d’index et les locataires partagent les fichiers d’index. Documents indexés d’un client sont visibles uniquement pour les requêtes pour ce client. Trois mécanismes indépendants empêchent la fuite d’informations :
- Filtrage des ID client
- Préfixe du terme client ID
- Vérifier des listes ACL

Tous les trois mécanismes devrait échouer pour la recherche renvoyer les documents au client incorrect.

## <a name="tenant-id-filtering-and-tenant-id-term-prefixing"></a>Le filtrage des ID client et le terme d’ID de client faisant précéder
Préfixes recherche tous les termes qui est indexée dans l’index de texte intégral avec l’ID de client. Par exemple, lorsque le terme «*foo*» est indexé pour un client avec l’ID «*123*», l’entrée dans l’index de texte intégral est «*123foo.*»

Chaque requête est convertie pour inclure l’ID de client à l’aide d’un processus appelé filtrage des ID de client. Par exemple, la requête «*foo*» est convertie en « <*guid*>. *foo* ET *l’ID client sur*: <*guid*> «, où <*guid*> représente le client effectue la requête. Conversion de cette requête se produit au sein de chaque nœud d’index et il peut influencer la transformation de requête, ni le contenu. Étant donné que l’ID de client est ajouté à chaque requête, la fréquence d’un terme dans d’autres clients ne peuvent pas déduite en examinant le meilleur correspondance de classement dans un client.

Préfixe du terme client ID se produit uniquement dans l’index de texte intégral. Recherches saisies, tel que «*titre : foo*», accédez à un index de recherche synthétique où les termes ne sont pas signalées par ID de locataire. Au lieu de cela, les recherches saisies ont pour préfixe le nom du champ. Par exemple, la requête «*titre : foo*» est convertie en «*fields.title:foo fields.tenantID et*: <*guid*>. » Étant donné que la fréquence d’un terme n’influence le classement de correspondances dans l’index de recherche synthétique, il est inutile de séparation du client en ajoutant des termes. Pour une recherche saisie comme «*titre : foo*», séparation contenu client dépend de conversion de requête de filtrage des ID de client.

## <a name="document-access-control-list-checks"></a>Vérification de la liste document Access contrôle
Recherche contrôle l’accès à des documents par le biais de listes ACL qui est enregistrés dans l’index de recherche. Chaque élément est indexée avec un ensemble de termes dans un champ de liste ACL spécial. Le champ de liste ACL contient un terme par groupe ou l’utilisateur qui peut afficher le document. Chaque requête est assorti d’une liste de termes accès au contrôle d’entrée, un pour chaque groupe auquel appartient l’utilisateur authentifié.

Par exemple, une requête comme « <*guid*>. *foo ID client sur AND*: <*guid*> » devient : « <*guid*>. *foo ID client sur AND*: <*guid*> *AND* (*docACL :*<*ace1*> *ou docACL*: <*ace2*> *ou docACL*: <*ace3*> *... *)"

Étant donné qu’utilisateur et les identificateurs de groupe et, par conséquent, ACE est uniques, cela offre un niveau supplémentaire de sécurité entre les clients pour les documents qui sont uniquement visibles à certains utilisateurs. Les mêmes sont le cas pour la spéciale « tout le monde, à l’exception des utilisateurs externes » ACE qui autorise l’accès pour les utilisateurs classiques dans le client. Mais dans la mesure où ACE pour « Tout le monde » est les mêmes pour tous les clients, séparation du client pour les documents publics dépend du filtrage des ID client. Refuser l’accès Qu'ace également pris en charge. L’augmentation de la requête ajoute une clause qui supprime un document à partir du résultat lorsqu’il existe une correspondance avec un ACE Refuser.

Dans la recherche Exchange Online, l’index est partitionné sur l’ID de boîte aux lettres pour les boîtes aux lettres d’utilisateur individuel au lieu de l’ID de client (ID d’abonnement) comme dans SharePoint Online. Le mécanisme de partitionnement est identique à SharePoint Online, mais il n’existe pas de liste ACL le filtrage.
