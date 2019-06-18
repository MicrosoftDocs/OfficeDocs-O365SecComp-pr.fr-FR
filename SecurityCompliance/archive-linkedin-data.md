---
title: Configuration d’un connecteur pour l’archivage des données LinkedIn dans Office 365 (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Les administrateurs peuvent configurer un connecteur natif pour importer des données à partir d’une page de la société LinkedIn vers Office 365. Cela vous permet d’archiver des données provenant de sources de données tierces dans Office 365 de sorte que vous puissiez utiliser les fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la conformité des données tierces de votre organisation.
ms.openlocfilehash: 2b89f990f18ae13ad15015f240ea4c4b0ec434b0
ms.sourcegitcommit: f2798d46acfbd56314e809cd3fe0350be807e420
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2019
ms.locfileid: "35017945"
---
# <a name="set-up-a-connector-to-archive-linkedin-data-in-office-365-preview"></a>Configuration d’un connecteur pour l’archivage des données LinkedIn dans Office 365 (aperçu)

La fonctionnalité connecteur permettant d’archiver les données des pages LinkedIn Company dans Office 365 est en aperçu.

Utilisez un connecteur natif dans le centre de sécurité & conformité dans Office 365 pour importer et archiver des données à partir des pages de la société LinkedIn. Une fois que vous avez configuré et configuré un connecteur, celui-ci se connecte au compte de la page de la société LinkedIn spécifique une fois toutes les 24 heures. Le connecteur convertit les messages publiés sur la page de l’entreprise en message électronique, puis importe ces éléments dans une boîte aux lettres dans Office 365.

Une fois que les données de la page de la société LinkedIn sont stockées dans une boîte aux lettres, vous pouvez appliquer les fonctionnalités de conformité d’Office 365 telles que la conservation pour litige, la recherche de contenu, l’archivage inaltérable, l’audit et les stratégies de rétention Office 365 aux données LinkedIn. Par exemple, vous pouvez rechercher ces éléments à l’aide de la recherche de contenu ou associer la boîte aux lettres de stockage à un dépositaire dans un cas avancé de découverte électronique. La création d’un connecteur pour importer et archiver des données LinkedIn dans Office 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.

## <a name="before-you--begin"></a>Avant de commencer

- Vous devez disposer des informations d’identification de connexion (adresse de messagerie ou numéro de téléphone et mot de passe) d’un compte d’utilisateur de LinkedIn qui est administrateur de la page de la société LinkedIn que vous souhaitez archiver. Vous utilisez ces informations d’identification pour vous connecter à LinkedIn lors de la configuration du connecteur.

- L’utilisateur qui crée un connecteur de page de société LinkedIn doit disposer du rôle d’exportation d’importation de boîte aux lettres dans Exchange Online. Cela est nécessaire pour accéder à la page **données** tierces d’archivage dans le centre de sécurité & conformité. Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle exportation d’importation de boîte aux lettres au groupe de rôles gestion de l’organisation dans Exchange Online. Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d’exportation d’importation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres. Pour plus d’informations, reportez-vous aux sections [créer des groupes de rôles](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou modifier des [groupes](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) de rôles dans l’article «gérer des groupes de rôles dans Exchange Online».

## <a name="create-a-linkedin-connector"></a>Créer un connecteur LinkedIn

1. Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données** , puis cliquez sur **archiver les données**tierces.

2. Sur la page **données tierces** d’archivage, cliquez sur **Ajouter un connecteur**, puis sur **LinkedIn**.

3. Sur la page **conditions de service** , cliquez sur **accepter**.

4. Sur la page **se connecter avec LinkedIn** , cliquez sur **se connecter avec LinkedIn**.

   La page de connexion LinkedIn s’affiche.

   ![Page de connexion à LinkedIn](media/LinkedInSigninPage.png)

5. Sur la page de connexion LinkedIn, entrez l’adresse de messagerie (ou le numéro de téléphone) et le mot de passe du compte LinkedIn associé à la page de la société que vous souhaitez archiver, puis cliquez sur **se connecter**.

   Une page d’Assistant s’affiche avec la liste de toutes les pages de la société LinkedIn associées au compte auquel vous vous êtes connecté. Un connecteur ne peut être configuré que pour une seule page de la société. Si votre organisation dispose de plusieurs pages d’entreprise LinkedIn, vous devez créer un connecteur pour chacune d’entre elles.

   ![Une page avec une liste de pages de la société LinkedIn s’affiche.](media/LinkedInSelectCompanyPage.png)


6. Sélectionnez la page de la société à partir de laquelle vous souhaitez archiver des éléments, puis cliquez sur **suivant**.

7. Sur la page **définir les filtres** , vous pouvez appliquer un filtre pour importer initialement les éléments qui sont un certain âge. Sélectionnez un âge, puis cliquez sur **suivant**.

8. Sur la page **définir le compte de stockage** , tapez l’adresse de messagerie d’une boîte aux lettres Office 365 dans laquelle les éléments LinkedIn seront importés, puis cliquez sur **suivant**. Les éléments sont importés dans le dossier boîte de réception de cette boîte aux lettres.

9. Passez en revue les paramètres du connecteur, puis cliquez sur **Enregistrer** pour terminer l’installation du connecteur.

Après avoir créé le connecteur, vous pouvez revenir à la page d' **archivage des données** tierces (cliquez sur **Actualiser** si nécessaire pour mettre à jour la liste des connecteurs) pour afficher le nouveau connecteur. La valeur dans la colonne d' **État** est en **attente de démarrage**. Le processus initial d’importation doit prendre jusqu’à 24 heures. Après la première exécution du connecteur et l’importation des éléments LinkedIn, le connecteur s’exécute une fois toutes les 24 heures et importe les nouveaux éléments créés sur la page de la société LinkedIn dans les 24 heures qui précèdent.

Pour afficher plus de détails, cliquez sur le connecteur dans la liste sur la page **données** tierces d’archivage pour afficher la page de menu volant. Sous **État**, la plage de dates affichée indique le filtre d’âge qui a été sélectionné lors de la création du connecteur. 

## <a name="more-information"></a>Plus d’informations

- Les éléments LinkedIn sont importés dans le dossier boîte de réception de la boîte aux lettres de stockage dans Office 365. Elles apparaissent sous forme de messages électroniques. Le nom complet de l’expéditeur du message est le nom de la page de la société LinkedIn. L’adresse de messagerie réelle de l’expéditeur est l’adresse de messagerie de la boîte aux lettres de stockage. Le nom de la page de la société est également pré-ajouté à la ligne d’objet. 

- En raison du comportement précédent, vous pouvez effectuer des `from` recherches `subject` dans les propriétés de ou de messagerie lors de l’utilisation d’un outil eDiscovery de Microsoft pour rechercher des éléments LinkedIn archivés dans Office 365. Par exemple, si le nom de la page société est «contoso Company page», vous pouvez utiliser l’une des paires *Property: value* suivantes dans la requête de recherche par mot clé:
   
   ```
   from:"Contoso Company Page"
   ```

    Ou

   ```
   subject:"Contoso Company Page"
   ```

- Pour faciliter la localisation ou la gestion des éléments LinkedIn importés dans Office 365, le propriétaire de la boîte aux lettres de stockage (ou quiconque lui a attribué l’autorisation FullAccess) peut configurer une règle de boîte de réception pour déplacer les éléments d’une page de la société LinkedIn spécifique vers un dossier spécifique. Cela est utile si la boîte aux lettres de stockage est utilisée pour archiver des éléments qui sont importés à partir de différentes sources de données tierces. Par exemple, vous pouvez créer une règle de boîte de réception qui déplace tous les éléments contenant le nom d’une page de la société LinkedIn spécifique dans le champ Subject vers un dossier spécifique.