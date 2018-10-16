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
# <a name="office-365-certificate-chains"></a><span data-ttu-id="fea63-106">Chaînes de certificats d’Office 365</span><span class="sxs-lookup"><span data-stu-id="fea63-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="fea63-p102">Office 365 utilise un certain nombre de fournisseurs de certificat différent. Voici la liste complète des certificats racines Office 365 connus que les clients peuvent rencontrer lors de l’accès à Office 365. Pour plus d’informations sur les certificats que vous devrez peut-être installer dans votre propre infrastructure, voir [planifier les certificats SSL de tiers pour Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Les informations de certificat suivantes s’applique à toutes les instances de cloud dans le monde entier et national d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="fea63-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="fea63-111">**Type de certificat**</span><span class="sxs-lookup"><span data-stu-id="fea63-111">**Certificate type**</span></span>|<span data-ttu-id="fea63-112">**Téléchargement P7b**</span><span class="sxs-lookup"><span data-stu-id="fea63-112">**P7b download**</span></span>|<span data-ttu-id="fea63-113">**Points de terminaison de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-113">**CRL Endpoints**</span></span>|<span data-ttu-id="fea63-114">**Points de terminaison OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="fea63-115">**Points de terminaison AIA**</span><span class="sxs-lookup"><span data-stu-id="fea63-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="fea63-116">Certificats racine de confiance publiquement</span><span class="sxs-lookup"><span data-stu-id="fea63-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="fea63-117">Groupement de certificat racine Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="fea63-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="fea63-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="fea63-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="fea63-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="fea63-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="fea63-120">N/A</span><span class="sxs-lookup"><span data-stu-id="fea63-120">N/A</span></span>  <br/> |<span data-ttu-id="fea63-121">N/A</span><span class="sxs-lookup"><span data-stu-id="fea63-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="fea63-122">Approuvés publiquement certificats intermédiaires</span><span class="sxs-lookup"><span data-stu-id="fea63-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="fea63-123">Groupement de certificats intermédiaires d’Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="fea63-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="fea63-124">cdp1.public-trust.com</span><span class="sxs-lookup"><span data-stu-id="fea63-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="fea63-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="fea63-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="fea63-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="fea63-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="fea63-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="fea63-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="fea63-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="fea63-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="fea63-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="fea63-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="fea63-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="fea63-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="fea63-131">crl3.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="fea63-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="fea63-132">crl4.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="fea63-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="fea63-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="fea63-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="fea63-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="fea63-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="fea63-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="fea63-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="fea63-136">OCSP.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="fea63-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="fea63-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="fea63-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="fea63-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="fea63-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="fea63-139">OCSP.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="fea63-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="fea63-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="fea63-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="fea63-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="fea63-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="fea63-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="fea63-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="fea63-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="fea63-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="fea63-144">racine-c3-2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="fea63-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="fea63-145">root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="fea63-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="fea63-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="fea63-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="fea63-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="fea63-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="fea63-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="fea63-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="fea63-149">cacert.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="fea63-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="fea63-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="fea63-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="fea63-151">Développez les sections intermédiaires ci-dessous pour afficher des détails supplémentaires sur les fournisseurs de certificat racine.</span><span class="sxs-lookup"><span data-stu-id="fea63-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="fea63-152">Détails du certificat racine Office 365</span><span class="sxs-lookup"><span data-stu-id="fea63-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="fea63-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="fea63-153"></span></span>

 <span data-ttu-id="fea63-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="fea63-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="fea63-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="fea63-155">|:-----|</span></span>
|<span data-ttu-id="fea63-156">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="fea63-157">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-157">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-158">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-158"></span></span>|
|<span data-ttu-id="fea63-159">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-159">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-160">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-160"></span></span>|
|<span data-ttu-id="fea63-161">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-162">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-162"></span></span>|
|<span data-ttu-id="fea63-163">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-164">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-164"></span></span>|
|<span data-ttu-id="fea63-165">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-165">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-166">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-166"></span></span>|
|<span data-ttu-id="fea63-167">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-168">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-168"></span></span>|
|<span data-ttu-id="fea63-169">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-170">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-170"></span></span>|
|<span data-ttu-id="fea63-171">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-172">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-172"></span></span>|
|<span data-ttu-id="fea63-173">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-174">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-174"></span></span>|
   
 <span data-ttu-id="fea63-175">**RACINE CNNIC**</span><span class="sxs-lookup"><span data-stu-id="fea63-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-176">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-176">**Subject**</span></span>|
|<span data-ttu-id="fea63-177">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-177"></span></span>|
|<span data-ttu-id="fea63-178">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-178">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-179">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-179"></span></span>|
|<span data-ttu-id="fea63-180">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-180">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-181">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-181"></span></span>|
|<span data-ttu-id="fea63-182">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-183">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-183"></span></span>|
|<span data-ttu-id="fea63-184">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-185">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-185"></span></span>|
|<span data-ttu-id="fea63-186">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-186">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-187">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-187"></span></span>|
|<span data-ttu-id="fea63-188">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-189">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-189"></span></span>|
|<span data-ttu-id="fea63-190">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-191">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-191"></span></span>|
|<span data-ttu-id="fea63-192">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-193">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-193"></span></span>|
|<span data-ttu-id="fea63-194">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-195">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-195"></span></span>|
|<span data-ttu-id="fea63-196">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-197">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-197"></span></span>|
   
 <span data-ttu-id="fea63-198">**Autorité de certification racine globale DigiCert**</span><span class="sxs-lookup"><span data-stu-id="fea63-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-199">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-199">**Subject**</span></span>|
|<span data-ttu-id="fea63-200">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-200"></span></span>|
|<span data-ttu-id="fea63-201">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-201">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-202">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-202"></span></span>|
|<span data-ttu-id="fea63-203">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-203">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-204">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-204"></span></span>|
|<span data-ttu-id="fea63-205">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-206">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-206"></span></span>|
|<span data-ttu-id="fea63-207">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-208">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-208"></span></span>|
|<span data-ttu-id="fea63-209">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-209">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-210">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-210"></span></span>|
|<span data-ttu-id="fea63-211">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-212">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-212"></span></span>|
|<span data-ttu-id="fea63-213">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-214">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-214"></span></span>|
|<span data-ttu-id="fea63-215">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-216">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-216"></span></span>|
|<span data-ttu-id="fea63-217">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-218">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-218"></span></span>|
|<span data-ttu-id="fea63-219">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-220">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-220"></span></span>|
   
 <span data-ttu-id="fea63-221">**Autorité de certification racine DigiCert High Assurance EV**</span><span class="sxs-lookup"><span data-stu-id="fea63-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-222">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-222">**Subject**</span></span>|
|<span data-ttu-id="fea63-223">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-223"></span></span>|
|<span data-ttu-id="fea63-224">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-224">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-225">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-225"></span></span>|
|<span data-ttu-id="fea63-226">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-226">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-227">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-227"></span></span>|
|<span data-ttu-id="fea63-228">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-229">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-229"></span></span>|
|<span data-ttu-id="fea63-230">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-231">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-231"></span></span>|
|<span data-ttu-id="fea63-232">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-232">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-233">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-233"></span></span>|
|<span data-ttu-id="fea63-234">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-235">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-235"></span></span>|
|<span data-ttu-id="fea63-236">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-237">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-237"></span></span>|
|<span data-ttu-id="fea63-238">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-239">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-239"></span></span>|
|<span data-ttu-id="fea63-240">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-241">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-241"></span></span>|
|<span data-ttu-id="fea63-242">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-243">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-243"></span></span>|
   
 <span data-ttu-id="fea63-244">**Autorité de certification racine de confiance D classe 3 2 2009**</span><span class="sxs-lookup"><span data-stu-id="fea63-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-245">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-245">**Subject**</span></span>|
|<span data-ttu-id="fea63-246">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-246"></span></span>|
|<span data-ttu-id="fea63-247">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-247">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-248">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-248"></span></span>|
|<span data-ttu-id="fea63-249">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-249">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-250">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-250"></span></span>|
|<span data-ttu-id="fea63-251">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-252">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-252"></span></span>|
|<span data-ttu-id="fea63-253">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-254">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-254"></span></span>|
|<span data-ttu-id="fea63-255">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-255">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-256">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-256"></span></span>|
|<span data-ttu-id="fea63-257">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-258">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-258"></span></span>|
|<span data-ttu-id="fea63-259">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-260">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-260"></span></span>|
|<span data-ttu-id="fea63-261">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-262">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-262"></span></span>|
|<span data-ttu-id="fea63-263">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-264">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-264"></span></span>|
|<span data-ttu-id="fea63-265">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-265">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-266">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-266"></span></span>|
   
 <span data-ttu-id="fea63-267">**Autorité de certification racine de confiance D classe 3 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="fea63-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-268">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-268">**Subject**</span></span>|
|<span data-ttu-id="fea63-269">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-269"></span></span>|
|<span data-ttu-id="fea63-270">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-270">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-271">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-271"></span></span>|
|<span data-ttu-id="fea63-272">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-272">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-273">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-273"></span></span>|
|<span data-ttu-id="fea63-274">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-275">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-275"></span></span>|
|<span data-ttu-id="fea63-276">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-277">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-277"></span></span>|
|<span data-ttu-id="fea63-278">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-278">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-279">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-279"></span></span>|
|<span data-ttu-id="fea63-280">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-281">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-281"></span></span>|
|<span data-ttu-id="fea63-282">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-283">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-283"></span></span>|
|<span data-ttu-id="fea63-284">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-285">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-285"></span></span>|
|<span data-ttu-id="fea63-286">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-287">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-287"></span></span>|
|<span data-ttu-id="fea63-288">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-288">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-289">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-289"></span></span>|
   
 <span data-ttu-id="fea63-290">**Racine de l’heure d’été X3 de l’autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="fea63-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-291">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-291">**Subject**</span></span>|
|<span data-ttu-id="fea63-292">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-292"></span></span>|
|<span data-ttu-id="fea63-293">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-293">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-294">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-294"></span></span>|
|<span data-ttu-id="fea63-295">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-295">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-296">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-296"></span></span>|
|<span data-ttu-id="fea63-297">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-298">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-298"></span></span>|
|<span data-ttu-id="fea63-299">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-300">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-300"></span></span>|
|<span data-ttu-id="fea63-301">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-301">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-302">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-302"></span></span>|
|<span data-ttu-id="fea63-303">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-304">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-304"></span></span>|
|<span data-ttu-id="fea63-305">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-306">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-306"></span></span>|
|<span data-ttu-id="fea63-307">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-308">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-308"></span></span>|
|<span data-ttu-id="fea63-309">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-310">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-310"></span></span>|
   
 <span data-ttu-id="fea63-311">**Confier autorité de Certification racine - G2**</span><span class="sxs-lookup"><span data-stu-id="fea63-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-312">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-312">**Subject**</span></span>|
|<span data-ttu-id="fea63-313">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-313"></span></span>|
|<span data-ttu-id="fea63-314">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-314">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-315">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-315"></span></span>|
|<span data-ttu-id="fea63-316">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-316">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-317">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-317"></span></span>|
|<span data-ttu-id="fea63-318">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-319">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-319"></span></span>|
|<span data-ttu-id="fea63-320">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-321">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-321"></span></span>|
|<span data-ttu-id="fea63-322">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-322">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-323">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-323"></span></span>|
|<span data-ttu-id="fea63-324">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-325">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-325"></span></span>|
|<span data-ttu-id="fea63-326">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-327">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-327"></span></span>|
|<span data-ttu-id="fea63-328">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-329">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-329"></span></span>|
|<span data-ttu-id="fea63-330">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-331">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-331"></span></span>|
   
 <span data-ttu-id="fea63-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="fea63-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-333">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-333">**Subject**</span></span>|
|<span data-ttu-id="fea63-334">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-334"></span></span>|
|<span data-ttu-id="fea63-335">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-335">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-336">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-336"></span></span>|
|<span data-ttu-id="fea63-337">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-337">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-338">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-338"></span></span>|
|<span data-ttu-id="fea63-339">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-340">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-340"></span></span>|
|<span data-ttu-id="fea63-341">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-342">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-342"></span></span>|
|<span data-ttu-id="fea63-343">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-343">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-344">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-344"></span></span>|
|<span data-ttu-id="fea63-345">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-346">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-346"></span></span>|
|<span data-ttu-id="fea63-347">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-348">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-348"></span></span>|
|<span data-ttu-id="fea63-349">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-350">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-350"></span></span>|
|<span data-ttu-id="fea63-351">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-352">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-352"></span></span>|
   
 <span data-ttu-id="fea63-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="fea63-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-354">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-354">**Subject**</span></span>|
|<span data-ttu-id="fea63-355">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-355"></span></span>|
|<span data-ttu-id="fea63-356">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-356">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-357">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-357"></span></span>|
|<span data-ttu-id="fea63-358">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-358">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-359">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-359"></span></span>|
|<span data-ttu-id="fea63-360">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-361">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-361"></span></span>|
|<span data-ttu-id="fea63-362">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-363">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-363"></span></span>|
|<span data-ttu-id="fea63-364">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-364">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-365">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-365"></span></span>|
|<span data-ttu-id="fea63-366">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-367">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-367"></span></span>|
|<span data-ttu-id="fea63-368">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-369">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-369"></span></span>|
|<span data-ttu-id="fea63-370">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-371">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-371"></span></span>|
|<span data-ttu-id="fea63-372">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-373">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-373"></span></span>|
|<span data-ttu-id="fea63-374">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-375">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-375"></span></span>|
|<span data-ttu-id="fea63-376">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-376">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-377">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-377"></span></span>|
   
 <span data-ttu-id="fea63-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="fea63-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-379">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-379">**Subject**</span></span>|
|<span data-ttu-id="fea63-380">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-380"></span></span>|
|<span data-ttu-id="fea63-381">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-381">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-382">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-382"></span></span>|
|<span data-ttu-id="fea63-383">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-383">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-384">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-384"></span></span>|
|<span data-ttu-id="fea63-385">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-386">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-386"></span></span>|
|<span data-ttu-id="fea63-387">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-388">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-388"></span></span>|
|<span data-ttu-id="fea63-389">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-389">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-390">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-390"></span></span>|
|<span data-ttu-id="fea63-391">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-392">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-392"></span></span>|
|<span data-ttu-id="fea63-393">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-394">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-394"></span></span>|
|<span data-ttu-id="fea63-395">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-396">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-396"></span></span>|
|<span data-ttu-id="fea63-397">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-398">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-398"></span></span>|
   
 <span data-ttu-id="fea63-399">**Thawte autorité de certification racine principal - G3**</span><span class="sxs-lookup"><span data-stu-id="fea63-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-400">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-400">**Subject**</span></span>|
|<span data-ttu-id="fea63-401">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-401"></span></span>|
|<span data-ttu-id="fea63-402">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-402">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-403">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-403"></span></span>|
|<span data-ttu-id="fea63-404">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-404">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-405">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-405"></span></span>|
|<span data-ttu-id="fea63-406">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-407">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-407"></span></span>|
|<span data-ttu-id="fea63-408">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-409">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-409"></span></span>|
|<span data-ttu-id="fea63-410">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-410">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-411">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-411"></span></span>|
|<span data-ttu-id="fea63-412">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-413">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-413"></span></span>|
|<span data-ttu-id="fea63-414">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-415">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-415"></span></span>|
|<span data-ttu-id="fea63-416">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-417">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-417"></span></span>|
|<span data-ttu-id="fea63-418">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-419">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-419"></span></span>|
   
 <span data-ttu-id="fea63-420">**Autorité de Certification publique principale VeriSign de classe 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="fea63-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-421">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-421">**Subject**</span></span>|
|<span data-ttu-id="fea63-422">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-422"></span></span>|
|<span data-ttu-id="fea63-423">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-423">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-424">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-424"></span></span>|
|<span data-ttu-id="fea63-425">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-425">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-426">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-426"></span></span>|
|<span data-ttu-id="fea63-427">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-428">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-428"></span></span>|
|<span data-ttu-id="fea63-429">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-430">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-430"></span></span>|
|<span data-ttu-id="fea63-431">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-431">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-432">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-432"></span></span>|
|<span data-ttu-id="fea63-433">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-434">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-434"></span></span>|
|<span data-ttu-id="fea63-435">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-436">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-436"></span></span>|
|<span data-ttu-id="fea63-437">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-438">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-438"></span></span>|
|<span data-ttu-id="fea63-439">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-440">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="fea63-441">Détails du certificat intermédiaire Office 365</span><span class="sxs-lookup"><span data-stu-id="fea63-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="fea63-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="fea63-442"></span></span>

 <span data-ttu-id="fea63-443">**SHA256 CNNIC SSL**</span><span class="sxs-lookup"><span data-stu-id="fea63-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-444">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-444">**Subject**</span></span>|
|<span data-ttu-id="fea63-445">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-445"></span></span>|
|<span data-ttu-id="fea63-446">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-446">**Issuer**</span></span>|
|<span data-ttu-id="fea63-447">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-447"></span></span>|
|<span data-ttu-id="fea63-448">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-448">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-449">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-449"></span></span>|
|<span data-ttu-id="fea63-450">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-450">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-451">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-451"></span></span>|
|<span data-ttu-id="fea63-452">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-453">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-453"></span></span>|
|<span data-ttu-id="fea63-454">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-455">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-455"></span></span>|
|<span data-ttu-id="fea63-456">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-456">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-457">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-457"></span></span>|
|<span data-ttu-id="fea63-458">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-459">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-459"></span></span>|
|<span data-ttu-id="fea63-460">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-461">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-461"></span></span>|
|<span data-ttu-id="fea63-462">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-463">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-463"></span></span>|
|<span data-ttu-id="fea63-464">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-465">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-465"></span></span>|
|<span data-ttu-id="fea63-466">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-467">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-467"></span></span>|
|<span data-ttu-id="fea63-468">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="fea63-468">**AIA URLs**</span></span>|
|<span data-ttu-id="fea63-469">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-469"></span></span>|
|<span data-ttu-id="fea63-470">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-470">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-471">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-471"></span></span>|
|<span data-ttu-id="fea63-472">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-473">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-473"></span></span>|
   
 <span data-ttu-id="fea63-474">**Autorité de certification de classe 3 D-TRUST SSL 1 2009**</span><span class="sxs-lookup"><span data-stu-id="fea63-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-475">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-475">**Subject**</span></span>|
|<span data-ttu-id="fea63-476">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-476"></span></span>|
|<span data-ttu-id="fea63-477">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-477">**Issuer**</span></span>|
|<span data-ttu-id="fea63-478">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-478"></span></span>|
|<span data-ttu-id="fea63-479">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="fea63-480">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-480"></span></span>|
|<span data-ttu-id="fea63-481">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-481">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-482">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-482"></span></span>|
|<span data-ttu-id="fea63-483">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-483">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-484">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-484"></span></span>|
|<span data-ttu-id="fea63-485">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-486">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-486"></span></span>|
|<span data-ttu-id="fea63-487">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-488">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-488"></span></span>|
|<span data-ttu-id="fea63-489">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-489">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-490">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-490"></span></span>|
|<span data-ttu-id="fea63-491">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-492">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-492"></span></span>|
|<span data-ttu-id="fea63-493">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-494">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-494"></span></span>|
|<span data-ttu-id="fea63-495">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-496">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-496"></span></span>|
|<span data-ttu-id="fea63-497">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-498">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-498"></span></span>|
|<span data-ttu-id="fea63-499">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-500">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-500"></span></span>|
|<span data-ttu-id="fea63-501">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-501">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-502">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-502"></span></span>|
|<span data-ttu-id="fea63-503">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-504">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-504"></span></span>|
   
 <span data-ttu-id="fea63-505">**Autorité de certification de classe 3 D-TRUST SSL 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="fea63-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-506">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-506">**Subject**</span></span>|
|<span data-ttu-id="fea63-507">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-507"></span></span>|
|<span data-ttu-id="fea63-508">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-508">**Issuer**</span></span>|
|<span data-ttu-id="fea63-509">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-509"></span></span>|
|<span data-ttu-id="fea63-510">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="fea63-511">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-511"></span></span>|
|<span data-ttu-id="fea63-512">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-512">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-513">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-513"></span></span>|
|<span data-ttu-id="fea63-514">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-514">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-515">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-515"></span></span>|
|<span data-ttu-id="fea63-516">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-517">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-517"></span></span>|
|<span data-ttu-id="fea63-518">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-519">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-519"></span></span>|
|<span data-ttu-id="fea63-520">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-520">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-521">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-521"></span></span>|
|<span data-ttu-id="fea63-522">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-523">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-523"></span></span>|
|<span data-ttu-id="fea63-524">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-525">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-525"></span></span>|
|<span data-ttu-id="fea63-526">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-527">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-527"></span></span>|
|<span data-ttu-id="fea63-528">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-529">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-529"></span></span>|
|<span data-ttu-id="fea63-530">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-531">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-531"></span></span>|
|<span data-ttu-id="fea63-532">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-532">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-533">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-533"></span></span>|
|<span data-ttu-id="fea63-534">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-535">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-535"></span></span>|
   
 <span data-ttu-id="fea63-536">**DigiCert Cloud Services CA-1**</span><span class="sxs-lookup"><span data-stu-id="fea63-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-537">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-537">**Subject**</span></span>|
|<span data-ttu-id="fea63-538">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-538"></span></span>|
|<span data-ttu-id="fea63-539">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-539">**Issuer**</span></span>|
|<span data-ttu-id="fea63-540">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-540"></span></span>|
|<span data-ttu-id="fea63-541">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-541">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-542">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-542"></span></span>|
|<span data-ttu-id="fea63-543">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-543">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-544">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-544"></span></span>|
|<span data-ttu-id="fea63-545">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-546">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-546"></span></span>|
|<span data-ttu-id="fea63-547">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-548">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-548"></span></span>|
|<span data-ttu-id="fea63-549">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-549">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-550">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-550"></span></span>|
|<span data-ttu-id="fea63-551">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-552">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-552"></span></span>|
|<span data-ttu-id="fea63-553">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-554">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-554"></span></span>|
|<span data-ttu-id="fea63-555">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-556">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-556"></span></span>|
|<span data-ttu-id="fea63-557">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-558">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-558"></span></span>|
|<span data-ttu-id="fea63-559">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-560">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-560"></span></span>|
|<span data-ttu-id="fea63-561">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-561">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-562">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-562"></span></span>|
|<span data-ttu-id="fea63-563">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-564">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-564"></span></span>|
   
 <span data-ttu-id="fea63-565">**DigiCert SHA2 High Assurance Server autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="fea63-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-566">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-566">**Subject**</span></span>|
|<span data-ttu-id="fea63-567">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-567"></span></span>|
|<span data-ttu-id="fea63-568">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-568">**Issuer**</span></span>|
|<span data-ttu-id="fea63-569">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-569"></span></span>|
|<span data-ttu-id="fea63-570">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-570">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-571">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-571"></span></span>|
|<span data-ttu-id="fea63-572">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-572">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-573">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-573"></span></span>|
|<span data-ttu-id="fea63-574">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-575">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-575"></span></span>|
|<span data-ttu-id="fea63-576">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-577">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-577"></span></span>|
|<span data-ttu-id="fea63-578">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-578">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-579">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-579"></span></span>|
|<span data-ttu-id="fea63-580">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-581">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-581"></span></span>|
|<span data-ttu-id="fea63-582">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-583">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-583"></span></span>|
|<span data-ttu-id="fea63-584">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-585">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-585"></span></span>|
|<span data-ttu-id="fea63-586">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-587">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-587"></span></span>|
|<span data-ttu-id="fea63-588">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-589">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-589"></span></span>|
|<span data-ttu-id="fea63-590">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-590">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-591">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-591"></span></span>|
|<span data-ttu-id="fea63-592">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-593">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-593"></span></span>|
   
 <span data-ttu-id="fea63-594">**Serveur sécurisé DigiCert SHA2 autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="fea63-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-595">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-595">**Subject**</span></span>|
|<span data-ttu-id="fea63-596">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-596"></span></span>|
|<span data-ttu-id="fea63-597">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-597">**Issuer**</span></span>|
|<span data-ttu-id="fea63-598">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-598"></span></span>|
|<span data-ttu-id="fea63-599">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-599">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-600">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-600"></span></span>|
|<span data-ttu-id="fea63-601">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-601">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-602">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-602"></span></span>|
|<span data-ttu-id="fea63-603">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-604">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-604"></span></span>|
|<span data-ttu-id="fea63-605">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-606">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-606"></span></span>|
|<span data-ttu-id="fea63-607">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-607">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-608">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-608"></span></span>|
|<span data-ttu-id="fea63-609">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-610">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-610"></span></span>|
|<span data-ttu-id="fea63-611">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-612">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-612"></span></span>|
|<span data-ttu-id="fea63-613">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-614">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-614"></span></span>|
|<span data-ttu-id="fea63-615">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-616">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-616"></span></span>|
|<span data-ttu-id="fea63-617">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-618">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-618"></span></span>|
|<span data-ttu-id="fea63-619">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-619">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-620">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-620"></span></span>|
|<span data-ttu-id="fea63-621">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-622">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-622"></span></span>|
   
 <span data-ttu-id="fea63-623">**Confier l’autorité de Certification - L1C**</span><span class="sxs-lookup"><span data-stu-id="fea63-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-624">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-624">**Subject**</span></span>|
|<span data-ttu-id="fea63-625">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-625"></span></span>|
|<span data-ttu-id="fea63-626">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-626">**Issuer**</span></span>|
|<span data-ttu-id="fea63-627">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-627"></span></span>|
|<span data-ttu-id="fea63-628">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-628">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-629">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-629"></span></span>|
|<span data-ttu-id="fea63-630">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-630">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-631">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-631"></span></span>|
|<span data-ttu-id="fea63-632">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-633">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-633"></span></span>|
|<span data-ttu-id="fea63-634">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-635">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-635"></span></span>|
|<span data-ttu-id="fea63-636">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-636">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-637">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-637"></span></span>|
|<span data-ttu-id="fea63-638">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-639">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-639"></span></span>|
|<span data-ttu-id="fea63-640">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-641">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-641"></span></span>|
|<span data-ttu-id="fea63-642">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-643">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-643"></span></span>|
|<span data-ttu-id="fea63-644">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-645">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-645"></span></span>|
|<span data-ttu-id="fea63-646">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-647">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-647"></span></span>|
|<span data-ttu-id="fea63-648">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-648">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-649">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-649"></span></span>|
|<span data-ttu-id="fea63-650">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-651">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-651"></span></span>|
   
 <span data-ttu-id="fea63-652">**Confier l’autorité de Certification - L1K**</span><span class="sxs-lookup"><span data-stu-id="fea63-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-653">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-653">**Subject**</span></span>|
|<span data-ttu-id="fea63-654">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-654"></span></span>|
|<span data-ttu-id="fea63-655">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-655">**Issuer**</span></span>|
|<span data-ttu-id="fea63-656">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-656"></span></span>|
|<span data-ttu-id="fea63-657">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-657">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-658">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-658"></span></span>|
|<span data-ttu-id="fea63-659">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-659">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-660">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-660"></span></span>|
|<span data-ttu-id="fea63-661">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-662">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-662"></span></span>|
|<span data-ttu-id="fea63-663">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-664">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-664"></span></span>|
|<span data-ttu-id="fea63-665">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-665">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-666">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-666"></span></span>|
|<span data-ttu-id="fea63-667">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-668">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-668"></span></span>|
|<span data-ttu-id="fea63-669">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-670">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-670"></span></span>|
|<span data-ttu-id="fea63-671">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-672">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-672"></span></span>|
|<span data-ttu-id="fea63-673">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-674">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-674"></span></span>|
|<span data-ttu-id="fea63-675">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-676">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-676"></span></span>|
|<span data-ttu-id="fea63-677">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-677">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-678">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-678"></span></span>|
|<span data-ttu-id="fea63-679">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-680">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-680"></span></span>|
   
 <span data-ttu-id="fea63-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="fea63-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-682">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-682">**Subject**</span></span>|
|<span data-ttu-id="fea63-683">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-683"></span></span>|
|<span data-ttu-id="fea63-684">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-684">**Issuer**</span></span>|
|<span data-ttu-id="fea63-685">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-685"></span></span>|
|<span data-ttu-id="fea63-686">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-686">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-687">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-687"></span></span>|
|<span data-ttu-id="fea63-688">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-688">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-689">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-689"></span></span>|
|<span data-ttu-id="fea63-690">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-691">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-691"></span></span>|
|<span data-ttu-id="fea63-692">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-693">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-693"></span></span>|
|<span data-ttu-id="fea63-694">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-694">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-695">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-695"></span></span>|
|<span data-ttu-id="fea63-696">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-697">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-697"></span></span>|
|<span data-ttu-id="fea63-698">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-699">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-699"></span></span>|
|<span data-ttu-id="fea63-700">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-701">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-701"></span></span>|
|<span data-ttu-id="fea63-702">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-703">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-703"></span></span>|
|<span data-ttu-id="fea63-704">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-705">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-705"></span></span>|
|<span data-ttu-id="fea63-706">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-706">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-707">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-707"></span></span>|
|<span data-ttu-id="fea63-708">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-709">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-709"></span></span>|
   
 <span data-ttu-id="fea63-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="fea63-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-711">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-711">**Subject**</span></span>|
|<span data-ttu-id="fea63-712">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-712"></span></span>|
|<span data-ttu-id="fea63-713">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-713">**Issuer**</span></span>|
|<span data-ttu-id="fea63-714">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-714"></span></span>|
|<span data-ttu-id="fea63-715">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-715">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-716">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-716"></span></span>|
|<span data-ttu-id="fea63-717">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-717">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-718">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-718"></span></span>|
|<span data-ttu-id="fea63-719">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-720">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-720"></span></span>|
|<span data-ttu-id="fea63-721">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-722">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-722"></span></span>|
|<span data-ttu-id="fea63-723">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-723">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-724">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-724"></span></span>|
|<span data-ttu-id="fea63-725">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-726">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-726"></span></span>|
|<span data-ttu-id="fea63-727">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-728">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-728"></span></span>|
|<span data-ttu-id="fea63-729">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-730">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-730"></span></span>|
|<span data-ttu-id="fea63-731">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-732">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-732"></span></span>|
|<span data-ttu-id="fea63-733">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-734">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-734"></span></span>|
|<span data-ttu-id="fea63-735">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-735">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-736">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-736"></span></span>|
|<span data-ttu-id="fea63-737">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-738">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-738"></span></span>|
   
 <span data-ttu-id="fea63-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span><span class="sxs-lookup"><span data-stu-id="fea63-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-740">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-740">**Subject**</span></span>|
|<span data-ttu-id="fea63-741">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-741"></span></span>|
|<span data-ttu-id="fea63-742">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-742">**Issuer**</span></span>|
|<span data-ttu-id="fea63-743">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-743"></span></span>|
|<span data-ttu-id="fea63-744">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-744">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-745">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-745"></span></span>|
|<span data-ttu-id="fea63-746">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-746">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-747">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-747"></span></span>|
|<span data-ttu-id="fea63-748">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-749">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-749"></span></span>|
|<span data-ttu-id="fea63-750">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-751">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-751"></span></span>|
|<span data-ttu-id="fea63-752">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-752">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-753">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-753"></span></span>|
|<span data-ttu-id="fea63-754">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-755">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-755"></span></span>|
|<span data-ttu-id="fea63-756">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-757">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-757"></span></span>|
|<span data-ttu-id="fea63-758">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-759">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-759"></span></span>|
|<span data-ttu-id="fea63-760">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-761">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-761"></span></span>|
|<span data-ttu-id="fea63-762">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-763">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-763"></span></span>|
|<span data-ttu-id="fea63-764">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-764">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-765">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-765"></span></span>|
|<span data-ttu-id="fea63-766">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-767">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-767"></span></span>|
   
 <span data-ttu-id="fea63-768">**GlobalSign organisation Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="fea63-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-769">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-769">**Subject**</span></span>|
|<span data-ttu-id="fea63-770">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-770"></span></span>|
|<span data-ttu-id="fea63-771">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-771">**Issuer**</span></span>|
|<span data-ttu-id="fea63-772">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-772"></span></span>|
|<span data-ttu-id="fea63-773">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-773">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-774">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-774"></span></span>|
|<span data-ttu-id="fea63-775">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-775">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-776">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-776"></span></span>|
|<span data-ttu-id="fea63-777">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-778">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-778"></span></span>|
|<span data-ttu-id="fea63-779">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-780">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-780"></span></span>|
|<span data-ttu-id="fea63-781">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-781">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-782">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-782"></span></span>|
|<span data-ttu-id="fea63-783">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-784">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-784"></span></span>|
|<span data-ttu-id="fea63-785">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-786">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-786"></span></span>|
|<span data-ttu-id="fea63-787">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-788">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-788"></span></span>|
|<span data-ttu-id="fea63-789">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-790">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-790"></span></span>|
|<span data-ttu-id="fea63-791">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-792">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-792"></span></span>|
|<span data-ttu-id="fea63-793">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-793">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-794">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-794"></span></span>|
|<span data-ttu-id="fea63-795">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-796">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-796"></span></span>|
   
 <span data-ttu-id="fea63-797">**GlobalSign organisation Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="fea63-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-798">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-798">**Subject**</span></span>|
|<span data-ttu-id="fea63-799">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-799"></span></span>|
|<span data-ttu-id="fea63-800">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-800">**Issuer**</span></span>|
|<span data-ttu-id="fea63-801">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-801"></span></span>|
|<span data-ttu-id="fea63-802">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-802">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-803">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-803"></span></span>|
|<span data-ttu-id="fea63-804">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-804">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-805">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-805"></span></span>|
|<span data-ttu-id="fea63-806">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-807">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-807"></span></span>|
|<span data-ttu-id="fea63-808">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-809">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-809"></span></span>|
|<span data-ttu-id="fea63-810">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-810">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-811">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-811"></span></span>|
|<span data-ttu-id="fea63-812">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-813">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-813"></span></span>|
|<span data-ttu-id="fea63-814">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-815">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-815"></span></span>|
|<span data-ttu-id="fea63-816">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-817">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-817"></span></span>|
|<span data-ttu-id="fea63-818">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-819">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-819"></span></span>|
|<span data-ttu-id="fea63-820">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-821">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-821"></span></span>|
|<span data-ttu-id="fea63-822">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-822">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-823">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-823"></span></span>|
|<span data-ttu-id="fea63-824">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-825">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-825"></span></span>|
   
 <span data-ttu-id="fea63-826">**Nous allons chiffrer autorité X3**</span><span class="sxs-lookup"><span data-stu-id="fea63-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-827">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-827">**Subject**</span></span>|
|<span data-ttu-id="fea63-828">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-828"></span></span>|
|<span data-ttu-id="fea63-829">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-829">**Issuer**</span></span>|
|<span data-ttu-id="fea63-830">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-830"></span></span>|
|<span data-ttu-id="fea63-831">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-831">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-832">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-832"></span></span>|
|<span data-ttu-id="fea63-833">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-833">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-834">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-834"></span></span>|
|<span data-ttu-id="fea63-835">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-836">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-836"></span></span>|
|<span data-ttu-id="fea63-837">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-838">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-838"></span></span>|
|<span data-ttu-id="fea63-839">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-839">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-840">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-840"></span></span>|
|<span data-ttu-id="fea63-841">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-842">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-842"></span></span>|
|<span data-ttu-id="fea63-843">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-844">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-844"></span></span>|
|<span data-ttu-id="fea63-845">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-846">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-846"></span></span>|
|<span data-ttu-id="fea63-847">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-848">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-848"></span></span>|
|<span data-ttu-id="fea63-849">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-850">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-850"></span></span>|
|<span data-ttu-id="fea63-851">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="fea63-851">**AIA URLs**</span></span>|
|<span data-ttu-id="fea63-852">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-852"></span></span>|
|<span data-ttu-id="fea63-853">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-853">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-854">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-854"></span></span>|
|<span data-ttu-id="fea63-855">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-856">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-856"></span></span>|
   
 <span data-ttu-id="fea63-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="fea63-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-858">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-858">**Subject**</span></span>|
|<span data-ttu-id="fea63-859">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-859"></span></span>|
|<span data-ttu-id="fea63-860">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-860">**Issuer**</span></span>|
|<span data-ttu-id="fea63-861">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-861"></span></span>|
|<span data-ttu-id="fea63-862">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-862">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-863">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-863"></span></span>|
|<span data-ttu-id="fea63-864">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-864">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-865">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-865"></span></span>|
|<span data-ttu-id="fea63-866">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-867">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-867"></span></span>|
|<span data-ttu-id="fea63-868">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-869">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-869"></span></span>|
|<span data-ttu-id="fea63-870">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-870">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-871">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-871"></span></span>|
|<span data-ttu-id="fea63-872">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-873">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-873"></span></span>|
|<span data-ttu-id="fea63-874">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-875">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-875"></span></span>|
|<span data-ttu-id="fea63-876">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-877">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-877"></span></span>|
|<span data-ttu-id="fea63-878">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-879">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-879"></span></span>|
|<span data-ttu-id="fea63-880">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-881">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-881"></span></span>|
|<span data-ttu-id="fea63-882">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-882">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-883">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-883"></span></span>|
   
 <span data-ttu-id="fea63-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="fea63-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-885">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-885">**Subject**</span></span>|
|<span data-ttu-id="fea63-886">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-886"></span></span>|
|<span data-ttu-id="fea63-887">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-887">**Issuer**</span></span>|
|<span data-ttu-id="fea63-888">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-888"></span></span>|
|<span data-ttu-id="fea63-889">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-889">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-890">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-890"></span></span>|
|<span data-ttu-id="fea63-891">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-891">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-892">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-892"></span></span>|
|<span data-ttu-id="fea63-893">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-894">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-894"></span></span>|
|<span data-ttu-id="fea63-895">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-896">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-896"></span></span>|
|<span data-ttu-id="fea63-897">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-897">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-898">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-898"></span></span>|
|<span data-ttu-id="fea63-899">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-900">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-900"></span></span>|
|<span data-ttu-id="fea63-901">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-902">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-902"></span></span>|
|<span data-ttu-id="fea63-903">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-904">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-904"></span></span>|
|<span data-ttu-id="fea63-905">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-906">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-906"></span></span>|
|<span data-ttu-id="fea63-907">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-908">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-908"></span></span>|
|<span data-ttu-id="fea63-909">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-909">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-910">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-910"></span></span>|
|<span data-ttu-id="fea63-911">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-912">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-912"></span></span>|
   
 <span data-ttu-id="fea63-913">**Autorité de certification Microsoft IT TLS 1**</span><span class="sxs-lookup"><span data-stu-id="fea63-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-914">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-914">**Subject**</span></span>|
|<span data-ttu-id="fea63-915">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-915"></span></span>|
|<span data-ttu-id="fea63-916">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-916">**Issuer**</span></span>|
|<span data-ttu-id="fea63-917">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-917"></span></span>|
|<span data-ttu-id="fea63-918">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-918">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-919">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-919"></span></span>|
|<span data-ttu-id="fea63-920">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-920">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-921">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-921"></span></span>|
|<span data-ttu-id="fea63-922">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-923">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-923"></span></span>|
|<span data-ttu-id="fea63-924">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-925">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-925"></span></span>|
|<span data-ttu-id="fea63-926">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-926">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-927">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-927"></span></span>|
|<span data-ttu-id="fea63-928">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-929">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-929"></span></span>|
|<span data-ttu-id="fea63-930">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-931">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-931"></span></span>|
|<span data-ttu-id="fea63-932">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-933">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-933"></span></span>|
|<span data-ttu-id="fea63-934">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-935">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-935"></span></span>|
|<span data-ttu-id="fea63-936">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-937">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-937"></span></span>|
|<span data-ttu-id="fea63-938">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-938">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-939">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-939"></span></span>|
|<span data-ttu-id="fea63-940">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-941">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-941"></span></span>|
   
 <span data-ttu-id="fea63-942">**Autorité de certification Microsoft IT TLS 2**</span><span class="sxs-lookup"><span data-stu-id="fea63-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-943">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-943">**Subject**</span></span>|
|<span data-ttu-id="fea63-944">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-944"></span></span>|
|<span data-ttu-id="fea63-945">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-945">**Issuer**</span></span>|
|<span data-ttu-id="fea63-946">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-946"></span></span>|
|<span data-ttu-id="fea63-947">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-947">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-948">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-948"></span></span>|
|<span data-ttu-id="fea63-949">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-949">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-950">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-950"></span></span>|
|<span data-ttu-id="fea63-951">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-952">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-952"></span></span>|
|<span data-ttu-id="fea63-953">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-954">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-954"></span></span>|
|<span data-ttu-id="fea63-955">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-955">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-956">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-956"></span></span>|
|<span data-ttu-id="fea63-957">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-958">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-958"></span></span>|
|<span data-ttu-id="fea63-959">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-960">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-960"></span></span>|
|<span data-ttu-id="fea63-961">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-962">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-962"></span></span>|
|<span data-ttu-id="fea63-963">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-964">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-964"></span></span>|
|<span data-ttu-id="fea63-965">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-966">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-966"></span></span>|
|<span data-ttu-id="fea63-967">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-967">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-968">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-968"></span></span>|
|<span data-ttu-id="fea63-969">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-970">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-970"></span></span>|
   
 <span data-ttu-id="fea63-971">**Autorité de certification Microsoft IT TLS 4**</span><span class="sxs-lookup"><span data-stu-id="fea63-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-972">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-972">**Subject**</span></span>|
|<span data-ttu-id="fea63-973">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-973"></span></span>|
|<span data-ttu-id="fea63-974">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-974">**Issuer**</span></span>|
|<span data-ttu-id="fea63-975">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-975"></span></span>|
|<span data-ttu-id="fea63-976">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-976">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-977">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-977"></span></span>|
|<span data-ttu-id="fea63-978">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-978">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-979">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-979"></span></span>|
|<span data-ttu-id="fea63-980">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-981">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-981"></span></span>|
|<span data-ttu-id="fea63-982">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-983">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-983"></span></span>|
|<span data-ttu-id="fea63-984">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-984">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-985">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-985"></span></span>|
|<span data-ttu-id="fea63-986">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-987">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-987"></span></span>|
|<span data-ttu-id="fea63-988">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-989">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-989"></span></span>|
|<span data-ttu-id="fea63-990">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-991">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-991"></span></span>|
|<span data-ttu-id="fea63-992">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-993">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-993"></span></span>|
|<span data-ttu-id="fea63-994">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-995">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-995"></span></span>|
|<span data-ttu-id="fea63-996">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-996">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-997">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-997"></span></span>|
|<span data-ttu-id="fea63-998">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-999">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-999"></span></span>|
   
 <span data-ttu-id="fea63-1000">**Autorité de certification Microsoft IT TLS 5**</span><span class="sxs-lookup"><span data-stu-id="fea63-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-1001">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1001">**Subject**</span></span>|
|<span data-ttu-id="fea63-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1002"></span></span>|
|<span data-ttu-id="fea63-1003">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-1003">**Issuer**</span></span>|
|<span data-ttu-id="fea63-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1004"></span></span>|
|<span data-ttu-id="fea63-1005">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-1005">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1006"></span></span>|
|<span data-ttu-id="fea63-1007">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1008"></span></span>|
|<span data-ttu-id="fea63-1009">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1010"></span></span>|
|<span data-ttu-id="fea63-1011">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1012"></span></span>|
|<span data-ttu-id="fea63-1013">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1014"></span></span>|
|<span data-ttu-id="fea63-1015">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1016"></span></span>|
|<span data-ttu-id="fea63-1017">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1018"></span></span>|
|<span data-ttu-id="fea63-1019">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1020"></span></span>|
|<span data-ttu-id="fea63-1021">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1022"></span></span>|
|<span data-ttu-id="fea63-1023">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1024"></span></span>|
|<span data-ttu-id="fea63-1025">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1026"></span></span>|
|<span data-ttu-id="fea63-1027">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1028"></span></span>|
   
 <span data-ttu-id="fea63-1029">**Classe Symantec EV 3 SSL CA - G3**</span><span class="sxs-lookup"><span data-stu-id="fea63-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-1030">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1030">**Subject**</span></span>|
|<span data-ttu-id="fea63-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1031"></span></span>|
|<span data-ttu-id="fea63-1032">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-1032">**Issuer**</span></span>|
|<span data-ttu-id="fea63-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1033"></span></span>|
|<span data-ttu-id="fea63-1034">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="fea63-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1035"></span></span>|
|<span data-ttu-id="fea63-1036">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-1036">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1037"></span></span>|
|<span data-ttu-id="fea63-1038">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1039"></span></span>|
|<span data-ttu-id="fea63-1040">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1041"></span></span>|
|<span data-ttu-id="fea63-1042">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1043"></span></span>|
|<span data-ttu-id="fea63-1044">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1045"></span></span>|
|<span data-ttu-id="fea63-1046">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1047"></span></span>|
|<span data-ttu-id="fea63-1048">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1049"></span></span>|
|<span data-ttu-id="fea63-1050">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1051"></span></span>|
|<span data-ttu-id="fea63-1052">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1053"></span></span>|
|<span data-ttu-id="fea63-1054">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1055"></span></span>|
|<span data-ttu-id="fea63-1056">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1057"></span></span>|
|<span data-ttu-id="fea63-1058">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1059"></span></span>|
   
 <span data-ttu-id="fea63-1060">**Serveur sécurisé Symantec classe 3 CA - G4**</span><span class="sxs-lookup"><span data-stu-id="fea63-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-1061">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1061">**Subject**</span></span>|
|<span data-ttu-id="fea63-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1062"></span></span>|
|<span data-ttu-id="fea63-1063">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-1063">**Issuer**</span></span>|
|<span data-ttu-id="fea63-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1064"></span></span>|
|<span data-ttu-id="fea63-1065">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="fea63-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1066"></span></span>|
|<span data-ttu-id="fea63-1067">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-1067">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1068"></span></span>|
|<span data-ttu-id="fea63-1069">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1070"></span></span>|
|<span data-ttu-id="fea63-1071">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1072"></span></span>|
|<span data-ttu-id="fea63-1073">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1074"></span></span>|
|<span data-ttu-id="fea63-1075">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1076"></span></span>|
|<span data-ttu-id="fea63-1077">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1078"></span></span>|
|<span data-ttu-id="fea63-1079">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1080"></span></span>|
|<span data-ttu-id="fea63-1081">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1082"></span></span>|
|<span data-ttu-id="fea63-1083">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1084"></span></span>|
|<span data-ttu-id="fea63-1085">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1086"></span></span>|
|<span data-ttu-id="fea63-1087">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1088"></span></span>|
|<span data-ttu-id="fea63-1089">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1090"></span></span>|
   
 <span data-ttu-id="fea63-1091">**Thawte SHA256 SSL autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="fea63-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-1092">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1092">**Subject**</span></span>|
|<span data-ttu-id="fea63-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1093"></span></span>|
|<span data-ttu-id="fea63-1094">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-1094">**Issuer**</span></span>|
|<span data-ttu-id="fea63-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1095"></span></span>|
|<span data-ttu-id="fea63-1096">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="fea63-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1097"></span></span>|
|<span data-ttu-id="fea63-1098">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-1098">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1099"></span></span>|
|<span data-ttu-id="fea63-1100">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1101"></span></span>|
|<span data-ttu-id="fea63-1102">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1103"></span></span>|
|<span data-ttu-id="fea63-1104">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1105"></span></span>|
|<span data-ttu-id="fea63-1106">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1107"></span></span>|
|<span data-ttu-id="fea63-1108">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1109"></span></span>|
|<span data-ttu-id="fea63-1110">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1111"></span></span>|
|<span data-ttu-id="fea63-1112">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1113"></span></span>|
|<span data-ttu-id="fea63-1114">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1115"></span></span>|
|<span data-ttu-id="fea63-1116">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1117"></span></span>|
|<span data-ttu-id="fea63-1118">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1119"></span></span>|
|<span data-ttu-id="fea63-1120">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1121"></span></span>|
   
 <span data-ttu-id="fea63-1122">**Autorité de certification SureServer de Verizon Akamai G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="fea63-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="fea63-1123">**Objet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1123">**Subject**</span></span>|
|<span data-ttu-id="fea63-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1124"></span></span>|
|<span data-ttu-id="fea63-1125">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="fea63-1125">**Issuer**</span></span>|
|<span data-ttu-id="fea63-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1126"></span></span>|
|<span data-ttu-id="fea63-1127">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="fea63-1127">**Serial Number**</span></span>|
|<span data-ttu-id="fea63-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1128"></span></span>|
|<span data-ttu-id="fea63-1129">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="fea63-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="fea63-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1130"></span></span>|
|<span data-ttu-id="fea63-1131">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="fea63-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="fea63-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1132"></span></span>|
|<span data-ttu-id="fea63-1133">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="fea63-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="fea63-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1134"></span></span>|
|<span data-ttu-id="fea63-1135">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="fea63-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="fea63-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1136"></span></span>|
|<span data-ttu-id="fea63-1137">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="fea63-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1138"></span></span>|
|<span data-ttu-id="fea63-1139">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="fea63-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="fea63-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1140"></span></span>|
|<span data-ttu-id="fea63-1141">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="fea63-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1142"></span></span>|
|<span data-ttu-id="fea63-1143">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1144"></span></span>|
|<span data-ttu-id="fea63-1145">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="fea63-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="fea63-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1146"></span></span>|
|<span data-ttu-id="fea63-1147">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="fea63-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="fea63-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1148"></span></span>|
|<span data-ttu-id="fea63-1149">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="fea63-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="fea63-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1150"></span></span>|
|<span data-ttu-id="fea63-1151">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="fea63-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="fea63-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="fea63-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="fea63-1153">Chemins d’accès du certificat supplémentaire</span><span class="sxs-lookup"><span data-stu-id="fea63-1153">Additional certificate paths</span></span>
<span data-ttu-id="fea63-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="fea63-1154"></span></span>

<span data-ttu-id="fea63-1155">Les éléments suivants sont hérités certificats qui ne sont pas incluses ci-dessus et sont fusionnées avec la liste ci-dessus au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="fea63-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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


