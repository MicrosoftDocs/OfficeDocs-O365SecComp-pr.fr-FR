---
title: Champs de métadonnées de document dans Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 33e2603aaeb4505768e76149b76dc18648250a52
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151936"
---
# <a name="document-metadata-fields-in-advanced-ediscovery"></a>Champs de métadonnées de document dans Advanced eDiscovery

Le tableau suivant répertorie les champs de métadonnées pour les documents dans un ensemble de révision dans un cas dans Advanced eDiscovery. Le tableau indique le nom du champ de métadonnées, indique s’il est possible d’effectuer une recherche dans le champ lors de l’exécution d’une requête dans un jeu de vérification, si le champ est présent lors de l’affichage des métadonnées d’un document sélectionné dans un jeu de révisions, et si le champ est inclus ou non lorsque des documents à nouveau exporté.

| Nom du champ | Nom de champ pouvant faire l’objet d’une recherche | Nom du champ exporté | Nom du champ d’affichage | Description |
| :- |  :- |  :- |  :- |  :- |
| ID de contenu de pièce jointe | AttachmentContentId |  | ID de contenu de pièce jointe | ID de contenu de la pièce jointe de l’élément. |
| Noms des pièces jointes | AttachmentNames | Attachment_Names | Noms des pièces jointes | Liste des noms des pièces jointes. |
| Score de privilège client pour les avocats | AttorneyClientPrivilegeScore |  | Score de privilège client pour les avocats | Avocat-score de contenu du modèle de privilège client. |
| Auteur | Auteur | Doc_authors | Auteur | Auteur à partir des métadonnées du document. |
| Cci | Cci | Email_bcc | Cci | Champ CCI pour les types de message.  Le format **est \<DisplayName SMTPAddress>**. |
| Cc | Cc | Email_cc | Cc | Champ CC pour les types de message.  Le format **est \<DisplayName SMTPAddress>**. |
| Étiquettes de conformité | ComplianceLabels | Compliance_labels | Étiquettes de conformité | Étiquettes de conformité appliquées dans Office 365. |
| Tracé transparent | CompoundPath | Compound_path | Tracé transparent | Chemin lisible par l’utilisateur qui décrit la source de l’élément. |
| Contenu | Contenu |  |  | Texte extrait de l’élément. |
| Corps de la conversation | Corps de la conversation |  | Corps de la conversation | Corps de la conversation de l’élément. |
| Sujet de conversation | Sujet de conversation |  | Sujet de conversation | Sujet de conversation de l’élément. |
| ID de conversation | ConversationId | Conversation_ID | ID de conversation | ID de conversation du message. |
| Index des conversations |  | Conversation_index | Index des conversations | Index des conversations à partir du message. |
| Heure du fichier PDF de conversation | ConversationPdfTime |  | Heure du fichier PDF de conversation | Date de création de la version PDF de la conversation. |
| Temps de gravure de la rédaction de conversation | ConversationRedactionBurnTime |  | Temps de gravure de la rédaction de conversation | Date à laquelle la version PDF de la conversation a été créée pour la conversation. |
| Date de création du document | CreatedTime | Doc_date_created | Date de création du document | Créer une date à partir des métadonnées du document. |
| Custodian | Custodian | Custodian | Custodian | Nom du dépositaire auquel l’élément a été associé. |
| Date | Date | Date | Date | Date est un champ calculé qui dépend du type de fichier.<br />**Courrier électronique**: date d’envoi<br />**Pièces jointes de courrier électronique**: date de dernière modification du document, si elle n’est pas disponible, la date d’envoi du parent<br />**Documents incorporés**: date de dernière modification du document, si elle n’est pas disponible, date de la dernière modification du parent.<br />**Documents SPO (y compris les pièces jointes modernes)**: date de dernière modification de SharePoint, si elle n’est pas disponible, la date de la dernière modification des documents.<br />**Documents non Office**: date de la dernière modification<br />**Réunions**: date de début de la réunion<br />**Messagerie vocale**: date d’envoi<br />**Messagerie instantanée**: date d’envoi. |
| Autres chemins d’accès | Dedupedcompoundpath | Deduped_compound_path | Autres chemins d’accès | Liste des chemins d’accès composés de documents qui sont des doublons exactes (courrier électronique: basé sur le contenu, les documents: basé sur le hachage). |
| Autres dépositaires | DedupedCustodians | Deduped_custodians | Autres dépositaires | Liste des dépositaires de documents qui sont des doublons exactes (pour la messagerie électronique: basée sur le contenu; pour les documents: basé sur le hachage). |
| Autres ID de fichier | DedupedFileIds | Deduped_file_IDs | Autres ID de fichier | Liste des ID de fichier des documents qui sont des doublons exactes (pour la messagerie électronique: basé sur le contenu; pour les documents: basé sur le hachage). |
| Commentaires de document | DocComments | Doc_comments | Commentaires de document | Commentaires des métadonnées du document. |
| Société de document |  | Doc_company | Société de document | Société à partir des métadonnées du document. |
| DocIndex |  |  |  | Index de la famille. -1 ou 0 signifie qu’il s’agit de la racine. |
| Mots clés de document |  | Doc_keywords | Mots clés de document | Mots clés des métadonnées du document. |
| Document modifié par |  | Doc_modified_by | Document modifié par | Date de dernière modification à partir des métadonnées de document. |
| Révision de document |  | Doc_revision | Révision de document | Révision des métadonnées du document. |
| Objet du document |  | Doc_subject | Objet du document | Objet des métadonnées du document. |
| Modèle de document |  | Doc_template | Modèle de document | Modèle à partir des métadonnées du document. |
| Thème dominant | DominantTheme | Dominant_theme | Thème dominant | Thème dominant calculé pour l’analyse. |
| Sous-ensemble dupliqué |  | Duplicate_subset | Sous-ensemble dupliqué | ID de groupe pour les doublons exacts. |
| EmailAction |  | Email_action |  | Aucun, répondre, transférer en fonction de la ligne d’objet d’un message. |
| Accusé de réception de courrier électronique |  | Email_delivery_receipt | Accusé de réception de courrier électronique | Adresse e-mail fournie dans les en-têtes Internet pour accusé de réception. |
| Importance | EmailImportance | Email_importance | Importance | Importance du message: **0**: faible; **1**: normal; **2**: haute |
| EmailLevel |  | Email_level |  | Indique le niveau d’un message dans le thread de messagerie auquel il appartient; les pièces jointes héritent la valeur de leur message parent. |
| ID du message électronique |  | Email_message_ID | ID du message électronique | ID de message Internet du message. |
| EmailReadReceipt |  | Email_read_receipt |  | Adresse de messagerie fournie dans les en-têtes Internet pour la confirmation de lecture. |
| Sécurité de messagerie | EmailSecurity | Email_security | Sécurité de messagerie | Paramètre de sécurité du message: **0**: aucun; **1**: signé; **2**: chiffrée; **3**: chiffré et signé. |
| Sensibilité du courrier électronique | EmailSensitivity | email_sensitivity | Sensibilité du courrier électronique | Paramètre de confidentialité du message: **0**: aucun; **1**: personnel; **2**: privé; **3**: CompanyConfidential. |
| Message électronique | EmailSet | Email_set | Message électronique | ID de groupe pour tous les messages dans le même groupe de courriers. |
| EmailThread |  | Email_thread |  | Position du message dans le jeu de courriers électroniques; se compose de tous les ID de nœud de la racine vers le message actuel, séparés par un point. |
| Type de contenu extrait |  | Extracted_content_type | Type de contenu extrait | Type de contenu extrait sous la forme d’un type MIME; par exemple, image/JPEG. |
| ExtractedTextLength |  | Extracted_text_length |  | Nombre de caractères dans le texte extrait. |
| Problème de pertinence de la situation familiale 1 |  | Family_relevance_score_case_issue_1 |  | Pertinence du scénario de pertinence de la famille 1 par rapport à la pertinence. |
| FamilyDuplicateSet |  | Family_duplicate_set |  | Identificateur numérique des familles qui sont des doublons exactes des uns des autres (même contenu et de toutes les mêmes pièces jointes). |
| ID de famille | FamilyId | Family_ID | ID de famille | ID de famille groupe tous les éléments; pour le courrier électronique, cela inclut le message et toutes les pièces jointes; pour les documents, cela inclut le document et tous les éléments incorporés. |
| Taille de la famille |  | Family_size | Taille de la famille | Nombre de documents dans la famille. |
| Problème 1 du score de cas de pertinence des fichiers |  | File_relevance_score_case_issue_1 |  | Pertinence du fichier cas du problème 1 par rapport à la pertinence. |
| Classe file | FileClass | File_class | Classe file | Pour le contenu provenant de SharePoint et OneDrive: **document**; pour le contenu à partir d’Exchange: **e-mail**ou **pièce jointe**. |
| ID de fichier | FileId | File_ID | ID de fichier | Identificateur de document unique dans le cas.|
| Date du système de fichiers créée |  | File_system_date_created | Date du système de fichiers créée | Date de création à partir du système de fichiers (s’applique uniquement aux données non Office 365). |
| Date du système de fichiers modifiée |  | File_system_date_modified | Date du système de fichiers modifiée | Date de modification à partir du système de fichiers (s’applique uniquement aux données non Office 365). |
| Type de fichier | FileType |  | Type de fichier | Type de fichier de l’élément, en fonction de l’extension de fichier. |
| Avec pièce jointe | HasAttachment | Email_has_attachment | Avec pièce jointe | Indique si le message contient des pièces jointes. |
| A un avocat | HasAttorney |  | A un avocat | True lorsqu’au moins un des participants figure dans la liste des avocats; Sinon, la valeur est false. |
| HasText |  | Has_text |  | Indique si l’élément contient du texte, si les valeurs possibles sont true et false. |
| ID non modifiable | ImmutableId | Immutable_ID | ID non modifiable | ID non modifiable tel qu’il est stocké dans Office 365. |
| Type inclusif | InclusiveType | Inclusive_type | Type inclusif | Type inclusif calculé pour l’analyse: **0** -non inclus; **1** -inclus; **2** -inclus moins; copie **3** -inclusive. |
| En réponse à l’ID |  | In_reply_to_ID | En réponse à l’ID | En réponse à l’ID du message. |
| Est représentatif | IsRepresentative | Is_representative | Est représentatif | Un document dans chaque ensemble de doublons exact est marqué comme représentatif. |
| Classe de l’élément | ItemClass | Item_class | Classe de l’élément | Classe d’élément fournie par Exchange Server; par exemple **IPM. Note** |
| Dernière modification | LastModifiedDate | Doc_date_modified | Dernière modification | Date de dernière modification à partir des métadonnées de document. |
| ID de chargement | LoadId | Load_ID | ID de chargement | Load ID, dans lequel l’élément a été chargé dans un jeu de révision. |
| Emplacement | Emplacement | Emplacement | Emplacement | Chaîne qui indique le type d’emplacement à partir duquel les documents ont été issus;<br />Données importées non-O365-><br />Teams-équipes ><br />EXO-> Exchange<br />SPO-> SharePoint<br />Onedrive entreprise-> OneDrive |
| Nom de l’emplacement | LocationName | Location_name | Nom de l’emplacement | Chaîne qui identifie la source de l’élément.  Pour Exchange, il s’agit de l’adresse SMTP de la boîte aux lettres.  Pour SharePoint et OneDrive, l’URL de la collection de sites. |
| Marqué comme représentant | MarkAsRepresentative |  | Marqué comme représentant | Un document de chaque ensemble de doublons exact est marqué comme représentant. |
| Marqué comme problème pré-balisé 1 |  | Marked_as_pre_tagged_Case_issue_1 |  | Marqué comme prébalisage du problème 1 de la pertinence. |
| Marqué comme émission d’un problème 1 |  | Marked_as_seed_Case_issue_1 |  | Marqué comme générateur de cas de générateur 1 de pertinence. |
| Date de fin de la réunion | MeetingEndDate | Meeting_end_date | Date de fin de la réunion | Date de fin de la réunion pour les réunions. |
| Date de début de la réunion | MeetingStartDate | Meeting_start_date | Date de début de la réunion | Date de début de réunion pour les réunions. |
| Type de message | MessageKind | Message_kind | Type de message | Type de message à rechercher.<br />Valeurs possibles : <br />contacts <br />docs <br />email <br />externaldata <br />faxes <br />im <br />journals <br />meetings <br />microsoftteams (renvoie les éléments des conversations, réunions et appels dans Microsoft Teams) <br />notes <br />posts <br />rssfeeds <br />tasks <br />voicemail |
| Extension Native | NativeExtension | Native_extension | Extension Native | Extension native de l’élément. |
| Nom de fichier natif | NativeFileName | Native_file_name | Nom de fichier natif | Nom de fichier natif de l’élément. |
| NativeMD5 |  | Native_MD5 |  | Hachage MD5 du flux de fichier. |
| ND/ET tri: exclusion des pièces jointes | NdEtSortExclAttach | ND_ET_sort_excl_attach | ND/ET tri: exclusion des pièces jointes | Concaténation du jeu de messages électroniques et de la définition de l’adresse de messagerie pour un tri efficace lors de la révision; D est ajouté en tant que préfixe aux ensembles ND et E est ajouté aux ensembles de messages électroniques. |
| Tri ND/ET: pièces jointes incluses | NdEtSortInclAttach | ND_ET_sort_incl_attach | Tri ND/ET: pièces jointes incluses | Concaténation du jeu de messages électroniques et de la définition de l’adresse de messagerie pour un tri efficace lors de la révision; D est ajouté en tant que préfixe aux ensembles ND et E est ajouté aux ensembles de messages électroniques. Chaque e-mail dans un ensemble de courriers est suivi des pièces jointes appropriées. |
| Problème 1 de cas de score de pertinence normalisé |  | Normalized_relevance_score_case_issue_1 |  | Note de pertinence normalisée problème 1 par rapport à la pertinence. |
| Auteurs O365 |  | O365_authors | Auteurs O365 | Auteur à partir de SharePoint. |
| O365 créé par |  | O365_created_by | O365 créé par | Créé par à partir de SharePoint. |
| Date de création d’O365 |  | O365_date_created | Date de création d’O365 | Date de création à partir de SharePoint. |
| Date d’Office 365 modifiée |  | O365_date_modified | Date d’Office 365 modifiée | Date de dernière modification à partir de SharePoint. |
| O365 modifié par |  | O365_modified_by | O365 modifié par | Modifié par à partir de SharePoint. |
| ID parent | ParentId | Parent_ID | ID parent | ID du parent de l’élément. |
| ParentNode |  | Parent_node |  | Message électronique le plus proche dans le fil de discussion. |
| Chemin d’accès parent | ParentPath | Parent_path | Chemin d’accès parent | Chemin d’accès composé du parent direct de l’élément. |
| Domaines des participants | ParticipantDomains | Email_participant_domains | Domaines des participants | Liste de tous les domaines des participants d’un message. |
| Participants | Participants | Email_participants | Participants | Liste de tous les participants d’un message; par exemple, expéditeur, à, CC, CCI. |
| ID de tableau croisé dynamique | PivotId | Pivot_ID | ID de tableau croisé dynamique | ID d’un tableau croisé dynamique. |
| Potentiellement privilégié | PotentiallyPrivileged | Potentially_privileged | Potentiellement privilégié | True si le modèle de détection des privilèges du client estime que le document est potentiellement privilégié |
| État de traitement | ProcessingStatus | Code_erreur | État de traitement | État de traitement après l’ajout de l’élément à un jeu de révision. |
| Problème de lecture du cas pour le pourcentage 1 |  | Read_percent_Case_issue_1 |  | Lire le problème de cas de pourcentage 1 par rapport à la pertinence. |
| Centile en lecture | ReadPercentile |  | Centile en lecture | En lecture de centile pour le document en fonction de la pertinence. |
| Nombre de destinataires |  | Recipient_count | Nombre de destinataires | Nombre de destinataires dans le message. |
| Domaines de destinataires | RecipientDomains | Email_recipient_domains | Domaines de destinataires | Liste de tous les domaines de destinataires d’un message. |
| Destinataires | Destinataires | Email_recipients | Destinataires | Liste de tous les destinataires d’un message (à, CC, CCI). |
| Problème de cas de groupe de chargement de pertinence 1 |  | Relevance_load_group_case_issue_1 |  | Cas de groupe de chargement de pertinence 1 de pertinence. |
| Description du cas du problème 1 du statut de pertinence |  | Relevance_status_description_Case_issue_1 |  | État de pertinence Description du cas problème 1 par rapport à la pertinence. |
| Problème lié à la balise de pertinence 1 |  | Relevance_tag_case_issue_1 |  | Balise de pertinence problème 1 par rapport à la pertinence. |
| Commentaire de pertinence |  | Relevance_comment | Commentaire de pertinence | Champ de commentaire à partir de la pertinence. |
| Score de pertinence | RelevanceScore |  | Score de pertinence | Score de pertinence d’un document basé sur la pertinence. |
| Balise de pertinence | RelevanceTag |  | Balise de pertinence | Score de pertinence d’un document basé sur la pertinence. |
| ID représentatif | RepresentativeId |  | ID représentatif | Identificateur numérique de chaque ensemble de doublons exacts. |
| Expéditeur | Expéditeur | Email_sender | Expéditeur | Champ sender (from) pour les types de message.  Le format **est \<DisplayName SmtpAddress>**. |
| Expéditeur/auteur | SenderAuthor |  | Expéditeur/auteur | Champ calculé composé de l’expéditeur ou de l’auteur de l’élément. |
| Domaine de l’expéditeur | SenderDomain | Email_sender_domain | Domaine de l’expéditeur | Domaine de l’expéditeur. |
| Sent | Sent | Email_date_sent | Sent | Date d’envoi du message. |
| Ordre défini: en premier | SetOrderInclusivesFirst | Set_order_inclusives_first | Définir l’ordre: inclus en premier. | Champ de tri-courrier électronique et pièces jointes: Counter-chronologique, documents: tableau croisé dynamique d’abord, puis par score de similarité, décroissant. |
| SimilarityPercent |  | Similarity_percent |  | Indique le degré de similarité d’un document par tableau croisé dynamique du jeu presque dupliqué. |
| Taille de fichier Native | Taille | Native_size | Taille de fichier Native | Nombre d’octets de l’élément natif. |
| Subject | Subject | Email_subject | Subject | Objet du message. |
| Subject/title | SubjectTitle |  | Subject/title | Champ calculé constitué de l’objet ou du titre de l’élément. |
| Marqué par le problème 1 |  | Tagged_by_Case_issue_1 |  | Utilisateur qui a balisé ce document pour le problème 1 en pertinence. |
| Tags | Tags | Tags | Tags | Balises appliquées dans un jeu de révision. |
| Liste des thèmes | ThemesList | Themes_list | Liste des thèmes | Liste des thèmes telle qu’elle est calculée pour l’analyse. |
| Titre | Titre | Doc_title | Titre | Titre des métadonnées du document. |
| À | À | Email_to | À | Champ à pour pour les types de message.  Le format **est\<DisplayName SmtpAddress>** |
| Unique dans le groupe de courriers | UniqueInEmailSet |  | Unique dans le groupe de courriers | False s’il existe un doublon de la pièce jointe dans son jeu de courriers. |
| A été résolu | WasRemediated | Was_Remediated | A été résolu | True si l’élément a été résolu, sinon false. |
| Statistiques | WordCount | Word_count | Statistiques | Nombre de mots dans l’élément. |
||||||

  > [!NOTE]
  > Pour plus d’informations sur les champs pouvant faire l’objet d’une recherche lorsque vous recherchez directement sur Office 365, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](https://docs.microsoft.com/en-us/office365/securitycompliance/keyword-queries-and-search-conditions)