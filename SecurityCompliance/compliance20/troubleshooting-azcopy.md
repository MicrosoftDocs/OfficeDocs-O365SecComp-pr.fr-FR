---
title: Résolution des problèmes liés à AzCopy dans Advanced eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 9711bee4ec9a61510b47568df37dfd3135e1e00c
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30742500"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery-preview"></a><span data-ttu-id="e39c9-102">Résolution des problèmes liés à AzCopy dans Advanced eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e39c9-102">Troubleshoot AzCopy in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="e39c9-103">Lors du chargement de données ou de documents autres que Office 365 pour la correction d'erreur dans Advanced eDiscovery (aperçu), l'interface utilisateur fournit une commande AzCopy Azure qui contient les paramètres de l'emplacement où les fichiers que vous souhaitez télécharger sont stockés et le dossier Azure emplacement de stockage vers lequel les fichiers seront téléchargés.</span><span class="sxs-lookup"><span data-stu-id="e39c9-103">When loading non-Office 365 data or documents for error remediation in Advanced eDiscovery (Preview), the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="e39c9-104">Pour télécharger vos documents, copiez cette commande, puis exécutez-la dans une invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e39c9-104">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="e39c9-105">La capture d'écran suivante illustre un exemple de commande AzCopy:</span><span class="sxs-lookup"><span data-stu-id="e39c9-105">The follow screenshot shows an example of an AzCopy command:</span></span>

![Télécharger des fichiers non-Office 365](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="e39c9-107">Dans la plupart des cas, la commande fournie fonctionne lorsque vous l'exécutez.</span><span class="sxs-lookup"><span data-stu-id="e39c9-107">In most cases, the command that's provided will work when you run it.</span></span> <span data-ttu-id="e39c9-108">Toutefois, il peut arriver que la commande affichée ne s'exécute pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e39c9-108">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="e39c9-109">Voici quelques raisons possibles.</span><span class="sxs-lookup"><span data-stu-id="e39c9-109">Here's a few possible reasons.</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="e39c9-110">AzCopy n'est pas installé sur l'ordinateur local ou il n'est pas installé à l'emplacement par défaut</span><span class="sxs-lookup"><span data-stu-id="e39c9-110">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="e39c9-111">Si AzCopy n'est pas installé ou s'il est installé à un emplacement autre que l'emplacement d'installation `%ProgramFiles(x86)%`par défaut (c'est-à-dire), il se peut que vous receviez le message d'erreur suivant lorsque vous exécutez la commande AzCopy:</span><span class="sxs-lookup"><span data-stu-id="e39c9-111">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

    The system cannot find the path specified.

<span data-ttu-id="e39c9-112">Si AzCopy n'est pas installé sur l'ordinateur local, vous pouvez procéder à l'installation à partir de là (en veillant à l' [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy)installer à l'emplacement par défaut):.</span><span class="sxs-lookup"><span data-stu-id="e39c9-112">If AzCopy isn't install on the local computer, you can install from here (being sure to install it in the default location): [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span></span>


<span data-ttu-id="e39c9-113">Si AzCopy est installé, mais qu'il est installé à un emplacement différent de l'emplacement par défaut, vous pouvez copier la commande, la coller dans un fichier texte, puis modifier le chemin d'accès à l'emplacement où AzCopy est réellement installé.</span><span class="sxs-lookup"><span data-stu-id="e39c9-113">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is actually installed.</span></span> <span data-ttu-id="e39c9-114">Par exemple, si Azcopy se trouve dans `%ProgramFiles%`, vous pouvez remplacer la première partie de la commande `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` par. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`</span><span class="sxs-lookup"><span data-stu-id="e39c9-114">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="e39c9-115">Une fois que vous avez effectué cette modification, copiez-la à partir du fichier texte, puis exécutez-la dans une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="e39c9-115">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="e39c9-116">Si AzCopy est installé à un emplacement autre que l'emplacement d'installation par défaut, envisagez de le désinstaller, puis de le réinstaller à l'emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="e39c9-116">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="e39c9-117">Cela vous permettra d'éviter ce problème à l'avenir.</span><span class="sxs-lookup"><span data-stu-id="e39c9-117">This will help prevent this issue in the future.</span></span>