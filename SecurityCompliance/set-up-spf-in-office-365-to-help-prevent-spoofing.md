---
title: Configurer SPF dans Office 365 pour empêcher l’usurpation
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 2/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 71373291-83d2-466f-86ea-fc61493743a6
description: "Résumé : Cet article explique comment mettre à jour un enregistrement DNS (Domain Name Service) afin que vous puissiez utiliser le SPF (Sender Policy Framework) avec votre domaine personnalisé dans Office 365. L'utilisation de SPF permet de valider les messages sortants envoyés à partir de votre domaine personnalisé."
ms.openlocfilehash: 1670e646d4eb847c72159e0b8b730ae08ea285a8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026361"
---
# <a name="set-up-spf-in-office-365-to-help-prevent-spoofing"></a>Configurer SPF dans Office 365 pour empêcher l’usurpation

 **Résumé :** Cet article explique comment mettre à jour un enregistrement DNS (Domain Name Service) afin que vous puissiez utiliser le SPF (Sender Policy Framework) avec votre domaine personnalisé dans Office 365. L'utilisation de SPF permet de valider les messages sortants envoyés à partir de votre domaine personnalisé. 
  
Afin d’utiliser un domaine personnalisé, Office 365 exige que vous ajoutiez un enregistrement TXT SPF (Sender Policy Framework) à votre enregistrement DNS pour éviter l’usurpation. SPF identifie les serveurs de messagerie qui sont autorisés à envoyer des messages en votre nom. En bref, SPF, ainsi que DKIM, DMARC et d’autres technologies prises en charge par Office 365, permettent d’éviter l’usurpation et le hameçonnage. SPF est ajouté sous la forme d’un enregistrement TXT qui est utilisé par le système DNS afin d’identifier les serveurs de messagerie autorisés à envoyer des messages au nom de votre domaine personnalisé. Les systèmes de messagerie électronique des destinataires peuvent se reporter à l’enregistrement TXT SPF pour déterminer si un message provenant de votre domaine personnalisé a été envoyé à partir d’un serveur de messagerie autorisé.
  
Par exemple, supposons que votre domaine personnalisé contoso.com utilise Office 365. Vous ajoutez un enregistrement TXT SPF qui répertorie les serveurs de messagerie Office 365 en tant que serveurs de messagerie légitimes pour votre domaine. Lorsque le serveur de messagerie de réception reçoit un message de la part de joe@contoso.com, le serveur recherche l’enregistrement TXT SPF pour contoso.com et détermine si le message est valide. Si le serveur de réception détecte que le message provient d’un serveur autre que les serveurs de messagerie Office 365 répertoriés dans l’enregistrement SPF, le serveur de messagerie de réception peut choisir de refuser le message en le marquant comme du courrier indésirable.
  
En outre, si votre domaine personnalisé ne dispose pas d’un enregistrement TXT SPF, certains serveurs de réception peuvent totalement rejeter le message. En effet, le serveur de réception ne peut pas valider le fait que le message provient d’un serveur de messagerie autorisé.
  
Si vous avez déjà configuré les messages pour Office 365, vous avez déjà inclus les serveurs de messagerie de Microsoft dans le système DNS sous la forme d’un enregistrement TXT SPF. Toutefois, il existe certains cas où vous devez mettre à jour votre enregistrement TXT SPF dans le système DNS. Par exemple :
  
- Auparavant, vous deviez ajouter un autre enregistrement TXT SPF à votre domaine personnalisé, si vous utilisiez SharePoint Online. Cela n'est plus nécessaire. Ce changement doit réduire le risque que les messages de notification SharePoint Online terminent dans le dossier Courrier indésirable. Mettez votre enregistrement TXT SPF à jour si vous avez atteint la limite de 10 recherches et recevez des erreurs de type « Vous avez dépassé la limite de recherche » et « Trop de sauts ».
    
- Vous avez un environnement hybride avec Office 365 et Exchange en local.
    
- Vous avez l'intention de configurer DKIM et DMARC (recommandé).
    
## <a name="updating-your-spf-txt-record-for-office-365"></a>Mise à jour de votre enregistrement TXT SPF pour Office 365
<a name="sectionSection0"> </a>

Avant de mettre à jour l'enregistrement TXT dans le système DNS, vous devez rassembler quelques informations et déterminer le format de l'enregistrement. Cela vous permettra d'éviter de générer des erreurs DNS. Pour obtenir des exemples avancés et des informations plus détaillées sur la syntaxe SPF prise en charge, voir la section [Fonctionnement de SPF pour éviter l'usurpation et le hameçonnage dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
Collectez les informations ci-dessous :
  
- L'enregistrement TXT SPF actuel pour votre domaine personnalisé. Pour obtenir des instructions, consultez [Recueillez les informations nécessaires pour créer des enregistrements DNS Office 365](https://support.office.microsoft.com/en-us/article/Gather-the-information-you-need-to-create-Office-365-DNS-records-77f90d4a-dc7f-4f09-8972-c1b03ea85a67).
    
- Les adresses IP de tous les serveurs de messagerie locaux. Par exemple, **192.168.0.1**.
    
- Les noms de domaine à utiliser pour tous les domaines de tiers que vous devez inclure dans votre enregistrement TXT SPF. Certains fournisseurs de messagerie en bloc disposent de sous-domaines configurés que leurs clients peuvent utiliser. Par exemple, la société MailChimp a configuré **servers.mcsv.net**.
    
- La règle de mise en œuvre que vous souhaitez utiliser pour votre enregistrement TXT SPF. Nous vous recommandons **-all**. Pour plus d'informations sur les autres options de syntaxe, voir [Syntaxe d'enregistrement TXT SPF pour Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFSyntaxO365).
    
### <a name="to-add-or-update-your-spf-txt-record"></a>Pour ajouter ou mettre à jour votre enregistrement TXT SPF

1. Si vous ne l'avez pas déjà fait, créez votre enregistrement TXT SPF à l'aide de la syntaxe du tableau suivant :
    
||**Si vous utilisez...**|**Courant pour les utilisateurs d'Office 365 ?**|**Ajoutez l'élément suivant...**|
|:-----|:-----|:-----|:-----|
|1  <br/> |Un système de messagerie (obligatoire)  <br/> |Courant. Tous les enregistrements TXT SPF commencent avec cette valeur  <br/> |v=spf1  <br/> |
|2  <br/> |Exchange Online  <br/> |Courant  <br/> |Include:SPF.protection.Outlook.com  <br/> |
|3  <br/> |Exchange Online dédié uniquement  <br/> |Non courant  <br/> |IP4:23.103.224.0/19 ip4:206.191.224.0/19 ip4:40.103.0.0/16 include:spf.protection.outlook.com  <br/> |
|4  <br/> |Office 365 Germany, Microsoft Cloud Germany uniquement  <br/> |Non courant  <br/> |Include:SPF.protection.Outlook.de  <br/> |
|5  <br/> |Système de messagerie tiers  <br/> |Non courant  <br/> |include:\<nom du domaine\>  <br/> Où <nom du domaine> est le nom de domaine du système de messagerie tiers.  <br/> |
|6  <br/> |Système de messagerie en local. Par exemple, Exchange Online Protection et un autre système de messagerie  <br/> |Non courant  <br/> | Utilisez l'un des éléments suivants pour chaque système de messagerie supplémentaire :  <br/>  ip4:\<  _IP address_\>  <br/>  ip6:\<  _IP address_\>  <br/>  include:\<  _domain name_\>  <br/>  Où la valeur de l'élément \<  _IP address_\> est l'adresse IP de l'autre système de messagerie et \< _domain name_\> correspond au nom de domaine de l'autre système de messagerie qui envoie un message au nom de votre domaine.  <br/> |
|7  <br/> |Un système de messagerie (obligatoire)  <br/> |Courant. Tous les enregistrements TXT SPF se terminent par cette valeur  <br/> |\< _enforcement rule_\>  <br/> Il peut s'agir de plusieurs valeurs. Il est recommandé d'utiliser **-all**.  <br/> |
   
1.1 par exemple, si vous êtes entièrement hébergé dans Office 365, autrement dit, vous n’avez aucun serveur de messagerie local, votre TXT SPF enregistrement comprend des lignes 1, 2 et 7 et se présente comme suit :
    
  ```
   v=spf1 include:spf.protection.outlook.com -all
  ```

1.2 il s’agit de l’enregistrement TXT de SPF Office 365 les plus courants. Cet enregistrement est valable pour presque tout le monde, quelle que soit la si votre centre de données Office 365 se trouve aux États-Unis, ou en Europe (y compris Allemagne) ou à un autre emplacement.
    
1.3 Toutefois, si vous avez acheté Office 365 Allemagne, composant de Cloud Microsoft Allemagne, vous devez utiliser l’instruction include à partir de la ligne 4 au lieu de la ligne 2. Par exemple, si vous êtes entièrement hébergé dans Office 365 Allemagne, autrement dit, vous n’avez aucun serveur de messagerie local, votre TXT SPF enregistrement comprend des lignes 1, 4 et 7 et se présente comme suit :
    
  ```
   v=spf1 include:spf.protection.outlook.de -all
  ```

1.4 Si vous ont déjà été déployées dans Office 365 et que vous avez configuré vos enregistrements SPF TXT pour votre domaine personnalisé et que vous migrez vers Office 365 Allemagne, vous devez mettre à jour votre enregistrement SPF TXT. Pour ce faire, remplacez **include:spf.protection.outlook.com** **include.spf.protection.outlook.de**.
    
2. Une fois que vous avez formulé votre enregistrement TXT SPF, vous devez mettre à jour l'enregistrement dans le système DNS. Vous ne pouvez avoir qu'un seul enregistrement TXT SPF pour un domaine. Si un enregistrement TXT SPF existe, au lieu d'ajouter un nouvel enregistrement, vous devez mettre à jour l'enregistrement existant. Accédez à [Créer des enregistrements DNS pour Office 365](https://support.office.microsoft.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23), puis cliquez sur le lien correspondant à votre hôte DNS. (Si votre hôte DNS ne possède pas de lien sur la page, vous pouvez [suivre les instructions générales](https://support.office.microsoft.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) pour ajouter des enregistrements ou contacter votre hôte DNS pour obtenir de l'aide.) 
    
3. Tester votre enregistrement SPF TXT.
    
## <a name="more-information-about-spf"></a>En savoir plus sur SPF
<a name="sectionSection1"> </a>

Pour obtenir des exemples avancés, des informations plus détaillées sur la syntaxe SPF prise en charge, l'usurpation, la résolution des problèmes et la façon dont Office 365 prend en charge SPF, voir la section [Fonctionnement de SPF pour éviter l'usurpation et le hameçonnage dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
## <a name="next-steps-after-you-set-up-spf-for-office-365"></a>Étapes suivantes : après avoir configuré SPF pour Office 365
<a name="sectionSection2"> </a>

Vous rencontrez des problèmes avec votre enregistrement TXT SPF ? Lisez [Résolution des problèmes : Meilleures pratiques pour SPF dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).
  
 SPF est conçu pour éviter l'usurpation mais il existe des techniques d'usurpation contre lesquelles SPF ne peut pas vous protéger. Afin de vous protéger contre ces techniques, une fois que vous avez configuré SPF, vous devez également configurer DKIM et DMARC pour Office 365. Consultez [Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md) pour commencer. Ensuite, consultez la rubrique [Utiliser DMARC pour valider les e-mails dans Office 365](use-dmarc-to-validate-email.md).
  

