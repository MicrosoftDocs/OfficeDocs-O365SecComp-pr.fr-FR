---
title: Création d'une empreinte numérique de document
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: exchange-online
localization_priority: Normal
ms.assetid: 1e0c579c-26e0-462a-a1b0-d7506dfe05fa
description: Travailleurs de l’information dans votre organisation gérer toutes sortes d’informations sensibles pendant une journée normale. Création d’empreintes de document facilite la protection de ces informations en identifiant les formulaires standard qui sont utilisés au sein de votre organisation. Cette rubrique décrit les concepts empreinte numérique de Document et comment en créer un à l’aide de PowerShell.
ms.openlocfilehash: d73b769e7a014f2642a0fcd66cc6a500c68c46c3
ms.sourcegitcommit: 4be502d1fc6cbaef4c72d599758d51efe3a173c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23867492"
---
# <a name="document-fingerprinting"></a>Création d'une empreinte numérique de document

Travailleurs de l’information dans votre organisation gérer toutes sortes d’informations sensibles pendant une journée normale. Dans la sécurité &amp; centre de conformité, l’empreinte numérique de Document facilite pour vous permet de protéger ces informations en identifiant les formulaires standard qui sont utilisés au sein de votre organisation. Cette rubrique décrit les concepts empreinte numérique de Document et comment en créer un à l’aide de PowerShell.
  
## <a name="basic-scenario-for-document-fingerprinting"></a>Scénario de base de création d'une empreinte numérique de document

Création d’empreintes de document est une fonctionnalité de prévention de perte de données (DLP) qui convertit un formulaire standard en un type d’informations sensibles, vous pouvez utiliser dans les règles de vos stratégies DLP. Par exemple, vous pouvez créer une empreinte numérique de document basée sur un modèle de brevet vide et ensuite créer une stratégie DLP qui détecte et bloque tous les modèles de brevets sortants avec contenu sensible renseignés. Si vous le souhaitez, vous pouvez configurer [les conseils de stratégie](use-notifications-and-policy-tips.md) pour informer les expéditeurs qu’ils peuvent envoyer des informations sensibles, et l’expéditeur doit vérifier que les destinataires sont autorisés à recevoir les brevets. Ce processus fonctionne avec les formulaires basés sur texte utilisés dans votre organisation. Voici des exemples de formulaires que vous pouvez télécharger supplémentaires : 
  
- Formulaires officiels
    
- Formulaires de conformité relatifs à la loi américaine HIPAA (Health Insurance Portability Accountability Act)
    
- Formulaires d'informations sur les employés pour les services de ressources humaines
    
- Formulaires personnalisés créés spécialement pour votre organisation
    
Dans l’idéal, votre organisation possède déjà une pratique établie de l’utilisation de certaines formes pour transmettre des informations sensibles. Après avoir téléchargé un formulaire vide pour être converti en une empreinte numérique de document et définir une stratégie correspondante, le DLP détecte tous les documents dans les messages sortants qui correspondent à cette empreinte.
  
## <a name="how-document-fingerprinting-works"></a>Fonctionnement de l'empreinte numérique de document

Vous avez probablement déjà deviner que les documents n’ont empreintes digitales réels, mais le nom explique la fonctionnalité. De la même manière que les empreintes digitales d’une personne possèdent des modèles uniques, les documents ont des modèles mot unique. Lorsque vous téléchargez un fichier, DLP identifie le modèle word unique dans le document, crée une empreinte numérique de document basée sur ce modèle et utilise cette empreinte numérique de document pour détecter les documents sortants contenant le même modèle. C’est pourquoi le téléchargement d’un formulaire ou modèle crée le type de l’empreinte numérique de document plus efficace. Toute personne qui remplit un formulaire utilise le même ensemble d’origine de mots et ajoute ensuite des mots son propre au document. Tant que le document sortant n’est pas protégé par mot de passe et contient tout le texte à partir du formulaire d’origine, DLP peut déterminer si le document correspond à l’empreinte numérique de document.
  
L'exemple suivant montre ce qui se passe si vous créez une empreinte numérique de document basée sur un modèle de brevet, mais vous pouvez utiliser n'importe quel formulaire comme base pour la création d'une empreinte numérique de document.
  
**Exemple d'un document de brevet correspondant à l'empreinte numérique de document d'un modèle de brevet**

![Document_Fingerprinting_diagram.png](media/Document_Fingerprinting_diagram.png)
  
Le modèle de brevet contient les champs vides « Title brevet », « Inventeurs, » et « Description » et des descriptions pour chacun de ces champs, qui est le modèle word. Lorsque vous téléchargez le modèle de brevet d’origine, il est dans un des types de fichiers pris en charge et en texte brut. Convertit DLP ce modèle word dans une empreinte numérique de document, qui est une petite XML Unicode contenant une valeur de hachage unique représentant le texte d’origine et l’empreinte numérique du fichier est enregistré en tant qu’une classification des données dans Active Directory. (Comme mesure de sécurité, le document d’origine n’est pas stocké sur le service ; uniquement la valeur de hachage est stockée et le document d’origine ne peuvent pas être reconstruit à partir de la valeur de hachage.) L’empreinte numérique de brevet devient alors un type d’informations sensibles que vous pouvez associer à une stratégie DLP. Une fois que vous associez l’empreinte numérique à une stratégie DLP, DLP détecte les messages électroniques sortants contenant des documents qui correspondent à l’empreinte numérique de brevet et traite en fonction de la stratégie de votre organisation. 

Par exemple, vous pouvez souhaiter définir une stratégie DLP qui empêche les employés d’envoyer des messages sortants contenant des brevets. DLP utilisera l’empreinte numérique de brevet pour détecter des brevets et bloquer les messages électroniques. Autrement, vous souhaiterez laisser votre service juridique pour être en mesure d’envoyer des brevets à d’autres organisations, car il a une entreprise besoin pour cela. Vous pouvez autoriser des services spécifiques envoyer des informations sensibles en créant des exceptions de ces services dans votre stratégie DLP, ou vous pouvez les autoriser à remplacer un Conseil de stratégie avec une justification.
  
### <a name="supported-file-types"></a>Types de fichiers pris en charge

Création d’empreintes de document prend en charge les mêmes types de fichier pris en charge dans les règles de transport. Pour obtenir la liste des types de fichiers pris en charge, voir [types de fichiers pris en charge pour l’analyse du contenu mail flow règle](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection). Une note rapide sur les types de fichier : règles de transport ni empreinte numérique de Document prend en charge le type de fichier .dotx, qui peut être source de confusion car il s’agit d’un fichier de modèle dans Word. Lorsque vous voyez le mot « modèle » dans cet article et autres rubriques empreinte numérique de Document, il fait référence à un document que vous avez établi comme un formulaire standard, pas le type de fichier de modèle.
  
#### <a name="limitations-of-document-fingerprinting"></a>Limites de l'empreinte numérique de document

Création d’empreintes de document ne détectera pas d’informations sensibles dans les cas suivants :
  
- Si les fichiers sont protégés par mot de passe
    
- Si les fichiers contiennent uniquement des images
    
- Si les documents ne contiennent pas l'intégralité du texte du formulaire d'origine utilisé pour créer l'empreinte numérique de document
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a>Utilisation de PowerShell pour créer un package de règles de classification basé sur l’empreinte numérique de document

Notez que vous pouvez en créer une empreinte numérique de document uniquement à l’aide de PowerShell dans la sécurité &amp; centre de conformité. Pour vous connecter, voir [se connecter à Office 365 sécurité & PowerShell du centre de conformité](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

DLP utilise les packages de règles de classification pour détecter les contenus sensibles. Pour créer un package de règles de classification basé sur une empreinte numérique de document, utilisez les applets de commande **New-DlpFingerprint** et **New-DlpSensitiveInformationType** . Étant donné que les résultats de **New-DlpFingerprint** ne sont pas stockés en dehors de la règle de classification des données, vous toujours exécuter **New-DlpFingerprint** et **New-DlpSensitiveInformationType** ou **Set-DlpSensitiveInformationType** dans le même Session PowerShell. L’exemple suivant crée une nouvelle empreinte numérique de document basée sur le fichier C:\My Documents\Contoso Employee Template.docx. Vous stockez la nouvelle empreinte en tant que variable afin que vous pouvez l’utiliser avec l’applet de commande **New-DlpSensitiveInformationType** dans la même session PowerShell. 
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Employee Template.docx" -Encoding byte -ReadCount 0
$Employee_Fingerprint = New-DlpFingerprint -FileData $Employee_Template -Description "Contoso Employee Template"
```

À présent, nous allons créer une règle de classification des données nommée « Contoso Employee Confidential » qui utilise l'empreinte numérique de document du fichier C:\My Documents\Contoso Customer Information Form.docx.
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Customer Information Form.docx" -Encoding byte -ReadCount 0
$Customer_Fingerprint = New-DlpFingerprint -FileData $Customer_Form -Description "Contoso Customer Information Form"
New-DlpSensitiveInformationType -Name "Contoso Customer Confidential" -Fingerprints $Customer_Fingerprint -Description "Message contains Contoso customer information." 
```

Vous pouvez désormais utiliser l’applet de commande **Get-DlpSensitiveInformationType** pour rechercher tous les packages de règles de classification des données DLP et, dans cet exemple, « Contoso Customer Confidential » fait partie de la liste de packages de règles de classification des données. 
  
Enfin, ajoutez le package de règles de classification des données « Contoso Customer Confidential » à une stratégie DLP dans la sécurité &amp; centre de conformité. Cet exemple ajoute une règle à une stratégie DLP existante nommée « ConfidentialPolicy ».

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

Vous pouvez également utiliser le package de règles de classification des données dans les règles de transport dans Exchange Online, comme illustré dans l’exemple suivant. Pour exécuter cette commande, vous devez d’abord [se connecter à Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Notez également que le temps requis pour le package de règles de synchronisation de la sécurité &amp; centre de conformité pour le centre d’administration Exchange.
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

DLP détecte désormais les documents qui correspondent à l’empreinte numérique de document Contoso Customer Form.docx.
  
Pour plus d’informations sur la syntaxe et les paramètres, voir :

- [Nouvelle DlpFingerprint](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [Nouvelle DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [Remove-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [Set-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [Get-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)
