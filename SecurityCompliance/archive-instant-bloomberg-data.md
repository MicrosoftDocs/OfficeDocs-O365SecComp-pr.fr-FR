---
title: Configuration d’un connecteur pour l’archivage des données Bloomberg instantanées dans Office 365 (aperçu)
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
ms.openlocfilehash: 0b69ddaa21196bd0e149eba672fec104eabe2e5e
ms.sourcegitcommit: ab16ddf4c050a995471a058150767a0778be0b88
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35431599"
---
# <a name="set-up-a-connector-to-archive-instant-bloomberg-data-in-office-365-preview"></a>Configuration d’un connecteur pour l’archivage des données Bloomberg instantanées dans Office 365 (aperçu)

La fonctionnalité de connecteur permettant d’archiver les données de la version Bloomberg instantanée dans Office 365 est en aperçu.

Utilisez un connecteur natif dans le centre de sécurité & conformité dans Office 365 pour importer et archiver les données de conversation des services financiers à partir de l’outil de collaboration [instant Bloomberg](https://www.bloomberg.com/professional/product/collaboration/) . Une fois que vous avez configuré et configuré un connecteur, il se connecte au site FTP Secure (SFTP) de votre organisation une fois par jour, convertit le contenu des messages de conversation en format de message électronique, puis importe ces éléments dans des boîtes aux lettres dans Office 365.

Une fois les données instantanées Bloomberg stockées dans les boîtes aux lettres des utilisateurs, vous pouvez appliquer les fonctionnalités de conformité d’Office 365 telles que la conservation pour litige, la recherche de contenu, l’archivage inaltérable, l’audit et les stratégies de rétention d’Office 365 aux données instantanées Bloomberg. Par exemple, vous pouvez rechercher des messages de conversation instant Bloomberg à l’aide de la recherche de contenu ou associer la boîte aux lettres qui contient les données Bloomberg instantanée à un dépositaire dans un cas avancé de découverte électronique. L’utilisation d’un connecteur Bloomberg instantané pour importer et archiver des données dans Office 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.

## <a name="overview-of-archiving-instant-bloomberg-data"></a>Vue d’ensemble de l’archivage des données de la fonctionnalité Bloomberg instantanée

La vue d’ensemble suivante décrit le processus d’utilisation d’un connecteur pour archiver des données de conversation de messagerie instantanée Bloomberg dans Office 365. 

![Processus d’importation et d’archivage de Bloomberg instantané](media/InstantBloombergDataArchiving.png)

1. Votre organisation travaille avec Bloomberg pour configurer un site Bloomberg SFTP. Vous allez également utiliser Bloomberg pour configurer la copie instantanée de messages de conversation sur votre site Bloomberg SFTP.

2. Une fois toutes les 24 heures, les messages de conversation provenant d’instant Bloomberg sont copiés sur le site Bloomberg SFTP.
    
3. Le connecteur Bloomberg instantané que vous créez dans le centre de sécurité & conformité se connecte au site de Bloomberg SFTP tous les jours et transfère les messages de conversation des dernières 24 heures vers une zone de stockage Azure sécurisée dans le Cloud Microsoft. Le connecteur convertit également le contenu d’un massage de conversation au format d’un message électronique.
    
4. Le connecteur importe les éléments de message de conversation vers la boîte aux lettres d’un utilisateur spécifique ou vers une autre boîte aux lettres. Le connecteur utilise la valeur de la propriété *CorporateEmailAddress* . Chaque message de conversation contient cette propriété, qui est renseignée avec l’adresse de messagerie de chaque participant du message de conversation. L’impossibilité d’importer un élément dans une boîte aux lettres utilisateur spécifique ou dans une autre boîte aux lettres est basée sur les critères suivants:
    
    a. **Éléments ayant une valeur dans la propriété CorporateEmailAddress qui correspond à un compte d’utilisateur office 365** : si le connecteur peut associer l’adresse de messagerie de la propriété *CorporateEmailAddress* à un compte d’utilisateur spécifique dans Office 365, le l’élément est copié dans le dossier boîte de réception de la boîte aux lettres Office 365 de l’utilisateur.
    
    b. **Éléments dont la propriété CorporateEmailAddress ne correspond pas à un compte d’utilisateur Office 365** : si le connecteur ne peut pas associer une adresse de messagerie de la propriété *CorporateEmailAddress* à un compte d’utilisateur spécifique dans Office 365, l’élément est copié dans le dossier boîte de réception d’une autre boîte aux lettres «fourre-tout» dans Office 365.

## <a name="before-you-begin"></a>Avant de commencer

La plupart des étapes d’implémentation nécessaires à l’archivage des données de la demande instantanée sont externes à Office 365 et doivent être effectuées pour pouvoir créer le connecteur dans le centre de sécurité & conformité.

- Abonnez-vous à [Blooomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA). Cette opération est nécessaire afin que vous puissiez vous connecter à Bloomberg Anywhere pour accéder au site Bloomberg SFTP que vous devez configurer et configurer.

- Configurez un site Bloomberg SFTP (Secure File Transfer Protocol). Après avoir travaillé avec Bloomberg pour configurer le site SFTP, les données de instant Bloomberg sont téléchargées sur le site SFTP tous les jours. Le connecteur que vous créez à l’étape 2 se connecte à ce site SFTP et transfère les données de conversation vers les boîtes aux lettres Office 365. SFTP chiffre également les données de conversation de la messagerie instantanée Bloomberg envoyées aux boîtes aux lettres Office 365 lors du processus de transfert.

    Pour plus d’informations sur Bloomberg SFTP (également appelé *BB-SFTP*):

    - Consultez le document «standards de connectivité SFTP» sur le [support Bloomberg](https://www.bloomberg.com/professional/support/documentation/).
    
    - Contacter le [support client Bloomberg](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc).

    Une fois que vous avez travaillé avec Bloomberg pour configurer un site SFTP, Bloomberg vous fournira des informations après avoir répondu au message d’implémentation Bloomberg. Enregistrez une copie des informations suivantes. Vous l’utilisez pour configurer un connecteur à l’étape 3.

    - Le code de confirmation, qui est un ID pour votre organisation et est utilisé pour se connecter au site Bloomberg SFTP.

    - Mot de passe pour votre site Bloomberg SFTP

    - URL du site de Bloomberg SFTP (par exemple, sftp.bloomberg.com)

    - Numéro de port pour le site Bloomberg SFTP

- Votre organisation doit consentir à autoriser le service d’importation Office 365 à accéder aux données de boîte aux lettres dans votre organisation. Pour accepter cette demande, accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), connectez-vous à l’aide des informations d’identification d’un administrateur général Office 365, puis acceptez la demande. Vous devez effectuer cette étape avant de pouvoir créer le connecteur Bloomberg instantané à l’étape 3.

- L’utilisateur qui crée un connecteur Bloomberg instantané à l’étape 3 (et qui télécharge les clés publiques et l’adresse IP à l’étape 1) doit se voir attribuer le rôle d’exportation d’importation de boîte aux lettres dans Exchange Online. Cela est nécessaire pour accéder à la page **données** tierces d’archivage dans le centre de sécurité & conformité. Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle exportation d’importation de boîte aux lettres au groupe de rôles gestion de l’organisation dans Exchange Online. Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d’exportation d’importation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres. Pour plus d’informations, reportez-vous aux sections [créer des groupes de rôles](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou modifier des [groupes](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) de rôles dans l’article «gérer des groupes de rôles dans Exchange Online».

## <a name="step-1-obtain-ssh-and-pgp-public-keys"></a>Étape 1: obtenir des clés publiques SSH et PGP

La première étape consiste à obtenir une copie des clés publiques pour le protocole SSH (Secure Shell) et PGP (Pretty bonne confidentialité). Utilisez ces clés à l’étape 2 pour configurer le site Bloomberg SFTP de sorte que le connecteur (que vous créez à l’étape 3) se connecte au site SFTP et transfère les données de conversation instant Bloomberg vers les boîtes aux lettres Office 365. Vous pouvez également obtenir une adresse IP dans cette étape, que vous utiliserez lors de la configuration du site Bloomberg SFTP.

1. Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données** , puis cliquez sur **archiver les données**tierces.

2. Sur la page **données** tierces d’archivage, cliquez sur **Ajouter un connecteur**, puis cliquez sur **Bloomberg instantané**.

3. Sur la page **conditions de service** , cliquez sur **accepter**.

4. Sur le **site ajouter des informations d’identification pour Bloomberg SFTP** sous étape 1, cliquez sur **Télécharger la clé SSH** et télécharger les liens de téléchargement de la **clé PGP** pour enregistrer une copie de chaque fichier de clé publique sur votre ordinateur local. Ces fichiers contiennent les éléments suivants qui seront utilisés pour configurer le site de Bloomberg SFTP à l’étape 2:

   - Clé publique SSH: cette clé est utilisée pour configurer le protocole SSH (Secure Shell) pour activer une connexion à distance sécurisée lorsque le connecteur se connecte au site Bloomberg SFTP.

   - Clé publique PGP: cette clé est utilisée pour configurer le chiffrement des données transférées à partir du site Bloomberg SFTP vers Office 365.

   - Adresse IP: le site Bloomberg SFTP est configuré pour accepter une demande de connexion uniquement à partir de cette adresse IP, utilisée par le connecteur Bloomberg instantané que vous créez à l’étape 3. 

5. Cliquez sur **Annuler** pour fermer l’Assistant. Vous revenez à cet Assistant à l’étape 3 pour créer le connecteur.

## <a name="step-2-configure-the-bloomberg-sftp-site"></a>Étape 2: configurer le site Bloomberg SFTP

L’étape suivante consiste à utiliser les clés publiques SSH et PGP, ainsi que l’adresse IP que vous avez obtenue à l’étape 1, pour configurer l’authentification SSH et le chiffrement PGP pour le site Bloomberg SFTP. Cela permet au connecteur Bloomberg instantané que vous créez à l’étape 3 de se connecter au site Bloomberg SFTP et de transférer les données de la procédure Bloomberg vers Office 365. Contactez le [support client Bloomberg](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) si vous avez besoin d’aide pour le configurer.

1. Ouvrez une session dans le panneau de configuration Bloomberg CCN à l’aide d’un compte pour votre organisation.

2. Accédez à CCN, puis cliquez sur l’onglet **clés publiques** .

3. Pour activer l’authentification SSH, cliquez sur **Ajouter**.

4. Dans la fenêtre **Ajouter une clé publique** , cliquez sur la liste déroulante **type de clé** , puis cliquez sur **connexion**.

5. Copiez l’intégralité de la clé publique SSH (tous les caractères compris entre guillemets doubles) que vous avez téléchargé à l’étape 1, collez-le dans ce champ, puis cliquez sur **Envoyer** pour enregistrer la clé.
 
    Par exemple, vous pouvez copier la clé publique SSH suivante:

    `
    ssh-rsa
    AAAAB3NzaC1yc2EAAAABIwAAAQEA1dxAyc0JzCmc5NzgyzRYhnj3FGHK5Kd9T2cwZNkmL/9nFhQupQor081rmuw9gACAmeot7y+V/fmijo/q4rxDe3Auu3hfLl1NpWlIssQJHzycms8zimtdQcXbMKwDQOnRthpEocF5ySs76KE72vaYQJTvclAamWWq0D75SUmXDFFr7afvEy57F7KgMD1ecg6lH7q8seSKbiiWxX1Ul0kL15fzpUyhjDP41owb1XC/dF7fJwAmCO1+HZfDLEp62q4tnApLpdd92KoR41LZTryO5dICKhk+S+JxPLkksxL0wm5YevOr2n4ScuRdsBV8mWKZ1Xw+cOss9O6L7cCcEiB3Ow==
    `

6. Pour activer le chiffrement PGP, cliquez à nouveau sur **Ajouter** sous l’onglet **clés publiques** , cliquez sur la liste déroulante **type de clé** , puis cliquez sur **chiffrement**.

7. Copiez l’intégralité de la clé publique PGP (tous les caractères compris entre guillemets doubles) que vous avez téléchargé à l’étape 1, collez-le dans ce champ, puis cliquez sur **Envoyer** pour enregistrer la clé. 

    Par exemple, vous pouvez copier la clé publique PGP suivante:

    `
    -----BEGIN PGP PUBLIC KEY BLOCK-----
    Version: BCPG C# v1.7.4137.9688
    nmQENBFz+6UQBCACKC4ilYoVOP5b/F0CO+oQYbag79Ov4NZxM4EKW51lUAvKNExRM\nc1C/gwXm8bghht8GEODckXXqx8qSSXUEeA/ROweXNtD1u1kn7PgYEFUeD/qE739m\nm5lxXF9Vod26AtKQ9Y1EvYoQEltwztAaXg8K8LQzB+tzN079d1cxM5tbiRQLttAh\nOt5amLXuINt8+dWyNas3DfgIBUmwfkwCbUO0ElrIhvvO3A85K97SX9Q6Py0SkfkK\nQpnULuhdjSm+7k7qlVMf0s8e/9jUXYKbMFkxlOoMq052vV0l0VQNSeuKoC+m6+LT\nEPab89AMt6S4Ujum9wTUy1eWNx9vV0y/w8N7ABEBAAG0JDM5MjM4ZTg3LWI1YWIt\nNGVmNi1hNTU5LWFmNTRjNmIwN2I0MokBHAQQAQIABgUCXP7pRAAKCRAJQdjaG//S\nCy70B/wKrR2CcqtZx56yrGJFfVy3niEt16VEA3xJM3D9nX0gmgo85Nh5gkiY3ahH\nnNEmgW5vlCM1gcgFeoZWe8A80G4QoabslSUzLbq9HsHOOAQApsfhrhXpylrAVa4n\nI53XUOxWdOTa4xsOob8hSRADqJbwHPOsoAr2A87TvZ9LSi2Mii5omeTq416CLnoS\nPBAEhelZm+ruy5JhzA1yXvWYFH08wNqSHO3bskdES2yW5SyQmYlcoEztWE0Q0Z+G\nZT3kOa/W2MbcZovFCQIfqhwVfXtIzx5uYUmxgk5cFKUJJMlO0AZK/HwM22xuuIWe\ndMa6OMo/n8tvEBxrLQMdVPlz+hZ6
    =AwmP
    -----END PGP PUBLIC KEY BLOCK-----
    `
8. De retour dans la fenêtre principale du panneau de configuration CCN, sous **ajouter votre adresse IP ici**, entrez l’adresse IP suivante (incluse dans le fichier Keys. txt que vous avez téléchargé à l’étape 1) dans le **champ Ajouter une adresse**.

   `
   40.124.28.216
   `

## <a name="step-3-create-an-instant-bloomberg-connector"></a>Étape 3: créer un connecteur Bloomberg instantané

La dernière étape consiste à créer un connecteur Bloomberg instantané dans le centre de sécurité & conformité. Le connecteur utilise les informations que vous fournissez pour vous connecter au site Bloomberg SFTP et transférer les messages de conversation dans les zones de boîte aux lettres utilisateur correspondantes dans Office 365. 

1. Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données** , puis cliquez sur **archiver les données**tierces.

2. Sur la page **données** tierces d’archivage, cliquez sur **Ajouter un connecteur**, puis cliquez sur **Bloomberg instantané**.

3. Sur la page **conditions de service** , cliquez sur **accepter**.

4. Sur la page **Ajouter des informations d’identification pour le site de Bloomberg SFTP** , sous étape 3, entrez les informations requises dans les zones suivantes, puis cliquez sur **suivant**.

    - **Code de confirmation** : ID de votre organisation et utilisé comme nom d’utilisateur pour le site Bloomberg SFTP.

    - **Mot de passe** – mot de passe pour le site de Bloomberg SFTP

    - **URL SFTP** : URL du site Bloomberg SFTP (par exemple, SFTP.Bloomberg.com).

    - **Port SFTP** : numéro de port du site Bloomberg SFTP. Le connecteur utilise cette connexion pour se connecter au site SFTP.

5. Sur la page **autre boîte aux lettres** , tapez l’adresse de messagerie d’une boîte aux lettres qui sera utilisée pour stocker les messages de conversation provenant d’un utilisateur de Bloomberg qui ne peuvent pas être associés à une boîte aux lettres utilisateur dans votre organisation.

   > [!NOTE]
   > Chaque message de conversation dans toutes les conversations de la notification instantanée Bloomberg inclut une propriété appelée *CorporateEmailAddress*, qui contient l’adresse de messagerie de votre organisation pour le participant de conversation. Pendant le processus d’importation, le connecteur tente d’importer des messages de conversation vers une boîte aux lettres d’utilisateur dans Office 365 qui a les mêmes adresses de messagerie que celles qui correspondent à celles de la propriété *CorporateEmailAddress* . S’il n’existe pas de boîte aux lettres Office 365 avec la même adresse que celle figurant dans la propriété *CorporateEmailAddress* , le connecteur importe le message de conversation vers l’autre boîte aux lettres que vous spécifiez sur cette page. Pour l’instant, les messages de conversation instantanée Bloomberg archivés dans l’autre boîte aux lettres ne sont pas analysés par les stratégies de surveillance dans Office 365.

6. Cliquez sur **suivant**, vérifiez vos paramètres, puis cliquez sur **préparer** pour créer le connecteur.

7. Accédez à la page **données** tierces d’archivage pour voir la progression du processus d’importation pour le nouveau connecteur.
