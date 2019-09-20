---
title: Réduire le courrier indésirable dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 06/07/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: 07824c51-2c45-4005-8596-03c0d7c4ff2a
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_IP
description: Découvrez les méthodes fréquemment utilisées pour réduire le courrier indésirable dans Office 365.
ms.openlocfilehash: d99b5e1452c60be713f0f4cfbab965d30eeeb8ef
ms.sourcegitcommit: bc25ea19c0b6d318751eadc4f27902b0054d5e2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2019
ms.locfileid: "36054706"
---
# <a name="how-to-reduce-spam-email-in-office-365"></a>Réduire le courrier indésirable dans Office 365

 **Vous recevez trop de courrier indésirable dans Office 365 ? Suivez ces conseils.**
  
Nous vous recommandons vivement de signaler les messages de type « Faux négatifs » à l’aide du [complément Signaler le message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) pour nous aider à améliorer nos filtres. Vous pouvez également nous soumettre le message pour examen à l’aide de l’[Explorateur de soumissions](admin-submission.md).

> [!TIP]
> Si vous pensez qu’il s’agit d’un message indésirable et qu’il se trouve dans le dossier Courrier indésirable, cela ne devrait pas poser de problème. Si vous ne voulez pas le voir dans la boîte de réception, vous devez modifier la stratégie anti-courrier indésirable pour mettre le message en quarantaine. Pour plus d’informations sur la mise en quarantaine d’un message, consultez l’article relatif à la [mise en quarantaine des courriers électroniques dans Office 365](quarantine-email-messages.md).

## <a name="fixing-allowed-spam"></a>Résolution du courrier indésirable autorisé

Souvent, les clients reçoivent des courriers indésirables dans leur boîte de réception en raison de configurations incorrectes. Le plus souvent, les domaines sont configurés dans une règle de flux de messagerie (également connue sous le nom de règle de transport) de sorte à contourner des filtres ou ils sont ajoutés à la liste des expéditeurs autorisés/approuvés. Cette configuration est incorrecte, car les messages ne sont pas filtrés par le filtre anti-courrier indésirable, alors qu’ils auraient pu être détectés par ailleurs.  

## <a name="solutions-to-other-common-causes-of-getting-too-much-spam"></a>Solutions à appliquer en cas de courrier indésirable excessif

Pour éviter que vous receviez trop de courrier indésirable, Exchange Online Protection (EOP) exige que les administrateurs effectuent certaines tâches. Si vous n’êtes pas l’administrateur de votre client Office 365 et que vous recevez trop de courrier indésirable, nous vous recommandons de travailler avec votre administrateur sur ces tâches. Dans le cas contraire, vous pouvez passer directement à la section dédiée aux utilisateurs.
  
### <a name="for-admins"></a>Pour les administrateurs

- **Pointez vos enregistrements DNS vers Office 365** Pour qu’EOP vous protège au mieux du courrier indésirable, les enregistrements DNS de votre serveur de messagerie (MX) pour tous les domaines doivent pointer vers Office 365 uniquement. Consultez l’article sur la [création d’enregistrements DNS pour Office 365 pendant la gestion de vos enregistrements DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).
    
- **Activez la règle de courrier indésirable dans toutes les boîtes aux lettres** L’action de filtrage du courrier indésirable est définie par défaut sur **Déplacer le message vers le dossier Courrier indésirable**. S’il s’agit de l’action favorite active de la stratégie anti-courrier indésirable, [la règle de courrier indésirable doit également être activée](https://support.office.com/fr-FR/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089) dans chaque boîte aux lettres. Pour le vérifier, vous pouvez exécuter la cmdlet Get-MailboxJunkEmailConfiguration dans une ou plusieurs boîtes aux lettres. Par exemple, vous pouvez vérifier toutes les boîtes aux lettres en exécutant la commande suivante : Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}
    
    Lorsque le résultat s’affiche, la propriété Enable doit être définie sur True. Si elle est définie sur False, vous pouvez exécuter Set-MailboxJunkEmailConfiguration pour la définir sur True, comme suit : Set-MailboxJunkEmailConfiguration -Identity $values.UserPrincipalName -Enabled $true.
    
- **Créez des règles de flux de messagerie dans Exchange Server local** Si vous utilisez Exchange Online Protection, mais que vos boîtes aux lettres se trouvent dans l’environnement Exchange Server local, créez des règles de flux de messagerie dans l’environnement Exchange Server local. Consultez les [instructions relatives à EOP](https://docs.microsoft.com/previous-versions/exchange-server/exchange-150/jj900470(v=exchg.150)).
    
- **Marquez le courrier en nombre comme courrier indésirable** Le courrier en nombre désigne le courrier auquel les utilisateurs peuvent être abonnés mais qui est considéré comme indésirable. Dans l’en-tête de messages X-Microsoft-Antispam, recherchez la propriété BCL (seuil de probabilité de courrier en nombre). Si cette valeur est inférieure au seuil défini dans le filtre anti-courrier indésirable, nous vous recommandons d’ajuster ce seuil pour que ces messages en nombre soient marqués comme courrier indésirable. Les utilisateurs tolèrent différemment le courrier en nombre et ont différentes préférences concernant son [traitement](https://docs.microsoft.com/fr-FR/office365/SecurityCompliance/bulk-complaint-level-values). Vous pouvez créer des stratégies ou des règles différentes selon les préférences des utilisateurs. 
    
- **Bloquer immédiatement un expéditeur** : si vous devez immédiatement bloquer un expéditeur, vous pouvez bloquer son adresse de courrier, son domaine ou son adresse IP. Si vous souhaitez en savoir plus, veuillez consulter la page [Créer des listes d’expéditeurs bloqués dans Office 365](create-block-sender-lists-in-office-365.md). Une entrée dans la liste verte d’un utilisateur final peut remplacer un blocage défini par l’administrateur.
    
- **Activer le complément Signaler le message pour les utilisateurs** : nous vous recommandons vivement d’[activer le complément Signaler le message pour vos utilisateurs](enable-the-report-message-add-in.md).

- **Utiliser l’[Explorateur de soumissions](admin-submission.md)**  : les administrateurs Office 365 peuvent désormais utiliser un ID de fichier ou de message réseau pour transmettre à Microsoft des courriers électroniques, des URL et des fichiers à analyser. En tant qu’administrateur, vous pouvez normalement consulter les commentaires de vos utilisateurs et utiliser des modèles pour régler les paramètres pouvant poser problème.

- **Autoriser [DKIM](use-dkim-to-validate-outbound-email.md)** à signer tous vos messages sortants pour renforcer la sécurité dans votre domaine et client.
 > [!TIP]
> Après avoir activé DKIM vous devez activer [DMARC](use-dkim-to-validate-outbound-email.md) étant donné que cet enregistrement permet de valider si DKIM et SPF fonctionnent correctement et généralement, les messages électroniques frauduleux n’ont pas la signature, étant donné qu’Office 365 gère votre clé symétrique publique et privée.
    
### <a name="for-users"></a>Pour les utilisateurs

- **Activez la règle de courrier indésirable et vérifiez votre liste verte** Vérifiez que la règle de l’action anti-courrier indésirable est activée et que l’expéditeur ou le domaine de l’expéditeur ne peut pas être remplacé dans votre liste verte. Pour accéder à ces paramètres, accédez aux paramètres du courrier indésirable [Bloquer ou autoriser](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). Ici, vous pouvez également choisir de bloquer l’adresse e-mail ou le domaine de l’expéditeur.
    
- **Signaler le courrier indésirable à Microsoft** : vous pouvez signaler le courrier indésirable à Microsoft à l’aide du complément [Signaler le message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
       
- **Désabonnez-vous du courrier en nombre** Si vous vous êtes abonné à ce message (bulletin d’informations, annonce de produit, etc.) et qu’il contient un lien Se désabonner provenant d’une source de confiance, nous vous recommandons simplement de vous désabonner. Généralement, Office 365 ne traite pas ces messages comme du courrier indésirable. Vous pouvez également choisir de bloquer l’expéditeur, ou de demander à votre administrateur de modifier les paramètres pour que tout le courrier en nombre soit traité comme du courrier indésirable.
