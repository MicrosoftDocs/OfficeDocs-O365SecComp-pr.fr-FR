---
title: Rétentions basées sur des événements
ms.author: stephow
author: stephow-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Cette rubrique explique comment configurer votre flux de processus métier pour automatiser la rétention via des événements à l’aide de l’API REST de Microsoft 365.
ms.openlocfilehash: c89abc373a6c0a1de6b6528c638dbd34e586b6d7
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152276"
---
# <a name="automate-event-based-retention"></a>Rétentions basées sur des événements

L’explosion de contenu dans les organisations et comment il peut devenir assistées (redondantes, obsolètes, triviale) est une affaire sérieuse. Pour continuer à répondre aux exigences légales, commerciales et défis liés à la conformité des réglementations, les entreprises doivent pouvoir conserver et protéger les informations importantes et trouver rapidement ce qui est pertinent. Conservant uniquement ce qui est important, les informations pertinentes sont la clé du succès d’une entreprise.

Les organisations peuvent donc tirer parti des solutions de rétention dans le centre de conformité et sécurité Office 365. La rétention peut être déclenchée en utilisant les[étiquettes de rétention](labels.md). Une étiquette de rétention a la possibilité de [baser la période de rétention sur un événement spécifique](event-driven-retention.md). En règle générale, la période de rétention est basée sur une date connue, comme la date ou date de dernière modification pour le contenu création. Toutefois, les organisations ont également des exigences à dispose de contenu en fonction des occurrences d’un événement, par exemple 7 ans après qu’un employé quitte une organisation.

Pour s’assurer de la conformité de la destruction de contenu, il est impératif de savoir quand un événement a lieu. Le volume du contenu en augmentant rapidement, il devient difficile à conserver et dispose du contenu d’une manière opportune et la conformité.

La rétention basée sur un événement résoud ce problème. Cette rubrique explique comment configurer votre flux de processus métier pour automatiser la rétention via des événements à l’aide de l’API REST de Microsoft 365.

## <a name="about-event-based-retention"></a>Rétentions basées sur des événements

Une organisation peut être grande petite ou moyenne. Le nombre de documents professionnels, documents juridiques, fichiers employé, contrats et documents produit qui sont créés et gérés sur une base quotidienne augmentent considérablement.

Par exemple, chaque jour, dizaines et des centaines d’employés rejoignent et quittent organisations. Le service ressources humaines continue de créer, mettre à jour ou supprimer des documents liés à l’employé en respectant les exigences professionnelles. Ce processus est susceptible d’être les stratégies de rétention différentes décrites pour l’entreprise :

- **La période de rétention du contenu peut être une date connue** telles que la date que le contenu a été créé, la dernière modification ou étiqueté. Par exemple, vous pouvez conserver les documents pendant sept ans après que qu’ils aient été créés, puis les supprimer.

- **La période de rétention du contenu peut également être une date inconnue**. Par exemple, avec des étiquettes de rétention, vous pouvez également baser une période de rétention sur lorsqu’un type spécifique d’événement se produit, par exemple un employé quittant l’organisation.

Le début de la période de rétention déclenche l’événement, et tout le contenu portant une étiquette pour ce type d’événement obtenez actions de rétention l’étiquette est appliquées dessus. Il s’agit rétention basée sur l’événement-pour plus d’informations, voir [vue d’ensemble de rétention basées sur les événements](event-driven-retention.md).

## <a name="set-up-event-based-retention"></a>Définir la rétentions basées sur des événements

Cette section décrit les activités devant être effectuées avant la conservation du contenu.

### <a name="identify-roles"></a>Identifier les rôles

Identifier les différents rôles d’une organisation qui effectuent des tâches de gestion d’enregistrement qui seraient responsables de la rétention efficace et de documents professionnels.

  | **Persona**| **Role**|
  | - | - |
  | Administrateur | Crée des types d’Événement de Rétention, Étiquettes de Rétention et Référentiels d’Enregistrement dans SharePoint |
  | Gestionnaire d’enregistrements                                  | Fournit des détails de recommandations et de conformité stratégies de rétention et des plannings de rétention   |
  | Administrateur système (entreprise)                          | Configure et gère les systèmes externes pour fonctionner avec Microsoft 365                       |
  | Travailleur de l'information                               | Gère le cycle de vie de leur processus métier (RH, Finance, etc. informatique)                 |

### <a name="set-up-the-security--compliance-center"></a>Accéder au Centre de Conformité et de Sécurité
  
1. L’administrateur de conformité crée un type d’événement : par exemple, la résiliation employé ou expiration de contrat ou fin de fabrication de produit (reportez-vous aux processus étape par étape dans l’article[rétention événement](https://docs.microsoft.com/fr-FR/office365/securitycompliance/event-driven-retention).
    
1. L’administrateur de conformité crée une étiquette en fonction d’un événement et l’associe à un type d’événement.
    
1. Il existe 4 types de déclencheurs pour les étiquettes de rétention :
            
    1. Date de création
                
    1. Dernière modification
                
    1. Date étiquette (lorsque le contenu a été étiqueté)
                
    1. Basé sur des événements
    
1. L’administrateur de conformité publie l’étiquette.

### <a name="set-up-sharepoint"></a>Configurer SharePoint
   
Pour créer un référentiel des enregistrements, l’administrateur de conformité :

1. Crée un site SharePoint.

1. Effectue les opérations suivantes :
        
    - Crée une bibliothèque SharePoint : définir l’étiquette en fonction des événement au niveau de la bibliothèque. Pour plus d’informations, voir [application d’une étiquette de rétention par défaut à tout le contenu dans une bibliothèque SharePoint, un dossier ou un ensemble de documents](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).
          
    - Configure un Document ensemble dans SharePoint. Pour plus d’informations, voir [présentation des ensembles de documents](https://support.office.com/fr-FR/article/Introduction-to-Document-Sets-3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234).
      
1. Attribue des Id de l’élément (biens QU'ID est un nom de produit ou un code utilisé par l’organisation, par exemple, la matricule peut être un id de l’élément) à chaque document employé définir (en attribuant des biens QU'ID dans le dossier, tous les éléments dans ce dossier hérite automatiquement le même ID de biens. Cela signifie que tous les éléments peuvent avoir leur période de rétention déclenchée par le même événement.

## <a name="ways-to-trigger-event-based-retention"></a>Méthodes pour déclencher la lecture rétention basée sur l’événement

Il existe deux façons avec lesquelles la rétention basée sur l’événement peut être déclenchée :

- **Utiliser l’interface utilisateur du centre de conformité** il s’agit d’un processus qui peut être utilisé pour conserver moins de contenu à la fois ou la fréquence de déclenchement de rétention n’est pas souvent, par exemple, mensuelle ou annuelle. Pour plus d’informations sur cette méthode, voir [vue d’ensemble de rétention basée sur les événements](event-driven-retention.md). Toutefois, cette méthode pour déclencher la rétention peut prendre du temps et est sujette aux erreurs, et peut donc ralentir l’évolutivité. Par conséquent, une solution automatisée plus transparente associée au déclenchement de rétention peut améliorer la sécurité et conformité des données.

- **À l’aide d’une API REST M365** Ce processus peut être utilisé lorsque les grandes quantités de contenu sont conservées à un moment et/ou la fréquence de rétention déclencheur est récurrente telle que de manière quotidienne ou hebdomadaire. Le flux détecte quand un événement se produit dans votre système métier de, puis crée automatiquement un événement connexe dans le centre de sécurité et conformité. Vous n’avez pas besoin de créer manuellement un événement dans l’interface utilisateur chaque fois que ce qui se passer.

Il existe deux options d’utilisation de l’API REST :

- **Microsoft Flow ou une application similaire** peut être utilisé(e )pour déclencher automatiquement l’occurrence d’un événement. Microsoft Flow est un orchestrateur pour la connexion à d’autres systèmes. À l’aide de Microsoft Flow ne requiert pas une solution personnalisée.

- **PowerShell ou un HTTP client pour appeler des API REST** à l’aide de PowerShell (version 6 ou version ultérieure) pour appeler l’API REST Microsoft 365 pour créer des événements. 

L’API Rest est un point de terminaison de service qui prend en charge des ensembles d’opérations HTTP (méthodes), qui fournit créer/récupération/mise à jour/supprimer l’accès aux ressources de service- pour plus d’informations, voir [composants d’une demande de l’API REST/réponse](https://docs.microsoft.com/fr-FR/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse) . Dans ce cas, les événements peuvent être créés en utilisant l’API REST de Microsoft 365 et récupérées à l’aide d’opérations (méthodes) POST et GET.

## <a name="example-scenarios"></a>Exemples de scénarios

Envisagez les scénarios suivants.

### <a name="scenario-1-employees-leaving-the-organization"></a>Scénario 1 : Employés quittant l’organisation 

Une organisation crée et stocke plusieurs documents liés à l’employé par employé. Ces documents sont gérés et conservées pendant le recrutement de chaque employé. Toutefois, lorsque l’employé quitte l’organisation ou l’emploi terminé, l’organisation est obligée par les exigences juridiques et professionnelles de conserver les documents de cet employé pendant une période prévue.

Maintenant si plusieurs employés quittent l’organisation tous les jours, l’organisation doit déclencher la lecture l’horloge de rétention de centaines si ce n’est pas de milliers de documents chaque jour.

En plus de cela, la période de rétention doit être calculée pour chacun de ces employés comme date d’achèvement employé + nombre de jours, mois ou années en fonction du type de l’employé enregistrer. Par exemple, la rémunération du travailleur de le déclarations employés et les avantages de l’employé doivent avoir différentes rétentions.

Le diagramme ci-dessous montre comment vous pouvez avoir plusieurs étiquettes qui sont associées à un événement spécifique. Tous les fichiers sous étiquette de travailleur rémunération et tous les fichiers sous étiquette avantages employé sont associés à un événement unique qui est l’employé quittant l’organisation. Chacun de ces différents fichiers doit avoir une différente horloge de rétention. Par conséquent, lorsqu’un employé quitte l’organisation, ces fichiers dans chaque étiquette rencontrent une différente période de rétention. Pour déclencher la lecture toutes ces différentes horloges de rétention pour chaque type de fichier ou une étiquette pour chaque employé est une tâche très difficile. Imaginez effectuer cette action pour plusieurs employés.

![Diagramme illustrant le type d’événement, des événements et des étiquettes](media/automate-event-driven-retention-event-diagram-employee-leaving.png)

Un processus automatisé associé au déclenchement de ces différentes horloges de rétention pour plusieurs employés sera donc un gagne-temps, exempte d’erreur et très efficace.

**Configuration automatisée de rétention basée sur des événements dans ce scénario :**

![Diagramme des rôles et des actions pour le scénario d’employé quittant l’organisation](media/automate-event-driven-retention-employee-termination-diagram.png)

  - L’administrateur crée des dossiers d’employé lié au Document, telles Cartier Marie, John Smith.

  - L’administrateur ajoute des fichiers employé tels que les avantages, paie, rémunération de travailleur à chaque dossier employé

  - L’administrateur affecte des Id de l’élément à chaque dossier employé. 

  - L SCC d’administration

  - Connexions dans le Centre de Conformité et de Sécurité

  - L’administrateur SCC crée des types d’événements liés à l’employé tels que « Renvoi employé », « Embauche employé » dans le Centre de Sécurité et Conformité.

  - Administrateur SCC crée une étiquette « Employés ».

  - Cette étiquette « Employés » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint

  - Le Système de Gestion des Ressources Humaines comme Workday peut fonctionner avec Microsoft Flow pour exécuter cette page régulièrement pour gérer les fichiers de l’employé

  - Si un employé a quitté l’organisation, le flux déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.

#### <a name="using-microsoft-flow"></a>Utilisation Microsoft Flow

Étape 1-créer un flux de créer un événement en utilisant l’API REST Microsoft 365

![Utilisation le flux pour créer un événement](media/automate-event-driven-retention-flow-1.png)

![Utilisation du flux pour appeler des API REST](media/automate-event-driven-retention-flow-2.png)

##### <a name="create-an-event"></a>Créer un événement

Utilisation du code d’exemple pour appeler des API REST

<table>
<thead>
<tr class="header">
<th>Méthode</th>
<th>POST</th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>URL</td>
<td>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent)</td>
<td></td>
</tr>
<tr class="even">
<td>En-têtes</td>
<td>Content-Type</td>
<td>application/atom+xml</td>
</tr>
<tr class="odd">
<td>Corps</td>
<td><p>&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</p>
<p>&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</p>
<p>xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</p>
<p>xmlns='http://www.w3.org/2005/Atom'&gt;</p>
<p>&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</p>
<p>&lt;mise à jour&gt;9/9/2017 22:50:00&lt;/ mis à jour&gt;</p>
<p>&lt;content type='application/xml'&gt;</p>
<p>&lt;m:properties&gt;</p>
<p>&lt;d:Name&gt;Licenciement employé&lt;/d:Name&gt;</p>
<p>&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</p>
<p>&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</p>
<p>&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</p>
<p>&lt;/m:properties&gt;</p>
<p>&lt;/contenu&gt;</p>
<p>&lt;/entrée&gt;</p></td>
<td></td>
</tr>
<tr class="even">
<td>Authentification</td>
<td>De base</td>
<td></td>
</tr>
<tr class="odd">
<td>Nom d’utilisateur</td>
<td>« Complianceuser »</td>
<td></td>
</tr>
<tr class="even">
<td>Mot de passe</td>
<td>« Compliancepassword »</td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="available-parameters"></a>Paramètres disponibles

<table>
<thead>
<tr class="header">
<th><strong>Paramètres</strong></th>
<th><strong>Description</strong></th>
<th><strong>Notes</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&lt;d:Name&gt;&lt;/d:Name&gt;</td>
<td>Entrez un nom unique pour la base de données,</td>
<td>Un nom ne peut pas contenir les espaces et les caractères suivants : % * \ &amp; &lt; &gt; | # ? , : ;</td>
</tr>
<tr class="even">
<td>&lt;d:EventType&gt;&lt;/d:EventType&gt;</td>
<td>Entrez le nom de l’événement (ou Guid),</td>
<td>Exemple : « employé licenciement anticipé ». Le type d’événement doit être associé à une étiquette de rétention.</td>
</tr>
<tr class="odd">
<td>&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</td>
<td>Entrez « ComplianceAssetId : « + Id d’employé</td>
<td>Exemple :&quot;ComplianceAssetId:12345&quot;</td>
</tr>
<tr class="even">
<td>&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</td>
<td>Date et heure de l’événement.</td>
<td><p>Format : AAAA-MM-JJThh, exemple :</p>
<p>2018-12-01T00:00:00Z</p></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a>Codes de réponse

| **Code de réponse** | **Description**       |
| ----------------- | --------------------- |
| 302               | Rediriger              |
| 201               | Créé               |
| 403               | Autorisation échouée  |
| 401               | Message d’échec d’authentification |

##### <a name="get-events-based-on-time-range"></a>Obtenir des événements en fonction de l’intervalle de temps

<table>
<thead>
<tr class="header">
<th>Méthode</th>
<th>GET</th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>URL</td>
<td><ol start="4" type="1">
<li><p>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</p></li>
</ol></td>
<td></td>
</tr>
<tr class="even">
<td>En-têtes</td>
<td>Content-Type</td>
<td>application/atom+xml</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Authentification</td>
<td>De base</td>
<td></td>
</tr>
<tr class="odd">
<td>Nom d’utilisateur</td>
<td>« Complianceuser »</td>
<td></td>
</tr>
<tr class="even">
<td>Mot de passe</td>
<td>« Compliancepassword »</td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a>Codes de réponse

| **Code de réponse** | **Description**                   |
| ----------------- | --------------------------------- |
| 200               | OK, une liste d’événements dans atome + xml |
| 404               | Introuvable                         |
| 302               | Rediriger                          |
| 401               | Autorisation échouée              |
| 403               | Message d’échec d’authentification             |

##### <a name="get-an-event-by-id"></a>Obtenir un événement par ID

| Méthode         | GET   |                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------- |
| URL            | [https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\)) |                      |
| En-tête         | Content-Type                                                                                                                                                                                                                                                       | application/atom+xml |
| Authentification | De base                                                                                                                                                                                                                                                              |                      |
| Nom d’utilisateur       | « Complianceuser »                                                                                                                                                                                                                                                   |                      |
| Mot de passe       | « Compliancepassword »                                                                                                                                                                                                                                               |                      |

##### <a name="response-codes"></a>Codes de réponse

| **Code de réponse** | **Description**                                      |
| ----------------- | ---------------------------------------------------- |
| 200               | OK, le corps du message de réponse contient l’événement dans atome + xml |
| 404               | Introuvable                                            |
| 302               | Rediriger                                             |
| 401               | Autorisation échouée                                 |
| 403               | Message d’échec d’authentification                                |

##### <a name="get-an-event-by-name"></a>Obtenir un événement par le nom

| Méthode         | GET       |                      |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| URL            | <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('EventByRESTPost-2226bfebcc2841a8968ba71f9516b763')> |                      |
| En-têtes        | Content-Type                                                                                                                                 | application/atom+xml |
| Authentification | De base                                                                                                                                        |                      |
| Nom d’utilisateur       | « Complianceuser »                                                                                                                             |                      |
| Mot de passe       | « Compliancepassword »                                                                                                                         |                      |

##### <a name="response-codes"></a>Codes de réponse

| **Code de réponse** | **Description**                                      |
| ----------------- | ---------------------------------------------------- |
| 200               | OK, le corps du message de réponse contient l’événement dans atome + xml |
| 404               | Introuvable                                            |
| 302               | Rediriger                                             |
| 401               | Autorisation échouée                                 |
| 403               | Message d’échec d’authentification                                |

#### <a name="using-powershell-ver6-or-higher-or-any-http-client"></a>L’aide de PowerShell (ver.6 ou une version ultérieure) ou n’importe quel client HTTP

Étape 1: Connectez-vous à PowerShell.

Étape 2: Exécutez le script suivant.

<table>
<tbody>
<tr class="odd">
<td><p>param([string]$baseUri)</p>
<p>$userName = &quot;Nomd’utilisateur&quot;</p>
<p>$password = &quot;Motdepasse&quot;</p>
<p>$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</p>
<p>$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</p>
<p>$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</p>
<p>Écriture hôte &quot;Commencez à créer un événement avec nom : $EventName&quot;</p>
<p>$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</p>
<p>&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</p>
<p>xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</p>
<p>xmlns='http://www.w3.org/2005/Atom'&gt;</p>
<p>&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</p>
<p>&lt;mise à jour&gt;14/7/2017 14:03:36&lt;/ mis à jour&gt;</p>
<p>&lt;content type='application/xml'&gt;</p>
<p>&lt;m:properties&gt;</p>
<p>&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</p>
<p>&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</p>
<p>&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</p>
<p>&lt;/m:properties&gt;</p>
<p>&lt;/contenu&gt;</p>
<p>&lt;/entrée&gt;&quot;</p>
<p>$event = $null</p>
<p>Essayez</p>
<p>{</p>
<p>$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Uri &quot;$baseUri/ComplianceRetentionEvent&quot;- ContentType &quot;application/atom + xml&quot;-l’authentification de base-Credential $credentials -MaximumRedirection 0</p>
<p>}</p>
<p>catch</p>
<p>{</p>
<p>$response = $_.Exception.Response</p>
<p>if($response.StatusCode -eq &quot;Redirect&quot;)</p>
<p>{</p>
<p>$url = $response.Headers.Location</p>
<p>Écriture hôte &quot;redirigés vers $url&quot;</p>
<p>$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Url -ContentType &quot;application/atom + xml&quot; -l’Authentification de base-Credential $credentials -MaximumRedirection 0</p>
<p>}</p>
<p>}</p>
<p>$event | fl *</p></td>
</tr>
</tbody>
</table>

#### <a name="verify-the-outcome-in-both-options"></a>Vérifier le résultat dans les deux options

Étape 1: Accéder au Centre de Conformité et de Sécurité

Étape 2 : Cliquez sur les événements sous gouvernance des données

Étape 3 : Vérifier l’Événement a été créé.

De même, les options ci-dessus pour automatiser la rétention basée sur des événements peuvent être également utilisées pour les scénarios suivants.

### <a name="scenario-2-contracts-expiring"></a>Scénario 2 : Contrats expiration

Une organisation peut avoir plusieurs enregistrements pour un contrat unique avec des clients, fournisseurs et partenaires. Ces documents peuvent résider dans une bibliothèque de documents tels que SharePoint. La fin d’un contrat détermine le début de la période de rétention des documents associé au contrat. Par exemple : tous les enregistrements liés au contrats doivent être conservés pour cinq ans de l’heure de l’expiration du contrat. L’événement qui déclenche la période de rétention de cinq ans est l’expiration du contrat.

Un système de gestion de relation client (CRM) pouvez travailler avec Microsoft 365 et la rétention de déclencheur de documents de contrat

**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**

![Diagramme des rôles et des tâches pour le scénario d’expiration contrat](media/automate-event-driven-retention-contract-expiration.png)

  - L’administrateur crée une bibliothèque SharePoint avec les différents dossiers pour chaque type de contrat.

  - L’administrateur ajoute des fichiers de contrat tels que des contrats de licence, les contrats de développement pour chaque dossier contrat

  - L’administrateur affecte des Id de l’élément à chaque dossier de contrat.

  - L’administrateur SCG se connecte au Centre de Conformité et de Sécurité

  - L’administrateur SCC crée un contrat lié aux types événements tels que « Création de contrat, » , « Expiration de contrat » dans le Centre de Sécurité et Conformité.

  - Administrateur SCC crée une étiquette « Expiration de contrat ».

  - Cette étiquette « Expiration du Contrat » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint

  - Le Système de Gestion de Contrat peut fonctionner avec Microsoft Flow ou une application similaire pour exécuter cette page régulièrement pour gérer les fichiers de contrat

  - Si un employé a quitté l’organisation, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.

### <a name="scenario-3-end-of-product-manufacturing"></a>Scénario 3 : Fin de la fabrication de produit

Une entreprise de fabrication produisant différentes lignes de produits crée plusieurs caractéristiques de fabrication et les prix de documents. Lorsque le produit n’est plus fabriqué, toutes les spécifications et documents liée à ce besoin produit sont conservés pendant une période spécifique suivant la fin de la durée de vie du produit.

Un système de planification (ERP) peut fonctionner avec Microsoft 365 et Microsoft Flow pour la rétention de déclencheur.

**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**

![Diagramme des rôles et des tâches pour le scénario de cycle de vie de produit](media/automate-event-driven-retention-product-lifecycle-expiration.png)

  - L’administrateur crée des dossiers du produit dans l’ensemble de Documents tel que produit 1, produit 2, etc..

  - L’administrateur ajoute des fichiers produit tels que les spécifications de fabrication, produit sur les tarifs, les licences produit pour chaque dossier du produit

  - L’administrateur affecte des Id de l’élément à chaque dossier produit.

  - L’administrateur SCG se connecte au Centre de Conformité et de Sécurité

  - L’administrateur SCC crée des types d’événement liés à l’employé tels que « Commencer la fabrication de produit », « Fin de fabrication de produit » dans le Centre de Sécurité et Conformité.

  - L’administrateur SCC crée l’étiquette « Fin de la Fabrication du Produit » dans le Centre de Sécurité et Conformité.

  - Cette étiquette «Fin de la Fabrication du Produit» est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint

  - Le Système de Gestion de Contrat ERP peut fonctionner avec Microsoft Flow ou des applications similaires pour s’exécuter régulièrement pour gérer les fichiers de produit

  - Si la fabrication d’un produit se termine, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de produit spécifiques.

## <a name="appendix"></a>Annexe

### <a name="using-redirect-302-response-results-to-call-the-rest-api"></a>Utiliser les résultats de réponses 302 de redirection pour appeler des API REST

1.  Appeler un appel d’événement de rétention POST à l’aide de l’URL API REST <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (les autorisations d’administrateur général sont obligatoires)

2.  Vérifiez le code de réponse. S’il s’agit 302, puis obtenez l’URL redirigé de propriété de l’emplacement de l’en-tête de réponse

3.  Appeler l’appel d’événement rétention POST à l’aide d’URL redirigé.

## <a name="credits"></a>Crédits

Cette rubrique a été révisée par :

Antonio Maio<br/>MVP Services et applications Microsoft Office<br/> Antonio.Maio@Protiviti.com
