---
title: Restriction de l’accès au contenu à l’aide du chiffrement dans les étiquettes de sensibilité
ms.author: stephow
author: stephow-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Lorsque vous créez une étiquette de sensibilité, vous pouvez restreindre l’accès au contenu auquel l’étiquette sera appliquée. Les étiquettes de sensibilité peuvent utiliser le chiffrement pour protéger le contenu.
ms.openlocfilehash: a30f5d6168ea8118ef6b30ff26a429857affaa4a
ms.sourcegitcommit: fd3db13cd4fc71cd2cb164fd702007acba3e7399
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2019
ms.locfileid: "36717659"
---
# <a name="restrict-access-to-content-by-using-encryption-in-sensitivity-labels"></a>Restriction de l’accès au contenu à l’aide du chiffrement dans les étiquettes de sensibilité

Lorsque vous créez une étiquette de sensibilité, vous pouvez restreindre l’accès au contenu auquel l’étiquette sera appliquée. Par exemple, avec les paramètres de chiffrement d’une étiquette de sensibilité, vous pouvez protéger le contenu comme suit :

- Seuls les utilisateurs de votre organisation peuvent ouvrir un document ou un e-mail confidentiel.
- Seuls les utilisateurs du département marketing peuvent modifier et imprimer le document ou l’e-mail d’annonce de promotion, alors que tous les autres utilisateurs de votre organisation peuvent uniquement le lire.
- Les utilisateurs ne peuvent pas transférer un e-mail ou y copier tout contenu relatif à une réorganisation interne.
- La liste de prix à jour envoyée aux partenaires ne peut pas être ouverte après une date spécifiée.

Lorsqu’un document ou un e-mail est chiffré, l’accès à son contenu est restreint de l’une des façons suivantes :

- Il peut uniquement être déchiffré par les utilisateurs autorisés par les paramètres de chiffrement de l’étiquette.
- Il reste chiffré quel que soit son emplacement, interne ou externe à votre organisation, même si le fichier est renommé.
- Il est chiffré lorsqu’il est inactif (par exemple dans un compte OneDrive) et en transit (par exemple, un e-mail envoyé).

Enfin, en tant qu’administrateur, lorsque vous créez une étiquette de confidentialité, vous pouvez choisir d’effectuer l’une des opérations suivantes :

- **Attribuer des autorisations maintenant**, afin de déterminer précisément les utilisateurs autorisés à accéder au contenu associé à cette étiquette.
- **Permettre aux utilisateurs d'attribuer des autorisations** lorsqu’ils appliquent l’étiquette au contenu. De cette façon, vous pouvez proposer aux membres de votre organisation la souplesse nécessaire pour mieux collaborer et accomplir leur travail.

Les paramètres de chiffrement sont disponibles lorsque vous créez une étiquette de sensibilité dans le Centre de conformité Microsoft 365, dans le Centre de sécurité Microsoft 365 ou dans le Centre de sécurité et conformité Office 365. Dans la zone de navigation gauche, sélectionnez **Classification** > **Etiquette de confidentialité** > **Créer une étiquette**.

## <a name="how-encryption-works"></a>Fonctionnement du chiffrement

Le chiffrement utilise Azure Rights Management (Azure RMS). Azure RMS repose sur des stratégies de chiffrement, d’identité et d’autorisation. Pour en savoir plus, reportez-vous à l’article [En quoi consiste Azure Rights Management ?](https://docs.microsoft.com/fr-FR/azure/information-protection/what-is-azure-rms)

## <a name="how-to-turn-on-encryption-for-a-sensitivity-label"></a>Comment activer le chiffrement pour une étiquette de sensibilité

Pour commencer, basculez le **chiffrement** vers **activé**, puis choisissez si vous souhaitez :

- **Attribuer des autorisations maintenant**, afin de déterminer précisément les utilisateurs autorisés à accéder au contenu associé à cette étiquette. Pour plus d’informations, voir la section suivante [affecter des autorisations maintenant](#assign-permissions-now).
- **Permettre aux utilisateurs d'attribuer des autorisations** lorsqu’ils appliquent l’étiquette au contenu. De cette façon, vous pouvez proposer aux membres de votre organisation la souplesse nécessaire pour mieux collaborer et accomplir leur travail. Pour plus d’informations, voir la section ci-dessous [permettre aux utilisateurs d’affecter des autorisations](#let-users-assign-permissions).

Par exemple, si vous avez une étiquette de confidentialité appelée **hautement confidentiel** qui sera appliquée à votre contenu le plus sensible, vous souhaiterez peut-être choisir le type d’autorisations qui lui sont associées.

Par ailleurs, si vous avez une étiquette de confidentialité appelée **contrats professionnels** et que le flux de travail de votre organisation exige que vos collègues collaborent sur ce contenu avec des personnes de façon ponctuelle, vous souhaiterez peut-être autoriser vos utilisateurs à décider qui obtient les autorisations lorsqu’ils attribuent l’étiquette. Cette flexibilité permet à la fois à vos utilisateurs de gagner en productivité et de réduire les demandes aux administrateurs de mise à jour ou de création de nouvelles étiquettes de confidentialité pour résoudre des scénarios spécifiques.

![Option pour ajouter des autorisations définies par l’utilisateur ou l’administrateur](media/sensitivity-label-user-or-admin-defined-permissions.png)

## <a name="assign-permissions-now"></a>Attribuer des autorisations maintenant

Utilisez les options ci-dessous pour contrôler les utilisateurs autorisés à accéder aux e-mails ou aux documents auxquels cette étiquette est appliquée. Vous pouvez :

1. **Appliquer le chiffrement aux e-mails et aux documents, ou uniquement aux e-mails.** Si vous sélectionnez uniquement les e-mails, les messages portant cette étiquette seront chiffrés dans Outlook, mais les documents qui portent cette étiquette ne seront pas chiffrés dans les autres applications, telles que Word ou PowerPoint. 
2. **Autoriser l’expiration des accès au contenu portant l’étiquette**, à une date spécifique ou au bout d’un certain nombre de jours après l’application de l’étiquette. Après cette période, les utilisateurs ne sont plus en mesure d’ouvrir l’élément étiqueté. Si vous spécifiez une date, elle prend effet le jour choisi à minuit dans votre fuseau horaire actuel. (Notez que certains clients de messagerie peuvent ne pas imposer l'expiration et ne pas afficher les e-mails dont la date d'expiration est dépassée, en raison de leurs mécanismes de mise en cache).
3. **Autoriser l’accès hors connexion** : Jamais, Toujours ou pendant un nombre de jours déterminé après que l’étiquette a été appliquée. Si vous limitez l’accès hors connexion sur Jamais ou sur un nombre de jours, lorsque ce seuil est atteint, les utilisateurs doivent s’authentifier à nouveau et leur accès est journalisé. Pour plus d’informations, reportez-vous à la section suivante sur la licence d’utilisation de Rights Management.

![Paramètres pour les autorisations définies par l’administrateur](media/sensitivity-encryption-settings-for-admin-defined-permissions.png)

### <a name="rights-management-use-license-for-offline-access"></a>Licence d’utilisation de Rights Management pour l’accès en mode hors connexion

Lorsqu’un utilisateur ouvre un document ou un e-mail en mode hors connexion et que celui-ci a été protégé par une étiquette de sensibilité, il reçoit une licence d’utilisation Azure Rights Management sur ce contenu. Cette licence d’utilisation est un certificat qui contient les droits d’utilisation de l’utilisateur sur le document ou l’e-mail, ainsi que la clé de chiffrement qui a été utilisée pour chiffrer le contenu. La licence d’utilisation contient également une date d’expiration si celle-ci a été définie, ainsi que la durée de validité de la licence.

Si aucune date d’expiration n’a été configurée, la période de validité par défaut de la licence d’utilisation est de 30 jours. Pendant la durée de la licence, l’utilisateur n’a pas besoin d’être authentifié ou autorisé à nouveau pour accéder au contenu. Il peut ainsi continuer à ouvrir le document ou l’e-mail protégé sans connexion à Internet. Lorsque la période de validité de la licence d’utilisation a expiré, l’utilisateur doit à nouveau s’authentifier ou être autorisé lorsqu’il souhaite accéder au document ou à l’e-mail protégé.

En plus de la nouvelle authentification, la stratégie et l’appartenance à un groupe d’utilisateurs sont également réévaluées. Autrement dit, les utilisateurs peuvent constater des résultats d’accès différents au même document ou au même e-mail si des modifications ont été apportées à la stratégie ou à l’appartenance au groupe depuis leur dernier accès au contenu.

Pour savoir comment modifier le paramètre de 30 jours par défaut, reportez-vous à [Licence d’utilisation Rights Management](https://docs.microsoft.com/fr-FR/azure/information-protection/configure-usage-rights#rights-management-use-license).

### <a name="assign-permissions-to-specific-users-or-groups"></a>Attribuer des autorisations à des utilisateurs ou des groupes spécifiques

Vous pouvez accorder des autorisations à des personnes spécifiques, de manière à ce qu’elles soient les seules à pouvoir interagir avec le contenu étiqueté.

Pour ce faire, suivez un processus simple en deux étapes :

1. Ajoutez tout d’abord les utilisateurs ou les groupes qui vont recevoir les autorisations sur le contenu étiqueté.
2. Choisissez ensuite les autorisations desquelles les utilisateurs bénéficieront sur le contenu étiqueté.

![Options d’attribution des autorisations aux utilisateurs](media/Sensitivity-Assign-permissions-settings.png)

#### <a name="add-users-or-groups"></a>Ajouter des utilisateurs ou des groupes

Lorsque vous attribuez des autorisations, vous pouvez choisir :

- Tous les membres de votre organisation (tous les membres du client). Ce paramètre exclut les comptes Invité.
- N’importe quel utilisateur, groupe de sécurité à extension messagerie, groupe de distribution, groupe Office 365 ou groupe de distribution dynamique. 
- Une adresse e-mail ou un domaine en dehors de votre organisation, tels que gmail.com, hotmail.com ou outlook.com.

Lorsque vous choisissez tous les membres de client ou parcourez l’annuaire, les utilisateurs ou les groupes doivent avoir une adresse e-mail.

Nous vous recommandons d’utiliser des groupes plutôt que des utilisateurs. En effet, avec cette stratégie, votre configuration reste plus simple.

#### <a name="choose-permissions"></a>Choisir les autorisations

Lorsque vous choisissez les autorisations à attribuer à ces utilisateurs ou ces groupes, vous pouvez sélectionner :

- Un [niveau d’autorisation prédéfini](https://docs.microsoft.com/fr-FR/azure/information-protection/configure-usage-rights#rights-included-in-permissions-levels) avec un groupe de droits prédéfini, par exemple, Co-auteur ou Réviseur.
- Un groupe d’autorisations personnalisé, avec lequel vous choisissez les autorisations que vous voulez.

Pour plus d’informations sur chacune des autorisations spécifiques, reportez-vous à [Descriptions et droits d’utilisation](https://docs.microsoft.com/fr-FR/azure/information-protection/configure-usage-rights#usage-rights-and-descriptions).  

![Options de choix d’autorisations prédéfinies ou personnalisées](media/Sensitivity-Choose-permissions-settings.png)

Notez qu’une même étiquette peut accorder différentes autorisations à différents utilisateurs. Par exemple, une étiquette unique peut affecter à certains utilisateurs des droits de réviseur et à un autre utilisateur des droits de co-auteur, comme illustré ci-dessous.

Pour ce faire, ajoutez des utilisateurs ou groupes, attribuez-leur des autorisations et enregistrez ces paramètres. Répétez ensuite ces étapes : ajoutez des utilisateurs, attribuez-leur des autorisations et enregistrez les paramètres à chaque fois. Vous pouvez répéter cette procédure autant de fois que nécessaire, afin de définir différentes autorisations pour différents utilisateurs.

![Différents utilisateurs avec différentes autorisations](media/Sensitivity-Multiple-users-permissions.png)

#### <a name="rights-management-issuer-user-applying-the-sensitivity-label-always-has-full-control"></a>L’émetteur de Rights Management (celui qui applique l’étiquette de sensibilité) bénéficie toujours d’un contrôle total.

Le chiffrement d’une étiquette de sensibilité utilise Azure RMS. Lorsqu’un utilisateur applique une étiquette de sensibilité pour protéger un document ou un e-mail à l’aide d’Azure RMS, il devient l’émetteur Rights Management sur ce contenu.

L’émetteur Rights Management bénéficie toujours d’autorisations en contrôle total sur le document ou l’e-mail et, par ailleurs :

- Si les paramètres de protection comportent une date d’expiration, l’émetteur Rights Management peut toujours ouvrir et modifier le document ou l’e-mail après cette date.
- L’émetteur Rights Management peut toujours accéder au document ou à l’e-mail hors connexion.
- L’émetteur Rights Management peut toujours ouvrir un document après sa révocation.

Pour plus d’informations, reportez-vous à [Émetteur Rights Management et propriétaire Rights Management](https://docs.microsoft.com/fr-FR/azure/information-protection/configure-usage-rights#rights-management-issuer-and-rights-management-owner).

## <a name="let-users-assign-permissions"></a>Permettre aux utilisateurs d’attribuer des autorisations

Vous pouvez utiliser ces options pour permettre aux utilisateurs d’attribuer des autorisations lorsqu’ils appliquent manuellement une étiquette de confidentialité à un contenu :

- Dans Outlook, un utilisateur peut appliquer des restrictions équivalant à l’option **ne pas transférer**. Cette option est prise en charge en mode natif dans Outlook sur Windows et n’exige pas que vous installiez le client de l’étiquetage unifié Azure Information Protection.
- Dans Word, PowerPoint et Excel, l’utilisateur est invité à sélectionner un niveau d’autorisation pour des utilisateurs, des groupes ou des organisations spécifiques. Cette option n’est pas prise en charge en mode natif dans ces applications Office donc vos utilisateurs doivent installer le client de l’étiquetage unifié Azure Information Protection.

Ces options déterminent les applications dans lesquelles l’étiquette de confidentialité s’affiche :

- Si seule l’option Outlook est activée pour l’étiquette de confidentialité, l’étiquette s’affiche pour les utilisateurs uniquement dans Outlook.
- Si seule l’option Word, PowerPoint et Excel est activée pour l’étiquette de confidentialité, l’étiquette s’affiche pour les utilisateurs uniquement dans ces applications.
- Si les deux options sont activées pour l’étiquette de confidentialité, l’étiquette s’affiche pour les utilisateurs de toutes les applications disponibles : Outlook, Word, PowerPoint et Excel.

Une étiquette de confidentialité permettant aux utilisateurs d’attribuer des autorisations peut être appliquée au contenu uniquement manuellement par les utilisateurs. Elle ne peut pas être appliquée automatiquement ou utilisée comme étiquette recommandée.

> [!NOTE]
> Pour permettre aux utilisateurs d’attribuer des autorisations, vous devez disposer d’un abonnement Azure Information Protection. Pour utiliser cette fonctionnalité dans Word, PowerPoint et Excel, vous devez télécharger et installer le [client de l’étiquetage unifié Microsoft Azure Information Protection](https://docs.microsoft.com/azure/information-protection/rms-client/install-unifiedlabelingclient-app). Nous travaillons à la prise en charge native de cette fonctionnalité dans ces applications Office, afin de ne pas avoir besoin du client Microsoft Azure Information Protection. Par ailleurs, le client ne s’exécute que sur Windows. Cette fonctionnalité n’est pas encore prise en charge sur Mac, iOS, Android ou Office pour le Web.

![Paramètres de chiffrement pour les autorisations définies par l’utilisateur](media/sensitivity-encryption-settings-for-user-defined-permissions.png)

### <a name="outlook-restrictions"></a>Restrictions Outlook

Dans Outlook, lorsqu’un utilisateur applique une étiquette de confidentialité qui lui permet d’attribuer des autorisations à un message, les restrictions sont identiques à celles de l’option ne pas transférer. L’utilisateur voit le nom et la description de l’étiquette dans la partie supérieure du message, ce qui indique que le contenu est protégé. Contrairement à Word, PowerPoint et Excel (voir la [section suivante](#word-powerpoint-and-excel-permissions)), les utilisateurs ne sont pas invités à sélectionner des autorisations spécifiques.

![Étiquette de niveau de confidentialité appliquée à un message dans Outlook](media/sensitivity-label-outlook-protection-applied.png)

Lorsque l’option ne pas transférer est appliquée à un e-mail, celui-ci est chiffré et les destinataires doivent être authentifiés. Les destinataires ne peuvent alors pas le transférer, l’imprimer ou en faire une copie. Par exemple, dans le client Outlook, le bouton transférer n’est pas disponible, les options du menu enregistrer sous et imprimer ne sont pas disponibles, et vous ne pouvez pas ajouter ou modifier des destinataires dans les zones à, CC ou CCI.

Les documents Office non protégés joints à l’e-mail héritent automatiquement des mêmes restrictions. Les droits d’utilisation appliqués à ces documents sont modifier le contenu, modifier; afficher, ouvert, lu et autoriser les macros. Si l’utilisateur souhaite appliquer des droits d’utilisation différents pour une pièce jointe, ou si la pièce jointe n’est pas un document Office qui prend en charge cette protection héritée, l’utilisateur doit protéger le fichier avant de le joindre à l’e-mail.

### <a name="word-powerpoint-and-excel-permissions"></a>Autorisations Word, PowerPoint et Excel

Dans Word, PowerPoint et Excel, lorsqu’un utilisateur applique une étiquette de confidentialité qui lui permet d’attribuer des autorisations à un document, il est invité à protéger le contenu comme illustré ci-dessous.

L’utilisateur peut ainsi :

- Sélectionner un niveau d’autorisation, tel que visionneuse (qui attribue l’autorisation Afficher uniquement) ou co-auteur (qui affecte les autorisations afficher, modifier, copier et imprimer).
- Sélectionner les utilisateurs, les groupes ou les organisations. Cela peut inclure des personnes à l’intérieur ou à l’extérieur de votre organisation.
- Sélectionnez une date d’expiration, après laquelle les utilisateurs sélectionnés ne pourront pas accéder au contenu. Pour plus d’informations, voir la section ci-dessus [licence d'utilisation de la gestion des droits pour l’accès hors connexion](#rights-management-use-license-for-offline-access).

![Options de protection pour l’utilisateur avec les autorisations personnalisées](media/sensitivity-aip-custom-permissions-dialog.png)

## <a name="what-happens-to-existing-encryption-when-a-labels-applied"></a>Qu’advient-il du chiffrement existant lorsqu’une nouvelle étiquette est appliquée ?

Avant l’application d’une étiquette de niveau de confidentialité à du contenu, il est possible qu’un utilisateur ait déjà chiffré le contenu en lui appliquant un autre paramètre de protection. Par exemple, un utilisateur peut avoir appliqué :

- L’option **Ne pas transférer**.
- Une protection personnalisée à l’aide du client d’étiquetage unifié Azure Information Protection.
- Un modèle Azure Rights Management Service (RMS) qui chiffre le contenu mais n’est pas associé à une étiquette.

Ce tableau explique ce qu’il advient du chiffrement existant lorsqu’une étiquette de niveau de confidentialité est appliquée à ce contenu.
<br/>
<br/>

| |**L’utilisateur applique une étiquette de niveau de confidentialité avec chiffrement désactivé**|**L’utilisateur applique une étiquette de niveau de confidentialité avec chiffrement activé**|**L’utilisateur applique une étiquette avec suppression de la protection**<sup>1</sup>|
|:-----|:-----|:-----|:-----|
|**Ne pas transférer**|E-mail - La protection est supprimée<br/>Document - La protection est conservée|La protection de l’étiquette est appliquée|L’option **Ne pas transférer** est supprimée|
|**Protection personnalisée**<sup>1</sup>|La protection est conservée|La protection de l’étiquette est appliquée|La protection personnalisée est supprimée|
|**Modèle Azure RMS**|La protection est conservée|La protection de l’étiquette est appliquée|La protection personnalisée est supprimée|

<sup>1</sup>Uniquement pris en charge dans le client d’étiquetage Azure Information Protection.

## <a name="storing-encrypted-content-in-onedrive-and-sharepoint"></a>Stockage du contenu chiffré dans OneDrive et SharePoint

Notez que lorsque le chiffrement est appliqué aux fichiers stockés dans OneDrive et SharePoint, le service ne peut pas traiter le contenu de ces fichiers. Autrement dit, des fonctionnalités telles que la co-création, eDiscovery, la recherche, Delve et d’autres fonctionnalités de collaboration ne fonctionnent pas. De plus, les stratégies de protection contre la perte de données peuvent uniquement fonctionner avec les métadonnées (y compris les étiquettes Office 365), mais pas avec le contenu des fichiers chiffrés (par exemple, des numéros de cartes de crédit au sein des fichiers).

Ceci s’applique uniquement au contenu stocké dans OneDrive et SharePoint. Dans Exchange Online, les règles de flux de messagerie (également connues sous le nom de règles de transport) utilisent le [compte de super utilisateur](https://docs.microsoft.com/fr-FR/azure/information-protection/configure-super-users) pour analyser le contenu chiffré et appliquer des stratégies DLP.

## <a name="important-prerequisites"></a>Conditions préalables importantes

Pour utiliser le chiffrement, vous devrez peut-être effectuer les tâches suivantes.

### <a name="activating-azure-rights-management"></a>Activation d’Azure Rights Management

Pour que le chiffrement puisse être utilisé dans les étiquettes de sensibilité, le service Azure Rights Management doit être activé dans votre client. Avec les clients les plus récents, le service est activé par défaut, mais il peut s’avérer nécessaire de l’activer manuellement. Pour plus d’informations, reportez-vous à [Activation d’Azure Rights Management](https://docs.microsoft.com/fr-FR/azure/information-protection/activate-service).

### <a name="configure-exchange-for-azure-information-protection"></a>Configurer Exchange pour Azure Information Protection

Il n’est pas nécessaire de configurer Exchange pour Azure Information Protection pour que les utilisateurs puissent appliquer des étiquettes dans Outlook pour protéger leurs e-mails. Toutefois, tant qu’Exchange n’a pas été configuré pour Azure Information Protection, vous ne bénéficiez pas de toutes les fonctionnalités de protection Azure Rights Management avec Exchange.
 
Par exemple, les utilisateurs ne peuvent pas afficher les e-mails protégés sur des téléphones mobiles ou avec Outlook sur le web, les messages e-mails protégés ne peuvent pas être indexés pour la recherche et vous ne pouvez pas configurer la protection contre la perte de données (DLP) Exchange Online pour la protection Rights Management. 

Pour vous assurer qu’Exchange est en mesure de prendre en charge ces scénarios supplémentaires, reportez-vous aux rubriques suivantes :

- Pour Exchange Online, consultez les instructions de la section [Exchange Online : configuration de la gestion des droits relatifs à l’information](https://docs.microsoft.com/fr-FR/azure/information-protection/configure-office365#exchange-online-irm-configuration).
- Pour Exchange en local, vous devez déployer le [connecteur RMS et configurer vos serveurs Exchange](https://docs.microsoft.com/fr-FR/azure/information-protection/deploy-rms-connector). 
