---
title: Définir des règles de flux de courrier pour le chiffrement du courriers dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à créer des règles de flux de messagerie (également appelées règles de transport) pour chiffrer et déchiffrer les messages à l'aide du chiffrement de messages Office 365 (OME).
ms.openlocfilehash: f76abe2d341b9e3677a90d447e70f6091e3a91cc
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276204"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Définir des règles de flux de courrier pour le chiffrement du courriers dans Office 365

En tant qu'administrateur général Office 365, vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) pour protéger les messages électroniques que vous envoyez et recevez. Vous pouvez définir des règles pour chiffrer les messages électroniques sortants et supprimer le chiffrement des messages chiffrés provenant de votre organisation ou des réponses aux messages chiffrés envoyés à partir de votre organisation. Vous pouvez utiliser le centre d'administration Exchange ou Exchange Online PowerShell pour créer ces règles. En plus des règles de chiffrement globales, vous pouvez également choisir d'activer ou de désactiver les options de chiffrement de messages individuelles pour les utilisateurs finaux.

||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins. |
||

Si vous avez récemment migré d'AD RMS vers Azure information protection, vous devrez passer en revue vos règles de flux de messagerie existantes pour vous assurer qu'elles continuent de fonctionner dans votre nouvel environnement. Par ailleurs, si vous souhaitez tirer parti des nouvelles fonctionnalités de chiffrement de messages Office 365 (OME) à l'aide d'Azure information protection, vous devez mettre à jour vos règles de flux de messagerie existantes. Dans le cas contraire, vos utilisateurs continueront à recevoir des messages chiffrés qui utilise le format de pièce jointe HTML précédent au lieu de la nouvelle expérience OME transparente. Si vous n'avez pas encore configuré OME, reportez-vous à la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md) pour obtenir des informations.

Pour plus d'informations sur les composants qui composent les règles de flux de messagerie et le fonctionnement des règles de flux de messagerie, consultez la rubrique [mail Flow Rules (transport Rules) in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules). Pour plus d'informations sur le fonctionnement des règles de flux de messagerie avec Azure information protection, consultez la rubrique [Configuration des règles de flux de messagerie Exchange Online pour les étiquettes Azure information protection](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).

> [!IMPORTANT]
> Pour les environnements Exchange hybrides, les utilisateurs locaux peuvent envoyer des messages chiffrés à l'aide de OME uniquement si les messages électroniques sont acheminés via Exchange Online. Pour configurer OME dans un environnement hybride Exchange, vous devez d'abord [configurer le déploiement hybride à l'aide de l'Assistant Configuration hybride](https://docs.microsoft.com/Exchange/exchange-hybrid) , puis [configurer le courrier pour qu'il passe de votre serveur de messagerie vers Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365). Une fois que vous avez configuré le flux de messagerie dans Office 365, vous pouvez configurer des règles de flux de messagerie pour OME en utilisant ces instructions.

## <a name="create-mail-flow-rules-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>Créer des règles de flux de messagerie pour chiffrer les messages électroniques avec les nouvelles fonctionnalités de OME

Vous pouvez définir des règles de flux de messagerie pour déclencher le chiffrement des messages avec les nouvelles fonctionnalités de OME à l'aide du centre d'administration Exchange.

### <a name="use-the-eac-to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities"></a>Utiliser le centre d'administration Exchange pour créer une règle de chiffrement des messages électroniques avec les nouvelles fonctionnalités OME

1. Dans un navigateur Web, à l'aide d'un compte professionnel ou scolaire auquel des autorisations d'administrateur général ont été accordées, [Connectez-vous à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Sélectionnez la vignette **admin** .

3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.

4. Dans le centre d'administration Exchange, accédez à **règles** de **flux** \> de messagerie et sélectionnez **nouvelle** ![icône](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **créer une nouvelle règle**. Pour plus d'informations sur l'utilisation du centre d'administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Dans **nom**, tapez un nom pour la règle, tel que chiffrer le courrier pour DrToniRamos@hotmail.com.

6. Dans l’option **Appliquer cette règle si**, sélectionnez une condition, puis entrez une valeur si nécessaire. Par exemple, pour chiffrer les messages adressés à DrToniRamos@hotmail.com :

   1. Dans **Appliquer cette règle si**, sélectionnez **le destinataire est**.

   2. Choisissez un nom existant dans la liste de contacts ou entrez une nouvelle adresse de messagerie dans la zone **vérifier les noms**.

      - Pour sélectionner un nom existant, sélectionnez-le dans la liste et cliquez sur **OK**.

      - Pour entrer un nouveau nom, tapez une adresse de messagerie dans la zone **vérifier les noms** , puis sélectionnez **vérifier les noms** \> **OK**.

7. Pour ajouter d'autres conditions, cliquez sur **autres options** , puis sur **Ajouter une condition** et sélectionnez dans la liste.

   Par exemple, pour appliquer la règle uniquement si le destinataire se trouve en dehors de votre organisation, sélectionnez Ajouter une **condition** , puis sélectionnez **le destinataire est externe/interne** \> à **l'extérieur de l'organisation** \> ****.

8. Pour activer le chiffrement à l'aide des nouvelles fonctionnalités OME, dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité des messages** , puis appliquer le chiffrement de **messages Office 365 et protection des droits**. Sélectionnez un modèle RMS dans la liste, cliquez sur **Enregistrer**, puis choisissez **OK**.
  
  La liste des modèles inclut tous les modèles et options par défaut, ainsi que tous les modèles personnalisés que vous avez créés pour être utilisés par Office 365. Si la liste est vide, vérifiez que vous avez configuré le chiffrement de messages Office 365 avec les nouvelles fonctionnalités, comme décrit dans la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md). Pour plus d'informations sur les modèles par défaut, reportez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d'informations sur l'option **ne pas transférer** , reportez-vous à l' [option ne pas transférer pour les messages électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Pour plus d'informations sur l'option **chiffrer uniquement** , reportez-vous à la rubrique [chiffrer uniquement](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

  Vous pouvez choisir **Ajouter une action** si vous souhaitez spécifier une autre action.

### <a name="use-the-eac-to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities"></a>Utiliser le centre d'administration Exchange pour mettre à jour une règle de flux de messagerie existante afin d'utiliser les nouvelles fonctionnalités OME

1. Dans un navigateur Web, à l'aide d'un compte professionnel ou scolaire auquel des autorisations d'administrateur général ont été accordées, [Connectez-vous à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Sélectionnez la vignette **admin** .

3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.

4. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.

5. Dans la liste des règles de flux de messagerie, sélectionnez la règle que vous souhaitez modifier afin d'utiliser les nouvelles fonctionnalités de **** ![OME, puis](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)cliquez sur modifier l'icône modifier.

6. Pour activer le chiffrement à l'aide des nouvelles fonctionnalités OME, dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité des messages** , puis appliquer le chiffrement de **messages Office 365 et protection des droits**. Sélectionnez un modèle RMS dans la liste, choisissez **Enregistrer** , puis **OK**.

   La liste des modèles inclut tous les modèles et options par défaut, ainsi que tous les modèles personnalisés que vous avez créés pour être utilisés par Office 365. Si la liste est vide, vérifiez que vous avez configuré le chiffrement de messages Office 365 avec les nouvelles fonctionnalités, comme décrit dans la rubrique [set up New Office 365 message Encryption Capabilities Built-Top of Azure information protection](set-up-new-message-encryption-capabilities.md). Pour plus d'informations sur les modèles par défaut, reportez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d'informations sur l'option **ne pas transférer** , reportez-vous à l' [option ne pas transférer pour les messages électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Pour plus d'informations sur l'option **chiffrer uniquement** , reportez-vous à la rubrique [chiffrer uniquement](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

   Vous pouvez choisir **Ajouter une action** si vous souhaitez spécifier une autre action.

7. Dans la liste **procédez comme suit** , supprimez toutes les actions qui sont affectées pour **modifier la sécurité** \> **des messages appliquer la version précédente de OME**.

8. Sélectionnez **Save (Enregistrer)**.

## <a name="create-mail-flow-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>Créer des règles de flux de messagerie pour le chiffrement de messages Office 365 sans les nouvelles fonctionnalités

Si vous n'avez pas encore déplacé votre organisation Office 365 vers les nouvelles fonctionnalités OME, utilisez ces tâches pour définir des règles de flux de messagerie afin de chiffrer les messages pour votre organisation. Microsoft vous recommande de planifier la migration vers les nouvelles fonctionnalités de OME dès que cela est raisonnable pour votre organisation. Pour obtenir des instructions, consultez la rubrique [set up New Office 365 message Encryption Capabilities Built-Top of Azure information protection](set-up-new-message-encryption-capabilities.md).

### <a name="use-the-eac-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a>Utiliser le centre d'administration Exchange pour créer une règle de flux de messagerie pour le chiffrement des messages électroniques sans les nouvelles fonctionnalités OME

1. Dans un navigateur Web, à l'aide d'un compte professionnel ou scolaire auquel des autorisations d'administrateur général ont été accordées, [Connectez-vous à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Sélectionnez la vignette **admin** .

3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.

4. Dans le centre d'administration Exchange, accédez à **règles** de **flux** \> de messagerie et sélectionnez **nouvelle** ![icône](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **créer une nouvelle règle**. Pour plus d'informations sur l'utilisation du centre d'administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Dans **nom**, tapez un nom pour la règle, tel que chiffrer le courrier pour DrToniRamos@hotmail.com.

6. Dans l’option **Appliquer cette règle si**, sélectionnez une condition, puis entrez une valeur si nécessaire. Par exemple, pour chiffrer les messages adressés à DrToniRamos@hotmail.com :

   1. Dans **Appliquer cette règle si**, sélectionnez **le destinataire est**.

   2. Choisissez un nom existant dans la liste de contacts ou entrez une nouvelle adresse de messagerie dans la zone **vérifier les noms**.

      - Pour sélectionner un nom existant, sélectionnez-le dans la liste et cliquez sur **OK**.

      - Pour entrer un nouveau nom, tapez une adresse de messagerie dans la zone **vérifier les noms** , puis sélectionnez **vérifier les noms** \> **OK**.

7. Pour ajouter d'autres conditions, sélectionnez **plus d'options** , puis ajouter une **condition** et sélectionnez-la dans la liste.

   Par exemple, pour appliquer la règle uniquement si le destinataire se trouve en dehors de votre organisation, sélectionnez Ajouter une **condition** , puis sélectionnez **le destinataire est externe/interne** \> à **l'extérieur de l'organisation** \> ****.

8. Pour activer le chiffrement sans utiliser les nouvelles fonctionnalités de OME, dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité** \> **des messages appliquer la version précédente de OME**, puis choisissez **Enregistrer**.

  Si vous recevez une erreur indiquant que les licences IRM ne sont pas activées, vous n'avez pas encore configuré OME pour votre organisation. Si vous souhaitez configurer OME maintenant, vous devez le configurer pour qu'il utilise les nouvelles fonctionnalités de OME. Pour plus d'informations, reportez-vous à la rubrique [set up New Office 365 message Encryption Capabilities Built-Top of Azure information protection](set-up-new-message-encryption-capabilities.md). Microsoft ne prend plus en charge la configuration de nouveaux déploiements de OME sans les nouvelles fonctionnalités.

  Vous pouvez choisir **Ajouter une action** si vous souhaitez spécifier une autre action.

### <a name="use-exchange-online-powershell-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a>Utiliser Exchange Online PowerShell pour créer une règle de flux de messagerie pour le chiffrement des messages électroniques sans les nouvelles fonctionnalités OME

1. Connectez-vous à Exchange Online PowerShell. Pour plus d'informations, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

2. Créez une règle à l'aide de la cmdlet **New-TransportRule** et __ définissez le paramètre `$true`ApplyOME sur.

   Cet exemple requiert que tous les messages électroniques envoyés à DrToniRamos@hotmail.com doivent être chiffrés.

   ```powershell
   New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
   ```

   **Remarques** :

   - Le nom unique de la nouvelle règle est «chiffrer la règle pour Dr toni Ramos».

   - Le paramètre _SentTo_ spécifie les destinataires des messages (identifiés par nom, adresse de messagerie, nom unique, etc.). Dans cet exemple, le destinataire est identifié par l'adresse de messagerie «DrToniRamos@hotmail.com».

   - Le paramètre _SentToScope_ spécifie l'emplacement des destinataires du message. Dans cet exemple, la boîte aux lettres du destinataire est dans Hotmail et ne fait pas partie de l'organisation Office 365, `NotInOrganization` la valeur est donc utilisée.

   Pour accéder à la syntaxe détaillée et aux informations relatives aux paramètres, voir [Nouvelle-RègleTransport](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).

### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Supprimer le chiffrement des réponses de messagerie chiffrées sans les nouvelles fonctionnalités OME

Lorsque vos utilisateurs de messagerie envoient des messages chiffrés, les destinataires de ces messages peuvent répondre avec des réponses chiffrées. Vous pouvez créer des règles de flux de messagerie pour supprimer automatiquement le chiffrement des réponses afin que les utilisateurs de messagerie de votre organisation n'aient pas à se connecter au portail de chiffrement pour les afficher. Vous pouvez utiliser les applets de commande du centre d'administration Exchange ou de Windows PowerShell pour définir ces règles. Si vous n'utilisez pas encore les nouvelles fonctionnalités de OME, vous pouvez uniquement déchiffrer les messages qui sont envoyés à partir de votre organisation ou les messages qui sont des réponses aux messages envoyés à partir de votre organisation. Vous ne pouvez pas déchiffrer les messages chiffrés provenant de l'extérieur de votre organisation.

#### <a name="use-the-eac-to-create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Utiliser le centre d'administration Exchange pour créer une règle de suppression du chiffrement des réponses de messagerie chiffrées sans les nouvelles fonctionnalités OME

1. Dans un navigateur Web, à l'aide d'un compte professionnel ou scolaire auquel des autorisations d'administrateur ont été accordées, [Connectez-vous à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Sélectionnez la vignette **admin** .

3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.

4. Dans le centre d'administration Exchange, accédez à **règles** de **flux** \> de messagerie et sélectionnez **nouvelle** ![icône](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **créer une nouvelle règle**. Pour plus d'informations sur l'utilisation du centre d'administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Dans **nom**, tapez le nom de la règle, par exemple supprimer le chiffrement du courrier entrant.

6. Dans **appliquer cette règle, si** sélectionnez les conditions où le chiffrement doit être supprimé des messages, comme **le destinataire se trouve** \> **à l'intérieur de l'organisation**.

7. Dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité** \> **des messages pour supprimer la version précédente de OME**.

8. Sélectionnez **Enregistrer**.

#### <a name="use-exchange-online-powershell-to-create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Utiliser Exchange Online PowerShell pour créer une règle afin de supprimer le chiffrement des réponses de messagerie chiffrées sans les nouvelles fonctionnalités OME

1. Connectez-vous à Exchange Online PowerShell. Pour plus d'informations, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

2. Créez une règle à l'aide de la cmdlet **New-TransportRule** et __ définissez le paramètre `$true`RemoveOME sur.

   Cet exemple supprime le chiffrement de tous les messages envoyés à des destinataires dans l'organisation Office 365.

   ```powershell
   New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
   ```

   **Remarques** :

   - Le nom unique de la nouvelle règle est «supprimer le chiffrement du courrier entrant».

   - Le paramètre _SentToScope_ spécifie l'emplacement des destinataires du message. Dans cet exemple, la valeur `InOrganization` value est utilisée, ce qui indique:

     - Le destinataire est une boîte aux lettres, un utilisateur de messagerie, un groupe ou un dossier public à extension messagerie au sein de votre organisation.

       ou

     - L'adresse de messagerie du destinataire est dans un domaine accepté configuré comme un domaine faisant autorité ou un domaine de relais interne dans votre organisation, _et_ le message a été envoyé ou reçu via une connexion authentifiée.

Pour accéder à la syntaxe détaillée et aux informations relatives aux paramètres, voir [Nouvelle-RègleTransport](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).

## <a name="related-topics"></a>Voir aussi

[Chiffrement dans Office 365](encryption.md)

[Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365](set-up-new-message-encryption-capabilities.md)

[Ajouter une personnalisation aux messages chiffrés](add-your-organization-brand-to-encrypted-messages.md)

[Règles de flux de messagerie (règles de transport) dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=506707)

[Règles de flux de messagerie (règles de transport) dans Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=506708)
