---
title: Création, test et réglage d’une stratégie DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'La plus simple et la plus courante pour prendre en main les stratégies DLP consiste à utiliser un des modèles inclus dans Office 365. '
ms.openlocfilehash: 1d4697811a5d8dd426fed80d3d60bcd2fbea6335
ms.sourcegitcommit: 42c7ad69f95fc4d2de13293b39cc44931b9f82e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2018
ms.locfileid: "26522786"
---
# <a name="create-test-and-tune-a-dlp-policy"></a>Création, test et réglage d’une stratégie DLP

**Auteur principal** </br>
Paul Cunningham, MVP Microsoft </br>
[365 pratique](https://practical365.com/) </br>
[@Practical365](https://twitter.com/practical365)</br>
__________________________________________________

Protection contre la perte de données est une fonctionnalité de conformité d’Office 365 qui est conçu pour aider votre organisation à empêcher l’exposition intentionnelle ou accidentelle des informations sensibles à des parties indésirables. DLP a ses racines dans Exchange Server et Exchange Online et est également applicable dans SharePoint Online et OneDrive for Business.

DLP utilise un moteur d’analyse de contenu pour examiner le contenu des messages électroniques et des fichiers, recherchez des informations sensibles telles que des numéros de carte de crédit et des informations d’identification personnelle (PII). Les informations sensibles doivent généralement pas être envoyées dans le message électronique ou incluses dans les documents, sans effectuer des étapes supplémentaires, telles que chiffrer le message électronique ou les fichiers. À l’aide de DLP vous pouvez détecter des informations sensibles et effectuer une action telle que :

- Ouvrez une session de l’événement à des fins d’audit
- Afficher un avertissement à l’utilisateur final qui envoie le courrier électronique ou de partage du fichier
- Bloquer activement le courrier électronique ou un partage de lieu de fichiers

Parfois les clients faire disparaître DLP, car elles ne considèrent ont le type de données qui a besoin de protection. Il est supposé que les données sensibles, telles que des dossiers médicaux ou des informations financières, existent uniquement pour les secteurs de la santé ou pour les entreprises qui exécutent des magasins en ligne. Mais toute entreprise peut gérer des informations sensibles sur une base régulière, même s’ils ne conscience. Une feuille de calcul de noms d’employés et les dates de naissance sont comme sensibles en tant qu’une feuille de calcul des noms de client et de carte de crédit. Et ce type d’information tend à flotter plus que vous pouvez le supposer, comme les employés passent en mode silencieux sur leurs tâches quotidiennes, pensant rien d’exporter un fichier CSV à partir d’un système et de courrier électronique à une personne. Vous pouvez également être surpris la fréquence à laquelle envoyer des messages électroniques contenant des détails de la banque ou une carte de crédit sans prendre en compte les conséquences employés.

## <a name="how-sensitive-information-is-detected-by-dlp"></a>Comment les informations sensibles sont détectées par DLP

Les informations sensibles sont identifiées par l’expression régulière (RegEx) critères spéciaux, conjointement avec d’autres indicateurs tels que la proximité de certains mots clés pour les modèles de correspondance. Numéros de carte de crédit est un exemple. Un numéro de carte de crédit VISA a 16 chiffres. Toutefois, ces chiffres peuvent être écrites de différentes manières, par exemple 1111-1111-1111-1111 1111 1111 1111 1111, ou 1111111111111111.

N’importe quelle chaîne à 16 chiffres n’est pas nécessairement un numéro de carte de crédit, il peut être un numéro de ticket à partir d’un système d’assistance technique ou un numéro de série d’un composant matériel. Pour faire la différence entre un numéro de carte de crédit et une chaîne de 16 chiffres sans conséquence, un calcul est effectué (somme de contrôle) pour vérifier que les numéros de correspond à un modèle de carte de crédit différentes marques connu.

En outre, la proximité de mots clés tels que « VISA » ou « Dow », ainsi que de la proximité des valeurs de date qui peut être la date d’expiration de carte de crédit, est considéré comme également à décider si les données sont un numéro de carte de crédit ou non.

En d’autres termes, DLP est généralement suffisamment intelligent pour la différence entre ces deux textes dans un message électronique :

- « Pourrez vous commander me un nouvel ordinateur portable. Utiliser mon numéro VISA 1111-1111-1111-1111, expiration 22/11 et m’envoyer la date de livraison estimée que vous avez ».
- « Mon numéro de série d’un ordinateur portable est 2222 : 2222 : 2222 : 2222 et il a été acheté sur 11/2010. Par ailleurs, est mon visa déplacements encore approuvé ? »

Référence pour conserver le signet est cette [rubrique sur les types d’informations sensibles](what-the-sensitive-information-types-look-for.md) qui explique comment chaque type d’informations est détecté.

## <a name="where-to-start-with-data-loss-prevention"></a>Où commencer avec la prévention de perte de données

Lorsque les risques de perte de données ne sont pas entièrement évidents, il est difficile de déterminer où exactement vous devez commencer par la mise en œuvre de DLP. Heureusement, les stratégies DLP peuvent être exécutées en « mode test », ce qui vous permet d’évaluer leur efficacité et la précision avant d’activer les.

Les stratégies DLP pour Exchange Online peuvent être gérés par le biais du centre d’administration Exchange. Mais vous pouvez configurer des stratégies DLP pour toutes les charges de travail par le biais de la sécurité et le centre de conformité, c’est ce que j’utilise pour des démonstrations dans cet article. Dans la sécurité et le centre de conformité, vous trouverez les stratégies DLP sous **prévention des pertes de données** > **stratégie**. Cliquez sur **créer une stratégie** de démarrage.

Office 365 propose une plage de [modèles de stratégie DLP](what-the-dlp-policy-templates-include.md) , vous pouvez utiliser pour créer des stratégies DLP. Supposons que vous êtes une entreprise australien. Vous pouvez filtrer les modèles de stratégie pour afficher uniquement ceux qui sont pertinents pour l’Australie, qui peuvent être classées dans les catégories générales de financier, médical et d’intégrité et de confidentialité.

![Possibilité de choisir le pays ou région](media/DLP-create-test-tune-choose-country.png)

Pour cette démonstration, je vais choisir données australien personnellement identifiables informations personnelles, qui inclut les types d’informations de numéro de permis de conduire et de numéro de fichier australien Tax (égal).

![Possibilité de choisir un modèle de stratégie](media/DLP-create-test-tune-choose-policy-template.png)

Nommez votre nouvelle stratégie DLP. Le modèle de stratégie DLP correspond à celui par défaut, mais vous devez choisir un nom plus descriptif de votre choix, étant donné que plusieurs stratégies peuvent être créées à partir du même modèle.

![Option pour nommer votre stratégie](media/DLP-create-test-tune-name-policy.png)

Choisissez les emplacements de la stratégie s’applique à. Les stratégies DLP applicables à Exchange Online, SharePoint Online et OneDrive for Business. Je vais laisser cette stratégie configurée pour appliquer à tous les emplacements.

![Possibilité de choisir tous les emplacements](media/DLP-create-test-tune-choose-locations.png)

À la première étape de **Paramètres de stratégie** simplement accepter les valeurs par défaut pour l’instant. Il existe beaucoup de personnalisation que vous pouvez faire dans les stratégies DLP, mais les valeurs par défaut sont un point de départ précis.

![Options permettant de personnaliser le type de contenu à protéger](media/DLP-create-test-tune-default-customization-settings.png)

Après avoir cliqué sur **suivant** s’affiche avec une page de **Paramètres de stratégie** supplémentaire avec d’autres options de personnalisation. Pour une stratégie que vous souhaitez uniquement tester, voici où vous pouvez commencer à apporter quelques modifications.

- J’ai désactivé les conseils de stratégie pour maintenant, qui est une étape raisonnable à effectuer si vous testez simplement finaliser et que vous ne voulez pas encore rien afficher aux utilisateurs. Conseils de stratégie affichent des avertissements aux utilisateurs qu’ils sont sur le point de violer une stratégie DLP. Par exemple, un utilisateur d’Outlook s’affiche un avertissement indiquant que le fichier qu'ils avez joint contienne les numéros de carte de crédit et entraîne leur messagerie électronique à rejeter. L’objectif de conseils de stratégie consiste à arrêter le comportement non compatibles avant tout.
- J’ai également de réduire le nombre d’instances de 10 à 1, afin que cette stratégie détecte un partage de données de PII australien, pas seulement en bloc des données de partage.
- J’ai également ajouté un autre destinataire pour le courrier électronique de rapport d’incident.

![Paramètres de stratégie supplémentaires](media/DLP-create-test-tune-more-policy-settings.png)

Enfin, j’ai configuré cette stratégie pour exécuter en mode test à l’origine. Notez également une option pour désactiver les conseils de stratégie en mode test. Cela vous donne la possibilité d’avoir des conseils de stratégie activés dans la stratégie, mais ensuite décider s’il faut afficher ou de supprimer les durant le test.

![Option pour tester les stratégies d’abord](media/DLP-create-test-tune-test-mode.png)

Dans l’écran de la révision finale, cliquez sur **créer** pour terminer la création de la stratégie.

## <a name="test-a-dlp-policy"></a>Tester une stratégie DLP

Votre nouvelle stratégie DLP commencera à prennent effet dans environ 1 heure. Vous pouvez sit et attendre pour qu’il puisse être déclenché par l’activité utilisateur normal, ou vous pouvez essayer de déclencher vous-même. Précédemment liés à cette [rubrique sur les types d’informations sensibles](what-the-sensitive-information-types-look-for.md), qui fournit des informations sur comment déclencher DLP correspondances.

Par exemple, la stratégie DLP que j’avais créé pour cet article détectera les numéros de fichier tax australien (égal). Conformément à la documentation, la correspondance est basée sur les critères suivants.

![Documentation sur le dossier fiscal Australie](media/DLP-create-test-tune-Australia-Tax-File-Number-doc.png)
 
Pour illustrer la détection égal de manière plutôt pointue, un message électronique comportant les mots « Numéro » et une chaîne de 9 chiffre à proximité seront accès via sans problème. La stratégie DLP n’est pas déclenché parce que la chaîne de chiffres 9 doit transmettre la somme de contrôle qui indique qu’il est un égal valide et pas seulement une chaîne sans conséquence de nombres.

![Dossier fiscal Australie qui ne transmet pas de somme de contrôle](media/DLP-create-test-tune-email-test1.png)

En revanche, un message électronique comportant les mots « Numéro » et un égal valide qui transmet la somme de contrôle déclenche la stratégie. Pour l’enregistrement, égal j’utilise a été effectuée à partir d’un site Web qui génère valide, mais non authentique, TFNs. Il existe des sites similaires qui génèrent des [numéros de carte de crédit valide mais faux](http://www.fakecreditcardgenerator.net/). Ces sites sont très utiles, car une des erreurs plus courantes lors du test d’une stratégie DLP utilise un faux numéro n’est pas valide et ne peuvent être transmis la somme de contrôle (et par conséquent ne déclenche la stratégie).

![Dossier fiscal Australie qui transmet la somme de contrôle](media/DLP-create-test-tune-email-test2.png)

Le courrier électronique de rapport d’incident inclut le type d’informations sensibles détecté, le nombre d’instances ont été détecté et le niveau de confiance de la détection.

![Rapport indiquant le numéro d’incident détecté](media/DLP-create-test-tune-email-incident-report.png)

Si vous laissez votre stratégie DLP en mode test et analysez les e-mails de rapport d’incident, vous pouvez commencer à vous familiariser l’exactitude de la stratégie DLP et l’efficacité sera lorsqu’elle est appliquée. Outre les rapports d’incidents, vous pouvez [utiliser les rapports DLP](view-the-dlp-reports.md) pour afficher une vue agrégée des correspondances de stratégies entre votre client.

## <a name="tune-a-dlp-policy"></a>Paramétrer une stratégie DLP

Lorsque vous analysez votre correspondances de stratégie que vous souhaiterez peut-être apporter quelques modifications pour le comportement des stratégies. À titre d’exemple, vous pouvez déterminer qu’un égal dans le message électronique n’est pas un problème (je pense que son toujours, mais elle optez pour des raisons de démonstration), mais un problème est de deux ou plusieurs instances. Plusieurs instances peuvent être un scénario risqué comme un employé du courrier électronique d’une exportation CSV à partir de la base de données de ressources humaines à la partie externe, par exemple un service comptable externe. Vous préférez sans aucun doute quelque chose détecter et bloquer.

Dans la sécurité et le centre de conformité, vous pouvez modifier une stratégie existante pour ajuster le comportement.

![Option permettant de modifier la stratégie](media/DLP-create-test-tune-edit-policy.png)
 
Vous pouvez ajuster les paramètres d’emplacement afin que la stratégie s’applique uniquement aux charges de travail spécifiques ou à des comptes et des sites spécifiques.

![Options permettant de choisir des emplacements spécifiques](media/DLP-create-test-tune-edit-locations.png)

Vous pouvez également régler les paramètres de stratégie et modifier les règles pour l’adapter à vos besoins.

![Option permettant de modifier la règle](media/DLP-create-test-tune-edit-rule.png)

Lors de la modification d’une règle d’une stratégie DLP, vous pouvez modifier :

- Les conditions, y compris le type et le nombre d’instances de données sensibles qui déclencheront la règle.
- Les actions qui sont effectuées, telles que la restriction de l’accès au contenu.
- Notifications d’utilisateur, qui sont des conseils de stratégie qui sont affichent à l’utilisateur dans leur navigateur web ou le client de messagerie.
- Substitutions par l’utilisateur, ce qui détermine si les utilisateurs peuvent choisir de procéder à leur messagerie ou le tout de même de partage de fichiers.
- Rapports d’incidents, pour informer les administrateurs.

![Options permettant de modifier les composants d’une règle](media/DLP-create-test-tune-editing-options.png)

Pour cette démonstration j’ai ajouté des notifications de l’utilisateur à la stratégie (soyez prudent de le faire sans formations utilisateur), et autorisé aux utilisateurs de remplacer la stratégie avec une justification ou en marquant comme un faux positif. Notez que vous pouvez personnaliser le texte d’info-bulle de courrier électronique et de la stratégie si vous souhaitez inclure des informations supplémentaires sur les stratégies de votre organisation, ou demander aux utilisateurs de contacter le support si vous avez des questions.

![Options pour les notifications d’utilisateur et les substitutions](media/DLP-create-test-tune-user-notifications.png)

La stratégie contient deux règles pour la gestion de volume élevé et faible volume, veillez donc à la fois avec les actions que vous souhaitez modifier. Il s’agit d’une opportunité de traiter les cas différemment en fonction de leurs caractéristiques. Par exemple, vous pourrez permettre de remplacer les violations de faible volume, mais pas permettre de remplacer les violations de volume élevé.

![Une règle pour volume élevé et une règle de faible volume](media/DLP-create-test-tune-two-rules.png)

En outre, si vous souhaitez réellement bloquer ou restreindre l’accès au contenu qui constitue une violation de stratégie, vous devez configurer une action sur la règle à le faire.

![Option pour restreindre l’accès au contenu](media/DLP-create-test-tune-restrict-access-action.png)

Après avoir enregistré ces modifications aux paramètres de stratégie, je dois également revenir à la page principaux paramètres de la stratégie et activer l’option Afficher les conseils de stratégie aux utilisateurs lorsque la stratégie est en mode test. Il s’agit d’un moyen efficace pour présenter les stratégies DLP à vos utilisateurs finaux, effectuez sensibilisation des utilisateurs, sans risque de faux positifs trop dont l’impact sur leur productivité.

![Option permettant d’afficher des conseils de stratégie en mode test](media/DLP-create-test-tune-show-policy-tips.png)

Sur le côté serveur (ou le nuage côté si vous préférez), la modification peut prendront effet immédiatement, en raison de divers intervalles de traitement. Si vous apportez une modification de la stratégie DLP qui permet d’afficher les conseils de nouvelle stratégie à un utilisateur, l’utilisateur ne peut pas voir les modifications prennent effet immédiatement dans leur client Outlook, qui vérifie les modifications de stratégie toutes les 24 heures. Si vous voulez accélérer le processus pour le test, vous pouvez utiliser ce correctif du Registre pour [Effacer le dernier horodatage téléchargement à partir de la clé PolicyNudges](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451). Outlook télécharge les dernières informations de stratégie la prochaine fois que vous redémarrez et commencez la rédaction d’un message électronique.

Si vous avez activés les conseils de stratégie, l’utilisateur commence à voir les conseils dans Outlook et permettre signaler faux positifs vous lorsqu’elles se produisent.

![Conseil de stratégie avec l’option à signaler comme faux positif](media/DLP-create-test-tune-policy-tip-in-outlook.png)

## <a name="investigate-false-positives"></a>Examiner les faux positifs

Modèles de stratégie DLP ne sont pas idéal directement à l’emploi. Il est probable que vous trouverez des faux positifs qui se produisent dans votre environnement, c’est pourquoi il est donc important faciliter la pratique dans un déploiement de DLP, prendre le temps d’adéquate tester et optimiser vos stratégies.

Voici un exemple de faux positif. Ce message est assez sans conséquence. L’utilisateur est fournir leur numéro de téléphone mobile à une personne et notamment leur signature électronique.

![Messagerie illustrant les faux positif](media/DLP-create-test-tune-false-positive-email.png)
 
Mais l’utilisateur voit un Conseil de stratégie les avertissant que le courrier électronique contienne des informations sensibles, en particulier, le nombre de licences un permis de conduire Australie.

![Permet de signaler comme faux positif dans le Conseil de stratégie](media/DLP-create-test-tune-policy-tip-closeup.png)

L’utilisateur peut signaler le faux positif, et l’administrateur peut consulter pourquoi il s’est produite. Dans le message électronique de rapport d’incident, le message est marqué comme faux positif.

![Faux positif de rapport d’incident affichant](media/DLP-create-test-tune-false-positive-incident-report.png)

Cas de licence de ce pilote est un bon exemple approfondir. La raison pour laquelle ce faux positif s’est produite qui est le type est déclenché par n’importe quelle chaîne 9 chiffres (même un qui fait partie d’une chaîne de 10 chiffres), « australien permis de conduire » au sein de proximité 300 caractères les mots clés « nouvelle sydney » (non sensible à la casse). Ainsi, il est déclenché par la signature d’e-mail et numéro de téléphone, uniquement parce que l’utilisateur se trouve dans Sydney.

Intéressant, si « Sydney, nouvelle » possède une virgule, la stratégie DLP n’est pas déclenchée. J’ai aucune idée pourquoi une virgule fait aucune différence ici, ni pourquoi villes et les autres États en Australie ne sont pas inclus dans les mots clés pour le type d’information les permis de conduire Australie licence, mais il vous accédez. Par conséquent, que faire parler ? Il existe deux options.

Une option consiste à supprimer le type d’information les permis de conduire Australie licence de la stratégie. Il est là, car il fait partie du modèle de stratégie DLP, mais nous ne sommes pas obligés de l’utiliser. Si vous êtes uniquement intéressé par pas permis de conduire et les numéros des fichiers, vous pouvez simplement le supprimer. Par exemple, vous pouvez supprimer de la règle de faible volume dans la stratégie, mais laissez dans la règle de volume élevé afin que les listes de plusieurs licences pilotes sont toujours détectés.

![Option permettant de supprimer des informations sensibles type de règle](media/DLP-create-test-tune-delete-low-volume-rule.png)
 
Une autre option consiste à simplement augmenter le nombre d’instances, afin qu’un faible volume de conduire permis d’est détecté uniquement lorsqu’il existe plusieurs instances.

![Option permettant de modifier le nombre d’instances](media/DLP-create-test-tune-edit-instance-count.png)

En plus de modifier le nombre d’instances, vous pouvez également ajuster la correspondance de précision (ou niveau de confiance). Si votre type d’informations sensibles a plusieurs modèles, vous pouvez régler la précision de correspondance dans votre règle, afin que votre règle établit une correspondance avec des modèles spécifiques. Par exemple, pour vous aider à réduire les faux positifs, vous pouvez définir l’exactitude de la correspondance de votre règle afin qu’elle corresponde à uniquement le modèle avec le niveau de confiance plus élevé. Présentation du mode de calcul de niveau de confiance est un peu délicat (et au-delà de la portée de cet article), mais voici une bonne explication de [l’utilisation de niveau de confiance pour régler vos règles](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy).

Enfin, si vous souhaitez obtenir encore un peu plus avancée, vous pouvez personnaliser n’importe quel type d’informations sensibles : par exemple, vous pouvez supprimer « Nouvelle Sydney » dans la liste des mots clés [de conduire Australie](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number), afin d’éliminer les faux positif déclenché au-dessus. Pour savoir comment procéder à l’aide de XML et PowerShell, consultez cette rubrique sur la [personnalisation d’un type d’informations sensibles intégrés](customize-a-built-in-sensitive-information-type.md).

## <a name="turn-off-a-dlp-policy"></a>Désactivation d’une stratégie DLP

Lorsque vous êtes satisfait que votre stratégie DLP est correctement et détecter efficacement les types d’informations sensibles, et que vos utilisateurs finaux êtes prêts à traiter les stratégies en place, vous pouvez activer la stratégie.

![Option pour activer la stratégie](media/DLP-create-test-tune-turn-on-policy.png)
 
Si vous vous attendez à voir lorsque la stratégie sera prennent effet, [se connecter à Office 365 sécurité & PowerShell du centre de conformité](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) et exécutez la [cmdlet Get-DlpCompliancePolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) pour voir la DistributionStatus.

![Applet de commande en cours d’exécution de PowerShell](media/DLP-create-test-tune-PowerShell.png)

Après avoir activé la stratégie DLP, vous devez exécuter des tests finals votre propre s’assurer que les actions de stratégie attendue sont en cours. Si vous essayez de tester les éléments tels que les données de carte de crédit, il existe des sites Web en ligne avec plus d’informations sur comment générer l’exemple de carte de crédit ou d’autres informations personnelles qui transmet les totaux de contrôle et déclencher vos stratégies.

Les stratégies qui autorisent les substitutions utilisateur présentera cette option à l’utilisateur dans le cadre d’une info-bulle de stratégie.

![Conseil de stratégie permettant de remplacement d’utilisateur](media/DLP-create-test-tune-override-option.png)

Les stratégies qui restreignent le contenu seront présenter l’avertissement à l’utilisateur dans le cadre d’une info-bulle de stratégie et les empêcher d’envoyer le courrier électronique.

![Conseil de stratégie que le contenu est limité](media/DLP-create-test-tune-restrict-warning.png)

## <a name="summary"></a>Résumé

Stratégies de protection contre la perte de données sont utiles pour les organisations de tous types. Test des stratégies DLP est un exercice risque faible en raison du contrôle sur les éléments tels que les conseils de stratégie, de remplacements de l’utilisateur final et rapports d’incidents. Vous pouvez tester en mode silencieux des stratégies DLP pour voir quel type de violations se produisent déjà dans votre organisation, puis élaborer des tâches avec faible taux de faux positifs, former les utilisateurs sur ce qui est autorisé et non autorisé et puis déploiement vos stratégies DLP pour le organisation.
