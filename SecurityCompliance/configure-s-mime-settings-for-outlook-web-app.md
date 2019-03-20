---
title: Configurer les paramètres S/MIME dans Exchange Online pour Outlook sur le Web
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: Brève description des administrateurs Exchange Online à faire pour afficher et configurer les paramètres S/MIME dans Outlook sur le Web dans Exchange Online.
ms.openlocfilehash: d890b7f39d16d8c0f3866d5ff0024fe31160af6b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693333"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a>Configurer les paramètres S/MIME dans Exchange Online pour Outlook sur le Web

En tant qu'administrateur d'Exchange Online, vous pouvez configurer Outlook sur le Web (anciennement Outlook Web App) pour permettre l'envoi et la réception de messages protégés par S/MIME. Utilisez les cmdlets **Get-SmimeConfig** et **Set-SmimeConfig** pour afficher et gérer cette fonctionnalité dans Exchange Online PowerShell. Pour vous connecter à Exchange Online PowerShell, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) et [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).

## <a name="considerations-for-chrome"></a>Considérations relatives au chrome

Pour utiliser S/MIME dans Outlook sur le Web dans le navigateur Web Google Chrome, vous (ou un autre administrateur) devez définir et configurer la stratégie de chrome nommée **ExtensionInstallForcelist** pour installer l'extension S/MIME Microsoft dans Chrome. La stratégie doit utiliser la syntaxe: `<extension-id>;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` par exemple: `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`. Et notez que l'application de cette stratégie nécessite des ordinateurs associés à un domaine, de sorte que l'utilisation de S/MIME dans Chrome requiert effectivement des ordinateurs liés à un domaine.

Cette étape est requise pour utiliser Chrome; il ne remplace pas le contrôle S/MIME qui est installé par les utilisateurs. Pour plus d'informations sur la stratégie **ExtensionInstallForcelist** , voir [ExtensionInstallForcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).

## <a name="for-more-information"></a>Pour plus d'informations

[S/MIME pour la signature et le chiffrement des messages](s-mime-for-message-signing-and-encryption.md)
