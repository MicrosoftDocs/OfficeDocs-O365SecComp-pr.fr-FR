---
title: Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365
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
description: Les nouvelles fonctionnalités de chiffrement de messages Office 365 basées sur Azure information protection, votre organisation peut utiliser la communication de messagerie protégée avec des personnes à l’intérieur et à l’extérieur de votre organisation. Les nouvelles fonctionnalités de OME fonctionnent avec d’autres organisations Office 365, Outlook.com, Gmail et d’autres services de messagerie.
ms.openlocfilehash: 835b1d6f40868684536dbea8f75dab0665950210
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854798"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365

Les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME) permettent aux organisations de partager des courriers électroniques protégés avec quiconque sur n’importe quel appareil. Les utilisateurs peuvent échanger des messages protégés avec d’autres organisations Office 365, ainsi que des clients non-Office 365 à l’aide de Outlook.com, Gmail et d’autres services de messagerie.

||
|:-----|
|Cet article fait partie d’une série d’articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et aux professionnels de l’informatique. Si vous recherchez simplement des informations sur l’envoi ou la réception d’un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l’article qui répond le mieux à vos besoins. |
||

Suivez les étapes ci-dessous pour vous assurer que les nouvelles fonctionnalités de OME sont disponibles dans votre organisation Office 365.

## <a name="verify-that-azure-rights-management-is-active"></a>Vérifier que la gestion des droits Azure est active

Les nouvelles fonctionnalités OME tirent parti des fonctionnalités de protection d’Azure [Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), la technologie utilisée par [Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) pour protéger les messages électroniques et les documents via le chiffrement et les contrôles d’accès.

La seule condition requise pour l’utilisation des nouvelles fonctionnalités OME est que la [gestion des droits Azure](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) doit être activée dans le client de votre organisation. Si c’est le cas, Office 365 active automatiquement les nouvelles fonctionnalités OME et vous n’avez rien à faire.

Azure RMS est également activé automatiquement pour la plupart des plans éligibles, de sorte que vous n’avez probablement pas à faire quoi que ce soit. Pour plus d’informations, reportez-vous à la rubrique [activation d’Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .

>[!IMPORTANT]
>Si vous utilisez le service AD RMS (Active Directory Rights Management) avec Exchange Online, vous devez [migrer vers Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) avant de pouvoir utiliser les nouvelles fonctionnalités de ome. OME n’est pas compatible avec AD RMS.  

Pour plus d’informations, reportez-vous aux rubriques suivantes :

- [Quels sont les abonnements nécessaires pour utiliser les nouvelles fonctionnalités d’ome?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) pour vérifier si votre plan d’abonnement inclut Azure information protection (qui inclut la fonctionnalité AD RMS).
- [Azure information protection](https://azure.microsoft.com/en-us/services/information-protection/) pour plus d’informations sur l’achat d’un abonnement éligible.  

### <a name="manually-activating-azure-rights-management"></a>Activation manuelle de la gestion des droits Azure

Si vous avez désactivé Azure RMS, ou s’il n’a pas été activé automatiquement pour une raison quelconque, vous pouvez l’activer manuellement dans:

- **Centre d’administration Microsoft 365**: Découvrez [Comment activer Azure Rights Management à partir du centre d’administration](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) pour obtenir des instructions.
- **Portail Azure**: Découvrez [Comment activer Azure Rights Management à partir du portail Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) pour obtenir des instructions.

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Configurer la gestion de votre clé de client Azure information protection

Cette étape est facultative. Autoriser Microsoft à gérer la clé racine pour Azure information protection est le paramètre par défaut et meilleure pratique recommandée pour la plupart des clients Office 365. Si c’est le cas, aucune action n’est nécessaire.

Il existe de nombreuses raisons, telles que les exigences de conformité, qui peuvent nécessiter la génération et la gestion de votre propre clé racine (également appelée créer votre propre clé (BYOK)). Dans ce cas, nous vous recommandons d’effectuer les étapes requises avant de configurer les nouvelles fonctionnalités de OME. Pour plus d’informations, consultez [la rubrique planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Vérifier la nouvelle configuration de OME dans Exchange Online PowerShell

Vous pouvez vérifier que votre client Office 365 est correctement configuré pour utiliser les nouvelles fonctionnalités de OME dans [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
  
1. [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) à l’aide d’un compte disposant d’autorisations d’administrateur général dans votre client Office 365.

2. Exécutez la cmdlet Get-IRMConfiguration.

     Vous devriez voir une valeur de $True pour le paramètre AzureRMSLicensingEnabled, qui indique que OME est configuré dans votre client. Si ce n’est pas le cas, utilisez Set-IRMConfiguration pour définir la valeur de AzureRMSLicensingEnabled sur $True afin d’activer OME.

3. Exécutez la cmdlet Test-IRMConfiguration à l’aide de la syntaxe suivante:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Exemple** :

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - L’envoi d’un message électronique est facultatif, mais force le système à effectuer des vérifications supplémentaires. Utilisez l’adresse de messagerie de n’importe quel utilisateur de votre client Office 365.

     Vos résultats doivent ressembler à ce qui suit:

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

   - Le nom de votre organisation Office 365 remplacera *contoso*.

   - Les noms de modèle par défaut peuvent être différents de ceux affichés ci-dessus. Pour plus d’informations, reportez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .

4. Exécutez la cmdlet Remove-PSSession pour vous déconnecter du service gestion des droits.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a>Étapes suivantes: définir des règles de flux de messagerie pour utiliser les nouvelles fonctionnalités de OME

S’il existe des règles de flux de messagerie précédemment configurées pour chiffrer les messages électroniques dans votre organisation Office 365, vous devez mettre à jour les règles existantes pour utiliser les nouvelles fonctionnalités de OME. Pour les nouveaux déploiements, vous devez créer des règles de flux de messagerie.

>[!IMPORTANT]
>Si vous ne mettez pas à jour les règles de flux de messagerie existantes, vos utilisateurs continueront à recevoir des messages chiffrés qui utilisent le format de pièce jointe HTML précédent au lieu de la nouvelle expérience OME transparente.

Les règles de flux de messagerie déterminent les conditions dans lesquelles les messages électroniques doivent être chiffrés, ainsi que les conditions de suppression de ce chiffrement. Lorsque vous définissez une action pour une règle, tous les messages qui correspondent aux conditions de la règle sont chiffrés lorsqu’ils sont envoyés.
  
Pour obtenir la procédure de création des règles de flux de messagerie pour OME, consultez la rubrique [define mail Flow Rules to Encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).

Pour mettre à jour les règles existantes afin d’utiliser les nouvelles fonctionnalités OME:

1. Dans le centre d’administration Microsoft 365, accédez à centre d’administration **> Exchange**.
2. Dans le centre d’administration Exchange, accédez à **flux de messagerie > règles**.
3. Pour chaque règle, dans **effectuer les opérations suivantes**:
    - Sélectionnez **modifier la sécurité des messages**.
    - Sélectionnez **appliquer le chiffrement de messages Office 365 et protection des droits**.
    - Sélectionnez un modèle RMS dans la liste.
    - Cliquez sur **Enregistrer**.
    - Sélectionnez **OK**.
