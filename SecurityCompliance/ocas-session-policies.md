---
title: Stratégies de session dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Les stratégies de session de sécurité d'application Cloud d'Office 365 permettent l'analyse au niveau de la session en temps réel, ce qui vous offre une visibilité granulaire sur les applications Office 365 et la possibilité d'effectuer différentes actions en fonction de la stratégie que vous avez définie pour une session utilisateur. Au lieu d'autoriser ou de bloquer entièrement l'accès, avec le contrôle de session, vous pouvez autoriser l'accès tout en surveillant la session et/ou limitez les activités de session spécifiques à l'aide des fonctionnalités de proxy inverse du contrôle d'application d'accès conditionnel.
ms.openlocfilehash: e0e4b04ee8cc0f7a14adbc26b074a5f2947e44c2
ms.sourcegitcommit: 866d8cab6bcfdd124516a8369e47ec797bc7cf8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2019
ms.locfileid: "30312091"
---
# <a name="session-policies-in-office-365-cloud-app-security"></a>Stratégies de session dans la sécurité des applications cloud Office 365

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étape suivante](ocas-access-policies.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |

Les stratégies de session de sécurité d'application Cloud d'Office 365 permettent l'analyse au niveau de la session en temps réel, ce qui vous offre une visibilité granulaire sur les applications Office 365 et la possibilité d'effectuer différentes actions en fonction de la stratégie que vous avez définie pour une session utilisateur. Au lieu d'autoriser ou de bloquer entièrement l'accès, avec le contrôle de session, vous pouvez autoriser l'accès tout en surveillant la session et/ou limitez les activités de session spécifiques à l'aide des fonctionnalités de proxy inverse du contrôle d'application d'accès conditionnel.

Par exemple, vous pouvez décider d'utiliser des appareils non gérés ou des sessions provenant d'emplacements spécifiques, afin de permettre à l'utilisateur d'accéder à l'application, mais aussi de limiter le téléchargement de fichiers sensibles ou de protéger certains documents lors du téléchargement. Les stratégies de session vous permettent de définir ces contrôles de session utilisateur et d'autoriser l'accès et vous permettent d'effectuer les opérations suivantes:

- [Surveiller toutes les activités](#monitor-all-activities)

- [Bloquer tous les téléchargements](#block-all-downloads)

- [Bloquer des activités spécifiques](#block-specific-activities)

- [Protéger les fichiers au téléchargement](#protect-files-on-download)

## <a name="prerequisites-to-using-session-policies"></a>Conditions préalables à l'utilisation des stratégies de session

- Licence Azure AD Premium P1

- Les applications Office 365 pertinentes doivent être [déployées avec le contrôle d'application d'accès conditionnel](ocas-deploy-conditional-access-app-control.md)

-  une [stratégie d'accès conditionnel Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)doit être mise en place pour rediriger les utilisateurs vers Office 365 Cloud App Security

## <a name="create-an-azure-ad-conditional-access-policy"></a>Créer une stratégie d'accès conditionnel Azure AD

Les stratégies d'accès conditionnel Azure Active Directory et les stratégies de session de sécurité des applications Cloud fonctionnent en tandem pour examiner chaque session utilisateur et prendre des décisions de stratégie pour chaque application. Pour configurer une stratégie d'accès conditionnel dans Azure AD, procédez comme suit:

1. Configurez une  [stratégie d'accès conditionnel Azure ad](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)avec des affectations pour un utilisateur ou un groupe d'utilisateurs et l'application que vous souhaitez contrôler avec le contrôle d'application d'accès conditionnel. Remarque: seules les applications qui ont été déployées  [avec le contrôle d'application d'accès conditionnel](ocas-deploy-conditional-access-app-control.md)seront affectées par cette stratégie.

2. dirigez les utilisateurs vers la sécurité des applications Cloud Office 365 en sélectionnant l'option **utiliser un contrôle d'application d'accès conditionnel appliqué aux restrictions** de la page de la **Session** .

## <a name="create-a-cloud-app-security-session-policy"></a>Créer une stratégie de session de sécurité d'application Cloud

Pour créer une stratégie de session, procédez comme suit:

1. Dans le portail, sélectionnez **contrôle** suivi de **stratégies**.

2. Dans la page **stratégies** , cliquez sur **créer une stratégie** et sélectionnez **stratégie de session**.

3. Dans la fenêtre **stratégie** de session, attribuez un nom à votre stratégie.

4. Dans le champ **type** de contrôle de session:
    
    - Sélectionnez **moniteur uniquement** si vous souhaitez uniquement surveiller les activités par les utilisateurs. Cette option permet de créer une stratégie d'analyse uniquement pour les applications sélectionnées où tous les abonnements, les téléchargements heuristiques et les types d'activité seront téléchargés.
    
    - Sélectionnez **contrôler le téléchargement de fichiers (avec DLP)** si vous souhaitez surveiller les activités de l'utilisateur. Vous pouvez effectuer des actions supplémentaires comme bloquer ou protéger les téléchargements pour les utilisateurs.
    
    - Sélectionnez **bloquer les activités** pour bloquer des activités spécifiques, que vous pouvez sélectionner à l'aide du filtre de **type** d'activité. Toutes les activités des applications sélectionnées seront surveillées (et signalées dans le journal d'activité). Les activités spécifiques que vous sélectionnez sont bloquées si vous sélectionnez l'action **bloquer** . Les activités spécifiques que vous avez sélectionnées déclencheront des alertes si vous sélectionnez l'action de **test** et que des alertes sont activées.

5. Sous **activité source** dans la section **activités correspondant à tous les éléments suivants** , sélectionnez des filtres d'activité supplémentaires à appliquer à la stratégie. Ces filtres peuvent inclure les options suivantes:
    
    - **Balises de périphérique**: utilisez ce filtre pour identifier les appareils non gérés.
    
    - **Emplacement**: utilisez ce filtre pour identifier les emplacements inconnus (et par conséquent).
    
    - **Adresse IP**: utilisez ce filtre pour filtrer par adresse IP ou utiliser les balises d'adresses IP précédemment attribuées.
    
    - **Balise de l'agent utilisateur**: utilisez ce filtre pour activer l'heuristique afin d'identifier les applications mobiles et de bureau. Ce filtre peut être défini sur égal ou différent de **client natif**. Ce filtre doit être testé par rapport à vos applications mobiles et de bureau pour chaque application Cloud.<br>Remarque: les stratégies de session ne prennent pas en charge les applications mobiles et de bureau. Les applications mobiles et les applications de bureau peuvent également être bloquées ou autorisées en créant une stratégie d'accès.

6. Si vous avez sélectionné l'option permettant de **contrôler le téléchargement de fichiers (avec DLP)**, sous **source** de l'activité dans la section **fichiers correspondant à tous les éléments suivants** , sélectionnez des filtres de fichiers supplémentaires à appliquer à la stratégie. Ces filtres peuvent inclure les options suivantes:
        
    - **Étiquette de classification** : utilisez ce filtre si votre organisation utilise Azure information protection et que vos données sont protégées par les étiquettes de classification. Vous pouvez filtrer les fichiers en fonction de l'étiquette de classification que vous lui avez appliquée. Pour plus d'informations sur l'intégration avec Azure information protection, voir [Azure information protection Integration](https://docs.microsoft.com/cloud-app-security/azip-integration).
        
    - **Nom de fichier** : utilisez ce filtre pour appliquer la stratégie à des fichiers spécifiques.
        
    - **Type de fichier** : utilisez ce filtre pour appliquer la stratégie à des types de fichiers spécifiques, par exemple, bloquer le téléchargement pour tous les fichiers. xls.
    
    - Dans la section **inspection** du contenu, indiquez si vous souhaitez autoriser le moteur DLP à analyser les documents et le contenu des fichiers.
    
    - Sous **actions**, sélectionnez l'un des éléments suivants:
        
        - **Test (surveiller toutes les activités)**: définissez cette action pour autoriser le téléchargement explicitement en fonction des filtres de stratégie que vous définissez.
        
        - **Bloquer (bloquer le téléchargement de fichiers et surveiller toutes les activités)**: définissez cette action de manière à bloquer explicitement le téléchargement en fonction des filtres de stratégie que vous avez définis. Pour plus d'informations, consultez [la rubrique How Block Download Works](https://docs.microsoft.com/en-us/cloud-app-security/session-policy-aad#block-download).
        
        - **Protect (appliquer une étiquette de classification pour télécharger et surveiller toutes les activités)**: cette option n'est disponible que si vous avez sélectionné l'option **Télécharger le téléchargement de fichiers (avec DLP)** sous **stratégie de session**. Si votre organisation utilise Azure information protection, vous pouvez définir une **action** pour appliquer un ensemble d'étiquettes de classification dans Azure information protection au fichier. Pour plus d'informations, voir [How Protect Protect Works](https://docs.microsoft.com/en-us/cloud-app-security/session-policy-aad#protect-download).

7. Vous pouvez **créer une alerte pour chaque événement correspondant à l'aide de la gravité de la stratégie**et définir une limite d'alerte. Indiquez si vous souhaitez que l'alerte s'affiche sous la forme d'un e-mail, d'un message texte ou des deux.

## <a name="monitor-all-activities"></a>Surveiller toutes les activités

Lorsque vous créez une stratégie de session, chaque session utilisateur correspondant à la stratégie est redirigée vers le contrôle de session et non vers l'application directement. L'utilisateur verra un avis de surveillance pour l'informer que ses sessions sont surveillées.

Si vous ne souhaitez pas informer l'utilisateur qu'il est surveillé, vous pouvez désactiver le message de notification.

1. Sous le COG paramètres, sélectionnez **paramètres généraux**.

2. Ensuite, sous **contrôle** d'accès conditionnel, sélectionnez **surveillance** de l'utilisateur et désélectionnez la case **avertir les utilisateurs** .

Pour conserver l'utilisateur au sein de la session, le contrôle d'application d'accès conditionnel remplace toutes les URL, tous les scripts Java et tous les cookies pertinents dans la session de l'application par les URL de sécurité de l'application Cloud d'Office 365. Par exemple, si l'application renvoie une page avec des liens dont les domaines `myapp.com`se terminent par, le contrôle d'application d'accès conditionnel remplace les `myapp.com.us.cas.ms`liens dont les domaines se terminent par des éléments tels que. De cette façon, l'ensemble de la session est surveillé par la sécurité des applications Cloud d'Office 365.

Contrôle des applications d'accès conditionnel enregistre les journaux de trafic de toutes les sessions utilisateur qui sont acheminées via ce dernier. Les journaux de trafic incluent le temps, l'adresse IP, l'agent utilisateur, les URL visitées et le nombre d'octets téléchargés et téléchargés. Ces journaux sont analysés et un rapport continu, le contrôle de l' **application d'accès conditionnel à la sécurité des applications Cloud**, est ajouté à la liste des rapports de découverte dans le Cloud dans le tableau de bord de découverte du Cloud.

### <a name="to-export-these-logs"></a>Pour exporter ces journaux:

1. Accédez au COG paramètres, puis cliquez sur **contrôle d'application d'accès conditionnel**.

2. Sur le côté droit du tableau, cliquez sur le bouton Exporter.<br>![bouton Exporter](media/image3.png)<br>

3. Sélectionnez la plage du rapport, puis cliquez sur **Exporter**. Ce processus peut prendre un certain temps.

### <a name="to-download-the-exported-log"></a>Pour télécharger le journal exporté:

1. Une fois que le rapport est prêt, accédez à **paramètres** , puis à **rapports**exportés.

2. Dans le tableau, sélectionnez le rapport approprié dans la liste des **journaux** de contrôle d'application d'accès conditionnel, puis cliquez sur Télécharger.<br>![bouton Télécharger](media/image4.png)<br>

## <a name="block-all-downloads"></a>Bloquer tous les téléchargements

Lorsque le paramètre **Block** est défini en tant qu' **action** que vous souhaitez effectuer dans la stratégie de session de sécurité des applications Cloud, le contrôle d'application d'accès conditionnel empêche un utilisateur de télécharger un fichier par filtre de fichier de la stratégie. Un événement de téléchargement est reconnu par la sécurité des applications Cloud Office 365 pour chaque application lorsqu'un utilisateur commence un téléchargement. Le contrôle d'application d'accès conditionnel intervient en temps réel pour l'empêcher de s'exécuter. Lorsque le signal reçu indique qu'un utilisateur a initié un téléchargement, le contrôle d'application d'accès conditionnel renvoie un message de **Téléchargement restreint** à l'utilisateur et remplace le fichier téléchargé par un fichier texte. Le message du fichier texte destiné à l'utilisateur peut être configuré et personnalisé à partir de la stratégie de session.

## <a name="block-specific-activities"></a>Bloquer des activités spécifiques

Lorsque l'option **bloquer les activités** est définie en tant que **type d'activité**, vous pouvez sélectionner des activités spécifiques à bloquer dans des applications spécifiques. Toutes les activités des applications sélectionnées seront surveillées et signalées dans le journal d'activité. Les activités spécifiques que vous sélectionnez sont bloquées si vous sélectionnez l'action **bloquer** . Les activités spécifiques que vous avez sélectionnées déclencheront des alertes si vous sélectionnez l'action de **test** et que des alertes sont activées.

**Bloquer des activités** spécifiques et les appliquer à des groupes spécifiques pour créer un mode complet en lecture seule pour votre organisation.

## <a name="protect-files-on-download"></a>Protéger les fichiers au téléchargement

Sélectionnez **bloquer les activités** pour bloquer des activités spécifiques, que vous pouvez rechercher à l'aide du filtre de **type** d'activité. Toutes les activités des applications sélectionnées seront surveillées (et signalées dans le journal d'activité). Les activités spécifiques que vous sélectionnez sont bloquées si vous sélectionnez l'action **bloquer** . Les activités spécifiques que vous avez sélectionnées déclencheront des alertes si vous sélectionnez l'action de **test** et que des alertes sont activées.

Lorsque la **protection** est définie comme l' **action** à effectuer dans la stratégie de session de sécurité des applications Cloud, le contrôle d'application d'accès conditionnel applique l'étiquetage et la protection ultérieure d'un fichier par les filtres de fichiers de la stratégie. Les étiquettes sont configurées dans la console Azure information protection et la **protection** doit être sélectionnée dans l'étiquette pour qu'elle apparaisse en tant qu'option dans la stratégie de sécurité de l'application Cloud. Lorsqu'une étiquette est sélectionnée et qu'un fichier est téléchargé qui répond aux critères de la stratégie de sécurité de l'application Cloud, l'étiquette et la protection correspondante (avec autorisations) sont appliquées au fichier lors du téléchargement. Le fichier d'origine reste tel quel dans l'application Cloud tandis que le fichier téléchargé est maintenant protégé. Les utilisateurs qui essaient d'accéder au fichier doivent respecter les autorisations requises déterminées par la protection appliquée.

## <a name="next-steps"></a>Étapes suivantes

- [En savoir plus sur les stratégies d'accès dans Office 365 Cloud App Security](ocas-access-policies.md)

- [Blocage des téléchargements sur les appareils non gérés à l'aide des fonctionnalités de contrôle d'application d'accès conditionnel Azure AD](https://docs.microsoft.com/en-us/cloud-app-security/use-case-proxy-block-session-aad)

