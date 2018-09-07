---
title: Réduire le courrier indésirable dans Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 07824c51-2c45-4005-8596-03c0d7c4ff2a
description: Découvrez les méthodes fréquemment utilisées pour réduire le courrier indésirable dans Office 365.
ms.openlocfilehash: e462bbb11862d795650b6378cd5de2681f0edf74
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528181"
---
# <a name="how-to-reduce-spam-email-in-office-365"></a>Réduire le courrier indésirable dans Office 365

 **Vous recevez trop de courrier indésirable dans Office 365 ? Suivez ces conseils.**
  
Dans Office 365, de nombreux problèmes liés au courrier indésirable peuvent être résolus en [affichant les en-têtes de message](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) et en identifiant l’origine du problème. Si un en-tête de message nommé X-Forefront-Antispam-Report contenant la chaîne SFV:NSPM s’affiche, cela signifie qu’Exchange Online Protection (EOP) a analysé le message et ne l’a pas considéré comme du courrier indésirable. Dans ce cas, nous vous recommandons vivement d’[utiliser le complément Message de notification](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) pour nous aider à améliorer nos filtres. Si cette valeur n’apparaît pas dans les en-têtes, cela peut signifier que le message n’a pas été jusqu’au bout de l’analyse de courrier indésirable, ou qu’il y a eu un problème de configuration conduisant le message à être ignoré. Dans ce cas, consultez les informations ci-dessous. 
  
Pour en savoir plus, consultez l’article relatif aux [en-têtes de messages anti-courrier indésirable](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).
  
## <a name="solutions-to-common-causes-of-getting-too-much-spam"></a>Solutions à appliquer en cas de courrier indésirable excessif

Pour éviter que vous receviez trop de courrier indésirable, Exchange Online Protection (EOP) exige que les administrateurs effectuent certaines tâches. Si vous n’êtes pas l’administrateur de votre client Office 365 et que vous recevez trop de courrier indésirable, nous vous recommandons de travailler avec votre administrateur sur ces tâches. Dans le cas contraire, vous pouvez passer directement à la section dédiée aux utilisateurs.
  
### <a name="for-admins"></a>Pour les administrateurs

- **Pointez vos enregistrements DNS vers Office 365** Pour qu’EOP vous protège efficacement du courrier indésirable, les enregistrements DNS de votre serveur de messagerie (MX) pour tous les domaines doivent pointer vers Office 365 uniquement. Si votre [MX ne pointe pas vers Office 365](https://blogs.msdn.microsoft.com/tzink/2017/12/28/if-you-use-office-365-but-your-mx-record-doesnt-point-to-office-you-may-want-to-close-down-your-security-settings/), EOP ne filtre pas le courrier indésirable pour vos utilisateurs. Consultez l’article sur la [création d’enregistrements DNS pour Office 365 pendant la gestion de vos enregistrements DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).
    
- **Activez la règle de courrier indésirable dans toutes les boîtes aux lettres** L’action de filtrage du courrier indésirable est définie par défaut sur **Déplacer le message vers le dossier Courrier indésirable**. S’il s’agit de l’action favorite active de la stratégie anti-courrier indésirable, [la règle de courrier indésirable doit également être activée](https://blogs.msdn.microsoft.com/tzink/2017/12/14/making-sure-your-junk-email-filtering-is-enabled-in-office-365/) dans chaque boîte aux lettres. Pour le vérifier, vous pouvez exécuter la cmdlet Get-MailboxJunkEmailConfiguration dans une ou plusieurs boîtes aux lettres. Par exemple, vous pouvez vérifier toutes les boîtes aux lettres en exécutant la commande suivante : Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}
    
    Quand le résultat s’affiche, la propriété Enable doit être définie sur True. Si elle est définie sur False, vous pouvez exécuter la commande Set-MailboxJunkEmailConfiguration pour la définir sur True.
    
- **Vérifiez vos règles de flux de messagerie et vos listes d’expéditeurs autorisés** Vérifiez l’en-tête d’un message qui aurait dû être marqué comme courrier indésirable. Repérez la propriété SCL dans l’en-tête X-Forefront-Antispam-Report. Si la valeur SCL est égale à -1, cela signifie que le message a été autorisé et a contourné le filtre anti-courrier indésirable d’EOP. Examinez les règles de flux de messagerie, les listes vertes et la liste d’expéditeurs autorisés du destinataire. Consultez également l’article [Détecter et résoudre les problèmes de remise des messages en tant qu’administrateur d’Office 365 pour les entreprises](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) pour savoir pourquoi un message a reçu une valeur SCL de -1. 
    
- **Créez des règles de flux de messagerie dans Exchange Server local** Si vous utilisez Exchange Online Protection, mais que vos boîtes aux lettres se trouvent dans l’environnement Exchange Server local, créez des règles de flux de messagerie dans l’environnement Exchange Server local. Consultez les [instructions relatives à EOP](https://technet.microsoft.com/library/ms.exch.eac.EditAntispamPolicy_SpamAction%28EXCHG.150%29.aspx?v=15.20.548.14&amp;l=1&amp;s=BPOS_S_E15_0).
    
- **Marquez le courrier en nombre comme courrier indésirable** Le courrier en nombre désigne le courrier auquel les utilisateurs peuvent être abonnés mais qui est considéré comme indésirable. Dans l’en-tête de messages X-Microsoft-Antispam, recherchez la propriété BCL (seuil de probabilité de courrier en nombre). Si cette valeur est inférieure au seuil défini dans le filtre anti-courrier indésirable, nous vous recommandons d’ajuster ce seuil pour que ces messages en nombre soient marqués comme courrier indésirable. Les utilisateurs tolèrent différemment le courrier en nombre et ont différentes préférences concernant son [traitement](https://blogs.msdn.microsoft.com/tzink/2014/08/25/different-levels-of-bulk-mail-filtering-in-office-365/). Vous pouvez créer des stratégies ou des règles différentes selon les préférences des utilisateurs. 
    
- **Bloquez immédiatement un expéditeur** Si vous devez immédiatement bloquer un expéditeur, vous pouvez bloquer son adresse e-mail, son domaine ou son adresse IP. Consultez l’article sur le [blocage du courrier indésirable avec le filtre Office 365 pour éviter les faux négatifs](block-email-spam-to-prevent-false-negatives.md). Une entrée dans la liste verte d’un utilisateur final peut remplacer un blocage défini par l’administrateur.
    
- **Activez le complément Message de notification pour les utilisateurs** Nous vous recommandons vivement d’[activer le complément Message de notification pour vos utilisateurs](enable-the-report-message-add-in.md). En tant qu’administrateur, vous pouvez également consulter les commentaires envoyés par vos utilisateurs et utiliser des modèles pour ajuster les paramètres qui peuvent être à l’origine des problèmes.
    
### <a name="for-users"></a>Pour les utilisateurs

- **Activez la règle de courrier indésirable et vérifiez votre liste verte** Vérifiez que la règle de l’action anti-courrier indésirable est activée et que l’expéditeur ou le domaine de l’expéditeur ne peut pas être remplacé dans votre liste verte. Pour accéder à ces paramètres, accédez aux paramètres du courrier indésirable [Bloquer ou autoriser](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). Ici, vous pouvez également choisir de bloquer l’adresse e-mail ou le domaine de l’expéditeur.
    
- **Signalez le courrier indésirable à Microsoft** Signalez les messages indésirables à Microsoft à l’aide du [complément Message de notification](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Vous pouvez également envoyer un message à junk@office365.microsoft.com et joindre un ou plusieurs messages au rapport.
    
    **Important** Si vous ne transférez pas les messages en pièces jointes, [les en-têtes seront manquants et nous ne serons pas en mesure d’améliorer](https://blogs.msdn.microsoft.com/tzink/2017/11/30/when-creating-support-tickets-about-spam-be-sure-to-include-message-headers/) le filtre anti-courrier indésirable dans Office 365. 
    
- **Désabonnez-vous du courrier en nombre** Si vous vous êtes abonné à ce message (bulletin d’informations, annonce de produit, etc.) et qu’il contient un lien Se désabonner provenant d’une source de confiance, nous vous recommandons simplement de vous désabonner. Généralement, Office 365 ne traite pas ces messages comme du courrier indésirable. Vous pouvez également choisir de bloquer l’expéditeur, ou de demander à votre administrateur de modifier les paramètres pour que tout le courrier en nombre soit traité comme du courrier indésirable. 
    

