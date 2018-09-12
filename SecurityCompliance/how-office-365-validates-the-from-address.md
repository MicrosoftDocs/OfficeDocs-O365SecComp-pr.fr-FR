---
title: Comment Office 365 valide l’adresse de provenance pour empêcher l’hameçonnage
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
description: 'Pour éviter l’hameçonnage, Office 365 et Outlook.com requièrent maintenant pour la conformité RFC à partir de : adresses.'
ms.openlocfilehash: 8425d4ef7635c2beddcd7915daf73736432d4ca9
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955426"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a>Comment Office 365 valide l’adresse de provenance pour empêcher l’hameçonnage

Office 365 et les comptes de messagerie Outlook.com recevoir un plus grand nombre d’attaques par hameçonnage. Une technique utiliser phishing consiste à envoyer des messages qui ont des valeurs pour le champ de : adresse qui ne sont pas conformes à [RFC 5322](https://tools.ietf.org/html/rfc5322). From : adresse est également appelée l’adresse 5322.From. Pour éviter ce type d’hameçonnage, Office 365 et Outlook.com exigent des messages reçus par le service pour inclure un compatibles RFC à partir de : adresse comme décrit dans cet article.
  
> [!NOTE]
> Les informations contenues dans cet article, vous devez avoir une connaissance élémentaire du format général des adresses de messagerie. Pour plus d’informations, voir [RFC 5322](https://tools.ietf.org/html/rfc5322) (notamment les sections 3.4.1 3.2.3 et 3.4), [RFC 5321](https://tools.ietf.org/html/rfc5321), ainsi que [RFC 3696](https://tools.ietf.org/html/rfc3696). Cet article est à l’application des stratégies pour l’adresse 5322.From. Cet article n’est pas sur l’adresse 5321.MailFrom. 
  
Malheureusement, il y a encore certains serveurs de messagerie hérités sur Internet qui continuent d’envoyer « légitimes » les messages qui ont un manquant ou mal formées à partir de : adresse. Si vous recevez régulièrement e-mail d’organisations qui utilisent ces systèmes hérités, encourager les organisations à mettre à jour leurs serveurs de messagerie pour se conformer aux normes de sécurité modernes.
  
Microsoft démarrera présentant l’application des stratégies décrites dans cet article sur le 9 novembre 2017.
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a>Comment Office 365 impose l’utilisation de valide à partir de : adresse afin d’empêcher les attaques par hameçonnage

Office 365 est apporter des modifications à la façon dont il impose l’utilisation de la provenance : adresse dans les messages qu’il reçoit afin de mieux vous protéger contre les attaques par hameçonnage. Dans cet article :
  
- [Tous les messages doivent inclure valide à partir de : adresse](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [Format du : adresse si vous n’incluez pas un nom d’affichage](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [Format du : adresse si vous incluez un nom d’affichage](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [Exemples supplémentaires de valides et non valides à partir de : adresses](how-office-365-validates-the-from-address.md#Examples)
    
- [Supprimer des réponses automatiques pour votre domaine personnalisé sans rompre la provenance : stratégie](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [Substitution de l’Office 365 à partir de : stratégie de mise en œuvre d’adresses](how-office-365-validates-the-from-address.md#Override)
    
- [Autres moyens de protéger et à méfaits dans Office 365](how-office-365-validates-the-from-address.md#OtherProtection)
    
L’envoi d’un autre utilisateur n’est pas affectée par cette modification, pour plus d’informations, de lire le blog de Terry Zink «[que nous signifient lorsque nous faisons référence à l’expéditeur d’un message électronique ?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)».
  
### <a name="all-messages-must-include-a-valid-from-address"></a>Tous les messages doivent inclure valide à partir de : adresse
<a name="MustIncludeFromAddress"> </a>

Certains messages automatisées n’incluent pas de : adresse lorsqu’ils sont envoyés. Dans le passé, lorsque Office 365 ou Outlook.com a reçu un message sans From : adresse, le service ajoutée par défaut à partir de : adresse au message afin de rendre le livrable :
  
```
From: <>
```

Démarrer le 9 novembre 2017, Office 365 seront introduites modifications apportées à ses serveurs de messagerie et de centres de données qui appliquent une nouvelle règle d’où des messages sans From : adresse sera n’est plus acceptée par Office 365 ou Outlook.com. Au lieu de cela, tous les messages reçus par Office 365 doivent déjà contenir valide à partir de : adresse. Sinon, le message sera être envoyé vers le courrier indésirable ou éléments supprimés des dossiers dans Outlook.com et Office 365. 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a>Vue d’ensemble de la syntaxe : format valide pour le : adresse pour Office 365
<a name="SyntaxOverviewFromAddress"> </a>

Le format de la valeur de la provenance : adresse est décrite en détail dans plusieurs RFC. Il existe de nombreuses variantes de l’adressage et ce qui peut être considéré comme valide ou non valide. Pour faire simple, Microsoft recommande que vous utilisez les définitions et le format suivant :
  
```
From: "displayname " <emailaddress >
```

Où :
  
- (Facultatif)  *DisplayName* est une expression qui décrit le propriétaire de l’adresse de messagerie. Par exemple, cela peut être un nom plus convivial pour décrire l’expéditeur que le nom de la boîte aux lettres. À l’aide d’un nom d’affichage est facultative. Toutefois, si vous choisissez d’utiliser un nom d’affichage, Microsoft recommande que vous toujours Placez entre guillemets comme indiqué. 
    
- (Requis)  *EmailAddress* est composée de : 
    
  ```
  local-part @domain
  ```

    Où :
    
  - (Requis)  *partie locale* est une chaîne qui identifie la boîte aux lettres associée à l’adresse. Il est unique au sein du domaine. Souvent, nom d’utilisateur du propriétaire de la boîte aux lettres ou le GUID est utilisé comme valeur pour la partie locale. 
    
  - (Requis)  *domaine* est le nom de domaine complet (FQDN) du serveur de messagerie qui héberge la boîte aux lettres identifié par la partie locale de l’adresse de messagerie. 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a>Format du : adresse si vous n’incluez pas un nom d’affichage
<a name="FormatNoDisplayName"> </a>

A correctement mis en forme à partir de : adresse qui n’inclut pas un nom d’affichage inclut uniquement une adresse de messagerie unique avec ou sans crochets pointus. Microsoft recommande que vous ne séparez pas les crochets avec des espaces. En outre, n’incluez pas rien après l’adresse de messagerie.
  
Les exemples suivants sont valides :
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

L’exemple suivant est valide mais pas recommandé car il contient des espaces entre crochets pointus et l’adresse de messagerie :
  
```
From: < sender@contoso.com >
```

L’exemple suivant n’est pas valide car il contient le texte après l’adresse de messagerie :
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a>Format du : adresse si vous incluez un nom d’affichage
<a name="FormatDisplayName"> </a>

Pour de : adresses incluant une valeur pour le nom complet, les règles suivantes s’appliquent :
  
- Si l’adresse d’expéditeur inclut un nom d’affichage et le nom complet inclut une virgule, puis le nom complet doit être placé entre guillemets. Par exemple :
    
    L’exemple suivant est valide :
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    L’exemple suivant n’est pas valide :
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    Ne pas mettre le nom complet entre guillemets si ce nom d’affichage comprend une virgule non valide en fonction de la RFC 5322.
    
    Meilleure pratique, put guillemets autour du nom complet, indépendamment de si ou pas il est une virgule dans le nom complet.
    
- Si l’adresse d’expéditeur comprend un nom d’affichage, l’adresse de messagerie doit être placé entre crochets.
    
    Meilleure pratique, Microsoft recommande vivement que vous insérez un espace entre le nom complet et l’adresse de messagerie.
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a>Exemples supplémentaires de valides et non valides à partir de : adresses
<a name="Examples"> </a>

- Valide :
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- Non valide. L’adresse de messagerie n’est pas placée entre parenthèses :
    
  ```
  From: Office 365 sender@contoso.com
  ```

- Valide, mais non recommandée. Le nom complet n’est pas entre guillemets. Meilleure pratique, placez toujours le nom complet entre guillemets :
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- Non valide. Tout est placé entre guillemets, pas seulement le nom d’affichage :
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- Non valide. Il n’existe aucune crochets autour de l’adresse de messagerie :
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- Non valide. Il n’existe aucun espace entre le nom complet et le crochet pointu gauche :
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- Non valide. Il n’existe aucun espace entre les balises quotation mark autour du nom complet et le crochet pointu gauche.
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a>Supprimer des réponses automatiques pour votre domaine personnalisé sans rompre la provenance : stratégie
<a name="SuppressAutoReply"> </a>

Avec la nouvelle à partir de : application de la stratégie, vous ne pouvez plus utiliser à partir de : \< \> pour supprimer des réponses automatiques. Au lieu de cela, vous devez configurer un enregistrement MX null pour votre domaine personnalisé.
  
Enregistrement (MX) de serveur de messagerie est un enregistrement de ressource dans DNS qui identifie le serveur de messagerie qui reçoit les messages pour votre domaine. Réponses automatiques (et toutes les réponses) sont supprimées naturellement car il n’existe aucune adresse publié auquel le serveur répond peut envoyer des messages.
  
Lorsque vous configurez un enregistrement MX null pour votre domaine personnalisé :
  
- Choisissez un domaine à partir de laquelle envoyer des messages qui n’accepte pas (recevoir) du courrier électronique. Par exemple, si votre domaine principal est contoso.com, vous pouvez choisir noreply.contoso.com.
    
- Configurer l’enregistrement MX null pour votre domaine. Un enregistrement MX null se compose d’un point unique, par exemple :
    
  ```
  noreply.contoso.com IN MX .
  ```

Pour plus d’informations sur la publication d’une valeur null MX, voir [RFC 7505](https://tools.ietf.org/html/rfc7505).
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a>Substitution de l’Office 365 à partir de : stratégie de mise en œuvre d’adresses
<a name="Override"> </a>

Une fois le déploiement de la nouvelle stratégie est terminée, vous pouvez uniquement ignorer cette stratégie pour les messages entrants que provenant de Office 365 à l’aide d’une des méthodes suivantes : 
  
- Adresses IP autorisées listes
    
- Règles de flux de messagerie Exchange Online
    
Microsoft recommande vivement par rapport à la substitution de l’application de la provenance : stratégie. Remplacement de cette stratégie peut accroître les risques de votre organisation d’exposition de courrier indésirable, les attaques par hameçonnage et les autres cybercrimes.
  
Vous ne pouvez pas remplacer cette stratégie pour les messages sortants que vous envoyez dans Office 365. En outre, Outlook.com ne permet pas les substitutions de n’importe quel type, même par le biais de prise en charge. 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a>Autres moyens de protéger et à méfaits dans Office 365
<a name="OtherProtection"> </a>

Pour plus d’informations sur comment vous pouvez renforcer votre organisation contre les cybercrimes phishing, spam, violations de données et d’autres menaces, voir [meilleures pratiques de sécurité pour Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).
  
## <a name="related-topics"></a>Voir aussi

[Messages de rétrodiffusion et EOP](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

