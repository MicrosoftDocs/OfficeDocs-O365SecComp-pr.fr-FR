---
title: Chaînes de certificats d’Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 utilise un certain nombre de fournisseurs de certificat différent. Voici la liste complète des certificats racines Office 365 connus que les clients peuvent rencontrer lors de l’accès à Office 365. Pour plus d’informations sur les certificats, vous devrez peut-être installer dans votre propre infrastructure, voir Plan pour les certificats SSL tiers pour Office 365. Les informations de certificat suivantes s’applique à toutes les instances de cloud dans le monde entier et national d’Office 365.
ms.openlocfilehash: 97e00833e57f8f6b7352650b0efdef51ddba77fa
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575358"
---
# <a name="office-365-certificate-chains"></a>Chaînes de certificats d’Office 365

Office 365 utilise un certain nombre de fournisseurs de certificat différent. Voici la liste complète des certificats racines Office 365 connus que les clients peuvent rencontrer lors de l’accès à Office 365. Pour plus d’informations sur les certificats que vous devrez peut-être installer dans votre propre infrastructure, voir [planifier les certificats SSL de tiers pour Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Les informations de certificat suivantes s’applique à toutes les instances de cloud dans le monde entier et national d’Office 365.
  

|**Type de certificat**|**Téléchargement P7b**|**Points de terminaison de révocation de certificats**|**Points de terminaison OCSP**|**Points de terminaison AIA**|
|:-----|:-----|:-----|:-----|:-----|
|[Certificats racine de confiance publiquement](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[Groupement de certificat racine Office 365 (P7B)](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |CRL.GlobalSign.NET  <br/> www.d-Trust.NET  <br/> |N/A  <br/> |N/A  <br/> |
|[Approuvés publiquement certificats intermédiaires](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[Groupement de certificats intermédiaires d’Office 365 (P7B)](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |cdp1.public-trust.com  <br/> CRL.cnnic.CN  <br/> CRL.Entrust.NET  <br/> CRL.GlobalSign.com  <br/> CRL.GlobalSign.NET  <br/> CRL.identrust.com  <br/> CRL.Thawte.com  <br/> crl3.DigiCert.com  <br/> crl4.DigiCert.com  <br/> s1.symcb.com  <br/> www.d-Trust.NET  <br/> |isrg.trustid.OCSP.identrust.com  <br/> OCSP.DigiCert.com  <br/> OCSP.Entrust.NET  <br/> OCSP.GlobalSign.com  <br/> OCSP.OmniRoot.com  <br/> OCSP.startssl.com  <br/> OCSP.Thawte.com  <br/> ocsp2.GlobalSign.com  <br/> ocspcnnicroot.cnnic.CN  <br/> racine-c3-2-2009.ocsp.d-trust.net  <br/> root-C3-ca2-EV-2009.OCSP.d-Trust.NET  <br/> s2.symcb.com  <br/> |AIA.startssl.com  <br/> Apps.identrust.com  <br/> cacert.OmniRoot.com  <br/> www.cnnic.CN  <br/> |
   
Développez les sections intermédiaires ci-dessous pour afficher des détails supplémentaires sur les fournisseurs de certificat racine.
  
## <a name="office-365-root-certificate-details"></a>Détails du certificat racine Office 365
<a name="RootCerts"> </a>

 **Baltimore CyberTrust Root**
  
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **RACINE CNNIC**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **Autorité de certification racine globale DigiCert**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **Autorité de certification racine DigiCert High Assurance EV**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **Autorité de certification racine de confiance D classe 3 2 2009**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
   
 **Autorité de certification racine de confiance D classe 3 2 EV 2009**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
   
 **Racine de l’heure d’été X3 de l’autorité de certification**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **Confier autorité de Certification racine - G2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **Entrust.net Certification Authority (2048)**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **GlobalSign**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
   
 **GlobalSign Root CA**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **Thawte autorité de certification racine principal - G3**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
 **Autorité de Certification publique principale VeriSign de classe 3 - G5**
  
||
|:-----|
|**Objet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
   
## <a name="office-365-intermediate-certificate-details"></a>Détails du certificat intermédiaire Office 365
<a name="IntermediateCerts"> </a>

 **SHA256 CNNIC SSL**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL AIA**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Autorité de certification de classe 3 D-TRUST SSL 1 2009**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Nom du sujet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Autorité de certification de classe 3 D-TRUST SSL 1 EV 2009**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Nom du sujet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **DigiCert Cloud Services CA-1**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **DigiCert SHA2 High Assurance Server autorité de certification**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Serveur sécurisé DigiCert SHA2 autorité de certification**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Confier l’autorité de Certification - L1C**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Confier l’autorité de Certification - L1K**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **GlobalSign**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **GlobalSign Extended Validation CA - SHA256 - G2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **GlobalSign Extended Validation CA - SHA256 - G3**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **GlobalSign organisation Validation CA - SHA256 - G2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **GlobalSign organisation Validation CA - SHA256 - G2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Nous allons chiffrer autorité X3**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL AIA**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Microsoft IT SSL SHA2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
   
 **Microsoft IT SSL SHA2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Autorité de certification Microsoft IT TLS 1**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Autorité de certification Microsoft IT TLS 2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Autorité de certification Microsoft IT TLS 4**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Autorité de certification Microsoft IT TLS 5**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Classe Symantec EV 3 SSL CA - G3**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Nom du sujet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Serveur sécurisé Symantec classe 3 CA - G4**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Nom du sujet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Thawte SHA256 SSL autorité de certification**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Nom du sujet**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
 **Autorité de certification SureServer de Verizon Akamai G14-SHA2**
  
||
|:-----|
|**Objet**|
|:-----|
|**Issuer**|
|:-----|
|**Numéro de série**|
|:-----|
|**Longueur de clé publique**|
|:-----|
|**Algorithme de signature**|
|:-----|
|**Validité pas avant**|
|:-----|
|**Validité pas après**|
|:-----|
|**Identificateur de clé sujet**|
|:-----|
|**Identificateur de clé d’autorité**|
|:-----|
|**Empreinte numérique (SHA-1)**|
|:-----|
|**Empreinte numérique (SHA-256)**|
|:-----|
|**Code confidentiel (SHA-256)**|
|:-----|
|**URL AIA**|
|:-----|
|**URL de révocation de certificats**|
|:-----|
|**URL OCSP**|
|:-----|
   
## <a name="additional-certificate-paths"></a>Chemins d’accès du certificat supplémentaire
<a name="IntermediateCerts"> </a>

Les éléments suivants sont hérités certificats qui ne sont pas incluses ci-dessus et sont fusionnées avec la liste ci-dessus au fil du temps.
  
```
evsecure-aia.verisign.com
sa.symcb.com
sd.symcb.com
*.omniroot.com
*.verisign.com
*.symcb.com
*.symcd.com
*.verisign.net
*.geotrust.com
*.entrust.net
*.public-trust.com
EVIntl-ocsp.verisign.com
EVSecure-ocsp.verisign.com
isrg.trustid.ocsp.identrust.com
ocsp.digicert.com
ocsp.entrust.net
ocsp.globalsign.com/ExtendedSSLSHA256CACross
ocsp.globalsign.com/rootr1
ocsp.globalsign.com/rootr2
ocsp2.globalsign.com/rootr3
ocsp.int-x3.letsencrypt.org/
ocsp.msocsp.com
ocsp.omniroot.com/baltimoreroot
ocsp2.globalsign.com/gsextendvalsha2g3r3
ocsp2.globalsign.com/gsorganizationvalsha2g2
ocsp2.globalsign.com/gsorganizationvalsha2g3
ocsp2.globalsign.com/rootr3
ocspx.digicert.com
s2.symcb.com
sr.symcd.com
su.symcd.com
vassg142.ocsp.omniroot.com
cdp1.public-trust.com/CRL/Omniroot2025.crl
crl.entrust.net/2048ca.crl
crl.entrust.net/g2ca.crl
crl.entrust.net/level1k.crl
crl.entrust.net/rootca1.crl
crl.globalsign.com/gs/gsextendvalsha2g3r3.crl
crl.globalsign.com/gs/gsorganizationvalsha2g2.crl
crl.globalsign.com/gsorganizationvalsha2g3.crl
crl.globalsign.com/root.crl
crl.globalsign.net/root-r2.crl
crl.globalsign.com/root-r3.crl
crl.globalsign.net/root.crl
crl.identrust.com/DSTROOTCAX3CRL.crl
crl.microsoft.com/pki/mscorp/crl/msitwww1.crl
crl.microsoft.com/pki/mscorp/crl/msitwww2.crl
crl3.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl3.digicert.com/DigiCertGlobalRootCA.crl
crl3.digicert.com/sha2-ev-server-g1.crl
crl3.digicert.com/sha2-ha-server-g5.crl
crl3.digicert.com/ssca-sha2-g5.crl
crl4.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl4.digicert.com/DigiCertGlobalRootCA.crl
crl4.digicert.com/DigiCertHighAssuranceEVRootCA.crl
crl4.digicert.com/sha2-ev-server-g1.crl
crl4.digicert.com/sha2-ha-server-g5.crl
crl4.digicert.com/ssca-sha2-g5.crl
EVIntl-crl.verisign.com/EVIntl2006.crl
EVSecure-crl.verisign.com/pca3-g5.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww1.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww2.crl
s1.symcb.com/pca3-g5.crl
sr.symcb.com/sr.crl
su.symcb.com/su.crl
vassg142.crl.omniroot.com/vassg142.crl
aia.entrust.net/l1k-chain256.cer
apps.identrust.com/roots/dstrootcax3.p7c
https://cacert.a.omniroot.com/vassg142.crt
https://cacert.a.omniroot.com/vassg142.der
https://cacert.omniroot.com/baltimoreroot.crt
https://cacert.omniroot.com/baltimoreroot.der
cacerts.digicert.com/DigiCertCloudServicesCA-1.crt
cacerts.digicert.com/DigiCertSHA2ExtendedValidationServerCA.crt
cacerts.digicert.com/DigiCertSHA2HighAssuranceServerCA.crt
cacerts.digicert.com/DigiCertSHA2SecureServerCA.crt
cert.int-x3.letsencrypt.org/
EVIntl-aia.verisign.com/EVIntl2006.cer
secure.globalsign.com/cacert/gsextendvalsha2g2r2.crt
secure.globalsign.com/cacert/gsextendvalsha2g3r3.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g2r1.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g3.crt
sr.symcb.com/sr.crt
su.symcb.com/su.crt
https://www.digicert.com/CACerts/DigiCertGlobalRootCA.crt
https://www.digicert.com/CACerts/DigiCertHighAssuranceEVRootCA.crt
www.microsoft.com/pki/mscorp/msitwww1.crt
www.microsoft.com/pki/mscorp/msitwww2.crt

```


