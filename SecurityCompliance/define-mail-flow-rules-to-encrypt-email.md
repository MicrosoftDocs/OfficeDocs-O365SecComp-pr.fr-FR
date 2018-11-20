---
title: Définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
description: En tant qu’administrateur global Office 365, vous pouvez créer des règles de flux pour activer Office 365 Message de chiffrement de messagerie. Vous pouvez chiffrer tous les messages électroniques sortants et supprimer le chiffrement des messages internes ou à partir des réponses aux messages chiffrés envoyés depuis votre organisation.
ms.openlocfilehash: 0ed112e216060cdd56afa2dfd08cdebd5740621d
ms.sourcegitcommit: d7e87ce4b1579ac47af2e853ef59ef058c40191f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/16/2018
ms.locfileid: "26547266"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365

En tant qu’administrateur global Office 365, vous pouvez créer des règles de flux de messagerie, également connu sous les règles de transport, pour protéger les messages électroniques envoyés et reçus. Vous pouvez définir des règles pour chiffrer les messages électroniques sortants et supprimer le chiffrement de messages chiffrés en provenance de l’intérieur de votre organisation ou de réponses aux messages chiffrés envoyés à partir de votre organisation. Vous pouvez utiliser le centre d’administration Exchange (EAC) ou les applets de commande Windows PowerShell pour Exchange Online pour créer ces règles.  En plus des règles de chiffrement globale, vous pouvez également choisir d’activer ou désactiver les options de chiffrement de message en particulier pour les utilisateurs finaux.
  
Si vous avez récemment migré à partir d’AD RMS pour la Protection des informations Azure, vous devrez consulter vos règles de flux de messagerie existante pour vous assurer qu’ils continuent à fonctionner dans votre nouvel environnement. En outre, si vous souhaitez tirer parti des nouvelles fonctionnalités d’Office 365 Message de chiffrement disponibles pour vous par le biais de la Protection des informations Azure, vous devez mettre à jour vos règles de flux de messagerie existante. Dans le cas contraire, vos utilisateurs continueront à recevoir des messages chiffrés qui utilise le format de pièce jointe HTML précédent au lieu de la nouvelle expérience OME transparent. Si vous n’avez pas configuré OME encore, voir [configurer les nouvelles fonctionnalités d’Office 365 Message Encryption greffées sur la Protection des informations Azure](set-up-new-message-encryption-capabilities.md) pour plus d’informations. 
  
Pour plus d’informations sur les composants qui constituent des règles de flux de messagerie et de la façon dont des règles de flux de messagerie, consultez la rubrique [règles de flux (règles de transport) de messagerie dans Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules). Pour plus d’informations sur le fonctionnement des règles de flux de messagerie avec Azure la Protection des informations, voir [configuration d’Exchange Online règles de flux de messagerie pour les étiquettes de Protection des informations Azure](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).
  
> [!IMPORTANT]
> Pour les environnements Exchange hybride, les utilisateurs locaux peuvent envoyer des messages chiffrés à l’aide d’OME uniquement si le courrier est routé via Exchange Online. Pour configurer les OME dans un environnement d’Exchange hybride, vous devez la première [configuration hybride à l’aide de l’Assistant Configuration hybride](https://docs.microsoft.com/Exchange/exchange-hybrid) , puis [configurer la messagerie pour transmettre à partir de votre serveur de messagerie vers Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365). Une fois que vous avez configurée courrier passe par Office 365, vous pouvez ensuite configurer les règles de flux de messagerie pour OME à l’aide de ce guide.

## <a name="create-a-mail-flow-rule-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>Créer une règle de flux de messagerie pour chiffrer les messages électroniques avec les nouvelles fonctionnalités OME

Vous pouvez définir des règles de flux de messagerie pour déclencher le chiffrement des messages avec les nouvelles fonctionnalités OME à l’aide du centre d’administration Exchange.
  
### <a name="to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities-by-using-the-eac"></a>Pour créer une règle pour le chiffrement des messages électroniques avec les nouvelles fonctionnalités OME à l’aide du CAE

1. Dans un navigateur web, avec un compte professionnel ou de l’école bénéficie des autorisations d’administrateur global, [se connecter à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Choisissez la vignette de **l’administrateur** . 
    
3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.
    
4. Dans le CAE, accédez à **flux de messagerie** \> **règles** \> ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) ( **Nouveau**) \> **créer une nouvelle règle**. Pour plus d’informations sur l’utilisation du centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).
    
5. Dans **nom**, tapez un nom pour la règle, comme Encrypt mail for DrToniRamos@hotmail.com.
    
6. Dans l’option **Appliquer cette règle si**, sélectionnez une condition, puis entrez une valeur si nécessaire. Par exemple, pour chiffrer les messages adressés à DrToniRamos@hotmail.com :

  1. Dans **Appliquer cette règle si**, sélectionnez **le destinataire est**.

  2. Choisissez un nom existant dans la liste de contacts ou entrez une nouvelle adresse de messagerie dans la zone **vérifier les noms**. 
    
    Pour sélectionner un nom existant, sélectionnez-le dans la liste et cliquez sur **OK**.
    
    Pour entrer un nouveau nom, tapez une adresse de messagerie dans la zone **vérifier les noms** puis sélectionnez **vérifier les noms** \> **OK**.
    
7. Pour ajouter d’autres conditions, cliquez sur **plus d’options** et choisissez **Ajouter une condition** et sélectionnez dans la liste. 
    
  Par exemple, pour appliquer la règle uniquement si le destinataire se situe en dehors de votre organisation, sélectionnez **Ajouter une condition** et puis sélectionnez **le destinataire est interne/externe** \> **en dehors de l’organisation** \> **OK**.
    
8. Pour activer le chiffrement à l’aide des nouvelles fonctionnalités OME, **procédez comme suit**, sélectionnez **Modifier la sécurité des messages** , puis choisissez **Appliquer le chiffrement de messages Office 365 et de protection par des droits**. Sélectionnez un modèle RMS à partir de la liste, cliquez sur **Enregistrer**, puis cliquez sur **OK**.
    
  La liste des modèles inclut tous les modèles par défaut et les options, ainsi que des modèles personnalisés que vous avez créé pour utilisent par Office 365. Si la liste est vide, assurez-vous que vous avez configuré le chiffrement de messages Office 365 avec les nouvelles fonctionnalités comme décrit dans [configurer les nouvelles fonctionnalités d’Office 365 Message Encryption basées sur Azure de Protection des informations](set-up-new-message-encryption-capabilities.md). Pour plus d’informations sur les modèles par défaut, voir [configuration et gestion des modèles pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d’informations sur l’option **Ne pas transférer** , voir [l’option ne pas transférer les messages électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Pour plus d’informations sur l’option **chiffrer uniquement** , voir [option chiffrer uniquement pour les courriers électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).
    
    Vous pouvez choisir **d’Ajouter une action** si vous souhaitez spécifier une autre action. 
    
### <a name="to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities-by-using-the-eac"></a>Pour mettre à jour une règle de flux de messagerie existante pour utiliser les nouvelles fonctionnalités OME à l’aide du CAE

1. Dans un navigateur web, avec un compte professionnel ou de l’école bénéficie des autorisations d’administrateur global, [se connecter à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Choisissez la vignette de **l’administrateur** . 
    
3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.
    
4. Dans le CAE, accédez à **flux de messagerie** \> **règles**.
    
5. Dans la liste des règles de flux de messagerie, sélectionnez la règle que vous souhaitez modifier pour utiliser les nouvelles fonctionnalités OME, puis choisissez ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) ( **Modifier**).
    
6. Pour activer le chiffrement à l’aide des nouvelles fonctionnalités OME, **procédez comme suit**, choisissez **Modifier la sécurité des messages** , puis **Appliquer le chiffrement de messages Office 365 et de protection par des droits**. Sélectionnez un modèle RMS à partir de la liste, cliquez sur **Enregistrer** , puis choisissez **OK**.
    
    La liste des modèles inclut tous les modèles par défaut et les options, ainsi que des modèles personnalisés que vous avez créé pour utilisent par Office 365. Si la liste est vide, assurez-vous que vous avez configuré le chiffrement de messages Office 365 avec les nouvelles fonctionnalités comme décrit dans [configurer les nouvelles fonctionnalités d’Office 365 Message Encryption basées sur Azure de Protection des informations](set-up-new-message-encryption-capabilities.md). Pour plus d’informations sur les modèles par défaut, voir [configuration et gestion des modèles pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d’informations sur l’option **Ne pas transférer** , voir [l’option ne pas transférer les messages électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Pour plus d’informations sur l’option **chiffrer uniquement** , voir [option chiffrer uniquement pour les courriers électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).
    
    Vous pouvez choisir **d’Ajouter une action** si vous souhaitez spécifier une autre action. 
    
7. Dans la liste **effectuer les opérations suivantes** , supprimez toutes les actions qui sont associées à **Modifier la sécurité des messages** \> **Appliquer la version précédente d’OME**.
    
8. Sélectionnez **Save (Enregistrer)**.
    
## <a name="creating-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>Création de règles pour le chiffrement de messages Office 365 sans les nouvelles fonctionnalités

Si vous n’avez pas encore déplacé votre organisation Office 365 pour les nouvelles fonctionnalités OME, suivez ces étapes pour définir des règles de flux de messagerie pour chiffrer les messages pour votre organisation. Microsoft vous recommande de vous un plan pour la déplacer vers les nouvelles fonctionnalités OME dès que possible pour votre organisation. Pour plus d’informations, voir [configurer les nouvelles fonctionnalités d’Office 365 Message Encryption greffées Azure la Protection des informations](set-up-new-message-encryption-capabilities.md).
  
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-the-eac"></a>Pour créer une règle pour le chiffrement des messages électroniques sans les nouvelles fonctionnalités OME à l’aide du CAE

1. Dans un navigateur web, avec un compte professionnel ou de l’école bénéficie des autorisations d’administrateur global, [se connecter à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Choisissez la vignette de **l’administrateur** . 
    
3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.
    
4. Dans le CAE, accédez à **flux de messagerie** \> **règles** \> **+** ( **Nouveau**) \> **créer une nouvelle règle**. Pour plus d’informations sur l’utilisation du centre d’administration Exchange, consultez la rubrique [Exchange admin center dans Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).
    
5. Dans **nom**, tapez un nom pour la règle, comme Encrypt mail for DrToniRamos@hotmail.com.
    
6. Dans l’option **Appliquer cette règle si**, sélectionnez une condition, puis entrez une valeur si nécessaire. Par exemple, pour chiffrer les messages adressés à DrToniRamos@hotmail.com : 
    
  1. Dans **Appliquer cette règle si**, sélectionnez **le destinataire est**.
    
  2. Choisissez un nom existant dans la liste de contacts ou entrez une nouvelle adresse de messagerie dans la zone **vérifier les noms**. 
    
    - Pour sélectionner un nom existant, sélectionnez-le dans la liste et cliquez sur **OK**.
    
    - Pour entrer un nouveau nom, tapez une adresse de messagerie dans la zone **vérifier les noms** puis sélectionnez **vérifier les noms** \> **OK**.
    
  7. Pour ajouter d’autres conditions, cliquez sur **plus d’options** et puis sélectionnez **Ajouter une condition** et sélectionnez dans la liste. 
    
    Par exemple, pour appliquer la règle uniquement si le destinataire se situe en dehors de votre organisation, sélectionnez **Ajouter une condition** et puis sélectionnez **le destinataire est interne/externe** \> **en dehors de l’organisation** \> **OK**.
    
  8. Pour activer le chiffrement sans utiliser les nouvelles fonctionnalités OME, dans **effectuer les opérations suivantes**, sélectionnez **Modifier la sécurité des messages** \> **Appliquer la version précédente d’OME**, puis cliquez sur **Enregistrer**.
    
    Si vous recevez une erreur de licence IRM n’est pas activé, puis vous n’avez pas configuré OME pour votre organisation encore. Si vous souhaitez configurer maintenant OME, vous devez le configurer pour utiliser les nouvelles fonctionnalités d’OME. Pour plus d’informations, voir [configurer les nouvelles fonctionnalités d’Office 365 Message Encryption greffées Azure la Protection des informations](set-up-new-message-encryption-capabilities.md). Microsoft ne prend en charge que la configuration de nouveaux déploiements de OME sans les nouvelles fonctionnalités.
    
    Vous pouvez choisir **d’Ajouter une action** si vous souhaitez spécifier une autre action. 
    
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-windows-powershell-for-exchange-online"></a>Pour créer une règle pour le chiffrement des messages électroniques sans les nouvelles fonctionnalités OME à l’aide de Windows PowerShell pour Exchange Online

1. Connexion à Exchange Online PowerShell. Pour plus d’informations, consultez la rubrique [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).
    
2. Créer une règle à l’aide de l’applet de commande **New-TransportRule** et définissez le paramètre _ApplyOME_ sur `$true`.
    
Par exemple, pour exiger que tous les messages électroniques qui leur sont adressés DrToniRamos@hotmail.com doivent être chiffrées, tapez :
    
```
New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
```

Dans cet exemple :
    
- Le nom de la nouvelle règle est « Règle chiffrer pour Dr Toni Ramos ».
    
- Le paramètre _SentTo_ spécifie une condition de recherche pour les destinataires de messages électroniques. Vous pouvez utiliser n’importe quelle valeur qui identifie le destinataire, par exemple une adresse de messagerie, le nom, le nom unique (DN), l’etc.. Dans cet exemple, le destinataire est identifié par l’adresse de messagerie « DrToniRamos@hotmail.com ». 
    
- Le paramètre _SentToScope_ spécifie une condition de recherche pour l’emplacement des destinataires. Dans cet exemple, la boîte aux lettres du destinataire est Hotmail et ne fait pas partie de l’organisation Office 365, afin que la valeur « NotInOrganization » est utilisée. 
    
Pour plus d’informations sur les conditions que vous pouvez définir des règles de flux de messagerie à l’aide de cette applet de commande, voir [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).
    
### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Supprimer le chiffrement des réponses aux messages électroniques chiffrés sans les nouvelles fonctionnalités OME

Lorsque les utilisateurs de votre messagerie envoient des messages chiffrés, destinataires de ces messages peuvent répondre avec réponses chiffrés. Vous pouvez créer des messages pour supprimer automatiquement le chiffrement des réponses afin que les utilisateurs de messagerie dans votre organisation n’êtes pas obligé de se connecter au portail de chiffrement pour afficher les règles de flux. Vous pouvez utiliser les applets de commande Windows PowerShell ou de centre d’administration Exchange pour définir ces règles. Si vous n’utilisez pas encore les nouvelles fonctionnalités OME, vous pouvez uniquement déchiffrer des messages qui sont que soit envoyés depuis votre organisation ou des messages qui constituent des réponses aux messages envoyés à partir de votre organisation. Impossible de déchiffrer des messages chiffrés à partir d’origine à l’extérieur de votre organisation.
  
#### <a name="create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-the-eac"></a>Créer une règle de suppression du chiffrement des réponses aux messages électroniques chiffrés sans les nouvelles fonctionnalités OME à l’aide du CAE
<a name="DecryptruleEACNoNewOME"> </a>

1. Dans un navigateur web, à l’aide d’un compte qui dispose des autorisations d’administration, [se connecter à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)Professionnel ou de l’école.
    
2. Choisissez la vignette de **l’administrateur** . 
    
3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.
    
4. Dans le CAE, accédez à **flux de messagerie** \> **règles** \> **+** ( **Nouveau**) \> **créer une nouvelle règle**. Pour plus d’informations sur l’utilisation du centre d’administration Exchange, consultez la rubrique [Exchange admin center dans Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).
    
5. Dans **nom**, tapez un nom pour la règle, comme supprimer le chiffrement du courrier entrant.
    
6. Dans **appliquer cette règle si** , sélectionnez les conditions où chiffrement doit être supprimé des messages, tels que **le destinataire se situe** \> **à l’intérieur de l’organisation**.
    
7. Dans **effectuer les opérations suivantes**, sélectionnez **Modifier la sécurité des messages** \> **Supprimer la version précédente d’OME**.
    
8. Sélectionnez **Enregistrer**.
    
#### <a name="create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-exchange-online-powershell"></a>Créer une règle pour supprimer le chiffrement des réponses aux messages électroniques chiffrés sans les nouvelles fonctionnalités OME à l’aide d’Exchange Online PowerShell
<a name="DecryptrulePShellNoNewOME"> </a>

1. Connexion à Exchange Online PowerShell. Pour plus d’informations, consultez la rubrique [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).
    
2. Créer une règle à l’aide de l’applet de commande **New-TransportRule** et définissez le paramètre _RemoveOME_ sur `$true`.
    
Par exemple, pour supprimer le chiffrement de tous les messages envoyés aux destinataires de votre organisation Office 365, tapez :
    
```
New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
```

Dans cet exemple :

- Le nom de la nouvelle règle est « Remove encryption from incoming mail ».

- Le paramètre _SentToScope_ spécifie une condition de recherche pour l’emplacement des destinataires. Dans cet exemple, la valeur « InOrganization » est utilisée qui indique que : 

  - Le destinataire est une boîte aux lettres, un utilisateur de messagerie, un groupe ou un dossier public à extension messagerie dans votre organisation.

  ou

  - L'adresse de messagerie du destinataire se trouve dans un domaine accepté configuré en tant que domaine faisant autorité ou un domaine de relais interne, et le message a été envoyé ou reçu via une connexion authentifiée.
    
Pour plus d’informations sur les conditions que vous pouvez définir des règles de flux de messagerie à l’aide de cette applet de commande, voir [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).
    
## <a name="related-topics"></a>Voir aussi

[Chiffrement dans Office 365](encryption.md)
  
[Configurer les nouvelles fonctionnalités d’Office 365 Message Encryption greffées sur la Protection des informations Azure](set-up-new-message-encryption-capabilities.md)
  
[Ajouter une personnalisation aux messages chiffrés](add-your-organization-brand-to-encrypted-messages.md)
  
[Règles de flux de messagerie (règles de transport) dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=506707)
  
[Règles de flux de messagerie (règles de transport) dans Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=506708)
  

