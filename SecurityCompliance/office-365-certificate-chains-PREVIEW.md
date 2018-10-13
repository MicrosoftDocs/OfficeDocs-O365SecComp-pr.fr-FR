---
title: Chaînes de certificats d’Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 utilise un certain nombre de fournisseurs de certificat différent. Voici la liste complète des certificats racines Office 365 connus que les clients peuvent rencontrer lors de l’accès à Office 365. Pour plus d’informations sur les certificats, vous devrez peut-être installer dans votre propre infrastructure, voir Plan pour les certificats SSL tiers pour Office 365. Les informations de certificat suivantes s’applique à toutes les instances de cloud dans le monde entier et national d’Office 365.
ms.openlocfilehash: 1dcc2dc38bb8e3239a3be3983791b0c60917dc5e
ms.sourcegitcommit: 13f40ff7c1799152bf45af2d8110f4f3235b770a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25549749"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="51c71-106">Chaînes de certificats d’Office 365</span><span class="sxs-lookup"><span data-stu-id="51c71-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="51c71-p102">Office 365 utilise un certain nombre de fournisseurs de certificat différent. Voici la liste complète des certificats racines Office 365 connus que les clients peuvent rencontrer lors de l’accès à Office 365. Pour plus d’informations sur les certificats que vous devrez peut-être installer dans votre propre infrastructure, voir [planifier les certificats SSL de tiers pour Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Les informations de certificat suivantes s’applique à toutes les instances de cloud dans le monde entier et national d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="51c71-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="51c71-111">**Type de certificat**</span><span class="sxs-lookup"><span data-stu-id="51c71-111">**Certificate type**</span></span>|<span data-ttu-id="51c71-112">**Téléchargement P7b**</span><span class="sxs-lookup"><span data-stu-id="51c71-112">**P7b download**</span></span>|<span data-ttu-id="51c71-113">**Points de terminaison de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-113">**CRL Endpoints**</span></span>|<span data-ttu-id="51c71-114">**Points de terminaison OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="51c71-115">**Points de terminaison AIA**</span><span class="sxs-lookup"><span data-stu-id="51c71-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="51c71-116">Certificats racine de confiance publiquement</span><span class="sxs-lookup"><span data-stu-id="51c71-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="51c71-117">Groupement de certificat racine Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="51c71-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="51c71-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="51c71-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="51c71-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="51c71-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="51c71-120">N/A</span><span class="sxs-lookup"><span data-stu-id="51c71-120">N/A</span></span>  <br/> |<span data-ttu-id="51c71-121">N/A</span><span class="sxs-lookup"><span data-stu-id="51c71-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="51c71-122">Approuvés publiquement certificats intermédiaires</span><span class="sxs-lookup"><span data-stu-id="51c71-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="51c71-123">Groupement de certificats intermédiaires d’Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="51c71-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="51c71-124">cdp1.public-trust.com</span><span class="sxs-lookup"><span data-stu-id="51c71-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="51c71-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="51c71-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="51c71-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="51c71-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="51c71-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="51c71-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="51c71-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="51c71-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="51c71-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="51c71-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="51c71-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="51c71-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="51c71-131">crl3.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="51c71-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="51c71-132">crl4.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="51c71-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="51c71-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="51c71-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="51c71-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="51c71-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="51c71-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="51c71-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="51c71-136">OCSP.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="51c71-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="51c71-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="51c71-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="51c71-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="51c71-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="51c71-139">OCSP.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="51c71-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="51c71-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="51c71-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="51c71-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="51c71-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="51c71-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="51c71-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="51c71-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="51c71-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="51c71-144">racine-c3-2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="51c71-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="51c71-145">root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="51c71-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="51c71-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="51c71-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="51c71-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="51c71-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="51c71-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="51c71-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="51c71-149">cacert.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="51c71-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="51c71-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="51c71-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="51c71-151">Développez les sections intermédiaires ci-dessous pour afficher des détails supplémentaires sur les fournisseurs de certificat racine.</span><span class="sxs-lookup"><span data-stu-id="51c71-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="51c71-152">Détails du certificat racine Office 365</span><span class="sxs-lookup"><span data-stu-id="51c71-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="51c71-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="51c71-153"></span></span>

 <span data-ttu-id="51c71-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="51c71-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="51c71-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="51c71-155">|:-----|</span></span>
|<span data-ttu-id="51c71-156">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="51c71-157">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-157">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-158">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-158"></span></span>|
|<span data-ttu-id="51c71-159">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-159">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-160">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-160"></span></span>|
|<span data-ttu-id="51c71-161">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-162">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-162"></span></span>|
|<span data-ttu-id="51c71-163">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-164">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-164"></span></span>|
|<span data-ttu-id="51c71-165">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-165">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-166">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-166"></span></span>|
|<span data-ttu-id="51c71-167">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-168">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-168"></span></span>|
|<span data-ttu-id="51c71-169">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-170">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-170"></span></span>|
|<span data-ttu-id="51c71-171">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-172">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-172"></span></span>|
|<span data-ttu-id="51c71-173">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-174">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-174"></span></span>|
   
 <span data-ttu-id="51c71-175">**RACINE CNNIC**</span><span class="sxs-lookup"><span data-stu-id="51c71-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-176">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-176">**Subject**</span></span>|
|<span data-ttu-id="51c71-177">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-177"></span></span>|
|<span data-ttu-id="51c71-178">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-178">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-179">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-179"></span></span>|
|<span data-ttu-id="51c71-180">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-180">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-181">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-181"></span></span>|
|<span data-ttu-id="51c71-182">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-183">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-183"></span></span>|
|<span data-ttu-id="51c71-184">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-185">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-185"></span></span>|
|<span data-ttu-id="51c71-186">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-186">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-187">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-187"></span></span>|
|<span data-ttu-id="51c71-188">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-189">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-189"></span></span>|
|<span data-ttu-id="51c71-190">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-191">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-191"></span></span>|
|<span data-ttu-id="51c71-192">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-193">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-193"></span></span>|
|<span data-ttu-id="51c71-194">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-195">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-195"></span></span>|
|<span data-ttu-id="51c71-196">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-197">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-197"></span></span>|
   
 <span data-ttu-id="51c71-198">**Autorité de certification racine globale DigiCert**</span><span class="sxs-lookup"><span data-stu-id="51c71-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-199">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-199">**Subject**</span></span>|
|<span data-ttu-id="51c71-200">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-200"></span></span>|
|<span data-ttu-id="51c71-201">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-201">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-202">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-202"></span></span>|
|<span data-ttu-id="51c71-203">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-203">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-204">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-204"></span></span>|
|<span data-ttu-id="51c71-205">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-206">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-206"></span></span>|
|<span data-ttu-id="51c71-207">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-208">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-208"></span></span>|
|<span data-ttu-id="51c71-209">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-209">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-210">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-210"></span></span>|
|<span data-ttu-id="51c71-211">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-212">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-212"></span></span>|
|<span data-ttu-id="51c71-213">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-214">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-214"></span></span>|
|<span data-ttu-id="51c71-215">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-216">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-216"></span></span>|
|<span data-ttu-id="51c71-217">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-218">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-218"></span></span>|
|<span data-ttu-id="51c71-219">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-220">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-220"></span></span>|
   
 <span data-ttu-id="51c71-221">**Autorité de certification racine DigiCert High Assurance EV**</span><span class="sxs-lookup"><span data-stu-id="51c71-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-222">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-222">**Subject**</span></span>|
|<span data-ttu-id="51c71-223">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-223"></span></span>|
|<span data-ttu-id="51c71-224">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-224">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-225">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-225"></span></span>|
|<span data-ttu-id="51c71-226">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-226">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-227">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-227"></span></span>|
|<span data-ttu-id="51c71-228">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-229">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-229"></span></span>|
|<span data-ttu-id="51c71-230">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-231">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-231"></span></span>|
|<span data-ttu-id="51c71-232">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-232">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-233">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-233"></span></span>|
|<span data-ttu-id="51c71-234">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-235">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-235"></span></span>|
|<span data-ttu-id="51c71-236">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-237">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-237"></span></span>|
|<span data-ttu-id="51c71-238">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-239">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-239"></span></span>|
|<span data-ttu-id="51c71-240">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-241">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-241"></span></span>|
|<span data-ttu-id="51c71-242">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-243">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-243"></span></span>|
   
 <span data-ttu-id="51c71-244">**Autorité de certification racine de confiance D classe 3 2 2009**</span><span class="sxs-lookup"><span data-stu-id="51c71-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-245">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-245">**Subject**</span></span>|
|<span data-ttu-id="51c71-246">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-246"></span></span>|
|<span data-ttu-id="51c71-247">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-247">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-248">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-248"></span></span>|
|<span data-ttu-id="51c71-249">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-249">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-250">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-250"></span></span>|
|<span data-ttu-id="51c71-251">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-252">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-252"></span></span>|
|<span data-ttu-id="51c71-253">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-254">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-254"></span></span>|
|<span data-ttu-id="51c71-255">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-255">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-256">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-256"></span></span>|
|<span data-ttu-id="51c71-257">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-258">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-258"></span></span>|
|<span data-ttu-id="51c71-259">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-260">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-260"></span></span>|
|<span data-ttu-id="51c71-261">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-262">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-262"></span></span>|
|<span data-ttu-id="51c71-263">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-264">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-264"></span></span>|
|<span data-ttu-id="51c71-265">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-265">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-266">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-266"></span></span>|
   
 <span data-ttu-id="51c71-267">**Autorité de certification racine de confiance D classe 3 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="51c71-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-268">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-268">**Subject**</span></span>|
|<span data-ttu-id="51c71-269">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-269"></span></span>|
|<span data-ttu-id="51c71-270">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-270">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-271">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-271"></span></span>|
|<span data-ttu-id="51c71-272">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-272">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-273">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-273"></span></span>|
|<span data-ttu-id="51c71-274">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-275">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-275"></span></span>|
|<span data-ttu-id="51c71-276">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-277">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-277"></span></span>|
|<span data-ttu-id="51c71-278">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-278">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-279">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-279"></span></span>|
|<span data-ttu-id="51c71-280">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-281">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-281"></span></span>|
|<span data-ttu-id="51c71-282">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-283">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-283"></span></span>|
|<span data-ttu-id="51c71-284">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-285">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-285"></span></span>|
|<span data-ttu-id="51c71-286">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-287">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-287"></span></span>|
|<span data-ttu-id="51c71-288">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-288">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-289">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-289"></span></span>|
   
 <span data-ttu-id="51c71-290">**Racine de l’heure d’été X3 de l’autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="51c71-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-291">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-291">**Subject**</span></span>|
|<span data-ttu-id="51c71-292">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-292"></span></span>|
|<span data-ttu-id="51c71-293">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-293">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-294">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-294"></span></span>|
|<span data-ttu-id="51c71-295">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-295">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-296">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-296"></span></span>|
|<span data-ttu-id="51c71-297">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-298">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-298"></span></span>|
|<span data-ttu-id="51c71-299">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-300">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-300"></span></span>|
|<span data-ttu-id="51c71-301">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-301">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-302">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-302"></span></span>|
|<span data-ttu-id="51c71-303">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-304">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-304"></span></span>|
|<span data-ttu-id="51c71-305">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-306">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-306"></span></span>|
|<span data-ttu-id="51c71-307">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-308">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-308"></span></span>|
|<span data-ttu-id="51c71-309">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-310">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-310"></span></span>|
   
 <span data-ttu-id="51c71-311">**Confier autorité de Certification racine - G2**</span><span class="sxs-lookup"><span data-stu-id="51c71-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-312">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-312">**Subject**</span></span>|
|<span data-ttu-id="51c71-313">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-313"></span></span>|
|<span data-ttu-id="51c71-314">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-314">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-315">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-315"></span></span>|
|<span data-ttu-id="51c71-316">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-316">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-317">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-317"></span></span>|
|<span data-ttu-id="51c71-318">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-319">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-319"></span></span>|
|<span data-ttu-id="51c71-320">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-321">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-321"></span></span>|
|<span data-ttu-id="51c71-322">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-322">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-323">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-323"></span></span>|
|<span data-ttu-id="51c71-324">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-325">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-325"></span></span>|
|<span data-ttu-id="51c71-326">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-327">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-327"></span></span>|
|<span data-ttu-id="51c71-328">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-329">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-329"></span></span>|
|<span data-ttu-id="51c71-330">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-331">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-331"></span></span>|
   
 <span data-ttu-id="51c71-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="51c71-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-333">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-333">**Subject**</span></span>|
|<span data-ttu-id="51c71-334">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-334"></span></span>|
|<span data-ttu-id="51c71-335">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-335">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-336">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-336"></span></span>|
|<span data-ttu-id="51c71-337">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-337">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-338">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-338"></span></span>|
|<span data-ttu-id="51c71-339">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-340">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-340"></span></span>|
|<span data-ttu-id="51c71-341">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-342">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-342"></span></span>|
|<span data-ttu-id="51c71-343">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-343">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-344">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-344"></span></span>|
|<span data-ttu-id="51c71-345">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-346">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-346"></span></span>|
|<span data-ttu-id="51c71-347">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-348">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-348"></span></span>|
|<span data-ttu-id="51c71-349">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-350">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-350"></span></span>|
|<span data-ttu-id="51c71-351">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-352">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-352"></span></span>|
   
 <span data-ttu-id="51c71-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="51c71-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-354">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-354">**Subject**</span></span>|
|<span data-ttu-id="51c71-355">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-355"></span></span>|
|<span data-ttu-id="51c71-356">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-356">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-357">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-357"></span></span>|
|<span data-ttu-id="51c71-358">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-358">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-359">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-359"></span></span>|
|<span data-ttu-id="51c71-360">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-361">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-361"></span></span>|
|<span data-ttu-id="51c71-362">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-363">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-363"></span></span>|
|<span data-ttu-id="51c71-364">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-364">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-365">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-365"></span></span>|
|<span data-ttu-id="51c71-366">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-367">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-367"></span></span>|
|<span data-ttu-id="51c71-368">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-369">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-369"></span></span>|
|<span data-ttu-id="51c71-370">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-371">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-371"></span></span>|
|<span data-ttu-id="51c71-372">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-373">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-373"></span></span>|
|<span data-ttu-id="51c71-374">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-375">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-375"></span></span>|
|<span data-ttu-id="51c71-376">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-376">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-377">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-377"></span></span>|
   
 <span data-ttu-id="51c71-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="51c71-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-379">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-379">**Subject**</span></span>|
|<span data-ttu-id="51c71-380">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-380"></span></span>|
|<span data-ttu-id="51c71-381">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-381">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-382">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-382"></span></span>|
|<span data-ttu-id="51c71-383">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-383">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-384">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-384"></span></span>|
|<span data-ttu-id="51c71-385">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-386">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-386"></span></span>|
|<span data-ttu-id="51c71-387">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-388">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-388"></span></span>|
|<span data-ttu-id="51c71-389">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-389">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-390">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-390"></span></span>|
|<span data-ttu-id="51c71-391">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-392">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-392"></span></span>|
|<span data-ttu-id="51c71-393">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-394">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-394"></span></span>|
|<span data-ttu-id="51c71-395">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-396">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-396"></span></span>|
|<span data-ttu-id="51c71-397">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-398">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-398"></span></span>|
   
 <span data-ttu-id="51c71-399">**Thawte autorité de certification racine principal - G3**</span><span class="sxs-lookup"><span data-stu-id="51c71-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-400">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-400">**Subject**</span></span>|
|<span data-ttu-id="51c71-401">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-401"></span></span>|
|<span data-ttu-id="51c71-402">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-402">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-403">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-403"></span></span>|
|<span data-ttu-id="51c71-404">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-404">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-405">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-405"></span></span>|
|<span data-ttu-id="51c71-406">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-407">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-407"></span></span>|
|<span data-ttu-id="51c71-408">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-409">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-409"></span></span>|
|<span data-ttu-id="51c71-410">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-410">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-411">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-411"></span></span>|
|<span data-ttu-id="51c71-412">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-413">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-413"></span></span>|
|<span data-ttu-id="51c71-414">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-415">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-415"></span></span>|
|<span data-ttu-id="51c71-416">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-417">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-417"></span></span>|
|<span data-ttu-id="51c71-418">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-419">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-419"></span></span>|
   
 <span data-ttu-id="51c71-420">**Autorité de Certification publique principale VeriSign de classe 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="51c71-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-421">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-421">**Subject**</span></span>|
|<span data-ttu-id="51c71-422">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-422"></span></span>|
|<span data-ttu-id="51c71-423">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-423">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-424">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-424"></span></span>|
|<span data-ttu-id="51c71-425">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-425">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-426">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-426"></span></span>|
|<span data-ttu-id="51c71-427">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-428">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-428"></span></span>|
|<span data-ttu-id="51c71-429">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-430">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-430"></span></span>|
|<span data-ttu-id="51c71-431">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-431">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-432">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-432"></span></span>|
|<span data-ttu-id="51c71-433">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-434">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-434"></span></span>|
|<span data-ttu-id="51c71-435">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-436">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-436"></span></span>|
|<span data-ttu-id="51c71-437">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-438">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-438"></span></span>|
|<span data-ttu-id="51c71-439">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-440">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="51c71-441">Détails du certificat intermédiaire Office 365</span><span class="sxs-lookup"><span data-stu-id="51c71-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="51c71-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="51c71-442"></span></span>

 <span data-ttu-id="51c71-443">**SHA256 CNNIC SSL**</span><span class="sxs-lookup"><span data-stu-id="51c71-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-444">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-444">**Subject**</span></span>|
|<span data-ttu-id="51c71-445">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-445"></span></span>|
|<span data-ttu-id="51c71-446">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-446">**Issuer**</span></span>|
|<span data-ttu-id="51c71-447">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-447"></span></span>|
|<span data-ttu-id="51c71-448">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-448">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-449">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-449"></span></span>|
|<span data-ttu-id="51c71-450">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-450">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-451">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-451"></span></span>|
|<span data-ttu-id="51c71-452">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-453">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-453"></span></span>|
|<span data-ttu-id="51c71-454">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-455">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-455"></span></span>|
|<span data-ttu-id="51c71-456">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-456">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-457">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-457"></span></span>|
|<span data-ttu-id="51c71-458">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-459">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-459"></span></span>|
|<span data-ttu-id="51c71-460">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-461">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-461"></span></span>|
|<span data-ttu-id="51c71-462">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-463">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-463"></span></span>|
|<span data-ttu-id="51c71-464">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-465">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-465"></span></span>|
|<span data-ttu-id="51c71-466">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-467">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-467"></span></span>|
|<span data-ttu-id="51c71-468">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="51c71-468">**AIA URLs**</span></span>|
|<span data-ttu-id="51c71-469">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-469"></span></span>|
|<span data-ttu-id="51c71-470">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-470">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-471">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-471"></span></span>|
|<span data-ttu-id="51c71-472">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-473">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-473"></span></span>|
   
 <span data-ttu-id="51c71-474">**Autorité de certification de classe 3 D-TRUST SSL 1 2009**</span><span class="sxs-lookup"><span data-stu-id="51c71-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-475">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-475">**Subject**</span></span>|
|<span data-ttu-id="51c71-476">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-476"></span></span>|
|<span data-ttu-id="51c71-477">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-477">**Issuer**</span></span>|
|<span data-ttu-id="51c71-478">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-478"></span></span>|
|<span data-ttu-id="51c71-479">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="51c71-480">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-480"></span></span>|
|<span data-ttu-id="51c71-481">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-481">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-482">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-482"></span></span>|
|<span data-ttu-id="51c71-483">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-483">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-484">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-484"></span></span>|
|<span data-ttu-id="51c71-485">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-486">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-486"></span></span>|
|<span data-ttu-id="51c71-487">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-488">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-488"></span></span>|
|<span data-ttu-id="51c71-489">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-489">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-490">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-490"></span></span>|
|<span data-ttu-id="51c71-491">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-492">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-492"></span></span>|
|<span data-ttu-id="51c71-493">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-494">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-494"></span></span>|
|<span data-ttu-id="51c71-495">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-496">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-496"></span></span>|
|<span data-ttu-id="51c71-497">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-498">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-498"></span></span>|
|<span data-ttu-id="51c71-499">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-500">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-500"></span></span>|
|<span data-ttu-id="51c71-501">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-501">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-502">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-502"></span></span>|
|<span data-ttu-id="51c71-503">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-504">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-504"></span></span>|
   
 <span data-ttu-id="51c71-505">**Autorité de certification de classe 3 D-TRUST SSL 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="51c71-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-506">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-506">**Subject**</span></span>|
|<span data-ttu-id="51c71-507">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-507"></span></span>|
|<span data-ttu-id="51c71-508">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-508">**Issuer**</span></span>|
|<span data-ttu-id="51c71-509">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-509"></span></span>|
|<span data-ttu-id="51c71-510">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="51c71-511">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-511"></span></span>|
|<span data-ttu-id="51c71-512">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-512">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-513">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-513"></span></span>|
|<span data-ttu-id="51c71-514">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-514">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-515">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-515"></span></span>|
|<span data-ttu-id="51c71-516">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-517">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-517"></span></span>|
|<span data-ttu-id="51c71-518">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-519">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-519"></span></span>|
|<span data-ttu-id="51c71-520">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-520">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-521">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-521"></span></span>|
|<span data-ttu-id="51c71-522">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-523">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-523"></span></span>|
|<span data-ttu-id="51c71-524">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-525">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-525"></span></span>|
|<span data-ttu-id="51c71-526">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-527">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-527"></span></span>|
|<span data-ttu-id="51c71-528">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-529">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-529"></span></span>|
|<span data-ttu-id="51c71-530">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-531">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-531"></span></span>|
|<span data-ttu-id="51c71-532">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-532">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-533">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-533"></span></span>|
|<span data-ttu-id="51c71-534">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-535">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-535"></span></span>|
   
 <span data-ttu-id="51c71-536">**DigiCert Cloud Services CA-1**</span><span class="sxs-lookup"><span data-stu-id="51c71-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-537">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-537">**Subject**</span></span>|
|<span data-ttu-id="51c71-538">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-538"></span></span>|
|<span data-ttu-id="51c71-539">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-539">**Issuer**</span></span>|
|<span data-ttu-id="51c71-540">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-540"></span></span>|
|<span data-ttu-id="51c71-541">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-541">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-542">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-542"></span></span>|
|<span data-ttu-id="51c71-543">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-543">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-544">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-544"></span></span>|
|<span data-ttu-id="51c71-545">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-546">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-546"></span></span>|
|<span data-ttu-id="51c71-547">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-548">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-548"></span></span>|
|<span data-ttu-id="51c71-549">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-549">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-550">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-550"></span></span>|
|<span data-ttu-id="51c71-551">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-552">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-552"></span></span>|
|<span data-ttu-id="51c71-553">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-554">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-554"></span></span>|
|<span data-ttu-id="51c71-555">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-556">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-556"></span></span>|
|<span data-ttu-id="51c71-557">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-558">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-558"></span></span>|
|<span data-ttu-id="51c71-559">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-560">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-560"></span></span>|
|<span data-ttu-id="51c71-561">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-561">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-562">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-562"></span></span>|
|<span data-ttu-id="51c71-563">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-564">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-564"></span></span>|
   
 <span data-ttu-id="51c71-565">**DigiCert SHA2 High Assurance Server autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="51c71-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-566">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-566">**Subject**</span></span>|
|<span data-ttu-id="51c71-567">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-567"></span></span>|
|<span data-ttu-id="51c71-568">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-568">**Issuer**</span></span>|
|<span data-ttu-id="51c71-569">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-569"></span></span>|
|<span data-ttu-id="51c71-570">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-570">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-571">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-571"></span></span>|
|<span data-ttu-id="51c71-572">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-572">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-573">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-573"></span></span>|
|<span data-ttu-id="51c71-574">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-575">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-575"></span></span>|
|<span data-ttu-id="51c71-576">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-577">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-577"></span></span>|
|<span data-ttu-id="51c71-578">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-578">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-579">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-579"></span></span>|
|<span data-ttu-id="51c71-580">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-581">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-581"></span></span>|
|<span data-ttu-id="51c71-582">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-583">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-583"></span></span>|
|<span data-ttu-id="51c71-584">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-585">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-585"></span></span>|
|<span data-ttu-id="51c71-586">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-587">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-587"></span></span>|
|<span data-ttu-id="51c71-588">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-589">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-589"></span></span>|
|<span data-ttu-id="51c71-590">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-590">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-591">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-591"></span></span>|
|<span data-ttu-id="51c71-592">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-593">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-593"></span></span>|
   
 <span data-ttu-id="51c71-594">**Serveur sécurisé DigiCert SHA2 autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="51c71-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-595">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-595">**Subject**</span></span>|
|<span data-ttu-id="51c71-596">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-596"></span></span>|
|<span data-ttu-id="51c71-597">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-597">**Issuer**</span></span>|
|<span data-ttu-id="51c71-598">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-598"></span></span>|
|<span data-ttu-id="51c71-599">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-599">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-600">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-600"></span></span>|
|<span data-ttu-id="51c71-601">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-601">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-602">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-602"></span></span>|
|<span data-ttu-id="51c71-603">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-604">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-604"></span></span>|
|<span data-ttu-id="51c71-605">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-606">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-606"></span></span>|
|<span data-ttu-id="51c71-607">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-607">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-608">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-608"></span></span>|
|<span data-ttu-id="51c71-609">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-610">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-610"></span></span>|
|<span data-ttu-id="51c71-611">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-612">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-612"></span></span>|
|<span data-ttu-id="51c71-613">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-614">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-614"></span></span>|
|<span data-ttu-id="51c71-615">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-616">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-616"></span></span>|
|<span data-ttu-id="51c71-617">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-618">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-618"></span></span>|
|<span data-ttu-id="51c71-619">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-619">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-620">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-620"></span></span>|
|<span data-ttu-id="51c71-621">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-622">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-622"></span></span>|
   
 <span data-ttu-id="51c71-623">**Confier l’autorité de Certification - L1C**</span><span class="sxs-lookup"><span data-stu-id="51c71-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-624">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-624">**Subject**</span></span>|
|<span data-ttu-id="51c71-625">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-625"></span></span>|
|<span data-ttu-id="51c71-626">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-626">**Issuer**</span></span>|
|<span data-ttu-id="51c71-627">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-627"></span></span>|
|<span data-ttu-id="51c71-628">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-628">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-629">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-629"></span></span>|
|<span data-ttu-id="51c71-630">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-630">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-631">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-631"></span></span>|
|<span data-ttu-id="51c71-632">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-633">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-633"></span></span>|
|<span data-ttu-id="51c71-634">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-635">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-635"></span></span>|
|<span data-ttu-id="51c71-636">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-636">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-637">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-637"></span></span>|
|<span data-ttu-id="51c71-638">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-639">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-639"></span></span>|
|<span data-ttu-id="51c71-640">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-641">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-641"></span></span>|
|<span data-ttu-id="51c71-642">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-643">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-643"></span></span>|
|<span data-ttu-id="51c71-644">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-645">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-645"></span></span>|
|<span data-ttu-id="51c71-646">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-647">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-647"></span></span>|
|<span data-ttu-id="51c71-648">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-648">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-649">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-649"></span></span>|
|<span data-ttu-id="51c71-650">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-651">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-651"></span></span>|
   
 <span data-ttu-id="51c71-652">**Confier l’autorité de Certification - L1K**</span><span class="sxs-lookup"><span data-stu-id="51c71-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-653">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-653">**Subject**</span></span>|
|<span data-ttu-id="51c71-654">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-654"></span></span>|
|<span data-ttu-id="51c71-655">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-655">**Issuer**</span></span>|
|<span data-ttu-id="51c71-656">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-656"></span></span>|
|<span data-ttu-id="51c71-657">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-657">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-658">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-658"></span></span>|
|<span data-ttu-id="51c71-659">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-659">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-660">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-660"></span></span>|
|<span data-ttu-id="51c71-661">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-662">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-662"></span></span>|
|<span data-ttu-id="51c71-663">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-664">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-664"></span></span>|
|<span data-ttu-id="51c71-665">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-665">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-666">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-666"></span></span>|
|<span data-ttu-id="51c71-667">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-668">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-668"></span></span>|
|<span data-ttu-id="51c71-669">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-670">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-670"></span></span>|
|<span data-ttu-id="51c71-671">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-672">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-672"></span></span>|
|<span data-ttu-id="51c71-673">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-674">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-674"></span></span>|
|<span data-ttu-id="51c71-675">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-676">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-676"></span></span>|
|<span data-ttu-id="51c71-677">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-677">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-678">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-678"></span></span>|
|<span data-ttu-id="51c71-679">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-680">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-680"></span></span>|
   
 <span data-ttu-id="51c71-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="51c71-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-682">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-682">**Subject**</span></span>|
|<span data-ttu-id="51c71-683">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-683"></span></span>|
|<span data-ttu-id="51c71-684">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-684">**Issuer**</span></span>|
|<span data-ttu-id="51c71-685">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-685"></span></span>|
|<span data-ttu-id="51c71-686">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-686">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-687">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-687"></span></span>|
|<span data-ttu-id="51c71-688">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-688">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-689">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-689"></span></span>|
|<span data-ttu-id="51c71-690">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-691">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-691"></span></span>|
|<span data-ttu-id="51c71-692">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-693">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-693"></span></span>|
|<span data-ttu-id="51c71-694">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-694">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-695">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-695"></span></span>|
|<span data-ttu-id="51c71-696">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-697">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-697"></span></span>|
|<span data-ttu-id="51c71-698">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-699">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-699"></span></span>|
|<span data-ttu-id="51c71-700">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-701">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-701"></span></span>|
|<span data-ttu-id="51c71-702">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-703">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-703"></span></span>|
|<span data-ttu-id="51c71-704">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-705">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-705"></span></span>|
|<span data-ttu-id="51c71-706">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-706">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-707">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-707"></span></span>|
|<span data-ttu-id="51c71-708">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-709">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-709"></span></span>|
   
 <span data-ttu-id="51c71-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="51c71-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-711">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-711">**Subject**</span></span>|
|<span data-ttu-id="51c71-712">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-712"></span></span>|
|<span data-ttu-id="51c71-713">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-713">**Issuer**</span></span>|
|<span data-ttu-id="51c71-714">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-714"></span></span>|
|<span data-ttu-id="51c71-715">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-715">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-716">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-716"></span></span>|
|<span data-ttu-id="51c71-717">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-717">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-718">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-718"></span></span>|
|<span data-ttu-id="51c71-719">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-720">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-720"></span></span>|
|<span data-ttu-id="51c71-721">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-722">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-722"></span></span>|
|<span data-ttu-id="51c71-723">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-723">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-724">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-724"></span></span>|
|<span data-ttu-id="51c71-725">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-726">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-726"></span></span>|
|<span data-ttu-id="51c71-727">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-728">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-728"></span></span>|
|<span data-ttu-id="51c71-729">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-730">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-730"></span></span>|
|<span data-ttu-id="51c71-731">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-732">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-732"></span></span>|
|<span data-ttu-id="51c71-733">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-734">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-734"></span></span>|
|<span data-ttu-id="51c71-735">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-735">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-736">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-736"></span></span>|
|<span data-ttu-id="51c71-737">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-738">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-738"></span></span>|
   
 <span data-ttu-id="51c71-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span><span class="sxs-lookup"><span data-stu-id="51c71-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-740">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-740">**Subject**</span></span>|
|<span data-ttu-id="51c71-741">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-741"></span></span>|
|<span data-ttu-id="51c71-742">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-742">**Issuer**</span></span>|
|<span data-ttu-id="51c71-743">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-743"></span></span>|
|<span data-ttu-id="51c71-744">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-744">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-745">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-745"></span></span>|
|<span data-ttu-id="51c71-746">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-746">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-747">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-747"></span></span>|
|<span data-ttu-id="51c71-748">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-749">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-749"></span></span>|
|<span data-ttu-id="51c71-750">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-751">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-751"></span></span>|
|<span data-ttu-id="51c71-752">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-752">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-753">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-753"></span></span>|
|<span data-ttu-id="51c71-754">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-755">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-755"></span></span>|
|<span data-ttu-id="51c71-756">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-757">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-757"></span></span>|
|<span data-ttu-id="51c71-758">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-759">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-759"></span></span>|
|<span data-ttu-id="51c71-760">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-761">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-761"></span></span>|
|<span data-ttu-id="51c71-762">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-763">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-763"></span></span>|
|<span data-ttu-id="51c71-764">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-764">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-765">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-765"></span></span>|
|<span data-ttu-id="51c71-766">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-767">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-767"></span></span>|
   
 <span data-ttu-id="51c71-768">**GlobalSign organisation Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="51c71-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-769">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-769">**Subject**</span></span>|
|<span data-ttu-id="51c71-770">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-770"></span></span>|
|<span data-ttu-id="51c71-771">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-771">**Issuer**</span></span>|
|<span data-ttu-id="51c71-772">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-772"></span></span>|
|<span data-ttu-id="51c71-773">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-773">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-774">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-774"></span></span>|
|<span data-ttu-id="51c71-775">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-775">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-776">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-776"></span></span>|
|<span data-ttu-id="51c71-777">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-778">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-778"></span></span>|
|<span data-ttu-id="51c71-779">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-780">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-780"></span></span>|
|<span data-ttu-id="51c71-781">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-781">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-782">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-782"></span></span>|
|<span data-ttu-id="51c71-783">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-784">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-784"></span></span>|
|<span data-ttu-id="51c71-785">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-786">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-786"></span></span>|
|<span data-ttu-id="51c71-787">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-788">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-788"></span></span>|
|<span data-ttu-id="51c71-789">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-790">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-790"></span></span>|
|<span data-ttu-id="51c71-791">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-792">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-792"></span></span>|
|<span data-ttu-id="51c71-793">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-793">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-794">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-794"></span></span>|
|<span data-ttu-id="51c71-795">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-796">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-796"></span></span>|
   
 <span data-ttu-id="51c71-797">**GlobalSign organisation Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="51c71-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-798">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-798">**Subject**</span></span>|
|<span data-ttu-id="51c71-799">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-799"></span></span>|
|<span data-ttu-id="51c71-800">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-800">**Issuer**</span></span>|
|<span data-ttu-id="51c71-801">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-801"></span></span>|
|<span data-ttu-id="51c71-802">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-802">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-803">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-803"></span></span>|
|<span data-ttu-id="51c71-804">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-804">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-805">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-805"></span></span>|
|<span data-ttu-id="51c71-806">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-807">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-807"></span></span>|
|<span data-ttu-id="51c71-808">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-809">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-809"></span></span>|
|<span data-ttu-id="51c71-810">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-810">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-811">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-811"></span></span>|
|<span data-ttu-id="51c71-812">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-813">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-813"></span></span>|
|<span data-ttu-id="51c71-814">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-815">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-815"></span></span>|
|<span data-ttu-id="51c71-816">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-817">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-817"></span></span>|
|<span data-ttu-id="51c71-818">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-819">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-819"></span></span>|
|<span data-ttu-id="51c71-820">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-821">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-821"></span></span>|
|<span data-ttu-id="51c71-822">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-822">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-823">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-823"></span></span>|
|<span data-ttu-id="51c71-824">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-825">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-825"></span></span>|
   
 <span data-ttu-id="51c71-826">**Nous allons chiffrer autorité X3**</span><span class="sxs-lookup"><span data-stu-id="51c71-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-827">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-827">**Subject**</span></span>|
|<span data-ttu-id="51c71-828">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-828"></span></span>|
|<span data-ttu-id="51c71-829">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-829">**Issuer**</span></span>|
|<span data-ttu-id="51c71-830">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-830"></span></span>|
|<span data-ttu-id="51c71-831">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-831">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-832">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-832"></span></span>|
|<span data-ttu-id="51c71-833">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-833">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-834">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-834"></span></span>|
|<span data-ttu-id="51c71-835">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-836">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-836"></span></span>|
|<span data-ttu-id="51c71-837">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-838">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-838"></span></span>|
|<span data-ttu-id="51c71-839">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-839">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-840">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-840"></span></span>|
|<span data-ttu-id="51c71-841">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-842">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-842"></span></span>|
|<span data-ttu-id="51c71-843">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-844">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-844"></span></span>|
|<span data-ttu-id="51c71-845">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-846">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-846"></span></span>|
|<span data-ttu-id="51c71-847">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-848">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-848"></span></span>|
|<span data-ttu-id="51c71-849">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-850">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-850"></span></span>|
|<span data-ttu-id="51c71-851">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="51c71-851">**AIA URLs**</span></span>|
|<span data-ttu-id="51c71-852">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-852"></span></span>|
|<span data-ttu-id="51c71-853">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-853">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-854">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-854"></span></span>|
|<span data-ttu-id="51c71-855">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-856">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-856"></span></span>|
   
 <span data-ttu-id="51c71-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="51c71-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-858">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-858">**Subject**</span></span>|
|<span data-ttu-id="51c71-859">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-859"></span></span>|
|<span data-ttu-id="51c71-860">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-860">**Issuer**</span></span>|
|<span data-ttu-id="51c71-861">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-861"></span></span>|
|<span data-ttu-id="51c71-862">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-862">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-863">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-863"></span></span>|
|<span data-ttu-id="51c71-864">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-864">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-865">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-865"></span></span>|
|<span data-ttu-id="51c71-866">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-867">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-867"></span></span>|
|<span data-ttu-id="51c71-868">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-869">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-869"></span></span>|
|<span data-ttu-id="51c71-870">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-870">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-871">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-871"></span></span>|
|<span data-ttu-id="51c71-872">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-873">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-873"></span></span>|
|<span data-ttu-id="51c71-874">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-875">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-875"></span></span>|
|<span data-ttu-id="51c71-876">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-877">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-877"></span></span>|
|<span data-ttu-id="51c71-878">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-879">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-879"></span></span>|
|<span data-ttu-id="51c71-880">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-881">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-881"></span></span>|
|<span data-ttu-id="51c71-882">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-882">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-883">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-883"></span></span>|
   
 <span data-ttu-id="51c71-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="51c71-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-885">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-885">**Subject**</span></span>|
|<span data-ttu-id="51c71-886">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-886"></span></span>|
|<span data-ttu-id="51c71-887">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-887">**Issuer**</span></span>|
|<span data-ttu-id="51c71-888">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-888"></span></span>|
|<span data-ttu-id="51c71-889">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-889">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-890">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-890"></span></span>|
|<span data-ttu-id="51c71-891">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-891">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-892">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-892"></span></span>|
|<span data-ttu-id="51c71-893">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-894">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-894"></span></span>|
|<span data-ttu-id="51c71-895">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-896">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-896"></span></span>|
|<span data-ttu-id="51c71-897">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-897">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-898">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-898"></span></span>|
|<span data-ttu-id="51c71-899">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-900">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-900"></span></span>|
|<span data-ttu-id="51c71-901">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-902">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-902"></span></span>|
|<span data-ttu-id="51c71-903">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-904">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-904"></span></span>|
|<span data-ttu-id="51c71-905">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-906">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-906"></span></span>|
|<span data-ttu-id="51c71-907">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-908">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-908"></span></span>|
|<span data-ttu-id="51c71-909">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-909">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-910">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-910"></span></span>|
|<span data-ttu-id="51c71-911">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-912">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-912"></span></span>|
   
 <span data-ttu-id="51c71-913">**Autorité de certification Microsoft IT TLS 1**</span><span class="sxs-lookup"><span data-stu-id="51c71-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-914">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-914">**Subject**</span></span>|
|<span data-ttu-id="51c71-915">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-915"></span></span>|
|<span data-ttu-id="51c71-916">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-916">**Issuer**</span></span>|
|<span data-ttu-id="51c71-917">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-917"></span></span>|
|<span data-ttu-id="51c71-918">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-918">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-919">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-919"></span></span>|
|<span data-ttu-id="51c71-920">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-920">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-921">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-921"></span></span>|
|<span data-ttu-id="51c71-922">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-923">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-923"></span></span>|
|<span data-ttu-id="51c71-924">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-925">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-925"></span></span>|
|<span data-ttu-id="51c71-926">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-926">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-927">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-927"></span></span>|
|<span data-ttu-id="51c71-928">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-929">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-929"></span></span>|
|<span data-ttu-id="51c71-930">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-931">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-931"></span></span>|
|<span data-ttu-id="51c71-932">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-933">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-933"></span></span>|
|<span data-ttu-id="51c71-934">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-935">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-935"></span></span>|
|<span data-ttu-id="51c71-936">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-937">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-937"></span></span>|
|<span data-ttu-id="51c71-938">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-938">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-939">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-939"></span></span>|
|<span data-ttu-id="51c71-940">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-941">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-941"></span></span>|
   
 <span data-ttu-id="51c71-942">**Autorité de certification Microsoft IT TLS 2**</span><span class="sxs-lookup"><span data-stu-id="51c71-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-943">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-943">**Subject**</span></span>|
|<span data-ttu-id="51c71-944">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-944"></span></span>|
|<span data-ttu-id="51c71-945">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-945">**Issuer**</span></span>|
|<span data-ttu-id="51c71-946">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-946"></span></span>|
|<span data-ttu-id="51c71-947">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-947">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-948">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-948"></span></span>|
|<span data-ttu-id="51c71-949">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-949">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-950">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-950"></span></span>|
|<span data-ttu-id="51c71-951">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-952">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-952"></span></span>|
|<span data-ttu-id="51c71-953">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-954">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-954"></span></span>|
|<span data-ttu-id="51c71-955">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-955">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-956">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-956"></span></span>|
|<span data-ttu-id="51c71-957">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-958">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-958"></span></span>|
|<span data-ttu-id="51c71-959">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-960">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-960"></span></span>|
|<span data-ttu-id="51c71-961">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-962">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-962"></span></span>|
|<span data-ttu-id="51c71-963">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-964">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-964"></span></span>|
|<span data-ttu-id="51c71-965">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-966">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-966"></span></span>|
|<span data-ttu-id="51c71-967">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-967">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-968">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-968"></span></span>|
|<span data-ttu-id="51c71-969">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-970">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-970"></span></span>|
   
 <span data-ttu-id="51c71-971">**Autorité de certification Microsoft IT TLS 4**</span><span class="sxs-lookup"><span data-stu-id="51c71-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-972">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-972">**Subject**</span></span>|
|<span data-ttu-id="51c71-973">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-973"></span></span>|
|<span data-ttu-id="51c71-974">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-974">**Issuer**</span></span>|
|<span data-ttu-id="51c71-975">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-975"></span></span>|
|<span data-ttu-id="51c71-976">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-976">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-977">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-977"></span></span>|
|<span data-ttu-id="51c71-978">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-978">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-979">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-979"></span></span>|
|<span data-ttu-id="51c71-980">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-981">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-981"></span></span>|
|<span data-ttu-id="51c71-982">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-983">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-983"></span></span>|
|<span data-ttu-id="51c71-984">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-984">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-985">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-985"></span></span>|
|<span data-ttu-id="51c71-986">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-987">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-987"></span></span>|
|<span data-ttu-id="51c71-988">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-989">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-989"></span></span>|
|<span data-ttu-id="51c71-990">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-991">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-991"></span></span>|
|<span data-ttu-id="51c71-992">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-993">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-993"></span></span>|
|<span data-ttu-id="51c71-994">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-995">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-995"></span></span>|
|<span data-ttu-id="51c71-996">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-996">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-997">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-997"></span></span>|
|<span data-ttu-id="51c71-998">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-999">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-999"></span></span>|
   
 <span data-ttu-id="51c71-1000">**Autorité de certification Microsoft IT TLS 5**</span><span class="sxs-lookup"><span data-stu-id="51c71-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-1001">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1001">**Subject**</span></span>|
|<span data-ttu-id="51c71-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1002"></span></span>|
|<span data-ttu-id="51c71-1003">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-1003">**Issuer**</span></span>|
|<span data-ttu-id="51c71-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1004"></span></span>|
|<span data-ttu-id="51c71-1005">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-1005">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1006"></span></span>|
|<span data-ttu-id="51c71-1007">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1008"></span></span>|
|<span data-ttu-id="51c71-1009">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1010"></span></span>|
|<span data-ttu-id="51c71-1011">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1012"></span></span>|
|<span data-ttu-id="51c71-1013">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1014"></span></span>|
|<span data-ttu-id="51c71-1015">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1016"></span></span>|
|<span data-ttu-id="51c71-1017">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1018"></span></span>|
|<span data-ttu-id="51c71-1019">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1020"></span></span>|
|<span data-ttu-id="51c71-1021">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1022"></span></span>|
|<span data-ttu-id="51c71-1023">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1024"></span></span>|
|<span data-ttu-id="51c71-1025">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1026"></span></span>|
|<span data-ttu-id="51c71-1027">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1028"></span></span>|
   
 <span data-ttu-id="51c71-1029">**Classe Symantec EV 3 SSL CA - G3**</span><span class="sxs-lookup"><span data-stu-id="51c71-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-1030">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1030">**Subject**</span></span>|
|<span data-ttu-id="51c71-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1031"></span></span>|
|<span data-ttu-id="51c71-1032">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-1032">**Issuer**</span></span>|
|<span data-ttu-id="51c71-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1033"></span></span>|
|<span data-ttu-id="51c71-1034">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="51c71-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1035"></span></span>|
|<span data-ttu-id="51c71-1036">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-1036">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1037"></span></span>|
|<span data-ttu-id="51c71-1038">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1039"></span></span>|
|<span data-ttu-id="51c71-1040">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1041"></span></span>|
|<span data-ttu-id="51c71-1042">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1043"></span></span>|
|<span data-ttu-id="51c71-1044">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1045"></span></span>|
|<span data-ttu-id="51c71-1046">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1047"></span></span>|
|<span data-ttu-id="51c71-1048">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1049"></span></span>|
|<span data-ttu-id="51c71-1050">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1051"></span></span>|
|<span data-ttu-id="51c71-1052">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1053"></span></span>|
|<span data-ttu-id="51c71-1054">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1055"></span></span>|
|<span data-ttu-id="51c71-1056">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1057"></span></span>|
|<span data-ttu-id="51c71-1058">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1059"></span></span>|
   
 <span data-ttu-id="51c71-1060">**Serveur sécurisé Symantec classe 3 CA - G4**</span><span class="sxs-lookup"><span data-stu-id="51c71-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-1061">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1061">**Subject**</span></span>|
|<span data-ttu-id="51c71-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1062"></span></span>|
|<span data-ttu-id="51c71-1063">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-1063">**Issuer**</span></span>|
|<span data-ttu-id="51c71-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1064"></span></span>|
|<span data-ttu-id="51c71-1065">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="51c71-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1066"></span></span>|
|<span data-ttu-id="51c71-1067">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-1067">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1068"></span></span>|
|<span data-ttu-id="51c71-1069">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1070"></span></span>|
|<span data-ttu-id="51c71-1071">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1072"></span></span>|
|<span data-ttu-id="51c71-1073">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1074"></span></span>|
|<span data-ttu-id="51c71-1075">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1076"></span></span>|
|<span data-ttu-id="51c71-1077">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1078"></span></span>|
|<span data-ttu-id="51c71-1079">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1080"></span></span>|
|<span data-ttu-id="51c71-1081">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1082"></span></span>|
|<span data-ttu-id="51c71-1083">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1084"></span></span>|
|<span data-ttu-id="51c71-1085">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1086"></span></span>|
|<span data-ttu-id="51c71-1087">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1088"></span></span>|
|<span data-ttu-id="51c71-1089">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1090"></span></span>|
   
 <span data-ttu-id="51c71-1091">**Thawte SHA256 SSL autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="51c71-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-1092">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1092">**Subject**</span></span>|
|<span data-ttu-id="51c71-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1093"></span></span>|
|<span data-ttu-id="51c71-1094">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-1094">**Issuer**</span></span>|
|<span data-ttu-id="51c71-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1095"></span></span>|
|<span data-ttu-id="51c71-1096">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="51c71-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1097"></span></span>|
|<span data-ttu-id="51c71-1098">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-1098">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1099"></span></span>|
|<span data-ttu-id="51c71-1100">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1101"></span></span>|
|<span data-ttu-id="51c71-1102">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1103"></span></span>|
|<span data-ttu-id="51c71-1104">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1105"></span></span>|
|<span data-ttu-id="51c71-1106">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1107"></span></span>|
|<span data-ttu-id="51c71-1108">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1109"></span></span>|
|<span data-ttu-id="51c71-1110">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1111"></span></span>|
|<span data-ttu-id="51c71-1112">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1113"></span></span>|
|<span data-ttu-id="51c71-1114">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1115"></span></span>|
|<span data-ttu-id="51c71-1116">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1117"></span></span>|
|<span data-ttu-id="51c71-1118">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1119"></span></span>|
|<span data-ttu-id="51c71-1120">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1121"></span></span>|
   
 <span data-ttu-id="51c71-1122">**Autorité de certification SureServer de Verizon Akamai G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="51c71-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="51c71-1123">**Objet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1123">**Subject**</span></span>|
|<span data-ttu-id="51c71-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1124"></span></span>|
|<span data-ttu-id="51c71-1125">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="51c71-1125">**Issuer**</span></span>|
|<span data-ttu-id="51c71-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1126"></span></span>|
|<span data-ttu-id="51c71-1127">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="51c71-1127">**Serial Number**</span></span>|
|<span data-ttu-id="51c71-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1128"></span></span>|
|<span data-ttu-id="51c71-1129">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="51c71-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="51c71-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1130"></span></span>|
|<span data-ttu-id="51c71-1131">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="51c71-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="51c71-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1132"></span></span>|
|<span data-ttu-id="51c71-1133">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="51c71-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="51c71-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1134"></span></span>|
|<span data-ttu-id="51c71-1135">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="51c71-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="51c71-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1136"></span></span>|
|<span data-ttu-id="51c71-1137">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="51c71-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1138"></span></span>|
|<span data-ttu-id="51c71-1139">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="51c71-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="51c71-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1140"></span></span>|
|<span data-ttu-id="51c71-1141">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="51c71-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1142"></span></span>|
|<span data-ttu-id="51c71-1143">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1144"></span></span>|
|<span data-ttu-id="51c71-1145">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="51c71-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="51c71-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1146"></span></span>|
|<span data-ttu-id="51c71-1147">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="51c71-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="51c71-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1148"></span></span>|
|<span data-ttu-id="51c71-1149">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="51c71-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="51c71-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1150"></span></span>|
|<span data-ttu-id="51c71-1151">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="51c71-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="51c71-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="51c71-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="51c71-1153">Chemins d’accès du certificat supplémentaire</span><span class="sxs-lookup"><span data-stu-id="51c71-1153">Additional certificate paths</span></span>
<span data-ttu-id="51c71-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="51c71-1154"></span></span>

<span data-ttu-id="51c71-1155">Les éléments suivants sont hérités certificats qui ne sont pas incluses ci-dessus et sont fusionnées avec la liste ci-dessus au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="51c71-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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


