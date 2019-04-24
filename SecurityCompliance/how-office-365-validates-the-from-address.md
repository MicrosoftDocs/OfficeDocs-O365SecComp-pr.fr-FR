---
title: Comment Office 365 valide l'adresse de pour empêcher le hameçonnage
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
ms.collection:
- M365-security-compliance
description: 'Pour éviter les attaques par hameçonnage, Office 365 et Outlook.com requièrent désormais une conformité RFC pour from: Addresses.'
ms.openlocfilehash: e540e56a7a40d13a92719865fccefefa61de47c2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32253932"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a>Comment Office 365 valide l'adresse de pour empêcher le hameçonnage

Les comptes de messagerie Office 365 et Outlook.com reçoivent un nombre plus élevé d'attaques par hameçonnage. L'une des techniques utilisées par les auteurs de phishing est d'envoyer des messages dont la valeur pour l'adresse de: n'est pas conforme à la norme [RFC 5322](https://tools.ietf.org/html/rfc5322). L'adresse from: est également appelée l'adresse 5322. from. Pour éviter ce type de hameçonnage, Office 365 et Outlook.com requièrent que les messages reçus par le service incluent une adresse à partir de la RFC telle que décrite dans cet article.
  
> [!NOTE]
> Les informations contenues dans cet article vous obligent à comprendre le format général des adresses de messagerie. Pour plus d'informations, reportez-vous à [rfc 5322](https://tools.ietf.org/html/rfc5322) (en particulier les sections 3.2.3, 3,4 et 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), ainsi que [RFC 3696](https://tools.ietf.org/html/rfc3696). Cet article traite de l'application de la stratégie pour l'adresse 5322. from. Cet article ne traite pas de l'adresse 5321. MailFrom. 
  
Malheureusement, il existe toujours des serveurs de messagerie hérités sur Internet qui continuent à envoyer des messages électroniques «légitimes» dont l'adresse est manquante ou incorrecte:. Si vous recevez régulièrement du courrier électronique d'organisations qui utilisent ces systèmes hérités, encouragez ces organisations à mettre à jour leurs serveurs de messagerie afin de se conformer aux normes de sécurité modernes.
  
Microsoft commencera à déployer la mise en œuvre des stratégies décrites dans cet article le 9 novembre 2017.
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a>Comment Office 365 applique l'utilisation d'une adresse valide from: pour éviter les attaques par hameçonnage

Office 365 apporte des modifications à la façon dont il applique l'utilisation de l'adresse de: dans les messages qu'il reçoit afin de mieux vous protéger contre les attaques par hameçonnage. Contenu de cet article :
  
- [Tous les messages doivent inclure une adresse valide:](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [Format de l'adresse de: Si vous n'incluez pas de nom d'affichage](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [Format de l'adresse de: Si vous incluez un nom d'affichage](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [Exemples supplémentaires d'adresses valides et non valides:](how-office-365-validates-the-from-address.md#Examples)
    
- [Supprimer les réponses automatiques à votre domaine personnalisé sans rompre la stratégie de:](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [Remplacement d'Office 365 de: stratégie de mise en œuvre des adresses](how-office-365-validates-the-from-address.md#Override)
    
- [Autres méthodes pour prévenir et protéger contre les cybercriminels dans Office 365](how-office-365-validates-the-from-address.md#OtherProtection)
    
L'envoi de la part d'un autre utilisateur n'est pas affecté par cette modification, pour plus d'informations, consultez le blog de Thierry Zink «[que dois-je dire lorsque nous faisons référence à l'expéditeur d'un e-mail?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)».
  
### <a name="all-messages-must-include-a-valid-from-address"></a>Tous les messages doivent inclure une adresse valide:
<a name="MustIncludeFromAddress"> </a>

Certains messages automatisés n'incluent pas une adresse de: lorsqu'ils sont envoyés. Dans le passé, lorsque Office 365 ou Outlook.com a reçu un message sans l'adresse de l'adresse:, le service a ajouté l'adresse suivante: par défaut du message afin de le faire livrer:
  
```
From: <>
```

À partir du 9 novembre 2017, Office 365 effectuera le déploiement des modifications apportées à ses centres de messages et serveurs de messagerie, ce qui appliquera une nouvelle règle lorsque les messages sans adresse de l'expéditeur ne seront plus acceptés par Office 365 ou Outlook.com. Au lieu de cela, tous les messages reçus par Office 365 doivent déjà contenir une adresse valide:. Dans le cas contraire, le message est envoyé vers le dossier courrier inDésirable ou éléments supprimés dans Outlook.com et Office 365. 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a>Vue d'ensemble de la syntaxe: format valide pour l'adresse de: pour Office 365
<a name="SyntaxOverviewFromAddress"> </a>

Le format de la valeur de l'adresse de: est défini en détail dans plusieurs RFC. Il existe de nombreuses variantes de l'adressage et ce qui peut être considéré comme valide ou non valide. Pour simplifier, Microsoft vous recommande d'utiliser le format et les définitions suivants:
  
```
From: "displayname " <emailaddress >
```

Où :
  
- Module  *DisplayName* est une expression qui décrit le propriétaire de l'adresse de messagerie. Par exemple, il peut s'agir d'un nom plus convivial pour décrire l'expéditeur que le nom de la boîte aux lettres. L'utilisation d'un nom complet est facultative. Toutefois, si vous choisissez d'utiliser un nom complet, Microsoft vous recommande de toujours le placer entre guillemets comme illustré ci-dessous. 
    
- Exige  *EmailAddress* est constituée des éléments suivants: 
    
  ```
  local-part @domain
  ```

    Où :
    
  - Exige  le *composant local* est une chaîne qui identifie la boîte aux lettres associée à l'adresse. Cela est unique au sein du domaine. Souvent, le nom d'utilisateur ou le GUID du propriétaire de la boîte aux lettres est utilisé comme valeur de la partie locale. 
    
  - Exige  *Domain* est le nom de domaine complet (FQDN) du serveur de messagerie qui héberge la boîte aux lettres identifiée par la partie locale de l'adresse de messagerie. 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a>Format de l'adresse de: Si vous n'incluez pas de nom d'affichage
<a name="FormatNoDisplayName"> </a>

Une adresse à partir de la mise en forme: l'adresse qui n'inclut pas de nom d'affichage n'inclut qu'une seule adresse de messagerie avec ou sans chevrons. Microsoft recommande de ne pas séparer les chevrons avec des espaces. En outre, n'incluez rien après l'adresse de messagerie.
  
Les exemples suivants sont valides:
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

L'exemple suivant est valide mais pas recommandé, car il contient des espaces entre les chevrons et l'adresse de messagerie:
  
```
From: < sender@contoso.com >
```

L'exemple suivant n'est pas valide, car il contient du texte après l'adresse de messagerie:
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a>Format de l'adresse de: Si vous incluez un nom d'affichage
<a name="FormatDisplayName"> </a>

Pour from: les adresses qui incluent une valeur pour le nom d'affichage, les règles suivantes s'appliquent:
  
- Si l'adresse de l'expéditeur inclut un nom complet et que le nom d'affichage inclut une virgule, le nom d'affichage doit être placé entre guillemets. Par exemple :
    
    L'exemple suivant est valide:
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    L'exemple suivant n'est pas valide:
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    Ne pas placer le nom d'affichage entre guillemets si ce nom d'affichage inclut une virgule n'est pas valide conformément à la norme RFC 5322.
    
    Il est recommandé de placer les guillemets entourant le nom d'affichage, qu'il y ait ou non une virgule dans le nom d'affichage.
    
- Si l'adresse de l'expéditeur inclut un nom complet, l'adresse de messagerie doit être placée entre crochets pointus.
    
    Nous vous recommandons vivement d'insérer un espace entre le nom d'affichage et l'adresse de messagerie.
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a>Exemples supplémentaires d'adresses valides et non valides:
<a name="Examples"> </a>

- Validation
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- Non valide. L'adresse de messagerie n'est pas entourée de crochets pointus:
    
  ```
  From: Office 365 sender@contoso.com
  ```

- Valide, mais pas recommandée. Le nom d'affichage n'est pas entouré de guillemets. Pour une meilleure pratique, placez toujours le nom d'affichage entre guillemets:
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- Non valide. Tout est placé entre guillemets, pas seulement le nom d'affichage:
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- Non valide. Il n'y a pas d'équerre entourant l'adresse de messagerie:
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- Non valide. Il n'y a pas d'espace entre le nom d'affichage et le crochet pointu gauche:
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- Non valide. Il n'y a pas d'espace entre le guillemet de fermeture entourant le nom d'affichage et le crochet pointu gauche.
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a>Supprimer les réponses automatiques à votre domaine personnalisé sans rompre la stratégie de:
<a name="SuppressAutoReply"> </a>

Avec la nouvelle from: application de stratégie, vous ne pouvez plus utiliser from \< \> : pour supprimer les réponses automatiques. Au lieu de cela, vous devez configurer un enregistrement MX null pour votre domaine personnalisé.
  
L'enregistrement de serveur de messagerie (MX) est un enregistrement de ressource dans le DNS qui identifie le serveur de messagerie qui reçoit les messages pour votre domaine. Les réponses automatiques (et toutes les réponses) sont naturellement supprimées car il n'existe aucune adresse publiée à laquelle le serveur de réponse peut envoyer des messages.
  
Lorsque vous configurez un enregistrement MX null pour votre domaine personnalisé:
  
- Choisissez un domaine à partir duquel envoyer des messages qui n'acceptent pas (recevoir) des courriers électroniques. Par exemple, si votre domaine principal est contoso.com, vous pouvez choisir noreply.contoso.com.
    
- ConFigurez l'enregistrement MX null pour votre domaine. Un enregistrement MX null se compose d'un point unique, par exemple:
    
  ```
  noreply.contoso.com IN MX .
  ```

Pour plus d'informations sur la publication d'une valeur null MX, voir [RFC 7505](https://tools.ietf.org/html/rfc7505).
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a>Remplacement d'Office 365 de: stratégie de mise en œuvre des adresses
<a name="Override"> </a>

Une fois le déploiement de la nouvelle stratégie terminé, vous pouvez uniquement contourner cette stratégie pour le courrier entrant que vous recevez d'Office 365 à l'aide de l'une des méthodes suivantes: 
  
- Listes d'adresses IP autorisées
    
- Règles de flux de messagerie Exchange Online
    
Microsoft recommande fortement de remplacer l'application de la stratégie from:. Le remplacement de cette stratégie peut augmenter le risque d'exposition de votre organisation au courrier indésirable, au hameçonnage et à d'autres crimes.
  
Vous ne pouvez pas remplacer cette stratégie pour les messages sortants que vous envoyez dans Office 365. De plus, Outlook.com n'autorisera pas les remplacements, même via la prise en charge. 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a>Autres méthodes pour prévenir et protéger contre les cybercriminels dans Office 365
<a name="OtherProtection"> </a>

Pour plus d'informations sur la façon dont vous pouvez renforcer votre organisation contre les cybercriminels, tels que le hameçonnage, le courrier indésirable, les violations de données et d'autres menaces, consultez la rubrique [meilleures pratiques en matière de sécurité pour Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).
  
## <a name="related-topics"></a>Voir aussi

[Messages de rétrodiffusion et EOP](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

