---
title: Types de fichiers pris en charge dans Advanced eDiscovery
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
ms.openlocfilehash: d8e9689cb04929137787225579dcda17005c8bfe
ms.sourcegitcommit: 7be8617ce75909f0fa1a2f6e72749e2ef4bb2d3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2019
ms.locfileid: "34088807"
---
# <a name="supported-file-types-in-advanced-ediscovery"></a>Types de fichiers pris en charge dans Advanced eDiscovery

Advanced eDiscovery prend en charge de nombreux types de fichiers à différents niveaux, décrits dans le tableau suivant. Cette liste n’est pas finalisée, et nous allons ajouter de nouveaux types de fichiers lors de notre test de validation. Le tableau indique si un type de fichier est pris en charge pour l’extraction de texte (OCR pour les images), affichable dans la visionneuse native et également pris en charge dans la visionneuse d’annotations dans Advanced eDiscovery.

## <a name="archive--container"></a>Archive/conteneur

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de conteneur | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |
| application/x-7z-compressé | Oui | Oui | Oui | .7z |
| application/x-rar-Compressed | Oui | Oui | Oui | . rar |
| application/tar x | Oui | Oui | Oui | . tar |
| application/code postal | Oui | Oui | Oui | . zip |
||||||||

## <a name="database"></a>Database

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/x-Msaccess | Oui | Oui | Oui | Non | Non | . mdb |
||||||||

## <a name="email"></a>E-mail

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-Outlook | Oui | Oui | Oui | Oui | Oui | . MSG |
| Message/RFC822 | Oui | Oui | Oui | Oui | Oui | . eml |
| Text/vCard-contact | Oui | Oui | Oui | Oui | Oui | . vcf |
||||||||

## <a name="email-container"></a>Conteneur de courrier électronique

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de conteneur | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |
| application/mbox | Oui | Oui | Oui | . mbox |
| application/vnd. MS-Outlook-PST | Oui | Oui | Oui | . pst |
||||||||

## <a name="html"></a>HTML

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/XHTML + XML | Oui | Oui | Oui | Oui | Oui | . XHTML |
| application/XML | Oui | Oui | Oui | Oui | Oui | . Xml |
| texte/html | Oui | Oui | Oui | Oui | Oui | . htm;. html;. shtml |
||||||||

## <a name="image"></a>Image

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte OCR | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| image/BMP | Oui | Oui | Oui | Oui | Oui | .bmp |
| image/EMF | Oui | Oui | Oui | Oui | Oui | . EMF |
| image/gif | Oui | Oui | Oui | Oui | Oui | .gif |
| image/jpeg | Oui | Oui | Oui | Oui | Oui | . jpeg;. jpg |
| image/png | Oui | Oui | Oui | Oui | Oui | .png |
| image/SVG + XML | Oui | Oui | Oui | Oui | Non | . svg |
| image/TIFF | Oui | Oui | Oui | Oui | Oui | . TIF |
| image/vnd. dwg | Oui | Oui | Oui | Oui | Oui | . dwg;. DXF |
| image/WMF | Oui | Oui | Oui | Oui | Oui | . wmf |
||||||||

## <a name="microsoft-excel"></a>Microsoft Excel

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-Excel | Oui | Oui | Oui | Oui | Oui | . dat;. xls |
| application/vnd. MS-Excel. Sheet. Binary. macroenabled. 12 | Oui | Oui | Oui | Oui | Non | . xlsb |
| application/vnd. MS-Excel. Sheet. macroenabled. 12 | Oui | Oui | Oui | Oui | Oui | . xlsm |
| application/vnd. MS-Excel. template. macroenabled. 12 | Oui | Oui | Oui | Non | Non | . xltm |
| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet | Oui | Oui | Oui | Oui | Oui | . xlsx |
| application/vnd. openxmlformats-officedocument. SpreadsheetML. Template | Oui | Oui | Oui | Oui | Oui | . xltx |
||||||||

## <a name="microsoft-powerpoint"></a>Microsoft PowerPoint

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-PowerPoint | Oui | Oui | Oui | Oui | Oui | . pot;. pps;. ppt |
| application/vnd.openxmlformats-officedocument.presentationml.presentation | Oui | Oui | Oui | Oui | Oui | .pptx |
| application/vnd. openxmlformats-officedocument. PresentationML. slideshow | Oui | Oui | Oui | Oui | Oui | . ppsx |
| application/vnd. openxmlformats-officedocument. PresentationML. Template | Oui | Oui | Oui | Oui | Oui | . potx |
||||||||

## <a name="microsoft-publisher"></a>Microsoft Publisher

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/x-mspublisher | Oui | Oui | Oui | Oui | Oui | . pub |
||||||||

## <a name="microsoft-visio"></a>Microsoft Visio

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-Visio. Drawing | Oui | Oui | Oui | Oui | Non |  |
| application/vnd. Visio | Oui | Oui | Oui | Oui | Oui | . VSD |
||||||||

## <a name="microsoft-word"></a>Microsoft Word

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/msword | Oui | Oui | Oui | Oui | Oui | . dat;. doc |
| application/format RTF | Oui | Oui | Oui | Oui | Oui | . doc;. rtf |
| application/vnd. MS-Word. document. macroenabled. 12 | Oui | Oui | Oui | Oui | Oui | .docm |
| application/vnd. MS-Word. template. macroenabled. 12 | Oui | Oui | Oui | Oui | Oui | . dotm |
| application/vnd.openxmlformats-officedocument.wordprocessingml.document | Oui | Oui | Oui | Oui | Oui | . docx |
| application/vnd. openxmlformats-officedocument. WordprocessingML. Template | Oui | Oui | Oui | Oui | Oui | . dotx |
||||||||

## <a name="microsoft-works"></a>Microsoft Works

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. ms-Works-SS | Oui | Oui | Non | Non | Non | . WPS |
| application/vnd. ms-Works-WP | Oui | Oui | Non | Non | Non | . WPS |
||||||||

## <a name="open-document-format"></a>Format Open Document

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. oasis. OpenDocument. Text | Oui | Oui | Oui | Oui | Oui | . odt |
||||||||

## <a name="other"></a>Other

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/json | Oui | Oui | Oui | Oui | Oui | N/A |
| application/vnd. MS-Graph | Oui | Oui | Non | Non | Non |  |
| application/winhlp | Oui | Oui | Non | Non | Non | . hlp |
| application/x-TNEF | Oui | Oui | Non | Non | Non |  |
||||||||

## <a name="plain-text"></a>Texte brut

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| texte/CSV | Oui | Oui | Oui | Oui | Oui | . csv |
| text/plain | Oui | Oui | Oui | Oui | Oui | . con;. css;. csv;. dat;. pl;. txt |
||||||||

## <a name="portable-document-format"></a>Portable Document Format

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/pdf | Oui | Oui | Oui | Oui | Oui | .pdf |
||||||||

## <a name="word-perfect"></a>Word Perfect

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. WordPerfect; version = 5.0 | Oui | Oui | Oui | Non | Non | . wpd |
| application/vnd. WordPerfect; version = 5.1 | Oui | Oui | Oui | Non | Non | . wpd |
| application/vnd. WordPerfect; version = 6. x | Oui | Oui | Oui | Non | Non | . wpd |
||||||||

## <a name="word-pro"></a>Word Pro

| Type MIME | Identification de fichier | Extraction de métadonnées | Extraction de texte | Visionneuse Native | Visionneuse d’annotations | Extensions possibles |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. Lotus-WordPro | Oui | Oui | Non | Non | Non | . LWP |
||||||||
