---
title: Création de listes d’expéditeurs bloqués et autorisés à l’échelle de l’organisation dans Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/8/2015
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150s
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: Si vous souhaitez être sûr de recevoir des messages d’un expéditeur particulier, étant donné que vous les approuvez et leurs messages, vous pouvez ajuster votre liste verte dans une stratégie de filtrage du courrier indésirable dans le centre d’administration Exchange.
ms.openlocfilehash: 4731fe4a72a3c331725b82e09240e6af91bb6afd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153726"
---
# <a name="create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365"></a>Création de listes d’expéditeurs bloqués et autorisés à l’échelle de l’organisation dans Office 365
  
Si vous voulez être sûr de bien recevoir les e-mails provenant d'un expéditeur précis, car vous faites confiance à cet expéditeur et à ses messages, vous pouvez ajuster votre liste verte dans une stratégie de filtrage du courrier indésirable dans le Centre d'administration Exchange (CAE) : **Protection** \> **Filtre anti-spam**. Pour en savoir plus, consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Une autre option consisterait à créer une règle de flux de messagerie Exchange (également appelée règle de transport) qui fonctionne comme la liste d’autorisation basée sur le domaine ou l’utilisateur dans le filtre de courrier indésirable. Vous pouvez bloquer les messages envoyés par un domaine ou un utilisateur particulier de la même manière.
  
Une règle de flux de messagerie est utile dans ce cas si vous devez filtrer des critères complexes, tels que la vérification des en-têtes de message ou les noms de pièces jointes, ou si vous souhaitez ajouter des actions complexes telles que l’ajout d’une clause d’exclusion de responsabilité au message ou l’application d’une période de temps pendant laquelle le RUL e est actif. Cependant, pour vous assurer que les e-mails d'un expéditeur spécifique ou d'un domaine contournent votre filtre anti-spam, nous vous recommandons de les ajouter à votre stratégie de filtrage du courrier indésirable. Pour cela, accédez au CAE dans **Protection** \> **Filtre anti-spam**. Pour plus d'informations, consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
  
> [!TIP]
> Une liste basée sur un domaine dans une règle de flux de messagerie n’est pas aussi sécurisée qu’une liste basée sur l’adresse IP, car les domaines peuvent être falsifiés. En outre, si l'adresse IP d'envoi est sur une liste rouge, elle sera toujours bloquée, même si le filtrage pour le domaine ou l'utilisateur est ignoré. Cela est dû au fait qu’une règle de flux de messagerie sur un domaine ou un utilisateur ne remplace pas la liste d’adresses IP bloquées. Nous vous recommandons d'utiliser une liste fondée sur l'adresse IP autant que possible. Pour créer une liste fondée sur l'adresse IP, vous pouvez utiliser la liste verte IP ou la liste rouge IP dans le filtre des connexions. Aucun des messages envoyés à partir de ces adresses IP n'est vérifié par le filtre de contenu. Pour savoir comment configurer la stratégie du filtre de connexion en ajoutant des adresses IP à la liste verte IP ou à la liste rouge IP, consultez la rubrique [Configuration de la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md). 
  
Pour les autres tâches de gestion relatives aux règles de flux de messagerie, consultez la rubrique [mail Flow Rules (transport Rules) in Exchange Online](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
## <a name="use-the-eac-to-customize-a-block-or-allow-list-to-prevent-or-receive-email-from-a-domain-or-user"></a>Personnaliser un bloc ou une liste verte pour bloquer ou recevoir des e-mails provenant d'un domaine ou d'un utilisateur avec le CAE

1. Dans le CAE, accédez à **Protection** \> **Filtre anti-spam**. 
    
2. Sur la page **Général**, effectuez l'une des opérations suivantes : 
    
  - Double-cliquez sur la stratégie par défaut ou une stratégie existante pour la modifier.
    
  - Cliquez sur **Nouveau** pour créer une stratégie personnalisée de filtrage du courrier indésirable à appliquer à des utilisateurs, des groupes et des domaines au sein de votre organisation. 
    
3. Sur la page **Listes vertes**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours remises dans la boîte de réception. Les e-mails provenant de ces entrées ne sont pas traités par le filtre anti-spam. Effectuez l'une des actions suivantes : 
    
  - Ajoutez des expéditeurs approuvés à la liste des expéditeurs autorisés. Cliquez sur **Ajouter**, puis ajoutez les adresses des expéditeurs à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur OK pour revenir à la page **Listes vertes**. 
    
  - Ajoutez des domaines approuvés à la liste de domaines autorisés. Cliquez sur **Ajouter**, puis ajoutez les domaines à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur OK pour revenir à la page **Listes vertes**. 
    
    > [!CAUTION]
    > Si vous autorisez des domaines de niveau supérieur, le courrier électronique indésirable sera probablement remis dans une boîte de réception. 
  
4. Dans la page **Listes rouges**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours marquées comme courrier indésirable. Le service applique l'action configurée de courrier indésirable à probabilité élevée sur le courrier électronique correspondant à ces entrées. 
    
  - Ajoutez des expéditeurs indésirables à la liste de blocage des expéditeurs. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les adresses des expéditeurs à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**. 
    
  - Ajoutez des domaines indésirables à la liste des domaines bloqués. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les domaines à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**. 
    
    > [!CAUTION]
    > Si vous bloquez des domaines de niveau supérieur, il est probable que le courrier électronique que vous souhaitez recevoir soit marqué comme courrier indésirable. 
  
## <a name="what-do-you-need-to-know-before-you-begin-creating-a-mail-flow-rule"></a>Que devez-vous savoir avant de commencer à créer une règle de flux de messagerie?
    
- Vous n’avez pas besoin de créer une règle de flux de messagerie pour contourner le filtrage du courrier indésirable ou marquer le courrier comme courrier indésirable pour un expéditeur ou un domaine. Utilisez les listes bloquer Exchange Online Protection et autoriser dans une stratégie de courrier indésirable au lieu de cette règle de flux de messagerie si vous voulez simplement bloquer ou autoriser un expéditeur ou un domaine spécifique et ne pas joindre de conditions supplémentaires. Pour en savoir plus, consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
    
- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l’entrée «règles de flux de messagerie» dans la rubrique [stratégie de messagerie et autorisations de conformité](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) . 
    
- Pour obtenir des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, reportez-vous à l’article **Raccourcis clavier dans le Centre d’administration Exchange**.
    
> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l’aide en participant aux forums Exchange. Visitez les forums sur [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542)ou [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-bypass-spam-filtering-for-a-domain-or-user"></a>Utiliser le centre d’administration Exchange pour créer une règle de flux de messagerie pour contourner le filtrage du courrier indésirable pour un domaine ou un utilisateur

1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**. Choisissez **Ajouter** ![une icône](media/ITPro-EAC-AddIcon.gif) ajouter, puis **ignorer le filtrage du courrier**indésirable.
    
2. Attribuez un nom à la règle. Sous **Appliquer cette règle si**, choisissez **L'expéditauer**, puis sélectionnez l'une des conditions suivantes : 
    
  - Si vous voulez spécifier un domaine, choisissez **le domaine est**. Dans la boîte de dialogue **Spécifier un domaine**, entrez le domaine de l'expéditeur que vous voulez désigner comme étant sûr, par exemple contoso.com. **Ajouter** ![Icône](media/ITPro-EAC-AddIcon.gif) ajouter pour le déplacer vers la liste des expressions. Répétez cette étape pour ajouter d'autres domaines, puis cliquez sur **OK** lorsque vous avez terminé. 
    
  - Si vous voulez spécifier un utilisateur, choisissez **est cette personne**. Dans la boîte de dialogue **Sélectionner les membres**, ajoutez l'utilisateur à partir de la liste ou saisissez son nom et cliquez sur **Vérifier les noms**. Répétez cette étape pour ajouter d'autres utilisateurs, puis cliquez sur **OK** lorsque vous avez terminé. 
    
3. Nous vous recommandons de cocher la case **Arrêter de traiter plus de règles** pour vous assurer qu'aucune autre règle ne peut inverser l'action de contournement. 
    
4. Pour l'option **Correspondance avec l'adresse de l'expéditeur dans le message**, sélectionnez **En-tête ou enveloppe**.
    
5. Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer, tester et activer la règle sur une période spécifique, etc.
    
6. Cliquez sur **Enregistrer** pour enregistrer la règle. 
    
Une fois la règle créée et appliquée, le filtrage du courrier indésirable est contourné pour le domaine ou l'utilisateur spécifié.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-that-blocks-messages-sent-from-a-domain-or-user"></a>Utiliser le centre d’administration Exchange pour créer une règle de flux de messagerie qui bloque les messages envoyés par un domaine ou un utilisateur

1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**. Sélectionnez **Ajouter** ![une icône](media/ITPro-EAC-AddIcon.gif) ajouter, puis **créer une nouvelle règle**.
    
2. Nommez la règle, puis cliquez sur **Autres options**. 
    
3. Sous **Appliquer cette règle si**, choisissez **L'expéditauer**, puis sélectionnez l'une des conditions suivantes : 
    
  - Si vous voulez spécifier un domaine, choisissez **le domaine est**. Dans la boîte de dialogue Spécifier un domaine, entrez le domaine de l'expéditeur des messages que vous souhaitez bloquer, par exemple contoso.com. Cliquez sur **Ajouter** ![une](media/ITPro-EAC-AddIcon.gif) icône pour le déplacer vers la liste des expressions. Répétez cette étape pour ajouter d'autres domaines, puis cliquez sur **OK** lorsque vous avez terminé. 
    
  - Si vous voulez spécifier un utilisateur, choisissez **est cette personne**. Dans la boîte de dialogue **Sélectionner les membres**, ajoutez l'utilisateur à partir de la liste ou saisissez son nom et cliquez sur **Vérifier les noms**. Répétez cette étape pour ajouter d'autres utilisateurs, puis cliquez sur **OK** lorsque vous avez terminé. 
    
4. Sous **Effectuer les opérations suivantes**, sélectionnez **Bloquer le message**, puis cliquez sur l'une des autres options telles que **Supprimer le message sans avertir personne**.
    
5. Cliquez sur **Plus d'options**, puis, pour l'option **Correspondance avec l'adresse de l'expéditeur dans le message**, sélectionnez **En-tête ou enveloppe**.
    
6. Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer, tester et activer la règle sur une période spécifique, etc. Nous vous recommandons de tester la règle pendant un certain temps avant de l'appliquer dans votre organisation.
    
7. Cliquez sur **Enregistrer** pour enregistrer la règle. 
    
Une fois la règle créée et appliquée, tous les messages envoyés à partir du domaine ou par l'utilisateur spécifié seront bloqués.
  
## <a name="see-also"></a>Voir aussi

[Configurer vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
[Utiliser les règles de flux de messagerie pour configurer le filtrage du courrier en nombre](use-transport-rules-to-configure-bulk-email-filtering.md)

