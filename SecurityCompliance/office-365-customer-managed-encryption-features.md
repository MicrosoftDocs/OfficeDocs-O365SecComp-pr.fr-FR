---
title: Fonctionnalités de chiffrement gérés par le client Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Découvrez la résistance des données dans Microsoft Office 365.'
ms.openlocfilehash: e835587e07246154cd700555cc7263370bde8755
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527512"
---
# <a name="customer-managed-encryption-features-in-office-365"></a>Fonctionnalités de client géré de chiffrement dans Office 365

Avec les technologies de chiffrement dans Office 365 est géré par Microsoft, Office 365 fonctionne également avec les technologies de chiffrement supplémentaires que vous pouvez gérer et configurer, telles que :
- [Gestion des droits Azure](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms)
- [Secure Multipurpose Internet Mail Extension](http://blogs.technet.com/b/exchange/archive/2014/12/15/how-to-configure-s-mime-in-office-365.aspx)
- [Chiffrement de messages Office 365](http://products.office.com/en-us/exchange/office-365-message-encryption)
- [Flux de messagerie sécurisée avec une organisation partenaire](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-for-secure-mail-flow-with-a-partner)

Vous trouverez également des informations supplémentaires sur ces technologies dans les [descriptions des services Office 365](https://technet.microsoft.com/en-us/library/office-365-service-descriptions.aspx).

## <a name="azure-rights-management"></a>Gestion des droits Azure
[Azure Rights Management](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms) (Azure RMS) est la technologie de protection utilisée par [La Protection des informations Azure](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection). Il utilise des stratégies de chiffrement, d’identité et d’autorisation pour aider à sécuriser vos fichiers et de messagerie sur plusieurs plateformes et périphériques, téléphones, tablettes et PC informations peuvent être protégées au sein et en dehors de votre organisation, car la protection reste avec les données. RMS Azure offre une protection permanente de tous les types de fichiers, protège les fichiers de n’importe où, prend en charge la collaboration d’entreprise-entreprise et une large gamme de Windows et les périphériques non Windows. Protection RMS Azure peut augmenter également les [stratégies de protection contre la perte de données](https://docs.microsoft.com/exchange/security-and-compliance/data-loss-prevention/data-loss-prevention). Pour plus d’informations sur les services et applications peuvent utiliser le service de Azure Rights Management à partir de la Protection des informations Azure, voir [comment les applications prennent en charge le service Azure Rights Management](https://docs.microsoft.com/information-protection/understand-explore/applications-support).

Azure RMS est intégrée à Office 365 et disponibles pour tous les clients Office 365. Pour configurer Office 365 pour utiliser RMS Azure, voir [configurer l’IRM à utiliser Azure Rights Management et Set up Information Rights Management (IRM) dans le centre d’administration SharePoint](https://technet.microsoft.com/en-us/library/dn151475(v=exchg.150).aspx). Si vous utilisez le serveur Active Directory (AD) RMS local, puis vous pouvez également [configurer IRM pour utiliser un site sur un serveur AD RMS](https://docs.microsoft.com/office365/SecurityCompliance/configure-irm-to-use-an-on-premises-ad-rms-server), mais nous vous recommandons vivement à [migrer vers Azure RMS](https://docs.microsoft.com/azure/information-protection/migrate-from-ad-rms-to-azure-rms) à utiliser les nouvelles fonctionnalités comme la collaboration sécurisée avec les autres organisations.

Lorsque vous protégez les données des clients avec Azure RMS, Azure RMS utilise une clé asymétrique RSA de 2048 bits avec l’intégrité de l’algorithme de hachage SHA-256 pour chiffrer les données. La clé symétrique pour les documents Office et le message électronique est AES 128 bits (mode CBC avec remplissage PKCS #7). Pour chaque document ou un courrier électronique qui est protégé par RMS Azure, Azure RMS crée une seule clé AES (« clé de contenu »), et cette clé est incorporée dans le document et persiste par le biais de versions du document. La clé de contenu est protégée par RSA clé (le « Azure Protection des informations client ») l’organisation dans le cadre de la stratégie dans le document et que la stratégie est également connectée par l’auteur du document. Cette clé de client est commune à tous les documents et les messages électroniques qui sont protégés par RMS Azure pour l’organisation et cette clé peut uniquement être modifiée par un administrateur de la Protection des informations Azure si l’organisation utilise une clé de client qui est géré par le client. Pour plus d’informations sur les contrôles de chiffrement utilisés par Azure RMS, voir [comment fonctionne RMS Azure ? Dans les coulisses](https://docs.microsoft.com/information-protection/understand-explore/how-does-it-work).

Dans une implémentation Azure RMS par défaut, Microsoft génère et gère la clé racine qui est unique pour chaque client. Clients peuvent gérer le cycle de vie de leur clé racine dans Azure RMS avec Azure clé coffre-fort Services à l’aide d’une méthode de gestion de clés appelée [Mettre votre propre clé (BYOK)](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key) ) qui permet de générer votre clé dans HSM sur site et garder le contrôle de cette clé après transfert FIPS 140-2 niveau 2-validé HSM. pour de Microsoft accéder à la clé racine n’est pas attribué à n’importe quel personnel comme les clés ne peuvent pas être exportées ou extrait les modules de sécurité matérielle leur protection. En outre, vous pouvez accéder un journal en temps réel near affichant tous les accès à la clé racine à tout moment. Pour plus d’informations, voir [Logging and analyse Azure Rights Management d’utilisation](https://docs.microsoft.com/azure/information-protection/log-analyze-usage).

Azure Rights Management permet atténue les menaces comme espionnage sophistiqué, attaques man-in-the-middle, le vol de données et les violations de stratégies de partage d’organisation involontaires. En même temps, aucun accès injustifiés des données du client en transit ou au repos par un utilisateur non autorisé qui ne possède pas les autorisations appropriées n’est pas autorisé par le biais des stratégies qui suivent que les données, et réduire les risques de ces données appartenant au bon transmet soit sciemment ou non et en fournissant des fonctions de protection contre la perte de données. En cas d’utilisation dans le cadre de la Protection des informations Azure, RMS Azure fournit également la Classification des données et étiquetage des capacités, le marquage de contenu, document suivi et l’accès révocation capacités d’accès. Pour en savoir plus sur ces fonctionnalités, voir [qu’est la Protection des informations Azure](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection), [plan de déploiement de la Protection des informations Azure](https://docs.microsoft.com/information-protection/plan-design/deployment-roadmap)et [didacticiel de démarrage rapide pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/get-started/infoprotect-quick-start-tutorial).

## <a name="secure-multipurpose-internet-mail-extension"></a>Secure Multipurpose Internet Mail Extension
Secure/Multipurpose Internet Mail Extensions (S/MIME) est une norme de chiffrement de clé publique et la signature numérique de données MIME. S/MIME est défini dans RFC 3369, 3370, 3850, 3851 et d’autres personnes. Il permet à un utilisateur chiffrer un message électronique et de signer numériquement un message électronique. Un message électronique qui est chiffré à l’aide de S/MIME pour pouvoir être déchiffré uniquement par le destinataire du courrier électronique à l’aide de sa clé privée, qui est uniquement disponible à ce destinataire. En tant que telles les e-mails ne peut pas être déchiffrés par toute personne autre que le destinataire du message électronique.

[Microsoft prend en charge S/MIME dans Office 365](http://blogs.technet.com/b/exchange/archive/2014/12/15/how-to-configure-s-mime-in-office-365.aspx). Certificats publics sont distribués sur site Active Directory du client et stockées dans les attributs qui peuvent être répliqués sur un client Office 365. Les clés privées qui correspondent aux clés publiques restent locales et ne sont jamais transmis à Office 365. Les utilisateurs peuvent composer, chiffrer, déchiffrer, lire et signer numériquement des messages électroniques entre deux utilisateurs dans une organisation à l’aide d’Outlook, Outlook sur le web et les clients Exchange ActiveSync. Pour plus d’informations, voir [chiffrement S/MIME maintenant dans Office 365](http://blogs.office.com/2014/02/26/smime-encryption-now-in-office-365/).

## <a name="office-365-message-encryption"></a>Chiffrement de messages Office 365
[Office 365 Message Encryption](https://products.office.com/en-us/exchange/office-365-message-encryption) (OME) greffées permet [La Protection des informations Azure](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection) (AIP) vous permet d’envoyer chiffré et protégé par des droits de messagerie à tout le monde. OME permet d’atténuer les menaces telles qu’espionnage sophistiqué et les attaques man-in-the-middle et autres menaces, telles qu’injustifiés accès aux données par un utilisateur non autorisé qui ne dispose pas des autorisations appropriées. Nous avons investi qui vous fournir une expérience de messagerie plus simple, plus intuitive et sécurisée greffée Azure la Protection des informations. Vous pouvez protéger les messages envoyés à partir d’Office 365 à tous les utilisateurs à l’intérieur ou à l’extérieur de votre organisation. Ces messages peuvent être affichés dans une variété de clients de messagerie à l’aide de n’importe quelle identité, y compris Azure Active Directory, Microsoft Account et ID de Google. Pour plus d’informations sur la façon dont votre organisation peut utiliser des messages chiffrés, voir [Office 365 Message Encryption](https://support.office.com/article/F87CB016-7876-4317-AE3C-9169B311FF8A).

## <a name="transport-layer-security"></a>Transport Layer Security
Si vous souhaitez sécuriser la communication avec un partenaire, vous pouvez utiliser des connecteurs entrants et sortants pour fournir la sécurité et l’intégrité des messages. Vous pouvez configurer TLS forcé d’entrant et sortant sur chaque connecteur, à l’aide d’un certificat. À l’aide d’un canal SMTP chiffré peut empêcher les données des vols par le biais d’une attaque man-in-the-middle. Pour plus d’informations, voir [comment Exchange Online utilise TLS pour sécuriser les connexions de messagerie](https://support.office.com/article/How-Exchange-Online-uses-TLS-to-secure-email-connections-in-Office-365-4CDE0CDA-3430-4DC0-B489-F2C0736C929F).

## <a name="domain-keys-identified-mail"></a>Clés de domaine identifié de messagerie
Exchange Online Protection (EOP) et Exchange Online prend en charge la validation entrante de messages DKIM Domain Keys Identified Mail (). DKIM est une méthode de validation qu’un message a été envoyé à partir du domaine, d' qu'il indique qu’il provient et qu’il a été falsifié pas par une autre personne. Il lie un message électronique à l’organisation responsable de l’envoyer et fait partie d’un modèle plus grand de chiffrement du courrier électronique. Pour plus d’informations sur les trois parties de ce modèle, voir :
- [Configurer SPF dans Office 365 pour empêcher l’usurpation](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)
- [Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)
- [Utiliser DMARC pour valider les e-mails dans Office 365](https://https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)