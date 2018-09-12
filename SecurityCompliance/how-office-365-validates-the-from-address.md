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
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="da2d3-103">Comment Office 365 valide l’adresse de provenance pour empêcher l’hameçonnage</span><span class="sxs-lookup"><span data-stu-id="da2d3-103">How Office 365 validates the From address to prevent phishing</span></span>

<span data-ttu-id="da2d3-p101">Office 365 et les comptes de messagerie Outlook.com recevoir un plus grand nombre d’attaques par hameçonnage. Une technique utiliser phishing consiste à envoyer des messages qui ont des valeurs pour le champ de : adresse qui ne sont pas conformes à [RFC 5322](https://tools.ietf.org/html/rfc5322). From : adresse est également appelée l’adresse 5322.From. Pour éviter ce type d’hameçonnage, Office 365 et Outlook.com exigent des messages reçus par le service pour inclure un compatibles RFC à partir de : adresse comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p101">Office 365 and Outlook.com email accounts receive an increasingly large number of phishing attacks. One technique phishers use is to send messages that have values for the From: address that are not compliant with [RFC 5322](https://tools.ietf.org/html/rfc5322). The From: address is also called the 5322.From address. To help prevent this type of phishing, Office 365 and Outlook.com require messages received by the service to include an RFC-compliant From: address as described in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="da2d3-p102">Les informations contenues dans cet article, vous devez avoir une connaissance élémentaire du format général des adresses de messagerie. Pour plus d’informations, voir [RFC 5322](https://tools.ietf.org/html/rfc5322) (notamment les sections 3.4.1 3.2.3 et 3.4), [RFC 5321](https://tools.ietf.org/html/rfc5321), ainsi que [RFC 3696](https://tools.ietf.org/html/rfc3696). Cet article est à l’application des stratégies pour l’adresse 5322.From. Cet article n’est pas sur l’adresse 5321.MailFrom.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p102">The information in this article requires you to have a basic understanding of the general format of email addresses. For more information, see [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularly sections 3.2.3, 3.4, and 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), as well as [RFC 3696](https://tools.ietf.org/html/rfc3696). This article is about policy enforcement for the 5322.From address. This article is not about the 5321.MailFrom address.</span></span> 
  
<span data-ttu-id="da2d3-p103">Malheureusement, il y a encore certains serveurs de messagerie hérités sur Internet qui continuent d’envoyer « légitimes » les messages qui ont un manquant ou mal formées à partir de : adresse. Si vous recevez régulièrement e-mail d’organisations qui utilisent ces systèmes hérités, encourager les organisations à mettre à jour leurs serveurs de messagerie pour se conformer aux normes de sécurité modernes.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p103">Unfortunately, there are still some legacy email servers on the Internet that continue to send "legitimate" email messages that have a missing or malformed From: address. If you regularly receive email from organizations that use these legacy systems, encourage those organizations to update their mail servers to comply with modern security standards.</span></span>
  
<span data-ttu-id="da2d3-114">Microsoft démarrera présentant l’application des stratégies décrites dans cet article sur le 9 novembre 2017.</span><span class="sxs-lookup"><span data-stu-id="da2d3-114">Microsoft will start rolling out enforcement of the policies described in this article on November 9, 2017.</span></span>
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a><span data-ttu-id="da2d3-115">Comment Office 365 impose l’utilisation de valide à partir de : adresse afin d’empêcher les attaques par hameçonnage</span><span class="sxs-lookup"><span data-stu-id="da2d3-115">How Office 365 enforces the use of a valid From: address to prevent phishing attacks</span></span>

<span data-ttu-id="da2d3-p104">Office 365 est apporter des modifications à la façon dont il impose l’utilisation de la provenance : adresse dans les messages qu’il reçoit afin de mieux vous protéger contre les attaques par hameçonnage. Dans cet article :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p104">Office 365 is making changes to the way it enforces the use of the From: address in messages it receives in order to better protect you from phishing attacks. In this article:</span></span>
  
- [<span data-ttu-id="da2d3-118">Tous les messages doivent inclure valide à partir de : adresse</span><span class="sxs-lookup"><span data-stu-id="da2d3-118">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="da2d3-119">Format du : adresse si vous n’incluez pas un nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="da2d3-119">Format of the From: address if you don't include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [<span data-ttu-id="da2d3-120">Format du : adresse si vous incluez un nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="da2d3-120">Format of the From: address if you include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [<span data-ttu-id="da2d3-121">Exemples supplémentaires de valides et non valides à partir de : adresses</span><span class="sxs-lookup"><span data-stu-id="da2d3-121">Additional examples of valid and invalid From: addresses</span></span>](how-office-365-validates-the-from-address.md#Examples)
    
- [<span data-ttu-id="da2d3-122">Supprimer des réponses automatiques pour votre domaine personnalisé sans rompre la provenance : stratégie</span><span class="sxs-lookup"><span data-stu-id="da2d3-122">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [<span data-ttu-id="da2d3-123">Substitution de l’Office 365 à partir de : stratégie de mise en œuvre d’adresses</span><span class="sxs-lookup"><span data-stu-id="da2d3-123">Overriding the Office 365 From: address enforcement policy</span></span>](how-office-365-validates-the-from-address.md#Override)
    
- [<span data-ttu-id="da2d3-124">Autres moyens de protéger et à méfaits dans Office 365</span><span class="sxs-lookup"><span data-stu-id="da2d3-124">Other ways to prevent and protect against cybercrimes in Office 365</span></span>](how-office-365-validates-the-from-address.md#OtherProtection)
    
<span data-ttu-id="da2d3-125">L’envoi d’un autre utilisateur n’est pas affectée par cette modification, pour plus d’informations, de lire le blog de Terry Zink «[que nous signifient lorsque nous faisons référence à l’expéditeur d’un message électronique ?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)».</span><span class="sxs-lookup"><span data-stu-id="da2d3-125">Sending on behalf of another user is not affected by this change, for more details, read Terry Zink's blog "[What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span></span>
  
### <a name="all-messages-must-include-a-valid-from-address"></a><span data-ttu-id="da2d3-126">Tous les messages doivent inclure valide à partir de : adresse</span><span class="sxs-lookup"><span data-stu-id="da2d3-126">All messages must include a valid From: address</span></span>
<span data-ttu-id="da2d3-127"><a name="MustIncludeFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-127"></span></span>

<span data-ttu-id="da2d3-p105">Certains messages automatisées n’incluent pas de : adresse lorsqu’ils sont envoyés. Dans le passé, lorsque Office 365 ou Outlook.com a reçu un message sans From : adresse, le service ajoutée par défaut à partir de : adresse au message afin de rendre le livrable :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p105">Some automated messages don't include a From: address when they are sent. In the past, when Office 365 or Outlook.com received a message without a From: address, the service added the following default From: address to the message in order to make it deliverable:</span></span>
  
```
From: <>
```

<span data-ttu-id="da2d3-p106">Démarrer le 9 novembre 2017, Office 365 seront introduites modifications apportées à ses serveurs de messagerie et de centres de données qui appliquent une nouvelle règle d’où des messages sans From : adresse sera n’est plus acceptée par Office 365 ou Outlook.com. Au lieu de cela, tous les messages reçus par Office 365 doivent déjà contenir valide à partir de : adresse. Sinon, le message sera être envoyé vers le courrier indésirable ou éléments supprimés des dossiers dans Outlook.com et Office 365.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p106">Starting November 9, 2017, Office 365 will be rolling out changes to its datacenters and mail servers which will enforce a new rule where messages without a From: address will no longer be accepted by Office 365 or Outlook.com. Instead, all messages received by Office 365 must already contain a valid From: address. Otherwise, the message will be sent to either the Junk Email or Deleted Items folders in Outlook.com and Office 365.</span></span> 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a><span data-ttu-id="da2d3-133">Vue d’ensemble de la syntaxe : format valide pour le : adresse pour Office 365</span><span class="sxs-lookup"><span data-stu-id="da2d3-133">Syntax overview: Valid format for the From: address for Office 365</span></span>
<span data-ttu-id="da2d3-134"><a name="SyntaxOverviewFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-134"></span></span>

<span data-ttu-id="da2d3-p107">Le format de la valeur de la provenance : adresse est décrite en détail dans plusieurs RFC. Il existe de nombreuses variantes de l’adressage et ce qui peut être considéré comme valide ou non valide. Pour faire simple, Microsoft recommande que vous utilisez les définitions et le format suivant :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p107">The format for the value of the From: address is defined in detail across several RFCs. There are many variations on addressing and what may be considered valid or invalid. To keep it simple, Microsoft recommends that you use the following format and definitions:</span></span>
  
```
From: "displayname " <emailaddress >
```

<span data-ttu-id="da2d3-138">Où :</span><span class="sxs-lookup"><span data-stu-id="da2d3-138">Where:</span></span>
  
- <span data-ttu-id="da2d3-p108">(Facultatif)  *DisplayName* est une expression qui décrit le propriétaire de l’adresse de messagerie. Par exemple, cela peut être un nom plus convivial pour décrire l’expéditeur que le nom de la boîte aux lettres. À l’aide d’un nom d’affichage est facultative. Toutefois, si vous choisissez d’utiliser un nom d’affichage, Microsoft recommande que vous toujours Placez entre guillemets comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p108">(Optional)  *displayname*  is a phrase that describes the owner of the email address. For example, this might be a more user-friendly name to describe the sender than the name of the mailbox. Using a display name is optional. However, if you choose to use a display name, Microsoft recommends that you always enclose it within quotation marks as shown.</span></span> 
    
- <span data-ttu-id="da2d3-143">(Requis)  *EmailAddress* est composée de :</span><span class="sxs-lookup"><span data-stu-id="da2d3-143">(Required)  *emailaddress*  is made up of:</span></span> 
    
  ```
  local-part @domain
  ```

    <span data-ttu-id="da2d3-144">Où :</span><span class="sxs-lookup"><span data-stu-id="da2d3-144">Where:</span></span>
    
  - <span data-ttu-id="da2d3-p109">(Requis)  *partie locale* est une chaîne qui identifie la boîte aux lettres associée à l’adresse. Il est unique au sein du domaine. Souvent, nom d’utilisateur du propriétaire de la boîte aux lettres ou le GUID est utilisé comme valeur pour la partie locale.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p109">(Required)  *local-part*  is a string that identifies the mailbox associated with the address. This is unique within the domain. Often, the mailbox owner's username or GUID is used as the value for the local-part.</span></span> 
    
  - <span data-ttu-id="da2d3-148">(Requis)  *domaine* est le nom de domaine complet (FQDN) du serveur de messagerie qui héberge la boîte aux lettres identifié par la partie locale de l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="da2d3-148">(Required)  *domain*  is the fully-qualified domain name (FQDN) of the mail server that hosts the mailbox identified by the local-part of the email address.</span></span> 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a><span data-ttu-id="da2d3-149">Format du : adresse si vous n’incluez pas un nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="da2d3-149">Format of the From: address if you don't include a display name</span></span>
<span data-ttu-id="da2d3-150"><a name="FormatNoDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-150"></span></span>

<span data-ttu-id="da2d3-p110">A correctement mis en forme à partir de : adresse qui n’inclut pas un nom d’affichage inclut uniquement une adresse de messagerie unique avec ou sans crochets pointus. Microsoft recommande que vous ne séparez pas les crochets avec des espaces. En outre, n’incluez pas rien après l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p110">A properly formatted From: address that does not include a display name includes only a single email address with or without angle brackets. Microsoft recommends that you do not separate the angle brackets with spaces. In addition, don't include anything after the email address.</span></span>
  
<span data-ttu-id="da2d3-154">Les exemples suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="da2d3-154">The following examples are valid:</span></span>
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

<span data-ttu-id="da2d3-155">L’exemple suivant est valide mais pas recommandé car il contient des espaces entre crochets pointus et l’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="da2d3-155">The following example is valid but not recommended because it contains spaces between the angle brackets and the email address:</span></span>
  
```
From: < sender@contoso.com >
```

<span data-ttu-id="da2d3-156">L’exemple suivant n’est pas valide car il contient le texte après l’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="da2d3-156">The following example is invalid because it contains text after the email address:</span></span>
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a><span data-ttu-id="da2d3-157">Format du : adresse si vous incluez un nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="da2d3-157">Format of the From: address if you include a display name</span></span>
<span data-ttu-id="da2d3-158"><a name="FormatDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-158"></span></span>

<span data-ttu-id="da2d3-159">Pour de : adresses incluant une valeur pour le nom complet, les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="da2d3-159">For From: addresses that include a value for the display name, the following rules apply:</span></span>
  
- <span data-ttu-id="da2d3-p111">Si l’adresse d’expéditeur inclut un nom d’affichage et le nom complet inclut une virgule, puis le nom complet doit être placé entre guillemets. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p111">If the sender address includes a display name, and the display name includes a comma, then the display name must be enclosed within quotation marks. For example:</span></span>
    
    <span data-ttu-id="da2d3-162">L’exemple suivant est valide :</span><span class="sxs-lookup"><span data-stu-id="da2d3-162">The following example is valid:</span></span>
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    <span data-ttu-id="da2d3-163">L’exemple suivant n’est pas valide :</span><span class="sxs-lookup"><span data-stu-id="da2d3-163">The following example is not valid:</span></span>
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    <span data-ttu-id="da2d3-164">Ne pas mettre le nom complet entre guillemets si ce nom d’affichage comprend une virgule non valide en fonction de la RFC 5322.</span><span class="sxs-lookup"><span data-stu-id="da2d3-164">Not enclosing the display name in quotation marks if that display name includes a comma is invalid according to RFC 5322.</span></span>
    
    <span data-ttu-id="da2d3-165">Meilleure pratique, put guillemets autour du nom complet, indépendamment de si ou pas il est une virgule dans le nom complet.</span><span class="sxs-lookup"><span data-stu-id="da2d3-165">As a best practice, put quote marks around the display name regardless of whether or not there is a comma within the display name.</span></span>
    
- <span data-ttu-id="da2d3-166">Si l’adresse d’expéditeur comprend un nom d’affichage, l’adresse de messagerie doit être placé entre crochets.</span><span class="sxs-lookup"><span data-stu-id="da2d3-166">If the sender address includes a display name, then the email address must be enclosed within angle brackets.</span></span>
    
    <span data-ttu-id="da2d3-167">Meilleure pratique, Microsoft recommande vivement que vous insérez un espace entre le nom complet et l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="da2d3-167">As a best practice, Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="da2d3-168">Exemples supplémentaires de valides et non valides à partir de : adresses</span><span class="sxs-lookup"><span data-stu-id="da2d3-168">Additional examples of valid and invalid From: addresses</span></span>
<span data-ttu-id="da2d3-169"><a name="Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-169"></span></span>

- <span data-ttu-id="da2d3-170">Valide :</span><span class="sxs-lookup"><span data-stu-id="da2d3-170">Valid:</span></span>
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- <span data-ttu-id="da2d3-p112">Non valide. L’adresse de messagerie n’est pas placée entre parenthèses :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p112">Invalid. The email address is not enclosed with angle brackets:</span></span>
    
  ```
  From: Office 365 sender@contoso.com
  ```

- <span data-ttu-id="da2d3-p113">Valide, mais non recommandée. Le nom complet n’est pas entre guillemets. Meilleure pratique, placez toujours le nom complet entre guillemets :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p113">Valid, but not recommended. The display name is not in quotes. As a best practice, always put quotation marks around the display name:</span></span>
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- <span data-ttu-id="da2d3-p114">Non valide. Tout est placé entre guillemets, pas seulement le nom d’affichage :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p114">Invalid. Everything is enclosed within quotation marks, not just the display name:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- <span data-ttu-id="da2d3-p115">Non valide. Il n’existe aucune crochets autour de l’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p115">Invalid. There are no angle brackets around the email address:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- <span data-ttu-id="da2d3-p116">Non valide. Il n’existe aucun espace entre le nom complet et le crochet pointu gauche :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p116">Invalid. There is no space between the display name and left angle bracket:</span></span>
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- <span data-ttu-id="da2d3-p117">Non valide. Il n’existe aucun espace entre les balises quotation mark autour du nom complet et le crochet pointu gauche.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p117">Invalid. There is no space between the closing quotation mark around the display name and the left angle bracket.</span></span>
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a><span data-ttu-id="da2d3-184">Supprimer des réponses automatiques pour votre domaine personnalisé sans rompre la provenance : stratégie</span><span class="sxs-lookup"><span data-stu-id="da2d3-184">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>
<span data-ttu-id="da2d3-185"><a name="SuppressAutoReply"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-185"></span></span>

<span data-ttu-id="da2d3-p118">Avec la nouvelle à partir de : application de la stratégie, vous ne pouvez plus utiliser à partir de : \< \> pour supprimer des réponses automatiques. Au lieu de cela, vous devez configurer un enregistrement MX null pour votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p118">With the new From: policy enforcement, you can no longer use From: \<\> to suppress auto-replies. Instead, you need to set up a null MX record for your custom domain.</span></span>
  
<span data-ttu-id="da2d3-p119">Enregistrement (MX) de serveur de messagerie est un enregistrement de ressource dans DNS qui identifie le serveur de messagerie qui reçoit les messages pour votre domaine. Réponses automatiques (et toutes les réponses) sont supprimées naturellement car il n’existe aucune adresse publié auquel le serveur répond peut envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p119">The mail exchanger (MX) record is a resource record in DNS that identifies the mail server that receives mail for your domain. Auto-replies (and all replies) are naturally suppressed because there is no published address to which the responding server can send messages.</span></span>
  
<span data-ttu-id="da2d3-190">Lorsque vous configurez un enregistrement MX null pour votre domaine personnalisé :</span><span class="sxs-lookup"><span data-stu-id="da2d3-190">When you set up a null MX record for your custom domain:</span></span>
  
- <span data-ttu-id="da2d3-p120">Choisissez un domaine à partir de laquelle envoyer des messages qui n’accepte pas (recevoir) du courrier électronique. Par exemple, si votre domaine principal est contoso.com, vous pouvez choisir noreply.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p120">Choose a domain from which to send messages that doesn't accept (receive) email. For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>
    
- <span data-ttu-id="da2d3-p121">Configurer l’enregistrement MX null pour votre domaine. Un enregistrement MX null se compose d’un point unique, par exemple :</span><span class="sxs-lookup"><span data-stu-id="da2d3-p121">Set up the null MX record for your domain. A null MX record consists of a single dot, for example:</span></span>
    
  ```
  noreply.contoso.com IN MX .
  ```

<span data-ttu-id="da2d3-195">Pour plus d’informations sur la publication d’une valeur null MX, voir [RFC 7505](https://tools.ietf.org/html/rfc7505).</span><span class="sxs-lookup"><span data-stu-id="da2d3-195">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a><span data-ttu-id="da2d3-196">Substitution de l’Office 365 à partir de : stratégie de mise en œuvre d’adresses</span><span class="sxs-lookup"><span data-stu-id="da2d3-196">Overriding the Office 365 From: address enforcement policy</span></span>
<span data-ttu-id="da2d3-197"><a name="Override"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-197"></span></span>

<span data-ttu-id="da2d3-198">Une fois le déploiement de la nouvelle stratégie est terminée, vous pouvez uniquement ignorer cette stratégie pour les messages entrants que provenant de Office 365 à l’aide d’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="da2d3-198">Once roll out of the new policy is complete, you can only bypass this policy for inbound mail you receive from Office 365 by using one of the following methods:</span></span> 
  
- <span data-ttu-id="da2d3-199">Adresses IP autorisées listes</span><span class="sxs-lookup"><span data-stu-id="da2d3-199">IP allow lists</span></span>
    
- <span data-ttu-id="da2d3-200">Règles de flux de messagerie Exchange Online</span><span class="sxs-lookup"><span data-stu-id="da2d3-200">Exchange Online mail flow rules</span></span>
    
<span data-ttu-id="da2d3-p122">Microsoft recommande vivement par rapport à la substitution de l’application de la provenance : stratégie. Remplacement de cette stratégie peut accroître les risques de votre organisation d’exposition de courrier indésirable, les attaques par hameçonnage et les autres cybercrimes.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p122">Microsoft strongly recommends against overriding the enforcement of the From: policy. Overriding this policy can increase your organization's risk of exposure to spam, phishing, and other cybercrimes.</span></span>
  
<span data-ttu-id="da2d3-p123">Vous ne pouvez pas remplacer cette stratégie pour les messages sortants que vous envoyez dans Office 365. En outre, Outlook.com ne permet pas les substitutions de n’importe quel type, même par le biais de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="da2d3-p123">You cannot override this policy for outbound mail you send in Office 365. In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span> 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a><span data-ttu-id="da2d3-205">Autres moyens de protéger et à méfaits dans Office 365</span><span class="sxs-lookup"><span data-stu-id="da2d3-205">Other ways to prevent and protect against cybercrimes in Office 365</span></span>
<span data-ttu-id="da2d3-206"><a name="OtherProtection"> </a></span><span class="sxs-lookup"><span data-stu-id="da2d3-206"></span></span>

<span data-ttu-id="da2d3-207">Pour plus d’informations sur comment vous pouvez renforcer votre organisation contre les cybercrimes phishing, spam, violations de données et d’autres menaces, voir [meilleures pratiques de sécurité pour Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span><span class="sxs-lookup"><span data-stu-id="da2d3-207">For more information on how you can strengthen your organization against cybercrimes like phishing, spamming, data breaches, and other threats, see [Security best practices for Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="da2d3-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da2d3-208">Related Topics</span></span>

[<span data-ttu-id="da2d3-209">Messages de rétrodiffusion et EOP</span><span class="sxs-lookup"><span data-stu-id="da2d3-209">Backscatter messages and EOP</span></span>](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

