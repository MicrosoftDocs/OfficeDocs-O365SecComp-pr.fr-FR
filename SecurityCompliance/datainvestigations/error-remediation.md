---
title: Erreur de correction lors du traitement des données pour une enquête
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 45e4fb0651cc137a67cc5322bf5e874ea31df838
ms.sourcegitcommit: 3f3f3ecb28ef65d023f3573f9a4e09a0586d8f53
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2019
ms.locfileid: "36490801"
---
# <a name="error-remediation-when-processing-data-for-an-investigation"></a>Erreur de correction lors du traitement des données pour une enquête

La correction des erreurs permet aux investigateurs de corriger les problèmes de données qui empêchent les enquêtes de données (préversion) de traiter correctement le contenu. Par exemple, les fichiers protégés par mot de passe ne peuvent pas être traités car les fichiers sont verrouillés ou chiffrés. À l’aide de la correction des erreurs, les investigateurs peuvent télécharger des fichiers avec de telles erreurs, supprimer la protection par mot de passe et télécharger les fichiers corrigés.

Utilisez le flux de travail suivant pour corriger les fichiers avec des erreurs dans les cas d’examens de données (aperçu).

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>Création d’une session de correction d’erreur pour corriger les fichiers avec des erreurs de traitement

>[!NOTE]
>Si l’Assistant de correction d’erreur est fermé à tout moment au cours de la procédure suivante, vous pouvez revenir à la session d’erreur de correction à partir de l’onglet **traitement** en sélectionnant **erreur correction** dans le menu déroulant **vue** .

1. Sous l’onglet **traitement** d’une enquête de données, sélectionnez **Erreurs** dans le menu déroulant **affichage** .

2. Sélectionnez les erreurs que vous souhaitez corriger en cliquant sur la case d’option en regard du type d’erreur ou du type de fichier.  Dans l’exemple suivant, nous effectuons la correction d’un fichier protégé par mot de passe.

3. Cliquez sur **+ nouvelle erreur de correction**.

    ![Correction des erreurs](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    La session de correction d’erreur commence avec une phase de préparation dans laquelle les fichiers contenant des erreurs sont copiés vers un emplacement Azure sécurisé afin qu’ils puissent être téléchargés.

    ![Préparation de la correction des erreurs](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. Une fois la préparation terminée, cliquez sur **suivant: Télécharger les fichiers** pour continuer le téléchargement.

    ![Télécharger des fichiers](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. Pour télécharger des fichiers, spécifiez le **chemin de destination pour le téléchargement**. Il s’agit d’un chemin d’accès sur votre ordinateur local où le fichier doit être téléchargé.  Le chemin d’accès par défaut,%USERPROFILE%\Downloads\errors, pointe vers le dossier downloads de l’utilisateur connecté; Cela peut être modifié selon vos besoins.

    >[!NOTE]
    >Nous vous recommandons d’utiliser un chemin d’accès local au lieu d’un chemin d’accès réseau distant pour des performances optimales.

    > [!NOTE]
    > Si vous n’avez pas installé AzCopy, vous pouvez l’installer à partir de cet emplacement:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

6. Copiez la commande prédéfinie en cliquant sur **copier dans le presse-papiers**. Démarrez une invite de commandes Windows, collez la commande, puis appuyez sur **entrée**.  

    Les fichiers sont téléchargés.

    ![Préparation de la correction des erreurs](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > Si vous rencontrez des problèmes lors de l’exécution de cette commande, consultez la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](../compliance20/troubleshooting-azcopy.md).

7. Après avoir téléchargé les fichiers, vous pouvez les corriger à l’aide d’un outil approprié. Pour les fichiers protégés par mot de passe, il existe plusieurs outils de craquage de mot de passe que vous pouvez utiliser. Si vous connaissiez les mots de passe des fichiers, vous pouvez les ouvrir et supprimer la protection par mot de passe.
    
   > [!NOTE]
    > Il est important de conserver la structure de répertoire et les noms de fichier des fichiers corrigés. Les noms de chemin d’accès des fichiers et dossiers téléchargés permettent d’associer les fichiers corrigés aux fichiers d’origine.  Si la structure du répertoire ou les noms de fichier sont modifiés, vous recevez l’erreur `Cannot apply Error Remediation to the current Evidenceset`suivante:.

8. À présent, revenez aux enquêtes de données (aperçu) et cliquez sur **suivant: charger les fichiers**.  Cette opération passe à l’étape suivante, dans laquelle vous pouvez à présent télécharger les fichiers.

    ![Charger des fichiers](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. Spécifiez l’emplacement des fichiers corrigés dans la zone **de texte chemin d’accès à l’emplacement des fichiers** , puis cliquez sur **copier dans le presse-papiers**.

10. Collez la commande dans une invite de commande Windows et appuyez sur **entrée** pour charger les fichiers.

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. Enfin, revenez aux enquêtes de données (aperçu) et cliquez sur **suivant: traiter les fichiers**.

12. Une fois le traitement terminé.  Vous pouvez revenir à la plage de travail et voir le fichier corrigé.

## <a name="what-happens-when-files-are-remediated"></a>Que se passe-t-il lorsque les fichiers sont convertis?

Lorsque les fichiers résolus sont téléchargés, les métadonnées d’origine sont conservées, à l’exception des champs suivants: 

- ExtractedTextSize
- HasText
- IsErrorRemediate
- LoadId
- ProcessingErrorMessage
- ProcessingStatus
- Texte
- WordCount
- WorkingsetId

Pour obtenir une définition de tous les champs de métadonnées de document dans les enquêtes de données (aperçu), consultez la rubrique [Field Metadata Fields](document-metadata-fields.md).