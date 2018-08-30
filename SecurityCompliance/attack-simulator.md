---
title: Attaque Simulator dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/19/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Découvrez trois différents types d’attaques informatiques que vous pouvez exécuter à l’aide d’attaque Simulator.
ms.openlocfilehash: 364144c0b2f8109c67fb262ce879414088380ebe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527837"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="5f736-103">Attaque Simulator dans Office 365</span><span class="sxs-lookup"><span data-stu-id="5f736-103">Attack Simulator in Office 365</span></span>

<span data-ttu-id="5f736-p101">Avec attaque Simulator (inclus dans [Office 365 menaces](office-365-ti.md)), si vous êtes membre de l’équipe de sécurité de votre organisation, vous pouvez exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et de rechercher des utilisateurs vulnérables avant une attaque réelle a un impact sur la ligne du bas.</span><span class="sxs-lookup"><span data-stu-id="5f736-p101">With Attack Simulator (included in [Office 365 Threat Intelligence](office-365-ti.md)), if you are a member of your organization's security team, you can run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="5f736-106">Attaque</span><span class="sxs-lookup"><span data-stu-id="5f736-106">The Attacks</span></span>

<span data-ttu-id="5f736-107">Au niveau de la version d’évaluation, nous vous proposons trois types de simulations attaque que vous pouvez exécuter :</span><span class="sxs-lookup"><span data-stu-id="5f736-107">At preview release we offer three kinds of attack simulations that you can run:</span></span>
  
- [<span data-ttu-id="5f736-108">Afficher l’attaque par hameçonnage de la sonde de nom</span><span class="sxs-lookup"><span data-stu-id="5f736-108">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="5f736-109">Attaque par mot de passe-Jet</span><span class="sxs-lookup"><span data-stu-id="5f736-109">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="5f736-110">Attaque par mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="5f736-110">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="5f736-111">Pour une attaque à lancer avec succès, le compte qui exécute l’attaque et ouvert une session doit utiliser l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="5f736-111">For an attack to be successfully launched, the account that is running the attack and logged on must use multi-factor authentication.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5f736-112">Prise en charge pour l’accès conditionnel seront prochainement disponibles.</span><span class="sxs-lookup"><span data-stu-id="5f736-112">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="5f736-113">Pour accéder aux Simulator attaque, dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="5f736-113">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="5f736-114">Avant de commencer...</span><span class="sxs-lookup"><span data-stu-id="5f736-114">Before you begin...</span></span>

<span data-ttu-id="5f736-115">Assurez-vous que vous et votre organisation satisfaire les conditions suivantes pour attaque Simulator :</span><span class="sxs-lookup"><span data-stu-id="5f736-115">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
  
- <span data-ttu-id="5f736-116">Votre organisation a des [Menaces Office 365](office-365-ti.md)avec attaque Simulator visibles dans la sécurité &amp; centre de conformité (accédez à **gestion de menace** \> **simulator attaque**)</span><span class="sxs-lookup"><span data-stu-id="5f736-116">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span>
    
- <span data-ttu-id="5f736-p102">Courrier électronique de votre organisation est hébergée dans Exchange Online. (Attaque Simulator n’est pas disponible pour les serveurs de messagerie sur site).</span><span class="sxs-lookup"><span data-stu-id="5f736-p102">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="5f736-119">Vous êtes un administrateur global d’Office 365</span><span class="sxs-lookup"><span data-stu-id="5f736-119">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="5f736-120">Votre organisation utilise [l’authentification multifacteur pour les utilisateurs d’Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span><span class="sxs-lookup"><span data-stu-id="5f736-120">Your organization is using [Multi-factor authentication for Office 365 users](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span></span>
    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="5f736-121">Afficher l’attaque par hameçonnage de la sonde de nom</span><span class="sxs-lookup"><span data-stu-id="5f736-121">Display name spear-phishing attack</span></span>

<span data-ttu-id="5f736-p103">L’hameçonnage est un terme générique pour une vaste gamme d’attaques classés comme une attaque de style d’ingénierie sociale. Cette attaque se concentre sur la tentative de phishing, une attaque ciblée plus qui est destinée à un groupe spécifique d’individus ou d’une organisation. En règle générale, une attaque personnalisée avec certains reconnaissance effectuée et à l’aide d’un nom d’affichage qui génère de confiance dans le destinataire, par exemple un message électronique qui semble provenir d’un responsable au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5f736-p103">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="5f736-p104">Cette attaque se concentre sur ce qui vous permet de manipuler les le message semble provenir d’en modifiant l’adresse de source et de nom complet. Lorsque les attaques par phishing de la sonde réussissent, cybercriminels accéder aux informations d’identification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5f736-p104">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="5f736-127">Pour simuler une attaque par hameçonnage de la sonde</span><span class="sxs-lookup"><span data-stu-id="5f736-127">To simulate a spear-phishing attack</span></span>

![Composez le corps du message électronique](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="5f736-p105">Vous pouvez concevoir l’éditeur HTML enrichi directement dans le champ **corps du message électronique** lui-même ou travailler avec la source HTML. Il existe deux champs importants pour inclusion dans le code HTML :</span><span class="sxs-lookup"><span data-stu-id="5f736-p105">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source. There are two important fields for inclusion in the HTML:</span></span> 
  
1. <span data-ttu-id="5f736-131">Dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="5f736-131">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="5f736-132">Spécifiez un nom de campagne explicite pour l’attaque ou sélectionnez un modèle.</span><span class="sxs-lookup"><span data-stu-id="5f736-132">Specify a meaningful campaign name for the attack or select a template.</span></span>
    
    ![Page de démarrage de hameçonnage](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="5f736-p106">Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="5f736-p106">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
    ![Sélectionner les destinataires](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="5f736-138">Configurez les détails de messagerie hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="5f736-138">Configure the Phishing email details.</span></span>
    
    ![Configurer les paramètres de messagerie](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    <span data-ttu-id="5f736-p107">La mise en forme HTML peut être complexe ou base en fonction des besoins votre campagne. Comme c’est HTML, vous pouvez insérer des images et du texte pour améliorer la believability. Vous pouvez contrôler à quoi ressemblera le message reçu dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="5f736-p107">The HTML formatting can be as complex or basic as your campaign needs. As it is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
1. <span data-ttu-id="5f736-p108">Entrez le texte du champ **de (nom)** . Il s’agit le champ qui indique le **Nom complet** dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="5f736-p108">Enter text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
2. <span data-ttu-id="5f736-p109">Entrez le texte ou **le champ** . Il s’agit le champ qui indique que l’adresse de messagerie de l’expéditeur dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="5f736-p109">Enter text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="5f736-p110">Vous pouvez entrer un espace de noms de messagerie existant au sein de votre organisation (Cela permettra l’adresse de messagerie résout dans le client du destinataire, emprunter un modèle de confiance très élevé), ou vous pouvez entrer une adresse de messagerie externe. L’adresse de messagerie que vous spécifiez ne doit pas réellement existe, mais il est nécessaire après le format d’une adresse SMTP valide, tel que user@domainname.extension.</span><span class="sxs-lookup"><span data-stu-id="5f736-p110">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
3. <span data-ttu-id="5f736-p111">Le sélecteur de liste déroulante, sélectionnez une URL du serveur de connexion hameçonnage qui reflète le type de contenu que vous aurez au sein de votre attaque. Vous permet de sélectionner, telles que les salaires technique, de documents de remise, etc., plusieurs URL à thème sont fournies. C’est effectivement qui cible les utilisateurs sont invités à cliquer sur l’URL.</span><span class="sxs-lookup"><span data-stu-id="5f736-p111">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
4. <span data-ttu-id="5f736-p112">Entrez une URL de page d’accueil personnalisée. L’utilisation de cette redirection des utilisateurs à une URL que vous spécifiez à la fin d’une attaque. Si vous avez des formations internes, par exemple, vous pouvez spécifier qu’ici.</span><span class="sxs-lookup"><span data-stu-id="5f736-p112">Enter a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
5. <span data-ttu-id="5f736-p113">Entrez le texte pour le champ **objet** . Il s’agit le champ qui indique que le **Nom de l’objet** dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="5f736-p113">Enter text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
5. <span data-ttu-id="5f736-156">Composez le **corps du message électronique** qui sera envoyé à la cible.</span><span class="sxs-lookup"><span data-stu-id="5f736-156">Compose the **Email body** that the target will receive.</span></span> 
  
 <span data-ttu-id="5f736-157">**${nom_utilisateur}** insère le nom de cibles dans le corps</span><span class="sxs-lookup"><span data-stu-id="5f736-157">**${username}** inserts the targets name into the Email body</span></span> 
  
 <span data-ttu-id="5f736-158">**${loginserverurl}** insère l’URL que nous voulons cibler les utilisateurs à cliquer sur</span><span class="sxs-lookup"><span data-stu-id="5f736-158">**${loginserverurl}** inserts the URL we want target users to click</span></span> 
    
6. <span data-ttu-id="5f736-p114">Cliquez sur **suivant,** puis sur **Terminer** pour lancer l’attaque. Le message électronique de phishing sonde est remis aux boîtes aux lettres des destinataires de votre cible.</span><span class="sxs-lookup"><span data-stu-id="5f736-p114">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="5f736-161">Attaque par mot de passe-Jet</span><span class="sxs-lookup"><span data-stu-id="5f736-161">Password-spray attack</span></span>

<span data-ttu-id="5f736-p115">Une attaque par jet de mot de passe par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a énuméré correctement une liste d’utilisateurs valides à partir du client, en utilisant leurs connaissances de mots de passe courants utilisés. Il est utilisé largement tel qu’il s’agit d’une attaque peu coûteuse pour exécuter et plus difficile à détecter que les attaques en force approches.</span><span class="sxs-lookup"><span data-stu-id="5f736-p115">A password spray attack against an organization is typically used after a bad actor has successfully enumerated a list of valid users from the tenant, utilizing their knowledge of common passwords used. It is utilized widely as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="5f736-164">Cette attaque se concentre sur ce qui vous permet de spécifier un mot de passe courants par rapport à une base de grande taille cible des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5f736-164">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="5f736-165">Pour simuler une attaque par mot de passe-Jet</span><span class="sxs-lookup"><span data-stu-id="5f736-165">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="5f736-166">Dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="5f736-166">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="5f736-167">Spécifiez un nom de campagne explicite de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="5f736-167">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="5f736-p116">Spécifier les destinataires cible. Il peut s’agir de personnes ou groupes de votre organisation. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="5f736-p116">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="5f736-p117">Spécifier un mot de passe à utiliser pour l’attaque. Par exemple, un mot de passe de courantes et pertinent vous pouvez essayer est `Fall2017`. Un autre peut être `Spring2018`, ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="5f736-p117">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="5f736-174">Cliquez sur **Terminer** pour lancer l’attaque.</span><span class="sxs-lookup"><span data-stu-id="5f736-174">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="5f736-175">Attaque par mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="5f736-175">Brute-force password attack</span></span>

<span data-ttu-id="5f736-p118">Une attaque par mot de passe en force brute par rapport à une organisation est généralement utilisée après qu’un acteur mauvaise a énuméré correctement une liste d’utilisateurs clés à partir du client. Cette attaque se concentre sur ce qui vous permet de spécifier un ensemble de mots de passe par rapport à un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5f736-p118">A brute-force password attack against an organization is typically used after a bad actor has successfully enumerated a list of key users from the tenant. This attack focuses on letting you specify a set of passwords against a single user.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="5f736-178">Pour simuler une attaque par mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="5f736-178">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="5f736-179">Dans la sécurité &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **simulator attaque**.</span><span class="sxs-lookup"><span data-stu-id="5f736-179">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="5f736-180">Spécifiez un nom de campagne explicite de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="5f736-180">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="5f736-p119">Spécifiez le destinataire cible. Un destinataire cible doit avoir une Exchange Online boîte aux lettres pour que l’attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="5f736-p119">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="5f736-p120">Spécifiez un ensemble de mots de passe à utiliser pour l’attaque. Par exemple, un mot de passe de courantes et pertinent vous pouvez essayer est `Fall2017`. Un autre peut être `Spring2018`, ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="5f736-p120">Specify a set of passwords to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="5f736-186">Cliquez sur **Terminer** pour lancer l’attaque.</span><span class="sxs-lookup"><span data-stu-id="5f736-186">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="related-topics"></a><span data-ttu-id="5f736-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f736-187">Related topics</span></span>

[<span data-ttu-id="5f736-188">Intelligence des menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="5f736-188">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  

