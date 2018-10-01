---
title: Protéger les fichiers SharePoint Online avec Azure Information Protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/08/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 5b9c8e41-25d2-436d-89bb-9aecb9ec2b80
description: 'Résumé : Découvrez comment appliquer la protection Azure Information Protection pour protéger les fichiers d’un site d’équipe SharePoint Online hautement confidentiel.'
ms.openlocfilehash: 738e64784de20af46050413985fb7932000f864e
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345796"
---
# <a name="protect-sharepoint-online-files-with-azure-information-protection"></a>Protéger les fichiers SharePoint Online avec Azure Information Protection

 **Résumé :** Découvrez comment appliquer la protection Azure Information Protection pour protéger les fichiers d’un site d’équipe SharePoint Online hautement confidentiel.
  
Suivez les étapes décrites dans cet article pour configurer Azure Information Protection afin de configurer le chiffrement et les autorisations des fichiers. Ces fichiers peuvent être ajoutés à une bibliothèque SharePoint configurée pour une protection hautement confidentielle. Sinon, ouvrez un fichier directement à partir du site et utilisez le client Azure Information Protection pour ajouter le chiffrement. La protection du chiffrement et des autorisations accompagne un fichier même lorsqu’il est téléchargé à partir du site. 

Cette procédure fait partie d’une solution plus globale de configuration d’une protection hautement confidentielle pour les sites SharePoint et les fichiers contenus dans ces sites. Pour plus d’informations, reportez-vous à l’article [Sécuriser des sites et des fichiers SharePoint Online](secure-sharepoint-online-sites-and-files.md). 

L’utilisation d’Azure Information Protection pour les fichiers dans SharePoint Online n’est pas recommandée pour tous les clients, mais elle est proposée en option aux clients qui ont besoin de ce niveau de protection pour un sous-ensemble de fichiers.

Voici quelques remarques importantes concernant cette solution :
- Lorsque le chiffrement Azure Information Protection est appliqué aux fichiers stockés dans Office 365, le service ne peut pas traiter le contenu de ces fichiers. La co-création, eDiscovery, la recherche, Delve et d’autres fonctionnalités de collaboration ne fonctionnent pas. Les stratégies de protection contre la perte de données peuvent uniquement fonctionner avec les métadonnées (y compris les étiquettes Office 365), mais pas le contenu de ces fichiers (par exemple, des numéros de cartes de crédit au sein des fichiers).
- Cette solution implique qu’un utilisateur doit sélectionner une étiquette qui applique la protection à partir d’Azure Information Protection. Si vous avez besoin du chiffrement automatique et si vous souhaitez que SharePoint puisse indexer et inspecter les fichiers, pensez à utiliser les services RMS dans SharePoint Online. Lorsque vous configurez une bibliothèque SharePoint pour les services RMS, les fichiers sont chiffrés automatiquement lorsqu’ils sont téléchargés pour modification. Les services RMS SharePoint comportent des limites pouvant influencer votre décision. Pour plus d’informations, reportez-vous à l’article [Configurer la Gestion des droits relatifs à l’information (Information Rights Management, IRM) dans le Centre d’administration SharePoint](https://support.office.com/article/Set-up-Information-Rights-Management-IRM-in-SharePoint-admin-center-239CE6EB-4E81-42DB-BF86-A01362FED65C).

## <a name="admin-setup"></a>Configuration de l’administrateur
Tout d’abord, suivez les instructions contenues dans [Activer Azure RMS avec le centre d’administration Office 365](https://docs.microsoft.com/information-protection/deploy-use/activate-office365) pour votre abonnement Office 365.
  
Ensuite, configurez Azure Information Protection avec une nouvelle sous-étiquette et une nouvelle stratégie étendue pour la protection et les autorisations de votre site d’équipe SharePoint Online hautement confidentiel.
  
1. Connectez-vous au portail Office 365 avec un compte disposant du rôle Administrateur de sécurité ou Administrateur d’entreprise. Pour obtenir de l’aide, consultez la rubrique [Se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).
    
2. Dans un nouvel onglet de votre navigateur, accédez au portail Azure ([https://portal.azure.com](https://portal.azure.com)).
    
3. Si vous configurez Azure Information Protection pour la première fois, consultez ces [instructions](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time).

4. Dans le volet Liste, cliquez sur **Tous les services**, saisissez **Informations**, puis cliquez sur **Azure Information Protection**.

5. Cliquez sur **Étiquettes**.
    
6. Cliquez avec le bouton droit de la souris sur l’étiquette **Hautement confidentiel**, puis sur **Ajouter une sous-étiquette**.
    
7. Entrez le nom de la sous-étiquette dans**Nom** et sa description dans **Description**.
    
8. Dans**Définir les autorisations pour les documents et les e-mails contenant cette étiquette**, cliquez sur**Protéger**.
    
9. Dans la section **Protection**, cliquez sur**Azure (clé cloud)**.
    
10. Dans le panneau**Protection**, cliquez sur**Ajouter des autorisations** sous**Paramètres de protection**.
    
11. Dans le panneau **Ajouter des autorisations**, sous **Spécifier les utilisateurs et les groupes**, cliquez sur **+ Parcourir le répertoire**.
    
12. Dans le volet **Utilisateurs et groupes AAD**, sélectionnez le groupe d’accès Membres de votre site d’équipe SharePoint Online hautement sensible, puis cliquez sur **Sélectionner**.
    
13. sSous **Choisir les autorisations parmi les autorisations personnalisées prédéfinies ou définies**, cliquez sur **Personnalisé**, puis sur les cases à cocher **Afficher les droits**, **Modifier le contenu**, **Enregistrer**, **Répondre** et **Répondre à tous**.
    
14. Cliquez deux fois sur **OK**.
    
15. Dans le panneau **Sous-étiquette**, cliquez sur **Enregistrer**, puis sur **OK**.

16. Dans le panneau **Azure Information Protection**, cliquez sur **Stratégies > + Ajouter une nouvelle stratégie**.
    
17. Saisissez le nom de la nouvelle stratégie dans**Nom de la stratégie** et une description dans**Description**.
    
18. Cliquez sur **Sélectionnez les utilisateurs ou groupes devant recevoir cette stratégie > Utilisateur/Groupes**, puis sélectionnez le groupe d’accès des membres de votre site d’équipe SharePoint Online hautement sensible. 
    
19. Cliquez sur**Sélectionner > OK**.

20. Cliquez sur**Ajouter ou supprimer des étiquettes**. Dans le volet**Stratégie : Ajouter ou supprimer des étiquettes**, cliquez sur le nom de votre sous-étiquette puis cliquez sur**OK**.   

21. Cliquez sur**Enregistrer**, puis cliquez sur**OK**.
 
## <a name="client-setup"></a>Configuration du client
Vous pouvez maintenant commencer à créer des documents et à les protéger avec Azure Information Protection et votre nouvelle étiquette.
  
Vous devez [installer le client Azure Information Protection](https://docs.microsoft.com/information-protection/rms-client/install-client-app) sur votre périphérique ou votre ordinateur Windows. Vous pouvez créer un script et automatiser l’installation, ou les utilisateurs peuvent installer le client manuellement. Consultez les ressources suivantes :
  
- [Côté client d’Azure Information Protection](https://docs.microsoft.com/information-protection/rms-client/use-client)
    
- [Installation du client Azure Information Protection](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide)
    
- [Page de téléchargement de l’installation manuelle](https://www.microsoft.com/download/details.aspx?id=53018)
    
Une fois l’installation effectuée, vos utilisateurs exécutent une application Office (par exemple, Microsoft Word) pour se connecter avec leur compte Office 365. Une nouvelle barre **Information Protection** permet aux utilisateurs de sélectionner la nouvelle étiquette. Assurez-vous que vos utilisateurs connaissent le site d’équipe SharePoint Online et savent quelle étiquette utiliser, afin de protéger leurs fichiers hautement confidentiels.
  
> [!NOTE]
> Si vous possédez plusieurs sites d’équipe SharePoint Online hautement sensibles, vous devez créer plusieurs stratégies étendues Azure Information Protection avec des sous-étiquettes et les paramètres ci-dessus. Les autorisations de chaque sous-étiquette doivent être définies pour le groupe d’accès des membres d’un site d’équipe SharePoint Online spécifique. 
  
## <a name="adding-permissions-for-external-users"></a>Ajout d’autorisations pour les utilisateurs externes
Il existe deux façons d’accorder à des utilisateurs externes un accès à des fichiers protégés par le service Azure Information Protection. Dans les deux cas, les utilisateurs externes doivent disposer d’un compte Azure AD. Si les utilisateurs externes ne sont pas membres d’une organisation qui utilise Azure AD, ils peuvent obtenir un compte Azure AD individuel via cette page d’inscription : [https://aka.ms/aip-signup](https://aka.ms/aip-signup).

 - Ajouter des utilisateurs externes à un groupe Azure AD qui est utilisé pour configurer la protection d’une étiquette. Vous devez tout d’abord ajouter le compte en tant qu’utilisateur B2B dans votre répertoire. La [mise en cache de l’appartenance au groupe par Azure Rights Management](https://docs.microsoft.com/azure/information-protection/plan-design/prepare#group-membership-caching-by-azure-information-protection) peut prendre quelques heures.  
 - Ajouter des utilisateurs externes directement à la protection d’étiquette. Vous pouvez ajouter tous les utilisateurs d’une organisation (par exemple, Fabrikam.com), un groupe Azure AD (par exemple, un groupe financier au sein d’une organisation) ou un utilisateur individuel. Par exemple, vous pouvez ajouter une équipe externe de régulateurs à la protection d’une étiquette.

## <a name="see-also"></a>Voir aussi

[Sécuriser les fichiers et sites SharePoint Online](secure-sharepoint-online-sites-and-files.md)
  
[Sécuriser les sites SharePoint Online dans un environnement de développement/test](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[Adoption du cloud et solutions hybrides](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




