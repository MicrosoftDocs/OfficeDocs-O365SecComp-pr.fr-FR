---
title: Correction d’erreur lors du traitement des données
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607718"
---
# <a name="error-remediation-when-processing-data"></a>Correction d’erreur lors du traitement des données

Correction d’erreur permet aux administrateurs de découverte électronique à résoudre les problèmes liés aux données qui empêchent le traitement correctement le contenu eDiscovery avancée (Preview). Par exemple, les fichiers qui sont protégés par mot de passe ne peuvent pas être traités dans la mesure où les fichiers sont verrouillés ou chiffrés. À l’aide de la correction d’erreur, les administrateurs de découverte électronique peuvent télécharger des fichiers avec ces erreurs, supprimez la protection par mot de passe et un télécharger les fichiers corrigés.

Utilisez la procédure suivante pour convertir des fichiers avec des erreurs dans les cas eDiscovery avancées (Preview).

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>Création d’une session de correction d’erreur pour résoudre les fichiers avec traitement des erreurs

>[!NOTE]
>Si la fermeture de l’Assistant de correction d’erreur à tout moment au cours de la procédure suivante, vous pouvez retourner à la session de correction d’erreur à partir de l’onglet **de traitement** en sélectionnant **correctives d’erreur** dans le menu déroulant **affichage** .

1. Sous l’onglet **de traitement** dans un cas eDiscovery avancées (Preview), sélectionnez **les erreurs** dans le menu déroulant **affichage** .

2. Sélectionnez les erreurs que vous souhaitez convertir en cliquant sur le bouton d’option en regard du type d’erreur ou un type de fichier.  Dans l’exemple suivant, nous allons corriger un fichier protégé de mot de passe.

3. Cliquez sur **+ Nouveau correction d’erreur**.

    ![Correction d’erreur](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    La session de correction d’erreur commencera commençant par une étape de préparation où les fichiers ayant subi une erreur qui sont déplacés vers un emplacement sécurisé Azure à télécharger.

    ![Préparation de la correction d’erreur](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. Une fois la préparation terminée, cliquez sur **suivant : télécharger des fichiers** pour poursuivre le téléchargement.

    ![Télécharger des fichiers](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. Pour télécharger des fichiers, spécifiez le **chemin d’accès de Destination pour le téléchargement**; Il s’agit d’un chemin d’accès sur votre ordinateur local où le fichier doit être téléchargé.  Le chemin d’accès par défaut, % USERPROFILE%\Downloads\errors, pointe vers le dossier Téléchargements connecté l’utilisateur. Cela peut être modifié selon vos besoins.

    >[!NOTE]
    >Nous vous recommandons d’utiliser un chemin d’accès local au lieu d’un chemin d’accès réseau distant pour des performances optimales.

    > [!NOTE]
    > Si vous n’avez pas installé AzCopy, vous pouvez l’installer à partir d’ici :https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

6. Copiez la commande prédéfinie en cliquant sur **Copier dans le Presse-papiers**. Démarrez une invite de commandes windows, collez la commande, puis appuyez sur **entrée**.  

    Les fichiers sont téléchargés.

    ![Préparation de la correction d’erreur](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > Si vous avez des problèmes d’exécution de cette commande, voir https://go.microsoft.com/fwlink/?linkid=2038117 pour des conseils de dépannage.

7. Après avoir téléchargé les fichiers, vous pouvez les résoudre un outil approprié. Pour les fichiers protégés par mot de passe, il existe un certain nombre de mot de passe que vous pouvez utiliser des outils de décodage. Si vous connaissez les mots de passe pour les fichiers, vous pouvez les ouvrir et supprimer le mot de passe.
    > [!NOTE]
    > INFORMATIQUE est important de conserver les noms de fichier et la structure de répertoire des fichiers corrigés intactes.  Toutes les conventions d’affectation de noms utilisés dans les fichiers téléchargés et les dossiers vous permettent d’associer les fichiers remdiated à l’original.

8. Retournez à la découverte électronique avancée (Preview) et cliquez sur **suivant : télécharger les fichiers**.  Ce est déplacés à l’étape suivante où vous pouvez désormais télécharger les fichiers.

    ![Télécharger des fichiers](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. Spécifier l’emplacement des fichiers corrigés dans la zone de texte **chemin d’accès à l’emplacement des fichiers** , puis cliquez sur **Copier dans un clibpboard**.

10. Collez la commande dans une invite de commandes Windows et appuyez sur **entrée** pour télécharger les fichiers.

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. Enfin, revenez à la découverte électronique avancée (Preview) et cliquez sur **suivant : traitement des fichiers**.

12. Lorsque le traitement est terminé.  Vous pouvez revenir à la plage de travail et consultez le fichier corrigé.

## <a name="what-happens-when-files-are-remediated"></a>Que se passe-t-il lorsque les fichiers sont résolues.

Lorsque des fichiers corrigés sont téléchargés, les métadonnées d’origine sont conservée à l’exception des champs suivants : 

- DocumentExtractedUrl
- ExtractedTextSize
- HasText
- IsErrorRemediate
- IsParentExtractedUrl
- ItemExtractedUrl
- LoadId
- ProcessingErrorMessage
- ProcessingStatus
- Texte
- WordCount
- WorkingsetId

Pour une définition de tous les champs de métadonnées de document d’eDiscovery avancée (Preview), voir [les champs de métadonnées de Document](document-metadata-fields.md).