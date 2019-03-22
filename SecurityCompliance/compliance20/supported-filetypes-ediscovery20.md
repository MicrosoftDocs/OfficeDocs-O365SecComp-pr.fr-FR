---
title: Types de fichiers pris en charge dans Advanced eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 7955debee750019d60b8016d736ba50f1ff70bce
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30737704"
---
# <a name="supported-file-types-in-advanced-ediscovery-preview"></a>Types de fichiers pris en charge dans Advanced eDiscovery (aperçu)

Advance eDiscovery (Preview) prend en charge de nombreux types de fichiers à différents niveaux, décrits dans le tableau suivant. Cette liste n'est pas finalisée, et nous allons ajouter de nouveaux types de fichiers lors de notre test de validation. Le tableau indique également si un type de fichier peut être affiché dans les visionneuses disponibles dans la découverte électronique avancée (aperçu).

| Type MIME | Classe file | Visionneuse Native | Visionneuse de texte | Visionneuse d'anNotations | Extraction de conteneur | Extensions |
| :- | :- | :- | :- | :- | :- | :- |
| application/msword | Document | Oui | Oui | Oui | Non | . doc;. dat |
| application/pdf | Document | Oui | Oui | Oui | Non | .pdf |
| application/format RTF | Document | Oui | Oui | Oui | Non | . rtf;. équ |
| application/vnd. MS-Excel | Document | Oui | Oui | Oui | Non | . xls;. dat |
| application/vnd. MS-Excel. Sheet. Binary. macroenabled. 12 | Productivité/format de document ouvert | Oui | Oui | Non | Non | . xlsb |
| application/vnd. MS-Excel. Sheet. macroenabled. 12 | Document | Oui | Oui | Oui | Non | . xlsm |
| application/vnd. MS-Excel. template. macroenabled. 12 | Productivité/format de document ouvert | Non | Oui | Non | Non | . xltm |
| application/vnd. MS-Outlook | Productivité | Non | Non | Non | Non | . MSG |
| application/vnd. MS-Outlook-PST | Productivité/collaboration | Non | Non | Non | Oui | . pst |
| application/vnd. MS-PowerPoint | Document | Oui | Oui | Oui | Non | . ppt;. pps;. cafetière |
| application/vnd. MS-Word. document. macroenabled. 12 | Document | Oui | Oui | Oui | Non | .docm |
| application/vnd. MS-Word. template. macroenabled. 12 | Document | Oui | Oui | Oui | Non | . dotm |
| application/vnd. oasis. OpenDocument. Text | Document | Oui | Oui | Oui | Non | ODT  |
| application/vnd.openxmlformats-officedocument.presentationml.presentation | Document | Oui | Oui | Oui | Non | .pptx |
| application/vnd. openxmlformats-officedocument. PresentationML. slideshow | Productivité/format de document ouvert | Oui | Oui | Oui | Non | . ppsx |
| application/vnd. openxmlformats-officedocument. PresentationML. Template | Document | Oui | Oui | Oui | Non | . potx |
| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet | Document | Oui | Oui | Oui | Non | . xlsx |
| application/vnd. openxmlformats-officedocument. SpreadsheetML. Template | Document | Oui | Oui | Oui | Non | . xltx |
| application/vnd.openxmlformats-officedocument.wordprocessingml.document | Document | Oui | Oui | Oui | Non | . docx |
| application/vnd. openxmlformats-officedocument. WordprocessingML. Template | Document | Oui | Oui | Oui | Non | . dotx |
| application/vnd. Visio | Document | Oui | Oui | Oui | Non | . VSD |
| application/x-7z-compressé | Archive/conteneur | Non | Non | Non | Oui | .7z |
| application/XHTML + XML | Document | Oui | Oui | Oui | Non | . XHTML |
| application/XML | Document | Oui | Oui | Oui | Non | . Xml |
| application/x-Msaccess | Document | Oui | Oui | Oui | Non | . mdb |
| application/x-mspublisher | Document | Oui | Oui | Oui | Non | . pub |
| application/x-rar-Compressed | Archive/conteneur | Non | Non | Non | Oui | . rar |
| application/code postal | Archive/conteneur | Non | Non | Non | Oui | . zip |
| image/BMP | Image | Oui | Oui | Oui | Non | . bmp |
| image/EMF | Image | Oui | Oui | Oui | Non | . EMF |
| image/gif | Document | Oui | Oui | Oui | Non | . gif |
| image/jpeg | Image | Oui | Oui | Oui | Non | . jpg;. jpeg;. dat;. jpgt |
| image/png | Image | Oui | Oui | Oui | Non | . png |
| image/TIFF | Image | Oui | Oui | Oui | Non | . TIF |
| image/vnd. dwg | Document | Oui | Oui | Oui | Non | . dwg;. format |
| image/WMF | Document | Oui | Oui | Oui | Non | . wmf |
| Message/RFC822 | Productivité/collaboration | Non | Non | Non | Non | . eml |
| texte/CSV | Document | Oui | Oui | Oui | Non | . csv |
| texte/html | Document | Oui | Oui | Oui | Non | . html;. shtml;. htm |
| text/plain | Document | Oui | Oui | Oui | Non | . txt;. css;. con;. pl;. csv;. dat |
| Text/vCard-contact | Document | Oui | Oui | Oui | Non | . vcf |
||||||||