---
title: Vue d’ensemble des stratégies de conservation
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 4/3/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 9c3b1d52-40ce-4ba3-a520-9ae0be15538a
description: Pour respecter les réglementations ou les règles internes, les organisations souhaitent conserver le contenu d’un certain temps. Avec une stratégie de conservation dans Office 365, vous pouvez conserver le contenu de sites, les boîtes aux lettres et les dossiers publics indéfiniment ou pendant une durée spécifique. Vous pouvez également filtrer le contenu sera conservé en fournissant des mots clés ou une plage de dates pour affiner les résultats.
ms.openlocfilehash: a26b85a563dd0e6f9ed8a70bfe9a310fc89a50f2
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272459"
---
# <a name="overview-of-preservation-policies"></a>Vue d’ensemble des stratégies de conservation

> [!IMPORTANT]
> Si vous utilisez une stratégie de conservation, cette stratégie a été convertie à une stratégie de rétention, qui est une nouvelle fonctionnalité qui fait tout qu'une stratégie de conservation et bien plus encore. La stratégie de conservation continuera à fonctionner et conserver votre contenu sans nécessiter la modification de votre part. Vous trouverez ces stratégies dans la page de **rétention** dans la sécurité &amp; centre de conformité. Pour plus d’informations, voir [que sont devenus les stratégies de conservation ?](retention-policies.md#what-happened-to-preservation-policies)
  
Pour respecter les réglementations ou les règles internes, les organisations souhaitent conserver le contenu d’un certain temps. Avec une stratégie de conservation dans Office 365, vous pouvez conserver le contenu de sites, les boîtes aux lettres et les dossiers publics indéfiniment ou pendant une durée spécifique. Vous pouvez également filtrer le contenu sera conservé en fournissant des mots clés ou une plage de dates pour affiner les résultats.
  
Par exemple, vous pouvez conserver le contenu dans les sites appartenant au service Ventes sept ans et de boîtes aux lettres spécifiques et affiner l’étendue de la stratégie en disant que vous souhaitez conserver uniquement le contenu à partir de ces deux dernières années contenant une spécifique nom du client.
  
Lorsque le contenu est soumis à une stratégie de conservation, les utilisateurs peuvent continuer à modifier et travailler avec le contenu comme si rien n’est modifié, car du contenu conservé en place, dans son emplacement d’origine. Mais si quelqu'un modifie ou supprime le contenu qui est soumis à la stratégie, une copie est enregistrée à un emplacement où il est conservé pendant que la stratégie est en vigueur.
  
Enfin, certaines organisations devrez conforme aux règles définies par les organismes tels que la Securities and Exchange Commission (SEC) règle 17 a-4, ce qui implique qu’après qu’une stratégie de conservation est activée, il ne peut pas être désactivé ou établie moins restrictive. Pour répondre à cette exigence, vous pouvez utiliser le verrouillage de conservation. Après une stratégie de verrouillé, personne, y compris l’administrateur — peut désactiver la stratégie ou rendre moins restrictives.
  
Créer et gérer des stratégies de conservation sur la page de rétention de sécurité Office 365 &amp; centre de conformité.
  
![Page de rétention dans Office 365 sécurité &amp; centre de conformité](media/edb2e228-efff-4619-89d1-8665b5f38639.png)
  
> [!NOTE]
> Pour inclure une boîte aux lettres Exchange Online dans une stratégie de conservation, la boîte aux lettres doit être attribué une licence Exchange Online Plan 2. Si une boîte aux lettres est attribué une licence Exchange Online Plan 1, vous devez attribuer une licence séparée de l’archivage Exchange Online pour l’inclure dans une stratégie de conservation. 
  
## <a name="how-a-preservation-policy-works-with-content-in-place"></a>Fonctionnement d’une stratégie de conservation avec du contenu sur place

Lorsque vous incluez un site, une boîte aux lettres ou un dossier public d’une stratégie de conservation, le contenu reste dans son emplacement d’origine. Personnes peuvent continuer à travailler avec leurs documents ou de messagerie, mais une copie du contenu telle qu’elle existait lorsque vous avez lancé la stratégie est conservée. Pour les sites, contenu est conservé dans la bibliothèque de conservation permanente ; pour les boîtes aux lettres et de dossiers publics, contenu est conservé dans le dossier éléments récupérables. Ces emplacements sécurisés et le contenu conservé ne sont pas visibles pour la plupart des personnes. Avec une stratégie de conservation, personnes est même inutile de connaître que leur contenu est soumis à la stratégie.
  
![Diagramme illustrant le fonctionnement des stratégies de conservation](media/2c1dd82b-84e0-49e0-ab46-d017df297040.png)
  
### <a name="site-content"></a>Contenu du site

Une stratégie de conservation est appliquée au niveau d’un site. Lorsque vous incluez un site dans une stratégie de conservation, une bibliothèque de conservation permanente est créée, s’il n’existe pas déjà. La plupart des utilisateurs ne peuvent pas afficher la bibliothèque de conservation permanente car elle est visible uniquement par les propriétaires de collection de sites.
  
Si un utilisateur essaie de modifier ou supprimer du contenu dans un site qui est soumis à une stratégie de conservation, tout d’abord la stratégie vérifie si le contenu de l’été modifié depuis la stratégie a été appliquée. S’il s’agit de la première modification dans la mesure où la stratégie de conservation a été appliquée, la stratégie de copie le contenu dans la bibliothèque de conservation permanente, puis permet à la personne à modifier ou supprimer le contenu d’origine. Notez que tout le contenu du site peut être copié dans la bibliothèque de conservation permanente, même si le contenu ne correspond pas au filtre de la requête utilisée par la stratégie de conservation.
  
Ensuite, un travail du minuteur nettoie la bibliothèque de conservation. Le travail du minuteur s’exécute périodiquement et compare tout le contenu de la bibliothèque de conservation aux filtres utilisés par les stratégies de conservation sur le site. À moins que le contenu corresponde à au moins un des filtres, le travail du minuteur supprime définitivement le contenu de la bibliothèque de conservation.
  
La commande précédente s’applique au contenu qui existe lors de la stratégie de conservation est appliquée. En outre, tout nouveau contenu qui a créé ou ajouté au site, une fois qu’il a été inclus dans la stratégie est conservé après la suppression. Toutefois, nouveau contenu n’est pas copié dans l’heure de bibliothèque du premier conservation maintenez qu'il est modifié uniquement lorsqu’il est supprimé. Pour conserver les versions de tous les fichiers, vous devez activer le contrôle de version, consultez la section sur le contrôle de version.
  
### <a name="mailbox-and-public-folder-content"></a>Contenu de boîtes aux lettres et de dossiers publics

Pour le courrier d'un utilisateur et d'autres éléments, une stratégie de conservation est appliquée au niveau d'une boîte aux lettres. Pour un dossier public, une stratégie de conservation est appliquée au niveau du dossier, et non au niveau de la boîte aux lettres. Les boîtes aux lettres et les dossiers publics utilisent le dossier Éléments récupérables pour conserver des éléments. Seules les personnes disposant d’autorisations de découverte électronique peuvent afficher le dossier Éléments récupérables d'un autre utilisateur.  
  
Par défaut, lorsqu’une personne supprime un message dans un dossier autre que le dossier éléments supprimés, le message est déplacé vers le dossier éléments supprimés. Lorsqu’une personne supprime un élément à partir du dossier éléments supprimés, le message est déplacé vers le dossier éléments récupérables et disparaît de la vue de l’utilisateur. En outre, une personne peut supprimer logicielle d’un élément (MAJ + SUPPR) dans n’importe quel dossier, ce qui ignore le dossier éléments supprimés et place l’élément directement dans le dossier éléments récupérables.
  
Lorsqu’une boîte aux lettres est incluse dans une stratégie de conservation, les éléments supprimés sont déplacés dans le dossier de conservation de découverte à l’intérieur du dossier Éléments récupérables. Lorsque l’Assistant de boîte aux lettres traite périodiquement la boîte aux lettres, il évalue les messages dans ce dossier. À moins que le contenu corresponde à au moins un des filtres utilisés par une stratégie de conservation, l’Assistant de boîte aux lettres supprime définitivement le contenu du dossier Éléments récupérables.
  
Le dossier éléments récupérables contient également un dossier Versions. Lorsqu’une personne tente de modifier certaines propriétés d’un élément de boîte aux lettres, telles que l’objet, corps, pièces jointes, les expéditeurs et destinataires, ou date envoyé ou reçu un message, une copie de l’élément d’origine est enregistrée dans le dossier de Versions avant la modification. Cela se produit pour chaque modification ultérieure. Après la suppression de la stratégie de conservation, copies dans le dossier de Versions sont supprimés par l’assistant de boîte aux lettres.
  
### <a name="where-a-preservation-policy-is-stored"></a>Emplacement de stockage d’une stratégie de conservation

Lorsque vous créez une stratégie de conservation, il est stocké de façon centralisée de la sécurité &amp; centre de conformité, puis déployés vers différentes sources de contenu qui inclut la stratégie, tels que des sites, des boîtes aux lettres et des dossiers publics.
  
Une fois la stratégie de conservation déployée vers ces sources de contenu, elle fonctionne exactement comme une archive permanente eDiscovery. Pour plus d’informations sur les archives permanentes, consultez :
  
- [Vue d’ensemble d’eDiscovery et archives permanentes](https://go.microsoft.com/fwlink/p/?LinkID=404352) (SharePoint Online) 
    
- [Mise en attente et en attente pour litige in-Place](https://go.microsoft.com/fwlink/p/?LinkID=404353) (Exchange Online) 
    
- [Dossier éléments récupérables](https://go.microsoft.com/fwlink/p/?LinkID=404354) (Exchange Online) 
    
### <a name="preservation-policy-vs-ediscovery-hold"></a>Stratégie de conservation et blocage eDiscovery

S’il est vrai que ces deux fonctionnalités bloquer le contenu, ces fonctionnalités ne doivent pas être confondues, car ils ont des objectifs différents :
  
- **Si vous souhaitez conserver le contenu dans le cadre d’une spécification de rétention, utilisez une stratégie de conservation.** Par exemple, si vous souhaitez conserver le contenu dans le cadre de votre plan de rétention de sept ans, utilisez une stratégie de conservation. Une stratégie de conservation permettre conserver le contenu pour une période spécifique, et à la fin de cette période, du contenu publié automatiquement à partir de la stratégie. La stratégie peut également être verrouillée afin que personne ne peut désactiver la stratégie ou rendre moins restrictives. Un blocage eDiscovery ne peut pas être verrouillé ou spécifiez une période de temps. En outre, une stratégie de conservation a généralement une durée d’années, alors qu’un blocage eDiscovery est temporaire et couramment dure uniquement la durée d’une affaire juridique. 
    
    En outre, vous pouvez créer une stratégie de conservation sans les étapes supplémentaires qu’eDiscovery peut-être nécessiter, telles que la création des cas, l’ajout de membres, ou effectuant le contenu de recherche.
    
- **Si vous souhaitez bloquer le contenu dans le cadre d’une demande juridique ou eDiscovery, utilisez un blocage eDiscovery.** Par exemple, si vous souhaitez bloquer le contenu dans des emplacements spécifiques dans le cadre d’une demande juridique, utilisez un blocage eDiscovery. Dans la découverte électronique, le contenu pertinent pour un cas est généralement sensible ou privilégiés, donc différents cas peuvent être limités aux différents membres. En outre, eDiscovery prend en charge les recherches de contenu peuvent être enregistrées, aperçus, analysées avec eDiscovery avancée, ou ont les résultats exportés. 
    
    Contrairement à une stratégie de conservation, un blocage eDiscovery ne peut pas spécifier une période de temps : un blocage eDiscovery est en vigueur jusqu'à ce que vous le désactivez ou le supprimer. En outre, un blocage eDiscovery ne peut pas être verrouillé.
    
## <a name="how-a-preservation-policy-works-with-document-versions-in-a-site"></a>Fonctionnement d’une stratégie de conservation avec les versions d’un document dans un site

Une stratégie de conservation ne conserve automatiquement toutes les versions d’un document dans un site. Pour ce faire, vous devez activer le contrôle de version pour les bibliothèques de documents dans le site. Pour plus d’informations, voir [Activer et configurer le contrôle de version pour une liste ou une bibliothèque](https://go.microsoft.com/fwlink/p/?LinkID=404350).
  
Si un document est supprimé d’un site qui est conservé et le contrôle de version est activé pour la bibliothèque, toutes les versions du document supprimé sont conservées. 
  
Si le contrôle de version n’est pas activé et un élément est soumis à plusieurs stratégies de conservation, la version est conservée est celle qui est actif lorsque chaque stratégie de conservation prend effet. Par exemple, si la version 27 d’un élément est la plus récente lorsque le site est conservé la première fois et version 51 est la plus récente lorsque le site est conservé la deuxième fois, versions 27 et 51 sont conservés.
  
## <a name="filtering-a-preservation-policy"></a>Filtrage d’une stratégie de conservation

Vous pouvez affiner le contenu soumis à une stratégie de conservation en ajoutant des mots clés ou une plage de dates à la stratégie. 
  
![Utilisations de mots clés et de plages de dates comme filtres lors de la création d’une stratégie de conservation](media/603cef40-8f7c-4140-956f-28c092273582.png)
  
### <a name="filter-by-using-keywords"></a>Filtrage à l’aide de mots clés

Une stratégie de conservation prend en charge le langage de requête de mot clé (KQL). Par exemple, vous pouvez utiliser les opérateurs de base et like et ou, et vous pouvez effectuer une recherche de proximité où « marketing de NEAR(30) wingtip » identifie les résultats où « wingtip » est de 30 caractères de « marketing ». Une requête de mots-clés vous permet d’identifier et de conserver uniquement le contenu pertinent.
  
### <a name="filter-by-using-a-date-range"></a>Filtrage à l’aide d’une plage de dates

Vous pouvez également filtrer la stratégie pour qu’elle ne conserve que le contenu dans une plage de dates spécifique. Pour les messages, la date est relative à la date de réception, et pour les documents et les sites, la date est relative à la date de modification. Cela signifie que vous pouvez conserver le contenu qui comprend le courrier reçu et les documents modifiés dans une plage de dates spécifique ou avant ou après une date de début ou de fin.
  
## <a name="preserving-content-for-a-specific-period-of-time"></a>Conservation du contenu pendant une période de temps spécifique

Avec une stratégie de conservation, vous pouvez conserver le contenu indéfiniment ou pendant un nombre de jours, de mois, voire d’années spécifique. Notez que la durée pendant laquelle le contenu est conservé est calculée à partir de l’âge du contenu, et non à partir de la date de création de la stratégie de conservation. 
  
Par exemple, si vous souhaitez conserver le contenu d’un site de sept ans et d’un document dans ce site n’a pas été modifié dans les six ans, le document sera conservé pour seulement une autre année s’il n’est pas modifié. Si le document est modifié à nouveau, la durée de vie du document est calculée à partir de la nouvelle date de dernière modification, et il sera conservé pour un autre sept ans.
  
De même, si vous souhaitez conserver le contenu d’une boîte aux lettres pendant sept ans, et qu’un message a été envoyé il y a six ans, le message sera conservé pendant une seule année, sauf si la date de réception est modifiée. Dans ce cas, une nouvelle version du message tel qu’il existait avant d’être modifié est conservée dans le dossier Éléments récupérables, et l’âge du message est calculé à partir de la nouvelle date de réception, et il sera conservé pendant sept années supplémentaires.
  
![Paramètre de durée pour une nouvelle stratégie de conservation](media/455aac78-4c29-4dbb-93a2-b431b99002d9.png)
  
## <a name="locking-a-preservation-policy"></a>Verrouillage d’une stratégie de conservation

Certaines organisations peuvent doivent se conformer aux règles définies par les organismes tels que la Securities and Exchange Commission (SEC) règle 17 a-4, ce qui implique qu’après qu’une stratégie de conservation est activée, il ne peut pas être désactivé ou établie moins restrictive. Avec verrou de conservation, vous pouvez verrouiller la stratégie afin que personne, y compris l’administrateur — peut désactiver la stratégie ou rendre moins restrictives.
  
Une fois une stratégie de verrouillé, personne ne peut désactiver ou supprimer le contenu de la stratégie. Et il n’est pas possible de modifier ou supprimer du contenu qui est soumis à la stratégie pendant la durée de conservation. Une fois la stratégie de l’été verrouillée, les méthodes seulement vous pouvez modifier la stratégie de conservation sont par l’ajout de contenu ou de l’extension de sa durée. Une stratégie verrouillée peut être augmentée ou étendue, mais ne peut pas être réduite ou désactivé.
  
Par conséquent, avant de verrouiller une stratégie de conservation, il est essentiel de bien comprendre les exigences de conformité de votre organisation, et ne pas verrouiller une stratégie jusqu'à ce que vous êtes certain qu’elle est ce dont vous avez besoin.
  
![Option permettant d’activer le verrouillage de conservation](media/cf9cc070-ddfb-469c-a47e-f88005a82fe4.png)
  
## <a name="turning-off-a-preservation-policy"></a>Désactivation d’une stratégie de conservation

Si vous choisissez de ne pas verrouiller la stratégie de conservation, vous pouvez le lancer à tout moment, y compris avant la fin de la période de temps spécifiée par la stratégie. Pour ce faire, désactivez simplement la stratégie.
  
![Option pour désactiver une stratégie de conservation sur la page de rétention de la sécurité &amp; centre de conformité](media/fdb44455-da01-4480-8fa6-0e3b29b1f535.png)
  
Toutefois, vous ne pouvez supprimer une stratégie de conservation alors que la stratégie s toujours active. Pour supprimer une stratégie de conservation, désactivez d’abord, puis supprimez la stratégie.
  
Après la désactivation d’une stratégie de conservation, tous les éléments soumis à cette stratégie dans la bibliothèque de blocage de conservation ou d’un dossier éléments récupérables sont éligibles pour le processus de nettoyage standard décrit plus haut. Notez que cela signifie que les éléments publiés à partir d’une stratégie ne sont pas immédiatement supprimés ; au lieu de cela, ils restent dans la bibliothèque de blocage de conservation ou d’un dossier éléments récupérables jusqu'à ce que le processus nettoie régulièrement la bibliothèque ou un dossier.
  
## <a name="using-preservation-policies-with-retention-policies-and-document-deletion-policies"></a>Utilisation de stratégies de conservation avec des stratégies de rétention et des stratégies de suppression de documents

Une stratégie de conservation garantit que le contenu est conservé indéfiniment ou pendant une période de temps spécifique, tandis qu’une stratégie de rétention pour une boîte aux lettres et une stratégie de suppression de documents pour un site garantissent que le contenu est supprimé après une période de temps spécifique. Si vous devez conserver un contenu pendant une période de temps fixe, vous pouvez utiliser une stratégie de conservation avec une stratégie de suppression ou de rétention. 
  
### <a name="site-content"></a>Contenu du site

Pour un site, vous pouvez utiliser une stratégie de conservation avec une stratégie de suppression de documents. Par exemple, vous pourriez conserver des documents pendant cinq ans après leur modification, puis configurer une stratégie de suppression pour les supprimer cinq ans après leur dernière modification.
  
Si une stratégie de suppression de documents supprime le contenu qui est soumis à une stratégie de conservation, le contenu sera conservé dans la bibliothèque de conservation permanente. Par exemple, si une stratégie de conservation conserve le contenu de deux ans, mais une stratégie de suppression de documents supprime le contenu après un an, tout le contenu est supprimé est toujours préservé. Pour plus d’informations, voir [vue d’ensemble des stratégies de suppression de documents](https://support.office.com/article/55e8d858-f278-482b-a198-2e62d6a2e6e5).
  
### <a name="mailbox-content"></a>Contenu de la boîte aux lettres

Pour une boîte aux lettres, vous pouvez associer une stratégie de conservation avec une stratégie de rétention qui comporte une balise de stratégie par défaut. Par exemple, vous pourriez conserver des éléments de boîte aux lettres pour sept ans, puis configurer une stratégie de rétention pour supprimer les sept ans après que qu’ils ont été reçus (pour les messages) ou créés (pour les éléments qui ne sont pas envoyées, tels que des notes). La stratégie de conservation garantit que les éléments supprimés sont conservés au moins la durée spécifiée, alors que la stratégie de rétention garantit que les éléments de boîte aux lettres sont supprimés à la fin de cette période. Pour plus d’informations, voir [les balises de rétention et stratégies de rétention](https://go.microsoft.com/fwlink/p/?LinkID=404351).
  
## <a name="permissions"></a>Autorisations

Les membres de votre équipe de conformité qui utiliseront la sécurité &amp; centre de conformité pour créer des stratégies de conservation besoin des autorisations pour le :
  
-  Sécurité Office 365 &amp; centre de conformité 
    
- aux sites dont le contenu doit être conservé ;
    
- aux boîtes aux lettres dont le contenu doit être conservé.
    
### <a name="office-365-security-amp-compliance-center"></a>Sécurité Office 365 &amp; centre de conformité

En tant qu’un administrateur du client, vous voulez être en mesure de fournir aux règlements et autres personnes à accéder à la sécurité &amp; centre de conformité, sans octroyer toutes les autorisations d’un administrateur de client. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
  
### <a name="sites"></a>Sites

Les membres de votre équipe de mise en conformité qui créent des stratégies de conservation ont besoin d’autorisations pour les collections de sites auxquelles des stratégies seront appliquées. En outre, si les responsables de la conformité créent également des stratégies de suppression de documents, ils doivent disposer d’autorisations pour la collection de sites du centre de stratégie de conformité où les stratégies de suppression de documents sont créées et stockées. Nous vous recommandons d’effectuer les actions suivantes :
  
1. Créer un groupe de sécurité qui contient tous les utilisateurs du centre de stratégie de conformité — probablement votre équipe de gestion des stratégies de conformité. Pour plus d’informations, voir [Groupes de sécurité Manage Mail-Enabled](https://go.microsoft.com/fwlink/p/?LinkID=404345) . 
    
2. Dans le centre de la stratégie de conformité, ajoutez le groupe de sécurité pour le groupe de propriétaires de collection de sites. Pour plus d’informations, consultez la rubrique [autorisations pour les administrateurs de collection de sites](https://go.microsoft.com/fwlink/p/?LinkID=404346) . 
    
3. Dans chaque collection de sites à laquelle vous devez affecter des stratégies de conservation, ajoutez le groupe de sécurité au groupe de visiteurs de la collection de sites (autorisations d’accès en lecture).
    
### <a name="mailboxes-and-public-folders"></a>Boîtes aux lettres et dossiers publics

Pour appliquer une stratégie de conservation à une boîte aux lettres, les responsables de la mise en conformité ont besoin au moins des autorisations d’accès en lecture pour cette boîte aux lettres. 
  
Pour appliquer une stratégie de conservation à un dossier public, les responsables de la mise en conformité doivent au moins disposer d’autorisations de lecture pour tous les dossiers publics.
  

