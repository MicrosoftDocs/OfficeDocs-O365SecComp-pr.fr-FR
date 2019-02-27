---
title: Résolution des problèmes de messages envoyés à Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/2/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
ms.collection:
- M365-security-compliance
description: Cet article fournit des informations de dépannage pour les expéditeurs qui rencontrent des problèmes lors de l'envoi d'e-mail à des boîtes de réception dans Office 365 et les meilleures pratiques pour l'envoi de courrier en nombre à des clients Office 365.
ms.openlocfilehash: cfb3901b930b63ef8a33391c673a32a73eaa1b07
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276294"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a>Résolution des problèmes de messages envoyés à Office 365

Cet article fournit des informations de dépannage pour les expéditeurs qui rencontrent des problèmes lors de l'envoi d'e-mail à des boîtes de réception dans Office 365 et les meilleures pratiques pour l'envoi de courrier en nombre à des clients Office 365.
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a>Résolution de problèmes courants liés à la remise de courrier à Office 365

Choisissez un de ces problèmes fréquemment rencontrés.
  
- [Vous gérez la réputation de l'expéditeur de votre IP et domaine ?](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [Vous envoyez des e-mails depuis de nouvelles adresses IP ?](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [Confirmer que votre DNS est configuré correctement](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [Vérifier que vous ne vous annoncez pas sous la forme d'une adresse IP non routable](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [Vous avez reçu une notification d'échec de remise lors de l'envoi de messages électroniques à un utilisateur dans Office 365](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [Mon e-mail s'est retrouvé dans le dossier du courrier indésirable du destinataire dans EOP](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [Le trafic provenant de mon adresse IP est limité par EOP](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a>Vous gérez la réputation de l'expéditeur de votre IP et domaine ?
<a name="ManageRep"> </a>

Les technologies de filtrage EOP sont conçues pour fournir des protections contre le courrier indésirable pour Microsoft Office 365 ainsi que d'autres produits Microsoft tels que Exchange Server, Microsoft Office Outlook et Windows Live Mail. Nous tirons également parti de SPF, DKIM et DMARC ; des technologies d'authentification de messagerie qui aident à résoudre le problème d'usurpation et d'hameçonnage en vérifiant que le domaine qui envoie l'e-mail est autorisé à le faire. Le filtrage EOP est affecté par de nombreux facteurs liés à l'IP d'envoi, le domaine, l'authentification, la précision de la liste, les taux de plaintes, le contenu, etc. Parmi ces facteurs, l'un des facteurs principaux responsable de la baisse de réputation d'un expéditeur et sa capacité à remettre un e-mail est son taux de plainte de courrier indésirable. 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a>Vous envoyez des e-mails depuis de nouvelles adresses IP ?
<a name="NewIPs"> </a>

Les adresses IP qui n'ont pas été utilisées précédemment pour envoyer des e-mails n'ont généralement pas de réputation créée dans nos systèmes. Par conséquent, les e-mails provenant de nouvelles adresses IP ont plus tendance à rencontrer des problèmes de remise. Une fois que l'adresse IP a créé une réputation de non envoi de courrier indésirable, EOP permet généralement une meilleure expérience de remise des courriers électroniques.
  
Les nouvelles adresses IP qui sont ajoutées pour des domaines authentifiés sous des enregistrements SPF existants bénéficient généralement de l’avantage d’hériter de la réputation d’envoi du domaine. Si votre domaine a une bonne réputation d’envoi, les nouvelles adresses IP peuvent expérimenter un temps de montée en puissance plus rapide. Une nouvelle adresse IP pourra être entièrement augmentée au bout de quelques semaines ou plus tôt selon le volume, la précision de la liste et les taux de plaintes de courrier indésirable.
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a>Confirmer que votre DNS est configuré correctement
<a name="ConfirmDNSsetup"> </a>

Pour savoir comment créer et gérer des enregistrements DNS, y compris l'enregistrement MX requis pour le routage du courrier, vous devez contacter votre fournisseur d'hébergement DNS.
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a>Vérifier que vous ne vous annoncez pas sous la forme d'une adresse IP non routable
<a name="NoReverseDNS"> </a>

Il se peut que nous n'acceptions pas les e-mails provenant d'expéditeurs dont la recherche DNS inversée a échoué. Dans certains cas, des expéditeurs légitimes s'annoncent de façon incorrecte sous la forme d'une adresse IP routable non Internet lorsqu'ils tentent d'ouvrir une connexion à EOP. Les adresses IP réservées pour le réseau privé (non routable) incluent :
  
- 192.168.0.0/16 (ou 192.168.0.0 - 192.168.255.255)
    
- 10.0.0.0/8 (ou 10.0.0.0 - 10.255.255.255)
    
- 172.16.0.0/11 (ou 172.16.0.0 - 172.31.255.255)
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a>Vous avez reçu une notification d'échec de remise lors de l'envoi de messages électroniques à un utilisateur dans Office 365
<a name="NDRInbound"> </a>

Certains problèmes de remise sont dus au blocage de l'adresse IP de l'expéditeur par Microsoft ou à l'identification du compte d'utilisateur comme expéditeur interdit en raison des activité de courrier indésirable précédentes. Si vous pensez que vous avez reçu la notification d'échec de remise par erreur, suivez d'abord toutes les instructions indiquées dans le message de notification d'échec de remise pour résoudre le problème. 
  
Pour plus d'informations sur l'erreur que vous avez reçue, consultez la liste complète des codes d'erreur SMTP dans [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).
  
 Par exemple, si vous recevez la notification d'échec de remise suivante, elle indique que l'adresse IP d'envoi a été bloquée par Microsoft. 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
Pour demander la suppression de cette liste, vous pouvez [Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a>Mon e-mail s'est retrouvé dans le dossier du courrier indésirable du destinataire dans EOP
<a name="JunkMailBox"> </a>

Si un message a été incorrectement identifié comme courrier indésirable par EOP, vous pouvez collaborer avec le destinataire pour envoyer ce faux positif à l'équipe d'analyse du courrier indésirable de Microsoft. Selon les résultats de l'analyse, les règles de filtrage de contenu du courrier indésirable du service peuvent être ajustées pour autoriser le message. Vous utilisez la messagerie pour envoyer à Microsoft des messages qui ne devraient pas être classés comme courrier indésirable. Ce faisant, veillez à respecter les étapes de la procédure suivante.
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a>Pour utiliser du courrier électronique pour soumettre des messages faux positifs à l’équipe d’analyse du courrier indésirable de Microsoft

1. Enregistrez le message que vous voulez envoyer comme courrier non indésirable.
    
2. Créez un message vide et joignez à ce message le courrier non indésirable.
    
    Vous pouvez joindre plusieurs messages non indésirables, le cas échéant.
    
3. Copiez et collez la ligne d'objet du message d'origine dans la ligne d'objet du nouveau message.
    
    > [!IMPORTANT]
    > Laissez le corps du message vide. 
  
4. Adressez votre nouveau message à [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a>Le trafic provenant de mon adresse IP est limité par EOP
<a name="AllowEOPIPs"> </a>

Si vous recevez une notification d'échec de remise d'EOP, cela indique que votre adresse IP est limitée par EOP, par exemple :
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
Vous avez reçu une notification d'échec de remise car une activité suspecte a été détectée sur l'adresse IP et a été restreinte temporairement le temps d'effectuer des évaluations supplémentaires. Si la suspicion est désactivée au cours de l'évaluation, cette restriction est bientôt levée.
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a>Je ne reçois pas les e-mails provenant d'expéditeurs dans Office 365
<a name="AllowEOPIPs"> </a>

 Pour recevoir des messages de nos utilisateurs, assurez-vous que votre réseau autorise les connexions à partir des adresses IP utilisées par EOP dans nos centres de donnees. Pour plus d'informations, consultez la rubrique [Exchange Online Protection IP](eop/exchange-online-protection-ip-addresses.md)Addresses. 
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a>Meilleures pratiques pour l'envoi en bloc d'e-mails aux utilisateurs d'Office 365
<a name="BulkMailer"> </a>

Si vous menez souvent des campagnes d'envoi en bloc d'e-mails aux utilisateurs d'Office 365 et souhaitez vous assurer que vos e-mails arrivent de manière sûre et opportune, suivez les conseils fournis dans cette section.
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a>Vérifier que le champ De : indique le nom de la personne qui envoie le message

L'Objet doit être un bref résumé du contenu du message, et le corps du message doit clairement et brièvement indiquer l'objet de l'offre, du service ou du produit. Par exemple :
  
Correct
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
Incorrect
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
Plus vous vous présentez et décrivez ce que vous faites de façon claire, moins vos courriers seront bloqués par la plupart des filtres anti-spam.
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a>Toujours inclure une option de désinscription dans les e-mails de campagne

Les e-mails de marketing, notamment les bulletins d'informations, doivent toujours inclure une option permettant de se désinscrire pour ne plus recevoir de futurs e-mails. Par exemple :
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
Certains expéditeurs incluent cette option en demandant aux destinataires d'envoyer un e-mail à un certain alias avec « Se désabonner » dans l'objet. Cela n'est pas préférable à l'exemple en un seul clic ci-dessus. Si vous choisissez de demander aux destinataires d'envoyer un message, assurez-vous que lorsqu'ils cliquent sur le lien, tous les champs requis sont renseignés au préalable.
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a>Utiliser l'option de contrôle de consentement double pour l'enregistrement à des e-mails de marketing ou à des bulletins d'informations

Cette pratique est recommandée par le secteur si votre entreprise requiert que les utilisateurs enregistrent leurs informations de contact ou les y encourage pour accéder à vos produits ou services. Certaines sociétés ont pris l'habitude d'inscrire automatiquement leurs utilisateurs pour les e-mails de marketing ou les bulletins d'informations électroniques lors du processus d'enregistrement. Néanmoins, cela est considéré comme une pratique marketing discutables dans le monde du filtrage des messages électroniques.
  
Au cours du processus d'enregistrement, si la case à cocher « Oui, merci de m'envoyer votre bulletin d'informations » ou « Oui, merci de m'envoyer les offres spéciales » est sélectionnée par défaut, les utilisateurs qui ne font pas assez attention risquent de s'inscrire par inadvertance aux e-mails de marketing ou aux bulletins d'informations qu'ils ne souhaitent pas recevoir.
  
 Nous vous recommandons l'option de contrôle de consentement double à la place, ce qui signifie que la case à cocher pour les e-mails de marketing ou les bulletins d'informations est désactivée par défaut. En outre, une fois que le formulaire d'inscription a été envoyé, un e-mail de vérification est envoyé à l'utilisateur avec une URL qui leur permet de confirmer leur décision de recevoir des e-mails de marketing. 
  
 Cela permet de garantir que seuls les utilisateurs qui souhaitent recevoir des e-mails de marketing sont inscrits pour les e-mails, en désactivant ensuite l'entreprise émettrice de toute pratique discutable. 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a>Vérifier que le contenu des messages électroniques est transparent et qu'il est possible de le suivre

La façon dont les e-mails sont envoyés est aussi importante que leur contenu. Lorsque vous créez le contenu d'un e-mail, utilisez les meilleures pratiques suivantes pour vous assurer que vos e-mails ne seront pas signalés par des services de filtrage des messages électroniques :
  
- Lorsque le message de l'e-mail demande aux destinataires d'ajouter l'expéditeur au carnet d'adresses, il doit clairement indiquer qu'une telle action ne constitue pas une garantie de remise.
    
- Les redirections incluses dans le corps du message doivent être similaires et cohérentes et non multiples et variées. Une redirection dans ce contexte est tout élément qui pointe en dehors du message, comme des liens et des documents. Si vous avez de très nombreux liens Se désabonner ou Mettre à jour le profil, ils doivent tous pointer vers le même domaine. Par exemple :
    
    Correct
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    Incorrect
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- Évitez les images et les pièces jointes volumineuses, ou les messages contenant uniquement une image.
    
- Vos paramètres publics de confidentialité ou P3P doivent signaler clairement la présence des pixels de suivi (bogues ou balises web).
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a>Supprimer les alias de messagerie incorrects de vos bases de données

Les alias de messagerie de votre base de données qui créent un renvoi sont inutiles et exposent vos messages électroniques sortants à des risques d'examen approfondi par les services de filtrage de courrier électronique. Assurez-vous que votre base de données de messagerie est à jour.
  

