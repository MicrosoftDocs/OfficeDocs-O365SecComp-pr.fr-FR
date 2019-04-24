---
title: 'FAQ : chiffrement de service avec une clé client pour Office 365'
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 41ae293a-bd5c-4083-acd8-e1a2b4329da6
description: Outre le chiffrement de base, le chiffrement au niveau du volume qui est activé via BitLocker et le gestionnaire de clés distribuées (DKM), Office 365 offre une couche de chiffrement supplémentaire au niveau de l'application pour le contenu client dans Office 365, y compris les données d'Exchange En ligne, Skype entreprise, SharePoint Online et OneDrive entreprise. Il s'agit du chiffrement de service.
ms.openlocfilehash: 8515354d716df22fa124c03e18c36914d27102f4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32266940"
---
# <a name="service-encryption-with-customer-key-for-office-365-faq"></a>FAQ : chiffrement de service avec une clé client pour Office 365

Outre le chiffrement de base, le chiffrement au niveau du volume qui est activé via BitLocker et le gestionnaire de clés distribuées (DKM), Office 365 offre une couche de chiffrement supplémentaire au niveau de l'application pour le contenu client dans Office 365, y compris les données d'Exchange En ligne, Skype entreprise, SharePoint Online et OneDrive entreprise. Il s'agit du chiffrement de service.
  
La clé client est basée sur le chiffrement de service et vous permet de fournir et de contrôler les clés utilisées pour chiffrer vos données au repos dans Office 365, comme décrit dans les [services en ligne (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx). Clé client vous permet de respecter les obligations de conformité car vous contrôlez les clés de chiffrement utilisées par Office 365 pour déchiffrer les données.
  
Pour fournir des commentaires sur la clé client, y compris la documentation, envoyez vos idées, suggestions et perspectives à customerkeyfeedback@microsoft.com.
  
## <a name="what-is-service-encryption-with-customer-key"></a>Qu'est-ce que le chiffrement de service avec la clé client?

La clé client améliore la capacité de votre organisation à répondre aux exigences des exigences de conformité qui spécifient des dispositions clés avec le fournisseur de services Cloud. La clé client vous permet de fournir et de contrôler les clés de chiffrement pour vos données Office 365 au niveau de l'application. Par conséquent, vous pouvez tester et révoquer les clés de votre organisation, si vous décidez de quitter le service. En révoquant les clés, les données ne sont pas lisibles pour le service. La révocation de clé est la première étape sur le chemin d'accès à la suppression des données.

## <a name="what-office-365-data-at-rest-is-covered-by-customer-key"></a>Quelles sont les données Office 365 de Rest couvertes par la clé client?
<a name="WhatDataIsCoveredbyCustomerKey"> </a>

Le contenu du site SharePoint Online et les fichiers stockés sur ce site, ainsi que les fichiers téléchargés sur OneDrive entreprise, sont couverts. Le contenu des boîtes aux lettres Exchange Online (corps de courrier électronique, entrées de calendrier et contenu de pièces jointes) est couvert. Les conversations textuelles de Skype entreprise sont couvertes, mais les enregistrements de diffusion de réunion Skype et les téléchargements de contenu de réunion Skype ne sont pas couverts. La diffusion de réunion Skype et le téléchargement de contenu de réunion Skype sont chiffrés avec tout autre contenu dans Office 365, mais nous ne proposons actuellement pas de contrôle par le client des clés de chiffrement.
  
## <a name="what-is-the-difference-between-customer-key-and-bring-your-own-key-byok-with-azure-information-protection-for-exchange-online"></a>Quelle est la différence entre la clé client et votre propre clé (BYOK) avec Azure information protection pour Exchange Online?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Ces deux options vous permettent de fournir et de contrôler vos propres clés de chiffrement; Toutefois, le chiffrement de service avec clé client chiffre vos données sur REST, résidant dans les serveurs Office 365, tandis que BYOK with Azure information Protection for Exchange Online chiffre votre transit de données et fournit une protection en ligne et hors connexion permanente. protection des messages électroniques et des pièces jointes pour Office 365. La clé client et BYOK avec Azure information protection pour Exchange Online sont complémentaires, et si vous choisissez d'utiliser les clés gérées par le service de Microsoft ou vos propres clés, le chiffrement de vos données sur place et en transit peut apporter une protection supplémentaire à partir de attaques malveillantes.
  
BYOK avec Azure information protection pour Exchange Online est proposé dans les fonctionnalités de chiffrement de messages Office 365.
  
## <a name="does-office-365-message-encryption-and-bring-your-own-key-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Est-ce que le chiffrement de messages Office 365 et apporter votre propre clé avec Azure information protection modifient l'approche de Microsoft pour les demandes de données tierces telles que les demandes?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. Le chiffrement de messages Office 365 et l'option permettant de fournir et de contrôler vos propres clés de chiffrement avec votre propre clé (BYOK) pour Azure information protection n'ont pas été conçus pour répondre aux apports à l'application de la Loi. Le chiffrement de messages Office 365 avec BYOK pour AIP a été conçu pour les clients ayant des objectifs de conformité qui doivent respecter leurs obligations de conformité internes ou externes. Microsoft prend des demandes tierces de données client très sérieusement. En tant que fournisseur de services Cloud, nous sommes toujours le partisan de la confidentialité des données client. Dans le cas où nous obtenons une demande, nous tentons toujours de rediriger la tierce partie vers le client pour obtenir les informations. (Lisez le blog de Brad Smith: [protection des données client de l'espionnage public](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Nous publions régulièrement des informations détaillées sur la demande que nous recevons [ici](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Pour plus d'informations, consultez le centre de gestion de la [confidentialité](https://www.microsoft.com/en-us/trustcenter/default.aspx) relatif aux demandes de données tierces et à la «divulgation des données client» dans les [services en ligne (OST) ](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="does-service-encryption-with-customer-key-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Est-ce que le chiffrement de service avec la clé client modifie l'approche de Microsoft pour les demandes de données tierces telles que les témoignages?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. La clé client n'a pas été conçue pour répondre aux apports à l'application de la Loi. Elle a été conçue pour les clients réglementés afin de répondre à leurs obligations de conformité internes ou externes. Microsoft prend des demandes tierces de données client très sérieusement. En tant que fournisseur de services Cloud, nous sommes toujours le partisan de la confidentialité des données client. Dans le cas où nous obtenons une demande, nous tentons toujours de rediriger la tierce partie vers le client pour obtenir les informations. (Lisez le blog de Brad Smith: [protection des données client de l'espionnage public](http://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Nous publions régulièrement des informations détaillées sur la demande que nous recevons [ici](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Pour plus d'informations, consultez le centre de gestion de la [confidentialité](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data) relatif aux demandes de données tierces et à la «divulgation des données client» dans les [services en ligne (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx) . 
  
## <a name="is-fasttrack-support-available-for-implementing-customer-key"></a>La prise en charge FastTrack est-elle disponible pour la mise en œuvre de la clé client?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. FastTrack est utilisé uniquement pour collecter les informations de configuration de client et de service nécessaires pour enregistrer la clé client. Les offres de clés de client sont publiées via FastTrack pour permettre aux clients et partenaires de soumettre ces informations requises à l'aide de la même méthode et de faciliter l'archivage des données fournies par les clients dans l'offre.
  
Si vous avez besoin d'une assistance supplémentaire au-delà de la documentation, contactez Microsoft Consulting Services (MCS), premier Field Engineering (PFE) ou un partenaire Microsoft pour obtenir de l'aide.
  
## <a name="if-my-keys-are-destroyed-how-can-i-recover"></a>Si mes clés sont détruites, comment puis-je récupérer?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

La clé de disponibilité vous permet de récupérer à partir de la perte imprévisible de clés racines que vous gérez. Si vous perdez vos clés racines, contactez le support Microsoft et Microsoft vous aidera à effectuer le processus d'activation de la clé de disponibilité. Vous utiliserez la clé de disponibilité pour migrer vers une nouvelle stratégie de chiffrement de données avec de nouvelles clés que vous avez configurées. 
  
## <a name="what-is-the-availability-key"></a>Qu'est-ce que la clé de disponibilité?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

La clé de disponibilité est une clé racine qui est configurée lorsque vous créez une stratégie de chiffrement de données. La clé de disponibilité est stockée et protégée dans Office 365 et fonctionne de la même manière que les deux clés racines fournies par vous pour une utilisation avec le chiffrement de service avec la clé client. Contrairement aux touches que vous fournissez et gérez dans le coffre de clés Azure, vous ne pouvez pas accéder directement à la clé de disponibilité. Le stockage et le contrôle de la clé de disponibilité sont délibérément différents des clés de coffre-fort de clés Azure pour trois raisons: Premièrement, la clé de disponibilité offre une fonctionnalité de haute disponibilité si les services Office 365 ne peuvent pas atteindre les clés hébergées dans la clé Azure Fortes Deuxièmement, la clé de disponibilité fournit une fonctionnalité de «coupure» dans le cas où les deux clés Azure Key Vault sont perdues; Enfin, la séparation des contrôles logiques assure une défense approfondie et protège contre la perte de toutes les clés d'une attaque ou d'un point de défaillance. Partager la responsabilité de protéger les clés, tout en utilisant une variété de protections et de processus pour la gestion des clés, réduit le risque que toutes les clés (et par conséquent, vos données) soient perdues ou détruites. Microsoft vous fournit une autorité exclusive sur la destruction de la clé de disponibilité. De par sa conception, personne de Microsoft n'a accès à la clé de disponibilité-elle est uniquement accessible par le code de service Office 365.
  
## <a name="how-many-data-encryption-policies-deps-can-i-create"></a>Combien de stratégies de chiffrement de données (DEPs) puis-je créer?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype entreprise:** Vous pouvez créer jusqu'à 50 DEPs. 
  
 **SharePoint Online et OneDrive entreprise:** Une DEP s'applique aux données d'un emplacement géographique, également appelé géo. Si vous utilisez la fonctionnalité multigéographique d'Office 365, vous pouvez créer une DEP par zone géographique. Si vous n'utilisez pas de multi-géo, vous pouvez créer une DEP.
  
## <a name="can-i-assign-a-data-encryption-policy-before-migrating-a-mailbox-to-the-cloud"></a>Puis-je assigner une stratégie de chiffrement de données avant de migrer une boîte aux lettres vers le Cloud?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Oui. Vous pouvez utiliser l'applet de commande Windows PowerShell Set-MailUser pour affecter une stratégie de chiffrement de données à l'utilisateur avant de migrer la boîte aux lettres vers Office 365. Dans ce cas, le contenu de la boîte aux lettres est chiffré à l'aide de la DEP attribuée lors de la migration du contenu. Cela peut être plus efficace que d'affecter une DEP une fois que la boîte aux lettres a déjà été migrée, puis d'attendre que le chiffrement ait lieu, ce qui peut prendre des heures voire des jours. 
  
## <a name="how-do-i-verify-that-encryption-with-customer-key-is-activated-and-office-365-has-finished-encrypting-with-customer-key"></a>Comment puis-je vérifier que le chiffrement avec la clé client est activé et qu'Office 365 a terminé le chiffrement avec la clé client?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype entreprise:** Vous pouvez vous [connecter à Exchange Online à l'aide de Remote PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , puis utiliser la cmdlet **[Get-MailboxStatistics]** pour chaque boîte aux lettres que vous souhaitez vérifier. Dans la sortie de la cmdlet Get-MailboxStatistics, la propriété _IsEncrypted_ renvoie la valeur **true** si la boîte aux lettres est chiffrée et la valeur **false** dans le cas contraire. Si la boîte aux lettres est chiffrée, la valeur renvoyée pour la propriété _DataEncryptionPolicyID_ est le GUID de la DEP avec laquelle la boîte aux lettres est chiffrée. Pour plus d'informations sur l'exécution de cette cmdlet, consultez la rubrique [Get-MailboxStatistics](https://technet.microsoft.com/en-us/library/bb124612%28v=exchg.160%29.aspx) et Using PowerShell with Exchange Online. 
  
Si les boîtes aux lettres ne sont pas chiffrées après avoir attendu 72 heures après l'heure à laquelle vous avez attribué la DEP, lancez un déplacement de boîte aux lettres. Pour ce faire, [Connectez-vous à Exchange Online à l'aide de Remote PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , puis utilisez la cmdlet New-MoveRequest et fournissez l'alias de la boîte aux lettres comme suit: 
  
```
New-MoveRequest <alias>
```

 **SharePoint Online et OneDrive entreprise:** Vous pouvez vous [connecter à SharePoint Online PowerShell](https://technet.microsoft.com/en-us/library/fp161372.aspx), puis utiliser la cmdlet **[Get-SPODataEncryptionPolicy]** pour vérifier l'état de votre client. La propriété * * _State_* * renvoie la valeur **Registered** si le chiffrement de clé du client est activé et si tous les fichiers de tous les sites ont été chiffrés. Si le chiffrement est toujours en cours, cette applet de commande fournit des informations sur le pourcentage de sites terminé. 
  
## <a name="if-i-want-to-switch-to-a-different-set-of-keys-how-long-does-it-take-for-the-new-set-of-keys-to-protect-my-data"></a>Si je veux basculer vers un autre ensemble de clés, combien de temps faut-il pour que le nouveau jeu de clés protège mes données?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype entreprise:** La protection d'une boîte aux lettres en fonction d'une nouvelle stratégie de chiffrement de données (DEP) à partir du moment où la nouvelle DEP est attribuée à la boîte aux lettres peut prendre jusqu'à 72 heures. 
  
 **SharePoint Online et OneDrive entreprise:** Une fois qu'une nouvelle clé a été affectée, le chiffrement de votre client complet peut prendre jusqu'à quatre heures. 
  
## <a name="is-my-existing-data-stored-without-encryption-at-any-time-while-it-is-decrypted-or-encrypted-with-customer-key"></a>Mes données existantes sont-elles stockées sans chiffrement à tout moment lorsqu'elles sont déchiffrées ou chiffrées avec la clé client?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. Vos données sont toujours chiffrées au repos dans le service Office 365 avec BitLocker et DKM. Pour plus d'informations, consultez les informations relatives à la sécurité, à la confidentialité et à la conformité pour Office 365, ainsi qu'à la [manière dont Exchange Online sécurise vos secrets de messagerie](https://support.office.com/article/989BA10C-F73F-4EFB-AD1B-AF3322E5F376).
  
## <a name="if-i-no-longer-want-to-use-customer-managed-encryption-keys-can-i-switch-to-microsoft-managed-keys"></a>Si je ne souhaite plus utiliser les clés de chiffrement gérées par le client, puis-je passer aux clés gérées par Microsoft?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype entreprise:** Pas encore. Cela sera pris en charge une fois le chiffrement de service dans Office 365 avec des clés gérées par Microsoft. Nous prévoyons de le faire dans le service une fois que nous aurons publié le chiffrement de service avec la clé client. 
  
 **SharePoint Online et OneDrive entreprise:** OK. Vous pouvez choisir de rétablir les clés gérées par Microsoft séparément pour chaque région (si vous utilisez la fonction multi-géo) ou pour toutes vos données si elles se trouvent dans une seule région. 
  
## <a name="if-i-lose-my-keys-how-long-does-it-take-to-recover-service-availability-using-the-recovery-key"></a>Si je perd mes clés, combien de temps faut-il pour récupérer la disponibilité des services à l'aide de la clé de récupération?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype entreprise:** Une fois que vous avez appelé pour utiliser la clé de disponibilité, les boîtes aux lettres seront accessibles en quelques minutes. 
  
 **SharePoint Online et OneDrive entreprise:** Cette opération est proportionnelle au nombre de sites dont vous disposez. Une fois que vous appelez Microsoft pour utiliser la clé de disponibilité, vous serez entièrement en ligne au cours des quatre heures. 
  
## <a name="how-is-the-availability-key-used-with-exchange-online"></a>Comment la clé de disponibilité est-elle utilisée avec Exchange Online?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

La clé de disponibilité est utilisée avec Exchange Online de trois façons:
  
- Disponibilité du service: dans le cas où les clés Azure Key Vault sont inaccessibles.
    
- Actions lancées par le code de service Office 365, telles que la création d'un index de recherche ou le déplacement de boîtes aux lettres.
    
- Récupération suite à une perte de clé, telle que la perte de clés Azure Key Vault associées à une seule DEP.
    
 **Utilisation de la clé de disponibilité pour la disponibilité du service dans le cas des clés Azure Key Vault sont inaccessibles.**
  
Office 365 utilise la clé de disponibilité à la fois pour la disponibilité et la récupération de service à partir d'un état de clé client présentant un manque d'intégrité pour Exchange Online. Il existe une hiérarchie de clés utilisée par la clé client. Cette hiérarchie est illustrée dans la figure suivante.
  
![](media/a760156b-737f-469a-80ab-c28b7a8b9160.png)
  
Si les deux clés Azure Key Vault d'une seule stratégie de chiffrement de données (DEP) ne sont pas disponibles, Office 365 peut utiliser la clé de disponibilité pour passer à une nouvelle DEP. Office 365 détermine s'il faut utiliser la clé de disponibilité pour la disponibilité du service différemment selon qu'une activité initiée par l'utilisateur, par exemple, lorsqu'un utilisateur télécharge du courrier électronique vers le client Outlook ou une activité initiée par le système, telle que l'indexation le contenu des boîtes aux lettres ou les recherches de découverte électronique déclenchait le processus.
  
Office 365 suit ce processus en réponse aux actions initiées par l'utilisateur pour déterminer s'il faut utiliser la clé de disponibilité pour les boîtes aux lettres des utilisateurs:
  
1. Office 365 lit la DEP à laquelle la boîte aux lettres est affectée afin de déterminer l'emplacement des deux clés de client dans le coffre-fort de clés Azure.
    
2. Office 365 choisit de manière aléatoire l'une des deux clés de client de la DEP et envoie une demande au coffre-fort de clés Azure pour désencapsuler la clé DEP à l'aide de la clé client.
    
3. Si la demande d'empaquetage de la clé DEP à l'aide de la clé client échoue et renvoie une erreur, Office 365 envoie une deuxième demande à la chambre forte des clés Azure, ce qui lui demande d'utiliser l'autre clé (deuxième) client.
    
4. Si la deuxième demande d'empaquetage de la clé DEP à l'aide de la clé client échoue et renvoie une erreur, Office 365 examine les résultats des deux requêtes:
    
  - Si l'examen détermine que les erreurs ne reflètent pas une action explicite de l'identité d'un client, Office 365 utilise la clé de disponibilité pour déchiffrer la clé DEP. La clé DEP est ensuite utilisée pour déchiffrer la clé de boîte aux lettres et terminer la demande de l'utilisateur.
    
    Dans ce cas, le coffre-fort de clés Azure ne peut pas répondre ou être inaccessible pour une raison quelconque. Office 365 n'a aucun moyen de déterminer si le client a refusé intentionnellement l'accès aux clés.
    
  - Si l'examen indique qu'une action délibérée a été effectuée pour rendre les clés du client indisponibles, la clé de disponibilité n'est pas utilisée, la demande de l'utilisateur échoue et l'utilisateur reçoit un message d'erreur, tel qu'un échec de connexion.
    
    Dans ce cas, le client est conscient que le service est concerné et la condition de la clé client est défectueuse. Par exemple, si un client utilise une seule DEP pour toutes les boîtes aux lettres de l'organisation, le client peut être confronté à un échec très répandu où les utilisateurs ne peuvent pas accéder à leur boîte aux lettres. Cela garantit que lorsque les deux clés client sont défectueuses, le client est informé de la nécessité de corriger la situation et de restaurer le service à un état sain.
    
 **Utilisation de la clé de disponibilité pour les actions lancées par le code de service Office 365.**
  
Le code de service Office 365 a toujours un jeton de connexion valide et ne peut pas être bloqué. Par conséquent, tant que la clé de disponibilité n'a pas été supprimée, elle peut être utilisée pour les actions lancées par le code de service Office 365 par le biais de ou internes, comme la création d'index de recherche ou le transfert de boîtes aux lettres.
  
 **Utilisation de la clé de disponibilité pour récupérer suite à une perte de clé.**
  
Vous pouvez utiliser la clé de disponibilité pour récupérer à partir de la perte de clés Azure Key Vault associées à la même DEP, comme décrit dans la réponse à l'entrée FAQ «si mes clés sont détruites, comment puis-je récupérer?».
  
## <a name="how-is-the-availability-key-used-with-sharepoint-online-and-onedrive-for-business"></a>Comment la clé de disponibilité est-elle utilisée avec SharePoint Online et OneDrive entreprise?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

L'architecture et l'implémentation de SharePoint Online et OneDrive entreprise et de la clé de disponibilité client diffèrent d'Exchange Online et de Skype entreprise.
  
Lorsqu'un client passe à des clés gérées par le client, Office 365 crée une clé intermédiaire propre au client (TIK). Office 365 chiffre le TIK deux fois, une fois avec chacune des clés de client, et stocke les deux versions chiffrées du TIK. Seules les versions chiffrées de TIK sont stockées, et un TIK peut uniquement être déchiffré avec les clés client. Le TIK est ensuite utilisé pour chiffrer les clés de site, qui sont ensuite utilisées pour chiffrer les clés BLOB. Les objets BLOB eux-mêmes sont chiffrés et stockés dans le service de stockage BLOB Microsoft Azure.
  
Office 365 suit ce processus pour accéder à un objet BLOB qui contient des données de fichier client:
  
1. DéChiffrer le TIK à l'aide de la clé client.
    
2. Utilisez la TIK déchiffrée pour déchiffrer une clé de site.
    
3. Utilisez la clé de site déchiffrée pour déchiffrer une clé BLOB.
    
4. Utilisez la clé BLOB déchiffrée pour déchiffrer le BLOB.
    
Lors du déchiffrement d'un TIK, Office 365 émet deux demandes de déchiffrement vers Azure Key Vault avec un décalage léger. Le premier à terminer fournit le résultat, annulant l'autre requête.
  
Si le client perd l'accès à ses clés client, Office 365 chiffre également le TIK avec une clé de disponibilité et le stocke avec le TIKs chiffré avec chaque clé client. La TIK chiffrée avec la clé de disponibilité est utilisée uniquement lorsque le client appelle Microsoft pour inscrire le chemin de récupération lorsqu'il perd l'accès à ses clés, de manière malveillante ou accidentelle.
  
Pour des raisons de disponibilité et d'envergure, les TIKs déchiffrées sont mises en cache dans un cache de mémoire à limite de temps. Deux heures avant la date d'expiration d'un cache TIK, Office 365 tente de déchiffrer chaque TIK. Le déChiffrement du TIKs prolonge la durée de vie du cache. Si le déchiffrement d'TIK échoue pendant une durée considérable, Office 365 génère une alerte pour notifier l'ingénierie avant l'expiration du cache. Uniquement si le client appelle Microsoft Office 365 lancer l'opération de récupération, ce qui implique le déchiffrement de l'TIK avec la clé de disponibilité stockée dans le magasin secret de Microsoft et l'intégration de nouveau au client à l'aide de l'TIK déchiffrée et d'un nouveau jeu de clés Azure Key Vault fournies par le client.
  
À l'heure actuelle, la clé client est impliquée dans la chaîne de chiffrement et de déchiffrement des données de fichier SharePoint Online stockées dans le magasin d'objets BLOB Azure, mais pas dans les éléments de liste SharePoint Online ou les métadonnées stockées dans la base de données SQL. Office 365 n'utilise pas la clé de disponibilité pour SharePoint Online ou OneDrive entreprise autre que le cas décrit ci-dessus, qui est initié par le client. L'accès humain aux données client est protégé par le référentiel sécurisé du client.
  
## <a name="how-is-customer-key-licensed"></a>Comment la clé client est-elle sous licence?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

La clé client est proposée dans la suite Office 365 Enterprise, «E5» et la référence SKU de conformité avancée. En outre, les clients doivent également acheter la licence appropriée pour utiliser Azure Key Vault.
  
Chaque utilisateur bénéficiant de la clé client doit être titulaire d'une licence s'il souhaite être couvert par la clé client.
  
Pour SharePoint Online, l'administrateur Office 365 qui configure la clé client doit également disposer d'une licence pour effectuer les étapes de configuration. En outre, les utilisateurs qui bénéficient de cette fonctionnalité doivent être titulaires d'une licence, notamment le propriétaire du site et les utilisateurs qui accèdent aux fichiers sur un ou plusieurs sites qui sont chiffrés à l'aide de la clé client. Les utilisateurs externes n'ont pas besoin d'être titulaires d'une licence pour accéder aux fichiers sur un ou plusieurs sites chiffrés à l'aide de la clé client.
  
Pour Exchange Online, les boîtes aux lettres «utilisateur» et «utilisateur de messagerie» doivent être sous licence. Toutes les autres, telles que les boîtes aux lettres partagées, ne doivent pas obligatoirement disposer d'une licence pour la clé client. Pour vérifier que votre boîte aux lettres Exchange Online dispose d'une licence correcte, exécutez l'applet de commande suivante:
  
```
(Get-Mailbox <alias >).PersistedCapabilities
```

Si la chaîne BPOS_S_EquivioAnalytics existe, la boîte aux lettres dispose d'une licence correcte. Si ce n'est pas le cas, vous devez appliquer la licence appropriée afin d'utiliser la fonctionnalité clé client pour cette boîte aux lettres.
  
## <a name="can-i-enable-customer-key-for-a-trial-subscription"></a>Puis-je activer la clé client pour un abonnement d'évaluation?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. Par définition, les abonnements d'essai ont une durée de vie limitée. Les clés de chiffrement hébergées dans les abonnements d'évaluation peuvent être perdues à la fin de la durée de vie de la version d'évaluation. Étant donné que Microsoft ne peut pas empêcher les clients de placer des données client importantes dans les abonnements à la version d'évaluation, l'utilisation d'une clé client avec des abonnements d'essai est interdite.
  
## <a name="how-much-will-using-customer-key-cost"></a>Combien va utiliser le coût clé client?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

En plus de la licence requise pour la clé client, les clients se verront attribuer un coût pour l'utilisation du coffre-fort. Les détails relatifs à la tarification de la [chambre forte des clés Azure](https://azure.microsoft.com/en-us/pricing/details/key-vault/) décrivent le modèle de coût et vous aideront à l'estimer. Il n'existe aucun moyen de prédire le coût exact qu'un client doit supporter car les modèles d'utilisation varient. L'expérience a démontré que le coût est très faible et qu'il tombe généralement entre $0,002 et $0,005 par utilisateur et par mois plus le coût des clés sauvegardées par HSM. Le coût varie également en fonction de la configuration de journalisation choisie par le client et de la quantité de stockage Azure utilisée pour les journaux de coffre-fort de clés Azure. 
  
## <a name="for-more-information"></a>Pour plus d'informations
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Pour commencer à utiliser la clé client, consultez [la rubrique contrôle de vos données dans Office 365 à l'aide de la clé client](controlling-your-data-using-customer-key.md).
  

