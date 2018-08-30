---
title: Empêcher l’est marqué comme courrier indésirable dans Office 365 et Exchange Online Protection de messagerie
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 74aaade0-efc0-46ac-b949-f2d1d59256fa
description: Conseils pour Office 365 administrateurs empêcher le bon courrier marqué comme courrier indésirable à partir d’est mis en quarantaine comme un faux positif. Personnaliser un listes fiables et autres options pour empêcher le bon courrier marqué comme courrier indésirable.
ms.openlocfilehash: 42b27d237592e95e6d175ab335959bc82269c0f7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527588"
---
# <a name="prevent-email-from-being-marked-as-spam-in-office-365-and-exchange-online-protection"></a>Empêcher l’est marqué comme courrier indésirable dans Office 365 et Exchange Online Protection de messagerie

Des administrateurs Exchange Online ou Exchange Online Protection (EOP) avec les informations d’identification d’un accès approprié peuvent utiliser ces étapes pour vous assurer qu’un message électronique en déplacement via le service n’est pas marqué comme courrier indésirable.
  
Il peut être frustrant pour que le courrier légitime, bonne mis en quarantaine ou bloqué comme du courrier indésirable et le débarquement dans un dossier de quarantaine. Vous pouvez utiliser une liste des expéditeurs approuvés ou une règle de flux de messagerie pour contourner le filtrage du courrier indésirable et empêcher qu’une bonne e-mails marqués comme courrier indésirable. Lorsqu’un message est incorrectement marqué comme courrier indésirable par le filtre de courrier indésirable, il s’agit d’un faux positif. Le filtre de courrier indésirable d’Office 365 offre également des options que les utilisateurs finaux peuvent personnaliser afin d’éviter les faux positifs.
  
Si vous avez besoin pour vous aider à false messagerie négative, autrement dit, un message de courrier indésirable qui obtient lorsqu’il ne doit pas, extraire les conseils présentés dans le [message électronique de blocage du courrier indésirable avec le filtre de courrier indésirable Office 365 pour éviter les problèmes négatifs false](block-email-spam-to-prevent-false-negatives.md).
  
## <a name="eop-only-customers-use-directory-synchronization"></a>Les clients EOP uniquement : utiliser la synchronisation d’annuaires

EOP est un service qui permet de protéger votre organisation contre le courrier indésirable et les programmes malveillants de filtrage des e-mails en nuage. Si vous avez des boîtes aux lettres dans Office 365, ils sont automatiquement protégés par EOP car il fait partie du service. 
  
Si vous êtes un client EOP uniquement, autrement dit, vous abonnez au service EOP pour une utilisation avec Exchange Server locale, vous devez synchroniser les paramètres de l’utilisateur avec le service à l’aide de la synchronisation d’annuaires. Cela garantit que des expéditeurs listes sont respectés par EOP. Pour plus d’informations, voir « Utiliser la synchronisation d’annuaires pour gérer les utilisateurs de messagerie » dans [Manage Mail Users in EOP](https://go.microsoft.com/fwlink/?LinkId=534098).
  
## <a name="prevent-false-positive-email-by-using-the-connection-filters-ip-allow-list"></a>Empêcher la messagerie positif false autoriser la liste à l’aide de la connexion IP du filtre

Si vous trouvez que courrier électronique d’un expéditeur est toujours déplacé vers les dossiers de courrier indésirable dans votre organisation, vous pouvez ajouter adresse IP de l’expéditeur de courrier électronique pour IP de votre filtre connexion de liste verte. En règle générale, cela empêche réponses positives false de cet expéditeur pour tous les destinataires au sein de votre organisation. L’exception se produit lorsqu’un utilisateur Active l’option « sécurisés répertorie uniquement : seuls les messages provenant de personnes ou les domaines figurant dans votre liste des expéditeurs approuvés ou la liste des destinataires approuvés seront remis à votre boîte de réception » dans Outlook et n’ajoute pas de cet expéditeur à la liste des expéditeurs fiables. Pour plus d’informations sur la substitution de cette option, voir [dépannage : un message s’achève dans le dossier courrier indésirable bien EOP a marqué le message comme non spam](prevent-email-from-being-marked-as-spam-0.md#TroubleshootingJunkEOPNonSpam).
  
 **Pour ajouter une adresse IP à votre connexion IP de filtre autorisés**
  
1. Obtenir l’en-tête d’un message envoyé par l’expéditeur que vous souhaitez autoriser. Procéder à partir de votre client de messagerie tels que Outlook ou Outlook sur le Web, comme indiqué dans [l’Analyseur d’en-tête de Message](https://go.microsoft.com/fwlink/p/?LinkId=306583).
    
2. Rechercher manuellement l’adresse IP après la balise CIP dans l’en-tête X-Forefront-Antispam-Report ou à l’aide de l’onglet de **L’Analyseur de Message** de l' [Analyseur de connectivité à distance](https://testconnectivity.microsoft.com/?tabid=mha).
    
3. Ajouter l’adresse IP adresse à l’adresse IP de liste verte en suivant les étapes décrites dans « Utiliser le CAE pour modifier la stratégie de filtrage de connexion par défaut » dans la [configuration de la stratégie de filtrage de connexion](https://go.microsoft.com/fwlink/?LinkId=534132).
    
## <a name="prevent-false-positive-email-by-configuring-spam-filter-policies"></a>Empêcher la messagerie positif false en configurant des stratégies de filtrage du courrier indésirable

Vous pouvez ajouter des adresses de messagerie individuelles ou les domaines à une liste verte en suivant les étapes de [configuration de vos stratégies de filtrage du courrier indésirable](https://go.microsoft.com/fwlink/?LinkID=534136).
  
## <a name="review-your-advanced-spam-filter-policies"></a>Passez en revue vos stratégies de filtrage avancé du courrier indésirable

Si vous avez restriction spéciale définie dans une stratégie de filtrage du courrier indésirable, par exemple, si vous avez un domaine entier, vous devez les consulter pour vérifier si elles risquent de provoquer des faux positifs. Voir [configurer vos stratégies de filtrage du courrier indésirable](https://go.microsoft.com/fwlink/?LinkId=534136)et désactiver les autres [options de filtrage avancé du courrier indésirable](https://go.microsoft.com/fwlink/?LinkId=534137) qui peut entraîner des messages doit être marqué comme courrier indésirable. 
  
## <a name="help-your-end-users-create-a-safe-sender-list-to-prevent-good-email-from-being-marked-as-spam"></a>Aider vos utilisateurs finaux de créer une liste des expéditeurs approuvés pour empêcher la messagerie électronique est marqué comme courrier indésirable
<a name="BKMK_email-user-help-safelist"> </a>

Demandez à vos utilisateurs d’ajouter des adresses des expéditeurs qui ils ont confiance à sa liste des expéditeurs approuvés dans [Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) ou [Outlook sur le Web](https://go.microsoft.com/fwlink/p/?LinkId=294862). Pour commencer dans Outlook sur le Web, choisissez **paramètres**![ConfigureAPowerBIAnalysisServicesConnector_settingsIcon](media/24bd5467-c8d2-4936-9c37-a179bd0e21ec.png) \> **Options** \> **bloquer ou autoriser**. Le diagramme suivant illustre un exemple d’ajout d’un élément à une liste d’expéditeurs autorisés.
  
![Ajout d’un expéditeur fiable dans Outlook Web App](media/8de6b24e-429e-4e8f-8ce8-53ba659cbfcb.png)
  
EOP respecte vos utilisateurs expéditeurs et destinataires, mais pas les domaines approuvés. Cela est vrai même si le domaine est ajouté par le biais de l’Outlook sur le Web, ou ajouté dans Outlook et synchronisés à l’aide de la synchronisation d’annuaire.
  
## <a name="troubleshooting-a-message-ends-up-in-the-junk-folder-even-though-eop-marked-the-message-as-non-spam"></a>Résolution des problèmes : Un message s’achève dans le dossier courrier indésirable bien EOP a marqué le message comme non-spam
<a name="TroubleshootingJunkEOPNonSpam"> </a>

Si vos utilisateurs disposent de l’option dans Outlook activé pour « sécurisés répertorie uniquement : seul courrier provenant de personnes ou les domaines figurant dans votre liste des expéditeurs approuvés ou la liste des destinataires approuvés est remis à votre boîte de réception », puis tous les messages seront dirigés vers le dossier courrier indésirable pour un expéditeur, sauf si l’expéditeur figure dans les destinataires liste des expéditeurs approuvés de pient. Cela se produit, indépendamment de si EOP marque un message comme non spam, ou si vous avez défini une règle dans EOP pour marquer un message comme non spam.
  
Vous pouvez désactiver l’option de listes fiables uniquement pour vos utilisateurs Outlook en suivant les instructions de [Outlook : paramètre de stratégie pour désactiver l’interface utilisateur de courrier indésirable et le mécanisme de filtrage](https://support.microsoft.com/en-us/kb/2180568).
  
Si vous affichez le message dans Outlook sur le Web, il y aura une info-bulle jaune sécurité qui indique que le message est dans le dossier courrier indésirable car l’expéditeur n’est pas dans la liste des expéditeurs approuvés du destinataire.
  
Si vous examinez l’en-tête d’un message, il peut inclure l’horodatage SFV:SKN (adresses IP autorisées ou autoriser ETR) ou SFV:NSPM (non spam), mais le message est toujours placé dans le dossier courrier indésirable de l’utilisateur. Il n’existe rien dans l’en-tête de message qui indique que l’utilisateur a « Listes approuvées uniquement » activée. Dans ce cas car l’option « Listes approuvées uniquement » définie par les utilisateurs dans Outlook remplace le paramètre EOP. 
  
 **Pour vérifier pourquoi un message d’un expéditeur fiable est marqué comme non-spam dans l’en-tête du message, mais toujours se termine dans le dossier courrier indésirable de l’utilisateur**
  
1. Pour plus d’informations pour se connecter à Exchange Online PowerShell, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). 
    
2. Exécutez la commande suivante pour afficher les paramètres de configuration du courrier indésirable de l’utilisateur :
    
  ```
  Get-MailboxJunkEmailConfiguration example@contoso.com | fl TrustedListsOnly,ContactsTrusted,TrustedSendersAndDomains
  ```

    Si TrustedListsOnly est défini sur True, cela signifie que ce paramètre est activé. Si ContactsTrusted est défini sur True, cela signifie que l’utilisateur fait confiance à la fois des Contacts et des expéditeurs approuvés. La TrustedSendersAndDomains répertorie le contenu de la liste des expéditeurs approuvés de l’utilisateur.
    
## <a name="still-need-help"></a>Besoin d’aide ?
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[![Obtenir de l’aide dans les forums de la communauté Office 365](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Administrateurs : Se connecter et créer une demande de service](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Administrateurs : Appelez le support technique](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  
## <a name="see-also"></a>Voir aussi
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[Vue d’ensemble du filtre de courrier indésirable](https://support.office.com/article/5AE3EA8E-CF41-4FA0-B02A-3B96E21DE089)
  
[Bloquer ou autoriser (paramètres de courrier indésirable)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](block-email-spam-to-prevent-false-negatives.md)

