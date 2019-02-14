---
title: Simulateur d’attaques dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: En tant qu’administrateur global Office 365, vous pouvez utiliser attaque Simulator pour exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et de rechercher des utilisateurs vulnérables avant une attaque réelle accède à votre entreprise.
ms.openlocfilehash: 77de6af6546ae584e3bd25c0d1a59d9f26928f33
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995165"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="e543b-104">Simulateur d’attaques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="e543b-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="e543b-p102">**Résumé** Si vous êtes un administrateur global d’Office 365 et votre organisation dispose [d’Informations sur les menaces Office 365](office-365-ti.md), vous pouvez utiliser l’attaque Simulator pour exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et de rechercher des utilisateurs vulnérables avant une attaque réelle a un impact sur la ligne du bas. Lisez cet article pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="e543b-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e543b-p103">À partir de février 2019 et présentant plusieurs mois suivant, sur les menaces Office 365 est devenu Office 365 Advanced Threat Protection Plan 2, avec les fonctionnalités de protection contre les menaces supplémentaires. Pour plus d’informations, voir [plans Office 365 avancée protection contre les menaces et les prix](https://products.office.com/exchange/advance-threat-protection) et [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="e543b-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="e543b-110">Attaque</span><span class="sxs-lookup"><span data-stu-id="e543b-110">The Attacks</span></span>

<span data-ttu-id="e543b-111">Trois types de simulations attaque sont actuellement disponibles :</span><span class="sxs-lookup"><span data-stu-id="e543b-111">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="e543b-112">Afficher l’attaque par hameçonnage de la sonde de nom</span><span class="sxs-lookup"><span data-stu-id="e543b-112">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="e543b-113">Attaque par mot de passe-Jet</span><span class="sxs-lookup"><span data-stu-id="e543b-113">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="e543b-114">Attaque par mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="e543b-114">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="e543b-p104">Pour une attaque à lancer avec succès, vous utilisez l’authentification multifacteur sur le compte que vous utilisez pour exécuter des attaques simulés. En outre, vous devez être un administrateur global d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="e543b-p104">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e543b-117">Prise en charge pour l’accès conditionnel seront prochainement disponibles.</span><span class="sxs-lookup"><span data-stu-id="e543b-117">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="e543b-118">Pour accéder aux Simulator attaque, dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="e543b-118">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="e543b-119">Avant de commencer...</span><span class="sxs-lookup"><span data-stu-id="e543b-119">Before you begin...</span></span>

<span data-ttu-id="e543b-120">Assurez-vous que vous et votre organisation satisfaire les conditions suivantes pour attaque Simulator :</span><span class="sxs-lookup"><span data-stu-id="e543b-120">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="e543b-p105">Courrier électronique de votre organisation est hébergée dans Exchange Online. (Attaque Simulator n’est pas disponible pour les serveurs de messagerie sur site).</span><span class="sxs-lookup"><span data-stu-id="e543b-p105">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="e543b-123">Vous êtes un administrateur global d’Office 365</span><span class="sxs-lookup"><span data-stu-id="e543b-123">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="e543b-124">Votre organisation utilise [l’authentification multifacteur pour les utilisateurs d’Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="e543b-124">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="e543b-125">Votre organisation a des [Menaces Office 365](office-365-ti.md)avec attaque Simulator visibles dans la sécurité &amp; centre de conformité (accédez à **gestion de menace** \> **simulator attaque**)</span><span class="sxs-lookup"><span data-stu-id="e543b-125">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="e543b-126">![Gestion des menaces - Simulator attaque](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="e543b-126">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="e543b-127">Afficher l’attaque par hameçonnage de la sonde de nom</span><span class="sxs-lookup"><span data-stu-id="e543b-127">Display name spear-phishing attack</span></span>

<span data-ttu-id="e543b-p106">L’hameçonnage est un terme générique pour une vaste gamme d’attaques classés comme une attaque de style d’ingénierie sociale. Cette attaque se concentre sur la tentative de phishing, une attaque ciblée plus qui est destinée à un groupe spécifique d’individus ou d’une organisation. En règle générale, une attaque personnalisée avec certains reconnaissance effectuée et à l’aide d’un nom d’affichage qui génère de confiance dans le destinataire, par exemple un message électronique qui semble provenir d’un responsable au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e543b-p106">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="e543b-p107">Cette attaque se concentre sur ce qui vous permet de manipuler les le message semble provenir d’en modifiant l’adresse de source et de nom complet. Lorsque les attaques par phishing de la sonde réussissent, cybercriminels accéder aux informations d’identification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e543b-p107">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="e543b-133">Pour simuler une attaque par hameçonnage de la sonde</span><span class="sxs-lookup"><span data-stu-id="e543b-133">To simulate a spear-phishing attack</span></span>

![Composez le corps du message électronique](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="e543b-135">Vous pouvez concevoir l’éditeur HTML enrichi directement dans le champ **corps du message électronique** lui-même ou travailler avec la source HTML.</span><span class="sxs-lookup"><span data-stu-id="e543b-135">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="e543b-136">Dans la [sécurité &amp; centre de conformité](https://protection.office.com), cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="e543b-136">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="e543b-137">Spécifiez un nom de campagne explicite pour l’attaque ou sélectionnez un modèle.</span><span class="sxs-lookup"><span data-stu-id="e543b-137">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Page de démarrage de hameçonnage](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="e543b-p108">Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Chaque destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="e543b-p108">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Sélectionner les destinataires](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="e543b-143">Configurez les détails de messagerie hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e543b-143">Configure the Phishing email details.</span></span> <br/>![Configurer les paramètres de messagerie](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="e543b-p109">La mise en forme HTML peut être complexe ou base en fonction des besoins votre campagne. Comme c’est le format de courrier HTML, vous pouvez insérer des images et du texte pour améliorer la believability. Vous pouvez contrôler à quoi ressemblera le message reçu dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="e543b-p109">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="e543b-p110">Spécifier le texte du champ **de (nom)** . Il s’agit le champ qui indique le **Nom complet** dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="e543b-p110">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="e543b-p111">Spécifiez le texte ou **le champ** . Il s’agit le champ qui indique que l’adresse de messagerie de l’expéditeur dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="e543b-p111">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="e543b-p112">Vous pouvez entrer un espace de noms de messagerie existant au sein de votre organisation (Cela permettra l’adresse de messagerie résout dans le client du destinataire, emprunter un modèle de confiance très élevé), ou vous pouvez entrer une adresse de messagerie externe. L’adresse de messagerie que vous spécifiez ne doit pas réellement existe, mais il est nécessaire après le format d’une adresse SMTP valide, tel que user@domainname.extension.</span><span class="sxs-lookup"><span data-stu-id="e543b-p112">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="e543b-p113">Le sélecteur de liste déroulante, sélectionnez une URL du serveur de connexion hameçonnage qui reflète le type de contenu que vous aurez au sein de votre attaque. Vous permet de sélectionner, telles que les salaires technique, de documents de remise, etc., plusieurs URL à thème sont fournies. C’est effectivement qui cible les utilisateurs sont invités à cliquer sur l’URL.</span><span class="sxs-lookup"><span data-stu-id="e543b-p113">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="e543b-p114">Spécifiez une URL de page d’accueil personnalisée. L’utilisation de cette redirection des utilisateurs à une URL que vous spécifiez à la fin d’une attaque. Si vous avez des formations internes, par exemple, vous pouvez spécifier qu’ici.</span><span class="sxs-lookup"><span data-stu-id="e543b-p114">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="e543b-p115">Spécifiez le texte pour le champ **objet** . Il s’agit le champ qui indique que le **Nom de l’objet** dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="e543b-p115">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="e543b-161">Composez le **corps du message électronique** qui sera envoyé à la cible.</span><span class="sxs-lookup"><span data-stu-id="e543b-161">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="e543b-162">`${username}`Insère le nom de cibles dans le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="e543b-162">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="e543b-163">`${loginserverurl}`Insérer l’URL que nous voulons cibler les utilisateurs à cliquer sur</span><span class="sxs-lookup"><span data-stu-id="e543b-163">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="e543b-p116">Cliquez sur **suivant,** puis sur **Terminer** pour lancer l’attaque. Le message électronique de phishing sonde est remis aux boîtes aux lettres des destinataires de votre cible.</span><span class="sxs-lookup"><span data-stu-id="e543b-p116">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="e543b-166">Attaque par mot de passe-Jet</span><span class="sxs-lookup"><span data-stu-id="e543b-166">Password-spray attack</span></span>

<span data-ttu-id="e543b-p117">Une attaque par jet de mot de passe par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a acquis avec succès une liste d’utilisateurs valides à partir du client. L’acteur mauvaise connaît les mots de passe courants que les employés d’utilisation. Il s’agit d’une attaque largement utilisée, comme il s’agit d’une attaque à exécuter et plus difficiles à détecter que les attaques en force approches peu coûteuse.</span><span class="sxs-lookup"><span data-stu-id="e543b-p117">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="e543b-170">Cette attaque se concentre sur ce qui vous permet de spécifier un mot de passe courants par rapport à une base de grande taille cible des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e543b-170">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="e543b-171">Pour simuler une attaque par mot de passe-Jet</span><span class="sxs-lookup"><span data-stu-id="e543b-171">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="e543b-172">Dans la [sécurité &amp; centre de conformité](https://protection.office.com), cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="e543b-172">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="e543b-173">Spécifiez un nom de campagne explicite de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="e543b-173">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="e543b-p118">Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="e543b-p118">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="e543b-p119">Spécifier un mot de passe à utiliser pour l’attaque. Par exemple, un mot de passe de courantes et pertinent vous pouvez essayer est `Fall2017`. Un autre peut être `Spring2018`, ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="e543b-p119">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="e543b-180">Cliquez sur **Terminer** pour lancer l’attaque.</span><span class="sxs-lookup"><span data-stu-id="e543b-180">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="e543b-181">Attaque par mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="e543b-181">Brute-force password attack</span></span>

<span data-ttu-id="e543b-p120">Une attaque par mot de passe en force brute par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a acquis avec succès une liste d’utilisateurs clés à partir du client. Cette attaque se concentre sur la tentative d’un ensemble de mots de passe sur un seul compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e543b-p120">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="e543b-184">Pour simuler une attaque par mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="e543b-184">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="e543b-185">Dans la [sécurité &amp; centre de conformité](https://protection.office.com), cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="e543b-185">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="e543b-186">Spécifiez un nom de campagne explicite de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="e543b-186">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="e543b-p121">Spécifiez le destinataire cible. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="e543b-p121">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="e543b-p122">Spécifiez un ensemble de mots de passe à utiliser pour l’attaque. Pour ce faire, vous pouvez utiliser un fichier texte (.txt) pour votre liste de mots de passe. Le fichier texte ne peut pas dépasser 10 Mo dans la taille du fichier. Utilisez un mot de passe par ligne et veillez à inclure un retour chariot après le dernier mot de passe dans votre liste.</span><span class="sxs-lookup"><span data-stu-id="e543b-p122">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="e543b-193">Cliquez sur **Terminer** pour lancer l’attaque.</span><span class="sxs-lookup"><span data-stu-id="e543b-193">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="e543b-194">Nouvelles fonctionnalités d’attaque Simulator</span><span class="sxs-lookup"><span data-stu-id="e543b-194">New features in Attack Simulator</span></span>

<span data-ttu-id="e543b-p123">Nouvelles fonctionnalités sont ajoutées à une attaque Simulator. Cela inclut :</span><span class="sxs-lookup"><span data-stu-id="e543b-p123">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="e543b-p124">**Options avancées de fonctionnalités de création de rapports**. Vous serez en mesure de voir les données telles que l’heure plus rapide (ou plus lent) pour ouvrir un message électronique de simulation attaque, l’heure plus rapide (ou plus lent) à cliquer sur un lien dans le message et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="e543b-p124">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="e543b-p125">**Éditeur de modèle de courrier électronique**. Vous pouvez créer un modèle de courrier électronique personnalisés et réutilisables que vous pouvez utiliser pour les simulations attaque future.</span><span class="sxs-lookup"><span data-stu-id="e543b-p125">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="e543b-201">Visitez le site de la [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) pour voir les nouveautés dans le développement et déploiement de ce qui est déjà lancé.</span><span class="sxs-lookup"><span data-stu-id="e543b-201">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>



