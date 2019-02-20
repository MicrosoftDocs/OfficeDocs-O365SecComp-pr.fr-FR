---
title: Protéger les applications avec Office 365 Cloud App Security App contrôle d'application d'accès conditionnel
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Arrêter les violations et les fuites en temps réel avec le contrôle d'application d'accès conditionnel à Office 365 Cloud App Security.
ms.openlocfilehash: 8656bf9d3e028bf6b44731c397b74d9c883db707
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103359"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a><span data-ttu-id="d3156-103">Protéger les applications avec Office 365 Cloud App Security App contrôle d'application d'accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="d3156-103">Protect apps with Office 365 Cloud App Security Conditional Access App Control</span></span>

|<span data-ttu-id="d3156-104">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="d3156-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="d3156-105">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="d3156-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="d3156-106">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="d3156-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="d3156-107">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d3156-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="d3156-108">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="d3156-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="d3156-109">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="d3156-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="d3156-110">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="d3156-110">You are here!</span></span>  <br/> [<span data-ttu-id="d3156-111">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d3156-111">Next step</span></span>](ocas-deploy-conditional-access-app-control.md) <br/> |[<span data-ttu-id="d3156-112">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="d3156-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="d3156-p101">Dans l'espace de travail d'aujourd'hui, il est souvent insuffisant de savoir ce qui se passe dans votre environnement Cloud après le fait. Vous souhaitez arrêter les violations et les fuites en temps réel, avant que les employés déposent intentionnellement ou involontairement vos données et votre organisation en péril. Il est important de permettre aux utilisateurs de votre organisation de tirer le meilleur parti des services et outils disponibles dans les applications Cloud, et de leur permettre de faire fonctionner leurs propres appareils. En même temps, vous avez besoin d'outils pour vous aider à protéger votre organisation contre les fuites de données et le vol de données en temps réel. Avec Azure Active Directory, la sécurité des applications Cloud Office 365 offre ces fonctionnalités dans une expérience holistique et intégrée avec un contrôle d'application d'accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="d3156-p101">In today’s workplace, it’s often not enough to know what’s happening in your cloud environment after the fact. You want to stop breaches and leaks in real time, before employees intentionally or inadvertently put your data and your organization at risk. It's important to enable users in your organization to make the most of the services and tools available to them in cloud apps, and let them bring their own devices to work. At the same time, you need tools to help protect your organization from data leaks, and data theft, in real time. Together with Azure Active Directory, Office 365 Cloud App Security delivers these capabilities in a holistic and integrated experience with Conditional Access App Control.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3156-118">pour utiliser le contrôle d'application d'accès conditionnel sécurité des applications cloud, vous avez besoin d'une  [licence Azure active Directory P1](https://azure.microsoft.com/pricing/details/active-directory/)et d'un abonnement [Office 365 Cloud app security](office-365-cas-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="d3156-118">To use Cloud App Security Conditional Access App Control, you need an [Azure Active Directory P1 license](https://azure.microsoft.com/pricing/details/active-directory/) and an active [Office 365 Cloud App Security](office-365-cas-overview.md) subscription.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="d3156-119">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="d3156-119">How it works</span></span>

<span data-ttu-id="d3156-p102">Le contrôle d'application d'accès conditionnel utilise une architecture de proxy inverse et est intégré de manière unique à l'accès conditionnel Azure AD. L'accès conditionnel Azure AD vous permet d'appliquer des contrôles d'accès aux applications de votre organisation en fonction de certaines conditions. Les conditions définissent l' *identité* de l'utilisateur ou du groupe d'utilisateurs, ainsi *que* les \*\* applications Cloud auxquelles une stratégie d'accès conditionnel est appliquée. Une fois que vous avez déterminé les conditions, vous pouvez acheminer les utilisateurs vers la sécurité des applications Cloud Office 365 où vous pouvez protéger les données avec le contrôle d'application d'accès conditionnel en appliquant les contrôles d'accès et de session.</span><span class="sxs-lookup"><span data-stu-id="d3156-p102">Conditional Access App Control uses a reverse proxy architecture and is uniquely integrated with Azure AD conditional access. Azure AD conditional access allows you to enforce access controls on your organization’s apps based on certain conditions. The conditions define *who* (user or group of users) and *what* (which cloud apps) and *where* (which locations and networks) a conditional access policy is applied to. After you’ve determined the conditions, you can route users to Office 365 Cloud App Security where you can protect data with Conditional Access App Control by applying access and session controls.</span></span>

<span data-ttu-id="d3156-p103">Le contrôle d'application d'accès conditionnel permet de surveiller et de contrôler en temps réel les sessions et l'accès aux applications utilisateur en fonction des stratégies d'accès et de session. Les stratégies d'accès et de session sont utilisées dans le portail de sécurité des applications Cloud pour affiner les filtres et définir les actions à effectuer sur un utilisateur. Avec les stratégies d'accès et de session, vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="d3156-p103">Conditional Access App Control enables user app access and sessions to be monitored and controlled in real time based on access and session policies. Access and session policies are used within the Cloud App Security portal to further refine filters and set actions to be taken on a user. With the access and session policies, you can:</span></span>

- <span data-ttu-id="d3156-p104">**Bloquer au téléchargement**: vous pouvez bloquer le téléchargement de documents sensibles. Par exemple, sur des appareils non gérés.</span><span class="sxs-lookup"><span data-stu-id="d3156-p104">**Block on download**: You can block the download of sensitive documents. For example, on unmanaged devices.</span></span>

- <span data-ttu-id="d3156-p105">**Protéger au téléchargement**: au lieu de bloquer le téléchargement de documents sensibles, vous pouvez exiger la protection des documents via le chiffrement au téléchargement. Ce chiffrement permet de s'assurer que le document est protégé et que l'accès des utilisateurs est authentifié si les données sont téléchargées sur un appareil non approuvé.</span><span class="sxs-lookup"><span data-stu-id="d3156-p105">**Protect on download**: Instead of blocking the download of sensitive documents, you can require documents to be protected via encryption on download. This encryption makes sure the document is protected and user access is authenticated if the data is downloaded to an untrusted device.</span></span>

- <span data-ttu-id="d3156-p106">**Surveiller les sessions utilisateur à faible niveau de fiabilité**: les utilisateurs à risque sont surveillés lorsqu'ils se connectent à des applications et que leurs actions sont consignées dans la session. Vous pouvez examiner et analyser le comportement de l'utilisateur pour comprendre où et dans quelles conditions les stratégies de session doivent être appliquées à l'avenir.</span><span class="sxs-lookup"><span data-stu-id="d3156-p106">**Monitor low-trust user sessions**: Risky users are monitored when they sign into apps and their actions are logged from within the session. You can investigate and analyze user behavior to understand where, and under what conditions, session policies should be applied in the future.</span></span>

- <span data-ttu-id="d3156-133">**Bloquer l'accès**: vous pouvez bloquer totalement l'accès à des applications spécifiques pour les utilisateurs provenant d'appareils non gérés ou de réseaux non d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="d3156-133">**Block access**: You can completely block access to specific apps for users coming from unmanaged devices or from non-corporate networks.</span></span>

- <span data-ttu-id="d3156-134">**Créer un mode lecture seule**: en surveillant et en bloquant les activités personnalisées dans l'application, vous pouvez créer un mode en lecture seule pour des applications spécifiques pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d3156-134">**Create read-only mode**: By monitoring and blocking custom in-app activities, you can create a read-only mode to specific apps for specific users.</span></span>

- <span data-ttu-id="d3156-p107">**Limiter les sessions utilisateur de réseaux non d'entreprise**: les utilisateurs qui accèdent à une application protégée à partir d'un emplacement qui ne fait pas partie de votre réseau d'entreprise bénéficient d'un accès restreint. Le téléchargement de documents sensibles est bloqué ou protégé.</span><span class="sxs-lookup"><span data-stu-id="d3156-p107">**Restrict user sessions from non-corporate networks**: Users accessing a protected app from a location that isn't part of your corporate network are allowed restricted access. The download of sensitive materials is blocked or protected.</span></span>

### <a name="how-session-control-works"></a><span data-ttu-id="d3156-137">Fonctionnement du contrôle de session</span><span class="sxs-lookup"><span data-stu-id="d3156-137">How session control works</span></span>

<span data-ttu-id="d3156-p108">La création d'une stratégie de session avec un contrôle d'application d'accès conditionnel vous permet de contrôler les sessions utilisateur en redirigeant l'utilisateur par le biais d'un proxy inverse au lieu de l'application directement. À partir de là, les demandes et les réponses des utilisateurs passent par la sécurité des applications Cloud d'Office 365 plutôt que directement par l'application.</span><span class="sxs-lookup"><span data-stu-id="d3156-p108">Creating a session policy with Conditional Access App Control enables you to control user sessions by redirecting the user through a reverse proxy instead of directly to the app. From then on, user requests and responses go through Office 365 Cloud App Security rather than directly to the app.</span></span>

<span data-ttu-id="d3156-p109">Pour conserver l'utilisateur au sein de la session, toutes les URL appropriées, tous les scripts Java et tous les cookies de la session de l'application sont remplacés par les URL de sécurité de l'application Cloud d'Office 365. Par exemple, si l'application renvoie une page avec des liens dont les domaines se terminent par myapp.com, le lien est remplacé par des domaines se terminant par une valeur semblable à la suivante: myapp.com.us.cas.ms</span><span class="sxs-lookup"><span data-stu-id="d3156-p109">To keep the user within the session, all the relevant URLs, Java scripts, and cookies within the app session are replaced with Office 365 Cloud App Security URLs. For example, if the app returns a page with links whose domains end with myapp.com, the link is replaced with domains ending with something like: myapp.com.us.cas.ms</span></span>

<span data-ttu-id="d3156-p110">Cette méthode ne nécessite aucune installation sur l'appareil. Cette méthode est idéale lors de la surveillance de sessions à partir d'appareils non gérés.</span><span class="sxs-lookup"><span data-stu-id="d3156-p110">This method doesn't require you to install anything on the device. This method is ideal when monitoring sessions from unmanaged devices.</span></span>

<span data-ttu-id="d3156-144">Une fois qu'une session est dirigée par le biais de la sécurité des applications Cloud d'Office 365, les actions suivantes peuvent être effectuées:</span><span class="sxs-lookup"><span data-stu-id="d3156-144">After a session is directed through Office 365 Cloud App Security, the following actions can be done:</span></span>

1. <span data-ttu-id="d3156-145">Inspecter le trafic pour les activités de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="d3156-145">Inspect the traffic for user activities</span></span>

2. <span data-ttu-id="d3156-146">Afficher les activités identifiées dans le journal d'activité de sécurité des applications Cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="d3156-146">Display the identified activities in the Office 365 Cloud App Security Activity log</span></span>

3. <span data-ttu-id="d3156-147">Enregistrer les journaux de trafic et les analyser</span><span class="sxs-lookup"><span data-stu-id="d3156-147">Save the traffic logs and analyze them</span></span>

4. <span data-ttu-id="d3156-148">Autoriser l'administrateur à exporter les journaux de trafic</span><span class="sxs-lookup"><span data-stu-id="d3156-148">Enable the admin to export the traffic logs</span></span>

5. <span data-ttu-id="d3156-149">Appliquer des stratégies sur la session</span><span class="sxs-lookup"><span data-stu-id="d3156-149">Enforce policies on the session</span></span>

## <a name="managed-device-identification"></a><span data-ttu-id="d3156-150">Identification des appareils gérés</span><span class="sxs-lookup"><span data-stu-id="d3156-150">Managed device identification</span></span>

<span data-ttu-id="d3156-p111">Le contrôle d'application d'accès conditionnel vous permet de créer des stratégies qui prennent en compte si un appareil est géré ou non. Pour déterminer si un périphérique est géré ou non, la fonctionnalité utilise les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="d3156-p111">Conditional Access App Control enables you to create policies that take into account whether a device is managed or not. To identify whether a device is managed or not, the feature uses:</span></span>

- <span data-ttu-id="d3156-153">Appareils conformes</span><span class="sxs-lookup"><span data-stu-id="d3156-153">Compliant devices</span></span>

- <span data-ttu-id="d3156-154">Appareils joints à un domaine</span><span class="sxs-lookup"><span data-stu-id="d3156-154">Domain-joined devices</span></span>

- <span data-ttu-id="d3156-155">Déploiement de certificats clients</span><span class="sxs-lookup"><span data-stu-id="d3156-155">Client certificates deployment</span></span>

### <a name="compliant-and-domain-joined-devices"></a><span data-ttu-id="d3156-156">Appareils conformes et joints à un domaine</span><span class="sxs-lookup"><span data-stu-id="d3156-156">Compliant and domain-joined devices</span></span>

<span data-ttu-id="d3156-p112">L'accès conditionnel Azure AD permet de transmettre directement des informations de périphériques conformes et joints à un domaine à la sécurité des applications Cloud Office 365. À partir de là, il est possible de développer une stratégie d'accès ou une stratégie de session qui utilise l'état de l'appareil en tant que filtre. Pour plus d'informations, consultez la rubrique [Présentation de la gestion des appareils dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="d3156-p112">Azure AD conditional access enables compliant and domain-joined device information to be passed directly to Office 365 Cloud App Security. From there, an access policy or a session policy can be developed that uses device state as a filter. For more information, see the [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>

### <a name="client-certificate-authenticated-devices"></a><span data-ttu-id="d3156-160">Appareils authentifiés par le certificat client</span><span class="sxs-lookup"><span data-stu-id="d3156-160">Client-certificate authenticated devices</span></span>

<span data-ttu-id="d3156-p113">Le mécanisme d'identification des périphériques peut demander l'authentification à partir d'appareils appropriés à l'aide de certificats clients. Vous pouvez utiliser des certificats clients existants déjà déployés dans votre organisation ou déployer de nouveaux certificats clients sur des appareils gérés. Vous utilisez ensuite la présence de ces certificats pour définir les stratégies d'accès et de session. Pour plus d'informations sur le déploiement des certificats clients, voir [Deploy ConditionalAttribute Access App Control for Office 365 Apps](ocas-deploy-conditional-access-app-control.md).</span><span class="sxs-lookup"><span data-stu-id="d3156-p113">The device identification mechanism can request authentication from relevant devices using client certificates. You can either use existing client certificates already deployed in your organization or roll out new client certificates to managed devices. You then use the presence of those certificates to set access and session policies. For information on how to deploy client certificates see [Deploy Conditional Access App Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).</span></span>

## <a name="supported-apps-and-clients"></a><span data-ttu-id="d3156-165">Applications et clients pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3156-165">Supported apps and clients</span></span>

<span data-ttu-id="d3156-166">Le contrôle d'application d'accès conditionnel pour Office 365 prend en charge les applications proposées suivantes:</span><span class="sxs-lookup"><span data-stu-id="d3156-166">Conditional Access App Control for Office 365 supports the following featured apps:</span></span>

- <span data-ttu-id="d3156-167">Exchange Online (aperçu)</span><span class="sxs-lookup"><span data-stu-id="d3156-167">Exchange Online (preview)</span></span>

- <span data-ttu-id="d3156-168">OneDrive entreprise (aperçu)</span><span class="sxs-lookup"><span data-stu-id="d3156-168">OneDrive for Business (preview)</span></span>

- <span data-ttu-id="d3156-169">Power BI (aperçu)</span><span class="sxs-lookup"><span data-stu-id="d3156-169">Power BI (preview)</span></span>

- <span data-ttu-id="d3156-170">SharePoint Online (aperçu)</span><span class="sxs-lookup"><span data-stu-id="d3156-170">SharePoint Online (preview)</span></span>

- <span data-ttu-id="d3156-171">Microsoft Teams (aperçu)</span><span class="sxs-lookup"><span data-stu-id="d3156-171">Microsoft Teams (preview)</span></span>

- <span data-ttu-id="d3156-172">Yammer (aperçu)</span><span class="sxs-lookup"><span data-stu-id="d3156-172">Yammer (preview)</span></span>

<span data-ttu-id="d3156-173">Les applications supplémentaires sont constamment intégrées au contrôle de session.</span><span class="sxs-lookup"><span data-stu-id="d3156-173">Additional apps are being continuously on-boarded to session control.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d3156-174">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d3156-174">Next steps</span></span>

- [<span data-ttu-id="d3156-175">Déployer le contrôle d'application d'accès conditionnel pour les applications Office 365</span><span class="sxs-lookup"><span data-stu-id="d3156-175">Deploy Conditional Access App Control for Office 365 apps</span></span>](ocas-deploy-conditional-access-app-control.md)

- [<span data-ttu-id="d3156-176">En savoir plus sur les stratégies de session dans Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d3156-176">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="d3156-177">En savoir plus sur les stratégies d'accès dans Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d3156-177">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 