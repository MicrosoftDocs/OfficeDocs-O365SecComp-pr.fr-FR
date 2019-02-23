---
title: Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Les nouvelles fonctionnalités de chiffrement de messages Office 365 basées sur Azure information protection, votre organisation peut utiliser la communication de messagerie protégée avec des personnes à l'intérieur et à l'extérieur de votre organisation. Les nouvelles fonctionnalités de OME fonctionnent avec d'autres organisations Office 365, Outlook.com, Gmail et d'autres services de messagerie.
ms.openlocfilehash: eddafca15fa4efdd3f929145e7933a3b7dfb5f27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220644"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365

Avec les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME), qui tirent parti des fonctionnalités de protection d'Azure information protection, votre organisation peut facilement partager le courrier électronique protégé avec n'importe quel appareil. Les utilisateurs peuvent envoyer et recevoir des messages protégés avec d'autres organisations Office 365, ainsi que des clients non-Office 365 à l'aide de Outlook.com, Gmail et autres services de messagerie.

||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins. |
||

## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>Prise en main de OME en activant Azure Rights Management, partie de Azure information protection

Il est désormais facile de commencer avec les nouvelles fonctionnalités de OME. Depuis le 2018 février, Office 365 active automatiquement les nouvelles fonctionnalités OME pour les organisations éligibles au sein de nos centres de donnees. Votre organisation est éligible s'il s'agit d'un nouveau client Office 365 et que votre organisation dispose des abonnements appropriés. **Si vous avez activé Azure Rights Management (Azure RMS), partie de Azure information protection, nous activons automatiquement le chiffrement de messages Office 365 pour vous.** Vous n'avez rien à faire d'autre pour activer OME. Pour activer Azure Rights Management, consultez la rubrique activation de la [gestion des droits Azure](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Pour plus d'informations sur les abonnements, voir «quels abonnements dois-je utiliser le nouveau OME capabilities?» dans le [Forum aux questions sur le chiffrement de messages Office 365](ome-faq.md). Pour plus d'informations sur l'achat d'un abonnement à Azure information protection, voir [Azure information protection](https://azure.microsoft.com/services/information-protection/).
  
Si vous utilisez Exchange Online avec Active Directory Rights Management Services (AD RMS), vous ne pouvez pas activer immédiatement ces nouvelles fonctionnalités. Au lieu de cela, vous devez d'abord migrer d'AD RMS vers Azure information protection. Une fois la migration terminée, vous pouvez effectuer les étapes suivantes.
  
Si vous choisissez de continuer à utiliser AD RMS sur site avec Exchange Online au lieu de migrer vers Azure information protection, vous ne pourrez pas utiliser ces nouvelles fonctionnalités.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>Comment les nouvelles fonctionnalités de OME fonctionnent

Les nouvelles fonctionnalités de chiffrement des messages Office 365 utilisent les fonctionnalités de protection, également appelées Azure Rights Management (Azure RMS), d'Azure information protection. Cela inclut les stratégies de chiffrement, d'identité et d'autorisation pour sécuriser votre courrier électronique. Vous pouvez chiffrer les messages à l'aide des modèles de gestion des droits, de l' [option ne pas transférer](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)et de l' [option de chiffrement uniquement](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails). Les utilisateurs peuvent ensuite chiffrer les messages électroniques et une variété de pièces jointes Office 365 à l'aide de ces options. Pour obtenir la liste complète des types de pièces jointes prises en charge, voir [«types de fichiers couverts par les stratégies IRM lorsqu'ils sont attachés à des messages» dans Introduction to IRM for email messages](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). En tant qu'administrateur, vous pouvez également définir des règles de flux de messagerie pour appliquer cette protection. Par exemple, vous pouvez définir une règle où tous les messages non protégés adressés à un destinataire spécifique ou contenant des mots spécifiques dans la ligne d'objet sont protégés contre tout accès non autorisé et les destinataires ne peuvent pas copier ou imprimer le contenu du message.
  
Contrairement à la version précédente de OME, ces nouvelles fonctionnalités fournissent une expérience d'expéditeur unifiée, que vous envoyiez du courrier à l'intérieur de votre organisation ou à des destinataires en dehors d'Office 365. De plus, les destinataires qui reçoivent un message électronique protégé envoyé à un compte Office 365 dans Outlook 2016 ou Outlook sur le Web ne doivent effectuer aucune action supplémentaire pour afficher le message. Elle fonctionne de façon transparente. Les destinataires qui utilisent d'autres clients de messagerie et des fournisseurs de services de messagerie ont également une expérience améliorée. Pour plus d'informations, consultez la rubrique [en savoir plus sur les messages protégés dans Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) et [Comment ouvrir un message protégé](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).

Pour obtenir une liste détaillée des différences entre la version précédente de OME et les nouvelles fonctionnalités OME, consultez la rubrique [compare versions of OME](ome-version-comparison.md).
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>Étapes à suivre pour configurer manuellement les nouvelles fonctionnalités de OME

Les nouvelles fonctionnalités de OME sont automatiquement activées pour la plupart des organisations Office 365. Si votre organisation n'a pas automatiquement OME activé, ou si vous avez désactivé les nouvelles fonctionnalités de OME, procédez comme suit pour configurer manuellement les nouvelles fonctionnalités de OME.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>Pour configurer manuellement les nouvelles fonctionnalités de OME

1. Vérifiez que vous disposez de l'abonnement approprié pour votre organisation. Pour plus d'informations sur les abonnements, voir «quels abonnements dois-je utiliser le nouveau OME capabilities?» dans le [Forum aux questions sur le chiffrement de messages Office 365.](ome-faq.md). Pour plus d'informations sur l'achat d'un abonnement à Azure information protection, voir [Azure information protection](https://azure.microsoft.com/services/information-protection/).

2. Déterminez si vous voulez que Microsoft gère la clé racine pour Azure information protection (valeur par défaut), ou générez et gérez vous-même cette clé (appelée apporter votre propre clé, ou BYOK). Si vous souhaitez générer et gérer cette clé vous-même, vous devez effectuer certaines étapes avant de configurer les nouvelles fonctionnalités de OME. Pour plus d'informations, consultez [la rubrique planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). Microsoft vous recommande d'effectuer ces étapes avant de configurer OME.

3. Activez les nouvelles fonctionnalités de OME en activant Azure Rights Management. Pour obtenir des instructions, consultez la rubrique activation de la [gestion des droits Azure](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Lorsque vous effectuez cette opération, Office 365 active automatiquement les nouvelles fonctionnalités OME.

    > [!TIP]
    > Outlook sur le Web met en cache son interface utilisateur, c'est pourquoi il est recommandé d'attendre un jour avant d'appliquer les nouvelles fonctionnalités de OME aux messages électroniques à l'aide de ce client. Avant que l'interface utilisateur ne soit mise à jour pour refléter la nouvelle configuration, les nouvelles fonctionnalités de OME ne sont pas disponibles. Une fois que l'interface utilisateur est mise à jour, les utilisateurs peuvent protéger les messages électroniques à l'aide des nouvelles fonctionnalités de OME.
  
4. Module ConFigurez de nouvelles règles de flux de messagerie ou mettez à jour des règles de flux de messagerie existantes qui définissent comment et quand vous souhaitez qu'Office 365 chiffre les messages envoyés à partir de votre organisation.

## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Vérifier que les nouvelles fonctionnalités de OME sont correctement configurées à l'aide de Windows PowerShell

Procédez comme suit pour vérifier que votre client est correctement configuré pour utiliser les nouvelles fonctionnalités de OME via Exchange Online PowerShell.
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Test-IRMConfiguration à l'aide de la syntaxe suivante:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   Par exemple :

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

    Où adresse de messagerie est l'adresse de messagerie d'un utilisateur dans votre organisation Office 365. S'il est facultatif, la fourniture d'une adresse de messagerie d'expéditeur force le système à effectuer des vérifications supplémentaires. Vos résultats doivent ressembler à ceux-ci:

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

    Où *contoso* est remplacé par le nom de votre organisation Office 365.

    Les noms des modèles par défaut renvoyés dans les résultats peuvent être différents de ceux affichés dans les résultats ci-dessus.

    Pour obtenir une présentation des modèles et des informations sur les modèles par défaut, reportez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d'informations sur l'option de non-transfert, l'option de chiffrement uniquement et sur la création de modèles supplémentaires ou sur la recherche des droits inclus dans un modèle existant, voir [Configuration des droits d'utilisation pour Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).

3. Exécutez la cmdlet Remove-PSSession pour vous déconnecter du service gestion des droits.
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>Étapes suivantes: définir de nouvelles règles de flux de messagerie qui utilisent les nouvelles fonctionnalités de OME

Cette étape est facultative pour les nouveaux déploiements OME, cependant, cette étape est requise pour les déploiements OME existants qui ont déjà des règles de flux de messagerie configurées pour chiffrer les messages sortants. Si vous souhaitez tirer parti des nouvelles fonctionnalités OME, vous devez mettre à jour vos règles de flux de messagerie existantes. Dans le cas contraire, vos utilisateurs continueront à recevoir des messages chiffrés qui utilise le format de pièce jointe HTML précédent au lieu de la nouvelle expérience OME transparente.
  
Les règles de flux de messagerie déterminent les conditions dans lesquelles les messages électroniques doivent être chiffrés, ainsi que les conditions de suppression de ce chiffrement. Lorsque vous définissez une action pour une règle, tous les messages qui correspondent aux conditions de la règle sont chiffrés lorsqu'ils sont envoyés.
  
Pour plus d'informations sur les règles de flux de messagerie, consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Voir aussi

[Envoyer, afficher et répondre à des messages chiffrés dans Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Enable-Aadrm](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[Connexion à Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[Définir des règles de flux de courrier pour le chiffrement du courriers dans Office 365](define-mail-flow-rules-to-encrypt-email.md)
