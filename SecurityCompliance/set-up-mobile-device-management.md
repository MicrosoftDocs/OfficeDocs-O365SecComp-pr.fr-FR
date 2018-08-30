---
title: Définir des Mobile Device Management (MDM) dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_OverviewMDM
- 'O365E_OverviewMDM '
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: dd892318-bc44-4eb1-af00-9db5430be3cd
description: La gestion des périphériques mobiles intégrées à Office 365 vous aident à sécuriser et gérer des appareils mobiles de vos utilisateurs comme iPhone, des tablettes, Androïd, et les téléphones Windows. Pour commencer, procédez comme suit pour activer et configurer la gestion des périphériques mobiles pour Office 365.
ms.openlocfilehash: c92290170b2937067e7407787282eaaa368b25b7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272359"
---
# <a name="set-up-mobile-device-management-mdm-in-office-365"></a>Définir des Mobile Device Management (MDM) dans Office 365

L’intégrés Mobile Device Management (MDM) pour Office 365 vous aident à sécuriser et gérer des appareils mobiles de vos utilisateurs comme iPhone, des tablettes, Androïd, et les téléphones Windows. Vous pouvez créer et gérer les stratégies de sécurité d’appareil, à distance réinitialiser un appareil et afficher les rapports détaillées des périphériques.
  
Des questions ? Nous avons créé [un forum aux questions pour aider à répondre aux questions des courants](frequently-asked-questions-about-mdm.md). Gardez à l’esprit que vous ne pouvez pas utiliser un [partenaires : offre l’administration déléguée](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) pour gérer la gestion des périphériques mobiles pour Office 365. 
  
Gestion des périphériques fait partie de la sécurité &amp; centre de conformité, il vous faudra donc à l’ouvrir pour lancer le programme d’installation de Mobile Device Manager.
  
Pour définir la gestion de l’appareil Mobile pour Office 365 vous devez :
  
1. [Activer le service de gestion des périphériques mobiles](#activate-the-mobile-device-management-service)  
2. [Configurer la gestion des périphériques mobiles](#set-up-mobile-device-management)
3. [Assurez-vous que les utilisateurs s’inscrire leurs périphériques](#step-4-recommended-manage-device-security-policies)
  
## <a name="activate-the-mobile-device-management-service"></a>Activer le service de gestion des périphériques mobiles

1. Connectez-vous à Office 365 avec votre compte professionnel ou scolaire. 
    
2. Accédez à [sécurité &amp; centre de conformité](https://protection.office.com).
    
3. Accédez à la **protection contre la perte de données** \> **Gestion des périphériques** et cliquez sur **quelques** pour lancer le processus d’activation. 
    
    ![Configurer la gestion des périphériques mobiles pour Office 365](media/368e1026-9aa5-431b-a722-8f7cf528f263.png)
  
4. Nous avons créé une stratégie de sécurité par défaut vous permet de vous aider à démarrer. Mettre à jour le nom de la stratégie de sécurité sur cette page, puis cliquez sur **Démarrer le programme d’installation**.
    
    ![Définir la stratégie de sécurité de gestion des périphériques mobiles](media/5619a2d1-f900-4268-9050-5d7eb57429a5.png)
  
5. Vous verrez l’écran du programme d’installation qui affiche la progression sur la configuration du service.
    
    ![Progression de l’installation Mobile Device Manager](media/db45d1bb-d247-4ac0-9deb-1b0c1ace9bfa.png)
  
> [!TIP]
> Vous pouvez également rechercher **Le programme d’installation de Mobile Device Manager** par le biais de recherche. Dans le centre d’administration Office 365 \> page **d’accueil** , gestion des appareils mobiles de type dans la zone de **recherche** . > ![Recherche pour la gestion des appareils mobiles dans le centre d’administration](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)
  
Elle peut prendre un certain temps pour activer la gestion des périphériques mobiles pour Office 365, mais lorsqu’il a terminé, vous recevrez un message électronique qui explique les étapes à suivre.
  
## <a name="set-up-mobile-device-management"></a>Configurer la gestion des périphériques mobiles

Lorsque le service est prêt, effectuez les quatre étapes suivantes pour terminer l’installation. Vous devrez peut-être cliquer sur [Gérer les paramètres](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) dans la page **Gestion des périphériques** dans la sécurité &amp; centre de conformité pour voir les paramètres suivants. 
  
![Configurer la gestion des appareils mobiles requis et les étapes recommandées](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
### <a name="step-1-required-configure-domains-for-mdm"></a>Étape 1 : Domaines de configuration (obligatoire) pour Mobile Device Manager

Si vous n’avez pas un domaine personnalisé associé à Office 365, ou si vous n'êtes pas la gestion des périphériques Windows, vous pouvez ignorer cette section. Dans le cas contraire, vous devez ajouter des enregistrements DNS pour le domaine à votre hôte DNS. Si vous avez ajouté les enregistrements déjà, dans le cadre de la configuration de votre domaine à Office 365, vous êtes prêt. Après avoir ajouté les enregistrements, les utilisateurs Office 365 dans votre organisation qui se connectent à leur appareil Windows avec une adresse de messagerie qui utilise votre domaine personnalisé sont redirigés pour vous inscrire dans Mobile Device Manager pour Office 365.
  
Besoin d’aide pour configurer les enregistrements ? Recherchez votre enregistrement de domaines dans la liste fournie dans [créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) et sélectionnez le nom du serveur d’inscriptions pour accéder à une aide détaillée pour la création d’enregistrements DNS. Utilisez ces instructions pour ajouter les deux enregistrements suivants : 
  
|**Nom d’hôte**|**Type d’enregistrement**|**Adresse**|**TTL**|
|:-----|:-----|:-----|:-----|
|EnterpriseEnrollment  <br/> |CNAME  <br/> |EnterpriseEnrollment.manage.microsoft.com  <br/> |3600  <br/> |
|EnterpriseRegistration  <br/> |CNAME  <br/> |EnterpriseRegistration.windows.net  <br/> |3600  <br/> |
   
Après avoir ajouté les deux enregistrements, retournez à la sécurité &amp; centre de conformité et accédez à **gestion de périphériques** \> **Gérer les paramètres** pour effectuer l’étape suivante. 
  
### <a name="step-2-required-configure-an-apns-certificate-for-ios-devices"></a>Étape 2 : (Obligatoire) configurer un certificat APNs pour les appareils iOS

Pour gérer les périphériques iOS comme iPad et l’iPhone, vous devez créer un certificat APNs.
  
Pour ce faire, suivez les étapes dans les liens **configurer** sur la **configuration de page de gestion des appareils mobiles**.
  
1. En regard de **configurer un certificat APNs pour les appareils iOS**, sélectionnez **configurer**.
    
2. Sélectionnez **télécharger votre fichier CSR** et enregistrez la demande de signature de certificat vers un quelque part sur votre ordinateur que vous allez vous souvenir. 
    
    ![Installer la boîte de dialogue certificat point](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Cliquez sur **suivant**.
    
4. Créer un certificat de point.
    
  - Sélectionnez **Apple APNS portail** pour ouvrir le portail de certificats Push Apple. 
    
    ![Installer point cert boîte de dialogue avec Apple APNS portail sélectionné](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Connectez-vous à l’aide d’un ID d’Apple.
    
    > [!IMPORTANT]
    > Utilisez une société Qu'apple ID associé à un compte de messagerie qui restera avec votre organisation, même si l’utilisateur qui gère le compte. Enregistrez ce code, car vous devez utiliser le même ID lorsqu’il est temps de renouveler le certificat. 
  
  - Sélectionnez **créer un certificat** et accepter les **Conditions d’utilisation**.
    
  - **Accédez** à la demande de signature de certificat vous avez téléchargé sur votre ordinateur à partir d’Office 365 et sélectionnez **Télécharger**.
    
  - **Télécharger** le certificat point créé par le portail de certificat Push Apple à votre ordinateur. 
    
    > [!TIP]
    > Si vous rencontrez des difficultés à télécharger le certificat, actualisez votre navigateur. 
  
5. Revenir à Office 365, puis cliquez sur **suivant** pour accéder à la page **APNS télécharger le certificat** . 
    
6. Recherchez le certificat point que vous avez téléchargé à partir du portail de certificats Push Apple.
    
    ![Cliquez sur le bouton Parcourir pour sélectionner le certificat APNS que vous avez téléchargé à partir d’Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Sélectionnez **Terminer**.
    
Après avoir ajouté le certificat point, retournez à la sécurité &amp; centre de conformité et accédez à **gestion de périphériques** \> **Gérer les paramètres** pour effectuer l’étape suivante. 
  
### <a name="step-3-recommended-set-up-multi-factor-authentication"></a>Étape 3 : (Recommandé) configurer l’authentification multifacteur

Si vous ne voyez pas l’authentification multifacteur (MFA) sous les **étapes recommandées**, vous pouvez ignorer cette section. Si cette option n’est répertoriée, il est recommandé de qu'activer MFA dans le portail Azure AD pour renforcer la sécurité de la gestion des périphériques mobiles pour le processus d’inscription d’Office 365. Il est désactivé par défaut.
  
MFA permet de sécuriser la connexion à Office 365 pour l’inscription de l’appareil mobile en exigeant un deuxième formulaire d’authentification. Les utilisateurs sont nécessaires pour confirmer un appel téléphonique, un message textuel ou une notification d’application sur leur appareil mobile après avoir entré correctement leur mot de passe du compte professionnel. Ils peuvent uniquement s’inscrire leur appareil après que ce deuxième formulaire d’authentification est terminé. Une fois que les périphériques des utilisateurs sont inscrits dans la gestion des périphériques mobiles pour Office 365, les utilisateurs peuvent accéder aux ressources de Office 365 avec seulement le compte de leur travail.
  
En regard de **configurer l’authentification multifacteur**, sélectionnez **configurer**. Pour savoir comment activer MFA dans le portail Azure AD, voir [configurer l’authentification multifacteur](https://go.microsoft.com/fwlink/p/?LinkId=519255).
  
Après avoir configuré MFA, retournez à la sécurité &amp; centre de conformité et accédez à **gestion de périphériques** \> **Gérer les paramètres** pour effectuer l’étape suivante. 
  
### <a name="step-4-recommended-manage-device-security-policies"></a>Étape 4 : Stratégies de sécurité d’appareil gérer (recommandé)

L’étape suivante consiste à créer et déployer des stratégies de sécurité de périphérique pour protéger les données de votre organisation Office 365. Par exemple, vous pouvez aider à éviter toute perte de données si un utilisateur perd leur appareil en créant une stratégie sur les périphériques de verrouillage après cinq minutes d’inactivité et périphériques effacée après 3 échecs de connexion.
  
Dans la **sécurité &amp; centre de conformité**, accédez aux **stratégies de sécurité** \> **stratégies de sécurité des périphériques** pour créer des stratégies de sécurité de périphérique et les règles d’accès. 
  
![Ajouter une stratégie de sécurité des périphériques](media/69a027f5-fbfb-482a-b850-9ccb280b8c62.png)
  
Pour obtenir des instructions étape par étape comment créer une nouvelle stratégie, voir [créer et déployer des stratégies de sécurité des périphériques](create-device-security-policies.md).
  
> [!TIP]
>  Lorsque vous créez une nouvelle stratégie, vous pouvez souhaiter définir la stratégie pour autoriser violation de stratégie d’accès et le rapport où périphérique d’un utilisateur n’est pas conforme à la stratégie. Cela vous permet de voir combien d’appareils mobiles est affecté par la stratégie sans blocage de l’accès à Office 365. > Avant de déployer une nouvelle stratégie pour tout le monde dans votre organisation, nous vous recommandons de que tester sur les appareils utilisés par un petit nombre d’utilisateurs. > En outre, avant de déployer des stratégies, permettent à votre organisation connaître l’impact potentiel d’inscrire un périphérique Mobile Device Manager pour Office 365. Selon la façon dont vous configurez les stratégies, les périphériques qui ne sont pas conformes à leur (périphériques non compatibles) peuvent être bloqués d’accéder à Office 365. Périphériques non conforme peut-être également les applications installées, des photos et autres informations personnelles, sur un appareil inscrit, risquent d’être supprimées si le périphérique est effacé. Informations supplémentaires : [Réinitialiser un appareil mobile dans Office 365](wipe-a-mobile-device.md). 
  
## <a name="make-sure-users-enroll-their-devices"></a>Assurez-vous que les utilisateurs s’inscrire leurs périphériques

Une fois que vous avez créé et déployé une stratégie de gestion des appareils mobiles, chaque utilisateur Office 365 sous licence dans votre organisation la stratégie de périphérique s’applique à recevoir un message d’inscription la prochaine fois qu’ils se connectent à Office 365 à partir de leur appareil mobile. Il doit exécuter les étapes de l’inscription et l’activation pouvoir accéder aux documents et au courrier électronique Office 365. Voir [inscrire votre appareil mobile pour le travail ou une école](enroll-your-mobile-device.md).
  
> [!IMPORTANT]
> Si la langue par défaut d’un utilisateur n’est pas pris en charge par le processus d’inscription, les utilisateurs peuvent recevoir des notifications d’inscription et étapes sur leurs appareils mobiles dans une autre langue. Pas toutes les langues prises en charge dans Office 365 sont actuellement pris en charge pour le processus d’inscription sur les appareils mobiles. 
  
Les utilisateurs avec des périphériques Android ou iOS sont nécessaires pour installer l’application de portail d’entreprise dans le cadre du processus d’inscription.
  
## <a name="related-topics"></a>Voir aussi

[Fonctionnalités de gestion des appareils mobiles](capabilities-of-mobile-device-management.md)
  
[Créer et déployer des stratégies de sécurité des appareils](create-device-security-policies.md)
  

