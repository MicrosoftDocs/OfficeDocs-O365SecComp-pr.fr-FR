---
title: Configuration d’un connecteur pour l’archivage des données Bloomberg instantanées dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Les administrateurs peuvent configurer un connecteur natif pour importer des données à partir de l’outil de conversation Bloomberg dans Office 365. Cela vous permet d’archiver des données provenant de sources de données tierces dans Office 365 de sorte que vous puissiez utiliser les fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer les données tierces de votre organisation.
ms.openlocfilehash: eda68a0fdc887a2042a78683eaef0693264d0684
ms.sourcegitcommit: a550519ca8f2a54712bf0a43be7f954e55675dac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35902466"
---
# <a name="set-up-a-connector-to-archive-instant-bloomberg-data-in-office-365"></a>Configuration d’un connecteur pour l’archivage des données Bloomberg instantanées dans Office 365

Utilisez un connecteur natif dans le centre de sécurité & conformité dans Office 365 pour importer et archiver les données de conversation des services financiers à partir de l’outil de collaboration [instant Bloomberg](https://www.bloomberg.com/professional/product/collaboration/) . Une fois que vous avez configuré et configuré un connecteur, il se connecte au site FTP Secure (SFTP) de votre organisation une fois par jour, convertit le contenu des messages de conversation en format de message électronique, puis importe ces éléments dans des boîtes aux lettres dans Office 365.

Une fois les données instantanées Bloomberg stockées dans les boîtes aux lettres des utilisateurs, vous pouvez appliquer les fonctionnalités de conformité d’Office 365 telles que la conservation pour litige, la recherche de contenu, l’archivage inaltérable, l’audit et les stratégies de rétention d’Office 365 aux données instantanées Bloomberg. Par exemple, vous pouvez rechercher des messages de conversation instant Bloomberg à l’aide de la recherche de contenu ou associer la boîte aux lettres qui contient les données Bloomberg instantanée à un dépositaire dans un cas avancé de découverte électronique. L’utilisation d’un connecteur Bloomberg instantané pour importer et archiver des données dans Office 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.

## <a name="overview-of-archiving-instant-bloomberg-data"></a>Vue d’ensemble de l’archivage des données de la fonctionnalité Bloomberg instantanée

La vue d’ensemble suivante décrit le processus d’utilisation d’un connecteur pour archiver des données de conversation de messagerie instantanée Bloomberg dans Office 365. 

![Processus d’importation et d’archivage de Bloomberg instantané](media/InstantBloombergDataArchiving.png)

1. Votre organisation travaille avec Bloomberg pour configurer un site Bloomberg SFTP. Vous allez également utiliser Bloomberg pour configurer la copie instantanée de messages de conversation sur votre site Bloomberg SFTP.

2. Une fois toutes les 24 heures, les messages de conversation provenant d’instant Bloomberg sont copiés sur le site Bloomberg SFTP.
    
3. Le connecteur Bloomberg instantané que vous créez dans le centre de sécurité & conformité se connecte au site de Bloomberg SFTP tous les jours et transfère les messages de conversation des dernières 24 heures vers une zone de stockage Azure sécurisée dans le Cloud Microsoft. Le connecteur convertit également le contenu d’un massage de conversation au format d’un message électronique.
    
4. Le connecteur importe les éléments de message de conversation vers la boîte aux lettres d’un utilisateur spécifique ou vers une autre boîte aux lettres. Le connecteur utilise la valeur de la propriété *CorporateEmailAddress* . Chaque message de conversation contient cette propriété, qui est renseignée avec l’adresse de messagerie de chaque participant du message de conversation. L’impossibilité d’importer un élément dans une boîte aux lettres utilisateur spécifique ou dans une autre boîte aux lettres est basée sur les critères suivants:
    
    a. **Éléments ayant une valeur dans la propriété CorporateEmailAddress qui correspond à un compte d’utilisateur Office 365:** Si le connecteur peut associer l’adresse de messagerie de la propriété *CorporateEmailAddress* à un compte d’utilisateur spécifique dans Office 365, l’élément est copié dans le dossier boîte de réception de la boîte aux lettres Office 365 de l’utilisateur.
    
    b. **Éléments dont la propriété CorporateEmailAddress ne correspond pas à un compte d’utilisateur Office 365:** Si le connecteur ne peut pas associer une adresse de messagerie de la propriété *CorporateEmailAddress* à un compte d’utilisateur spécifique dans Office 365, l’élément est copié dans le dossier boîte de réception d’une boîte aux lettres «fourre-tout» alternative dans Office 365.

## <a name="before-you-begin"></a>Avant de commencer

La plupart des étapes d’implémentation nécessaires à l’archivage des données de la demande instantanée sont externes à Office 365 et doivent être effectuées pour pouvoir créer le connecteur dans le centre de sécurité & conformité.

- Votre organisation doit consentir à autoriser le service d’importation Office 365 à accéder aux données de boîte aux lettres dans votre organisation. Pour accepter cette demande, accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), connectez-vous à l’aide des informations d’identification d’un administrateur général Office 365, puis acceptez la demande. Vous devez effectuer cette étape avant de pouvoir créer le connecteur Bloomberg instantané à l’étape 3.

- S’abonner à [Bloomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA). Cette opération est nécessaire afin que vous puissiez vous connecter à Bloomberg Anywhere pour accéder au site Bloomberg SFTP que vous devez configurer et configurer.

- Configurez un site Bloomberg SFTP (Secure File Transfer Protocol). Après avoir travaillé avec Bloomberg pour configurer le site SFTP, les données de instant Bloomberg sont téléchargées sur le site SFTP tous les jours. Le connecteur que vous créez à l’étape 2 se connecte à ce site SFTP et transfère les données de conversation vers les boîtes aux lettres Office 365. SFTP chiffre également les données de conversation de la messagerie instantanée Bloomberg envoyées aux boîtes aux lettres Office 365 lors du processus de transfert.

    Pour plus d’informations sur Bloomberg SFTP (également appelé *BB-SFTP*):

    - Consultez le document «standards de connectivité SFTP» sur le [support Bloomberg](https://www.bloomberg.com/professional/support/documentation/).
    
    - Contacter le [support client Bloomberg](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc).

    Une fois que vous avez travaillé avec Bloomberg pour configurer un site SFTP, Bloomberg vous fournira des informations après avoir répondu au message d’implémentation Bloomberg. Enregistrez une copie des informations suivantes. Vous l’utilisez pour configurer un connecteur à l’étape 3.

    - Le code de confirmation, qui est un ID pour votre organisation et est utilisé pour se connecter au site Bloomberg SFTP.

    - Mot de passe pour votre site Bloomberg SFTP

    - URL du site de Bloomberg SFTP (par exemple, sftp.bloomberg.com)

    - Numéro de port pour le site Bloomberg SFTP

- L’utilisateur qui crée un connecteur Bloomberg instantané à l’étape 3 (et qui télécharge les clés publiques et l’adresse IP à l’étape 1) doit se voir attribuer le rôle d’exportation d’importation de boîte aux lettres dans Exchange Online. Cela est nécessaire pour accéder à la page **données** tierces d’archivage dans le centre de sécurité & conformité. Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle exportation d’importation de boîte aux lettres au groupe de rôles gestion de l’organisation dans Exchange Online. Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d’exportation d’importation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres. Pour plus d’informations, reportez-vous aux sections [créer des groupes de rôles](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou modifier des [groupes](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) de rôles dans l’article «gérer des groupes de rôles dans Exchange Online».

## <a name="step-1-obtain-ssh-and-pgp-public-keys"></a>Étape 1: obtenir des clés publiques SSH et PGP

La première étape consiste à obtenir une copie des clés publiques pour le protocole SSH (Secure Shell) et PGP (Pretty bonne confidentialité). Utilisez ces clés à l’étape 2 pour configurer le site Bloomberg SFTP de sorte que le connecteur (que vous créez à l’étape 3) se connecte au site SFTP et transfère les données de conversation instant Bloomberg vers les boîtes aux lettres Office 365. Vous pouvez également obtenir une adresse IP dans cette étape, que vous utiliserez lors de la configuration du site Bloomberg SFTP.

1. Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données** , puis cliquez sur **archiver les données**tierces.

2. Sur la page **données** tierces d’archivage, cliquez sur **Ajouter un connecteur**, puis cliquez sur **Bloomberg instantané**.

3. Sur la page **conditions de service** , cliquez sur **accepter**.

4. Sur le **site ajouter des informations d’identification pour Bloomberg SFTP** sous étape 1, cliquez sur les liens **Télécharger la clé SSH**, **Télécharger la clé PGP**et **Télécharger l’adresse IP** pour enregistrer une copie de chaque fichier sur votre ordinateur local. Ces fichiers contiennent les éléments suivants qui sont utilisés pour configurer le site de Bloomberg SFTP à l’étape 2:

   - Clé publique SSH: cette clé permet de configurer le protocole SSH (Secure Shell) pour activer une connexion à distance sécurisée lorsque le connecteur se connecte au site Bloomberg SFTP.

   - Clé publique PGP: cette clé permet de configurer le chiffrement des données transférées à partir du site Bloomberg SFTP vers Office 365.

   - Adresse IP: le site d’Bloomberg SFTP est configuré pour accepter une demande de connexion uniquement à partir de cette adresse IP, utilisée par le connecteur Bloomberg instantané que vous créez à l’étape 3. 

5. Cliquez sur **Annuler** pour fermer l’Assistant. Vous revenez à cet Assistant à l’étape 3 pour créer le connecteur.

## <a name="step-2-configure-the-bloomberg-sftp-site"></a>Étape 2: configurer le site Bloomberg SFTP

L’étape suivante consiste à utiliser les clés publiques SSH et PGP, ainsi que l’adresse IP que vous avez obtenue à l’étape 1, pour configurer l’authentification SSH et le chiffrement PGP pour le site Bloomberg SFTP. Cela permet au connecteur Bloomberg instantané que vous créez à l’étape 3 de se connecter au site Bloomberg SFTP et de transférer les données de la fonctionnalité Bloomberg vers Office 365. Vous devez utiliser le support client Bloomberg pour configurer votre site Bloomberg SFTP. Contactez le support technique de [client Bloomberg](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) pour obtenir de l’aide. 

> [!IMPORTANT]
> Bloomberg recommande de joindre les trois fichiers que vous avez téléchargés à l’étape 1 à un message électronique et de les envoyer à leur équipe de support technique lorsqu’ils travaillent dessus pour configurer votre site Bloomberg SFTP.

## <a name="step-3-create-an-instant-bloomberg-connector"></a>Étape 3: créer un connecteur Bloomberg instantané

La dernière étape consiste à créer un connecteur Bloomberg instantané dans le centre de sécurité & conformité. Le connecteur utilise les informations que vous fournissez pour vous connecter au site Bloomberg SFTP et transférer les messages de conversation dans les zones de boîte aux lettres utilisateur correspondantes dans Office 365. 

1. Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données** , puis cliquez sur **archiver les données**tierces.

2. Sur la page **données** tierces d’archivage, cliquez sur **Ajouter un connecteur**, puis cliquez sur **Bloomberg instantané**.

3. Sur la page **conditions de service** , cliquez sur **accepter**.

4. Sur la page **Ajouter des informations d’identification pour le site de Bloomberg SFTP** , sous étape 3, entrez les informations requises dans les zones suivantes, puis cliquez sur **suivant**.

    - **Code de confirmation:** ID de votre organisation et utilisé comme nom d’utilisateur pour le site Bloomberg SFTP.

    - **Mot de passe:** Mot de passe pour le site de Bloomberg SFTP

    - **URL sftp:** URL du site de Bloomberg SFTP (par exemple, sftp.bloomberg.com).

    - **Port sftp:** Numéro de port du site Bloomberg SFTP. Le connecteur utilise cette connexion pour se connecter au site SFTP.

5. Sur la page **autre boîte aux lettres** , tapez l’adresse de messagerie d’une boîte aux lettres qui est utilisée pour stocker les messages de conversation provenant d’un message de notification d’instant de la part qui ne sont pas associés à une boîte aux lettres utilisateur dans votre organisation.

   > [!NOTE]
   > Chaque message de conversation dans toutes les conversations de la notification instantanée Bloomberg inclut une propriété appelée *CorporateEmailAddress*, qui contient l’adresse de messagerie de votre organisation pour le participant de conversation. Pendant le processus d’importation, le connecteur tente d’importer des messages de conversation vers une boîte aux lettres d’utilisateur dans Office 365 qui a les mêmes adresses de messagerie que celles qui correspondent à celles de la propriété *CorporateEmailAddress* . S’il n’existe pas de boîte aux lettres Office 365 avec la même adresse que celle figurant dans la propriété *CorporateEmailAddress* , le connecteur importe le message de conversation vers l’autre boîte aux lettres que vous spécifiez sur cette page. Pour l’instant, les messages de conversation instantanée Bloomberg archivés dans l’autre boîte aux lettres ne sont pas analysés par les stratégies de surveillance dans Office 365.

6. Cliquez sur **suivant**, vérifiez vos paramètres, puis cliquez sur **préparer** pour créer le connecteur.

7. Accédez à la page **données** tierces d’archivage pour voir la progression du processus d’importation pour le nouveau connecteur.
