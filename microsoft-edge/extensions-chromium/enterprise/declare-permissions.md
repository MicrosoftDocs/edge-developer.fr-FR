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
# <a name="declare-api-permissions-in-extension-manifests"></a><span data-ttu-id="ba877-104">Déclarer des autorisations d’API dans les manifestes d’extension</span><span class="sxs-lookup"><span data-stu-id="ba877-104">Declare API permissions in extension manifests</span></span>  

<span data-ttu-id="ba877-105">Pour utiliser la plupart des `chrome.*` API, votre extension doit déclarer le `permissions` manifeste.</span><span class="sxs-lookup"><span data-stu-id="ba877-105">To use most of the `chrome.*` APIs, your extension must declare the `permissions` in the manifest.</span></span>  <span data-ttu-id="ba877-106">Vous pouvez déclarer des autorisations à l’aide d’une chaîne d’autorisation à partir du tableau qui suit, ou utiliser un modèle pour faire correspondre des chaînes similaires.</span><span class="sxs-lookup"><span data-stu-id="ba877-106">You may declare permissions using a permission string from the table that follows, or use a pattern to match similar strings.</span></span>  <span data-ttu-id="ba877-107">Les autorisations permettent de limiter votre extension si elle est compromise par un programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="ba877-107">Permissions help to constrain your extension if it gets compromised by malware.</span></span>  <span data-ttu-id="ba877-108">Certaines autorisations peuvent s’afficher pour les utilisateurs avant l’installation de l’extension à l’aide des avertissements d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ba877-108">Some permissions may display to users before installation of the extension using Permission Warnings.</span></span>  

<span data-ttu-id="ba877-109">Si une API nécessite que vous déclariez des autorisations dans le manifeste, examinez la documentation de cette API pour comprendre les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ba877-109">If an API requires you to declare permissions in the manifest, review the documentation for that API to understand the needed permissions.</span></span>  <span data-ttu-id="ba877-110">Par exemple, la page API de stockage décrit comment déclarer `storage` l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ba877-110">For example, the Storage API page describes how to declare the `storage` permission.</span></span>  

<span data-ttu-id="ba877-111">L’extrait de code suivant décrit comment déclarer des autorisations dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="ba877-111">The following code snippet outlines how to declare permissions in the manifest file.</span></span>  

```json
"permissions": [
  "tabs",
  "bookmarks",
  "http://www.blogger.com/",
  "http://*.google.com/",
  "unlimitedStorage"
]
```  

<span data-ttu-id="ba877-112">Le tableau suivant répertorie les chaînes d’autorisation actuellement disponibles à utiliser dans votre manifeste, ainsi que les descriptions.</span><span class="sxs-lookup"><span data-stu-id="ba877-112">The following table lists the currently available permission strings to use in your manifest, and the descriptions.</span></span>  

| <span data-ttu-id="ba877-113">Chaîne d’autorisation</span><span class="sxs-lookup"><span data-stu-id="ba877-113">Permission string</span></span> | <span data-ttu-id="ba877-114">Détails</span><span class="sxs-lookup"><span data-stu-id="ba877-114">Details</span></span> |  
|:--- |:--- |  
| `activeTab` | <span data-ttu-id="ba877-115">Demande l’octroi d’autorisations à l’extension conformément à la `activeTab` spécification.</span><span class="sxs-lookup"><span data-stu-id="ba877-115">Requests that the extension is granted permissions according to the `activeTab` specification.</span></span> |  
| `alarms` | <span data-ttu-id="ba877-116">Donne à votre extension l’accès à `chrome.alarms` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-116">Gives your extension access to the `chrome.alarms` API.</span></span> |  
| `background` | <span data-ttu-id="ba877-117">Permet à Microsoft Edge de démarrer tôt et de s’arrêter tardivement, de sorte que les extensions peuvent avoir une durée de vie plus longue.</span><span class="sxs-lookup"><span data-stu-id="ba877-117">Makes Microsoft Edge start up early and shut down late, so that extensions may have a longer life.</span></span>  <span data-ttu-id="ba877-118">Lorsqu’une extension installée dispose d’autorisations, Microsoft Edge s’exécute de manière invisible dès que l’utilisateur se connecte à l’ordinateur de l’utilisateur et avant que `background` l’utilisateur lance Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba877-118">When any installed extension has `background` permission, Microsoft Edge runs invisibly as soon as the user logs into the user's computer, and before the user launches Microsoft Edge.</span></span>  <span data-ttu-id="ba877-119">L’autorisation permet également à Microsoft Edge de poursuivre son exécution, même après la fermeture de sa dernière fenêtre, jusqu’à ce que l’utilisateur `background` quitte explicitement Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba877-119">The `background` permission also makes Microsoft Edge continue running, even after its last window is closed, until the user explicitly quits Microsoft Edge.</span></span>  <span data-ttu-id="ba877-120">Cette autorisation n’affecte pas les extensions qui sont désactivées dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="ba877-120">This permission does not affect extensions that are turned off in the browser.</span></span>  <span data-ttu-id="ba877-121">`background`L’autorisation est normalement utilisée sur une page d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ba877-121">The `background` permission is normally used on a background page.</span></span> |  
| `bookmarks` | <span data-ttu-id="ba877-122">Donne à votre extension l’accès à `chrome.bookmarks` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-122">Gives your extension access to the `chrome.bookmarks` API.</span></span> |  
| `browsingData` | <span data-ttu-id="ba877-123">Donne à votre extension l’accès à `chrome.browsingData` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-123">Gives your extension access to the `chrome.browsingData` API.</span></span> |  
| `certificateProvider` | <span data-ttu-id="ba877-124">Donne à votre extension l’accès à `chrome.certificateProvider` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-124">Gives your extension access to the `chrome.certificateProvider` API.</span></span> |  
| `clipboardRead` | <span data-ttu-id="ba877-125">Obligatoire si l’extension utilise `document.execCommand('paste')` .</span><span class="sxs-lookup"><span data-stu-id="ba877-125">Required if the extension uses `document.execCommand('paste')`.</span></span> |  
| `clipboardWrite` | <span data-ttu-id="ba877-126">Indique que l’extension utilise `document.execCommand('copy')` ou `document.execCommand('cut')` .</span><span class="sxs-lookup"><span data-stu-id="ba877-126">Indicates the extension uses `document.execCommand('copy')` or `document.execCommand('cut')`.</span></span> |  
| `contentSettings` | <span data-ttu-id="ba877-127">Donne à votre extension l’accès à `chrome.contentSettings` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-127">Gives your extension access to the `chrome.contentSettings` API.</span></span> |  
| `contextMenus` | <span data-ttu-id="ba877-128">Donne à votre extension l’accès à `chrome.contextMenus` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-128">Gives your extension access to the `chrome.contextMenus` API.</span></span> |  
| `cookies` | <span data-ttu-id="ba877-129">Donne à votre extension l’accès à `chrome.cookies` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-129">Gives your extension access to the `chrome.cookies` API.</span></span> |  
| `debugger` | <span data-ttu-id="ba877-130">Donne à votre extension l’accès à `chrome.debugger` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-130">Gives your extension access to the `chrome.debugger` API.</span></span> |  
| `declarativeContent` | <span data-ttu-id="ba877-131">Donne à votre extension l’accès à `chrome.declarativeContent` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-131">Gives your extension access to the `chrome.declarativeContent` API.</span></span> |  
| `declarativeNetRequest` | <span data-ttu-id="ba877-132">Donne à votre extension l’accès à `chrome.declarativeNetRequest` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-132">Gives your extension access to the `chrome.declarativeNetRequest` API.</span></span> |  
| `declarativeNetRequestFeedback` | <span data-ttu-id="ba877-133">Accorde à l’extension l’accès aux événements et méthodes au sein de l’API, qui renvoie des informations sur les règles `chrome.declarativeNetRequest` déclaratives qui correspondent.</span><span class="sxs-lookup"><span data-stu-id="ba877-133">Grants the extension access to events and methods within the `chrome.declarativeNetRequest` API, which returns information on declarative rules matched.</span></span> |  
| `declarativeWebRequest` | <span data-ttu-id="ba877-134">Donne à votre extension l’accès à `chrome.declarativeWebRequest` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-134">Gives your extension access to the `chrome.declarativeWebRequest` API.</span></span> |  
| `desktopCapture` | <span data-ttu-id="ba877-135">Donne à votre extension l’accès à `chrome.desktopCapture` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-135">Gives your extension access to the `chrome.desktopCapture` API.</span></span> |  
| `documentScan` | <span data-ttu-id="ba877-136">Donne à votre extension l’accès à `chrome.documentScan` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-136">Gives your extension access to the `chrome.documentScan` API.</span></span> |  
| `downloads` | <span data-ttu-id="ba877-137">Donne à votre extension l’accès à `chrome.downloads` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-137">Gives your extension access to the `chrome.downloads` API.</span></span> |  
| `enterprise.deviceAttributes` | <span data-ttu-id="ba877-138">Donne à votre extension l’accès à `chrome.enterprise.deviceAttributes` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-138">Gives your extension access to the `chrome.enterprise.deviceAttributes` API.</span></span> |  
| `enterprise.hardwarePlatform` | <span data-ttu-id="ba877-139">Donne à votre extension l’accès à `chrome.enterprise.hardwarePlatform` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-139">Gives your extension access to the `chrome.enterprise.hardwarePlatform` API.</span></span> |  
| `enterprise.networkingAttributes` | <span data-ttu-id="ba877-140">Donne à votre extension l’accès à `chrome.enterprise.networkingAttributes` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-140">Gives your extension access to the `chrome.enterprise.networkingAttributes` API.</span></span> |  
| `enterprise.platformKeys` | <span data-ttu-id="ba877-141">Donne à votre extension l’accès à `chrome.enterprise.platformKeys` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-141">Gives your extension access to the `chrome.enterprise.platformKeys` API.</span></span> |  
| `experimental` | <span data-ttu-id="ba877-142">Obligatoire si l’extension utilise une `chrome.experimental.*` API.</span><span class="sxs-lookup"><span data-stu-id="ba877-142">Required if the extension uses any `chrome.experimental.*` API.</span></span> |  
| `fileBrowserHandler` | <span data-ttu-id="ba877-143">Donne à votre extension l’accès à `chrome.fileBrowserHandler` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-143">Gives your extension access to the `chrome.fileBrowserHandler` API.</span></span> |  
| `fileSystemProvider` | <span data-ttu-id="ba877-144">Donne à votre extension l’accès à `chrome.fileSystemProvider` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-144">Gives your extension access to the `chrome.fileSystemProvider` API.</span></span> |  
| `fontSettings` | <span data-ttu-id="ba877-145">Donne à votre extension l’accès à `chrome.fontSettings` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-145">Gives your extension access to the `chrome.fontSettings` API.</span></span> |  
| `geolocation` | <span data-ttu-id="ba877-146">Permet à l’extension d’utiliser l’API de géolocalisation sans demander d’autorisation à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba877-146">Allows the extension to use the geolocation API without prompting the user for permission.</span></span> |  
| `history` | <span data-ttu-id="ba877-147">Donne à votre extension l’accès à `chrome.history` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-147">Gives your extension access to the `chrome.history` API.</span></span> |  
| `identity` | <span data-ttu-id="ba877-148">Donne à votre extension l’accès à `chrome.identity` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-148">Gives your extension access to the `chrome.identity` API.</span></span> |  
| `idle` | <span data-ttu-id="ba877-149">Donne à votre extension l’accès à `chrome.idle` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-149">Gives your extension access to the `chrome.idle` API.</span></span> |  
| `loginState` | <span data-ttu-id="ba877-150">Donne à votre extension l’accès à `chrome.loginState` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-150">Gives your extension access to the `chrome.loginState` API.</span></span> |  
| `management` | <span data-ttu-id="ba877-151">Donne à votre extension l’accès à `chrome.management` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-151">Gives your extension access to the `chrome.management` API.</span></span> |  
| `nativeMessaging` | <span data-ttu-id="ba877-152">Donne à votre extension l’accès à l’API de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="ba877-152">Gives your extension access to the native messaging API.</span></span> |  
| `notifications` | <span data-ttu-id="ba877-153">Donne à votre extension l’accès à `chrome.notifications` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-153">Gives your extension access to the `chrome.notifications` API.</span></span> |  
| `pageCapture` | <span data-ttu-id="ba877-154">Donne à votre extension l’accès à `chrome.pageCapture` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-154">Gives your extension access to the `chrome.pageCapture` API.</span></span> |  
| `platformKeys` | <span data-ttu-id="ba877-155">Donne à votre extension l’accès à `chrome.platformKeys` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-155">Gives your extension access to the `chrome.platformKeys` API.</span></span> |  
| `power` | <span data-ttu-id="ba877-156">Donne à votre extension l’accès à `chrome.power` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-156">Gives your extension access to the `chrome.power` API.</span></span> |  
| `printerProvider` | <span data-ttu-id="ba877-157">Donne à votre extension l’accès à `chrome.printerProvider` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-157">Gives your extension access to the `chrome.printerProvider` API.</span></span> |  
| `printing` | <span data-ttu-id="ba877-158">Donne à votre extension l’accès à `chrome.printing` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-158">Gives your extension access to the `chrome.printing` API.</span></span> |  
| `printingMetrics` | <span data-ttu-id="ba877-159">Donne à votre extension l’accès à `chrome.printingMetrics` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-159">Gives your extension access to the `chrome.printingMetrics` API.</span></span> |  
| `privacy` | <span data-ttu-id="ba877-160">Donne à votre extension l’accès à `chrome.privacy` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-160">Gives your extension access to the `chrome.privacy` API.</span></span> |  
| `processes` | <span data-ttu-id="ba877-161">Donne à votre extension l’accès à `chrome.processes` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-161">Gives your extension access to the `chrome.processes` API.</span></span> |  
| `proxy` | <span data-ttu-id="ba877-162">Donne à votre extension l’accès à `chrome.proxy` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-162">Gives your extension access to the `chrome.proxy` API.</span></span> |  
| `scripting` | <span data-ttu-id="ba877-163">Donne à votre extension l’accès à `chrome.scripting` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-163">Gives your extension access to the `chrome.scripting` API.</span></span> |  
| `search` | <span data-ttu-id="ba877-164">Donne à votre extension l’accès à `chrome.search` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-164">Gives your extension access to the `chrome.search` API.</span></span> |  
| `sessions` | <span data-ttu-id="ba877-165">Donne à votre extension l’accès à `chrome.sessions` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-165">Gives your extension access to the `chrome.sessions` API.</span></span> |  
| `signedInDevices` | <span data-ttu-id="ba877-166">Donne à votre extension l’accès à `chrome.signedInDevices` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-166">Gives your extension access to the `chrome.signedInDevices` API.</span></span> |  
| `storage` | <span data-ttu-id="ba877-167">Donne à votre extension l’accès à `chrome.storage` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-167">Gives your extension access to the `chrome.storage` API.</span></span> |  
| `system.cpu` | <span data-ttu-id="ba877-168">Donne à votre extension l’accès à `chrome.system.cpu` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-168">Gives your extension access to the `chrome.system.cpu` API.</span></span> |  
| `system.display` | <span data-ttu-id="ba877-169">Donne à votre extension l’accès à `chrome.system.display` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-169">Gives your extension access to the `chrome.system.display` API.</span></span> |  
| `system.memory` | <span data-ttu-id="ba877-170">Donne à votre extension l’accès à `chrome.system.memory` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-170">Gives your extension access to the `chrome.system.memory` API.</span></span> |  
| `system.storage` | <span data-ttu-id="ba877-171">Donne à votre extension l’accès à `chrome.system.storage` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-171">Gives your extension access to the `chrome.system.storage` API.</span></span> |  
| `tabCapture` | <span data-ttu-id="ba877-172">Donne à votre extension l’accès à `chrome.tabCapture` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-172">Gives your extension access to the `chrome.tabCapture` API.</span></span> |  
| `tabGroups` | <span data-ttu-id="ba877-173">Donne à votre extension l’accès à `chrome.tabGroups` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-173">Gives your extension access to the `chrome.tabGroups` API.</span></span> |  
| `tabs` | <span data-ttu-id="ba877-174">Donne à votre extension l’accès aux champs privilégiés des objets qui peuvent être utilisés par plusieurs `Tab` API, y compris `chrome.tabs` et `chrome.windows` .</span><span class="sxs-lookup"><span data-stu-id="ba877-174">Gives your extension access to privileged fields of the `Tab` objects that may be used by several APIs including `chrome.tabs` and `chrome.windows`.</span></span>  <span data-ttu-id="ba877-175">Dans de nombreux cas, votre extension n’a pas besoin de déclarer l’autorisation d’utiliser `tabs` ces API.</span><span class="sxs-lookup"><span data-stu-id="ba877-175">In many circumstances, your extension does not need to declare the `tabs` permission to make use of these APIs.</span></span> |  
| `topSites` | <span data-ttu-id="ba877-176">Donne à votre extension l’accès à `chrome.topSites` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-176">Gives your extension access to the `chrome.topSites` API.</span></span> |  
| `tts` | <span data-ttu-id="ba877-177">Donne à votre extension l’accès à `chrome.tts` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-177">Gives your extension access to the `chrome.tts` API.</span></span> |  
| `ttsEngine` | <span data-ttu-id="ba877-178">Donne à votre extension l’accès à `chrome.ttsEngine` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-178">Gives your extension access to the `chrome.ttsEngine` API.</span></span> |  
| `unlimitedStorage` | <span data-ttu-id="ba877-179">Fournit un quota illimité pour le stockage des données côté client, telles que les bases de données et les fichiers de stockage local.</span><span class="sxs-lookup"><span data-stu-id="ba877-179">Provides an unlimited quota for storing client-side data, such as databases and local storage files.</span></span>  <span data-ttu-id="ba877-180">Sans cette autorisation, l’extension est limitée à 5 Mo de stockage local.</span><span class="sxs-lookup"><span data-stu-id="ba877-180">Without this permission, the extension is limited to 5 MB of local storage.</span></span> |  
| `vpnProvider` | <span data-ttu-id="ba877-181">Donne à votre extension l’accès à `chrome.vpnProvider` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-181">Gives your extension access to the `chrome.vpnProvider` API.</span></span> |  
| `wallpaper` | <span data-ttu-id="ba877-182">Donne à votre extension l’accès à `chrome.wallpaper` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-182">Gives your extension access to the `chrome.wallpaper` API.</span></span> |  
| `webNavigation` | <span data-ttu-id="ba877-183">Donne à votre extension l’accès à `chrome.webNavigation` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-183">Gives your extension access to the `chrome.webNavigation` API.</span></span> |  
| `webRequest` | <span data-ttu-id="ba877-184">Donne à votre extension l’accès à `chrome.webRequest` l’API.</span><span class="sxs-lookup"><span data-stu-id="ba877-184">Gives your extension access to the `chrome.webRequest` API.</span></span> |  
| `webRequestBlocking` | <span data-ttu-id="ba877-185">Obligatoire si l’extension utilise `chrome.webRequest` l’API pour bloquer les demandes.</span><span class="sxs-lookup"><span data-stu-id="ba877-185">Required if the extension uses the `chrome.webRequest` API to block requests.</span></span> |  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="ba877-186">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba877-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ba877-187">La page d’origine se trouve [ici.](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/)</span><span class="sxs-lookup"><span data-stu-id="ba877-187">The original page is found [here](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ba877-189">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba877-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
