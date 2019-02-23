---
title: "Forum aux questions sur la protection anti-courrier indésirable" ms. Author: krowley Author: kccross Manager: laurawi ms. Date: 12/9/2016 ms. audience: professionnel ms. topic: article ms. service: O365-seccomp ms. Custom: TN2DMC localization_priority: normal Search. appverid:
- MET150 ms. AssetID: c534a35d-B121-45DA-9d0a-ce738ce51fce ms. collection:
    - M365-Security-Description de la conformité: «cette rubrique fournit des questions fréquemment posées et des réponses sur la protection contre le courrier indésirable. Les réponses sont applicables pour les clients Microsoft Exchange Online et Exchange Online Protection (EOP). "
---

# <a name="anti-spam-protection-faq"></a>Forum Aux Questions sur la protection anti-courrier indésirable

Cette rubrique fournit des réponses aux questions fréquemment posées concernant la protection contre le courrier indésirable. Les réponses s'appliquent aux clients de Microsoft Exchange Online et Exchange Online Protection (EOP). 
  
> [!TIP]
> Pour obtenir des questions et des réponses sur les listes d'expéditeurs approuvés et d'expéditeurs bloqués, consultez la rubrique [Safe sender and blocked sender Lists in Exchange Online](safe-sender-and-blocked-sender-lists-faq.md). Pour obtenir des questions et des réponses sur la mise en quarantaine, consultez la rubrique [mise en quarantaine](quarantine-faq.md). 
  
 **Q. Par défaut, qu'arrive-t-il à un message identifié comme courrier indésirable ?**
  
R. **Pour les messages entrants :** L'essentiel du courrier indésirable est supprimé par filtrage des connexions, sur la base de l'adresse IP de l'expéditeur. Le service inspecte ensuite le contenu du message. Par défaut, le courrier indésirable filtré sur le contenu est envoyé au dossier Courrier indésirable du destinataire. Vous pouvez modifier ce comportement. Par exemple, vous pouvez mettre les messages de courrier indésirable en quarantaine en configurant la stratégie de filtrage de contenu. 
  
> [!IMPORTANT]
> Pour les clients autonomes EOP : Afin que l'action **Déplacer le message dans le dossier Courrier indésirable** fonctionne avec des boîtes aux lettres locales, vous devez configurer deux règles de transport Exchange sur vos serveurs locaux de manière à détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, consultez la rubrique [Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
 **Pour les messages sortants :** le message est routé par le pool de remise à risque plus élevé ou est retourné et non remis. Dans ce cas, l'expéditeur doit recevoir un message de notification d'état de remise (DSN) indiquant que le message n'a pas pu être remis. 
  
 **Q. Qu'est-ce qu'une variante « zero-day » et comment est-elle gérée par le service ?**
  
R. Une variante « zero-day » est une variante de courrier indésirable de première génération, auparavant inconnue, qui n'a jamais été capturée ni analysée. Par conséquent, nos filtres de contenu de courrier indésirable ne disposent pas encore des informations nécessaires pour la détecter. Une fois qu'un exemple de courrier indésirable « zero-day » est capturé et analysé par nos analystes de courrier indésirable, et s'il répond aux critères de classification, nos filtres de contenu de courrier indésirable sont mis à jour pour le détecter, et il n'est plus considéré comme « zero-day ». ( **Remarque :** si vous recevez un message susceptible d'être une variante de courrier indésirable « zero-day », pour nous aider à améliorer le service, veuillez soumettre le message à Microsoft à l'aide de l'une des méthodes décrites dans la rubrique [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).)
  
 **Q. Dois-je configurer le service pour bénéficier d'une protection anti-courrier indésirable ?**
  
R. Après vous être inscrit au service et avoir ajouté votre domaine, le filtrage du courrier indésirable est automatiquement activé pour l'ensemble de l'organisation via les stratégies anti-courrier indésirable par défaut. Les stratégies par défaut sont réglées pour vous protéger sans avoir à effectuer de configuration supplémentaire (sauf l'exception indiquée ci-dessus pour les clients autonomes EOP). En qualité d'administrateur, vous pouvez modifier les stratégies anti-courrier indésirable par défaut pour les adapter au mieux aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.
  
Pour plus d'informations sur la configuration de vos stratégies anti-spam, consultez les rubriques suivantes :
  
[Configuration de la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md)
  
[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  
 **Q. Si je modifie une stratégie anti-courrier indésirable, combien de temps après l'enregistrement de mes changements ces derniers prennent-ils effet ?**
  
R. Les changements devraient prendre effet au bout d'une heure maximum.
  
 **Q. Le filtrage des messages électroniques en bloc est-il automatiquement activé ?**
  
R. Par défaut, l'option avancée de filtrage du courrier indésirable **Courrier électronique en masse** est activée pour les nouveaux clients. Pour les clients migrés, ce paramètre correspond à la configuration FOPE. Pour plus d'informations sur le courrier en masse, voir [Quelle est la différence entre courrier indésirable et message électronique en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md)
  
 **Q. Le service fournit-il le filtrage d'URL ?**
  
R. Oui, le service a un filtre d'URL qui vérifie les URL contenues dans les messages. Si des URL associées à du contenu indésirable ou malveillant connu sont détectées, le message est marqué comme courrier indésirable.
  
 **Q. Comment les clients utilisant le service peuvent-ils signaler des faux négatifs (courrier indésirable) et des faux positifs (messages légitimes) à Microsoft ?**
  
R. Les messages de courrier indésirable et de courrier non indésirable peuvent être envoyés à Microsoft pour être analysés de plusieurs façons. Pour plus d'informations, consultez [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). 
  
 **Q. Puis-je obtenir des rapports sur le courrier indésirable ?**
  
R. Oui. Par exemple, vous pouvez obtenir un rapport de détection de courrier indésirable dans le centre d'administration Office 365. Ce rapport indique le volume de courrier indésirable sous la forme d'un nombre de messages uniques. Pour plus d'informations sur les rapports, consultez les liens suivants :
  
Clients Exchange Online: [surveillance, création de rapports et suivi des messages dans Exchange Online](http://technet.microsoft.com/library/87bdeeae-bd80-4a3b-95c5-62fbaf97c2e8.aspx)
  
Clients Exchange Online Protection: [création de rapports et suivi des messages dans Exchange Online Protection](eop/reporting-and-message-trace-in-exchange-online-protection.md)
  
 **Q. quelqu'un m'a envoyé un message et je ne le trouve pas. Je pense qu'elle a peut-être été détectée comme courrier indésirable. Existe-t-il un outil permettant de découvrir?**
  
R. Oui, l'outil de suivi des messages vous permet de suivre les messages électroniques quand ils sont acheminés via le service afin de déterminer ce qui leur est arrivé. Pour plus d'informations sur l'utilisation de l'outil de suivi des messages pour comprendre pourquoi un message a été détecté comme courrier indésirable, consultez la rubrique [Le message a-t-il été marqué comme courrier indésirable ?](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx#BKMB_Whywasamessagemarkedasspam)
  
 **Q. Le service limite-t-il (limite de débit) ma messagerie si mes utilisateurs envoient du courrier indésirable sortant ?**
  
R. Si plus de la moitié du courrier envoyé via le service par un même utilisateur au cours d'une certain laps de temps (par exemple, par heure) est considéré comme indésirable par Office 365, l'utilisateur ne peut plus envoyer de messages. Dans la plupart des cas, si un message sortant est déterminé comme étant du courrier indésirable, il est routé via le pool de remises à haut risque, ce qui réduit la probabilité d'ajout du pool d'IP sortantes normales à une liste rouge.
  
Vous pouvez envoyer une notification à une adresse de messagerie spécifique quand un utilisateur est bloqué en relation avec l'envoi de courrier indésirable sortant. Pour plus d'informations sur ce paramètre, consultez la rubrique [Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md).
  
 **Q. Puis-je utiliser un fournisseur tiers de blocage de courrier indésirable et de programme malveillant en association avec Exchange Online ?**
  
R. Oui, vous pouvez configurer un autre service de filtrage anti-courrier indésirable et anti-programme malveillant pour protéger vos boîtes aux lettres Exchange Online. Pour le courrier entrant, vous devez rediriger les messages électroniques vers le fournisseur tiers en modifiant vos enregistrements MX afin qu'ils pointent vers ce fournisseur, puis rediriger les messages vers EOP à des fins de traitement supplémentaire. Pour le courrier sortant, configurez la destination de remise de message au fournisseur tiers (hôte actif), comme indiqué dans la rubrique [Scenario: Outbound Smart Hosting](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx).
  
 **Q. Est-ce que Microsoft dispose de documentation concernant la façon dont je peux me protéger contre les tentatives de hameçonnage ?**
  
Oui, en effet, veuillez consulter les articles suivants :
  
[Obtenez de l'aide pour les escroqueries par hameçonnage, les fraudes de loteries et autres types d'arnaques](http://go.microsoft.com/fwlink/p/?LinkId=325606)
  
Arnaques par message électronique ou site web : [comment se protéger](http://go.microsoft.com/fwlink/p/?LinkID=325607)
  
 **Q. Le courrier indésirable et les messages malveillants font-ils l'objet d'une enquête pour savoir qui les a envoyés, ou sont-ils transférés à des services chargés de l'application de la loi ?**
  
R. Le service se concentre sur la détection et la suppression du courrier indésirable et des programmes malveillants. Il nous arrive toutefois d'enquêter sur des campagnes de courrier indésirable ou d'attaque particulièrement dangereuses ou nuisibles, et de poursuivre leurs auteurs. Cela peut impliquer une collaboration avec nos unités criminalité numérique et juridique afin de retrouver le réseau zombie de l'expéditeur du courrier indésirable, d'empêcher celui-ci d'utiliser le service (s'il l'utilise pour envoyer des messages sortants) et de transmettre les informations à la justice en vue de poursuites pénales.
  
 **Q. Quelles sont les meilleures pratiques d'envoi de courrier sortant pour garantir la remise de mes messages électroniques ?**
  
R. Les instructions ci-dessous constituent les meilleures pratiques pour l'envoi de messages électroniques sortants.
  
1. **Le domaine d'envoi du message électronique doit se résoudre dans DNS.**
    
    Par exemple, si l'expéditeur est user@example.com, le domaine example.com est résolu en adresse IP 192.0.43.10. Si un domaine d'envoi n'a pas d'enregistrement A et aucun enregistrement MX dans le système DNS, le service achemine le message via le pool de remise à risque plus élevé que le contenu du message soit ou non du courrier indésirable. Pour plus d'informations sur le pool de remise à risque plus élevé, consultez la rubrique [pool de remise à haut risque pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md). 
    
2. **L'adresse IP d'envoi du serveur de courrier sortant doit avoir une entrée DNS inversée (PTR).**
    
    Par exemple, en cas d'envoi à partir de l'adresse IP 192.0.43.10, l'entrée DNS inversée pour cette adresse IP est 43-10.any.icann.org. 
    
3. **Les commandes HELO/EHLO et MAIL FROM doivent être cohérentes, et se présenter sous la forme d'un nom de domaine plutôt que d'une adresse IP.**
    
    La commande HELO/EHLO doit être configurée pour correspondre à la DNS inversée de l'adresse IP d'envoi, de façon à ce que le domaine ne change pas dans les diverses parties des en-têtes de message.
    
4. **Veillez à ce que les enregistrements SPF appropriés soient configurés dans DNS.**
    
    Les enregistrements SPF constituent un mécanisme permettant de valider le fait que du courrier électronique envoyé par un domaine provient réellement de ce dernier et n'est pas falsifié. Pour plus d'informations sur les enregistrements SPF, consultez les liens suivants :
    
    [Configurer SPF dans Office 365 pour empêcher l’usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
    
    [Créer des enregistrements DNS pour Office 365](https://go.microsoft.com/fwlink/?LinkID=275414)
    
5. **Signature de courrier électronique avec DKIM, canonisation assouplie.**
    
    Si un expéditeur souhaite signer ses messages à l'aide de la technologie DKIM (Domain Keys Identified Mail) et envoyer du courrier sortant via le service, il doit utiliser l'algorithme de canonisation d'en-tête assouplie. Signer avec une canonisation d'en-tête stricte peut entraîner une invalidation de la signature par le service.
    
6. **Les propriétaires de domaine doivent disposer d'informations exactes dans la base de données WHOIS.**
    
    Ces informations identifient les propriétaires de domaine et indiquent comment les contacter en entrant la société mère stable, le point de contact et les serveurs de noms.
    
7. **Pour les publipostages en bloc, le nom de: doit indiquer la personne qui envoie le message, tandis que la ligne d'objet du message doit être un bref résumé de la description du message.**
    
    Le corps du message doit contenir une indication claire concernant l'offre, le service ou le produit. Par exemple, si un expéditeur envoie un publipostage pour le compte de la société Contoso, voici à quoi doit ressembler le contenu des champs De et Objet du message électronique :
    
    De : marketing@contoso.com
    
    Objet : Nouveau catalogue à jour pour la période de Noël 
    
    Voici un exemple de ce qu'il ne faut pas faire parce que ce n'est pas assez descriptif :
    
    De : utilisateur@hotmail.com
    
    Objet : Catalogues
    
8. **Si vous envoyez un publipostage à un grand nombre de destinataires et que le message présente le format d'un bulletin d'informations, il doit contenir un lien de désabonnement au bas du texte de contenu.**
    
    L'option de désabonnement doit ressembler à ceci :
    
    Ce message a été adressé à exemple@contoso.com par expéditeur@fabrikam.com. Mise à jour du profil ou de l'adresse de messagerie | Suppression immédiate avec **SafeUnsubscribe** | Politique de confidentialité
    
9. **En cas d'envoi d'un publipostage, l'acquisition de liste doit être effectuée à l'aide d'un contrôle de consentement double (double opt-in). Si vous êtes un expéditeur de publipostage, cette pratique est recommandée par le secteur.**
    
    La pratique de contrôle de consentement double consiste à demander à un utilisateur d'effectuer deux actions pour confirmer son abonnement à un courrier électronique marketing :
    
1. une première fois en cliquant sur une case à cocher non encore activée pour indiquer qu'il consent à recevoir d'autres offres ou messages électroniques du mercaticien ;
    
2. une deuxième fois lorsque le mercaticien envoie un message électronique de confirmation à l'adresse de messagerie fournie par l'utilisateur, lui demandant de cliquer sur un lien sensible au temps pour valider sa confirmation.
    
    Pour les expéditeurs de publipostages, le recours au contrôle de consentement double a pour effet de leur forger une bonne réputation.
    
10. **Les expéditeurs de publipostage doivent proposer un contenu transparent dont ils peuvent être jugés responsables :**
    
1. Tout texte demandant au destinataire d'ajouter l'expéditeur à son carnet d'adresses devrait clairement indiquer qu'une telle action ne constitue par une garantie de remise.
    
2. Lors de l'élaboration de redirections dans le corps du message, utilisez un style de lien cohérent.
    
3. N'envoyez pas d'images ou de pièces jointes volumineuses, ou des messages contenant uniquement une image.
    
4. Si vous utilisez des pixels de suivi (bogues ou balises web), signalez clairement leur présence dans vos paramètres publics de confidentialité ou P3P.
    
11. **Mettez en forme les notifications d'état de remise du courrier sortant.**
    
    Lors de la génération de messages de notification d'état de remise, les expéditeurs doivent suivre le format de notification de non-remise, tel que spécifié dans la rubrique [RFC 3464](https://go.microsoft.com/fwlink/?LinkId=279715).
    
12. **Supprimez les adresses de messagerie de notification de non-remise pour les utilisateurs inexistants.**
    
    Si vous recevez une notification d'échec de remise (NDR) indiquant qu'une adresse de messagerie n'est plus utilisée, supprimez l'alias correspondant de votre liste. Les adresses électroniques changent au fil du temps et certaines personnes les abandonnent.
    
13. **Utilisez le programme Smart Network Data Services (SNDS) de Hotmail.**
    
    Hotmail utilise un programme nommé Smart Network Data Services qui permet aux expéditeurs de consulter des plaintes d'utilisateurs finaux. Le programme SNDS est le portail principal pour le dépannage des problèmes de remise liés à Hotmail.
    
## <a name="for-more-information"></a>Pour plus d'informations

[Protection contre le courrier indésirable pour Office 365](https://support.office.com/article/6a601501-a6a8-4559-b2e7-56b59c96a586)
  
[Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online](safe-sender-and-blocked-sender-lists-faq.md)
  
[En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md)
  
[Messages de rétrodiffusion et EOP](backscatter-messages-and-eop.md)
  

