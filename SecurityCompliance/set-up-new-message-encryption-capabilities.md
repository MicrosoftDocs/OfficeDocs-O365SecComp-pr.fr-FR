---
title: Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Nouvelles fonctionnalités de chiffrement de messages Office 365 basées sur Azure Information Protection, votre organisation peut utiliser une communication de messagerie protégée avec des personnes à l’intérieur et à l’extérieur de votre organisation. Les nouvelles fonctionnalités OME fonctionnent avec les autres organisations Office 365, Outlook.com, Gmail et d’autres services de messagerie.
ms.openlocfilehash: 835b1d6f40868684536dbea8f75dab0665950210
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854798"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365

Les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME) permettent aux organisations de partager des courriers électroniques protégés avec n’importe quel appareil. Les utilisateurs peuvent échanger des messages protégés avec d’autres organisations Office 365, ainsi que des clients non-Office 365 à l’aide de Outlook.com, Gmail et d’autres services de messagerie.

||
|:-----|
|Cet article fait partie d’une grande série d’articles sur le chiffrement de messages Office 365. Ces informations sont destinées aux administrateurs et aux professionnels de l’informatique. Si vous recherchez simplement des informations sur l’envoi ou la réception d’un message chiffré, consultez la liste des articles dans [Chiffrement de messages Office 365](ome.md) (OME) et trouvez l’article qui correspond le mieux à vos besoins. |
||

Suivez les étapes ci-dessous pour vous assurer que les nouvelles fonctionnalités OME sont disponibles dans votre organisation Office 365.

## <a name="verify-that-azure-rights-management-is-active"></a>Vérifiez que Azure Rights Management est activé.

Les nouvelles fonctionnalités OME tirent parti des fonctionnalités de protection dans [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/fr-FR/azure/information-protection/what-is-information-protection), technologie utilisée par [Azure Information Protection](https://docs.microsoft.com/fr-FR/azure/information-protection/what-is-azure-rms) pour protéger les messages électroniques et les documents via les contrôles d’accès et de chiffrement.

La seule condition préalable à l’utilisation des nouvelles fonctionnalités OME est qu’[Azure Rights Management](https://docs.microsoft.com/fr-FR/azure/information-protection/what-is-azure-rms) doit être activé dans le client de votre organisation. Si c’est le cas, Office 365 active les nouvelles fonctionnalités OME automatiquement et vous n’avez rien à faire.

Azure RMS est également activé automatiquement pour la plupart des offres éligibles, de sorte que vous n’avez probablement pas besoin d’effectuer quoi que ce soit à cet égard. Pour plus d’informations, reportez-vous à [Activation d’Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service).

>[!IMPORTANT]
>Si vous utilisez Active Directory Rights Management Services (AD RMS) avec Exchange Online, vous devez [migrer vers Azure Information Protection](https://docs.microsoft.com/fr-FR/azure/information-protection/migrate-from-ad-rms-to-azure-rms) avant de pouvoir utiliser les nouvelles fonctionnalités OME. OME n’est pas compatible avec AD RMS.  

Pour plus d’informations, voir :

- [De quels abonnements ai-je besoin pour utiliser les nouvelles fonctionnalités OME ?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) pour vérifier si votre plan d’abonnement inclut Azure Information Protection (qui inclut les fonctionnalités Azure RMS).
- [Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) pour plus d’informations sur l’achat d’un abonnement éligible.  

### <a name="manually-activating-azure-rights-management"></a>Activation manuelle d’Azure Rights Management

Si vous avez désactivé Azure RMS, ou si le service n’a pas été automatiquement activé pour une raison quelconque, vous pouvez l’activer manuellement dans le :

- 
  **Centre d’administration Microsoft 365** : reportez-vous à [Comment activer Azure Rights Management à partir du centre d’administration](https://docs.microsoft.com/fr-FR/azure/information-protection/activate-office365) pour obtenir des instructions.
- **Portail Azure** : reportez-vous à [Comment activer Azure Rights Management à partir du portail Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) pour obtenir des instructions.

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Configurer la gestion de votre clé de client Azure Information Protection

Il s’agit d’une étape facultative. Autoriser Microsoft à gérer la clé racine pour Azure Information Protection est le paramètre par défaut et la meilleure pratique recommandée pour la plupart des clients Office 365. Si cela est le cas, vous n’avez rien à faire.

Il existe de nombreuses raisons, par exemple des exigences de conformité, qui peuvent nécessiter de créer et gérer votre propre clé racine (également connue sous le nom Utilisation de votre propre clé (BYOK)). Si c’est le cas, nous vous recommandons d’effectuer les étapes requises avant de configurer les nouvelles fonctionnalités OME. Pour plus d’informations, reportez-vous à [Planification et implémentation de votre clé de client Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Vérifier la nouvelle configuration OME dans Exchange Online PowerShell

Vous pouvez vérifier que votre client Office 365 est correctement configuré pour utiliser les nouvelles fonctionnalités OME dans [Exchange Online PowerShell](https://docs.microsoft.com/fr-FR/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
  
1. 
  [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/fr-FR/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) à l’aide d’un compte disposant des autorisations d’administrateur général dans votre client Office 365.

2. Exécutez la cmdlet Get-IRMConfiguration.

     Une valeur de $True s’affiche pour le paramètre AzureRMSLicensingEnabled qui indique que OME est configuré dans votre client. Si ce n’est pas le cas, utilisez Set-IRMConfiguration pour activer la valeur d’AzureRMSLicensingEnabled sur $True pour activer OME.

3. Exécutez la cmdlet Test-IRMConfiguration en utilisant la syntaxe suivante :

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Exemple** :

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - La fourniture d’un courrier électronique d’expéditeur est facultative, mais oblige le système à effectuer des vérifications supplémentaires. Utilisez l’adresse de courrier électronique de n’importe quel utilisateur de votre client Office 365.

     Vos résultats doivent être similaires à ce qui suit :

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - Le nom de votre organisation Office 365 remplacera *Contoso*.

   - Les noms des modèles par défaut peuvent être différents de ceux affichés ci-dessus. Pour plus d’informations, reportez-vous à [Configurer et gérer des modèles pour Azure Information Protection](https://docs.microsoft.com/fr-FR/azure/information-protection/configure-policy-templates).

4. Exécutez la cmdlet Remove-PSSession pour vous déconnecter du service Rights Management.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a>Étapes suivantes : définir des règles de flux de messagerie pour utiliser les nouvelles fonctionnalités OME

S’il existe des règles de flux de messagerie précédemment configurées permettant de chiffrer le courrier électronique dans votre organisation Office 365, vous devez mettre à jour les règles existantes pour utiliser les nouvelles fonctionnalités OME. Pour les nouveaux déploiements, vous devez créer des règles de flux de messagerie.

>[!IMPORTANT]
>Si vous ne mettez pas à jour les règles de flux de messagerie existantes, vos utilisateurs continueront à recevoir des e-mails chiffrés qui utilisent le format de pièces jointes HTML précédent, au lieu de la nouvelle expérience OME transparente.

Les règles de flux de messagerie déterminent les conditions dans lesquelles les e-mails doivent être chiffrés, ainsi que les conditions pour supprimer ce chiffrement. Lorsque vous configurez une action pour une règle, tous les messages correspondant aux conditions de la règle sont chiffrés lorsqu’elles sont envoyées.
  
Pour plus d’informations sur la création de règles de flux de messagerie pour OME, reportez-vous à [Définir des règles de flux de courrier pour le chiffrement du courrier dans Office 365](define-mail-flow-rules-to-encrypt-email.md).

Pour mettre à jour les règles existantes afin d’utiliser les nouvelles fonctionnalités OME :

1. Dans le Centre d’administration Microsoft 365, accédez à **Centres d’administration > Exchange**.
2. Dans le Centre d’administration Exchange, accédez à **Flux de messagerie > Règles**.
3. Pour chaque règle, dans **Procédez comme suit** :
    - Sélectionnez **Modifier la sécurité des messages**.
    - Sélectionnez **Appliquer le chiffrement des messages Office 365 et la protection des droits**.
    - Sélectionnez un modèle RMS dans la liste.
    - Cliquez sur **Enregistrer**.
    - Sélectionnez **OK**.
