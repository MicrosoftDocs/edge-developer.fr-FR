---
description: Découvrez comment déclarer des autorisations pour les API dans votre manifeste
title: Déclarer des autorisations d’API dans les manifestes d’extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, extensions, centre de partenaires, développeur
ms.openlocfilehash: 987279a8072388d3fd47ee8b7cbf5f9bb3c483e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461517"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="declare-api-permissions-in-extension-manifests"></a>Déclarer des autorisations d’API dans les manifestes d’extension  

Pour utiliser la plupart des `chrome.*` API, votre extension doit déclarer le `permissions` manifeste.  Vous pouvez déclarer des autorisations à l’aide d’une chaîne d’autorisation du tableau qui suit ou utiliser un modèle pour faire correspondre des chaînes similaires.  Les autorisations permettent de limiter votre extension si elle est compromise par un programme malveillant.  Certaines autorisations peuvent s’afficher pour les utilisateurs avant l’installation de l’extension à l’aide des avertissements d’autorisation.  

Si une API nécessite que vous déclariez des autorisations dans le manifeste, examinez la documentation de cette API pour comprendre les autorisations nécessaires.  Par exemple, la page Stockage API indique comment déclarer `storage` l’autorisation.  

L’extrait de code suivant décrit comment déclarer des autorisations dans le fichier manifeste.  

```json
"permissions": [
  "tabs",
  "bookmarks",
  "http://www.blogger.com/",
  "http://*.google.com/",
  "unlimitedStorage"
]
```  

Le tableau suivant répertorie les chaînes d’autorisation actuellement disponibles à utiliser dans votre manifeste, ainsi que les descriptions.  

| Chaîne d’autorisation | Détails |  
|:--- |:--- |  
| `activeTab` | Demande l’octroi d’autorisations à l’extension conformément à la `activeTab` spécification. |  
| `alarms` | Donne à votre extension l’accès à `chrome.alarms` l’API. |  
| `background` | Permet Microsoft Edge démarrer tôt et s’arrêter tard, de sorte que les extensions peuvent avoir une durée de vie plus longue.  Lorsqu’une extension installée dispose d’une autorisation, Microsoft Edge s’exécute de manière invisible dès que l’utilisateur se connecte à l’ordinateur de l’utilisateur et avant que l’utilisateur ne lance `background` Microsoft Edge.  `background`L’autorisation permet également Microsoft Edge l’exécution, même après la fermeture de sa dernière fenêtre, jusqu’à ce que l’utilisateur quitte Microsoft Edge.  Cette autorisation n’affecte pas les extensions qui sont désactivées dans le navigateur.  `background`L’autorisation est normalement utilisée sur une page d’arrière-plan. |  
| `bookmarks` | Donne à votre extension l’accès à `chrome.bookmarks` l’API. |  
| `browsingData` | Donne à votre extension l’accès à `chrome.browsingData` l’API. |  
| `certificateProvider` | Donne à votre extension l’accès à `chrome.certificateProvider` l’API. |  
| `clipboardRead` | Obligatoire si l’extension utilise `document.execCommand('paste')` . |  
| `clipboardWrite` | Indique que l’extension utilise `document.execCommand('copy')` ou `document.execCommand('cut')` . |  
| `contentSettings` | Donne à votre extension l’accès à `chrome.contentSettings` l’API. |  
| `contextMenus` | Donne à votre extension l’accès à `chrome.contextMenus` l’API. |  
| `cookies` | Donne à votre extension l’accès à `chrome.cookies` l’API. |  
| `debugger` | Donne à votre extension l’accès à `chrome.debugger` l’API. |  
| `declarativeContent` | Donne à votre extension l’accès à `chrome.declarativeContent` l’API. |  
| `declarativeNetRequest` | Donne à votre extension l’accès à `chrome.declarativeNetRequest` l’API. |  
| `declarativeNetRequestFeedback` | Accorde à l’extension l’accès aux événements et méthodes au sein de l’API, qui renvoie des informations sur les règles `chrome.declarativeNetRequest` déclaratives qui correspondent. |  
| `declarativeWebRequest` | Donne à votre extension l’accès à `chrome.declarativeWebRequest` l’API. |  
| `desktopCapture` | Donne à votre extension l’accès à `chrome.desktopCapture` l’API. |  
| `documentScan` | Donne à votre extension l’accès à `chrome.documentScan` l’API. |  
| `downloads` | Donne à votre extension l’accès à `chrome.downloads` l’API. |  
| `enterprise.deviceAttributes` | Donne à votre extension l’accès à `chrome.enterprise.deviceAttributes` l’API. |  
| `enterprise.hardwarePlatform` | Donne à votre extension l’accès à `chrome.enterprise.hardwarePlatform` l’API. |  
| `enterprise.networkingAttributes` | Donne à votre extension l’accès à `chrome.enterprise.networkingAttributes` l’API. |  
| `enterprise.platformKeys` | Donne à votre extension l’accès à `chrome.enterprise.platformKeys` l’API. |  
| `experimental` | Obligatoire si l’extension utilise une `chrome.experimental.*` API. |  
| `fileBrowserHandler` | Donne à votre extension l’accès à `chrome.fileBrowserHandler` l’API. |  
| `fileSystemProvider` | Donne à votre extension l’accès à `chrome.fileSystemProvider` l’API. |  
| `fontSettings` | Donne à votre extension l’accès à `chrome.fontSettings` l’API. |  
| `geolocation` | Permet à l’extension d’utiliser l’API de géolocalisation sans demander d’autorisation à l’utilisateur. |  
| `history` | Donne à votre extension l’accès à `chrome.history` l’API. |  
| `identity` | Donne à votre extension l’accès à `chrome.identity` l’API. |  
| `idle` | Donne à votre extension l’accès à `chrome.idle` l’API. |  
| `loginState` | Donne à votre extension l’accès à `chrome.loginState` l’API. |  
| `management` | Donne à votre extension l’accès à `chrome.management` l’API. |  
| `nativeMessaging` | Donne à votre extension l’accès à l’API de messagerie native. |  
| `notifications` | Donne à votre extension l’accès à `chrome.notifications` l’API. |  
| `pageCapture` | Donne à votre extension l’accès à `chrome.pageCapture` l’API. |  
| `platformKeys` | Donne à votre extension l’accès à `chrome.platformKeys` l’API. |  
| `power` | Donne à votre extension l’accès à `chrome.power` l’API. |  
| `printerProvider` | Donne à votre extension l’accès à `chrome.printerProvider` l’API. |  
| `printing` | Donne à votre extension l’accès à `chrome.printing` l’API. |  
| `printingMetrics` | Donne à votre extension l’accès à `chrome.printingMetrics` l’API. |  
| `privacy` | Donne à votre extension l’accès à `chrome.privacy` l’API. |  
| `processes` | Donne à votre extension l’accès à `chrome.processes` l’API. |  
| `proxy` | Donne à votre extension l’accès à `chrome.proxy` l’API. |  
| `scripting` | Donne à votre extension l’accès à `chrome.scripting` l’API. |  
| `search` | Donne à votre extension l’accès à `chrome.search` l’API. |  
| `sessions` | Donne à votre extension l’accès à `chrome.sessions` l’API. |  
| `signedInDevices` | Donne à votre extension l’accès à `chrome.signedInDevices` l’API. |  
| `storage` | Donne à votre extension l’accès à `chrome.storage` l’API. |  
| `system.cpu` | Donne à votre extension l’accès à `chrome.system.cpu` l’API. |  
| `system.display` | Donne à votre extension l’accès à `chrome.system.display` l’API. |  
| `system.memory` | Donne à votre extension l’accès à `chrome.system.memory` l’API. |  
| `system.storage` | Donne à votre extension l’accès à `chrome.system.storage` l’API. |  
| `tabCapture` | Donne à votre extension l’accès à `chrome.tabCapture` l’API. |  
| `tabGroups` | Donne à votre extension l’accès à `chrome.tabGroups` l’API. |  
| `tabs` | Donne à votre extension l’accès aux champs privilégiés des objets qui peuvent être utilisés par plusieurs `Tab` API, y compris `chrome.tabs` et `chrome.windows` .  Dans de nombreux cas, votre extension n’a pas besoin de déclarer l’autorisation d’utiliser `tabs` ces API. |  
| `topSites` | Donne à votre extension l’accès à `chrome.topSites` l’API. |  
| `tts` | Donne à votre extension l’accès à `chrome.tts` l’API. |  
| `ttsEngine` | Donne à votre extension l’accès à `chrome.ttsEngine` l’API. |  
| `unlimitedStorage` | Fournit un quota illimité pour le stockage des données côté client, telles que les bases de données et les fichiers de stockage locaux.  Sans cette autorisation, l’extension est limitée à 5 Mo de stockage local. |  
| `vpnProvider` | Donne à votre extension l’accès à `chrome.vpnProvider` l’API. |  
| `wallpaper` | Donne à votre extension l’accès à `chrome.wallpaper` l’API. |  
| `webNavigation` | Donne à votre extension l’accès à `chrome.webNavigation` l’API. |  
| `webRequest` | Donne à votre extension l’accès à `chrome.webRequest` l’API. |  
| `webRequestBlocking` | Obligatoire si l’extension utilise `chrome.webRequest` l’API pour bloquer les demandes. |  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
