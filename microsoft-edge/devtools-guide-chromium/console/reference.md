---
description: Référence complète pour chaque fonctionnalité et comportement de l’interface utilisateur de la console dans Microsoft Edge DevTools.
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f14663ca1883c0a81184f9a4fa67ddcbd3f08a24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564524"
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
# <a name="console-reference"></a><span data-ttu-id="4b645-104">Référence de la console</span><span class="sxs-lookup"><span data-stu-id="4b645-104">Console reference</span></span>  

<span data-ttu-id="4b645-105">Cet article est une référence des fonctionnalités liées à Microsoft Edge console DevTools.</span><span class="sxs-lookup"><span data-stu-id="4b645-105">This article is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="4b645-106">Il part du principe que vous êtes déjà familiarisé avec l’utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4b645-106">It assumes you're already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="4b645-107">Si ce n’est pas le cas, accédez à l’exécution de [JavaScript][DevtoolsConsoleConsoleJavascript] dans la console et à la journalisation [des messages dans la console.][DevtoolsConsoleConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="4b645-107">If not, navigate to [Get started with running JavaScript in the Console][DevtoolsConsoleConsoleJavascript] and [Get started with logging messages in the Console][DevtoolsConsoleConsoleLog].</span></span>  

<span data-ttu-id="4b645-108">Si vous recherchez la référence d’API sur des fonctions telles que , accédez à Référence `console.log()` de [l’API console.][DevToolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="4b645-108">If you're looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="4b645-109">Pour obtenir la référence sur des fonctions telles que , accédez à Référence de `monitorEvents()` l’API des [utilitaires de console.][DevToolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="4b645-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="4b645-110">Ouvrir la console</span><span class="sxs-lookup"><span data-stu-id="4b645-110">Open the Console</span></span>  

<span data-ttu-id="4b645-111">Vous pouvez ouvrir la **console en** tant [qu’outil](#open-the-console-tool) dans le volet supérieur ou en tant [qu’outil dans le caisse.](#open-the-console-tool-in-the-drawer)</span><span class="sxs-lookup"><span data-stu-id="4b645-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="4b645-112">Ouvrir l’outil Console</span><span class="sxs-lookup"><span data-stu-id="4b645-112">Open the Console tool</span></span>  

<span data-ttu-id="4b645-113">Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="4b645-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="L’outil Console" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="4b645-115">**L’outil Console**</span><span class="sxs-lookup"><span data-stu-id="4b645-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="4b645-116">Pour ouvrir **l’outil Console** à partir du [menu][DevtoolsCommandMenuIndex]Commande, tapez, puis exécutez la commande Afficher la console qui a le `Console` badge **Panneau** en côté. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b645-116">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Exécutez la commande pour afficher l’outil Console" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="4b645-118">Exécutez la commande pour afficher **l’outil Console**</span><span class="sxs-lookup"><span data-stu-id="4b645-118">Run the command to display the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="4b645-119">Ouvrir l’outil Console dans le caisse</span><span class="sxs-lookup"><span data-stu-id="4b645-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="4b645-120">Sélectionnez `Esc` ou choisissez Personnaliser et contrôler **DevTools** \( \), puis choisissez Afficher le caisse `...` de la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-120">Select `Esc` or choose **Customize and control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Afficher le caisse de la console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="4b645-122">Afficher le caisse de la console</span><span class="sxs-lookup"><span data-stu-id="4b645-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="4b645-123">Le caisse s’ouvre en bas de la fenêtre DevTools, avec l’outil **Console** ouvert.</span><span class="sxs-lookup"><span data-stu-id="4b645-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Outil Console dans le caisse" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="4b645-125">Outil **Console** dans le **caisse**</span><span class="sxs-lookup"><span data-stu-id="4b645-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="4b645-126">Pour ouvrir **l’outil Console** à partir du [menu][DevtoolsCommandMenuIndex]Commande, tapez, puis exécutez la commande Afficher la console qui a le badge à l’aide `Console` de celui-ci. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b645-126">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Exécutez la commande pour afficher l’outil **Console** dans le caisse" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="4b645-128">Exécutez la commande pour afficher **l’outil Console** dans le **caisse**</span><span class="sxs-lookup"><span data-stu-id="4b645-128">Run the command to display the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="4b645-129">Ouvrir la console Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b645-129">Open Console Settings</span></span>  

<span data-ttu-id="4b645-130">Sélectionnez **le bouton Paramètres** console \( Icône Paramètres console ![ ](../media/settings-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="4b645-130">Choose the **Console Settings** \(![Console Settings icon](../media/settings-button-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Console Paramètres" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="4b645-132">Console Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b645-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="4b645-133">Les liens suivants expliquent chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="4b645-133">The following links explain each setting.</span></span>  

*   [<span data-ttu-id="4b645-134">Masquer le réseau</span><span class="sxs-lookup"><span data-stu-id="4b645-134">Hide network</span></span>](#hide-network-messages)  
*   [<span data-ttu-id="4b645-135">Conserver le journal</span><span class="sxs-lookup"><span data-stu-id="4b645-135">Preserve log</span></span>](#persist-messages-across-page-loads)  
*   [<span data-ttu-id="4b645-136">Contexte sélectionné uniquement</span><span class="sxs-lookup"><span data-stu-id="4b645-136">Selected context only</span></span>](#filter-out-messages-from-different-contexts)  
*   [<span data-ttu-id="4b645-137">Groupe similaire</span><span class="sxs-lookup"><span data-stu-id="4b645-137">Group similar</span></span>](#turn-off-message-grouping)  
*   [<span data-ttu-id="4b645-138">Log XMLHttpRequests</span><span class="sxs-lookup"><span data-stu-id="4b645-138">Log XMLHttpRequests</span></span>](#log-xhr-and-fetch-requests)  
*   [<span data-ttu-id="4b645-139">Évaluation enthousiaste</span><span class="sxs-lookup"><span data-stu-id="4b645-139">Eager evaluation</span></span>](#turn-off-eager-evaluation)  
*   [<span data-ttu-id="4b645-140">Autocomplete de l’historique</span><span class="sxs-lookup"><span data-stu-id="4b645-140">Autocomplete from history</span></span>](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="4b645-141">Ouvrir la barre latérale de la console</span><span class="sxs-lookup"><span data-stu-id="4b645-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="4b645-142">Pour afficher la barre **latérale, choisissez** **Afficher la barre latérale de la console** \( Afficher la barre latérale de la console ![ ](../media/show-console-sidebar-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="4b645-142">To display the **Sidebar**, choose **Show console sidebar** \(![Show console sidebar](../media/show-console-sidebar-icon.msft.png)\).</span></span>  <span data-ttu-id="4b645-143">La **barre latérale vous** aide à filtrer.</span><span class="sxs-lookup"><span data-stu-id="4b645-143">The **Sidebar** is helps you filter.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Console Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **<span data-ttu-id="4b645-145">Console Sidebar</span><span class="sxs-lookup"><span data-stu-id="4b645-145">Console Sidebar</span></span>**  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="4b645-146">Afficher les messages</span><span class="sxs-lookup"><span data-stu-id="4b645-146">View messages</span></span>  

<span data-ttu-id="4b645-147">Cette section contient des fonctionnalités qui modifient la présentation des messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="4b645-147">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="4b645-148">Pour une walkthrough pratique, accédez à [Afficher les messages.][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]</span><span class="sxs-lookup"><span data-stu-id="4b645-148">For a hands-on walkthrough, navigate to [View messages][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].</span></span>  

### <a name="turn-off-message-grouping"></a><span data-ttu-id="4b645-149">Désactiver le regroupement de messages</span><span class="sxs-lookup"><span data-stu-id="4b645-149">Turn off message grouping</span></span>  

<span data-ttu-id="4b645-150">Pour désactiver le comportement de regroupement des messages par défaut de la **console,** ouvrez console [Paramètres](#open-console-settings) et cochez la case en regard de **Groupe similaire**.</span><span class="sxs-lookup"><span data-stu-id="4b645-150">To turn off the default message grouping behavior of the **Console**, [open Console Settings](#open-console-settings) and choose the checkbox next to **Group similar**.</span></span>  <span data-ttu-id="4b645-151">Pour obtenir un exemple, accédez [à Log XHR et fetch requests](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="4b645-151">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="4b645-152">Enregistrer les demandes XHR et Fetch</span><span class="sxs-lookup"><span data-stu-id="4b645-152">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="4b645-153">Pour enregistrer toutes les demandes et toutes les demandes sur la console, ouvrez console Paramètres et cochez la case en regard de `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**. \*\*\*\* [](#open-console-settings)</span><span class="sxs-lookup"><span data-stu-id="4b645-153">To log all `XMLHttpRequest` and `Fetch` requests to the **Console** as each happens, [open Console Settings](#open-console-settings) and choose the checkbox next to **Log XMLHttpRequests**.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Log XMLHttpRequest and Fetch requests" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="4b645-155">Journal `XMLHttpRequest` et `Fetch` demandes</span><span class="sxs-lookup"><span data-stu-id="4b645-155">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  

<span data-ttu-id="4b645-156">Le premier message de la figure précédente affiche le comportement de regroupement par défaut de la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-156">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="4b645-157">Persist messages across page loads</span><span class="sxs-lookup"><span data-stu-id="4b645-157">Persist messages across page loads</span></span>  

<span data-ttu-id="4b645-158">Lorsque vous chargez une nouvelle page web, l’action par défaut permet d’effacer la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-158">When you load a new webpage, the default action clears the **Console**.</span></span>  <span data-ttu-id="4b645-159">Pour conserver les messages entre les chargements de page, [ouvrez](#open-console-settings) Paramètres console et cochez la case en regard **de Conserver le journal.**</span><span class="sxs-lookup"><span data-stu-id="4b645-159">To persist messages across page loads, [open Console Settings](#open-console-settings) and choose the checkbox next to **Preserve Log**.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="4b645-160">Masquer les messages réseau</span><span class="sxs-lookup"><span data-stu-id="4b645-160">Hide network messages</span></span>  

<span data-ttu-id="4b645-161">L’action par défaut Microsoft Edge consiste à enregistrer les messages réseau dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-161">The default action for Microsoft Edge is to logs network messages to the **Console**.</span></span>  <span data-ttu-id="4b645-162">Dans la figure suivante, le message choisi représente un code d’état HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="4b645-162">In the following figure, the chosen message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un message 429 dans la console" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="4b645-164">Un `429` message dans la **console**</span><span class="sxs-lookup"><span data-stu-id="4b645-164">A `429` message in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="4b645-165">Pour masquer les messages réseau, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b645-165">To hide network messages, complete the following actions.</span></span>  

1.  <span data-ttu-id="4b645-166">[Ouvrez console Paramètres](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="4b645-166">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="4b645-167">Cochez la case en regard de **Masquer le réseau.**</span><span class="sxs-lookup"><span data-stu-id="4b645-167">Choose the checkbox next to **Hide Network**.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="4b645-168">Filtrer les messages</span><span class="sxs-lookup"><span data-stu-id="4b645-168">Filter messages</span></span>  

<span data-ttu-id="4b645-169">Il existe de nombreuses façons de filtrer les messages dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-169">Many ways exist to filter out messages in the **Console**.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="4b645-170">Filtrer les messages du navigateur</span><span class="sxs-lookup"><span data-stu-id="4b645-170">Filter out browser messages</span></span>  

<span data-ttu-id="4b645-171">[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et choisissez # **messages** utilisateur pour afficher uniquement les messages provenant du JavaScript de la page web.</span><span class="sxs-lookup"><span data-stu-id="4b645-171">[Open the Console Sidebar](#open-the-console-sidebar) and choose **# user messages** to only display messages that came from the JavaScript of the webpage.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Afficher les messages de l’utilisateur" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="4b645-173">Afficher les messages de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4b645-173">Display user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="4b645-174">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="4b645-174">Filter by log level</span></span>  

<span data-ttu-id="4b645-175">DevTools affecte à chaque `console.*` méthode l’un des quatre niveaux de gravité.</span><span class="sxs-lookup"><span data-stu-id="4b645-175">DevTools assigns each `console.*` method one of the four severity levels.</span></span>  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
<span data-ttu-id="4b645-176">Par exemple, `console.log()` se trouve dans le `Info` groupe, mais dans le `console.error()` `Error` groupe.</span><span class="sxs-lookup"><span data-stu-id="4b645-176">For example, `console.log()` is in the `Info` group, but `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="4b645-177">La [référence de l’API][DevToolsConsoleApi] console décrit le niveau de gravité de chaque méthode applicable.</span><span class="sxs-lookup"><span data-stu-id="4b645-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="4b645-178">Chaque message journal de la console par le navigateur présente également un niveau de gravité.</span><span class="sxs-lookup"><span data-stu-id="4b645-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="4b645-179">Vous pouvez masquer n’importe quel niveau de messages qui ne vous intéresse pas.</span><span class="sxs-lookup"><span data-stu-id="4b645-179">You may hide any level of messages that you're not interested in.</span></span>  <span data-ttu-id="4b645-180">Par exemple, si seuls les messages vous `Error` intéressent, vous pouvez masquer les trois autres groupes.</span><span class="sxs-lookup"><span data-stu-id="4b645-180">For example, if you're only interested in `Error` messages, you may hide the other three groups.</span></span>  

<span data-ttu-id="4b645-181">Pour filtrer les messages, sélectionnez la dropdown **Niveaux** de journal et `Verbose` choisissez , ou `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="4b645-181">To filter the messages, choose the **Log Levels** dropdown and choose `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="La dropdown Log Levels" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="4b645-183">La **dropdown Log Levels**</span><span class="sxs-lookup"><span data-stu-id="4b645-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="4b645-184">Pour utiliser le niveau de journal pour filtrer, ouvrez la barre latérale de la [console,](#open-the-console-sidebar) puis choisissez **Erreurs, Avertissements,** **Informations**ou **Détaillé.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b645-184">To use the log level to filter, [open the Console Sidebar](#open-the-console-sidebar) and then choose **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Utiliser la barre latérale pour afficher les avertissements" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="4b645-186">Utiliser la barre latérale pour afficher les avertissements</span><span class="sxs-lookup"><span data-stu-id="4b645-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="4b645-187">Filtrer les messages par URL</span><span class="sxs-lookup"><span data-stu-id="4b645-187">Filter messages by URL</span></span>  

<span data-ttu-id="4b645-188">Tapez `url:` suivi d’une URL pour afficher uniquement les messages provenant de cette URL.</span><span class="sxs-lookup"><span data-stu-id="4b645-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="4b645-189">Une fois que `url:` vous avez tapé, DevTools affiche toutes les URL pertinentes.</span><span class="sxs-lookup"><span data-stu-id="4b645-189">After you type `url:`, DevTools displays all relevant URLs.</span></span>  <span data-ttu-id="4b645-190">Les domaines fonctionnent également.</span><span class="sxs-lookup"><span data-stu-id="4b645-190">Domains also work.</span></span>  <span data-ttu-id="4b645-191">Par exemple, si et journalisation des messages, vous permet de vous concentrer sur les messages de `https://example.com/a.js` `https://example.com/b.js` ces deux `url:https://example.com` scripts.</span><span class="sxs-lookup"><span data-stu-id="4b645-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` allows you to focus on the messages from these two scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Un filtre d’URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="4b645-193">Un filtre d’URL</span><span class="sxs-lookup"><span data-stu-id="4b645-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="4b645-194">Pour masquer les messages d’une URL, tapez `-url:` .</span><span class="sxs-lookup"><span data-stu-id="4b645-194">To hide messages from a URL, type `-url:`.</span></span>  <span data-ttu-id="4b645-195">Il s’agit d’un filtre d’URL négatif.</span><span class="sxs-lookup"><span data-stu-id="4b645-195">It's a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtre d’URL négatif qui masque tous les messages qui correspondent à https://b.wal.co l’URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="4b645-197">Filtre d’URL négatif qui masque tous les messages qui correspondent à `https://b.wal.co` l’URL</span><span class="sxs-lookup"><span data-stu-id="4b645-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="4b645-198">Pour afficher des messages à partir d’une URL unique, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b645-198">To display messages from a single URL, complete the following actions.</span></span>  

1.  <span data-ttu-id="4b645-199">[Ouvrez la barre latérale de la console.](#open-the-console-sidebar)</span><span class="sxs-lookup"><span data-stu-id="4b645-199">[Open the Console Sidebar](#open-the-console-sidebar).</span></span>  
1.  <span data-ttu-id="4b645-200">Développez la section **# messages de l’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="4b645-200">Expand the **# user messages** section.</span></span>  
1.  <span data-ttu-id="4b645-201">Choisissez l’URL du script qui contient les messages sur lesquels vous souhaitez vous concentrer.</span><span class="sxs-lookup"><span data-stu-id="4b645-201">Choose the URL of the script that contains the messages on which you want to focus.</span></span>  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Afficher les messages provenant de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="4b645-203">Afficher les messages d’où ils sont issus</span><span class="sxs-lookup"><span data-stu-id="4b645-203">Display the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="4b645-204">Filtrer les messages à partir de différents contextes</span><span class="sxs-lookup"><span data-stu-id="4b645-204">Filter out messages from different contexts</span></span>  

<span data-ttu-id="4b645-205">Supposons que vous avez une annonce \(ad\) sur votre page web.</span><span class="sxs-lookup"><span data-stu-id="4b645-205">Suppose that you have an advertisement \(ad\) on your webpage.</span></span>  <span data-ttu-id="4b645-206">La publicitaire est incorporée dans un `<iframe>` et génère de nombreux messages dans votre **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-206">The ad is embedded in an `<iframe>` and generates many messages in your **Console**.</span></span>  <span data-ttu-id="4b645-207">Étant donné que la publicitaire s’exécute dans un contexte [JavaScript](#choose-javascript-context)différent, une façon de masquer les messages consiste à ouvrir la [console Paramètres](#open-console-settings) et à cocher la case en regard du contexte **sélectionné uniquement.**</span><span class="sxs-lookup"><span data-stu-id="4b645-207">Because the ad is running in a different [JavaScript context](#choose-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and choose the checkbox next to **Selected Context Only**.</span></span>  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a><span data-ttu-id="4b645-208">Filtrer les messages qui ne correspondent pas à un modèle d’expression régulière</span><span class="sxs-lookup"><span data-stu-id="4b645-208">Filter out messages that don't match a regular expression pattern</span></span>  

<span data-ttu-id="4b645-209">Tapez une expression régulière telle que dans la boîte de texte Filtre pour filtrer les messages qui ne correspondent `/[gm][ta][mi]/` pas à ce modèle. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b645-209">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** textbox to filter out any messages that don't match that pattern.</span></span>  <span data-ttu-id="4b645-210">DevTools vérifie si le modèle est trouvé dans le texte du message ou dans le script à l’origine de la consigner.</span><span class="sxs-lookup"><span data-stu-id="4b645-210">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrer les messages qui ne correspondent pas à l’expression regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="4b645-212">Filtrer les messages qui ne correspondent pas à `/[gm][ta][mi]/` l’expression regex</span><span class="sxs-lookup"><span data-stu-id="4b645-212">Filter out any messages that don't match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="4b645-213">Exécuter JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b645-213">Run JavaScript</span></span>  

<span data-ttu-id="4b645-214">Cette section contient des fonctionnalités liées à l’exécution de JavaScript dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-214">This section contains features related to running JavaScript in the **Console**.</span></span>  <span data-ttu-id="4b645-215">Pour une walkthrough pratique, accédez à [Exécuter JavaScript][DevtoolsConsoleConsoleJavascript].</span><span class="sxs-lookup"><span data-stu-id="4b645-215">For a hands-on walkthrough, navigate to [Run JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  

### <a name="rerun-expressions-from-history"></a><span data-ttu-id="4b645-216">Réexécuter des expressions à partir de l’historique</span><span class="sxs-lookup"><span data-stu-id="4b645-216">Rerun expressions from history</span></span>  

<span data-ttu-id="4b645-217">Sélectionnez `Up Arrow` pour passer en cycle l’historique des expressions JavaScript que vous avez précédemment dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-217">Select `Up Arrow` to cycle through the history of JavaScript expressions that you ran earlier in the **Console**.</span></span>  <span data-ttu-id="4b645-218">Sélectionnez `Enter` pour exécuter à nouveau cette expression.</span><span class="sxs-lookup"><span data-stu-id="4b645-218">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="4b645-219">Regarder la valeur d’une expression en temps réel avec des expressions live</span><span class="sxs-lookup"><span data-stu-id="4b645-219">Watch the value of an expression in real time with Live Expressions</span></span>  

<span data-ttu-id="4b645-220">Si vous vous trouvez en train de taper la même expression JavaScript dans la **console** à plusieurs reprises, vous trouverez peut-être plus facile de créer une **expression live.**</span><span class="sxs-lookup"><span data-stu-id="4b645-220">If you find yourself typing the same JavaScript expression in the **Console** repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="4b645-221">Avec **les expressions live,** vous tapez une expression une fois, puis vous l’épinglez en haut de votre **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-221">With **Live Expressions**, you type an expression once and then pin it to the top of your **Console**.</span></span>  <span data-ttu-id="4b645-222">La valeur de l’expression est mise à jour en temps quasi réel.</span><span class="sxs-lookup"><span data-stu-id="4b645-222">The value of the expression updates in near real time.</span></span>  <span data-ttu-id="4b645-223">Accédez à [regarder les valeurs d’expression JavaScript Real-Time avec des expressions live.][DevToolsConsoleLiveExpressions]</span><span class="sxs-lookup"><span data-stu-id="4b645-223">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="turn-off-eager-evaluation"></a><span data-ttu-id="4b645-224">Désactiver l’évaluation enthousiaste</span><span class="sxs-lookup"><span data-stu-id="4b645-224">Turn off Eager Evaluation</span></span>  

<span data-ttu-id="4b645-225">**L’évaluation** enthousiaste affiche un aperçu de la valeur de retour lorsque vous tapez des expressions JavaScript dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-225">**Eager Evaluation** displays a preview of the return value as you type JavaScript expressions in the **Console**.</span></span>  <span data-ttu-id="4b645-226">Pour désactiver les aperçus de valeur de retour, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b645-226">To turn off the return value previews, complete the following actions.</span></span>  

1.  <span data-ttu-id="4b645-227">[Ouvrez console Paramètres](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="4b645-227">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="4b645-228">Supprimez la case à cocher en regard **de l’évaluation enthousiaste.**</span><span class="sxs-lookup"><span data-stu-id="4b645-228">Remove the checkbox next to **Eager Evaluation**.</span></span>  
    
### <a name="turn-off-autocomplete-from-history"></a><span data-ttu-id="4b645-229">Désactiver la mise encomplet automatique de l’historique</span><span class="sxs-lookup"><span data-stu-id="4b645-229">Turn off autocomplete from history</span></span>  

<span data-ttu-id="4b645-230">Lorsque vous tapez une expression, la fenêtre popup de la console de mise à jour automatique affiche les expressions que vous avez précédemment entrées. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b645-230">As you type out an expression, the autocomplete popup window for the **Console** displays expressions that you ran earlier.</span></span>  <span data-ttu-id="4b645-231">Les expressions sont pré-pendées avec le `>` caractère.</span><span class="sxs-lookup"><span data-stu-id="4b645-231">The expressions are pre-pended with the `>` character.</span></span>  <span data-ttu-id="4b645-232">Pour arrêter d’afficher les expressions de votre historique, ouvrez \*\*\*\* la [Paramètres](#open-console-settings) console et supprimez la case à cocher en regard de la case à cocher De l’historique de la mise à jour automatique.</span><span class="sxs-lookup"><span data-stu-id="4b645-232">To stop displaying expressions from your history, [open Console Settings](#open-console-settings) and remove the checkbox next to **Autocomplete From History** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="4b645-233">Dans la figure suivante, `document.querySelector('a')` sont des expressions qui ont été `document.querySelector('img')` évaluées précédemment.</span><span class="sxs-lookup"><span data-stu-id="4b645-233">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Le menu popup de la mise à jour automatique affiche les expressions de l’historique" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="4b645-235">Le menu popup de la mise à jour automatique affiche les expressions de l’historique</span><span class="sxs-lookup"><span data-stu-id="4b645-235">The autocomplete popup menu displays expressions from history</span></span>  
:::image-end:::  

### <a name="choose-javascript-context"></a><span data-ttu-id="4b645-236">Choisir le contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b645-236">Choose JavaScript context</span></span>  

<span data-ttu-id="4b645-237">L’option par défaut pour la liste de listes des contextes **JavaScript** est **supérieure,** ce qui représente le contexte de navigation [de][MdnDocsGlossaryBrowsingContext] la page web principale.</span><span class="sxs-lookup"><span data-stu-id="4b645-237">The default option for the **JavaScript Context** dropdown is **top**, which represents the [browsing context][MdnDocsGlossaryBrowsingContext] of the main webpage.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="La dropdown de contexte JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="4b645-239">La **dropdown de contexte JavaScript**</span><span class="sxs-lookup"><span data-stu-id="4b645-239">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="4b645-240">Supposons que vous avez une vidéo sur votre page web incorporée dans un `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="4b645-240">Suppose you have an ad on your webpage embedded in an `<iframe>`.</span></span>  <span data-ttu-id="4b645-241">Vous souhaitez exécuter JavaScript pour ajuster le DOM de l’ad.</span><span class="sxs-lookup"><span data-stu-id="4b645-241">You want to run JavaScript to tweak the DOM of the ad.</span></span>  <span data-ttu-id="4b645-242">Tout d’abord, choisissez le contexte de navigation de la nouvelle dans la description du **contexte JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="4b645-242">First, choose the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Choisir un autre contexte JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="4b645-244">Choisir un autre contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b645-244">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="4b645-245">Effacer la console</span><span class="sxs-lookup"><span data-stu-id="4b645-245">Clear the Console</span></span>  

<span data-ttu-id="4b645-246">Pour effacer la **console,** terminez l’un des flux de travail suivants.</span><span class="sxs-lookup"><span data-stu-id="4b645-246">To clear the **Console**, complete any of the following workflows.</span></span>  

*   <span data-ttu-id="4b645-247">Choisissez le **bouton Effacer la console** \( Effacer la console ![ ](../media/clear-console-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="4b645-247">Choose the **Clear Console** \(![Clear Console](../media/clear-console-button-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="4b645-248">Pointez sur un message, ouvrez le menu contextuel \(clic droit\), puis choisissez **Effacer la console.**</span><span class="sxs-lookup"><span data-stu-id="4b645-248">Hover on a message, open the contextual menu \(right-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="4b645-249">Entrez `clear()` dans la **console,** puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4b645-249">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="4b645-250">Exécutez `console.clear()` à partir de JavaScript pour votre page web.</span><span class="sxs-lookup"><span data-stu-id="4b645-250">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="4b645-251">Sélectionnez `Control` + `L` pendant que **la console** est en focus.</span><span class="sxs-lookup"><span data-stu-id="4b645-251">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4b645-252">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="4b645-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Journal des messages dans l’outil console | Documents Microsoft"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console en tant qu’environnement JavaScript | Documents Microsoft"  
[DevtoolsConsoleIndex]: .index.md "Utiliser la console | Documents Microsoft"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Inspecter et filtrer les informations sur la page web | Documents Microsoft"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Surveiller les modifications apportées dans JavaScript à l’aide d’expressions | Documents Microsoft"  
[DevtoolsConsoleUtilities]: ./utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu Microsoft Edge commande DevTools | Documents Microsoft"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexte de navigation | MDN"  

> [!NOTE]
> <span data-ttu-id="4b645-262">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4b645-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4b645-263">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4b645-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="4b645-265">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4b645-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
