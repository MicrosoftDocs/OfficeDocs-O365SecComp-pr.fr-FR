---
title: Chiffrement de service avec la clé de client pour le Forum aux questions sur Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 41ae293a-bd5c-4083-acd8-e1a2b4329da6
description: Outre la planification, le chiffrement au niveau du volume qui est activé par le biais de BitLocker et distribué clé Manager (DKM), Office 365 offre un niveau supplémentaire de chiffrement au niveau des applications de contenu client dans Office 365, notamment les données à partir d’Exchange En ligne, Skype pour les entreprises, SharePoint Online et OneDrive for Business. Il s’agit de chiffrement du service.
ms.openlocfilehash: 38731d22b78274e42b0886c41884a0395d8df69f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559239"
---
# <a name="service-encryption-with-customer-key-for-office-365-faq"></a>Chiffrement de service avec la clé de client pour le Forum aux questions sur Office 365

Outre la planification, le chiffrement au niveau du volume qui est activé par le biais de BitLocker et distribué clé Manager (DKM), Office 365 offre un niveau supplémentaire de chiffrement au niveau des applications de contenu client dans Office 365, notamment les données à partir d’Exchange En ligne, Skype pour les entreprises, SharePoint Online et OneDrive for Business. Il s’agit de chiffrement du service.
  
Clé de client repose sur le chiffrement de service et permet de vous fournir et les clés de contrôle qui sont utilisés pour chiffrer vos données au repos dans Office 365, comme décrit dans les [Termes du contrat de Services en ligne (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx). Clé de client vous permet de répondre aux obligations de conformité car vous contrôler les clés de chiffrement Office 365 utilise pour déchiffrer les données.
  
Pour fournir des commentaires sur la clé client, y compris la documentation, envoyez vos idées, les suggestions et les perspectives à customerkeyfeedback@microsoft.com.
  
## <a name="what-is-service-encryption-with-customer-key"></a>Quel est le chiffrement de service avec la clé client ?

Clé de client est une fonctionnalité qui vous permet de mettre en service et de gérer les clés utilisées pour chiffrer les données au repos dans Office 365. La fonctionnalité exploite le chiffrement service, qui est le chiffrement est effectué par Office 365 Exchange et SharePoint. Chiffrement service offre les avantages au-delà de ce que BitLocker peut fournir - à savoir supérieure défense en profondeur contre les attaques. Chiffrement de service est une contre-mesure forte si une personne malveillante tente de contourner le système de contrôle d’accès Office 365 qui est utilisé pour traiter toutes les demandes d’accès aux données client. Il s’agit, car le chiffrement service signifie qu’un administrateur de serveur n’a pas de contrôle ou même accès au chiffrement des clés et ne pouvez pas désactiver le chiffrement, à la différence avec BitLocker. Par conséquent, une personne malveillante avec un accès administratif à un serveur hébergeant les données du client qui a été chiffrées à l’aide du chiffrement de service ne pourront pas lire les données du client et même si les données chiffrées sont copiées sur le serveur il reste inutile. 
  
## <a name="what-office-365-data-at-rest-is-covered-by-customer-key"></a>Les données d’Office 365 au repos sont couverts par la clé client ?
<a name="WhatDataIsCoveredbyCustomerKey"> </a>

Contenu du site SharePoint Online et les fichiers stockés sur ce site et les fichiers téléchargés vers OneDrive entreprise sont abordées. Contenu de boîte aux lettres Exchange Online (corps du message électronique, des entrées de calendrier et le contenu des pièces jointes de courrier électronique) est traité. Conversations du texte à partir de Skype pour les entreprises sont traitées, mais Skype réunion diffusion des enregistrements et les téléchargements de contenu de réunion Skype ne sont pas couvertes. Diffusion de réunion Skype et Skype réunion les téléchargements de contenu sont chiffrées ainsi que tout autre contenu dans Office 365, mais nous actuellement n’offre contrôle client des clés de chiffrement.
  
## <a name="what-is-the-difference-between-customer-key-and-bring-your-own-key-byok-with-azure-information-protection-for-exchange-online"></a>Quelle est la différence entre la clé client et mettre votre propre clé (BYOK) avec Azure Information Protection pour Exchange Online ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Les deux options permettent de fournir et de contrôler vos propres clés de chiffrement ; Toutefois, le chiffrement service avec la clé client crypte vos données au repos, qui résident dans Office 365 serveurs au repos, tandis que BYOK avec Azure Information Protection pour Exchange Online crypte vos données de transit permanente en ligne et hors connexion protection des messages électroniques et des pièces jointes pour Office 365. Clé de client et BYOK avec Azure Information Protection pour Exchange Online sont complémentaires, et si vous choisissez d’utiliser les touches de service gérés de Microsoft ou votre propre, chiffrer les données au repos transit peut offrir une protection renforcée à partir de attaques malveillantes.
  
BYOK avec Azure Information Protection pour Exchange Online est proposé dans les fonctionnalités d’Office 365 Message Encryption.
  
## <a name="does-office-365-message-encryption-and-bring-your-own-key-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Chiffrement de messages Office 365 et mettre votre propre clé avec la Protection des informations Azure modifie-t-il l’approche de Microsoft aux demandes de données tiers tels que comparaître ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. Chiffrement de messages Office 365 et l’option pour fournir et contrôler vos propres clés de chiffrement avec mettre votre propre clé (BYOK) pour Azure informations Protection (AIP) n’est pas conçu pour répondre à comparaître de l’application de la réglementation. Chiffrement de messages Office 365 avec BYOK pour le point d’installation administrative a été conçu pour la conformité destinées axée clients qui doivent satisfaire aux obligations de conformité internes ou externes. Microsoft prend très au sérieux tiers demandes de données du client. En tant qu’un fournisseur de services en nuage, nous toujours représenter la confidentialité des données du client. En cas de nous obtenons aux citations à comparaître, nous toujours tenter de rediriger le tiers au client afin d’obtenir les informations. (Veuillez lire le blog de Brad Smith : [protéger les données de clients de gouvernement snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Nous publier régulièrement des informations détaillées de la demande de réception [ici](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Voir le [Centre de gestion de la confidentialité de Microsoft](https://www.microsoft.com/en-us/trustcenter/default.aspx) concernant les demandes de données tiers et « Divulgation des données du client » dans les [Termes du contrat de Services en ligne (OST) ](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)pour plus d’informations.
  
## <a name="does-service-encryption-with-customer-key-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Chiffrement de service avec la clé client modifie-t-il l’approche de Microsoft aux demandes de données tiers tels que comparaître ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. Clé de client n’a pas été conçue pour répondre à comparaître de l’application de la réglementation. Il a été conçu pour les clients régulés répondre aux obligations de conformité internes ou externes. Microsoft prend très au sérieux tiers demandes de données du client. En tant qu’un fournisseur de services en nuage, nous toujours représenter la confidentialité des données du client. En cas de nous obtenons aux citations à comparaître, nous toujours tenter de rediriger le tiers au client afin d’obtenir les informations. (Veuillez lire le blog de Brad Smith : [protéger les données de clients de gouvernement snooping](http://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Nous publier régulièrement des informations détaillées de la demande de réception [ici](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Voir le [Centre de gestion de la confidentialité de Microsoft](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data) concernant les demandes de données tiers et « Divulgation des données du client » dans les [Termes du contrat de Services en ligne (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx) pour plus d’informations. 
  
## <a name="is-fasttrack-support-available-for-implementing-customer-key"></a>Prise en charge FastTrack n’est disponible pour l’implémentation de clé de client ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. FastTrack est uniquement utilisée pour recueillir des informations de configuration de client et de service qui est requises pour s’inscrire pour la clé client. La clé client offre sont publiés par le biais de FastTrack afin qu’il soit pratique pour les clients et partenaires à envoyer ces informations nécessaires à l’aide de la même méthode et facilite l’archivage des données qui fournissent des clients de l’offre.
  
Si vous avez besoin d’une assistance supplémentaire au-delà de la documentation, contactez Microsoft Consulting Services (MCS), Premier champ Engineering (PFE) ou un partenaire Microsoft.
  
## <a name="if-my-keys-are-destroyed-how-can-i-recover"></a>Si mes clés sont détruits, comment puis-je récupérer ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

La clé de disponibilité vous offre la possibilité de récupérer à partir de la perte de clés racine que vous gérez inattendue. Si vous perdez vos clés racine, contacter le Support de Microsoft et Microsoft vous aideront dans le processus d’activation de la clé de disponibilité. Vous allez utiliser la clé de disponibilité pour migrer vers une nouvelle stratégie de chiffrement des données avec de nouvelles clés mis en service par vous. 
  
## <a name="what-is-the-availability-key"></a>Quelle est la clé de disponibilité ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

La clé de disponibilité est une clé racine qui est mis en service lorsque vous créez une stratégie de chiffrement des données. La clé de disponibilité est stockée et protégée dans Office 365 et est similaire aux clés deux racine qui sont fournis par vous pour une utilisation avec le chiffrement de service avec la clé client. Contrairement aux clés que vous fournissez et gérer dans Azure clé coffre-fort, vous ne pouvez pas accéder directement à la clé de disponibilité. Stockage et contrôle de la clé de disponibilité sont délibérément différents de clés Azure clé coffre-fort pour trois raisons : tout d’abord, la clé de disponibilité fournit une fonctionnalité de haute disponibilité dans le cas où des services Office 365 ne peuvent pas accéder clés hébergés dans Azure clé Coffre-fort ; Ensuite, la clé de disponibilité fournit une fonctionnalité « arrêt verre » dans le cas où les deux clés Azure clé coffre-fort sont perdues ; et enfin, la séparation des contrôles logiques fournit la défense en profondeur et protège contre la perte de toutes les clés à partir d’une seule attaque ou point de défaillance. Partage de la responsabilité pour protéger les clés, lors de l’utilisation des protections et des processus de gestion de clés, réduit finalement le risque que toutes les clés (et par conséquent vos données) seront perdues ou détruites. Microsoft offre seuls à pouvoir par la destruction de la clé de disponibilité. Par leur conception, personne chez Microsoft a accès à la clé de la disponibilité : elle est uniquement accessible par le code du service Office 365.
  
## <a name="how-many-data-encryption-policies-deps-can-i-create"></a>Stratégies de chiffrement de données (Dép.) combien puis-je créer ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype pour les entreprises :** Vous pouvez créer jusqu'à 50 Dép.. 
  
 **SharePoint Online et OneDrive for Business :** Un PED s’applique aux données dans un emplacement géographique, également appelé une geo. Si vous utilisez la fonctionnalité multi-geo d’Office 365, vous pouvez créer un PED par localisés. Si vous n’utilisez pas multi-localisés, vous pouvez créer un dépôt
  
## <a name="can-i-assign-a-data-encryption-policy-before-migrating-a-mailbox-to-the-cloud"></a>Puis-je affecter une stratégie de chiffrement des données avant de migrer une boîte aux lettres vers le nuage ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Oui. Vous pouvez utiliser l’applet de commande Windows PowerShell Set-MailUser pour attribuer une stratégie de chiffrement des données (PED) à l’utilisateur avant de migrer les boîtes aux lettres vers Office 365. Lorsque vous effectuez cette opération, le contenu de la boîte aux lettres est chiffré à l’aide de la prévention affectée comme le contenu est migré. Cela peut être plus efficace que l’attribution d’un PED après que la boîte aux lettres a déjà été migré et puis en attente pour le chiffrement ait lieu, ce qui peut prendre plusieurs jours heures ou éventuellement. 
  
## <a name="how-do-i-verify-that-encryption-with-customer-key-is-activated-and-office-365-has-finished-encrypting-with-customer-key"></a>Comment vérifier que le chiffrement avec la clé client est activé et Office 365 a terminé, EFS avec la clé client ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype pour les entreprises :** Vous pouvez [vous connecter à Exchange Online PowerShell à distance](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , puis utilisez l’applet de commande **[Get-MailboxStatistics]** pour chaque boîte aux lettres que vous voulez vérifier. Dans la sortie de l’applet de commande Get-MailboxStatistics, la propriété _IsEncrypted_ renvoie la valeur **true** si la boîte aux lettres est chiffré et la valeur **false** si elle n’est pas. Si la boîte aux lettres est chiffré, la valeur renvoyée par la propriété _DataEncryptionPolicyID_ est le GUID de la prévention dont la boîte aux lettres est chiffré. Pour plus d’informations sur l’exécution de cette applet de commande, voir [Get-MailboxStatistics](https://technet.microsoft.com/en-us/library/bb124612%28v=exchg.160%29.aspx) et à l’aide de PowerShell avec Exchange Online. 
  
Si les boîtes aux lettres ne sont pas chiffrées après avoir attendu 72 heures depuis le moment où vous avez affecté la prévention, d’initier un déplacement de boîte aux lettres. Pour ce faire, [se connecter à Exchange Online à l’aide de PowerShell à distance](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) et utilisez l’applet de commande New-MoveRequest et entrer l’alias de la boîte aux lettres comme suit : 
  
```
New-MoveRequest <alias>
```

 **SharePoint Online et OneDrive for Business :** Vous pouvez [vous connecter à SharePoint Online PowerShell](https://technet.microsoft.com/en-us/library/fp161372.aspx), puis utilisez l’applet de commande **[Get-SPODataEncryptionPolicy]** pour vérifier l’état de votre client. Le ** _état_** propriété renvoie la valeur **enregistré** si le chiffrement de la clé client est activé et tous les fichiers dans tous les sites ont été chiffrés. Si le chiffrement est en cours d’exécution, cette applet de commande fournit des informations sur le pourcentage de sites est terminé. 
  
## <a name="if-i-want-to-switch-to-a-different-set-of-keys-how-long-does-it-take-for-the-new-set-of-keys-to-protect-my-data"></a>Si je souhaite basculer vers un autre jeu de clés, combien de temps faut-il pour le nouveau jeu de clés pour protéger mes données ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype pour les entreprises :** Cela peut prendre jusqu'à 72 heures pour protéger une boîte aux lettres selon une stratégie de chiffrement nouvelles données (PED) depuis le moment où que le nouveau PED est affectée à la boîte aux lettres. 
  
 **SharePoint Online et OneDrive for Business :** Cela peut prendre jusqu'à quatre heures pour chiffrer à nouveau votre ensemble client lorsqu’une nouvelle clé a été affectée. 
  
## <a name="is-my-existing-data-stored-without-encryption-at-any-time-while-it-is-decrypted-or-encrypted-with-customer-key"></a>Mes données existantes stockées sans chiffrement à tout moment lorsqu’elle est déchiffré ou chiffré avec la clé client ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. Vos données sont toujours chiffrées au repos dans le service Office 365 avec BitLocker et DKM. Pour plus d’informations, voir le « sécurité, de confidentialité et les informations de conformité pour Office 365 » et [comment Exchange Online protège les secrets de votre courrier électronique](https://support.office.com/article/989BA10C-F73F-4EFB-AD1B-AF3322E5F376).
  
## <a name="if-i-no-longer-want-to-use-customer-managed-encryption-keys-can-i-switch-to-microsoft-managed-keys"></a>Si je ne souhaitez plus utiliser des clés de chiffrement de client géré, puis-je basculer clés gérés par Microsoft ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype pour les entreprises :** Pas encore. Il sera prise en charge une fois que le chiffrement dans Office 365 service des clés gérés par Microsoft est déployée globalement. Nous pensons que ce déploiement soit effectué dans le service après que nous chiffrement du service de publication avec la clé client. 
  
 **SharePoint Online et OneDrive for Business :** Oui. Vous pouvez choisir de revenir à l’utilisation de clés gérés par Microsoft séparément pour chaque localisés (si vous utilisez la fonctionnalité multi-geo) ou pour toutes vos données si elle est dans un seul localisés. 
  
## <a name="if-i-lose-my-keys-how-long-does-it-take-to-recover-service-availability-using-the-recovery-key"></a>Si j’ai perdent mes clés, combien de temps faut-il pour récupérer la disponibilité du service à l’aide de la clé de récupération ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online et Skype pour les entreprises :** Lorsque vous appelez utiliser la clé de la disponibilité, les boîtes aux lettres seront accessibles dans les minutes. 
  
 **SharePoint Online et OneDrive for Business :** Cette opération est proportionnelle au nombre de sites que vous avez. Une fois que vous appelez Microsoft pour utiliser la clé de la disponibilité, vous serez entièrement en ligne au sein d’environ quatre heures. 
  
## <a name="how-is-the-availability-key-used-with-exchange-online"></a>Comment la clé de disponibilité est utilisée avec Exchange Online ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Il existe trois méthodes que la clé de disponibilité est utilisée avec Exchange Online :
  
- Service de disponibilité - dans le cas où les clés Azure clé coffre-fort sont inaccessibles.
    
- Actions initiées par le code du service Office 365 - telles que création d’index de recherche ou de déplace de boîte aux lettres.
    
- Récupérer à partir de la perte de clés - tels que la perte de deux clés Azure clé coffre-fort associé à une seule prévention
    
 **À l’aide de la clé de disponibilité pour la disponibilité du service dans les événements clés Azure clé coffre-fort sont inaccessibles.**
  
Office 365 utilise la clé de la disponibilité à la fois pour la disponibilité du service et de récupération à partir d’un état défectueux de la clé client pour Exchange Online. Il existe une hiérarchie des clés utilisées par la clé client. Cette hiérarchie est illustrée dans la figure suivante.
  
![](media/a760156b-737f-469a-80ab-c28b7a8b9160.png)
  
Si les deux clés Azure clé coffre-fort d’une stratégie de chiffrement unique données (PED) ne sont pas disponibles, Office 365 peut utiliser la disponibilité clé pour passer à un nouvel Office 365 prévention détermine s’il faut utiliser la clé de disponibilité pour la disponibilité du service différemment selon qu’une activité initiées par l’utilisateur, par exemple, lorsqu’un utilisateur télécharge un courrier électronique pour le client Outlook, ou une activité exécutée par le système, telles que l’indexation du contenu des boîtes aux lettres, ou pour les recherches de découverte électronique, déclenche le processus.
  
Office 365 suit ce processus en réponse aux actions d’initiées par l’utilisateur pour déterminer s’il faut utiliser la clé de la disponibilité des boîtes aux lettres :
  
1. Office 365 lit la PED affectée de la boîte aux lettres afin de déterminer l’emplacement des clés deux client dans Azure clé coffre-fort.
    
2. Office 365 choisit une des deux clients clés à partir de la prévention et envoie une demande à Azure clé coffre-fort pour désencapsuler la clé de la fonctionnalité à l’aide de la clé client de manière aléatoire.
    
3. Si la demande pour désencapsuler la prévention de clé à l’aide de la clé client échoue et renvoie une erreur, Office 365 demande un deuxième Azure clé coffre-fort, cette fois demander au programme d’utiliser l’autre clé de client (seconde).
    
4. Si la deuxième demande pour désencapsuler la clé de la fonctionnalité à l’aide de l’échec de clés client et renvoie une erreur, Office 365 examine les résultats de deux requêtes :
    
  - Si l’examen détermine que les erreurs ne sont pas reflètent une action explicite en une identité de client, Office 365 utilise la clé de disponibilité pour déchiffrer la clé de la fonctionnalité. La prévention clé est ensuite utilisée pour déchiffrer la clé de boîte aux lettres et de terminer la demande de l’utilisateur.
    
    Dans ce cas, Azure clé coffre-fort est incapable de répondre ou inaccessible pour une raison quelconque. Office 365 n’a aucun moyen pour déterminer si le client a révoqué intentionnellement accès aux clés.
    
  - Si l’examen indique cette action délibérée ont été prise pour restituer les clés client non disponible, puis la clé de disponibilité ne sera pas utilisée, la demande de l’utilisateur échoue et l’utilisateur reçoit un message d’erreur, tels que des échecs de connexion.
    
    Dans ce cas, le client soit averti que service est affecté et la condition de la clé client est défectueux. Par exemple, si un client utilise un seul PED pour toutes les boîtes aux lettres dans l’organisation, le client peut rencontrer une défaillance plus répandue où les utilisateurs ne peuvent pas accéder à leurs boîtes aux lettres. Cela garantit que lorsque les deux clés client sont défectueux, le client est informé de la nécessité de corriger la situation et restaurer le service dans un état intègre.
    
 **À l’aide de la clé de disponibilité pour les actions initiées par le code du service Office 365.**
  
Toujours, de code Office 365 service dispose d’un jeton de connexion valide et ne peuvent pas être bloqué. Par conséquent, jusqu'à ce que la clé de la disponibilité a été supprimée, il pouvant servir à actions initiative, ou internes de code du service Office 365, telles que création d’index de recherche ou le déplacement de boîtes aux lettres.
  
 **À l’aide de la clé de la disponibilité à récupérer à partir de la perte de clés.**
  
Vous pouvez utiliser la clé de la disponibilité à récupérer à partir de la perte de deux clés Azure clé coffre-fort qui sont associés à la même PED, comme décrit dans la réponse à l’entrée du Forum aux questions » si mes clés sont détruits, comment puis-je récupérer ? ».
  
## <a name="how-is-the-availability-key-used-with-sharepoint-online-and-onedrive-for-business"></a>Comment la clé de disponibilité est utilisée avec SharePoint Online et OneDrive entreprise ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Et SharePoint Online OneDrive pour l’architecture métier et l’implémentation de la clé de la clé de client et de disponibilité sont différentes dans Exchange Online et Skype pour les entreprises.
  
Lorsqu’un client clés de client géré, Office 365 crée une clé de niveau intermédiaire client spécifique (TIK). Office 365 crypte la TIK à deux reprises, une fois avec chacune des clés de client et stocke les deux versions chiffrées de la TIK. Seules les versions chiffrées de la TIK sont stockées, et un TIK peut uniquement être déchiffré avec les clés de client. Le TIK est ensuite utilisée pour chiffrer les clés de site, qui sont ensuite utilisés pour chiffrer les clés de l’objet blob. Les objets BLOB eux-mêmes sont chiffrées et stockées dans le service de stockage Blob Azure de Microsoft.
  
Office 365 suit ce processus pour accéder à un objet blob qui contient des données de fichier client :
  
1. Déchiffrer le TIK à l’aide de la clé client.
    
2. Utilisez le TIK déchiffré pour déchiffrer une clé de site.
    
3. Utilisez la clé site déchiffré pour déchiffrer une clé blob.
    
4. Utilisez la clé blob déchiffré pour déchiffrer le blob.
    
Lors du déchiffrement un TIK, Office 365 émet deux demandes de déchiffrement à Azure clé coffre-fort avec un décalage de légères. La première personne à fin fournit le résultat, l’annulation de la demande autres.
  
Au cas où le client perd l’accès à leurs clés client, Office 365 également crypte la TIK avec une clé de disponibilité et stocke ce ainsi que les TIKs chiffrés avec la clé de chaque client. Le TIK chiffrée avec la clé de disponibilité est utilisé uniquement lorsque le client appelle Microsoft pour inscrire le chemin d’accès de récupération lorsqu’ils ont perdu l’accès à leurs clés, par accident ou à des fins malveillantes.
  
Pour la disponibilité et à l’échelle raisons, TIKs déchiffrés sont mis en cache dans un cache mémoire limitée dans le temps. Avant de définie un cache TIK à expiration, les deux heures tente de déchiffrer chaque TIK Office 365. Déchiffrement du TIKs étend la durée de vie du cache. Si le déchiffrement TIK échoue pour un temps considérable, Office 365 génère une alerte pour notifier ingénierie avant l’expiration du cache. Uniquement si le client appelle Microsoft Office 365 initier l’opération de récupération, ce qui implique de déchiffrer de que la TIK avec la clé de la disponibilité stockés dans Microsoft magasin secrète et intégration du client en utilisant le déchiffré TIK et un nouvel ensemble clés de Azure clé coffre-fort fourni par le client.
  
À compter d’aujourd'hui, clé client impliquée dans la chaîne de chiffrement et au déchiffrement des données de fichier SharePoint Online stockées dans le magasin d’objets blob Azure, mais pas les éléments de liste SharePoint Online ou des métadonnées stockées dans la base de données SQL. Office 365 n’utilise pas la clé disponibilité, pour SharePoint Online ou OneDrive entreprise autre que le cas ci-dessus, qui est le client qui a initié. Accès utilisateur aux données client est protégé par la zone de sécurité client.
  
## <a name="how-is-customer-key-licensed"></a>La clé client possède une licence ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Clé de client est proposée dans la Suite de contenu d’entreprise Office 365, « E5 » et la référence de conformité avancées. En outre, les clients doivent également acheter la licence appropriée pour l’utilisation de coffre-fort de clé Azure.
  
Chaque utilisateur bénéficiant de clé de client doit s’ils souhaitent être couverts par la clé client de licence.
  
Pour SharePoint Online, l’administrateur Office 365 configure la clé client doit également être sous licence, pour effectuer les étapes de configuration. En outre, les utilisateurs qui bénéficient de la fonctionnalité doivent être sous licence : Cela inclut le propriétaire du site et tous les utilisateurs l’accès aux fichiers sur un ou plusieurs sites sont chiffrés à l’aide de la clé client. Des utilisateurs externes n’est pas obligé de licence lui permettant d’accéder aux fichiers sur un ou plusieurs sites sont chiffrés à l’aide de la clé client.
  
Pour Exchange Online, les boîtes aux lettres « utilisateur » et « messagerie « boîtes aux lettres doivent être une licence. Tous les autres, telles que les boîtes aux lettres partagées, ne sont pas nécessaire d’avoir une licence pour la clé client. Pour vérifier que votre boîte aux lettres Exchange Online est sous licence correctement, exécutez l’applet de commande suivante :
  
```
(Get-Mailbox <alias >).PersistedCapabilities
```

Si la chaîne BPOS_S_EquivioAnalytics existe, puis la boîte aux lettres est sous licence. Si ce n’est pas le cas, vous devez appliquer la licence appropriée pour pouvoir utiliser la fonctionnalité de clé de client pour cette boîte aux lettres.
  
## <a name="can-i-enable-customer-key-for-a-trial-subscription"></a>Puis-je activer la clé client pour un abonnement d’évaluation ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Non. Par définition, les abonnements d’évaluation ont une durée de vie limitée. Clés de chiffrement qui sont hébergées dans les abonnements d’évaluation peuvent être perdues à la fin de la durée de vie d’évaluation. Étant donné que Microsoft ne peut pas et n’empêche pas les clients de placer des données client importantes dans les abonnements d’évaluation, l’utilisation de la clé client avec abonnements d’évaluation est interdite.
  
## <a name="how-much-will-using-customer-key-cost"></a>Quelle sera à l’aide de la clé client coût ?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Outre les licences requises pour la clé client, les clients verront un coût d’utilisation de clé coffre-fort. [Azure clé coffre-fort tarifs](https://azure.microsoft.com/en-us/pricing/details/key-vault/) décrit le modèle de coût et vous aide à l’estimation. Il n’existe aucun moyen de prévoir le coût exact qui prendra en charge les clients varier des modèles d’utilisation. L’expérience a montré que le coût est très faible et généralement se situe dans la plage de 0,002 $ à $0,005 par utilisateur et par mois ainsi que le coût des clés de secours HSM. Le coût varient également en fonction de la configuration de journalisation est choisie par le client et le volume de stockage Azure utilisé pour les journaux de coffre-fort de clé Azure. 
  
## <a name="for-more-information"></a>Pour plus d'informations
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Pour vous familiariser avec la clé client, voir [contrôle de vos données dans Office 365 à l’aide de la clé client](controlling-your-data-using-customer-key.md).
  

