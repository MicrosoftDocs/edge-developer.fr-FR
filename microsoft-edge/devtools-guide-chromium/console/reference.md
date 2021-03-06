---
description: Une référence complète sur chaque fonctionnalité et comportement liés à l’interface utilisateur de la console dans Microsoft Edge DevTools.
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399161"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="console-reference"></a><span data-ttu-id="735c5-104">Référence de la console</span><span class="sxs-lookup"><span data-stu-id="735c5-104">Console reference</span></span>  

<span data-ttu-id="735c5-105">Cette page est une référence de fonctionnalités liées à la console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="735c5-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="735c5-106">Il part du principe que vous êtes déjà familiarisé avec l’utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.</span><span class="sxs-lookup"><span data-stu-id="735c5-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="735c5-107">Si ce n’est pas le cas, accédez à l’exécution de [JavaScript][DevToolsConsoleJavascript] dans la console et à la journalisation des [messages dans la console.][DevToolsConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="735c5-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="735c5-108">Si vous recherchez la référence d’API sur des fonctions telles que , accédez à Référence `console.log()` de [l’API console.][DevToolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="735c5-108">If you are looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="735c5-109">Pour obtenir la référence sur des fonctions telles que , accédez à Référence de `monitorEvents()` [l’API des utilitaires de console.][DevToolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="735c5-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="735c5-110">Ouvrir la console</span><span class="sxs-lookup"><span data-stu-id="735c5-110">Open the Console</span></span>  

<span data-ttu-id="735c5-111">Vous pouvez ouvrir la **console en tant** qu’outil dans le [volet](#open-the-console-tool) supérieur ou en tant qu’outil dans [le caisse.](#open-the-console-tool-in-the-drawer)</span><span class="sxs-lookup"><span data-stu-id="735c5-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="735c5-112">Ouvrir l’outil Console</span><span class="sxs-lookup"><span data-stu-id="735c5-112">Open the Console tool</span></span>  

<span data-ttu-id="735c5-113">Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="735c5-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="L’outil Console" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="735c5-115">**L’outil Console**</span><span class="sxs-lookup"><span data-stu-id="735c5-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="735c5-116">Pour ouvrir **l’outil Console** à partir du [menu][DevToolsCommandMenu]Commande, commencez à taper, puis exécutez la commande Afficher la console qui a le `Console` badge **Panneau** à côté. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="735c5-116">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Commande pour afficher le panneau console" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="735c5-118">Commande pour afficher **l’outil Console**</span><span class="sxs-lookup"><span data-stu-id="735c5-118">The command to show the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="735c5-119">Ouvrir l’outil Console dans le caisse</span><span class="sxs-lookup"><span data-stu-id="735c5-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="735c5-120">Sélectionnez `Escape` ou choisissez Personnaliser et contrôler **DevTools** \( \), puis choisissez Afficher le caisse `...` de la **console.**</span><span class="sxs-lookup"><span data-stu-id="735c5-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Afficher le caisse de la console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="735c5-122">Afficher le caisse de la console</span><span class="sxs-lookup"><span data-stu-id="735c5-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="735c5-123">Le caisse s’ouvre en bas de la fenêtre DevTools, avec l’outil **Console** ouvert.</span><span class="sxs-lookup"><span data-stu-id="735c5-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Outil Console dans le caisse" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="735c5-125">Outil **Console** dans le **caisse**</span><span class="sxs-lookup"><span data-stu-id="735c5-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="735c5-126">Pour ouvrir **l’outil Console** à partir du [menu][DevToolsCommandMenu]Commande, commencez à taper, puis exécutez la commande Afficher la console qui a le badge à l’aide `Console` de celui-ci. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="735c5-126">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Commande permettant d’afficher l’outil **Console** dans le caisse" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="735c5-128">Commande permettant d’afficher **l’outil Console** dans le **caisse**</span><span class="sxs-lookup"><span data-stu-id="735c5-128">The command to show the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="735c5-129">Ouvrir les paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="735c5-129">Open Console Settings</span></span>  

<span data-ttu-id="735c5-130">Choose **Console Settings** \( ![ Console Settings icon ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="735c5-130">Choose **Console Settings** \(![Console Settings icon][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Paramètres de la console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="735c5-132">Paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="735c5-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="735c5-133">Les liens ci-dessous expliquent chaque paramètre :</span><span class="sxs-lookup"><span data-stu-id="735c5-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="735c5-134">Masquer le réseau</span><span class="sxs-lookup"><span data-stu-id="735c5-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="735c5-135">Conserver le journal</span><span class="sxs-lookup"><span data-stu-id="735c5-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="735c5-136">Contexte sélectionné uniquement</span><span class="sxs-lookup"><span data-stu-id="735c5-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="735c5-137">Groupe similaire</span><span class="sxs-lookup"><span data-stu-id="735c5-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="735c5-138">Log XmlHttpRequests</span><span class="sxs-lookup"><span data-stu-id="735c5-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="735c5-139">Évaluation enthousiaste</span><span class="sxs-lookup"><span data-stu-id="735c5-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="735c5-140">Autocomplete From History</span><span class="sxs-lookup"><span data-stu-id="735c5-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="735c5-141">Ouvrir la barre latérale de la console</span><span class="sxs-lookup"><span data-stu-id="735c5-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="735c5-142">Choisissez **Afficher la barre latérale de la console** \( Afficher la barre latérale de la console \) pour afficher la barre latérale, ce qui est utile pour le ![ ][ImageShowConsoleSidebarIcon] filtrage.</span><span class="sxs-lookup"><span data-stu-id="735c5-142">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Console Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="735c5-144">**Console** Barre latérale</span><span class="sxs-lookup"><span data-stu-id="735c5-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="735c5-145">Afficher les messages</span><span class="sxs-lookup"><span data-stu-id="735c5-145">View messages</span></span>  

<span data-ttu-id="735c5-146">Cette section contient des fonctionnalités qui modifient la présentation des messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="735c5-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="735c5-147">Pour une walkthrough pratique, accédez à [Afficher les messages.][DevToolsConsoleViewMessages]</span><span class="sxs-lookup"><span data-stu-id="735c5-147">For a hands-on walkthrough, navigate to [View messages][DevToolsConsoleViewMessages].</span></span>  

### <a name="disable-message-grouping"></a><span data-ttu-id="735c5-148">Désactiver le regroupement de messages</span><span class="sxs-lookup"><span data-stu-id="735c5-148">Disable message grouping</span></span>  

<span data-ttu-id="735c5-149">[Ouvrez paramètres de](#open-console-settings) la console et désactivez **le groupe** de façon à désactiver le comportement de regroupement des messages par défaut de la console.</span><span class="sxs-lookup"><span data-stu-id="735c5-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="735c5-150">Pour obtenir un exemple, accédez à [Log XHR et fetch requests](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="735c5-150">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="735c5-151">Enregistrer les demandes XHR et Fetch</span><span class="sxs-lookup"><span data-stu-id="735c5-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="735c5-152">[Ouvrez les paramètres de](#open-console-settings) la console et activez **log XMLHttpRequests** pour enregistrer toutes les demandes et les demandes sur la `XMLHttpRequest` console au cours de leur `Fetch` temps.</span><span class="sxs-lookup"><span data-stu-id="735c5-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Log XMLHttpRequest and Fetch requests" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="735c5-154">Journal `XMLHttpRequest` et `Fetch` demandes</span><span class="sxs-lookup"><span data-stu-id="735c5-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="735c5-155">Le premier message de la figure précédente affiche le comportement de regroupement par défaut de la **console.**</span><span class="sxs-lookup"><span data-stu-id="735c5-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="735c5-156">Persist messages across page loads</span><span class="sxs-lookup"><span data-stu-id="735c5-156">Persist messages across page loads</span></span>  

<span data-ttu-id="735c5-157">Par défaut, la console s’effacera chaque fois que vous chargez une nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="735c5-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="735c5-158">Pour conserver les messages entre les chargements de page, [ouvrez paramètres](#open-console-settings) de la console, puis activez la case à cocher Conserver **le** journal.</span><span class="sxs-lookup"><span data-stu-id="735c5-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="735c5-159">Masquer les messages réseau</span><span class="sxs-lookup"><span data-stu-id="735c5-159">Hide network messages</span></span>  

<span data-ttu-id="735c5-160">Par défaut, le navigateur enregistre les messages réseau dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="735c5-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="735c5-161">Dans la figure suivante, le message sélectionné représente un code d’état HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="735c5-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un message 429 dans la console" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="735c5-163">Un `429` message dans la **console**</span><span class="sxs-lookup"><span data-stu-id="735c5-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="735c5-164">Pour masquer les messages réseau :</span><span class="sxs-lookup"><span data-stu-id="735c5-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="735c5-165">[Ouvrez paramètres de la console.](#open-console-settings)</span><span class="sxs-lookup"><span data-stu-id="735c5-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="735c5-166">Activez la **case à cocher** Masquer le réseau.</span><span class="sxs-lookup"><span data-stu-id="735c5-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="735c5-167">Filtrer les messages</span><span class="sxs-lookup"><span data-stu-id="735c5-167">Filter messages</span></span>  

<span data-ttu-id="735c5-168">Il existe de nombreuses façons de filtrer les messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="735c5-168">There are many ways to filter out messages in the Console.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="735c5-169">Filtrer les messages du navigateur</span><span class="sxs-lookup"><span data-stu-id="735c5-169">Filter out browser messages</span></span>  

<span data-ttu-id="735c5-170">[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et choisissez **Messages** de l’utilisateur pour afficher uniquement les messages provenant du JavaScript de la page.</span><span class="sxs-lookup"><span data-stu-id="735c5-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Afficher les messages de l’utilisateur" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="735c5-172">Afficher les messages de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="735c5-172">View user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="735c5-173">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="735c5-173">Filter by log level</span></span>  

<span data-ttu-id="735c5-174">DevTools affecte à chaque `console.*` méthode un niveau de gravité.</span><span class="sxs-lookup"><span data-stu-id="735c5-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="735c5-175">Il existe 4 niveaux `Verbose` : , `Info` et `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="735c5-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="735c5-176">Par exemple, `console.log()` se trouve dans le `Info` groupe, tandis `console.error()` qu’il se trouve dans le `Error` groupe.</span><span class="sxs-lookup"><span data-stu-id="735c5-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="735c5-177">La [référence de l’API][DevToolsConsoleApi] console décrit le niveau de gravité de chaque méthode applicable.</span><span class="sxs-lookup"><span data-stu-id="735c5-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="735c5-178">Chaque message journal de la console par le navigateur présente également un niveau de gravité.</span><span class="sxs-lookup"><span data-stu-id="735c5-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="735c5-179">Vous pouvez masquer n’importe quel niveau de messages qui ne vous intéresse pas.</span><span class="sxs-lookup"><span data-stu-id="735c5-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="735c5-180">Par exemple, si seuls les messages vous intéressent, vous pouvez `Error` masquer les 3 autres groupes.</span><span class="sxs-lookup"><span data-stu-id="735c5-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="735c5-181">Choose the **Log Levels** dropdown to enable or disable , , `Verbose` or `Info` `Warning` `Error` messages.</span><span class="sxs-lookup"><span data-stu-id="735c5-181">Choose the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="La dropdown Log Levels" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="735c5-183">La **dropdown Log Levels**</span><span class="sxs-lookup"><span data-stu-id="735c5-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="735c5-184">Vous pouvez également filtrer par niveau de journal en \*\*\*\* ouvrant la barre latérale de la [console,](#open-the-console-sidebar) puis en cinglant les **erreurs, les avertissements,** les informations **ou** **les commentaires.**</span><span class="sxs-lookup"><span data-stu-id="735c5-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and thenchoosing **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Utiliser la barre latérale pour afficher les avertissements" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="735c5-186">Utiliser la barre latérale pour afficher les avertissements</span><span class="sxs-lookup"><span data-stu-id="735c5-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="735c5-187">Filtrer les messages par URL</span><span class="sxs-lookup"><span data-stu-id="735c5-187">Filter messages by URL</span></span>  

<span data-ttu-id="735c5-188">Tapez `url:` suivi d’une URL pour afficher uniquement les messages provenant de cette URL.</span><span class="sxs-lookup"><span data-stu-id="735c5-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="735c5-189">Une fois que `url:` vous avez tapé, DevTools affiche toutes les URL pertinentes.</span><span class="sxs-lookup"><span data-stu-id="735c5-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="735c5-190">Les domaines fonctionnent également.</span><span class="sxs-lookup"><span data-stu-id="735c5-190">Domains also work.</span></span>  <span data-ttu-id="735c5-191">Par exemple, si et journalisation des messages, vous permet de vous concentrer sur les messages de `https://example.com/a.js` `https://example.com/b.js` ces `url:https://example.com` 2 scripts.</span><span class="sxs-lookup"><span data-stu-id="735c5-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Filtre d’URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="735c5-193">Filtre d’URL</span><span class="sxs-lookup"><span data-stu-id="735c5-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="735c5-194">Tapez `-url:` pour masquer les messages de cette URL.</span><span class="sxs-lookup"><span data-stu-id="735c5-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="735c5-195">Il s’agit d’un filtre d’URL négatif.</span><span class="sxs-lookup"><span data-stu-id="735c5-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtre d’URL négatif qui masque tous les messages qui correspondent à https://b.wal.co l’URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="735c5-197">Filtre d’URL négatif qui masque tous les messages qui correspondent à `https://b.wal.co` l’URL</span><span class="sxs-lookup"><span data-stu-id="735c5-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="735c5-198">Vous pouvez également afficher les messages à partir d’une URL unique en ouvrant la barre latérale de la [console,](#open-the-console-sidebar)en développez la section **Messages** utilisateur, puis enchoosant l’URL du script contenant les messages sur lesquels vous souhaitez vous concentrer.</span><span class="sxs-lookup"><span data-stu-id="735c5-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and thenchoosing the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Afficher les messages provenant de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="735c5-200">Afficher les messages d’où ils sont issus</span><span class="sxs-lookup"><span data-stu-id="735c5-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="735c5-201">Filtrer les messages à partir de différents contextes</span><span class="sxs-lookup"><span data-stu-id="735c5-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="735c5-202">Supposons que vous avez une annonce \(ad\) sur votre page.</span><span class="sxs-lookup"><span data-stu-id="735c5-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="735c5-203">La publicitaire est incorporée dans une console et génère un `<iframe>` grand nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="735c5-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="735c5-204">Étant donné que la publicitaire s’exécute dans un contexte [JavaScript](#select-javascript-context)différent, une façon de masquer les messages consiste à ouvrir les [paramètres](#open-console-settings) de la console et à activer la case à cocher Contexte **uniquement** sélectionné.</span><span class="sxs-lookup"><span data-stu-id="735c5-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and turn on the **Selected Context Only** checkbox.</span></span>  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a><span data-ttu-id="735c5-205">Filtrer les messages qui ne correspondent pas à un modèle d’expression régulière</span><span class="sxs-lookup"><span data-stu-id="735c5-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="735c5-206">Tapez une expression régulière telle que dans la zone de texte Filtrer pour filtrer les messages qui ne `/[gm][ta][mi]/` correspondent pas à ce modèle. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="735c5-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="735c5-207">DevTools vérifie si le modèle est trouvé dans le texte du message ou dans le script à l’origine de la consigner.</span><span class="sxs-lookup"><span data-stu-id="735c5-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrer tous les messages qui ne correspondent pas à l’expression regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="735c5-209">Filtrer les messages qui ne correspondent pas à `/[gm][ta][mi]/` l’expression regex</span><span class="sxs-lookup"><span data-stu-id="735c5-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="735c5-210">Exécuter JavaScript</span><span class="sxs-lookup"><span data-stu-id="735c5-210">Run JavaScript</span></span>  

<span data-ttu-id="735c5-211">Cette section contient des fonctionnalités liées à l’exécution de JavaScript dans la console.</span><span class="sxs-lookup"><span data-stu-id="735c5-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="735c5-212">Pour une walkthrough pratique, accédez à [Exécuter JavaScript][DevToolsConsoleOverviewJavascript].</span><span class="sxs-lookup"><span data-stu-id="735c5-212">For a hands-on walkthrough, navigate to [Run JavaScript][DevToolsConsoleOverviewJavascript].</span></span>  

### <a name="re-run-expressions-from-history"></a><span data-ttu-id="735c5-213">Ré-exécuter des expressions à partir de l’historique</span><span class="sxs-lookup"><span data-stu-id="735c5-213">Re-run expressions from history</span></span>  

<span data-ttu-id="735c5-214">Sélectionnez la clé à utiliser pour passer en cycle de l’historique des expressions JavaScript que vous avez précédemment dans `Up Arrow` la console.</span><span class="sxs-lookup"><span data-stu-id="735c5-214">Select the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="735c5-215">Sélectionnez `Enter` pour exécuter à nouveau cette expression.</span><span class="sxs-lookup"><span data-stu-id="735c5-215">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="735c5-216">Regarder la valeur d’une expression en temps réel avec des expressions en direct</span><span class="sxs-lookup"><span data-stu-id="735c5-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="735c5-217">Si vous vous trouvez en train de taper la même expression JavaScript dans la console à plusieurs reprises, vous trouverez peut-être plus facile de créer une **expression live.**</span><span class="sxs-lookup"><span data-stu-id="735c5-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="735c5-218">Avec **les expressions live,** vous tapez une expression une seule fois, puis vous l’épinglez en haut de votre console.</span><span class="sxs-lookup"><span data-stu-id="735c5-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="735c5-219">La valeur de l’expression est mise à jour en temps quasi réel.</span><span class="sxs-lookup"><span data-stu-id="735c5-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="735c5-220">Accédez à [regarder les valeurs d’expression JavaScript Real-Time avec des expressions live.][DevToolsConsoleLiveExpressions]</span><span class="sxs-lookup"><span data-stu-id="735c5-220">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="disable-eager-evaluation"></a><span data-ttu-id="735c5-221">Désactiver l’évaluation enthousiaste</span><span class="sxs-lookup"><span data-stu-id="735c5-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="735c5-222">Lorsque vous tapez des expressions JavaScript dans la console, **l’évaluation de l’enthousiaste** affiche un aperçu de la valeur de retour de cette expression.</span><span class="sxs-lookup"><span data-stu-id="735c5-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="735c5-223">[Ouvrez les paramètres de](#open-console-settings) la console et désactivez la case à cocher Évaluation de l’adage **pour** désactiver les aperçus de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="735c5-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <a name="disable-autocomplete-from-history"></a><span data-ttu-id="735c5-224">Désactiver la mise encomplet automatique de l’historique</span><span class="sxs-lookup"><span data-stu-id="735c5-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="735c5-225">Lorsque vous tapez une expression, la fenêtre popup de la console de lacomplet automatique affiche les expressions que vous avez déjà écrites.</span><span class="sxs-lookup"><span data-stu-id="735c5-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="735c5-226">Ces expressions sont précédées du `>` caractère.</span><span class="sxs-lookup"><span data-stu-id="735c5-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="735c5-227">[Ouvrez paramètres de](#open-console-settings) \*\*\*\* la console et désactivez la case à cocher De l’historique pour arrêter d’afficher les expressions de votre historique.</span><span class="sxs-lookup"><span data-stu-id="735c5-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="735c5-228">Dans la figure suivante, `document.querySelector('a')` sont des expressions qui ont été `document.querySelector('img')` évaluées précédemment.</span><span class="sxs-lookup"><span data-stu-id="735c5-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="La fenêtre de recomplet automatique affiche les expressions de l’historique" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="735c5-230">La fenêtre de recomplet automatique affiche les expressions de l’historique</span><span class="sxs-lookup"><span data-stu-id="735c5-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <a name="select-javascript-context"></a><span data-ttu-id="735c5-231">Sélectionner un contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="735c5-231">Select JavaScript context</span></span>  

<span data-ttu-id="735c5-232">Par défaut, la liste liste de listes des [][MDNBrowsingContext] contextes **JavaScript** est définie sur **haut,** ce qui représente le contexte de navigation du document principal.</span><span class="sxs-lookup"><span data-stu-id="735c5-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="La dropdown de contexte JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="735c5-234">La **dropdown de contexte JavaScript**</span><span class="sxs-lookup"><span data-stu-id="735c5-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="735c5-235">Supposons que vous avez une vidéo sur votre page incorporée dans un `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="735c5-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="735c5-236">Vous souhaitez exécuter JavaScript afin d’ajuster le DOM de la commande.</span><span class="sxs-lookup"><span data-stu-id="735c5-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="735c5-237">Vous devez tout d’abord sélectionner le contexte de navigation de la nouvelle dans la dropdown Contexte **JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="735c5-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Choisir un autre contexte JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="735c5-239">Choisir un autre contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="735c5-239">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="735c5-240">Effacer la console</span><span class="sxs-lookup"><span data-stu-id="735c5-240">Clear the Console</span></span>  

<span data-ttu-id="735c5-241">Vous pouvez utiliser l’un des flux de travail suivants pour effacer la console :</span><span class="sxs-lookup"><span data-stu-id="735c5-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="735c5-242">Choose **Clear Console** \( Clear Console ![ ][ImageClearConsoleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="735c5-242">Choose **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="735c5-243">Pointez sur un message, ouvrez le menu contextuel \(righ-click\), puis choisissez **Effacer la console.**</span><span class="sxs-lookup"><span data-stu-id="735c5-243">Hover on a message, open the contextual menu \(righ-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="735c5-244">Entrez `clear()` dans la **console,** puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="735c5-244">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="735c5-245">Exécutez `console.clear()` à partir de JavaScript pour votre page web.</span><span class="sxs-lookup"><span data-stu-id="735c5-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="735c5-246">Sélectionnez `Control` + `L` pendant que **la console** est en focus.</span><span class="sxs-lookup"><span data-stu-id="735c5-246">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="735c5-247">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="735c5-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Affichage des messages enregistrés : vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Exécution de JavaScript : vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Commencer à utiliser JavaScript dans la console | Documents Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Regardez les valeurs des expressions JavaScript en temps réel avec les expressions | Documents Microsoft"  
[DevToolsConsoleLog]: ./log.md "Commencer à journalisation des messages dans la console | Documents Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexte de navigation | MDN"  

> [!NOTE]
> <span data-ttu-id="735c5-257">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="735c5-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="735c5-258">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="735c5-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="735c5-260">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="735c5-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
