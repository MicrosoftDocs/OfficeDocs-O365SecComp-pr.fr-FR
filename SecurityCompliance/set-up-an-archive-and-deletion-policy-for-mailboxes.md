---
title: Configurer une stratégie d'archivage et de suppression pour les boîtes aux lettres de votre organisation Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
ms.assetid: ec3587e4-7b4a-40fb-8fb8-8aa05aeae2ce
description: Créer une stratégie d'archivage et de suppression dans Office 365 qui déplace automatiquement les éléments vers la boîte aux lettres d'archivage d'un utilisateur.
ms.openlocfilehash: 09fef681884dd12b76bf0e30aa757d6e656f99a7
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223513"
---
# <a name="set-up-an-archive-and-deletion-policy-for-mailboxes-in-your-office-365-organization"></a>Configurer une stratégie d'archivage et de suppression pour les boîtes aux lettres de votre organisation Office 365

 Dans Office 365, les administrateurs peuvent créer une stratégie d'archivage et de suppression qui déplace automatiquement les éléments vers la boîte aux lettres d'archivage d'un utilisateur et supprime automatiquement les éléments de la boîte aux lettres. L'administrateur effectue cette opération en créant une stratégie de rétention qui est affectée aux boîtes aux lettres et déplace des éléments vers la boîte aux lettres d'archivage d'un utilisateur au bout d'un certain temps, ce qui supprime également les éléments de la boîte aux lettres une fois qu'ils ont atteint une certaine limite d'âge. Les règles réelles qui déterminent les éléments déplacés ou supprimés et lorsque cela se produit sont appelées balises de rétention. Les balises de réTention sont liées à une stratégie de rétention, qui à son tour est affectée à la boîte aux lettres d'un utilisateur. Une balise de rétention applique les paramètres de rétention aux messages et dossiers individuels dans la boîte aux lettres d'un utilisateur. Il définit la durée pendant laquelle un message reste dans la boîte aux lettres et l'action effectuée lorsque le message atteint l'âge de rétention spécifié. Lorsqu'un message atteint son âge de rétention, il est déplacé vers la boîte aux lettres d'archivage de l'utilisateur ou supprimé. 
  
La procédure décrite dans cet article permet de configurer une stratégie d'archivage et de rétention pour une organisation fictive nommée Alpine House. La configuration de cette stratégie inclut les tâches suivantes:
  
- Activation d'une boîte aux lettres d'archivage pour chaque utilisateur de l'organisation. Cela permet aux utilisateurs d'ajouter des boîtes aux lettres et est requis afin qu'une stratégie de rétention puisse déplacer des éléments vers la boîte aux lettres d'archivage. Il permet également de déménager des éléments dans leur boîte aux lettres d'archivage. 
    
- La création de trois balises de rétention personnalisées qui effectuent les opérations suivantes: 
    
  - Déplace automatiquement les éléments datant de 3 ans vers la boîte aux lettres d'archivage de l'utilisateur. Le fait de placer des éléments dans la boîte aux lettres d'archivage libère de l'espace dans la boîte aux lettres principale d'un utilisateur.
    
  - Supprime automatiquement les éléments datant de 5 ans du dossier éléments supprimés. Cela libère également de l'espace dans la boîte aux lettres principale de l'utilisateur. Si nécessaire, l'utilisateur aura la possibilité de récupérer ces éléments. Pour plus d'informations, consultez la note de bas de page dans la section [informations supplémentaires](#more-information) . 
    
  - Supprime automatiquement (et définitivement) les éléments datant de 7 ans à la fois des boîtes aux lettres principale et d'archivage. En raison de réglementations de conformité, certaines organisations doivent conserver le courrier électronique pendant une certaine période de temps. Une fois cette période expirée, une organisation peut vouloir supprimer définitivement ces boîtes aux lettres utilisateur. 
    
- Création d'une nouvelle stratégie de rétention et ajout des nouvelles balises de rétention personnalisées à celle-ci. En outre, vous ajoutez également des balises de rétention intégrées à la nouvelle stratégie de rétention. Cela inclut les balises personnelles que les utilisateurs peuvent affecter aux éléments dans leur boîte aux lettres. Vous ajouterez également une balise de rétention qui déplace les éléments du dossier éléments récupérables de la boîte aux lettres principale de l'utilisateur vers le dossier éléments récupérables dans la boîte aux lettres d'archivage. Cela permet de libérer de l'espace dans le dossier éléments récupérables d'un utilisateur lorsque sa boîte aux lettres est placée en conservation.
    
Vous pouvez suivre une partie ou la totalité des étapes décrites dans cet article pour configurer une stratégie d'archivage et de suppression pour les boîtes aux lettres de votre organisation. Nous vous recommandons de tester ce processus sur quelques boîtes aux lettres avant de l'implémenter sur toutes les boîtes aux lettres de votre organisation.
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être un administrateur général dans votre organisation Office 365 pour effectuer les étapes décrites dans cette rubrique. 
    
-  Lorsque vous créez un nouveau compte d'utilisateur dans Office 365 et que vous affectez à l'utilisateur une licence Exchange Online, une boîte aux lettres est automatiquement créée pour l'utilisateur. Lorsque la boîte aux lettres est créée, une stratégie de rétention par défaut, appelée stratégie MRM par défaut, lui est automatiquement attribuée. Dans cet article, vous allez créer une nouvelle stratégie de rétention, puis l'affecter à des boîtes aux lettres utilisateur, en remplaçant la stratégie MRM par défaut. Une boîte aux lettres ne peut avoir qu'une seule stratégie de rétention affectée à un moment donné.
    
- Pour en savoir plus sur les balises de rétention et les stratégies de rétention dans Exchange Online, voir [balises et stratégies](https://go.microsoft.com/fwlink/p/?LinkId=404424)de rétention.
    
## <a name="step-1-enable-archive-mailboxes-for-users"></a>Étape 1: activer les boîtes aux lettres d'archivage pour les utilisateurs

La première étape consiste à activer la boîte aux lettres d'archivage pour chaque utilisateur de votre organisation. La boîte aux lettres d'archivage d'un utilisateur doit être activée afin qu'une balise de rétention avec une action de rétention «déplacer vers l'archive» puisse déplacer l'élément après l'expiration de la durée de rétention. 
  
> [!NOTE]
> Vous pouvez activer des boîtes aux lettres d'archivage à tout moment au cours de ce processus, dès lors qu'elles sont activées à un moment donné avant que le processus ne soit terminé. Si une boîte aux lettres d'archivage n'est pas activée, aucune action n'est effectuée sur les éléments auxquels une stratégie d'archivage est attribuée. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte d'administrateur général.
    
    
3. Dans le centre &amp; de sécurité conformité, accédez à **Archives**de **gouvernance** \> des données.
    
    Une liste des boîtes aux lettres de votre organisation s'affiche et indique si la boîte aux lettres d'archivage correspondante est activée ou désactivée. 
    
4. Sélectionnez toutes les boîtes aux lettres en cliquant sur le premier de la liste, en maintenant enfoncée la touche **MAJ** , puis en cliquant sur la dernière de la liste. 
    
    > [!TIP]
    > Cette étape part du principe qu'aucune boîte aux lettres d'archivage n'est activée. Si vous avez des boîtes aux lettres pour lesquelles l'archivage est activé, maintenez la touche **CTRL** enfoncée et cliquez sur chaque boîte aux lettres contenant une boîte aux lettres d'archivage désactivée. Vous pouvez aussi cliquer sur l'en-tête de colonne **boîte aux lettres** d'archivage pour trier les lignes selon que la boîte aux lettres d'archivage est activée ou désactivée pour faciliter la sélection des boîtes aux lettres. 
  
5. Dans le volet d'informations, sous **modification en bloc**, cliquez sur **activer**.
    
    Un avertissement s'affiche indiquant que les éléments datant de plus de deux ans seront déplacés vers la nouvelle boîte aux lettres d'archivage. Cela est dû au fait que la stratégie de rétention par défaut qui est affectée à une nouvelle boîte aux lettres utilisateur lors de sa création comporte une balise de stratégie d'archivage par défaut dont l'âge de rétention est de 2 ans. La balise de stratégie d'archivage par défaut personnalisée que vous allez créer à l'étape 2 a une durée de rétention de 3 ans. Cela signifie que les éléments de 3 ans ou plus seront déplacés vers la boîte aux lettres d'archivage.
    
6. Cliquez sur **Oui** pour fermer le message d'avertissement et démarrer le processus pour activer la boîte aux lettres d'archivage pour chaque boîte aux lettres sélectionnée. 
    
7. Une fois le processus terminé, cliquez **** ![sur Actualiser l'actualisation](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) pour mettre à jour la liste sur la page d' **archivage** . 
    
    La boîte aux lettres d'archivage est activée pour tous les utilisateurs de votre organisation.
    
    ![La liste des boîtes aux lettres avec la boîte aux lettres d'archivage activée](media/61a7cb97-1bed-4808-aa5f-b6b761cfa8de.png)
  
8. Laissez le centre &amp; de sécurité conformité ouvert. Vous l'utiliserez à l'étape suivante.
    
## <a name="step-2-create-new-retention-tags-for-the-archive-and-deletion-policies"></a>Étape 2: créer de nouvelles balises de rétention pour les stratégies d'archivage et de suppression

Dans cette étape, vous allez créer les trois balises de rétention personnalisées qui ont été décrites précédemment.
  
- Centre de la salle Alpine 3 ans déplacer vers l'archive (stratégie d'archivage personnalisée)
    
- Suppression définitive de l'année Alpine House 7 (stratégie de suppression personnalisée)
    
- Alpine House supprimé éléments supprimés 5 ans supprimer et autoriser la récupération (balise personnalisée pour le dossier éléments supprimés)
    
Pour créer des balises de rétention, vous devez utiliser le centre d'administration Exchange dans votre organisation Exchange Online.
  
1. Dans le centre &amp; de sécurité conformité, cliquez sur le lanceur d'applications dans le coin supérieur gauche, puis cliquez sur la vignette **administrateur** . 
    
2. Dans le volet de navigation de gauche du centre d'administration Office 365, cliquez sur **centres d'administration**, puis cliquez sur **Exchange**.
    
    ![Screenshot shows the Office 365 admin center with the Admin centers option expanded and Exchange selected.](media/47399df2-0bc4-42e2-b183-07750a46bc68.png)
  
3. Dans le centre d'administration Exchange, accédez à balises de rétention de **gestion** \> **** de conformité
    
    Une liste des balises de rétention de votre organisation s'affiche.
    
### <a name="create-a-custom-archive-default-policy-tag"></a>Créer une balise de stratégie d'archivage par défaut personnalisée
  
Tout d'abord, vous allez créer une balise de stratégie d'archivage par défaut personnalisée (DPT) qui déplace les éléments vers la boîte aux lettres d'archivage après 3 ans. 
  
1. Sur la **** page balises de rétention, cliquez](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)sur nouvelle icône nouvelle **balise**![, puis sélectionnez **appliqué automatiquement à la boîte aux lettres entière (par défaut)**. 
    
2. Sur la page **nouvelle balise appliquée automatiquement à la boîte aux lettres entière (par défaut)** , renseignez les champs suivants: 
    
    ![Paramètres permettant de créer une balise de stratégie d'archivage par défaut](media/41c0a43c-9c72-44e0-8947-da0831896432.png)
  
1. **Name (nom** ) Tapez un nom pour la nouvelle balise de rétention. 
    
2. **Action** de rétention Sélectionnez **déplacer vers l'archive** pour déplacer des éléments vers la boîte aux lettres d'archivage à l'expiration de la période de rétention. 
    
3. **Période** de rétention Sélectionnez **quand l'élément atteint l'âge suivant (en jours)**, puis entrez la durée de la période de rétention. Dans ce scénario, les éléments seront déplacés vers la boîte aux lettres d'archivage après 1095 jours (3 ans).
    
4. **Commentaire** Module Tapez un commentaire qui explique l'objectif de la balise de rétention personnalisée. 
    
3. Cliquez sur **Enregistrer** pour créer l'archive personnalisée DPT. 
    
    La nouvelle archive DPT est affichée dans la liste des balises de rétention.
    
### <a name="create-a-custom-deletion-default-policy-tag"></a>Créer une balise de stratégie par défaut de suppression personnalisée
  
Ensuite, vous allez créer un autre DPT personnalisé, mais celui-ci sera une stratégie de suppression qui supprime définitivement les éléments après 7 ans.
  
1. Sur la **** page balises de rétention, cliquez](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)sur nouvelle icône nouvelle **balise**![, puis sélectionnez **appliqué automatiquement à la boîte aux lettres entière (par défaut)**. 
    
2. Sur la page **nouvelle balise appliquée automatiquement à la boîte aux lettres entière (par défaut)** , renseignez les champs suivants: 
    
    ![Paramètres permettant de créer une balise de stratégie par défaut de suppression](media/f1f0ff62-eec9-4824-8e7c-d93dcfb09a79.png)
  
1. **Name (nom** ) Tapez un nom pour la nouvelle balise de rétention. 
    
2. **Action** de rétention Sélectionnez **Supprimer définitivement** pour purger les éléments de la boîte aux lettres à l'expiration de la période de rétention. 
    
3. **Période** de rétention Sélectionnez **quand l'élément atteint l'âge suivant (en jours)**, puis entrez la durée de la période de rétention. Pour ce scénario, les éléments seront purgés après 2555 jours (7 ans).
    
4. **Commentaire** Module Tapez un commentaire qui explique l'objectif de la balise de rétention personnalisée. 
    
3. Cliquez sur **Enregistrer** pour créer la suppression personnalisée DPT. 
    
    La nouvelle suppression d'DPT apparaît dans la liste des balises de rétention.
    
### <a name="create-a-custom-retention-policy-tag-for-the-deleted-items-folder"></a>Créer une balise de stratégie de rétention personnalisée pour le dossier éléments supprimés
  
La dernière balise de rétention que vous allez créer est une balise de stratégie de rétention personnalisée (RPT) pour le dossier éléments supprimés. Cette balise supprime les éléments du dossier éléments supprimés après 5 ans et fournit une période de récupération lorsque les utilisateurs peuvent utiliser l'outil récupérer les éléments supprimés pour récupérer un élément.
  
1. Sur la **** page balises de rétention, cliquez](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)sur nouvelle icône nouvelle **balise** ![, puis sélectionnez **appliqué automatiquement à un dossier par défaut**. 
    
2. Sur la **nouvelle balise appliquée automatiquement à une page de dossier par défaut** , renseignez les champs suivants: 
    
    ![Paramètres permettant de créer une nouvelle balise de stratégie de rétention pour le dossier éléments supprimés](media/6f3104bd-5edb-48ac-884d-5fe13d81dd1d.png)
  
1. **Name (nom** ) Tapez un nom pour la nouvelle balise de rétention. 
    
2. **Appliquer cette balise au dossier par défaut suivant** Dans la liste déroulante, sélectionnez **éléments supprimés**.
    
3. **Action** de rétention Sélectionnez **supprimer et autoriser la récupération** pour supprimer des éléments à l'expiration de la période de rétention, mais autoriser les utilisateurs à récupérer un élément supprimé pendant la période de rétention des éléments supprimés (la valeur par défaut est 14 jours). 
    
4. **Période** de rétention Sélectionnez **quand l'élément atteint l'âge suivant (en jours)**, puis entrez la durée de la période de rétention. Pour ce scénario, les éléments seront supprimés après 1825 jours (5 ans).
    
5. **Commentaire** Module Tapez un commentaire qui explique l'objectif de la balise de rétention personnalisée. 
    
3. Cliquez sur **Enregistrer** pour créer l'arborescence personnalisée pour le dossier éléments supprimés. 
    
    La nouvelle arborescence RPT est affichée dans la liste des balises de rétention.

## <a name="step-3-create-a-new-retention-policy"></a>Étape 3: créer une stratégie de rétention

Une fois que vous avez créé les balises de rétention personnalisées, l'étape suivante consiste à créer une nouvelle stratégie de rétention et à ajouter les balises de rétention. Vous allez ajouter les trois balises de rétention personnalisées que vous avez créées à l'étape 2, et les balises intégrées mentionnées dans la première section. À l'étape 4, vous allez affecter cette nouvelle stratégie de rétention aux boîtes aux lettres des utilisateurs.
  
1. Dans le centre d'administration Exchange, accédez à **stratégies**de rétention de **gestion** \> de la conformité.
    
2. Sur la page **stratégies** de rétention, cliquez](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)sur **nouvelle** ![icône.
    
3. Dans la zone **nom** , tapez un nom pour la nouvelle stratégie de rétention; par exemple, **stratégie d'archivage et de suppression Alpine House**. 
    
4. Sous **balises**de rétention,](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)cliquez sur **Ajouter** ![une nouvelle icône.
    
    Une liste des balises de rétention de votre organisation s'affiche. Remarque les balises personnalisées que vous avez créées à l'étape 2 sont affichées.
    
5. Ajoutez les 9 balises de rétention mises en surbrillance dans la capture d'écran suivante (ces balises sont décrites plus en détail dans la section [plus d'informations](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) ). Pour ajouter une balise de rétention, sélectionnez-la, puis cliquez sur **Ajouter**. 
    
    ![Ajouter des balises de rétention à la nouvelle stratégie de rétention](media/d8e87176-0716-4238-9e6a-7c4af35541dc.png)
  
    > [!TIP]
    > Vous pouvez sélectionner plusieurs balises de rétention en maintenant enfoncée la touche **CTRL** , puis en cliquant sur chaque balise. 
  
6. Une fois que vous avez ajouté les balises de rétention, cliquez sur **OK**.
    
7. Sur la page **nouvelle stratégie** de rétention, cliquez sur **Enregistrer** pour créer la nouvelle stratégie. 
    
    La nouvelle stratégie de rétention est affichée dans la liste. Sélectionnez-le pour afficher les balises de rétention associées dans le volet d'informations.
    
    ![La nouvelle stratégie de rétention et la liste des balises de rétention liées](media/63bc45e6-110b-4dc9-a85f-8eb1961a8258.png)
  
## <a name="step-4-assign-the-new-retention-policy-to-user-mailboxes"></a>Étape 4: affecter la nouvelle stratégie de rétention aux boîtes aux lettres utilisateur

Lorsqu'une nouvelle boîte aux lettres est créée, une stratégie de rétention nommée Default MRM Policy lui est affectée par défaut. Dans cette étape, vous allez remplacer cette stratégie de rétention (car une boîte aux lettres ne peut avoir qu'une seule stratégie de rétention) en affectant la nouvelle stratégie de rétention que vous avez créée à l'étape 3 aux boîtes aux lettres utilisateur de votre organisation. Cette étape suppose que vous assignez la nouvelle stratégie à toutes les boîtes aux lettres de votre organisation.
  
1. Dans le CAE, accédez à **Destinataires** \> **Boîtes aux lettres**.
    
    Une liste de toutes les boîtes aux lettres utilisateur de votre organisation s'affiche. 
    
2. Sélectionnez toutes les boîtes aux lettres en cliquant sur le premier de la liste, en maintenant enfoncée la touche **MAJ** , puis en cliquant sur la dernière de la liste. 
    
3. Dans le volet d'informations sur le côté droit du centre d'administration Exchange, sous **modification en bloc**, cliquez sur **plus d'options**.
    
4. Sous **Stratégie de rétention**, cliquez sur **Mettre à jour**.
    
5. Dans la page **affecter une stratégie** de rétentIon en bloc, dans la liste déRoulante sélectionnez la stratégie de rétention, sélectionnez la stratégie de rétention que vous avez créée à l'étape 3; **** par exemple, **stratégie d'archivage et de RétentIon Alpine House**.
    
6. Cliquez sur **Enregistrer** pour enregistrer la nouvelle affectation de stratégie de rétention. 
    
7. Pour vérifier que la nouvelle stratégie de rétention a été affectée à des boîtes aux lettres, vous pouvez effectuer les opérations suivantes: sélectionnez une boîte aux lettres dans la page boîtes aux lettres, puis cliquez sur modifier. 
    
1. Sélectionnez une boîte aux lettres dans la page **boîtes aux lettres** , **** ![puis cliquez](media/d7dc7e5f-17a1-4eb9-b42d-487db59e2e21.png)sur modifier. 
    
2. Dans la page des propriétés de boîte aux lettres de l'utilisateur sélectionné, cliquez sur **fonctionnalités de boîte aux lettres**.
    
    Le nom de la nouvelle stratégie affectée à la boîte aux lettres est affiché dans la liste déroulante **stratégie** de rétention. 

## <a name="optional-step-5-run-the-managed-folder-assistant-to-apply-the-new-settings"></a>Module Étape 5: exécuter l'Assistant dossier géré pour appliquer les nouveaux paramètres

Une fois que vous avez appliqué la nouvelle stratégie de rétention aux boîtes aux lettres à l'étape 4, il peut s'écouler jusqu'à 7 jours dans Exchange Online pour que les nouveaux paramètres de rétention soient appliqués aux boîtes aux lettres. Cela est dû au fait qu'un processus appelé Assistant dossier géré traite les boîtes aux lettres une fois tous les 7 jours. Au lieu d'attendre l'exécution de l'Assistant dossier géré, vous pouvez forcer l'exécution de l'applet de commande **Start-ManagedFolderAssistant** dans Exchange Online PowerShell. 
  
 **Que se passe-t-il lorsque vous exécutez l'Assistant dossier géré?** Il applique les paramètres dans la stratégie de rétention en inspectant les éléments de la boîte aux lettres et en déterminant s'ils font l'objet d'une rétention. Il marque ensuite les éléments soumis à la rétention à l'aide de la balise de rétention appropriée, puis prend l'action de rétention spécifiée sur les éléments après leur âge de rétention. 
  
Voici les étapes à suivre pour vous connecter à Exchange Online PowerShell, puis exécuter l'Assistant dossier géré sur toutes les boîtes aux lettres de votre organisation.
  
1. Sur votre ordinateur local, ouvrez Windows PowerShell et exécutez la commande suivante.
    
    ```
    $UserCredential = Get-Credential
    ```

    Dans la boîte de dialogue **demande d'informations d'identification Windows PowerShell** , tapez le nom d'utilisateur et le mot de passe de votre compte d'administrateur global 365 Office, puis cliquez sur **OK**.
    
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
    > Pour plus d'informations ou si vous rencontrez des problèmes pour vous connecter à votre organisation Exchange Online, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283). 
  
5. Exécutez les deux commandes suivantes pour démarrer l'Assistant dossier géré pour toutes les boîtes aux lettres utilisateur de votre organisation.
    
    ```
    $Mailboxes = Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"}
    ```

    ```
    $Mailboxes.Identity | Start-ManagedFolderAssistant
    ```

Voilà! Vous avez configuré une stratégie d'archivage et de suppression pour l'organisation Alpine House.
  
## <a name="optional-step-6-make-the-new-retention-policy-the-default-for-your-organization"></a>Module Étape 6: définir la nouvelle stratégie de rétention comme stratégie par défaut pour votre organisation

À l'étape 4, vous devez affecter la nouvelle stratégie de rétention aux boîtes aux lettres existantes. Toutefois, vous pouvez configurer Exchange Online de sorte que la nouvelle stratégie de rétention soit affectée à de nouvelles boîtes aux lettres créées à l'avenir. Pour ce faire, utilisez Exchange Online PowerShell pour mettre à jour le plan de boîte aux lettres par défaut de votre organisation. Un *plan de boîte aux lettres* est un modèle qui configure automatiquement les propriétés sur les nouvelles boîtes aux lettres.  Cette étape facultative vous permet de remplacer la stratégie de rétention actuelle affectée au plan de boîte aux lettres (par défaut, la stratégie MRM par défaut) par la stratégie de rétention que vous avez créée à l'étape 3. Une fois que vous avez mis à jour le plan de boîte aux lettres, la nouvelle stratégie de rétention est attribuée aux nouvelles boîtes aux lettres.

1. [Connectez-vous à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) ou consultez l'étape 5.

2. Exécutez la commande suivante pour afficher les informations sur les plans de boîte aux lettres dans votre organisation.

    ```
    Get-MailboxPlan | Format-Table DisplayName,RetentionPolicy,IsDefault
    ```
    Notez le plan de boîte aux lettres défini par défaut.

3. Exécutez la commande suivante pour affecter la nouvelle stratégie de rétention que vous avez créée à l'étape 3 (par exemple, stratégie d'archivage et de réTention **Alpine House**) au plan de boîte aux lettres par défaut. Cet exemple suppose que le nom du plan de boîte aux lettres par défaut est **ExchangeOnlineEnterprise**.

    ```
    Set-MailboxPlan "ExchangeOnlineEnterprise" -RetentionPolicy "Alpine House Archive and Retention Policy"
    ```
4. Vous pouvez réexécuter la commande à l'étape 2 pour vérifier que la stratégie de rétention attribuée au plan de boîte aux lettres par défaut a été modifiée.

## <a name="more-information"></a>Plus d’informations

- Comment l'âge de rétention est-il calculé? L'âge de rétention des éléments de boîte aux lettres est calculé à partir de la date de livraison ou de la date de création des éléments, tels que les messages brouillons qui ne sont pas envoyés, mais qui sont créés par l'utilisateur. Lorsque l'Assistant dossier géré traite les éléments d'une boîte aux lettres, il marque une date de début et une date d'expiration pour tous les éléments qui ont des balises de rétention avec l'action supprimer et autoriser la récupération ou supprimer définitivement la rétention. Les éléments associés à une balise Archive sont marqués avec une date de déplacement. 
    
- Le tableau suivant fournit plus d'informations sur chaque balise de rétention ajoutée à la stratégie de rétention personnalisée créée en suivant les étapes de cette rubrique.
    
    |**Balise de réTention**|**Ce que fait cette balise**|**Intégré ou personnalisé?**|**Type**|
    |:-----|:-----|:-----|:-----|
    |Déplacement vers l'archive de la maison Alpine 3 ans  <br/> |Déplace les éléments datant de 1095 jours (3 ans) vers la boîte aux lettres d'archivage.  <br/> |Personnalisé (voir [étape 2: créer de nouvelles balises de rétention pour les stratégies d'archivage et de suppression](#step-2-create-new-retention-tags-for-the-archive-and-deletion-policies))  <br/> |Balise de stratégie par défaut (Archive); Cette balise est automatiquement appliquée à l'ensemble de la boîte aux lettres.  <br/> |
    |Suppression définitive de l'année Alpine House 7  <br/> |Supprime définitivement les éléments de la boîte aux lettres principale ou de la boîte aux lettres d'archivage pendant 7 ans.  <br/> |Personnalisé (voir [étape 2: créer de nouvelles balises de rétention pour les stratégies d'archivage et de suppression](#step-2-create-new-retention-tags-for-the-archive-and-deletion-policies))  <br/> |Balise de stratégie par défaut (suppression); Cette balise est automatiquement appliquée à l'ensemble de la boîte aux lettres.  <br/> |
    |Éléments supprimés de la maison Alpine 5 ans supprimer et autoriser la récupération  <br/> |Supprime les éléments du dossier éléments supprimés datant de 5 ans. Les utilisateurs peuvent récupérer ces éléments pendant 14 jours après leur suppression.<sup>\*</sup> <br/> |Personnalisé (voir [étape 2: créer de nouvelles balises de rétention pour les stratégies d'archivage et de suppression](#step-2-create-new-retention-tags-for-the-archive-and-deletion-policies))  <br/> |Balise de stratégie de réTention (éléments supprimés); Cette balise est automatiquement appliquée aux éléments du dossier éléments supprimés.  <br/> |
    |Éléments récupérables 14 jours déplacer vers l'archive  <br/> |Déplace les éléments qui se trouvent dans le dossier éléments récupérables pendant 14 jours vers le dossier éléments récupérables dans la boîte aux lettres d'archivage.  <br/> |Intégré  <br/> |Balise de stratégie de réTention (éléments récupérables); Cette balise est automatiquement appliquée aux éléments du dossier éléments récupérables.  <br/> |
    |Courrier inDésirable  <br/> |Supprime définitivement les éléments qui se trouvent dans le dossier courrier inDésirable pendant 30 jours. Les utilisateurs peuvent récupérer ces éléments pendant 14 jours après leur suppression.<sup>\*</sup> <br/> |Intégré  <br/> |Balise de stratégie de réTention (courrier inDésirable); Cette balise est automatiquement appliquée aux éléments du dossier courrier inDésirable.  <br/> |
    |Suppression après 1 mois  <br/> |Supprime définitivement les éléments datant de 30 jours. Les utilisateurs peuvent récupérer ces éléments pendant 14 jours après leur suppression.<sup>\*</sup> <br/> |Intégré  <br/> |Familiale Cette balise peut être appliquée par les utilisateurs.  <br/> |
    |Suppression après 1 an  <br/> |Supprime définitivement les éléments datant de 365 jours. Les utilisateurs peuvent récupérer ces éléments pendant 14 jours après leur suppression.<sup>\*</sup> <br/> |Intégré  <br/> |Familiale Cette balise peut être appliquée par les utilisateurs.  <br/> |
    |Ne jamais supprimer  <br/> |Cette balise empêche la suppression d'éléments par une stratégie de rétention.  <br/> |Intégré  <br/> |Familiale Cette balise peut être appliquée par les utilisateurs.  <br/> |
    |Déplacement vers l'archive après 1 an - Personnel  <br/> |Déplace les éléments vers la boîte aux lettres d'archivage après 1 an.  <br/> |Intégré  <br/> |Familiale Cette balise peut être appliquée par les utilisateurs.  <br/> |
   
    > <sup>\*</sup>Les utilisateurs peuvent utiliser l'outil de récupération des éléments supprimés dans Outlook et Outlook sur le Web (anciennement Outlook Web App) pour récupérer un élément supprimé pendant la période de rétention des éléments supprimés, qui est de 14 jours par défaut dans Exchange Online. Un administrateur peut utiliser Windows PowerShell pour augmenter la période de rétention des éléments supprimés jusqu'à un maximum de 30 jours. Pour plus d'informations, reportez-vous à la rubrique: [récupérer des éléments supprimés dans Outlook pour Windows](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce) et [modifier la période de rétention des éléments supprimés pour une boîte aux lettres dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940)
  
- L'utilisation de la balise de rétention **éléments récupérables 14 jours** permet de libérer de l'espace de stockage dans le dossier éléments récupérables dans la boîte aux lettres principale de l'utilisateur. Ceci est utile lorsque la boîte aux lettres d'un utilisateur est placée en conservation, ce qui signifie que rien n'est définitivement supprimé de la boîte aux lettres de l'utilisateur. Si vous ne déplacez pas les éléments vers la boîte aux lettres d'archivage, il est possible que le quota de stockage du dossier éléments récupérables dans la boîte aux lettres principale soit atteint. Pour plus d'informations à ce sujet et sur la façon de l'éviter, voir [augmenter le quota des éléments récupérables pour les boîtes aux lettres en attente](https://go.microsoft.com/fwlink/p/?LinkId=786479).
