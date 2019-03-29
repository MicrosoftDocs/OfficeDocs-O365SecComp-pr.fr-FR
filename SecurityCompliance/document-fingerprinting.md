---
title: Création d'une empreinte numérique de document
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
search.appverid: MET150
ms.service: exchange-online
ms.collection: M365-security-compliance
localization_priority: Normal
description: Les professionnels de l'informatique de votre organisation gèrent toutes sortes d'informations sensibles au cours d'une journée typique. La création d'une empreinte numérique de document facilite la protection de ces informations en identifiant les formulaires standard utilisés au sein de votre organisation. Cette rubrique décrit les concepts sous-jacents à la création d'une empreinte numérique de document et la manière d'en créer une à l'aide de PowerShell.
ms.openlocfilehash: bf28d1d901598337a5c9c18d80590b136c539d26
ms.sourcegitcommit: a79eb9907759d4cd849c3f948695a9ff890b19bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2019
ms.locfileid: "30866350"
---
# <a name="document-fingerprinting"></a>Création d’une empreinte numérique de document

Les professionnels de l'informatique de votre organisation gèrent toutes sortes d'informations sensibles au cours d'une journée typique. Dans le centre &amp; de sécurité conformité, la création d'une empreinte numérique de document facilite la protection de ces informations en identifiant les formulaires standard utilisés dans votre organisation. Cette rubrique décrit les concepts sous-jacents à la création d'une empreinte numérique de document et la manière d'en créer une à l'aide de PowerShell.
  
## <a name="basic-scenario-for-document-fingerprinting"></a>Scénario de base de création d’une empreinte numérique de document

La création d'une empreinte numérique de document est une fonctionnalité de protection contre la perte de données (DLP) qui permet de convertir un formulaire standard en un type d'informations sensibles que vous pouvez utiliser dans les règles de vos stratégies DLP. Par exemple, vous pouvez créer une empreinte numérique de document basée sur un modèle de brevet vierge, puis créer une stratégie DLP qui détecte et bloque tous les modèles de brevet sortants comportant des informations sensibles. Si vous le souhaitez, vous pouvez configurer des [conseils de stratégie](use-notifications-and-policy-tips.md) pour informer les expéditeurs qu'ils peuvent envoyer des informations sensibles et que l'expéditeur doit vérifier que les destinataires sont qualifiés pour recevoir les brevets. Ce processus fonctionne avec n'importe quel formulaire texte utilisé dans votre organisation. Voici d'autres exemples de formulaires que vous pouvez télécharger : 
  
- Formulaires officiels
    
- Formulaires de conformité relatifs à la loi américaine HIPAA (Health Insurance Portability Accountability Act)
    
- Formulaires d'informations sur les employés pour les services de ressources humaines
    
- Formulaires personnalisés créés spécialement pour votre organisation
    
Dans l'idéal, votre organisation a pour habitude professionnelle d'utiliser certains formulaires pour la transmission d'informations sensibles. Une fois que vous avez téléchargé un formulaire vide à convertir en empreinte numérique de document et configuré une stratégie correspondante, le DLP détecte tous les documents dans les messages sortants qui correspondent à cette empreinte digitale.
  
## <a name="how-document-fingerprinting-works"></a>Fonctionnement de l’empreinte numérique de document

Vous avez probablement déjà deviné que les documents n'ont pas d'empreintes digitales réelles, mais le nom contribue à expliquer la fonctionnalité. De la même manière que les empreintes digitales d'une personne répondent à des modèles uniques, les documents répondent à des modèles de mots uniques. Lorsque vous chargez un fichier, DLP identifie le modèle de mot unique dans le document, crée une empreinte numérique de document basée sur ce modèle et utilise cette empreinte numérique de document pour détecter les documents sortants contenant le même modèle. C'est pourquoi le téléchargement d'un formulaire ou d'un modèle permet de créer le type d'empreinte numérique de document le plus efficace. Toute personne qui remplit un formulaire utilise le même ensemble de mots d'origine, puis ajoute ses propres mots au document. Tant que le document sortant n'est pas protégé par mot de passe et qu'il contient tout le texte du formulaire d'origine, DLP peut déterminer si le document correspond à l'empreinte numérique de document.
  
L'exemple suivant montre ce qui se passe si vous créez une empreinte numérique de document basée sur un modèle de brevet, mais vous pouvez utiliser n'importe quel formulaire comme base pour la création d'une empreinte numérique de document.
  
**Exemple d'un document de brevet correspondant à l'empreinte numérique de document d'un modèle de brevet**

![Document_Fingerprinting_diagram. png](media/Document_Fingerprinting_diagram.png)
  
Le modèle brevet contient les champs vides «titre du brevet», «stocks» et «description», ainsi que les descriptions pour chacun de ces champs, c'est-à-dire le modèle Word. Lorsque vous téléchargez le modèle de brevet d'origine, il se trouve dans l'un des types de fichier pris en charge et en texte brut. DLP convertit ce modèle Word en empreinte digitale de document, qui est un petit fichier XML Unicode contenant une valeur de hachage unique représentant le texte d'origine, et l'empreinte digitale est enregistrée en tant que classification des données dans Active Directory. (Par mesure de sécurité, le document d'origine n'est pas stocké sur le service; seule la valeur de hachage est stockée et le document d'origine ne peut pas être reconstruit à partir de la valeur de hachage.) L'empreinte de brevet devient alors un type d'informations sensibles que vous pouvez associer à une stratégie DLP. Une fois que vous avez associé l'empreinte digitale à une stratégie DLP, DLP détecte tous les messages électroniques sortants contenant des documents qui correspondent à l'empreinte digitale du brevet et les traite en fonction de la stratégie de votre organisation. 

Par exemple, vous pouvez configurer une stratégie DLP qui empêche les employés normaux d'envoyer des messages sortants contenant des brevets. DLP utilise l'empreinte digitale brevet pour détecter les brevets et bloquer ces e-mails. Vous pouvez également permettre à votre service juridique d'envoyer des brevets à d'autres organisations, car ils ont besoin d'une activité professionnelle. Vous pouvez autoriser des services spécifiques à envoyer des informations sensibles en créant des exceptions pour ces services dans votre stratégie DLP, ou vous pouvez leur permettre de remplacer un Conseil de stratégie par une justification professionnelle.
  
### <a name="supported-file-types"></a>Types de fichiers pris en charge

La création d'une empreinte numérique de document prend en charge les mêmes types de fichiers que ceux pris en charge dans les règles de flux de messagerie (également appelées règles de transport). Pour obtenir la liste des types de fichiers pris en charge, consultez la rubrique [types de fichiers pris en charge pour l'inspection du contenu des règles de flux de messagerie](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection). Une note rapide sur les types de fichiers: ni les règles de flux de messagerie, ni l'empreinte numérique de document ne prennent en charge le type de fichier. dotx, ce qui peut prêter à confusion car il s'agit d'un fichier de modèle dans Word. Lorsque le mot «modèle» apparaît dans cette rubrique et dans d'autres rubriques relatives à l'empreinte numérique de document, il fait référence à un document que vous avez établi en tant que formulaire standard, et non au type de fichier de modèle.
  
#### <a name="limitations-of-document-fingerprinting"></a>Limites de l’empreinte numérique de document

L'empreinte numérique de document ne détecte pas les informations sensibles dans les cas suivants:
  
- Si les fichiers sont protégés par mot de passe
    
- Si les fichiers contiennent uniquement des images
    
- Si les documents ne contiennent pas l'intégralité du texte du formulaire d'origine utilisé pour créer l'empreinte numérique de document
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a>Utiliser PowerShell pour créer un package de règles de classification basé sur l'empreinte numérique de document

Notez que vous pouvez créer une empreinte numérique de document uniquement à l'aide de PowerShell &amp; dans le centre de sécurité conformité. Pour vous connecter, voir [Connect to Office 365 Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

DLP utilise les packages de règles de classification pour détecter le contenu sensible. Pour créer un package de règles de classification basé sur une empreinte numérique de document, utilisez les cmdlets **New-DlpFingerprint** et **New-DlpSensitiveInformationType** . Étant donné que les résultats de **New-DlpFingerprint** ne sont pas stockés en dehors de la règle de classification des données, vous devez toujours exécuter **New-DlpFingerprint** et **New-DlpSensitiveInformationType** ou **Set-DlpSensitiveInformationType** dans le même Session PowerShell. L'exemple suivant crée une empreinte numérique de document à partir du fichier C:\My Documents\Contoso Employee Template.docx. La nouvelle empreinte est stockée en tant que variable pour que vous puissiez l’utiliser avec la cmdlet **New-DlpSensitiveInformationType** dans la même session PowerShell. 
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Employee Template.docx" -Encoding byte -ReadCount 0
$Employee_Fingerprint = New-DlpFingerprint -FileData $Employee_Template -Description "Contoso Employee Template"
```

À présent, nous allons créer une règle de classification des données nommée « Contoso Employee Confidential » qui utilise l'empreinte numérique de document du fichier C:\My Documents\Contoso Customer Information Form.docx.
  
```
$Customer_Form = Get-Content "C:\My Documents\Contoso Customer Information Form.docx" -Encoding byte -ReadCount 0
$Customer_Fingerprint = New-DlpFingerprint -FileData $Customer_Form -Description "Contoso Customer Information Form"
New-DlpSensitiveInformationType -Name "Contoso Customer Confidential" -Fingerprints $Customer_Fingerprint -Description "Message contains Contoso customer information." 
```

Vous pouvez désormais utiliser l'applet de commande **Get-DlpSensitiveInformationType** pour rechercher tous les packages de règles de classification des données DLP et, dans cet exemple, «contoso Customer Confidential» fait partie de la liste des packages de règles de classification des données. 
  
Enfin, ajoutez le package de règles de classification des données «Contoso Customer Confidential» à une stratégie &amp; DLP dans le centre de sécurité conformité. Cet exemple ajoute une règle à une stratégie DLP existante nommée «ConfidentialPolicy».

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

Vous pouvez également utiliser le package de règles de classification des données dans les règles de flux de messagerie dans Exchange Online, comme illustré dans l'exemple suivant. Pour exécuter cette commande, vous devez tout d'abord vous [connecter à Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Notez également que le package de règles doit être synchronisé entre le centre de sécurité &amp; et le centre d'administration Exchange.
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

DLP détecte désormais les documents qui correspondent à l'empreinte numérique de document Customer Form. docx.
  
Pour obtenir des informations sur la syntaxe et les paramètres, voir:

- [New-DlpFingerprint](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [New-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [Remove-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [Set-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [Get-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)
