---
title: Ce qu’incluent les modèles de stratégie DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.DLPNewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c2e588d3-8f4f-4937-a286-8c399f28953a
description: Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut les modèles de stratégie prêt à l’emploi des exigences de conformité courantes, telles que pour vous aider à protéger les informations sensibles soumis à la loi américaine sur Health Insurance ( HIPAA), États-Unis Gramm-Leach-Bliley Act (GLBA) ou US Patriot Act. Cette rubrique répertorie tous les de la stratégie de modèles, les types d’informations sensibles dont ils recherchent et quelles sont les conditions par défaut et les actions.
ms.openlocfilehash: 345738244b9573b1af4d55ede86a568bf136f048
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528265"
---
# <a name="what-the-dlp-policy-templates-include"></a>Ce qu’incluent les modèles de stratégie DLP

Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut les modèles de stratégie prêt à l’emploi des exigences de conformité courantes, telles que pour vous aider à protéger les informations sensibles soumis à la loi américaine sur Health Insurance ( HIPAA), États-Unis Gramm-Leach-Bliley Act (GLBA) ou US Patriot Act. Cette rubrique répertorie tous les de la stratégie de modèles, les types d’informations sensibles dont ils recherchent et quelles sont les conditions par défaut et les actions. Cette rubrique n’inclut pas tous les détails de la configuration de chaque modèle de stratégie ; au lieu de cela, la rubrique présente avec vous suffisamment d’informations pour vous aider à décider quel modèle est le meilleur point de départ pour votre scénario. N’oubliez pas, vous pouvez personnaliser ces modèles de stratégie pour répondre à vos besoins spécifiques.
  
## <a name="australia-financial-data"></a>Données financières en Australie

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour l’Australie : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de dossier fiscal australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour l’Australie : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de dossier fiscal australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="australia-health-records-act-hrip-act"></a>Australia Health Records Act (HRIP Act)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi HRIP australienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de dossier médical australien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi HRIP australienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de dossier médical australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="australia-personally-identifiable-information-pii-data"></a>Australia Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour l’Australie : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire australien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour l’Australie : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de permis de conduire australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="australia-privacy-act"></a>Australia Privacy Act

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Protection des données pour l’Australie : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport australien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Protection des données pour l’Australie : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-financial-data"></a>Données financières au Canada

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour le Canada : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour le Canada : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-health-information-act-hia"></a>Canada Health Information Act (HIA)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi HIA canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi HIA canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-health-act-phipa---ontario"></a>Canada Personal Health Act (PHIPA) - Ontario

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi LPRPS canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi LPRPS canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-health-information-act-phia---manitoba"></a>Canada Personal Health Information Act (PHIA) - Manitoba

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi LRMP canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi LRMP canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-information-protection-act-pipa"></a>Canada Personal Information Protection Act (PIPA)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi PIPA canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi PIPA canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-information-protection-act-pipeda"></a>Canada Personal Information Protection and Electronic Documents Act (PIPEDA)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi LPRPDE canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi LPRPDE canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personally-identifiable-information-pii-data"></a>Canada Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour le Canada : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour le Canada : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="france-data-protection-act"></a>Loi informatique et liberté en France

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi sur la protection des données pour la France : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi sur la protection des données pour la France : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="france-financial-data"></a>Données financières en France

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour la France : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour la France : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="france-personally-identifiable-information-pii-data"></a>France Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour la France : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire français — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport français — Nombre minimal 1, nombre maximal 9  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour la France : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de permis de conduire français — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport français — Nombre minimal 10, nombre maximal « tout »  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="general-data-protection-regulation-gdpr"></a>Protection de données général règlement (PIBR)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Volume faible contenu sensible à l’Union européenne  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire UE — nombre Min 1, le nombre maximal de 9  <br/>  National numéro d’Identification de l’UE : Nombre de Min 1, le nombre maximal de 9  <br/>  Numéro de passeport UE : Nombre Min 1, le nombre maximal de 9  <br/>  Numéro de sécurité sociale de l’Union européenne (NAS) ou ID équivalente — nombre Min 1, le nombre maximal de 9  <br/>  Nombre de Min UE Tax Identification nombre (numéro d’identification) : 1, le nombre maximal de 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer des rapports d’incident à l’administrateur  <br/> |
|Volume important de contenu de l’UE critiques trouvé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire UE — nombre Min 1, le nombre maximal de 9  <br/>  National numéro d’Identification de l’UE : Nombre de Min 1, le nombre maximal de 9  <br/>  Numéro de passeport UE : Nombre Min 1, le nombre maximal de 9  <br/>  Numéro de sécurité sociale de l’Union européenne (NAS) ou ID équivalente — nombre Min 1, le nombre maximal de 9  <br/>  Nombre de Min UE Tax Identification nombre (numéro d’identification) : 1, le nombre maximal de 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Restreindre l’accès au contenu pour les utilisateurs externes  <br/>  Avertir les utilisateurs avec conseils de messagerie et de la stratégie  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer des rapports d’incident à l’administrateur  <br/> |
   
## <a name="germany-financial-data"></a>Données financières en Allemagne

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour l’Allemagne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour l’Allemagne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="germany-personally-identifiable-information-pii-data"></a>Germany Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour l’Allemagne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire allemand — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport allemand — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour l’Allemagne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire allemand — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport allemand — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="israel-financial-data"></a>Données financières en Israël

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour Israël : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire israélien — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour Israël : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="israel-personally-identifiable-information-pii-data"></a>Israel Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour Israël : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour Israël : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="israel-protection-of-privacy"></a>Israel Protection of Privacy

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Protection des données pour Israël : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire israélien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Protection des données pour Israël : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="japan-financial-data"></a>Données financières au Japon

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour le Japon : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire japonais — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour le Japon : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire japonais — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="japan-personally-identifiable-information-pii-data"></a>Japan Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour le Japon : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour le Japon : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="japan-protection-of-personal-information"></a>Japan Protection of Personal Information

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi PPI pour le Japon : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi PPI pour le Japon : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="pci-data-security-standard-pci-dss"></a>PCI Data Security Standard (PCI DSS)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Norme PCI DSS : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Norme PCI DSS : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="saudi-arabia---anti-cyber-crime-law"></a>Saudi Arabia - Anti-Cyber Crime Law

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|ACC pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|ACC pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="saudi-arabia-financial-data"></a>Données financières en Arabie Saoudite

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="saudi-arabia-personally-identifiable-information-pii-data"></a>Saudi Arabia Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national saoudien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national saoudien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-access-to-medical-reports-act"></a>U.K. Access to Medical Reports Act

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi AMRA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi AMRA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-data-protection-act"></a>U.K. Data Protection Act

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|DPA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|DPA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-financial-data"></a>Données financières R.U.

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-personal-information-online-code-of-practice-piocp"></a>U.K. Personal Information Online Code of Practice (PIOCP)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PIOCP pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PIOCP pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-personally-identifiable-information-pii-data"></a>U.K. Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-privacy-and-electronic-communications-regulations"></a>U.K. Privacy and Electronic Communications Regulations

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PECR pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PECR pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-federal-trade-commission-ftc-consumer-rules"></a>U.S. Federal Trade Commission (FTC) Consumer Rules

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Règles de protection des consommateurs du FTC pour les États-Unis : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’acheminement ABA — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Règles de protection des consommateurs du FTC pour les États-Unis : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’acheminement ABA — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-financial-data"></a>Données financières US

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour les États-Unis : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’acheminement ABA — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour les États-Unis : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’acheminement ABA — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-gramm-leach-bliley-act-glba"></a>U.S. Gramm-Leach-Bliley Act (GLBA)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi GLBA américaine : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi GLBA américaine : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-health-insurance-act-hipaa"></a>U.S. Health Insurance Act (HIPAA)

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Contenu correspond aux États-Unis HIPAA  <br/> | Contient des informations sensibles suivantes :  <br/>  Numéro de sécurité sociale américain (SSN) — nombre Min 1, Max compter à un  <br/>  Numéro de la Drug Enforcement Agency (DEA) — Nombre Min 1, Max compter à un  <br/> **ET** <br/>  Contenu contient une de ces conditions :  <br/>  Classification de maux international (ICD-9-CM) — nombre Min 1, Max compter les  <br/>  Classification de maux international (ICD-10-CM) — nombre Min 1, Max compter les  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
   
## <a name="us-patriot-act"></a>U.S. Patriot Act

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi USA Patriot Act américaine : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi USA Patriot Act américaine : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-personally-identifiable-information-pii-data"></a>U.S. Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour les États-Unis : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour les États-Unis : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-state-breach-notification-laws"></a>U.S. State Breach Notification Laws

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Lois américaines sur les violations de la sécurité : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Lois américaines sur les violations de la sécurité : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de permis de conduire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-state-social-security-number-confidentiality-laws"></a>U.S. State Social Security Number Confidentiality Laws

|**Nom de la règle**|**Conditions <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Lois SSN américaines : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Lois SSN américaines : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   

