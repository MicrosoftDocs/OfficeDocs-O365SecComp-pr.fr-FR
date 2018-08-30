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
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527985"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="88539-106">Chaînes de certificats d’Office 365</span><span class="sxs-lookup"><span data-stu-id="88539-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="88539-p102">Office 365 utilise un certain nombre de fournisseurs de certificat différent. Voici la liste complète des certificats racines Office 365 connus que les clients peuvent rencontrer lors de l’accès à Office 365. Pour plus d’informations sur les certificats que vous devrez peut-être installer dans votre propre infrastructure, voir [planifier les certificats SSL de tiers pour Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Les informations de certificat suivantes s’applique à toutes les instances de cloud dans le monde entier et national d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="88539-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="88539-111">**Type de certificat**</span><span class="sxs-lookup"><span data-stu-id="88539-111">**Certificate type**</span></span>|<span data-ttu-id="88539-112">**Téléchargement P7b**</span><span class="sxs-lookup"><span data-stu-id="88539-112">**P7b download**</span></span>|<span data-ttu-id="88539-113">**Points de terminaison de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-113">**CRL Endpoints**</span></span>|<span data-ttu-id="88539-114">**Points de terminaison OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="88539-115">**Points de terminaison AIA**</span><span class="sxs-lookup"><span data-stu-id="88539-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="88539-116">Certificats racine de confiance publiquement</span><span class="sxs-lookup"><span data-stu-id="88539-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="88539-117">Groupement de certificat racine Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="88539-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="88539-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="88539-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="88539-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="88539-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="88539-120">N/D</span><span class="sxs-lookup"><span data-stu-id="88539-120">N/A</span></span>  <br/> |<span data-ttu-id="88539-121">S/O</span><span class="sxs-lookup"><span data-stu-id="88539-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="88539-122">Approuvés publiquement certificats intermédiaires</span><span class="sxs-lookup"><span data-stu-id="88539-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="88539-123">Groupement de certificats intermédiaires d’Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="88539-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="88539-124">cdp1.public-trust.com</span><span class="sxs-lookup"><span data-stu-id="88539-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="88539-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="88539-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="88539-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="88539-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="88539-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="88539-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="88539-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="88539-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="88539-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="88539-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="88539-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="88539-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="88539-131">crl3.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="88539-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="88539-132">crl4.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="88539-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="88539-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="88539-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="88539-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="88539-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="88539-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="88539-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="88539-136">OCSP.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="88539-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="88539-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="88539-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="88539-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="88539-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="88539-139">OCSP.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="88539-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="88539-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="88539-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="88539-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="88539-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="88539-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="88539-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="88539-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="88539-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="88539-144">racine-c3-2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="88539-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="88539-145">root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="88539-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="88539-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="88539-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="88539-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="88539-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="88539-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="88539-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="88539-149">cacert.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="88539-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="88539-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="88539-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="88539-151">Développez les sections intermédiaires ci-dessous pour afficher des détails supplémentaires sur les fournisseurs de certificat racine.</span><span class="sxs-lookup"><span data-stu-id="88539-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="88539-152">Détails du certificat racine Office 365</span><span class="sxs-lookup"><span data-stu-id="88539-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="88539-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="88539-153"></span></span>

 <span data-ttu-id="88539-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="88539-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="88539-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="88539-155">|:-----|</span></span>
|<span data-ttu-id="88539-156">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="88539-157">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-157">**Serial Number**</span></span>|
|<span data-ttu-id="88539-158">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-158"></span></span>|
|<span data-ttu-id="88539-159">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-159">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-160">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-160"></span></span>|
|<span data-ttu-id="88539-161">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-162">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-162"></span></span>|
|<span data-ttu-id="88539-163">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-164">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-164"></span></span>|
|<span data-ttu-id="88539-165">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-165">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-166">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-166"></span></span>|
|<span data-ttu-id="88539-167">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-168">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-168"></span></span>|
|<span data-ttu-id="88539-169">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-170">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-170"></span></span>|
|<span data-ttu-id="88539-171">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-172">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-172"></span></span>|
|<span data-ttu-id="88539-173">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-174">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-174"></span></span>|
   
 <span data-ttu-id="88539-175">**RACINE CNNIC**</span><span class="sxs-lookup"><span data-stu-id="88539-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-176">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-176">**Subject**</span></span>|
|<span data-ttu-id="88539-177">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-177"></span></span>|
|<span data-ttu-id="88539-178">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-178">**Serial Number**</span></span>|
|<span data-ttu-id="88539-179">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-179"></span></span>|
|<span data-ttu-id="88539-180">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-180">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-181">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-181"></span></span>|
|<span data-ttu-id="88539-182">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-183">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-183"></span></span>|
|<span data-ttu-id="88539-184">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-185">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-185"></span></span>|
|<span data-ttu-id="88539-186">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-186">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-187">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-187"></span></span>|
|<span data-ttu-id="88539-188">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-189">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-189"></span></span>|
|<span data-ttu-id="88539-190">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-191">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-191"></span></span>|
|<span data-ttu-id="88539-192">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-193">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-193"></span></span>|
|<span data-ttu-id="88539-194">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-195">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-195"></span></span>|
|<span data-ttu-id="88539-196">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-197">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-197"></span></span>|
   
 <span data-ttu-id="88539-198">**Autorité de certification racine globale DigiCert**</span><span class="sxs-lookup"><span data-stu-id="88539-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-199">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-199">**Subject**</span></span>|
|<span data-ttu-id="88539-200">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-200"></span></span>|
|<span data-ttu-id="88539-201">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-201">**Serial Number**</span></span>|
|<span data-ttu-id="88539-202">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-202"></span></span>|
|<span data-ttu-id="88539-203">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-203">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-204">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-204"></span></span>|
|<span data-ttu-id="88539-205">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-206">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-206"></span></span>|
|<span data-ttu-id="88539-207">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-208">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-208"></span></span>|
|<span data-ttu-id="88539-209">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-209">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-210">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-210"></span></span>|
|<span data-ttu-id="88539-211">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-212">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-212"></span></span>|
|<span data-ttu-id="88539-213">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-214">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-214"></span></span>|
|<span data-ttu-id="88539-215">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-216">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-216"></span></span>|
|<span data-ttu-id="88539-217">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-218">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-218"></span></span>|
|<span data-ttu-id="88539-219">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-220">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-220"></span></span>|
   
 <span data-ttu-id="88539-221">**Autorité de certification racine DigiCert High Assurance EV**</span><span class="sxs-lookup"><span data-stu-id="88539-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-222">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-222">**Subject**</span></span>|
|<span data-ttu-id="88539-223">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-223"></span></span>|
|<span data-ttu-id="88539-224">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-224">**Serial Number**</span></span>|
|<span data-ttu-id="88539-225">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-225"></span></span>|
|<span data-ttu-id="88539-226">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-226">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-227">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-227"></span></span>|
|<span data-ttu-id="88539-228">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-229">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-229"></span></span>|
|<span data-ttu-id="88539-230">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-231">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-231"></span></span>|
|<span data-ttu-id="88539-232">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-232">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-233">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-233"></span></span>|
|<span data-ttu-id="88539-234">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-235">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-235"></span></span>|
|<span data-ttu-id="88539-236">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-237">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-237"></span></span>|
|<span data-ttu-id="88539-238">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-239">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-239"></span></span>|
|<span data-ttu-id="88539-240">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-241">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-241"></span></span>|
|<span data-ttu-id="88539-242">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-243">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-243"></span></span>|
   
 <span data-ttu-id="88539-244">**Autorité de certification racine de confiance D classe 3 2 2009**</span><span class="sxs-lookup"><span data-stu-id="88539-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-245">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-245">**Subject**</span></span>|
|<span data-ttu-id="88539-246">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-246"></span></span>|
|<span data-ttu-id="88539-247">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-247">**Serial Number**</span></span>|
|<span data-ttu-id="88539-248">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-248"></span></span>|
|<span data-ttu-id="88539-249">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-249">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-250">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-250"></span></span>|
|<span data-ttu-id="88539-251">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-252">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-252"></span></span>|
|<span data-ttu-id="88539-253">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-254">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-254"></span></span>|
|<span data-ttu-id="88539-255">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-255">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-256">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-256"></span></span>|
|<span data-ttu-id="88539-257">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-258">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-258"></span></span>|
|<span data-ttu-id="88539-259">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-260">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-260"></span></span>|
|<span data-ttu-id="88539-261">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-262">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-262"></span></span>|
|<span data-ttu-id="88539-263">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-264">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-264"></span></span>|
|<span data-ttu-id="88539-265">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-265">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-266">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-266"></span></span>|
   
 <span data-ttu-id="88539-267">**Autorité de certification racine de confiance D classe 3 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="88539-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-268">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-268">**Subject**</span></span>|
|<span data-ttu-id="88539-269">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-269"></span></span>|
|<span data-ttu-id="88539-270">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-270">**Serial Number**</span></span>|
|<span data-ttu-id="88539-271">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-271"></span></span>|
|<span data-ttu-id="88539-272">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-272">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-273">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-273"></span></span>|
|<span data-ttu-id="88539-274">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-275">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-275"></span></span>|
|<span data-ttu-id="88539-276">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-277">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-277"></span></span>|
|<span data-ttu-id="88539-278">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-278">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-279">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-279"></span></span>|
|<span data-ttu-id="88539-280">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-281">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-281"></span></span>|
|<span data-ttu-id="88539-282">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-283">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-283"></span></span>|
|<span data-ttu-id="88539-284">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-285">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-285"></span></span>|
|<span data-ttu-id="88539-286">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-287">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-287"></span></span>|
|<span data-ttu-id="88539-288">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-288">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-289">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-289"></span></span>|
   
 <span data-ttu-id="88539-290">**Racine de l’heure d’été X3 de l’autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="88539-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-291">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-291">**Subject**</span></span>|
|<span data-ttu-id="88539-292">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-292"></span></span>|
|<span data-ttu-id="88539-293">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-293">**Serial Number**</span></span>|
|<span data-ttu-id="88539-294">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-294"></span></span>|
|<span data-ttu-id="88539-295">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-295">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-296">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-296"></span></span>|
|<span data-ttu-id="88539-297">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-298">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-298"></span></span>|
|<span data-ttu-id="88539-299">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-300">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-300"></span></span>|
|<span data-ttu-id="88539-301">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-301">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-302">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-302"></span></span>|
|<span data-ttu-id="88539-303">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-304">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-304"></span></span>|
|<span data-ttu-id="88539-305">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-306">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-306"></span></span>|
|<span data-ttu-id="88539-307">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-308">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-308"></span></span>|
|<span data-ttu-id="88539-309">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-310">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-310"></span></span>|
   
 <span data-ttu-id="88539-311">**Confier autorité de Certification racine - G2**</span><span class="sxs-lookup"><span data-stu-id="88539-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-312">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-312">**Subject**</span></span>|
|<span data-ttu-id="88539-313">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-313"></span></span>|
|<span data-ttu-id="88539-314">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-314">**Serial Number**</span></span>|
|<span data-ttu-id="88539-315">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-315"></span></span>|
|<span data-ttu-id="88539-316">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-316">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-317">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-317"></span></span>|
|<span data-ttu-id="88539-318">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-319">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-319"></span></span>|
|<span data-ttu-id="88539-320">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-321">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-321"></span></span>|
|<span data-ttu-id="88539-322">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-322">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-323">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-323"></span></span>|
|<span data-ttu-id="88539-324">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-325">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-325"></span></span>|
|<span data-ttu-id="88539-326">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-327">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-327"></span></span>|
|<span data-ttu-id="88539-328">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-329">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-329"></span></span>|
|<span data-ttu-id="88539-330">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-331">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-331"></span></span>|
   
 <span data-ttu-id="88539-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="88539-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-333">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-333">**Subject**</span></span>|
|<span data-ttu-id="88539-334">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-334"></span></span>|
|<span data-ttu-id="88539-335">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-335">**Serial Number**</span></span>|
|<span data-ttu-id="88539-336">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-336"></span></span>|
|<span data-ttu-id="88539-337">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-337">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-338">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-338"></span></span>|
|<span data-ttu-id="88539-339">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-340">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-340"></span></span>|
|<span data-ttu-id="88539-341">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-342">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-342"></span></span>|
|<span data-ttu-id="88539-343">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-343">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-344">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-344"></span></span>|
|<span data-ttu-id="88539-345">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-346">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-346"></span></span>|
|<span data-ttu-id="88539-347">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-348">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-348"></span></span>|
|<span data-ttu-id="88539-349">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-350">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-350"></span></span>|
|<span data-ttu-id="88539-351">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-352">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-352"></span></span>|
   
 <span data-ttu-id="88539-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="88539-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-354">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-354">**Subject**</span></span>|
|<span data-ttu-id="88539-355">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-355"></span></span>|
|<span data-ttu-id="88539-356">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-356">**Serial Number**</span></span>|
|<span data-ttu-id="88539-357">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-357"></span></span>|
|<span data-ttu-id="88539-358">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-358">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-359">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-359"></span></span>|
|<span data-ttu-id="88539-360">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-361">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-361"></span></span>|
|<span data-ttu-id="88539-362">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-363">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-363"></span></span>|
|<span data-ttu-id="88539-364">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-364">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-365">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-365"></span></span>|
|<span data-ttu-id="88539-366">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-367">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-367"></span></span>|
|<span data-ttu-id="88539-368">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-369">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-369"></span></span>|
|<span data-ttu-id="88539-370">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-371">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-371"></span></span>|
|<span data-ttu-id="88539-372">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-373">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-373"></span></span>|
|<span data-ttu-id="88539-374">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-375">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-375"></span></span>|
|<span data-ttu-id="88539-376">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-376">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-377">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-377"></span></span>|
   
 <span data-ttu-id="88539-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="88539-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-379">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-379">**Subject**</span></span>|
|<span data-ttu-id="88539-380">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-380"></span></span>|
|<span data-ttu-id="88539-381">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-381">**Serial Number**</span></span>|
|<span data-ttu-id="88539-382">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-382"></span></span>|
|<span data-ttu-id="88539-383">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-383">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-384">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-384"></span></span>|
|<span data-ttu-id="88539-385">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-386">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-386"></span></span>|
|<span data-ttu-id="88539-387">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-388">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-388"></span></span>|
|<span data-ttu-id="88539-389">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-389">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-390">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-390"></span></span>|
|<span data-ttu-id="88539-391">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-392">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-392"></span></span>|
|<span data-ttu-id="88539-393">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-394">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-394"></span></span>|
|<span data-ttu-id="88539-395">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-396">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-396"></span></span>|
|<span data-ttu-id="88539-397">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-398">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-398"></span></span>|
   
 <span data-ttu-id="88539-399">**Thawte autorité de certification racine principal - G3**</span><span class="sxs-lookup"><span data-stu-id="88539-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-400">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-400">**Subject**</span></span>|
|<span data-ttu-id="88539-401">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-401"></span></span>|
|<span data-ttu-id="88539-402">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-402">**Serial Number**</span></span>|
|<span data-ttu-id="88539-403">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-403"></span></span>|
|<span data-ttu-id="88539-404">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-404">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-405">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-405"></span></span>|
|<span data-ttu-id="88539-406">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-407">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-407"></span></span>|
|<span data-ttu-id="88539-408">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-409">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-409"></span></span>|
|<span data-ttu-id="88539-410">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-410">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-411">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-411"></span></span>|
|<span data-ttu-id="88539-412">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-413">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-413"></span></span>|
|<span data-ttu-id="88539-414">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-415">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-415"></span></span>|
|<span data-ttu-id="88539-416">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-417">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-417"></span></span>|
|<span data-ttu-id="88539-418">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-419">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-419"></span></span>|
   
 <span data-ttu-id="88539-420">**Autorité de Certification publique principale VeriSign de classe 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="88539-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-421">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-421">**Subject**</span></span>|
|<span data-ttu-id="88539-422">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-422"></span></span>|
|<span data-ttu-id="88539-423">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-423">**Serial Number**</span></span>|
|<span data-ttu-id="88539-424">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-424"></span></span>|
|<span data-ttu-id="88539-425">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-425">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-426">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-426"></span></span>|
|<span data-ttu-id="88539-427">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-428">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-428"></span></span>|
|<span data-ttu-id="88539-429">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-430">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-430"></span></span>|
|<span data-ttu-id="88539-431">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-431">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-432">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-432"></span></span>|
|<span data-ttu-id="88539-433">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-434">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-434"></span></span>|
|<span data-ttu-id="88539-435">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-436">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-436"></span></span>|
|<span data-ttu-id="88539-437">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-438">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-438"></span></span>|
|<span data-ttu-id="88539-439">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-440">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="88539-441">Détails du certificat intermédiaire Office 365</span><span class="sxs-lookup"><span data-stu-id="88539-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="88539-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="88539-442"></span></span>

 <span data-ttu-id="88539-443">**SHA256 CNNIC SSL**</span><span class="sxs-lookup"><span data-stu-id="88539-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-444">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-444">**Subject**</span></span>|
|<span data-ttu-id="88539-445">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-445"></span></span>|
|<span data-ttu-id="88539-446">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-446">**Issuer**</span></span>|
|<span data-ttu-id="88539-447">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-447"></span></span>|
|<span data-ttu-id="88539-448">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-448">**Serial Number**</span></span>|
|<span data-ttu-id="88539-449">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-449"></span></span>|
|<span data-ttu-id="88539-450">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-450">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-451">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-451"></span></span>|
|<span data-ttu-id="88539-452">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-453">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-453"></span></span>|
|<span data-ttu-id="88539-454">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-455">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-455"></span></span>|
|<span data-ttu-id="88539-456">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-456">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-457">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-457"></span></span>|
|<span data-ttu-id="88539-458">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-459">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-459"></span></span>|
|<span data-ttu-id="88539-460">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-461">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-461"></span></span>|
|<span data-ttu-id="88539-462">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-463">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-463"></span></span>|
|<span data-ttu-id="88539-464">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-465">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-465"></span></span>|
|<span data-ttu-id="88539-466">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-467">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-467"></span></span>|
|<span data-ttu-id="88539-468">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="88539-468">**AIA URLs**</span></span>|
|<span data-ttu-id="88539-469">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-469"></span></span>|
|<span data-ttu-id="88539-470">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-470">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-471">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-471"></span></span>|
|<span data-ttu-id="88539-472">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-473">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-473"></span></span>|
   
 <span data-ttu-id="88539-474">**Autorité de certification de classe 3 D-TRUST SSL 1 2009**</span><span class="sxs-lookup"><span data-stu-id="88539-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-475">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-475">**Subject**</span></span>|
|<span data-ttu-id="88539-476">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-476"></span></span>|
|<span data-ttu-id="88539-477">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-477">**Issuer**</span></span>|
|<span data-ttu-id="88539-478">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-478"></span></span>|
|<span data-ttu-id="88539-479">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="88539-480">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-480"></span></span>|
|<span data-ttu-id="88539-481">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-481">**Serial Number**</span></span>|
|<span data-ttu-id="88539-482">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-482"></span></span>|
|<span data-ttu-id="88539-483">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-483">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-484">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-484"></span></span>|
|<span data-ttu-id="88539-485">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-486">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-486"></span></span>|
|<span data-ttu-id="88539-487">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-488">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-488"></span></span>|
|<span data-ttu-id="88539-489">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-489">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-490">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-490"></span></span>|
|<span data-ttu-id="88539-491">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-492">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-492"></span></span>|
|<span data-ttu-id="88539-493">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-494">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-494"></span></span>|
|<span data-ttu-id="88539-495">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-496">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-496"></span></span>|
|<span data-ttu-id="88539-497">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-498">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-498"></span></span>|
|<span data-ttu-id="88539-499">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-500">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-500"></span></span>|
|<span data-ttu-id="88539-501">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-501">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-502">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-502"></span></span>|
|<span data-ttu-id="88539-503">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-504">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-504"></span></span>|
   
 <span data-ttu-id="88539-505">**Autorité de certification de classe 3 D-TRUST SSL 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="88539-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-506">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-506">**Subject**</span></span>|
|<span data-ttu-id="88539-507">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-507"></span></span>|
|<span data-ttu-id="88539-508">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-508">**Issuer**</span></span>|
|<span data-ttu-id="88539-509">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-509"></span></span>|
|<span data-ttu-id="88539-510">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="88539-511">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-511"></span></span>|
|<span data-ttu-id="88539-512">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-512">**Serial Number**</span></span>|
|<span data-ttu-id="88539-513">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-513"></span></span>|
|<span data-ttu-id="88539-514">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-514">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-515">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-515"></span></span>|
|<span data-ttu-id="88539-516">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-517">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-517"></span></span>|
|<span data-ttu-id="88539-518">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-519">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-519"></span></span>|
|<span data-ttu-id="88539-520">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-520">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-521">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-521"></span></span>|
|<span data-ttu-id="88539-522">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-523">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-523"></span></span>|
|<span data-ttu-id="88539-524">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-525">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-525"></span></span>|
|<span data-ttu-id="88539-526">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-527">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-527"></span></span>|
|<span data-ttu-id="88539-528">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-529">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-529"></span></span>|
|<span data-ttu-id="88539-530">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-531">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-531"></span></span>|
|<span data-ttu-id="88539-532">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-532">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-533">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-533"></span></span>|
|<span data-ttu-id="88539-534">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-535">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-535"></span></span>|
   
 <span data-ttu-id="88539-536">**DigiCert Cloud Services CA-1**</span><span class="sxs-lookup"><span data-stu-id="88539-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-537">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-537">**Subject**</span></span>|
|<span data-ttu-id="88539-538">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-538"></span></span>|
|<span data-ttu-id="88539-539">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-539">**Issuer**</span></span>|
|<span data-ttu-id="88539-540">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-540"></span></span>|
|<span data-ttu-id="88539-541">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-541">**Serial Number**</span></span>|
|<span data-ttu-id="88539-542">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-542"></span></span>|
|<span data-ttu-id="88539-543">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-543">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-544">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-544"></span></span>|
|<span data-ttu-id="88539-545">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-546">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-546"></span></span>|
|<span data-ttu-id="88539-547">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-548">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-548"></span></span>|
|<span data-ttu-id="88539-549">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-549">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-550">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-550"></span></span>|
|<span data-ttu-id="88539-551">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-552">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-552"></span></span>|
|<span data-ttu-id="88539-553">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-554">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-554"></span></span>|
|<span data-ttu-id="88539-555">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-556">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-556"></span></span>|
|<span data-ttu-id="88539-557">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-558">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-558"></span></span>|
|<span data-ttu-id="88539-559">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-560">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-560"></span></span>|
|<span data-ttu-id="88539-561">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-561">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-562">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-562"></span></span>|
|<span data-ttu-id="88539-563">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-564">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-564"></span></span>|
   
 <span data-ttu-id="88539-565">**DigiCert SHA2 High Assurance Server autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="88539-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-566">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-566">**Subject**</span></span>|
|<span data-ttu-id="88539-567">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-567"></span></span>|
|<span data-ttu-id="88539-568">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-568">**Issuer**</span></span>|
|<span data-ttu-id="88539-569">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-569"></span></span>|
|<span data-ttu-id="88539-570">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-570">**Serial Number**</span></span>|
|<span data-ttu-id="88539-571">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-571"></span></span>|
|<span data-ttu-id="88539-572">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-572">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-573">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-573"></span></span>|
|<span data-ttu-id="88539-574">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-575">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-575"></span></span>|
|<span data-ttu-id="88539-576">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-577">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-577"></span></span>|
|<span data-ttu-id="88539-578">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-578">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-579">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-579"></span></span>|
|<span data-ttu-id="88539-580">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-581">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-581"></span></span>|
|<span data-ttu-id="88539-582">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-583">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-583"></span></span>|
|<span data-ttu-id="88539-584">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-585">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-585"></span></span>|
|<span data-ttu-id="88539-586">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-587">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-587"></span></span>|
|<span data-ttu-id="88539-588">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-589">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-589"></span></span>|
|<span data-ttu-id="88539-590">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-590">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-591">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-591"></span></span>|
|<span data-ttu-id="88539-592">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-593">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-593"></span></span>|
   
 <span data-ttu-id="88539-594">**Serveur sécurisé DigiCert SHA2 autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="88539-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-595">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-595">**Subject**</span></span>|
|<span data-ttu-id="88539-596">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-596"></span></span>|
|<span data-ttu-id="88539-597">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-597">**Issuer**</span></span>|
|<span data-ttu-id="88539-598">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-598"></span></span>|
|<span data-ttu-id="88539-599">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-599">**Serial Number**</span></span>|
|<span data-ttu-id="88539-600">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-600"></span></span>|
|<span data-ttu-id="88539-601">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-601">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-602">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-602"></span></span>|
|<span data-ttu-id="88539-603">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-604">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-604"></span></span>|
|<span data-ttu-id="88539-605">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-606">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-606"></span></span>|
|<span data-ttu-id="88539-607">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-607">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-608">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-608"></span></span>|
|<span data-ttu-id="88539-609">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-610">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-610"></span></span>|
|<span data-ttu-id="88539-611">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-612">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-612"></span></span>|
|<span data-ttu-id="88539-613">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-614">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-614"></span></span>|
|<span data-ttu-id="88539-615">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-616">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-616"></span></span>|
|<span data-ttu-id="88539-617">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-618">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-618"></span></span>|
|<span data-ttu-id="88539-619">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-619">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-620">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-620"></span></span>|
|<span data-ttu-id="88539-621">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-622">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-622"></span></span>|
   
 <span data-ttu-id="88539-623">**Confier l’autorité de Certification - L1C**</span><span class="sxs-lookup"><span data-stu-id="88539-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-624">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-624">**Subject**</span></span>|
|<span data-ttu-id="88539-625">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-625"></span></span>|
|<span data-ttu-id="88539-626">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-626">**Issuer**</span></span>|
|<span data-ttu-id="88539-627">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-627"></span></span>|
|<span data-ttu-id="88539-628">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-628">**Serial Number**</span></span>|
|<span data-ttu-id="88539-629">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-629"></span></span>|
|<span data-ttu-id="88539-630">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-630">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-631">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-631"></span></span>|
|<span data-ttu-id="88539-632">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-633">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-633"></span></span>|
|<span data-ttu-id="88539-634">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-635">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-635"></span></span>|
|<span data-ttu-id="88539-636">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-636">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-637">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-637"></span></span>|
|<span data-ttu-id="88539-638">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-639">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-639"></span></span>|
|<span data-ttu-id="88539-640">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-641">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-641"></span></span>|
|<span data-ttu-id="88539-642">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-643">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-643"></span></span>|
|<span data-ttu-id="88539-644">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-645">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-645"></span></span>|
|<span data-ttu-id="88539-646">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-647">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-647"></span></span>|
|<span data-ttu-id="88539-648">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-648">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-649">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-649"></span></span>|
|<span data-ttu-id="88539-650">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-651">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-651"></span></span>|
   
 <span data-ttu-id="88539-652">**Confier l’autorité de Certification - L1K**</span><span class="sxs-lookup"><span data-stu-id="88539-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-653">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-653">**Subject**</span></span>|
|<span data-ttu-id="88539-654">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-654"></span></span>|
|<span data-ttu-id="88539-655">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-655">**Issuer**</span></span>|
|<span data-ttu-id="88539-656">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-656"></span></span>|
|<span data-ttu-id="88539-657">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-657">**Serial Number**</span></span>|
|<span data-ttu-id="88539-658">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-658"></span></span>|
|<span data-ttu-id="88539-659">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-659">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-660">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-660"></span></span>|
|<span data-ttu-id="88539-661">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-662">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-662"></span></span>|
|<span data-ttu-id="88539-663">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-664">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-664"></span></span>|
|<span data-ttu-id="88539-665">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-665">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-666">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-666"></span></span>|
|<span data-ttu-id="88539-667">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-668">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-668"></span></span>|
|<span data-ttu-id="88539-669">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-670">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-670"></span></span>|
|<span data-ttu-id="88539-671">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-672">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-672"></span></span>|
|<span data-ttu-id="88539-673">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-674">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-674"></span></span>|
|<span data-ttu-id="88539-675">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-676">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-676"></span></span>|
|<span data-ttu-id="88539-677">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-677">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-678">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-678"></span></span>|
|<span data-ttu-id="88539-679">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-680">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-680"></span></span>|
   
 <span data-ttu-id="88539-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="88539-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-682">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-682">**Subject**</span></span>|
|<span data-ttu-id="88539-683">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-683"></span></span>|
|<span data-ttu-id="88539-684">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-684">**Issuer**</span></span>|
|<span data-ttu-id="88539-685">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-685"></span></span>|
|<span data-ttu-id="88539-686">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-686">**Serial Number**</span></span>|
|<span data-ttu-id="88539-687">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-687"></span></span>|
|<span data-ttu-id="88539-688">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-688">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-689">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-689"></span></span>|
|<span data-ttu-id="88539-690">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-691">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-691"></span></span>|
|<span data-ttu-id="88539-692">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-693">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-693"></span></span>|
|<span data-ttu-id="88539-694">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-694">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-695">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-695"></span></span>|
|<span data-ttu-id="88539-696">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-697">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-697"></span></span>|
|<span data-ttu-id="88539-698">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-699">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-699"></span></span>|
|<span data-ttu-id="88539-700">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-701">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-701"></span></span>|
|<span data-ttu-id="88539-702">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-703">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-703"></span></span>|
|<span data-ttu-id="88539-704">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-705">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-705"></span></span>|
|<span data-ttu-id="88539-706">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-706">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-707">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-707"></span></span>|
|<span data-ttu-id="88539-708">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-709">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-709"></span></span>|
   
 <span data-ttu-id="88539-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="88539-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-711">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-711">**Subject**</span></span>|
|<span data-ttu-id="88539-712">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-712"></span></span>|
|<span data-ttu-id="88539-713">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-713">**Issuer**</span></span>|
|<span data-ttu-id="88539-714">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-714"></span></span>|
|<span data-ttu-id="88539-715">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-715">**Serial Number**</span></span>|
|<span data-ttu-id="88539-716">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-716"></span></span>|
|<span data-ttu-id="88539-717">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-717">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-718">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-718"></span></span>|
|<span data-ttu-id="88539-719">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-720">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-720"></span></span>|
|<span data-ttu-id="88539-721">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-722">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-722"></span></span>|
|<span data-ttu-id="88539-723">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-723">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-724">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-724"></span></span>|
|<span data-ttu-id="88539-725">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-726">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-726"></span></span>|
|<span data-ttu-id="88539-727">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-728">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-728"></span></span>|
|<span data-ttu-id="88539-729">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-730">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-730"></span></span>|
|<span data-ttu-id="88539-731">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-732">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-732"></span></span>|
|<span data-ttu-id="88539-733">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-734">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-734"></span></span>|
|<span data-ttu-id="88539-735">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-735">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-736">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-736"></span></span>|
|<span data-ttu-id="88539-737">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-738">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-738"></span></span>|
   
 <span data-ttu-id="88539-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span><span class="sxs-lookup"><span data-stu-id="88539-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-740">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-740">**Subject**</span></span>|
|<span data-ttu-id="88539-741">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-741"></span></span>|
|<span data-ttu-id="88539-742">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-742">**Issuer**</span></span>|
|<span data-ttu-id="88539-743">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-743"></span></span>|
|<span data-ttu-id="88539-744">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-744">**Serial Number**</span></span>|
|<span data-ttu-id="88539-745">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-745"></span></span>|
|<span data-ttu-id="88539-746">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-746">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-747">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-747"></span></span>|
|<span data-ttu-id="88539-748">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-749">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-749"></span></span>|
|<span data-ttu-id="88539-750">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-751">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-751"></span></span>|
|<span data-ttu-id="88539-752">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-752">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-753">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-753"></span></span>|
|<span data-ttu-id="88539-754">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-755">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-755"></span></span>|
|<span data-ttu-id="88539-756">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-757">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-757"></span></span>|
|<span data-ttu-id="88539-758">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-759">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-759"></span></span>|
|<span data-ttu-id="88539-760">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-761">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-761"></span></span>|
|<span data-ttu-id="88539-762">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-763">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-763"></span></span>|
|<span data-ttu-id="88539-764">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-764">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-765">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-765"></span></span>|
|<span data-ttu-id="88539-766">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-767">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-767"></span></span>|
   
 <span data-ttu-id="88539-768">**GlobalSign organisation Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="88539-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-769">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-769">**Subject**</span></span>|
|<span data-ttu-id="88539-770">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-770"></span></span>|
|<span data-ttu-id="88539-771">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-771">**Issuer**</span></span>|
|<span data-ttu-id="88539-772">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-772"></span></span>|
|<span data-ttu-id="88539-773">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-773">**Serial Number**</span></span>|
|<span data-ttu-id="88539-774">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-774"></span></span>|
|<span data-ttu-id="88539-775">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-775">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-776">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-776"></span></span>|
|<span data-ttu-id="88539-777">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-778">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-778"></span></span>|
|<span data-ttu-id="88539-779">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-780">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-780"></span></span>|
|<span data-ttu-id="88539-781">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-781">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-782">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-782"></span></span>|
|<span data-ttu-id="88539-783">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-784">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-784"></span></span>|
|<span data-ttu-id="88539-785">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-786">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-786"></span></span>|
|<span data-ttu-id="88539-787">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-788">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-788"></span></span>|
|<span data-ttu-id="88539-789">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-790">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-790"></span></span>|
|<span data-ttu-id="88539-791">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-792">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-792"></span></span>|
|<span data-ttu-id="88539-793">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-793">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-794">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-794"></span></span>|
|<span data-ttu-id="88539-795">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-796">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-796"></span></span>|
   
 <span data-ttu-id="88539-797">**GlobalSign organisation Validation CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="88539-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-798">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-798">**Subject**</span></span>|
|<span data-ttu-id="88539-799">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-799"></span></span>|
|<span data-ttu-id="88539-800">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-800">**Issuer**</span></span>|
|<span data-ttu-id="88539-801">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-801"></span></span>|
|<span data-ttu-id="88539-802">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-802">**Serial Number**</span></span>|
|<span data-ttu-id="88539-803">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-803"></span></span>|
|<span data-ttu-id="88539-804">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-804">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-805">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-805"></span></span>|
|<span data-ttu-id="88539-806">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-807">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-807"></span></span>|
|<span data-ttu-id="88539-808">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-809">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-809"></span></span>|
|<span data-ttu-id="88539-810">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-810">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-811">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-811"></span></span>|
|<span data-ttu-id="88539-812">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-813">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-813"></span></span>|
|<span data-ttu-id="88539-814">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-815">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-815"></span></span>|
|<span data-ttu-id="88539-816">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-817">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-817"></span></span>|
|<span data-ttu-id="88539-818">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-819">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-819"></span></span>|
|<span data-ttu-id="88539-820">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-821">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-821"></span></span>|
|<span data-ttu-id="88539-822">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-822">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-823">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-823"></span></span>|
|<span data-ttu-id="88539-824">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-825">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-825"></span></span>|
   
 <span data-ttu-id="88539-826">**Nous allons chiffrer autorité X3**</span><span class="sxs-lookup"><span data-stu-id="88539-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-827">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-827">**Subject**</span></span>|
|<span data-ttu-id="88539-828">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-828"></span></span>|
|<span data-ttu-id="88539-829">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-829">**Issuer**</span></span>|
|<span data-ttu-id="88539-830">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-830"></span></span>|
|<span data-ttu-id="88539-831">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-831">**Serial Number**</span></span>|
|<span data-ttu-id="88539-832">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-832"></span></span>|
|<span data-ttu-id="88539-833">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-833">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-834">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-834"></span></span>|
|<span data-ttu-id="88539-835">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-836">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-836"></span></span>|
|<span data-ttu-id="88539-837">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-838">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-838"></span></span>|
|<span data-ttu-id="88539-839">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-839">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-840">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-840"></span></span>|
|<span data-ttu-id="88539-841">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-842">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-842"></span></span>|
|<span data-ttu-id="88539-843">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-844">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-844"></span></span>|
|<span data-ttu-id="88539-845">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-846">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-846"></span></span>|
|<span data-ttu-id="88539-847">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-848">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-848"></span></span>|
|<span data-ttu-id="88539-849">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-850">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-850"></span></span>|
|<span data-ttu-id="88539-851">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="88539-851">**AIA URLs**</span></span>|
|<span data-ttu-id="88539-852">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-852"></span></span>|
|<span data-ttu-id="88539-853">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-853">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-854">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-854"></span></span>|
|<span data-ttu-id="88539-855">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-856">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-856"></span></span>|
   
 <span data-ttu-id="88539-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="88539-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-858">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-858">**Subject**</span></span>|
|<span data-ttu-id="88539-859">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-859"></span></span>|
|<span data-ttu-id="88539-860">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-860">**Issuer**</span></span>|
|<span data-ttu-id="88539-861">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-861"></span></span>|
|<span data-ttu-id="88539-862">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-862">**Serial Number**</span></span>|
|<span data-ttu-id="88539-863">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-863"></span></span>|
|<span data-ttu-id="88539-864">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-864">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-865">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-865"></span></span>|
|<span data-ttu-id="88539-866">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-867">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-867"></span></span>|
|<span data-ttu-id="88539-868">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-869">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-869"></span></span>|
|<span data-ttu-id="88539-870">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-870">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-871">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-871"></span></span>|
|<span data-ttu-id="88539-872">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-873">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-873"></span></span>|
|<span data-ttu-id="88539-874">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-875">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-875"></span></span>|
|<span data-ttu-id="88539-876">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-877">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-877"></span></span>|
|<span data-ttu-id="88539-878">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-879">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-879"></span></span>|
|<span data-ttu-id="88539-880">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-881">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-881"></span></span>|
|<span data-ttu-id="88539-882">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-882">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-883">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-883"></span></span>|
   
 <span data-ttu-id="88539-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="88539-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-885">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-885">**Subject**</span></span>|
|<span data-ttu-id="88539-886">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-886"></span></span>|
|<span data-ttu-id="88539-887">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-887">**Issuer**</span></span>|
|<span data-ttu-id="88539-888">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-888"></span></span>|
|<span data-ttu-id="88539-889">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-889">**Serial Number**</span></span>|
|<span data-ttu-id="88539-890">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-890"></span></span>|
|<span data-ttu-id="88539-891">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-891">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-892">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-892"></span></span>|
|<span data-ttu-id="88539-893">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-894">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-894"></span></span>|
|<span data-ttu-id="88539-895">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-896">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-896"></span></span>|
|<span data-ttu-id="88539-897">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-897">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-898">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-898"></span></span>|
|<span data-ttu-id="88539-899">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-900">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-900"></span></span>|
|<span data-ttu-id="88539-901">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-902">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-902"></span></span>|
|<span data-ttu-id="88539-903">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-904">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-904"></span></span>|
|<span data-ttu-id="88539-905">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-906">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-906"></span></span>|
|<span data-ttu-id="88539-907">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-908">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-908"></span></span>|
|<span data-ttu-id="88539-909">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-909">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-910">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-910"></span></span>|
|<span data-ttu-id="88539-911">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-912">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-912"></span></span>|
   
 <span data-ttu-id="88539-913">**Autorité de certification Microsoft IT TLS 1**</span><span class="sxs-lookup"><span data-stu-id="88539-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-914">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-914">**Subject**</span></span>|
|<span data-ttu-id="88539-915">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-915"></span></span>|
|<span data-ttu-id="88539-916">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-916">**Issuer**</span></span>|
|<span data-ttu-id="88539-917">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-917"></span></span>|
|<span data-ttu-id="88539-918">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-918">**Serial Number**</span></span>|
|<span data-ttu-id="88539-919">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-919"></span></span>|
|<span data-ttu-id="88539-920">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-920">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-921">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-921"></span></span>|
|<span data-ttu-id="88539-922">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-923">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-923"></span></span>|
|<span data-ttu-id="88539-924">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-925">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-925"></span></span>|
|<span data-ttu-id="88539-926">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-926">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-927">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-927"></span></span>|
|<span data-ttu-id="88539-928">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-929">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-929"></span></span>|
|<span data-ttu-id="88539-930">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-931">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-931"></span></span>|
|<span data-ttu-id="88539-932">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-933">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-933"></span></span>|
|<span data-ttu-id="88539-934">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-935">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-935"></span></span>|
|<span data-ttu-id="88539-936">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-937">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-937"></span></span>|
|<span data-ttu-id="88539-938">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-938">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-939">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-939"></span></span>|
|<span data-ttu-id="88539-940">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-941">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-941"></span></span>|
   
 <span data-ttu-id="88539-942">**Autorité de certification Microsoft IT TLS 2**</span><span class="sxs-lookup"><span data-stu-id="88539-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-943">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-943">**Subject**</span></span>|
|<span data-ttu-id="88539-944">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-944"></span></span>|
|<span data-ttu-id="88539-945">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-945">**Issuer**</span></span>|
|<span data-ttu-id="88539-946">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-946"></span></span>|
|<span data-ttu-id="88539-947">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-947">**Serial Number**</span></span>|
|<span data-ttu-id="88539-948">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-948"></span></span>|
|<span data-ttu-id="88539-949">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-949">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-950">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-950"></span></span>|
|<span data-ttu-id="88539-951">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-952">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-952"></span></span>|
|<span data-ttu-id="88539-953">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-954">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-954"></span></span>|
|<span data-ttu-id="88539-955">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-955">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-956">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-956"></span></span>|
|<span data-ttu-id="88539-957">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-958">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-958"></span></span>|
|<span data-ttu-id="88539-959">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-960">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-960"></span></span>|
|<span data-ttu-id="88539-961">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-962">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-962"></span></span>|
|<span data-ttu-id="88539-963">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-964">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-964"></span></span>|
|<span data-ttu-id="88539-965">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-966">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-966"></span></span>|
|<span data-ttu-id="88539-967">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-967">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-968">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-968"></span></span>|
|<span data-ttu-id="88539-969">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-970">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-970"></span></span>|
   
 <span data-ttu-id="88539-971">**Autorité de certification Microsoft IT TLS 4**</span><span class="sxs-lookup"><span data-stu-id="88539-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-972">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-972">**Subject**</span></span>|
|<span data-ttu-id="88539-973">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-973"></span></span>|
|<span data-ttu-id="88539-974">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-974">**Issuer**</span></span>|
|<span data-ttu-id="88539-975">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-975"></span></span>|
|<span data-ttu-id="88539-976">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-976">**Serial Number**</span></span>|
|<span data-ttu-id="88539-977">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-977"></span></span>|
|<span data-ttu-id="88539-978">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-978">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-979">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-979"></span></span>|
|<span data-ttu-id="88539-980">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-981">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-981"></span></span>|
|<span data-ttu-id="88539-982">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-983">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-983"></span></span>|
|<span data-ttu-id="88539-984">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-984">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-985">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-985"></span></span>|
|<span data-ttu-id="88539-986">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-987">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-987"></span></span>|
|<span data-ttu-id="88539-988">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-989">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-989"></span></span>|
|<span data-ttu-id="88539-990">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-991">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-991"></span></span>|
|<span data-ttu-id="88539-992">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-993">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-993"></span></span>|
|<span data-ttu-id="88539-994">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-995">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-995"></span></span>|
|<span data-ttu-id="88539-996">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-996">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-997">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-997"></span></span>|
|<span data-ttu-id="88539-998">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-999">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-999"></span></span>|
   
 <span data-ttu-id="88539-1000">**Autorité de certification Microsoft IT TLS 5**</span><span class="sxs-lookup"><span data-stu-id="88539-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-1001">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-1001">**Subject**</span></span>|
|<span data-ttu-id="88539-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1002"></span></span>|
|<span data-ttu-id="88539-1003">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-1003">**Issuer**</span></span>|
|<span data-ttu-id="88539-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1004"></span></span>|
|<span data-ttu-id="88539-1005">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-1005">**Serial Number**</span></span>|
|<span data-ttu-id="88539-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1006"></span></span>|
|<span data-ttu-id="88539-1007">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1008"></span></span>|
|<span data-ttu-id="88539-1009">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1010"></span></span>|
|<span data-ttu-id="88539-1011">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1012"></span></span>|
|<span data-ttu-id="88539-1013">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1014"></span></span>|
|<span data-ttu-id="88539-1015">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1016"></span></span>|
|<span data-ttu-id="88539-1017">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1018"></span></span>|
|<span data-ttu-id="88539-1019">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1020"></span></span>|
|<span data-ttu-id="88539-1021">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1022"></span></span>|
|<span data-ttu-id="88539-1023">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1024"></span></span>|
|<span data-ttu-id="88539-1025">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1026"></span></span>|
|<span data-ttu-id="88539-1027">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1028"></span></span>|
   
 <span data-ttu-id="88539-1029">**Classe Symantec EV 3 SSL CA - G3**</span><span class="sxs-lookup"><span data-stu-id="88539-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-1030">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-1030">**Subject**</span></span>|
|<span data-ttu-id="88539-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1031"></span></span>|
|<span data-ttu-id="88539-1032">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-1032">**Issuer**</span></span>|
|<span data-ttu-id="88539-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1033"></span></span>|
|<span data-ttu-id="88539-1034">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="88539-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1035"></span></span>|
|<span data-ttu-id="88539-1036">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-1036">**Serial Number**</span></span>|
|<span data-ttu-id="88539-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1037"></span></span>|
|<span data-ttu-id="88539-1038">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1039"></span></span>|
|<span data-ttu-id="88539-1040">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1041"></span></span>|
|<span data-ttu-id="88539-1042">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1043"></span></span>|
|<span data-ttu-id="88539-1044">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1045"></span></span>|
|<span data-ttu-id="88539-1046">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1047"></span></span>|
|<span data-ttu-id="88539-1048">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1049"></span></span>|
|<span data-ttu-id="88539-1050">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1051"></span></span>|
|<span data-ttu-id="88539-1052">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1053"></span></span>|
|<span data-ttu-id="88539-1054">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1055"></span></span>|
|<span data-ttu-id="88539-1056">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1057"></span></span>|
|<span data-ttu-id="88539-1058">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1059"></span></span>|
   
 <span data-ttu-id="88539-1060">**Serveur sécurisé Symantec classe 3 CA - G4**</span><span class="sxs-lookup"><span data-stu-id="88539-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-1061">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-1061">**Subject**</span></span>|
|<span data-ttu-id="88539-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1062"></span></span>|
|<span data-ttu-id="88539-1063">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-1063">**Issuer**</span></span>|
|<span data-ttu-id="88539-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1064"></span></span>|
|<span data-ttu-id="88539-1065">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="88539-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1066"></span></span>|
|<span data-ttu-id="88539-1067">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-1067">**Serial Number**</span></span>|
|<span data-ttu-id="88539-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1068"></span></span>|
|<span data-ttu-id="88539-1069">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1070"></span></span>|
|<span data-ttu-id="88539-1071">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1072"></span></span>|
|<span data-ttu-id="88539-1073">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1074"></span></span>|
|<span data-ttu-id="88539-1075">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1076"></span></span>|
|<span data-ttu-id="88539-1077">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1078"></span></span>|
|<span data-ttu-id="88539-1079">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1080"></span></span>|
|<span data-ttu-id="88539-1081">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1082"></span></span>|
|<span data-ttu-id="88539-1083">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1084"></span></span>|
|<span data-ttu-id="88539-1085">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1086"></span></span>|
|<span data-ttu-id="88539-1087">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1088"></span></span>|
|<span data-ttu-id="88539-1089">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1090"></span></span>|
   
 <span data-ttu-id="88539-1091">**Thawte SHA256 SSL autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="88539-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-1092">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-1092">**Subject**</span></span>|
|<span data-ttu-id="88539-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1093"></span></span>|
|<span data-ttu-id="88539-1094">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-1094">**Issuer**</span></span>|
|<span data-ttu-id="88539-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1095"></span></span>|
|<span data-ttu-id="88539-1096">**Nom du sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="88539-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1097"></span></span>|
|<span data-ttu-id="88539-1098">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-1098">**Serial Number**</span></span>|
|<span data-ttu-id="88539-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1099"></span></span>|
|<span data-ttu-id="88539-1100">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1101"></span></span>|
|<span data-ttu-id="88539-1102">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1103"></span></span>|
|<span data-ttu-id="88539-1104">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1105"></span></span>|
|<span data-ttu-id="88539-1106">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1107"></span></span>|
|<span data-ttu-id="88539-1108">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1109"></span></span>|
|<span data-ttu-id="88539-1110">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1111"></span></span>|
|<span data-ttu-id="88539-1112">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1113"></span></span>|
|<span data-ttu-id="88539-1114">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1115"></span></span>|
|<span data-ttu-id="88539-1116">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1117"></span></span>|
|<span data-ttu-id="88539-1118">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1119"></span></span>|
|<span data-ttu-id="88539-1120">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1121"></span></span>|
   
 <span data-ttu-id="88539-1122">**Autorité de certification SureServer de Verizon Akamai G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="88539-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="88539-1123">**Objet**</span><span class="sxs-lookup"><span data-stu-id="88539-1123">**Subject**</span></span>|
|<span data-ttu-id="88539-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1124"></span></span>|
|<span data-ttu-id="88539-1125">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="88539-1125">**Issuer**</span></span>|
|<span data-ttu-id="88539-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1126"></span></span>|
|<span data-ttu-id="88539-1127">**Numéro de série**</span><span class="sxs-lookup"><span data-stu-id="88539-1127">**Serial Number**</span></span>|
|<span data-ttu-id="88539-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1128"></span></span>|
|<span data-ttu-id="88539-1129">**Longueur de clé publique**</span><span class="sxs-lookup"><span data-stu-id="88539-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="88539-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1130"></span></span>|
|<span data-ttu-id="88539-1131">**Algorithme de signature**</span><span class="sxs-lookup"><span data-stu-id="88539-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="88539-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1132"></span></span>|
|<span data-ttu-id="88539-1133">**Validité pas avant**</span><span class="sxs-lookup"><span data-stu-id="88539-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="88539-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1134"></span></span>|
|<span data-ttu-id="88539-1135">**Validité pas après**</span><span class="sxs-lookup"><span data-stu-id="88539-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="88539-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1136"></span></span>|
|<span data-ttu-id="88539-1137">**Identificateur de clé sujet**</span><span class="sxs-lookup"><span data-stu-id="88539-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="88539-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1138"></span></span>|
|<span data-ttu-id="88539-1139">**Identificateur de clé d’autorité**</span><span class="sxs-lookup"><span data-stu-id="88539-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="88539-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1140"></span></span>|
|<span data-ttu-id="88539-1141">**Empreinte numérique (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="88539-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="88539-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1142"></span></span>|
|<span data-ttu-id="88539-1143">**Empreinte numérique (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1144"></span></span>|
|<span data-ttu-id="88539-1145">**Code confidentiel (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="88539-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="88539-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1146"></span></span>|
|<span data-ttu-id="88539-1147">**URL AIA**</span><span class="sxs-lookup"><span data-stu-id="88539-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="88539-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1148"></span></span>|
|<span data-ttu-id="88539-1149">**URL de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="88539-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="88539-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1150"></span></span>|
|<span data-ttu-id="88539-1151">**URL OCSP**</span><span class="sxs-lookup"><span data-stu-id="88539-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="88539-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="88539-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="88539-1153">Chemins d’accès du certificat supplémentaire</span><span class="sxs-lookup"><span data-stu-id="88539-1153">Additional certificate paths</span></span>
<span data-ttu-id="88539-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="88539-1154"></span></span>

<span data-ttu-id="88539-1155">Les éléments suivants sont hérités certificats qui ne sont pas incluses ci-dessus et sont fusionnées avec la liste ci-dessus au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="88539-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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


