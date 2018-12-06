---
title: Installer le complément Surveillance pour la version de bureau d’Outlook
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- ZOL160
ms.assetid: 6c5620e6-aba3-4910-8f3a-b55451656ff7
description: Installer le complément Office 365 surveillance pour la version de bureau d’Outlook
ms.openlocfilehash: b0cb0d78ab5f8887628528dd53b49fb15de44126
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180864"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a>Installer le complément Surveillance pour la version de bureau d’Outlook

Pour passer en revue les communications identifiées par une stratégie de surveillance, utilisez relecteurs le complément de contrôle pour Outlook et Outlook web app. Le complément est installé automatiquement dans Outlook web app pour tous les relecteurs spécifiés dans la stratégie. Cependant, réviseurs doivent exécuter certaines étapes de l’installer dans la version de bureau d’Outlook.
  
> [!NOTE]
> Utilisateurs contrôlés par des stratégies de surveillance doivent avoir une licence d’Office 365 entreprise E3 avec le module complémentaire de conformité avancée ou être inclus dans un abonnement à Office 365 entreprise E5. Si vous n’avez un plan d’entreprise E5 existant et essayer de surveillance, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Étape 1 : Copier l’adresse de la boîte aux lettres de surveillance

Pour installer le complément pour Outlook du bureau, vous devez l’adresse pour la boîte aux lettres de surveillance qui a été créé dans le cadre de la configuration de stratégie de surveillance.
  
> [!NOTE]
> Si un autre utilisateur la stratégie, vous devez obtenir cette adresse à partir de celles-ci pour installer le complément.
 
 **Pour rechercher l’adresse de boîte aux lettres de surveillance**
  
1. Se connecter à la [sécurité &amp; centre de conformité](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365.
    
2. Accédez à **la gouvernance des données** \> **surveillance**.
    
3. Cliquez sur la stratégie de surveillance qui collecte les communications que vous souhaitez examiner.
    
4. Dans la stratégie de détails flottant, sous ** boîte aux lettres de surveillance **, copiez l’adresse.<br/>![La section « Boîte aux lettres de surveillance » de volant de détails d’une stratégie de surveillance avec l’adresse de boîte aux lettres de surveillance mis en surbrillance](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Étape 2 : Configurer la boîte aux lettres de contrôle d’accès du bureau d’Outlook

Ensuite, relecteurs vous devrez exécuter deux commandes Exchange Online PowerShell afin qu’ils peuvent connecter Outlook à la boîte aux lettres de surveillance.
  
1. Connexion à Exchange Online PowerShell. [Comment faire ceci ?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)
    
2. Exécutez les commandes suivantes, où *SupervisoryReview{GUID}@domain.onmicrosoft.com* est l’adresse que vous avez copié à l’étape 1 ci-dessus et *utilisateur* est le nom du relecteur doivent se connecter à la boîte aux lettres de surveillance à l’étape 3.
    - ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```<br/>
    - ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```
    
3. Attendez au moins une heure avant de passer à l’étape 3 ci-dessous.
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Étape 3 : Créer un profil Outlook pour se connecter à la boîte aux lettres de surveillance

La dernière étape, relecteurs vous devrez créer un profil Outlook pour se connecter à la boîte aux lettres de surveillance.
 
> [!NOTE]
> Pour créer un nouveau profil Outlook, vous allez utiliser les paramètres de messagerie dans le panneau de configuration Windows. Le chemin d’accès que vous prenez pour accéder à ces paramètres peut-être dépendre d’un système d’exploitation Windows (Windows 7, Windows 8 ou Windows 10) que vous utilisez et la version d’Outlook est installée.
  
1. Ouvrez le panneau de configuration, et dans la zone de **recherche** en haut de la fenêtre, tapez **Mail**.<br/>(Ne savez pas comment atteindre le panneau de configuration ? Voir [où est le panneau de configuration ?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. Ouvrez l’application de **messagerie** .
    
3. Dans la **Configuration de la messagerie - Outlook**, cliquez sur **Afficher les profils**.<br/>![La « configuration de la messagerie - Outlook' boîte de dialogue avec le bouton Afficher les profils en surbrillance](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. Dans la **messagerie**, cliquez sur **Ajouter**. Puis, dans le **Nouveau profil**, entrez un nom pour la boîte aux lettres de surveillance (par exemple, **surveillance**).<br/>![La boîte de dialogue « Nouveau profil » l’affichage du nom « Surveillance » dans la zone Nom du profil](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. Dans **Outlook de se connecter à Office 365**, cliquez sur **se connecter à un autre compte**.<br/>![Le message « Outlook de se connecter à Office 365 » avec le lien « Se connecter à un autre compte » en surbrillance](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Dans la **Configuration de compte automatique**, sélectionnez **configuration manuelle ou types de serveurs supplémentaires**, puis cliquez sur **suivant**.
    
7. **Sélectionnez votre Type de compte**, choisissez **Office 365**. Puis, dans la zone **Adresse de messagerie** , entrez l’adresse de la boîte aux lettres de surveillance que vous avez copié précédemment.<br/>![La page « Choisir votre propre Type de compte de la boîte de dialogue Ajouter un compte dans Outlook affiche la boîte de « Adresse de messagerie » mise en surbrillance.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Lorsque vous y êtes invité, entrez vos informations d’identification d’Office 365.
    
9. Si elle réussit, vous verrez le **surveillance - \<nom de la stratégie\> ** dossier répertorié dans la vue liste des dossiers dans Outlook.