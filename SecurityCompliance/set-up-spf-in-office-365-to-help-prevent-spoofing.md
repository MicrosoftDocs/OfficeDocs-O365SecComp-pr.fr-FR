---
title: Configurer SPF dans Office 365 pour empêcher l’usurpation
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 2/19/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 71373291-83d2-466f-86ea-fc61493743a6
ms.collection:
- M365-security-compliance
description: "Résumé : Cet article explique comment mettre à jour un enregistrement DNS (Domain Name Service) afin que vous puissiez utiliser le SPF (Sender Policy Framework) avec votre domaine personnalisé dans Office 365. L'utilisation de SPF permet de valider les messages sortants envoyés à partir de votre domaine personnalisé."
ms.openlocfilehash: 5194a9a8a8b694bc2dbac0eaf9b50517e46a9064
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158196"
---
# <a name="set-up-spf-in-office-365-to-help-prevent-spoofing"></a>Configurer SPF dans Office 365 pour empêcher l’usurpation

 **Résumé :** Cet article explique comment mettre à jour un enregistrement DNS (Domain Name Service) afin que vous puissiez utiliser le SPF (Sender Policy Framework) avec votre domaine personnalisé dans Office 365. L'utilisation de SPF permet de valider les messages sortants envoyés à partir de votre domaine personnalisé. 
  
Afin d'utiliser un domaine personnalisé, Office 365 exige que vous ajoutiez un enregistrement TXT SPF (Sender Policy Framework) à votre enregistrement DNS pour éviter l'usurpation. SPF identifie les serveurs de messagerie qui sont autorisés à envoyer des messages en votre nom. En bref, SPF, ainsi que DKIM, DMARC et d'autres technologies prises en charge par Office 365, permettent d'éviter l'usurpation et le hameçonnage. SPF est ajouté sous la forme d'un enregistrement TXT qui est utilisé par le système DNS afin d'identifier les serveurs de messagerie autorisés à envoyer des messages au nom de votre domaine personnalisé. Les systèmes de messagerie électronique des destinataires peuvent se reporter à l'enregistrement TXT SPF pour déterminer si un message provenant de votre domaine personnalisé a été envoyé à partir d'un serveur de messagerie autorisé.
  
Par exemple, supposons que votre domaine personnalisé contoso.com utilise Office 365. Vous ajoutez un enregistrement TXT SPF qui répertorie les serveurs de messagerie Office 365 en tant que serveurs de messagerie légitimes pour votre domaine. Lorsque le serveur de messagerie de réception reçoit un message de la part de joe@contoso.com, le serveur recherche l'enregistrement TXT SPF pour contoso.com et détermine si le message est valide. Si le serveur de réception détecte que le message provient d'un serveur autre que les serveurs de messagerie Office 365 répertoriés dans l'enregistrement SPF, le serveur de messagerie de réception peut choisir de refuser le message en le marquant comme du courrier indésirable.
  
En outre, si votre domaine personnalisé ne dispose pas d'un enregistrement TXT SPF, certains serveurs de réception peuvent totalement rejeter le message. En effet, le serveur de réception ne peut pas valider le fait que le message provient d'un serveur de messagerie autorisé.
  
Si vous avez déjà configuré les messages pour Office 365, vous avez déjà inclus les serveurs de messagerie de Microsoft dans le système DNS sous la forme d'un enregistrement TXT SPF. Toutefois, il existe certains cas où vous devez mettre à jour votre enregistrement TXT SPF dans le système DNS. Par exemple :
  
- Auparavant, vous deviez ajouter un autre enregistrement TXT SPF à votre domaine personnalisé, si vous utilisiez SharePoint Online. Cela n'est plus nécessaire. Ce changement doit réduire le risque que les messages de notification SharePoint Online terminent dans le dossier Courrier indésirable. Mettez votre enregistrement TXT SPF à jour si vous avez atteint la limite de 10 recherches et recevez des erreurs de type « Vous avez dépassé la limite de recherche » et « Trop de sauts ».
    
- Vous avez un environnement hybride avec Office 365 et Exchange en local.
    
- Vous avez l’intention de configurer DKIM et DMARC (recommandé).
    
## <a name="updating-your-spf-txt-record-for-office-365"></a>Mise à jour de votre enregistrement TXT SPF pour Office 365

Avant de mettre à jour l’enregistrement TXT dans le système DNS, vous devez rassembler quelques informations et déterminer le format de l’enregistrement. Cela vous permettra d’éviter de générer des erreurs DNS. Pour obtenir des exemples avancés et des informations plus détaillées sur la syntaxe SPF prise en charge, voir la section [Fonctionnement de SPF pour éviter l’usurpation et le hameçonnage dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
Collectez les informations ci-dessous :
  
- L'enregistrement TXT SPF actuel pour votre domaine personnalisé. Pour obtenir des instructions, consultez [Recueillez les informations nécessaires pour créer des enregistrements DNS Office 365](https://support.office.microsoft.com/en-us/article/Gather-the-information-you-need-to-create-Office-365-DNS-records-77f90d4a-dc7f-4f09-8972-c1b03ea85a67).
    
- Les adresses IP de tous les serveurs de messagerie locaux. Par exemple, **192.168.0.1**.
    
- Les noms de domaine à utiliser pour tous les domaines de tiers que vous devez inclure dans votre enregistrement TXT SPF. Certains fournisseurs de messagerie en bloc disposent de sous-domaines configurés que leurs clients peuvent utiliser. Par exemple, la société MailChimp a configuré **servers.mcsv.net**.
    
- La règle de mise en œuvre que vous souhaitez utiliser pour votre enregistrement TXT SPF. Nous vous recommandons **-all**. Pour plus d’informations sur les autres options de syntaxe, voir [Syntaxe d’enregistrement TXT SPF pour Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFSyntaxO365).
    
### <a name="to-add-or-update-your-spf-txt-record"></a>Pour ajouter ou mettre à jour votre enregistrement TXT SPF

1. Si vous ne l'avez pas déjà fait, créez votre enregistrement TXT SPF à l'aide de la syntaxe du tableau suivant :
    
||**Si vous utilisez...**|**Courant pour les utilisateurs d'Office 365 ?**|**Ajoutez l'élément suivant...**|
|:-----|:-----|:-----|:-----|
|0,1  <br/> |Un système de messagerie (obligatoire)  <br/> |Courant. Tous les enregistrements TXT SPF commencent avec cette valeur  <br/> |v=spf1  <br/> |
|n°2  <br/> |Exchange Online  <br/> |Courant  <br/> |include:spf.protection.outlook.com  <br/> |
|3  <br/> |Exchange Online dédié uniquement  <br/> |Non courant  <br/> |IP4:23.103.224.0/19 IP4:206.191.224.0/19 IP4:40.103.0.0/16 incluent include. protection. Outlook. com  <br/> |
|4  <br/> |Office 365 Germany, Microsoft Cloud Germany uniquement  <br/> |Non courant  <br/> |inclure include. protection. Outlook. de  <br/> |
|disque  <br/> |Système de messagerie tiers  <br/> |Non courant  <br/> |include:\<nom du domaine\>  <br/> Where domain name is the domain name of the third party email system.  <br/> |
|6.x  <br/> |Système de messagerie en local. Par exemple, Exchange Online Protection et un autre système de messagerie  <br/> |Non courant  <br/> | Utilisez l'un des éléments suivants pour chaque système de messagerie supplémentaire :  <br/>  ip4:\<  _IP address_\>  <br/>  ip6:\<  _IP address_\>  <br/>  include:\<  _domain name_\>  <br/>  Où la valeur de l'élément \<  _IP address_\> est l'adresse IP de l'autre système de messagerie et \< _domain name_\> correspond au nom de domaine de l'autre système de messagerie qui envoie un message au nom de votre domaine.  <br/> |
|7j/7  <br/> |Un système de messagerie (obligatoire)  <br/> |Courant. Tous les enregistrements TXT SPF se terminent par cette valeur  <br/> |\< _enforcement rule_\>  <br/> Il peut s'agir de plusieurs valeurs. Il est recommandé d'utiliser **-all**.  <br/> |
   
1,1 par exemple, si vous êtes entièrement hébergé dans Office 365, autrement dit, vous n’avez pas de serveur de messagerie local, votre enregistrement TXT SPF inclut les lignes 1, 2 et 7 et se présente comme suit:
    
  ```
   v=spf1 include:spf.protection.outlook.com -all
  ```

1,2 il s’agit de l’enregistrement TXT SPF Office 365 le plus courant. Cet enregistrement fonctionne pour tout le monde, que votre centre de informations Office 365 soit situé aux États-Unis ou en Europe (y compris Germany) ou dans un autre emplacement.
    
1,3 Toutefois, si vous avez acheté Office 365 Germany, partie de Microsoft Cloud Germany, vous devez utiliser l’instruction include de la ligne 4 au lieu de la ligne 2. Par exemple, si vous êtes entièrement hébergé par Office 365 Germany, ce qui signifie que vous n’avez aucun serveur de messagerie local, votre enregistrement TXT SPF inclut les lignes 1, 4 et 7 et se présente comme suit :
    
  ```
   v=spf1 include:spf.protection.outlook.de -all
  ```

1,4 Si vous êtes déjà déployé dans Office 365 et que vous avez configuré vos enregistrements TXT SPF pour votre domaine personnalisé et que vous effectuez une migration vers Office 365 Germany, vous devez mettre à jour votre enregistrement TXT SPF. Pour ce faire, modifiez **include include. protection. Outlook. com** pour **inclure include. protection. Outlook. de**.
    
2. Une fois que vous avez formulé votre enregistrement TXT SPF, vous devez mettre à jour l'enregistrement dans le système DNS. Vous ne pouvez avoir qu'un seul enregistrement TXT SPF pour un domaine. Si un enregistrement TXT SPF existe, au lieu d'ajouter un nouvel enregistrement, vous devez mettre à jour l'enregistrement existant. Accédez à [Créer des enregistrements DNS pour Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider?view=o365-worldwide), puis cliquez sur le lien correspondant à votre hôte DNS. 
    
3. Testez votre enregistrement TXT SPF.
    
## <a name="more-information-about-spf"></a>En savoir plus sur SPF

Pour obtenir des exemples avancés, des informations plus détaillées sur la syntaxe SPF prise en charge, l’usurpation, la résolution des problèmes et la façon dont Office 365 prend en charge SPF, voir la section [Fonctionnement de SPF pour éviter l’usurpation et le hameçonnage dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
## <a name="next-steps-after-you-set-up-spf-for-office-365"></a>Étapes suivantes : après avoir configuré SPF pour Office 365

Vous rencontrez des problèmes avec votre enregistrement TXT SPF ? Lisez [Résolution des problèmes : Meilleures pratiques pour SPF dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).
  
 SPF est conçu pour éviter l'usurpation mais il existe des techniques d'usurpation contre lesquelles SPF ne peut pas vous protéger. Afin de vous protéger contre ces techniques, une fois que vous avez configuré SPF, vous devez également configurer DKIM et DMARC pour Office 365. Consultez [Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md) pour commencer. Ensuite, consultez la rubrique [Utiliser DMARC pour valider les e-mails dans Office 365](use-dmarc-to-validate-email.md).
  

