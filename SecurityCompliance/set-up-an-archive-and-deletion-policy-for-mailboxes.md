---
title: Configurer une stratégie d’archivage et de suppression des boîtes aux lettres dans votre organisation Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
ms.assetid: ec3587e4-7b4a-40fb-8fb8-8aa05aeae2ce
description: Créer une stratégie d’archivage et de suppression dans Office 365 qui déplace automatiquement les éléments de boîte aux lettres d’archivage d’un utilisateur.
ms.openlocfilehash: 740164ee840a32aff20f5c2dc1b1ae433d95cfe5
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522295"
---
# <a name="set-up-an-archive-and-deletion-policy-for-mailboxes-in-your-office-365-organization"></a>Configurer une stratégie d’archivage et de suppression des boîtes aux lettres dans votre organisation Office 365

 **Cet article est destiné aux administrateurs. Vous souhaitez ajouter des stratégies d’archivage et de rétention aux éléments dans votre boîte aux lettres ? Voir [attribuer la stratégie de rétention pour les messages électroniques](https://support.office.com/article/3e5fd2dc-633f-4a38-b313-b31b81f7cf7a) | [stratégies de rétention et d’archivage dans Outlook sur le web pour les entreprises](https://support.office.com/article/465372e4-e16b-47db-bee0-aba44799085e)**
  
Dans Office 365, vous pouvez créer une stratégie d’archivage et de suppression qui déplace automatiquement les éléments de boîte aux lettres d’archivage d’un utilisateur et supprime automatiquement les éléments de la boîte aux lettres. Vous pouvez le faire en créant une stratégie de rétention qui ' s affectés aux boîtes aux lettres et déplace les éléments dans la boîte aux lettres de l’utilisateur archive après un certain temps et qui supprime également les éléments de la boîte aux lettres après avoir atteint une certaine limite d’âge. Les règles réels qui déterminent quels éléments sont déplacés ou supprimés et dans ce cas sont les balises de rétention appelée. Balises de rétention sont liés à une stratégie de rétention, qui à son tour est affectée à la boîte aux lettres d’un utilisateur. Une balise de rétention applique les paramètres de rétention des messages et des dossiers de boîte aux lettres d’un utilisateur. Il définit la durée pendant laquelle un message reste dans la boîte aux lettres et l’action entreprise lorsque le message atteint l’âge de rétention spécifié. Lorsqu’un message atteint sa âge de rétention, il est soit déplacé vers la boîte aux lettres de l’utilisateur archive ou elle est supprimée. 
  
Les étapes décrites dans cette rubrique seront définir une stratégie d’archivage et de rétention pour une entreprise fictive nommée Alpine House. Configuration de cette stratégie comprend les tâches suivantes :
  
- Activation d’une boîte aux lettres d’archive pour chaque utilisateur dans l’organisation. Cela permet aux utilisateurs de stockage de boîtes aux lettres d’ajout et est nécessaire afin qu’une stratégie de rétention peut déplacer les éléments vers la boîte aux lettres d’archive. Il également Imaginons une utilisateur banque d’archivage des informations par le déplacement d’éléments à leur boîte aux lettres d’archive. 
    
- Création de trois balises de rétention personnalisée qui effectuent les opérations suivantes : 
    
  - Déplace automatiquement les éléments qui sont de trois ans à la boîte aux lettres de l’utilisateur archive. Transférer les éléments dans la boîte aux lettres d’archive libère de l’espace dans la boîte aux lettres principale d’un utilisateur.
    
  - Supprime automatiquement les éléments qui ont 5 ans à partir du dossier éléments supprimés. Cela libère également l’espace dans la boîte aux lettres principale de l’utilisateur. L’utilisateur aura la possibilité de récupérer ces éléments si nécessaire. Voir la note de bas de page dans la section [informations supplémentaires](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) pour plus d’informations. 
    
  - Automatiquement (et définitivement) supprime les éléments qui sont 7 ans à partir de deux principal et boîte aux lettres d’archive. En raison des réglementations de conformité, d’une organisation est requises pour conserver le courrier électronique pour un certain temps. Une fois cette période expirée, une organisation souhaiterez peut-être supprimer définitivement les boîtes aux lettres utilisateur ces éléments. 
    
- Création d’une nouvelle stratégie de rétention et lui en ajoutant les nouvelles balises de rétention personnalisée. En outre, vous allez également ajouter des balises de rétention intégrée à la nouvelle stratégie de rétention. Cela inclut les balises personnelles que les utilisateurs peuvent attribuer aux éléments de boîte aux lettres. Vous allez également ajouter une balise de rétention qui déplace les éléments à partir du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur dans le dossier éléments récupérables dans leur boîte aux lettres d’archive. Ce vous permet de libérer de l’espace dans le dossier des éléments récupérables d’un utilisateur lorsque leur boîte aux lettres est mis en attente.
    
Vous pouvez suivre certaines ou toutes les étapes décrites dans cet article pour configurer une stratégie d’archivage et de suppression des boîtes aux lettres de votre organisation. Nous vous conseillons de tester ce processus sur quelques boîtes aux lettres avant l’implémentation de toutes les boîtes aux lettres dans votre organisation.
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être un administrateur global dans votre organisation Office 365 pour effectuer les étapes décrites dans cette rubrique. 
    
-  Lorsque vous créez un nouveau compte d’utilisateur dans Office 365 et attribuez une licence Exchange Online à l’utilisateur, une boîte aux lettres est automatiquement créée pour l’utilisateur. Lors de la création de la boîte aux lettres, il est automatiquement attribué une stratégie de rétention par défaut, appelée stratégie MRM par défaut. Dans cet article, vous créez une nouvelle stratégie de rétention et puis attribuez-le aux boîtes aux lettres utilisateur, en remplaçant la stratégie MRM par défaut. Une boîte aux lettres peut avoir qu’une seule stratégie de rétention qui lui est affectée à la fois.
    
- Pour en savoir plus sur les balises de rétention et les stratégies de rétention dans Exchange Online, voir [balises de rétention et stratégies de rétention](https://go.microsoft.com/fwlink/p/?LinkId=404424).
    
## <a name="step-1-enable-archive-mailboxes-for-users"></a>Étape 1 : Activer archive les boîtes aux lettres pour les utilisateurs

La première étape consiste à activer la boîte aux lettres d’archive pour chaque utilisateur dans votre organisation. Boîte aux lettres de l’utilisateur archive doit être activée afin qu’une balise de rétention avec une action de rétention « Déplacer vers une Archive » peut déplacer l’élément après que l’âge de rétention expire. 
  
> [!NOTE]
> Vous pouvez activer les boîtes aux lettres d’archive n’importe quel moment au cours de ce processus, simplement comme comme elles sont activées à un moment donné avant de terminer le processus. Si une boîte aux lettres d’archivage n’est pas activé, aucune action n’est effectuée sur tous les éléments qui ont une stratégie d’archivage qui lui est affectée. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte d’administrateur global.
    
    
3. Dans la sécurité &amp; centre de conformité, accédez à **la gouvernance des données** \> **Archive**.
    
    Une liste des boîtes aux lettres dans votre organisation s’affiche et indique si la boîte aux lettres d’archive correspondant est activé ou désactivé. 
    
4. Sélectionnez les boîtes aux lettres en cliquant sur le premier dans la liste, maintenez enfoncée la touche **MAJ enfoncée** , puis en cliquant sur la dernière occurrence dans la liste. 
    
    > [!TIP]
    > Cette étape suppose qu’aucune boîte aux lettres d’archivage n’est activées. Si vous avez des boîtes aux lettres avec l’archive activé, maintenez enfoncée la touche **CTRL enfoncée** et cliquez sur chaque boîte aux lettres qui a une boîte aux lettres d’archive désactivé. Ou vous pouvez cliquer sur l’en-tête de colonne de **boîte aux lettres d’Archive** pour trier les lignes selon si la boîte aux lettres d’archive est activée ou désactivée pour faciliter l’accès à sélectionner des boîtes aux lettres. 
  
5. Dans le volet de détails, sous **Modifier en bloc**, cliquez sur **Activer**.
    
    Un avertissement s’affiche indiquant que les éléments qui datent de plus de deux ans seront déplacées vers la nouvelle boîte aux lettres d’archive. Il s’agit de la stratégie de rétention par défaut qui a attribué une nouvelle boîte aux lettres de l’utilisateur lors de sa création ayant une balise de stratégie par défaut archive ayant un âge de rétention de 2 ans. La balise de stratégie par défaut archive personnalisé que vous créerez à l’étape 2 a un âge de rétention de 3 ans. Cela signifie que les éléments sont 3 ans ou antérieure seront déplacées vers la boîte aux lettres d’archive.
    
6. Cliquez sur **Oui** pour fermer le message d’avertissement et démarrer le processus pour activer la boîte aux lettres d’archive pour chaque boîte aux lettres sélectionnée. 
    
7. Le processus est terminé, cliquez sur **Actualiser** ![Actualiser](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) pour mettre à jour la liste dans la page **Archive** . 
    
    La boîte aux lettres d’archivage est activée pour tous les utilisateurs de votre organisation.
    
    ![La liste des boîtes aux lettres avec la boîte aux lettres d’archive activé](media/61a7cb97-1bed-4808-aa5f-b6b761cfa8de.png)
  
8. Laissez la sécurité &amp; ouvrir Centre de conformité. Vous allez utiliser dans l’étape suivante.
    
## <a name="step-2-create-new-retention-tags-for-the-archive-and-deletion-policies"></a>Étape 2 : Créer des balises de rétention nouvelle pour les stratégies d’archivage et de suppression

Dans cette étape, vous allez créer trois balises de rétention personnalisée qui ont été décrites précédemment.
  
- Alpine voie 3 ans déplacer vers l’Archive (stratégie d’archivage personnalisés)
    
- Alpine voie 7 année supprimer définitivement (stratégie de suppression personnalisées)
    
- Alpine voie supprimé éléments 5 ans supprimer et autoriser la récupération (balise personnalisée pour le dossier éléments supprimés)
    
Pour créer des balises de rétention, vous allez utiliser le centre d’administration Exchange (EAC) dans votre organisation Exchange Online.
  
1. Dans la sécurité &amp; centre de conformité, cliquez sur le Lanceur de l’application dans le coin supérieur gauche, puis cliquez sur la vignette de **l’administrateur** . 
    
2. Dans le volet de navigation de gauche du centre d’administration Office 365, cliquez sur **Centre d’administration**, puis cliquez sur **Exchange**.
    
    ![Screenshot shows the Office 365 admin center with the Admin centers option expanded and Exchange selected.](media/47399df2-0bc4-42e2-b183-07750a46bc68.png)
  
3. Dans le CAE, accédez à **gestion de la conformité** \> **balises de rétention**
    
    Une liste des balises de rétention pour votre organisation s’affiche.
    
### <a name="create-a-custom-archive-default-policy-tag"></a>Créer une balise de stratégie d’archivage personnalisés par défaut
  
Tout d’abord, vous allez créer une balise de stratégie par défaut (DPT) archive personnalisé qui va déplacer des éléments à la boîte aux lettres d’archivage après 3 ans. 
  
1. Dans la page **balises de rétention** , cliquez sur **nouvelle balise**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), puis sélectionnez **appliqué automatiquement à la boîte aux lettres entière (par défaut)**. 
    
2. Dans la page **nouvelle balise appliquée automatiquement à la boîte aux lettres entière (par défaut)** , complétez les champs suivants : 
    
    ![Paramètres pour créer une nouvelle balise de stratégie par défaut archive](media/41c0a43c-9c72-44e0-8947-da0831896432.png)
  
1. **Nom** Tapez un nom pour la nouvelle balise de rétention. 
    
2. **Action de rétention** Sélectionnez **déplacer vers l’Archive** pour déplacer des éléments à la boîte aux lettres d’archivage lors de la période de rétention. 
    
3. **Période de rétention** Sélectionnez **lorsque l’élément atteint l’âge suivant (en jours)**, puis entrez la durée de la période de rétention. Dans ce scénario, les éléments seront déplacées vers la boîte aux lettres d’archivage après 1095 jours (3 ans).
    
4. **Commentaire** (Facultatif) Tapez un commentaire qui explique l’objectif de la balise de rétention personnalisée. 
    
3. Cliquez sur **Enregistrer** pour créer l’archive personnalisé DPT. 
    
    La nouvelle DPT archive est affiché dans la liste des balises de rétention.
    
### <a name="create-a-custom-deletion-default-policy-tag"></a>Créer une balise de stratégie de suppression personnalisées par défaut
  
Ensuite, vous allez créer un autre DPT personnalisé, mais celle-ci sera une stratégie de suppression qui supprime définitivement les éléments après 7 ans.
  
1. Dans la page **balises de rétention** , cliquez sur **nouvelle balise**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), puis sélectionnez **appliqué automatiquement à la boîte aux lettres entière (par défaut)**. 
    
2. Dans la page **nouvelle balise appliquée automatiquement à la boîte aux lettres entière (par défaut)** , complétez les champs suivants : 
    
    ![Paramètres pour créer une nouvelle balise de stratégie par défaut de suppression](media/f1f0ff62-eec9-4824-8e7c-d93dcfb09a79.png)
  
1. **Nom** Tapez un nom pour la nouvelle balise de rétention. 
    
2. **Action de rétention** Sélectionnez **Supprimer** pour supprimer définitivement les éléments à partir de la boîte aux lettres lors de la période de rétention. 
    
3. **Période de rétention** Sélectionnez **lorsque l’élément atteint l’âge suivant (en jours)**, puis entrez la durée de la période de rétention. Dans ce scénario, les éléments seront purgés après 2555 jours (7 ans).
    
4. **Commentaire** (Facultatif) Tapez un commentaire qui explique l’objectif de la balise de rétention personnalisée. 
    
3. Cliquez sur **Enregistrer** pour créer la suppression personnalisée DPT. 
    
    La nouvelle DPT suppression est affiché dans la liste des balises de rétention.
    
### <a name="create-a-custom-retention-policy-tag-for-the-deleted-items-folder"></a>Créer une balise de stratégie de rétention personnalisée pour le dossier éléments supprimés
  
La dernière balise de rétention que vous créerez est une balise de stratégie de rétention personnalisée (RPT) pour le dossier éléments supprimés. Cette balise supprime les éléments dans le dossier éléments supprimés après 5 ans et fournit un point de récupération lorsque les utilisateurs peuvent utiliser l’outil récupérer les éléments supprimés pour récupérer un élément.
  
1. Dans la page **balises de rétention** , cliquez sur **nouvelle balise** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), puis sélectionnez **appliqué automatiquement à un dossier par défaut**. 
    
2. Dans la page **nouvelle balise appliquée automatiquement à un dossier par défaut** , complétez les champs suivants : 
    
    ![Paramètres pour créer une nouvelle balise de stratégie de rétention du dossier éléments supprimés](media/6f3104bd-5edb-48ac-884d-5fe13d81dd1d.png)
  
1. **Nom** Tapez un nom pour la nouvelle balise de rétention. 
    
2. **Appliquer cette balise dans le dossier par défaut suivant** Dans la liste déroulante, sélectionnez les **Éléments supprimés**.
    
3. **Action de rétention** Sélectionnez **Supprimer et autoriser la récupération** pour supprimer des éléments lors de la période de rétention expire, mais permettre aux utilisateurs de récupérer un élément supprimé dans la période de rétention des éléments supprimés (qui par défaut est 14 jours). 
    
4. **Période de rétention** Sélectionnez **lorsque l’élément atteint l’âge suivant (en jours)**, puis entrez la durée de la période de rétention. Dans ce scénario, les éléments seront supprimés après jours 1825 (5 ans).
    
5. **Commentaire** (Facultatif) Tapez un commentaire qui explique l’objectif de la balise de rétention personnalisée. 
    
3. Cliquez sur **Enregistrer** pour créer le rapport personnalisé pour le dossier éléments supprimés. 
    
    Le nouveau rapport s’affiche dans la liste des balises de rétention.

## <a name="step-3-create-a-new-retention-policy"></a>Étape 3 : Créer une nouvelle stratégie de rétention

Après avoir créé les balises de rétention personnalisée, l’étape suivante consiste à créer une nouvelle stratégie de rétention et ajoutez les balises de rétention. Vous allez ajouter trois balises de rétention personnalisée que vous avez créé à l’étape 2 et les balises intégrés qui ont été mentionnés dans la première section. À l’étape 4, vous allez assigner cette nouvelle stratégie de rétention aux boîtes aux lettres de l’utilisateur.
  
1. Dans le CAE, accédez à **gestion de la conformité** \> **des stratégies de rétention**.
    
2. Dans la page **des stratégies de rétention** , cliquez sur **Nouveau** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).
    
3. Dans la zone **nom** , tapez un nom pour la nouvelle stratégie de rétention ; par exemple, **Alpine voie Archive et la stratégie de suppression**. 
    
4. Sous **les balises de rétention**, cliquez sur **Ajouter** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).
    
    Une liste des balises de rétention dans votre organisation s’affiche. Notez que les balises personnalisées que vous avez créé à l’étape 2 sont affichés.
    
5. Ajoutez les balises de rétention 9 qui sont mis en surbrillance dans la capture d’écran suivante (ces balises sont décrites plus en détail dans la section [plus d’informations](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) ). Pour ajouter une balise de rétention, sélectionnez-la, puis cliquez sur **Ajouter**. 
    
    ![Ajouter des balises de rétention à la nouvelle stratégie de rétention](media/d8e87176-0716-4238-9e6a-7c4af35541dc.png)
  
    > [!TIP]
    > Vous pouvez sélectionner plusieurs balises de rétention en maintenant la touche **Ctrl** enfoncée, puis en cliquant sur chaque balise. 
  
6. Une fois que vous avez ajouté les balises de rétention, cliquez sur **OK**.
    
7. Dans la page **nouvelle stratégie de rétention** , cliquez sur **Enregistrer** pour créer la nouvelle stratégie. 
    
    La nouvelle stratégie de rétention s’affiche dans la liste. Sélectionner pour afficher les balises de rétention liées dans le volet détails.
    
    ![La nouvelle stratégie de rétention et la liste des balises de rétention liées](media/63bc45e6-110b-4dc9-a85f-8eb1961a8258.png)
  
## <a name="step-4-assign-the-new-retention-policy-to-user-mailboxes"></a>Étape 4 : Affecter la nouvelle stratégie de rétention aux boîtes aux lettres utilisateur

Lorsqu’une nouvelle boîte aux lettres est créé, une stratégie de rétention nommée stratégie MRM par défaut est affectée à celui-ci par défaut. Dans cette étape, vous allez remplacer cette stratégie de rétention (car une boîte aux lettres peut avoir qu’une seule stratégie de rétention qui lui est affectée) en affectant la nouvelle stratégie de rétention que vous avez créé à l’étape 3 pour les boîtes aux lettres utilisateur dans votre organisation. Cette étape suppose que vous devez attribuer la nouvelle stratégie à toutes les boîtes aux lettres dans votre organisation.
  
1. Dans le CAE, accédez à **Destinataires** \> **Boîtes aux lettres**.
    
    Une liste de toutes les boîtes aux lettres d’utilisateur dans votre organisation s’affiche. 
    
2. Sélectionnez les boîtes aux lettres en cliquant sur le premier dans la liste, maintenez enfoncée la touche **MAJ enfoncée** , puis en cliquant sur la dernière occurrence dans la liste. 
    
3. Dans le volet de détails sur le côté droit du CAE, sous **Modifier en bloc**, cliquez sur **autres options**.
    
4. Sous **Stratégie de rétention**, cliquez sur **Mettre à jour**.
    
5. Dans la page **en bloc attribuer la stratégie de rétention** , dans la liste déroulante **Sélectionner la stratégie de rétention** , sélectionnez la stratégie de rétention que vous avez créé à l’étape 3 ; par exemple, **Alpine voie Archive et la stratégie de rétention**.
    
6. Cliquez sur **Enregistrer** pour enregistrer la nouvelle affectation de stratégie de rétention. 
    
7. Pour vérifier que la nouvelle stratégie de rétention a été attribuée aux boîtes aux lettres, vous disposez des options suivantes : sélectionnez une boîte aux lettres dans la page de boîtes aux lettres, puis cliquez sur Modifier. 
    
1. Sélectionnez une boîte aux lettres dans la page de **boîtes aux lettres** , puis cliquez sur **Modifier** ![modifier](media/d7dc7e5f-17a1-4eb9-b42d-487db59e2e21.png). 
    
2. Dans la page de propriétés de boîte aux lettres de l’utilisateur sélectionné, cliquez sur **fonctionnalités de boîte aux lettres**.
    
    Le nom de la nouvelle stratégie attribuée à la boîte aux lettres s’affiche dans la liste déroulante de **la stratégie de rétention** . 
    

  
## <a name="optional-step-5-run-the-managed-folder-assistant-to-apply-the-new-settings"></a>(Facultatif) Étape 5 : Exécuter l’Assistant dossier géré pour appliquer les nouveaux paramètres
<a name="step3"> </a>

Après avoir appliqué la nouvelle stratégie de rétention aux boîtes aux lettres à l’étape 4, elle peut prendre jusqu'à sept jours dans Exchange Online pour les nouveaux paramètres de rétention à appliquer aux boîtes aux lettres. Il s’agit, car un processus appelé l’Assistant dossier géré boîtes aux lettres du processus de 7 jours. Au lieu d’attendre l’Assistant dossier géré à exécuter, vous pouvez forcer cette situation en exécutant l’applet de commande **Start-ManagedFolderAssistant** dans Exchange Online PowerShell. 
  
 **Que se passe-t-il lorsque vous exécutez l’Assistant dossier géré ?** Il applique les paramètres dans la stratégie de rétention par inspection des éléments dans la boîte aux lettres et de déterminer si elles sont soumis à rétention. Il affecte ensuite les éléments soumis à rétention avec la balise de rétention appropriées et effectue l’action de rétention spécifié sur les éléments au-delà de leur âge de rétention. 
  
Voici les étapes pour se connecter à Exchange Online PowerShell, puis exécutez l’Assistant dossier géré sur chaque boîte aux lettres dans votre organisation.
  
1. Sur votre ordinateur local, ouvrez Windows PowerShell et exécutez la commande suivante.
    
    ```
    $UserCredential = Get-Credential
    ```

    Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell** , tapez le nom d’utilisateur et le mot de passe de votre compte d’administrateur global Office 365, puis cliquez sur **OK**.
    
2. Exécutez la commande suivante.
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. Exécutez la commande suivante.
    
    ```
    Import-PSSession $Session
    ```

4. Pour vérifier que vous êtes connecté à votre organisation Exchange Online, exécutez la commande suivante pour obtenir la liste de toutes les boîtes aux lettres de votre organisation.
    
    ```
    Get-Mailbox
    ```

    > [!NOTE]
    > Pour plus d'informations ou si vous rencontrez des problèmes pour vous connecter à votre organisation Exchange Online, consultez la rubrique [Connexion à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283). 
  
5. Exécutez les deux commandes suivantes pour démarrer l’Assistant dossier géré pour toutes les boîtes aux lettres utilisateur dans votre organisation.
    
    ```
    $Mailboxes = Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"}
    ```

    ```
    $Mailboxes.Identity | Start-ManagedFolderAssistant
    ```

Voilà ! Vous avez configuré une stratégie d’archivage et de suppression de l’organisation Alpine House.
  
## <a name="more-information"></a>Plus d'informations
<a name="moreinfo"> </a>

- Comment est calculée âge de rétention ? L’âge de rétention des éléments de boîte aux lettres est calculée à partir de la date de remise ou de la date de création des éléments tels que les messages de projet qui ne sont pas envoyées, mais sont créés par l’utilisateur. Lorsque l’Assistant dossier géré traite les éléments dans une boîte aux lettres, elle affecte à une date de début et une date d’expiration pour tous les éléments qui ont des balises de rétention avec l’action de rétention supprimer et autoriser la récupération ou supprimer définitivement. Éléments qui ont une balise d’archivage sont marqués avec une date de déplacement. 
    
- Le tableau suivant fournit plus d’informations sur chaque balise de rétention qui est ajouté à la stratégie de rétention personnalisée qui a été créée en suivant les étapes décrites dans cette rubrique.
    
    |**Balise de rétention**|**Ce que fait cette balise**|**Intégrée ou personnalisée ?**|**Type (Type)**|
    |:-----|:-----|:-----|:-----|
    |Déplacement vers l’Archive-3 ans Alpine House  <br/> |Déplace les éléments qui sont 1095 jours (3 ans) à la boîte aux lettres d’archive.  <br/> |Personnalisé (voir [étape 2 : créer des balises de rétention nouvelle pour les stratégies d’archivage et de suppression](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Balise de stratégie par défaut (archive) ; Cette balise est automatiquement appliquée à la boîte aux lettres entière.  <br/> |
    |Maison Alpine 7 ans supprimer définitivement  <br/> |Supprime définitivement les éléments dans la boîte aux lettres principale ou de la boîte aux lettres d’archive lorsqu’ils sont 7 ans.  <br/> |Personnalisé (voir [étape 2 : créer des balises de rétention nouvelle pour les stratégies d’archivage et de suppression](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Balise de stratégie par défaut (suppression) ; Cette balise est automatiquement appliquée à la boîte aux lettres entière.  <br/> |
    |Maison Alpine supprimé éléments 5 ans supprimer et autoriser la récupération  <br/> |Supprime les éléments à partir du dossier éléments supprimés sont 5 ans. Les utilisateurs peuvent récupérer ces éléments de 14 jours après que qu’ils sont supprimées.<sup>\*</sup> <br/> |Personnalisé (voir [étape 2 : créer des balises de rétention nouvelle pour les stratégies d’archivage et de suppression](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Balise de stratégie de rétention (éléments supprimés) ; Cette balise est automatiquement appliquée aux éléments dans le dossier éléments supprimés.  <br/> |
    |Jours de 14 éléments récupérables déplacement vers l’Archive  <br/> |Déplace les éléments qui ont été dans le dossier éléments récupérables de 14 jours dans le dossier éléments récupérables dans la boîte aux lettres d’archive.  <br/> |Intégré  <br/> |Balise de stratégie de rétention (éléments récupérables) ; Cette balise est automatiquement appliquée aux éléments dans le dossier éléments récupérables.  <br/> |
    |Courrier indésirable  <br/> |Supprime définitivement les éléments qui ont été dans le dossier courrier indésirable pendant 30 jours. Les utilisateurs peuvent récupérer ces éléments de 14 jours après que qu’ils sont supprimées.<sup>\*</sup> <br/> |Intégré  <br/> |Balise de stratégie de rétention (courrier indésirable) ; Cette balise est automatiquement appliquée aux éléments dans le dossier courrier indésirable.  <br/> |
    |Suppression après 1 mois  <br/> |Supprime définitivement les éléments qui sont des 30 derniers jours. Les utilisateurs peuvent récupérer ces éléments de 14 jours après que qu’ils sont supprimées.<sup>\*</sup> <br/> |Intégré  <br/> |Personnel ; Cette balise peut être appliquée par les utilisateurs.  <br/> |
    |Suppression après 1 an  <br/> |Supprime définitivement les éléments qui sont 365 jours. Les utilisateurs peuvent récupérer ces éléments de 14 jours après que qu’ils sont supprimées.<sup>\*</sup> <br/> |Intégré  <br/> |Personnel ; Cette balise peut être appliquée par les utilisateurs.  <br/> |
    |Ne jamais supprimer  <br/> |Cette balise empêcher la suppression par une stratégie de rétention des éléments.  <br/> |Intégré  <br/> |Personnel ; Cette balise peut être appliquée par les utilisateurs.  <br/> |
    |Déplacement vers l'archive après 1 an - Personnel  <br/> |Déplace les éléments à la boîte aux lettres d’archive après 1 an.  <br/> |Intégré  <br/> |Personnel ; Cette balise peut être appliquée par les utilisateurs.  <br/> |
   
    > <sup>\*</sup>Les utilisateurs peuvent utiliser l’outil récupérer les éléments supprimés dans Outlook et Outlook Web App pour récupérer un élément supprimé dans la période de rétention des éléments supprimés qui par défaut est 14 jours dans Exchange Online. Un administrateur peut utiliser Windows PowerShell pour augmenter la période de rétention des éléments supprimés pour un maximum de 30 jours. Pour plus d’informations, voir : [récupérer les éléments supprimés dans Outlook pour Windows](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce) et [Modifier la période de rétention des éléments supprimés pour une boîte aux lettres dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940)
  
- À l’aide de l’aide de balise **récupérables éléments 14 jours sont déplacés vers l’Archive** rétention libre espace de stockage dans le dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur. Cela est utile lors de la boîte aux lettres d’un utilisateur est mis en attente, ce qui signifie que rien n’est jamais définitivement supprimés de la boîte aux lettres. Sans transférer les éléments dans la boîte aux lettres d’archivage, il est possible de que sera atteint le quota de stockage pour le dossier éléments récupérables dans la boîte aux lettres principale. Pour plus d’informations à ce sujet et comment l’éviter, voir [augmenter les éléments récupérables quota de boîtes aux lettres sur Maintenez](https://go.microsoft.com/fwlink/p/?LinkId=786479).
