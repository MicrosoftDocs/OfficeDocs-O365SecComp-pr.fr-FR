---
title: Simulateur d’attaques dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: En tant qu'administrateur général Office 365, vous pouvez utiliser un simulateur d'attaque pour exécuter des scénarios d'attaque réaliste dans votre organisation. Cela peut vous aider à identifier et à trouver des utilisateurs vulnérables avant qu'une attaque réelle ne touche votre entreprise.
ms.openlocfilehash: ba5658dfa9075b5779f8ca09ccad3547dbddcbb5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216274"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="06019-104">Simulateur d’attaques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="06019-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="06019-p102">**Résumé** Si vous êtes un administrateur général Office 365 et que votre organisation dispose d' [office 365 Threat Intelligence](office-365-ti.md), vous pouvez utiliser un simulateur d'attaque pour exécuter des scénarios d'attaque réaliste dans votre organisation. Cela peut vous aider à identifier et à trouver des utilisateurs vulnérables avant qu'une attaque réelle n'influe sur votre ligne de base. Lisez cet article pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="06019-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06019-p103">Depuis le mois de février 2019 et le déploiement sur les prochains mois, Office 365 Threat Intelligence est devenu Office 365 Advanced Threat Protection Plan 2, avec des fonctionnalités supplémentaires de protection contre les menaces. Pour en savoir plus, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="06019-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="06019-110">Les attaques</span><span class="sxs-lookup"><span data-stu-id="06019-110">The Attacks</span></span>

<span data-ttu-id="06019-111">Trois types de simulations d'attaques sont actuellement disponibles:</span><span class="sxs-lookup"><span data-stu-id="06019-111">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="06019-112">Nom d'affichage-attaque de Spear Phishing</span><span class="sxs-lookup"><span data-stu-id="06019-112">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="06019-113">Attaque par pulvérisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="06019-113">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="06019-114">Attaque de mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="06019-114">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="06019-p104">Pour qu'une attaque réussisse, vous utilisez l'authentification multifacteur sur le compte que vous utilisez pour exécuter des attaques simulées. En outre, vous devez être un administrateur général Office 365.</span><span class="sxs-lookup"><span data-stu-id="06019-p104">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="06019-117">La prise en charge de l'accès conditionnel sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="06019-117">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="06019-118">Pour accéder à un simulateur d'attaque &amp; , dans le centre de sécurité conformité, sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="06019-118">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="06019-119">Avant de commencer...</span><span class="sxs-lookup"><span data-stu-id="06019-119">Before you begin...</span></span>

<span data-ttu-id="06019-120">Assurez-vous que vous et votre organisation remplissez les conditions requises suivantes pour le simulateur d'attaque:</span><span class="sxs-lookup"><span data-stu-id="06019-120">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="06019-p105">Le courrier électronique de votre organisation est hébergé dans Exchange Online. (Le simulateur d'attaque n'est pas disponible pour les serveurs de messagerie locaux.)</span><span class="sxs-lookup"><span data-stu-id="06019-p105">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="06019-123">Vous êtes un administrateur général Office 365</span><span class="sxs-lookup"><span data-stu-id="06019-123">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="06019-124">Votre organisation utilise l' [authentification multifacteur pour les utilisateurs d'Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="06019-124">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="06019-125">votre organisation dispose de l'aide à la [décision d'Office 365](office-365-ti.md), avec un &amp; simulateur d'attaque visible dans le centre de sécurité conformité (allez sur **threat management** \> **attack simulator**)</span><span class="sxs-lookup"><span data-stu-id="06019-125">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="06019-126">![Gestion des menaces-simulateur d'attaque](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="06019-126">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="06019-127">Nom d'affichage-attaque de Spear Phishing</span><span class="sxs-lookup"><span data-stu-id="06019-127">Display name spear-phishing attack</span></span>

<span data-ttu-id="06019-p106">Le hameçonnage est un terme générique pour une suite d'attaques classées comme une attaque de style d'ingénierie sociale. Cette attaque est axée sur le Spear Phishing, une attaque plus ciblée, dirigée par un groupe spécifique de personnes ou une organisation. En règle générale, une attaque personnalisée avec une reconnaissance a été effectuée et utilise un nom complet qui générera une approbation dans le destinataire, comme un message électronique qui semble provenir d'un cadre de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="06019-p106">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="06019-p107">Cette attaque est axée sur la possibilité de manipuler le nom d'affichage et l'adresse source du message. Lorsque les attaques de Spear Phishing sont réussies, les cybercriminels peuvent accéder aux informations d'identification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="06019-p107">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="06019-133">Pour simuler une attaque par hameçonnage (Spear Phishing)</span><span class="sxs-lookup"><span data-stu-id="06019-133">To simulate a spear-phishing attack</span></span>

![Composer le corps du message électronique](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="06019-135">Vous pouvez concevoir l'éditeur HTML enrichi directement dans le champ de **corps du message** lui-même ou utiliser la source HTML.</span><span class="sxs-lookup"><span data-stu-id="06019-135">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="06019-136">Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="06019-136">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="06019-137">Spécifiez un nom de campagne significatif pour l'attaque ou sélectionnez un modèle.</span><span class="sxs-lookup"><span data-stu-id="06019-137">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Page de démarrage du hameçonnage](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="06019-p108">Spécifiez les destinataires cibles. Il peut s'agir d'individus ou de groupes au sein de votre organisation. Chaque destinataire ciblé doit disposer d'une boîte aux lettres Exchange Online pour que l'attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="06019-p108">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Sélection de destinataires](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="06019-143">ConFigurez les détails du courrier électronique de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="06019-143">Configure the Phishing email details.</span></span> <br/>![Configurer les détails du courrier électronique](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="06019-p109">La mise en forme HTML peut être aussi complexe ou basique que les besoins de votre campagne. Comme le format du message est HTML, vous pouvez insérer des images et du texte pour améliorer la convivialité. Vous avez le contrôle sur ce à quoi ressemblera le message reçu dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="06019-p109">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="06019-p110">Spécifiez le texte du champ **de (nom)** . Il s'agit du champ qui indique le **nom d'affichage** dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="06019-p110">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="06019-p111">Spécifiez le texte ou le champ **de** . Il s'agit du champ qui indique comme adresse de messagerie de l'expéditeur dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="06019-p111">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="06019-p112">Vous pouvez entrer un espace de noms de messagerie existant dans votre organisation (en procédant ainsi à la résolution de l'adresse de messagerie dans le client de réception, ce qui facilite un modèle d'approbation très élevée) ou vous pouvez entrer une adresse de messagerie externe. L'adresse de messagerie que vous spécifiez n'a pas besoin d'exister réellement, mais elle doit suivre le format d'une adresse SMTP valide, telle que User @ domainname. extension.</span><span class="sxs-lookup"><span data-stu-id="06019-p112">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="06019-p113">À l'aide du sélecteur de liste déroulante, sélectionnez une URL de serveur de connexion d'hameçonnage reflétant le type de contenu que vous aurez au sein de votre attaque. Plusieurs URL à thèmes vous sont proposées, telles que livraison de documents, technique, paie, etc. Il s'agit en fait de l'URL sur laquelle les utilisateurs ciblés sont invités à cliquer.</span><span class="sxs-lookup"><span data-stu-id="06019-p113">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="06019-p114">Spécifiez une URL de page d'accueil personnalisée. Cette opération permet de rediriger les utilisateurs vers une URL que vous spécifiez à la fin d'une attaque réussie. Si vous avez une formation interne à la sensibilisation, par exemple, vous pouvez spécifier cela ici.</span><span class="sxs-lookup"><span data-stu-id="06019-p114">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="06019-p115">Spécifiez le texte du champ **Subject** . Il s'agit du champ qui indique le **nom** de l'objet dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="06019-p115">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="06019-161">Composez le **corps du message électronique** que la cible recevra.</span><span class="sxs-lookup"><span data-stu-id="06019-161">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="06019-162">`${username}`insère le nom des cibles dans le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="06019-162">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="06019-163">`${loginserverurl}`insère l'URL sur laquelle les utilisateurs cibles doivent cliquer</span><span class="sxs-lookup"><span data-stu-id="06019-163">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="06019-p116">Choisissez **suivant,** puis **Terminer** pour lancer l'attaque. Le message électronique de Spear Phishing est remis aux boîtes aux lettres de vos destinataires cibles.</span><span class="sxs-lookup"><span data-stu-id="06019-p116">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="06019-166">Attaque par pulvérisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="06019-166">Password-spray attack</span></span>

<span data-ttu-id="06019-p117">Une attaque par pulvérisation de mot de passe contre une organisation est généralement utilisée après qu'un acteur incorrect a réussi à acquérir une liste d'utilisateurs valides du client. L'acteur incorrect connaît les mots de passe courants que les personnes utilisent. Il s'agit d'une attaque très utilisée, car il s'agit d'une attaque bon marché à exécuter et plus difficile à détecter que les approches en force.</span><span class="sxs-lookup"><span data-stu-id="06019-p117">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="06019-170">Cette attaque est axée sur la possibilité de spécifier un mot de passe commun pour un grand nombre d'utilisateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="06019-170">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="06019-171">Pour simuler une attaque par pulvérisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="06019-171">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="06019-172">Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="06019-172">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="06019-173">Spécifiez un nom de campagne significatif pour l'attaque.</span><span class="sxs-lookup"><span data-stu-id="06019-173">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="06019-p118">Spécifiez les destinataires cibles. Il peut s'agir d'individus ou de groupes au sein de votre organisation. Un destinataire ciblé doit disposer d'une boîte aux lettres Exchange Online pour que l'attaque réussisse.</span><span class="sxs-lookup"><span data-stu-id="06019-p118">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="06019-p119">Spécifiez un mot de passe à utiliser pour l'attaque. Par exemple, vous pouvez essayer un mot de passe courant et `Fall2017`pertinent. Un autre peut `Spring2018`être ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="06019-p119">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="06019-180">Cliquez sur **Terminer** pour lancer l'attaque.</span><span class="sxs-lookup"><span data-stu-id="06019-180">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="06019-181">Attaque de mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="06019-181">Brute-force password attack</span></span>

<span data-ttu-id="06019-p120">Une attaque de mot de passe en force contre une organisation est généralement utilisée après qu'un acteur incorrect a réussi à acquérir une liste d'utilisateurs clés auprès du client. Cette attaque consiste à essayer un ensemble de mots de passe sur le compte d'un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06019-p120">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="06019-184">Pour simuler une attaque de mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="06019-184">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="06019-185">Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="06019-185">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="06019-186">Spécifiez un nom de campagne significatif pour l'attaque.</span><span class="sxs-lookup"><span data-stu-id="06019-186">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="06019-p121">Spécifiez le destinataire cible. Un destinataire ciblé doit disposer d'une boîte aux lettres Exchange Online pour que l'attaque réussisse.</span><span class="sxs-lookup"><span data-stu-id="06019-p121">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="06019-p122">Spécifiez un ensemble de mots de passe à utiliser pour l'attaque. Pour ce faire, vous pouvez utiliser un fichier texte (. txt) pour votre liste de mots de passe. Le fichier texte ne peut pas dépasser 10 Mo dans la taille du fichier. Utilisez un mot de passe par ligne et assurez-vous d'inclure un retour à la ligne après le dernier mot de passe de votre liste.</span><span class="sxs-lookup"><span data-stu-id="06019-p122">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="06019-193">Cliquez sur **Terminer** pour lancer l'attaque.</span><span class="sxs-lookup"><span data-stu-id="06019-193">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="06019-194">Nouvelles fonctionnalités dans un simulateur d'attaque</span><span class="sxs-lookup"><span data-stu-id="06019-194">New features in Attack Simulator</span></span>

<span data-ttu-id="06019-p123">De nouvelles fonctionnalités sont ajoutées au simulateur d'attaques. Ces éléments sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="06019-p123">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="06019-p124">**Fonctionnalités de création de rapports avancées**. Vous pourrez voir des données telles que le temps le plus rapide (ou le plus lent) pour ouvrir un message électronique de simulation d'attaque, le temps le plus rapide (ou le plus lent) de cliquer sur un lien dans le message, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="06019-p124">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="06019-p125">**Éditeur de modèles de courrier électronique**. Vous pouvez créer un modèle de courrier électronique personnalisé réutilisable que vous pouvez utiliser pour les simulations d'attaque ultérieures.</span><span class="sxs-lookup"><span data-stu-id="06019-p125">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="06019-201">Consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) pour découvrir les éléments en cours de développement, le déploiement et les fonctionnalités déjà lancées.</span><span class="sxs-lookup"><span data-stu-id="06019-201">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>



