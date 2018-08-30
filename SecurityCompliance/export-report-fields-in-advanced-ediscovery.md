---
title: Champs d’exportation des rapports dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 840a5aff-ecd0-4e56-ad22-fe99bc143687
description: Décrit tous les champs qui sont inclus dans les rapports d’exportation pour la découverte avancée.
ms.openlocfilehash: a578523098248bcfa16ea8ba97d756d97ba060fa
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527789"
---
# <a name="export-report-fields-in-office-365-advanced-ediscovery"></a>Champs d’exportation des rapports dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette rubrique décrit les champs du rapport exportation eDiscovery avancée pour la norme et de tous les modèles.
  
## <a name="export-report-fields"></a>Champs du rapport d’exportation

Le tableau suivant répertorie les champs de chaque modèle de l’exportation.
  
|**Nom de champ d’exportation**|**Groupe**|**Description**|**Disponible dans le modèle Standard**|**Disponible dans tous les modèles**|
|:-----|:-----|:-----|:-----|:-----|
|Row_number  <br/> |Général  <br/> |Numéro de ligne.  <br/> |Oui  <br/> |Oui  <br/> |
|File_ID  <br/> |Général  <br/> |ID du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|File_class  <br/> |Traitement  <br/> |Fichier de classe.  <br/> |Oui  <br/> |Oui  <br/> |
|Family_ID  <br/> |Traitement  <br/> |Identificateur numérique qui est utilisée pour regrouper les fichiers (généralement instance de courrier électronique et ses pièces jointes).  <br/> |Oui  <br/> |Oui  <br/> |
|For_review  <br/> |Traitement  <br/> |Indicateur pour indiquer que le champ va être inclus dans l’exportation pour passer en revue les.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_file_name  <br/> |Traitement  <br/> |Nom de fichier natif, sans référencer le dossier et l’extension.  <br/> |Oui  <br/> |Oui  <br/> |
|Dépositaires  <br/> |Général  <br/> |Dépositaire du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Set_ID  <br/> |Analyse  <br/> |« Définie ND » ou id « Set de messagerie ».  <br/> |Oui  <br/> |Oui  <br/> |
|Inclusive_type  <br/> |Courrier électronique  <br/> |Indique si le fichier est inclus, en fonction des valeurs suivantes : 0 - pas inclus, 1 - 2 inclus - inclus moins 3 - copie (inclus).  <br/> |Oui  <br/> |Oui  <br/> |
|Marked_as_pivot  <br/> |NEAR doublons  <br/> |Indique si le fichier est un tableau croisé dynamique.  <br/> |Oui  <br/> |Oui  <br/> |
|Similarity_percent  <br/> |NEAR doublons  <br/> |Pourcentage de similarité par rapport de tableau croisé dynamique.  <br/> |Oui  <br/> |Oui  <br/> |
|Duplicate_subset  <br/> |NEAR doublons  <br/> |Identificateur unique du sous-ensemble en double. Indique si le fichier comporte des doublons texte exact.  <br/> |Oui  <br/> |Oui  <br/> |
|Date  <br/> |Général  <br/> |Date de fichier (varie selon le type de fichier - courrier : date d’envoi ; document : date de modification).  <br/> |Oui  <br/> |Oui  <br/> |
|Dominant_theme  <br/> |Analyse  <br/> |Thème principal du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Themes_list  <br/> |Thèmes  <br/> |Liste des noms de thèmes.  <br/> |Oui  <br/> |Oui  <br/> |
|ND_set  <br/> |EquiSet  <br/> |Identificateur numérique unique d’un ensemble Nearduplicate.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_set  <br/> |Courrier électronique  <br/> |Identificateur numérique unique d’un jeu de courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_thread  <br/> |Courrier électronique  <br/> |Décrit la position du courrier électronique dans le courrier électronique valeur assure tous les ID de nœud à partir de la racine du message électronique actuel, séparés par des virgules.  <br/> |Oui  <br/> |Oui  <br/> |
|Objet_message_électronique  <br/> |Courrier électronique  <br/> |Sujet du courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_date_sent  <br/> |Courrier électronique  <br/> |Date à laquelle le courrier électronique a été envoyé.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_participants  <br/> |Courrier électronique  <br/> |Adresses de messagerie de tous les participants dans un thread de messagerie, y compris les liens manquants.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_participant_domains  <br/> |Courrier électronique  <br/> |Domaines de tous les participants dans un thread de messagerie, y compris pour le lien manquant.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_sender  <br/> |Courrier électronique  <br/> |Nom de l’expéditeur de courrier électronique et/ou adresse.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_sender_domain  <br/> |Courrier électronique  <br/> |Domaine de l’expéditeur de messagerie.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_to  <br/> |Courrier électronique  <br/> |Destinataire du message électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_cc  <br/> |Courrier électronique  <br/> |Destinataire CC du message électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_bcc  <br/> |Courrier électronique  <br/> |Destinataire Cci du message électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_recipient_domains  <br/> |Courrier électronique  <br/> |Destinataires des messages domaines (à, CC et Cci).  <br/> |Oui  <br/> |Oui  <br/> |
|Email_date_received  <br/> |Courrier électronique  <br/> |Date de réception de courrier électronique.  <br/> |Oui  <br/> |Oui  <br/> |
|Email_action  <br/> |Courrier électronique  <br/> |Valeurs : En fonction de l’objet de message : « Transférer » (pour « TR : »), « Reply » (pour « RE : ») ou « Autres » (autre objet).  <br/> |Oui  <br/> |Oui  <br/> |
|Meeting_Start_Date/heure  <br/> ||La date et l’heure à laquelle un élément de réunion a démarré.  <br/> |Oui  <br/> |Oui  <br/> |
|Meeting_End_Date/heure  <br/> ||La date et l’heure à laquelle un élément de réunion s’est terminée.  <br/> |Oui  <br/> |Oui  <br/> |
|File_relevance_score  <br/> |Pertinence  <br/> |Score de pertinence (0-100). Par le problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Family_relevance_score  <br/> |Pertinence  <br/> |Famille max score de pertinence (0-100). Par le problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Relevance_tag  <br/> |Pertinence  <br/> |Marquage du fichier, si le fichier a été marqué manuellement dans la pertinence. Par le problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Relevance_load_group  <br/> |Pertinence  <br/> |Groupe de chargement de la pertinence du fichier spécifié, avec un champ par le problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Normalized_relevance_score  <br/> |Pertinence  <br/> |La pertinence normalisée score (0-100), qui est comparable entre les sorties et charges.  <br/> |Oui  <br/> |Oui  <br/> |
|Marked_as_seed  <br/> |Pertinence  <br/> |Marquage du fichier, si elle a été définie comme un fichier d’amorçage dans la pertinence par/catégorie du problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Marked_as_pre marqué  <br/> |Pertinence  <br/> |Marquage du fichier, si elle a été définie en tant que préalable avec balise dans la pertinence par/catégorie du problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Relevance_status_description  <br/> |Pertinence  <br/> |Description de l’état de la pertinence.  <br/> |Oui  <br/> |Oui  <br/> |
|Commentaires  <br/> |Général  <br/> |Commentaire entré par l’utilisateur.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_input_path  <br/> |Traitement  <br/> |Exporter le chemin d’accès d’entrée.  <br/> |Oui  <br/> |Oui  <br/> |
|Pivot_ID  <br/> |NEAR doublons  <br/> |ID de tableau croisé dynamique du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Family_size  <br/> |Traitement  <br/> |Nombre de fichiers dans un jeu de variantes.  <br/> |Oui  <br/> |Oui  <br/> |
|Type_natif  <br/> |Traitement  <br/> |Type de fichier natif. Par exemple, une feuille de calcul ou présentation.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_MD5  <br/> |Traitement  <br/> |Valeur de hachage MD5 du fichier natif.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_size  <br/> |Traitement  <br/> |Taille de fichier natif.  <br/> |Oui  <br/> |Oui  <br/> |
|Native_extension  <br/> |Traitement  <br/> |Extension de fichier natif.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_date_modified  <br/> |Propriétés de document  <br/> |Date de modification du fichier natif, proviennent des métadonnées du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_date_created  <br/> |Propriétés de document  <br/> |Date de fichier natif a été créé, tiré les métadonnées du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_modified_by  <br/> |Propriétés de document  <br/> |Utilisateur ayant modifié le fichier natif, proviennent des métadonnées du fichier.  <br/> |Oui  <br/> |Oui  <br/> |
|O365_date_modified  <br/> |Propriétés de document  <br/> |Date de fichier natif a été modifié, extraites de champs SharePoint ou Exchange.  <br/> |Oui  <br/> |Oui  <br/> |
|O365_date_created  <br/> |Propriétés de document  <br/> |Date de fichier natif a été créé, extraites de champs SharePoint ou Exchange.  <br/> |Oui  <br/> |Oui  <br/> |
|O365_modified_by  <br/> |Propriétés de document  <br/> |Dernier utilisateur ayant modifié le fichier natif, provenant de champs SharePoint ou Exchange.  <br/> |Oui  <br/> |Oui  <br/> |
|Compound_path  <br/> |Traitement  <br/> |Chemin d’accès de fichier natif, y compris sa source composé.  <br/> |Oui  <br/> |Oui  <br/> |
|Input_path  <br/> |Traitement  <br/> |Chemin d’accès du fichier d’entrée.  <br/> |Oui  <br/> |Oui  <br/> |
|Input_date_modified  <br/> |Traitement  <br/> |Dernière modification du fichier d’entrée de date.  <br/> |Oui  <br/> |Oui  <br/> |
|ND_ET_sort_excl_attach  <br/> |Analyse  <br/> |Affectez concaténation de courriers électroniques et ND pour révision. Avait » est ajouté, comme un préfixe pour les ensembles de ND et « E » est ajouté à la messagerie définit.  <br/> |Oui  <br/> |Oui  <br/> |
|ND_ET_sort_incl_attach  <br/> |Analyse  <br/> |Définie concaténation de courriers électroniques et serait ND pour passer en revue les » est ajouté, comme un préfixe pour les ensembles de ND et « E » est ajouté aux ensembles de courrier électronique. En outre, chaque e-mail au sein d’un Email_set est suivi par ses pièces jointes appropriés.  <br/> |Oui  <br/> |Oui  <br/> |
|Deduped_custodians  <br/> |Général  <br/> |Dépositaires des fichiers déduplication laissez duper  <br/> |Oui  <br/> |Oui  <br/> |
|Deduped_file_IDs  <br/> |Général  <br/> |ID de retrait laissez duper de fichiers  <br/> |Oui  <br/> |Oui  <br/> |
|Deduped_paths  <br/> |Général  <br/> |Chemins d’accès des fichiers d’annulation laissez duper  <br/> |Oui  <br/> |Oui  <br/> |
|File_key  <br/> |Général  <br/> |Identificateur interne pour une utilisation future.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_native_path  <br/> |Traitement  <br/> |Chemin d’accès du fichier natif dans le package d’exportation.  <br/> |Oui  <br/> |Oui  <br/> |
|Extracted_text_path  <br/> |Traitement  <br/> |Chemin d’accès du fichier extrait.  <br/> |Oui  <br/> |Oui  <br/> |
|Process_batch  <br/> |Traitement  <br/> |Identificateur de lot pour lot d’importation.  <br/> |Oui  <br/> |Oui  <br/> |
|Process_status_ID  <br/> |Traitement  <br/> |Identificateur représentant processus état de l’étape.  <br/> |Oui  <br/> |Oui  <br/> |
|Process_status_description  <br/> |Traitement  <br/> |Processus de description de l’état étape : réussite ou la description de l’erreur.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_status_ID  <br/> |Traitement  <br/> |ID de l’état d’exportation.  <br/> |Oui  <br/> |Oui  <br/> |
|Export_status_description  <br/> |Traitement  <br/> |Description de l’état de l’exportation ; réussite ou la description de l’erreur.  <br/> |Oui  <br/> |Oui  <br/> |
|Read_percent  <br/> |Pertinence  <br/> |% De lecture (0-100). Par le problème.  <br/> |Oui  <br/> |Oui  <br/> |
|Doc_author  <br/> |Propriétés de document  <br/> |Propriétés de document : auteur.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_comments  <br/> |Propriétés de document  <br/> |Propriétés de document : commentaires.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_keywords  <br/> |Propriétés de document  <br/> |Propriétés de document : mots clés.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_last_saved_by  <br/> |Propriétés de document  <br/> |Propriétés de document : dernier enregistré par.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_revision  <br/> |Propriétés de document  <br/> |Propriétés de document : numéro de révision.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_subject  <br/> |Propriétés de document  <br/> |Propriétés de document : objet.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_template  <br/> |Propriétés de document  <br/> |Propriétés de document : modèle.  <br/> |Non  <br/> |Oui  <br/> |
|Doc_title  <br/> |Propriétés de document  <br/> |Propriétés de document : titre.  <br/> |Non  <br/> |Oui  <br/> |
|Email_has_attachment  <br/> |Courrier électronique  <br/> |Indique si le message électronique a une ou plusieurs pièces jointes.  <br/> |Non  <br/> |Oui  <br/> |
|Email_importance  <br/> |Courrier électronique  <br/> |Propriété importance de messagerie.  <br/> |Non  <br/> |Oui  <br/> |
|Niveau_courrier_électronique  <br/> |Courrier électronique  <br/> |Indique le niveau de messagerie dans le thread de messagerie. Les pièces jointes, la valeur du courrier électronique associée.  <br/> |Non  <br/> |Oui  <br/> |
|Email_recipients  <br/> |Courrier électronique  <br/> |Destinataires de courrier électronique adresses (à, CC et Cci) ou nom.  <br/> |Non  <br/> |Oui  <br/> |
|Email_security  <br/> |Courrier électronique  <br/> |Propriété de sécurité du courrier électronique.  <br/> |Non  <br/> |Oui  <br/> |
|Email_sensitivity  <br/> |Courrier électronique  <br/> |Propriété sensitivity de messagerie.  <br/> |Non  <br/> |Oui  <br/> |
|Export_batch  <br/> |Traitement  <br/> |Nom de lot dernière exportation du fichier.  <br/> |Non  <br/> |Oui  <br/> |
|Export_session  <br/> |Traitement  <br/> |Dernière session d’exportation du fichier, y compris des Id de date.  <br/> |Non  <br/> |Oui  <br/> |
|Extracted_text_length  <br/> |Traitement  <br/> |Longueur de caractères du fichier texte extrait.  <br/> |Non  <br/> |Oui  <br/> |
|Family_duplicate_set  <br/> |Traitement  <br/> |Identificateur numérique pour les familles de doublons texte exact de l’autre (respectivement - tous les membres de la famille sont identiques).  <br/> |Non  <br/> |Oui  <br/> |
|Has_Text  <br/> |Traitement  <br/> |Indique s’il existe un texte dans le fichier : 0 - aucun ; 1 - Oui.  <br/> |Non  <br/> |Oui  <br/> |
|Input_file_ID  <br/> |Traitement  <br/> |ID du fichier d’entrée à partir de laquelle le fichier a été extrait à partir de.  <br/> |Non  <br/> |Oui  <br/> |
|Native_SHA_256  <br/> |Traitement  <br/> |Valeur de hachage SHA-256 du fichier natif.  <br/> |Non  <br/> |Oui  <br/> |
|O365_authors  <br/> |Propriétés de document  <br/> |Utilisateurs qui a modifié le fichier natif, provenant de champs SharePoint ou Exchange.  <br/> |Non  <br/> |Oui  <br/> |
|O365_created_by  <br/> |Propriétés de document  <br/> |Utilisateur qui a créé le fichier natif, provenant de champs SharePoint ou Exchange.  <br/> |Non  <br/> |Oui  <br/> |
|Parent_node  <br/> |Courrier électronique  <br/> |Se rapporte à un nœud dans un thread de messagerie vers le nœud parent le plus proche qui n’est pas un lien manquant.  <br/> |Non  <br/> |Oui  <br/> |
|Set_order_inclusives_first  <br/> |Courrier électronique  <br/> |Les messages électroniques et les pièces jointes : ordre chronologique de compteur (Inclusives premier). Documents : pivote premier et le reste par score de similarité, décroissant.  <br/> |Non  <br/> |Oui  <br/> |
|Tagged_By  <br/> |Pertinence  <br/> |Utilisateur qui a marqué le fichier de pertinence pour le problème spécifique.  <br/> |Non  <br/> |Oui  <br/> |
|Word_count  <br/> |Analyse  <br/> |Nombre de mots du document.  <br/> |Non  <br/> |Oui  <br/> |
|||||||||||
||||||
||||||
   
## <a name="related-topics"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Exportation des données du cas avec eDiscovery avancée](export-case-data-in-advanced-ediscovery.md)
  
[Exportation des résultats](export-results-in-advanced-ediscovery.md)
  
[Affichage de l’historique des commandes et l’exportation des résultats antérieurs](view-batch-history-and-export-past-results.md)
  

