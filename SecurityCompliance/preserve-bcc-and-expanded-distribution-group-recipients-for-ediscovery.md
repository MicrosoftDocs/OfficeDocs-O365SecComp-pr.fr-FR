---
title: Conserver les destinataires Cci et les destinataires de groupe de distribution étendu pour la découverte électronique
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/19/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: eb8ddf15-0080-457e-9d83-e73e193da334
description: La conservation inaltérable, la conservation pour litige et les stratégies de rétention d'Office 365 vous permettent de conserver le contenu de la boîte aux lettres pour répondre aux exigences de conformité réglementaire et de découverte électronique.
ms.openlocfilehash: fcf5567bc50f25ce51d8d569d772559a376703d0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261682"
---
# <a name="preserve-bcc-and-expanded-distribution-group-recipients-for-ediscovery"></a>Conserver les destinataires Cci et les destinataires de groupe de distribution étendu pour la découverte électronique
  
La conservation inaltérable, la conservation pour litige et les stratégies de rétention d' [Office 365](http://go.microsoft.com/fwlink/?LinkID=827811) (créées dans le centre de sécurité _AMP_ Compliance Center) vous permettent de conserver le contenu de la boîte aux lettres conformément aux exigences de conformité réglementaire et de découverte électronique. Les informations sur les destinataires directement indiqués dans les champs À et Cc d'un message sont incluses dans tous les messages par défaut, mais votre organisation peut exiger la capacité de rechercher et de reproduire des détails sur tous les destinataires d'un message. Cela inclut les opérations suivantes : 
  
- **Les destinataires spécifiés dans le champ Cci d'un message :** les destinataires en copie carbone invisible sont stockés dans le message qui se trouve dans la boîte aux lettres de l'expéditeur, mais ne figurent pas dans les en-têtes du message remis aux destinataires. 
    
- **Les destinataires de groupe de distribution étendu :** les destinataires qui reçoivent le message car ils sont membres d'un groupe de distribution auquel le message a été adressé, figurent dans le champ À, Cc ou Cci. 
    
Exchange Online et Exchange Server 2013 (mise à jour cumulative 7 et versions ultérieures) conservent des informations sur le champ CCI et les destinataires de groupe de distribution étendus. Vous pouvez rechercher ces informations à l'aide d'une recherche de découverte électronique inaltérable dans le centre d'administration Exchange ou une recherche de contenu dans le centre de sécurité & Compliance Center. 
  
## <a name="how-bcc-recipients-and-expanded-distribution-group-recipients-are-preserved"></a>Conservation des destinataires en copie carbone invisible et des destinataires de groupe de distribution étendu
<a name="sectionSection0"> </a>

Comme indiqué précédemment, les informations sur les destinataires en copie carbone invisible sont stockées avec le message dans la boîte aux lettres de l'expéditeur. Ces informations sont indexées et disponibles pour les recherches de découverte électronique et les conservations. 
  
Les informations sur les destinataires de groupe de distribution étendu sont stockées avec le message après vous avez placé une boîte aux lettres en conservation inaltérable ou en conservation pour litige. Dans Office 365, ces informations sont également stockées lorsqu'une stratégie de rétention Office 365 est appliquée à une boîte aux lettres. L'appartenance au groupe de distribution est déterminée au moment où le message est envoyé. La liste des destinataires étendue stockée avec le message n'est pas concernée par les modifications d'appartenance au groupe une fois que le message est envoyé. 
  
|**Informations sur...**|**Stockage dans...**|**Stockage par défaut ?**|**Accessibles à...**|
|:-----|:-----|:-----|:-----|
|Destinataires À et Cc  <br/> |Propriétés de message dans les boîtes aux lettres de l'expéditeur et des destinataires  <br/> |Oui  <br/> |Expéditeur, destinataires et responsables de la mise en conformité  <br/> |
|Destinataires en copie carbone invisible  <br/> |Propriété de message dans la boîte aux lettres de l'expéditeur  <br/> |Oui  <br/> |Expéditeurs et responsables de la mise en conformité  <br/> |
|Destinataires de groupe de distribution étendu  <br/> |Propriétés de message dans la boîte aux lettres de l'expéditeur  <br/> |Non. Les informations sur les destinataires du groupe de distribution étendu sont stockées une fois qu'une boîte aux lettres est placée en conservation inaltérable ou en conservation pour litige, ou affectée à une stratégie de rétention Office 365.  <br/> |Responsables de la mise en conformité  <br/> |
   
## <a name="searching-for-messages-sent-to-bcc-and-expanded-distribution-group-recipients"></a>Recherche de messages envoyés aux destinataires en copie carbone invisible et aux destinataires de groupe de distribution étendu
<a name="sectionSection1"> </a>

Lors de la recherche de messages envoyés à un destinataire, les résultats de découverte électronique incluent désormais les messages envoyés à un groupe de distribution dont le destinataire est membre. Le tableau suivant présente les scénarios où les messages envoyés à des destinataires en copie carbone invisible et à des destinataires de groupe de distribution étendu sont renvoyés dans les recherches de découverte électronique.
  
Scénario 1 : John est membre du groupe de distribution Ventes aux États-Unis. Ce tableau présente les résultats de la recherche de découverte électronique lorsque Bob envoie un message à John directement ou indirectement via un groupe de distribution.
  
|**Lorsque vous recherchez les messages envoyés dans la boîte aux lettres de Bob...**|**Et le message est envoyé avec...**|**Les résultats incluent le message...**|
|:-----|:-----|:-----|
|À:John  <br/> |John dans le champ À  <br/> |Oui  <br/> |
|À:John  <br/> |Ventes aux États-Unis dans le champ À  <br/> |Oui  <br/> |
|À:Ventes aux États-Unis  <br/> |Ventes aux États-Unis dans le champ À  <br/> |Oui  <br/> |
|Cc:John  <br/> |John dans le champ Cc  <br/> |Oui  <br/> |
|Cc:John  <br/> |Ventes aux États-Unis dans le champ Cc  <br/> |Oui  <br/> |
|Cc:Ventes aux États-Unis  <br/> |Ventes aux États-Unis dans le champ Cc  <br/> |Oui  <br/> |
   
Scénario 2 : Bob envoie un courrier électronique à John (À/Cc) et Jack (Cci, directement ou indirectement via un groupe de distribution). Le tableau ci-dessous montre les résultats de la recherche de découverte électronique.
  
|**Lorsque vous recherchez...**|**Pour les messages envoyés...**|**Les résultats incluent le message...**|**Notes**|
|:-----|:-----|:-----|:-----|
|Boîte aux lettres de Bob  <br/> |À/Cc:John  <br/> |Oui  <br/> |Indique que Jack était inclus dans le champ Cci  <br/> |
|Boîte aux lettres de Bob  <br/> |Cci:Jack  <br/> |Oui  <br/> |Indique que Jack était inclus dans le champ Cci  <br/> |
|Boîte aux lettres de Bob  <br/> |Cci:Jack (via un groupe de distribution)  <br/> |Oui  <br/> |La liste des membres du groupe de distribution indiqué dans le champ Cci, étendu lors de l'envoi du message, est visible dans l'aperçu de la recherche de découverte électronique, l'exportation et les journaux.  <br/> |
|Boîte aux lettres de John  <br/> |À/Cc:John  <br/> |Oui  <br/> |Aucune indication des destinataires en copie carbone invisible.  <br/> |
|Boîte aux lettres de John  <br/> |Cci:Jack (directement ou via un groupe de distribution)  <br/> |Non  <br/> |Les informations du champ Cci ne sont pas stockées dans le message remis aux destinataires. Vous devez les rechercher dans la boîte aux lettres de l'expéditeur.  <br/> |
|Boîte aux lettres de Jack  <br/> |À/Cc:John (directement ou via un groupe de distribution)  <br/> |Oui  <br/> |Les informations des champs À/Cc sont incluses dans le message remis à tous les destinataires.  <br/> |
|Boîte aux lettres de Jack  <br/> |Cci:Jack (directement ou via un groupe de distribution)  <br/> |Non  <br/> |Les informations du champ Cci ne sont pas stockées dans le message remis aux destinataires. Vous devez les rechercher dans la boîte aux lettres de l'expéditeur.  <br/> |
   
## <a name="frequently-asked-questions"></a>Questions fréquemment posées
<a name="sectionSection2"> </a>

 **Q. Quand les informations sur le destinataire en Cci sont-elles stockées et à quel emplacement ?**
  
A. Les informations relatives au destinataire en Cci sont conservées par défaut dans le message d'origine, dans la boîte aux lettres de l'expéditeur. Si le destinataire CCI est un groupe de distribution, l'appartenance au groupe de distribution n'est étendue que si la boîte aux lettres de l'expéditeur est bloquée ou affectée à une stratégie de rétention Office 365.
  
 **Q. Quand la liste des destinataires de groupe de distribution étendu est-elle stockée et à quel emplacement ?**
  
R. L'appartenance au groupe est étendue au moment de l'envoi du message. La liste des membres de groupe de distribution étendu est stockée dans le message d'origine, dans la boîte aux lettres de l'expéditeur. La boîte aux lettres de l'expéditeur doit être en conservation inaltérable, mise en attente pour litige ou affectée à une stratégie de rétention Office 365.
  
 **Q. Les destinataires indiqués dans les champs À et Cc peuvent-ils voir les destinataires indiqués dans le champ Cci ?**
  
R. Non. Ces informations ne sont pas incluses dans les en-têtes de message et ne sont pas visibles pour les destinataires indiqués dans les champs À et Cc. L'expéditeur peut voir le champ Cci stocké dans le message original de sa boîte aux lettres. Les responsables de la mise en conformité peuvent voir ces informations lors d'une recherche dans la boîte aux lettres de l'expéditeur.
  
 **Q. Comment puis-je m'assurer que les destinataires de groupe de distribution étendu sont toujours conservés ?**
  
R. Pour garantir que les membres de groupe de distribution étendus sont toujours conservés avec un message, [Placez toutes les boîtes aux lettres en conservation](http://technet.microsoft.com/library/4c141604-3210-44cc-b98e-f3e0f15613b8.aspx) ou créez une stratégie de rétention Office 365 à l'échelle de l'organisation. 
  
 **Q. Quels types de groupe sont pris en charge ?**
  
R. Les groupes de distribution, les groupes de sécurité à extension messagerie et les groupes de distribution dynamique sont pris en charge. 
  
 **Q. Y a-t-il une limite en ce qui concerne le nombre de destinataires de groupes de distribution étendus et stockés dans le message ?**
  
R. Jusqu'à 10 000 membres d'un groupe de distribution sont conservés.
  
 **Q. Les groupes de distribution imbriqués sont-ils pris en charge ?**
  
R. Oui, 25 niveaux de groupes de distribution imbriqués sont étendus.
  
 **Q. Où les informations du champ Cci et les informations relatives aux destinataires de groupe de distribution étendu sont-elles visibles ?**
  
R. Ces informations sont visibles pour les responsables de la mise en conformité lors d'une recherche de découverte électronique. Les destinataires en Cci et les destinataires de groupe de distribution étendu sont inclus dans les résultats de recherche copiés vers une boîte aux lettres de découverte ou exportés vers un fichier PST et dans le journal de découverte électronique inclus dans les résultats de la recherche. Les informations relatives aux destinataires en copie carbone invisible sont également disponibles dans l'aperçu de la recherche.
  
 **Q. Que se passe-t-il si un membre d'un groupe de distribution est masqué dans la liste d'adresses globale (LAG) de l'organisation ?**
  
R. Il n'y a aucune conséquence. Même si des destinataires sont masqués dans la LAG, ils restent inclus dans la liste des destinataires pour le groupe de distribution étendu.
  

