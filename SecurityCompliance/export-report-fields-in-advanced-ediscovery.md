---
title: Exporter des champs de rapport dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 840a5aff-ecd0-4e56-ad22-fe99bc143687
description: Décrit tous les champs inclus dans les rapports d’exportation pour Advanced eDiscovery.
ms.openlocfilehash: 3e73cc1c106dfa98bd35f84c352fc89d0e45b74d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154468"
---
# <a name="export-report-fields-in-office-365-advanced-ediscovery"></a>Exporter des champs de rapport dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette rubrique décrit les champs de rapport d’exportation eDiscovery avancés pour les modèles standard et tous.
  
## <a name="export-report-fields"></a>Exportation des champs d’un rapport

Le tableau suivant répertorie les champs de chaque modèle d’exportation.
  
|**Exporter le nom du champ**|**Group**|**Description**|**Disponible dans le modèle standard**|**Disponible dans tous les modèles**|
|:-----|:-----|:-----|:-----|:-----|
|Row_number  <br/> |Général  <br/> |Numéro de ligne.  <br/> |Oui  <br/> |Oui  <br/> |
|File_ID  <br/> |Général  <br/> |ID de fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|File_class  <br/> |Traitement  <br/> |Classe de fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Family_ID  <br/> |Traitement  <br/> |Identificateur numérique utilisé pour regrouper les fichiers (en règle générale, l’instance de messagerie et ses pièces jointes).  <br/> |Oui  <br/> |Oui  <br/> |
|For_review  <br/> |Traitement  <br/> |Indicateur pour indiquer que le champ sera inclus dans Export pour révision.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_file_name  <br/> |Traitement  <br/> |Nom de fichier natif, sans référencement du dossier et de l’extension.  <br/> |Oui  <br/> |Oui  <br/> |
|Des dépositaires  <br/> |Général  <br/> |Dépositaire du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Set_ID  <br/> |Analyse  <br/> |ID «ND set» ou «jeu de courrier électronique».  <br/> |Oui  <br/> |Oui  <br/> |
|Inclusive_type  <br/> |E-mail  <br/> |Indique si le fichier est inclus, en fonction des valeurs suivantes: 0-non inclus, 1-inclusive, 2-inclusive moins, 3-inclusive.  <br/> |Oui  <br/> |Oui  <br/> |
|Marked_as_pivot  <br/> |Quasi-doublons  <br/> |Indique si le fichier est un tableau croisé dynamique.  <br/> |Oui  <br/> |Oui  <br/> |
|Similarity_percent  <br/> |Quasi-doublons  <br/> |Pourcentage de similarité par rapport au tableau croisé dynamique.  <br/> |Oui  <br/> |Oui  <br/> |
|Duplicate_subset  <br/> |Quasi-doublons  <br/> |Identificateur unique du sous-ensemble en double. Indique si le fichier contient des doublons de texte exactes.  <br/> |Oui  <br/> |Oui  <br/> |
|Date  <br/> |Général  <br/> |Date du fichier (en fonction du type de fichier: adresse de messagerie: date d’envoi; document: date de modification).  <br/> |Oui  <br/> |Oui  <br/> |
|Dominant_theme  <br/> |Analyse  <br/> |Thème principal du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Themes_list  <br/> |Thèmes  <br/> |Liste des noms de thèmes.  <br/> |Oui  <br/> |Oui  <br/> |
|ND_set  <br/> |EquiSet  <br/> |Identificateur numérique unique d’un jeu Nearduplicate.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_set  <br/> |E-mail  <br/> |Identificateur numérique unique d’un ensemble de courriers électroniques.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_thread  <br/> |E-mail  <br/> |Décrit la position du courrier électronique dans le jeu de courrier électronique composé de tous les ID de nœud de la racine vers l’e-mail actuel, séparés par des points.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_subject  <br/> |E-mail  <br/> |Objet du message électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_date_sent  <br/> |E-mail  <br/> |Date à laquelle le courrier électronique a été envoyé.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_participants  <br/> |E-mail  <br/> |Adresses de messagerie de tous les participants d’un thread de messagerie, y compris pour les liens manquants.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_participant_domains  <br/> |E-mail  <br/> |Domaines de tous les participants d’une thread de messagerie, y compris pour les liens manquants.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_sender  <br/> |E-mail  <br/> |Nom et/ou adresse de l’expéditeur de courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_sender_domain  <br/> |E-mail  <br/> |Domaine de l’expéditeur de courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_to  <br/> |E-mail  <br/> |Destinataire du courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_cc  <br/> |E-mail  <br/> |Destinataire CC du courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_bcc  <br/> |E-mail  <br/> |Destinataire CCI du courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_recipient_domains  <br/> |E-mail  <br/> |Les domaines de destinataires de messagerie (à, CC et CCI).  <br/> |Oui  <br/> |Oui  <br/> |
|Email_date_received  <br/> |E-mail  <br/> |Date à laquelle le courrier électronique a été reçu.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_action  <br/> |E-mail  <br/> |Valeurs: en fonction de l’objet de l’E-mail: "Forward" (pour "tr:"), "reply" (pour "RE:") ou "Other" (autre objet).  <br/> |Oui  <br/> |Oui  <br/> |
|Meeting_Start_Date/heure  <br/> ||Date et heure de début d’un élément de réunion.  <br/> |Oui  <br/> |Oui  <br/> |
|Meeting_End_Date/heure  <br/> ||Date et heure de fin d’un élément de réunion.  <br/> |Oui  <br/> |Oui  <br/> |
|File_relevance_score  <br/> |Importance  <br/> |Score de pertinence (0-100). Par problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Family_relevance_score  <br/> |Importance  <br/> |Score max de pertinence de la famille (0-100). Par problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Relevance_tag  <br/> |Importance  <br/> |Balisage du fichier, si le fichier a été marqué manuellement en pertinence. Par problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Relevance_load_group  <br/> |Importance  <br/> |Groupe de chargement de pertinence, du fichier spécifié, avec un champ par problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Normalized_relevance_score  <br/> |Importance  <br/> |Note de pertinence normalisée (0-100), comparable entre les problèmes et les charges.  <br/> |Oui  <br/> |Oui  <br/> |
|Marked_as_seed  <br/> |Importance  <br/> |Balisage du fichier, s’il a été défini en tant que fichier Seed en fonction de la pertinence par problème/catégorie.  <br/> |Oui  <br/> |Oui  <br/> |
|Balises Marked_as_pre  <br/> |Importance  <br/> |Balisage du fichier, s’il a été défini comme étant prédéfini en fonction de la pertinence par problème/catégorie.  <br/> |Oui  <br/> |Oui  <br/> |
|Relevance_status_description  <br/> |Importance  <br/> |Description de l’état de pertinence.  <br/> |Oui  <br/> |Oui  <br/> |
|Commentaire  <br/> |Général  <br/> |Commentaire entré par l’utilisateur.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_input_path  <br/> |Traitement  <br/> |Exporter le chemin d’accès d’entrée.  <br/> |Oui  <br/> |Oui  <br/> |
|Pivot_ID  <br/> |Quasi-doublons  <br/> |ID de tableau croisé dynamique du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Family_size  <br/> |Traitement  <br/> |Nombre de fichiers dans une famille.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_type  <br/> |Traitement  <br/> |Type de fichier natif. Par exemple, feuille de calcul ou présentation.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_MD5  <br/> |Traitement  <br/> |Valeur de hachage MD5 du fichier natif.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_size  <br/> |Traitement  <br/> |Taille de fichier native.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_extension  <br/> |Traitement  <br/> |Extension de fichier native.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_date_modified  <br/> |Propriétés du document  <br/> |Date à laquelle le fichier natif a été modifié, extrait des métadonnées du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_date_created  <br/> |Propriétés du document  <br/> |Date de création du fichier natif, extraite des métadonnées du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_modified_by  <br/> |Propriétés du document  <br/> |Utilisateur qui a modifié le fichier natif, pris à partir des métadonnées du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|O365_date_modified  <br/> |Propriétés du document  <br/> |Date à laquelle le fichier natif a été modifié, extrait des champs SharePoint ou Exchange.  <br/> |Oui  <br/> |Oui  <br/> |
|O365_date_created  <br/> |Propriétés du document  <br/> |Date de création du fichier natif, extraite de champs SharePoint ou Exchange.  <br/> |Oui  <br/> |Oui  <br/> |
|O365_modified_by  <br/> |Propriétés du document  <br/> |Utilisateur qui a modifié le fichier natif pour la dernière fois, issu de champs SharePoint ou Exchange.  <br/> |Oui  <br/> |Oui  <br/> |
|Compound_path  <br/> |Traitement  <br/> |Chemin d’accès natif incluant sa source composée.  <br/> |Oui  <br/> |Oui  <br/> |
|Input_path  <br/> |Traitement  <br/> |Chemin d’accès du fichier d’entrée.  <br/> |Oui  <br/> |Oui  <br/> |
|Input_date_modified  <br/> |Traitement  <br/> |Date de la dernière modification du fichier d’entrée.  <br/> |Oui  <br/> |Oui  <br/> |
|ND_ET_sort_excl_attach  <br/> |Analyse  <br/> |Concaténation de l’ensemble de messages électroniques et de la définition de la valeur. 'D’est ajouté en tant que préfixe aux ensembles ND, et’E’est ajouté à l’adresse de messagerie ssets.  <br/> |Oui  <br/> |Oui  <br/> |
|ND_ET_sort_incl_attach  <br/> |Analyse  <br/> |La concaténation du jeu de messages et de la sauvegarde de l’ensemble de messages pour révision d est ajoutée en tant que préfixe aux ensembles ND, et «E» est ajouté aux groupes de courriers. Par ailleurs, chaque message électronique dans un Email_set est suivi des pièces jointes appropriées.  <br/> |Oui  <br/> |Oui  <br/> |
|Deduped_custodians  <br/> |Général  <br/> |Dépositaires de fichiers de duped  <br/> |Oui  <br/> |Oui  <br/> |
|Deduped_file_IDs  <br/> |Général  <br/> |ID de fichiers de duped  <br/> |Oui  <br/> |Oui  <br/> |
|Deduped_paths  <br/> |Général  <br/> |Chemins d’accès aux fichiers de duped  <br/> |Oui  <br/> |Oui  <br/> |
|File_key  <br/> |Général  <br/> |Identificateur interne pour une utilisation ultérieure.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_native_path  <br/> |Traitement  <br/> |Chemin d’accès du fichier natif dans le package d’exportation.  <br/> |Oui  <br/> |Oui  <br/> |
|Extracted_text_path  <br/> |Traitement  <br/> |Chemin d’accès du fichier extrait.  <br/> |Oui  <br/> |Oui  <br/> |
|Process_batch  <br/> |Traitement  <br/> |Identificateur de lot pour le lot d’importation.  <br/> |Oui  <br/> |Oui  <br/> |
|Process_status_ID  <br/> |Traitement  <br/> |Identificateur représentant l’état de l’étape de processus.  <br/> |Oui  <br/> |Oui  <br/> |
|Process_status_description  <br/> |Traitement  <br/> |Description de l’état du processus: description réussie ou erreur.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_status_ID  <br/> |Traitement  <br/> |ID de l’état de l’exportation.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_status_description  <br/> |Traitement  <br/> |Description de l’état d’exportation; Description de l’erreur ou de la réussite.  <br/> |Oui  <br/> |Oui  <br/> |
|Read_percent  <br/> |Importance  <br/> |Lire% (0-100). Par problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_author  <br/> |Propriétés du document  <br/> |Propriétés du document: auteur.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_comments  <br/> |Propriétés du document  <br/> |Propriétés du document: commentaires.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_keywords  <br/> |Propriétés du document  <br/> |Propriétés du document: Mots clés.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_last_saved_by  <br/> |Propriétés du document  <br/> |Propriétés du document: dernière sauvegarde par.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_revision  <br/> |Propriétés du document  <br/> |Propriétés du document: numéro de révision.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_subject  <br/> |Propriétés du document  <br/> |Propriétés du document: objet.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_template  <br/> |Propriétés du document  <br/> |Propriétés du document: modèle.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_title  <br/> |Propriétés du document  <br/> |Propriétés du document: titre.  <br/> |Non  <br/> |Oui  <br/> |
|Email_has_attachment  <br/> |E-mail  <br/> |Indique si l’e-mail comporte une ou plusieurs pièces jointes.  <br/> |Non  <br/> |Oui  <br/> |
|Email_importance  <br/> |E-mail  <br/> |Propriété d’importance de messagerie.  <br/> |Non  <br/> |Oui  <br/> |
|Email_level  <br/> |E-mail  <br/> |Indique le niveau de messagerie au sein du thread de messagerie. Pour les pièces jointes, la valeur de l’e-mail joint.  <br/> |Non  <br/> |Oui  <br/> |
|Email_recipients  <br/> |E-mail  <br/> |Destinataires de messagerie nom et/ou adresses (à, CC et CCI).  <br/> |Non  <br/> |Oui  <br/> |
|Email_security  <br/> |E-mail  <br/> |Propriété de sécurité de messagerie.  <br/> |Non  <br/> |Oui  <br/> |
|Email_sensitivity  <br/> |E-mail  <br/> |Propriété de sensibilité du courrier électronique.  <br/> |Non  <br/> |Oui  <br/> |
|Export_batch  <br/> |Traitement  <br/> |Nom de lot de la dernière exportation du fichier.  <br/> |Non  <br/> |Oui  <br/> |
|Export_session  <br/> |Traitement  <br/> |ID de session de la dernière exportation du fichier, y compris la date.  <br/> |Non  <br/> |Oui  <br/> |
|Extracted_text_length  <br/> |Traitement  <br/> |Longueur de caractère du fichier texte extrait.  <br/> |Non  <br/> |Oui  <br/> |
|Family_duplicate_set  <br/> |Traitement  <br/> |Identificateur numérique des familles qui sont des doublons de texte exacts les uns des autres (respectivement-tous les membres des familles sont des doublons exacts).  <br/> |Non  <br/> |Oui  <br/> |
|Has_Text  <br/> |Traitement  <br/> |Indique s’il existe un texte dans le fichier: 0-non; 1-Oui.  <br/> |Non  <br/> |Oui  <br/> |
|Input_file_ID  <br/> |Traitement  <br/> |ID du fichier d’entrée à partir duquel le fichier a été extrait.  <br/> |Non  <br/> |Oui  <br/> |
|Native_SHA_256  <br/> |Traitement  <br/> |Valeur de hachage SHA-256 du fichier natif.  <br/> |Non  <br/> |Oui  <br/> |
|O365_authors  <br/> |Propriétés du document  <br/> |Utilisateurs ayant modifié le fichier natif, extraits de champs SharePoint ou Exchange.  <br/> |Non  <br/> |Oui  <br/> |
|O365_created_by  <br/> |Propriétés du document  <br/> |Utilisateur qui a créé le fichier natif, issu de champs SharePoint ou Exchange.  <br/> |Non  <br/> |Oui  <br/> |
|Parent_node  <br/> |E-mail  <br/> |Associe un nœud dans un thread de messagerie au nœud parent le plus proche qui n’est pas un lien manquant.  <br/> |Non  <br/> |Oui  <br/> |
|Set_order_inclusives_first  <br/> |E-mail  <br/> |E-mails et pièces jointes: compteurs chronologiques (inclus en premier). Documents: les tableaux croisés dynamiques et le reste par score de similarité, décroissant.  <br/> |Non  <br/> |Oui  <br/> |
|Tagged_By  <br/> |Importance  <br/> |Utilisateur qui a balisé le fichier en pertinence pour le problème spécifique.  <br/> |Non  <br/> |Oui  <br/> |
|Word_count  <br/> |Analyse  <br/> |Nombre de mots dans le document.  <br/> |Non  <br/> |Oui  <br/> |
|||||||||||
||||||
||||||
   
## <a name="related-topics"></a>Rubriques connexes

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Exportation de données de cas avec eDiscovery avancé](export-case-data-in-advanced-ediscovery.md)
  
[Exportation des résultats](export-results-in-advanced-ediscovery.md)
  
[Affichage de l’historique du lot et exportation des résultats passés](view-batch-history-and-export-past-results.md)
  

