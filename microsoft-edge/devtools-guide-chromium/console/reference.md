---
description: Référence complète sur chaque fonctionnalité et chaque comportement liés à l’interface utilisateur de la console dans Microsoft Edge DevTools.
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6a79031e6efbc4b83b83685f32e060a6268dbb2a
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993141"
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





# <span data-ttu-id="b0948-104">Référence de la console</span><span class="sxs-lookup"><span data-stu-id="b0948-104">Console Reference</span></span>   



<span data-ttu-id="b0948-105">Cette page est une référence des fonctionnalités liées à la console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0948-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="b0948-106">Il part du principe que vous connaissez déjà l’utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b0948-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="b0948-107">Si ce n’est pas le cas, voir [prendre en main JavaScript dans la console][DevToolsConsoleJavascript] et [commencer à utiliser les messages de journalisation dans la console][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="b0948-107">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="b0948-108">Si vous recherchez la référence de l’API sur des fonctions telles que voir référence sur l’API de la `console.log()` [console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="b0948-108">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="b0948-109">Pour obtenir une référence sur les fonctions telles que `monitorEvents()` , consultez la [référence des API d’utilitaires de console][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="b0948-109">For the reference on functions like `monitorEvents()`, see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="b0948-110">Ouvrez la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-110">Open the Console</span></span>   

<span data-ttu-id="b0948-111">Vous pouvez ouvrir la console en tant que [panneau](#open-the-console-panel) ou en tant qu' [onglet dans le tiroir](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="b0948-111">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="b0948-112">Ouvrir l’écran de la console</span><span class="sxs-lookup"><span data-stu-id="b0948-112">Open the Console panel</span></span>   

<span data-ttu-id="b0948-113">Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="b0948-113">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Panneau de la console" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="b0948-115">Panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="b0948-115">The **Console** panel</span></span>  
:::image-end:::  

<span data-ttu-id="b0948-116">Pour ouvrir le panneau console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande Afficher la **console** contenant le badge du **panneau** .</span><span class="sxs-lookup"><span data-stu-id="b0948-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Commande pour afficher le panneau de la console" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="b0948-118">Commande pour afficher le panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="b0948-118">The command to show the **Console** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="b0948-119">Ouvrir l’onglet de console dans le tiroir</span><span class="sxs-lookup"><span data-stu-id="b0948-119">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="b0948-120">Appuyez `Escape` ou cliquez sur **personnaliser et contrôler devtools** \ ( `...` \), puis sélectionnez **afficher le tiroir**de la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-120">Press `Escape` or click **Customize And Control DevTools** \(`...`\) and then select **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Afficher le tiroir de la console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="b0948-122">Afficher le tiroir de la console</span><span class="sxs-lookup"><span data-stu-id="b0948-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="b0948-123">Le tiroir apparaît en bas de la fenêtre de DevTools, avec l’onglet **console** ouvert.</span><span class="sxs-lookup"><span data-stu-id="b0948-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Onglet Console du tiroir" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="b0948-125">Onglet **console** du **tiroir**</span><span class="sxs-lookup"><span data-stu-id="b0948-125">The **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="b0948-126">Pour ouvrir l’onglet de la console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande **afficher la console** dont le badge est associé au **tiroir** .</span><span class="sxs-lookup"><span data-stu-id="b0948-126">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Commande d’affichage de l’onglet de la console dans le tiroir" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="b0948-128">Commande d’affichage de l’onglet de la **console** dans le **tiroir**</span><span class="sxs-lookup"><span data-stu-id="b0948-128">The command to show the **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

### <span data-ttu-id="b0948-129">Ouvrir les paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="b0948-129">Open Console Settings</span></span>   

<span data-ttu-id="b0948-130">Cliquez sur paramètres de la **console** \ (paramètres de la ![ console ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b0948-130">Click **Console Settings** \(![Console Settings][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Paramètres de la console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="b0948-132">Paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="b0948-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="b0948-133">Les liens ci-dessous décrivent chaque paramètre:</span><span class="sxs-lookup"><span data-stu-id="b0948-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="b0948-134">Masquer le réseau</span><span class="sxs-lookup"><span data-stu-id="b0948-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="b0948-135">Conserver le journal</span><span class="sxs-lookup"><span data-stu-id="b0948-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="b0948-136">Contexte sélectionné uniquement</span><span class="sxs-lookup"><span data-stu-id="b0948-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="b0948-137">Groupe similaire</span><span class="sxs-lookup"><span data-stu-id="b0948-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="b0948-138">Enregistrer les fichiers XmlHttpRequest</span><span class="sxs-lookup"><span data-stu-id="b0948-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="b0948-139">Évaluation hâtif</span><span class="sxs-lookup"><span data-stu-id="b0948-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="b0948-140">Saisie semi-automatique dans l’historique</span><span class="sxs-lookup"><span data-stu-id="b0948-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <span data-ttu-id="b0948-141">Ouvrir la barre latérale de la console</span><span class="sxs-lookup"><span data-stu-id="b0948-141">Open the Console Sidebar</span></span>   

<span data-ttu-id="b0948-142">Cliquez sur **afficher la barre latérale** de la console \ ( ![ afficher barre latérale ][ImageShowConsoleSidebarIcon] \) pour afficher la barre latérale, qui est utile pour le filtrage.</span><span class="sxs-lookup"><span data-stu-id="b0948-142">Click **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barre latérale de la console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="b0948-144">**Console** Gadget</span><span class="sxs-lookup"><span data-stu-id="b0948-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <span data-ttu-id="b0948-145">Afficher des messages</span><span class="sxs-lookup"><span data-stu-id="b0948-145">View messages</span></span>   

<span data-ttu-id="b0948-146">Cette section contient des fonctionnalités qui changent le mode d’affichage des messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="b0948-147">Pour obtenir une procédure pas à pas, voir [afficher les messages][DevToolsConsoleViewMessages] .</span><span class="sxs-lookup"><span data-stu-id="b0948-147">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="b0948-148">Désactiver le regroupement des messages</span><span class="sxs-lookup"><span data-stu-id="b0948-148">Disable message grouping</span></span>   

<span data-ttu-id="b0948-149">[Ouvrez les paramètres](#open-console-settings) de la console et désactivez l’option groupe, de la **même façon** que le comportement de regroupement des messages par défaut de la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="b0948-150">Pour obtenir un exemple [, voir journaux de XHR et récupérer des requêtes](#log-xhr-and-fetch-requests) .</span><span class="sxs-lookup"><span data-stu-id="b0948-150">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="b0948-151">Journalisation des requêtes XHR et FETCH</span><span class="sxs-lookup"><span data-stu-id="b0948-151">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="b0948-152">[Ouvrez les paramètres](#open-console-settings) de la console et activez le **Journal** des utilisateurs pour enregistrer toutes les `XMLHttpRequest` `Fetch` demandes de la console en temps réel.</span><span class="sxs-lookup"><span data-stu-id="b0948-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Enregistrer les demandes de fichiers XMLHttpRequest et FETCH" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="b0948-154">Journalisation `XMLHttpRequest` et `Fetch` demandes</span><span class="sxs-lookup"><span data-stu-id="b0948-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="b0948-155">Le message supérieur de la figure précédente affiche le comportement de regroupement par défaut de la **console**.</span><span class="sxs-lookup"><span data-stu-id="b0948-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="b0948-156">Faire persister des messages au chargement de la page</span><span class="sxs-lookup"><span data-stu-id="b0948-156">Persist messages across page loads</span></span>   

<span data-ttu-id="b0948-157">Par défaut, la console est effacée dès que vous chargez une nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="b0948-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="b0948-158">Pour conserver les messages au cours du chargement de la page, [cliquez sur paramètres](#open-console-settings) de la console, puis activez la case à cocher conserver le **Journal** .</span><span class="sxs-lookup"><span data-stu-id="b0948-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="b0948-159">Masquer les messages réseau</span><span class="sxs-lookup"><span data-stu-id="b0948-159">Hide network messages</span></span>   

<span data-ttu-id="b0948-160">Par défaut, le navigateur enregistre les messages réseau sur la **console**.</span><span class="sxs-lookup"><span data-stu-id="b0948-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="b0948-161">Dans l’illustration suivante, le message sélectionné représente un code d’état HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="b0948-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Message 429 dans la console" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="b0948-163">`429`Message sur la **console**</span><span class="sxs-lookup"><span data-stu-id="b0948-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="b0948-164">Pour masquer les messages réseau:</span><span class="sxs-lookup"><span data-stu-id="b0948-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="b0948-165">[Ouvrez paramètres](#open-console-settings)de la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="b0948-166">Activez la case à cocher **masquer le réseau** .</span><span class="sxs-lookup"><span data-stu-id="b0948-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <span data-ttu-id="b0948-167">Filtrer les messages</span><span class="sxs-lookup"><span data-stu-id="b0948-167">Filter messages</span></span>   

<span data-ttu-id="b0948-168">Il existe de nombreuses façons de filtrer les messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-168">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="b0948-169">Filtrer les messages du navigateur</span><span class="sxs-lookup"><span data-stu-id="b0948-169">Filter out browser messages</span></span>   

<span data-ttu-id="b0948-170">[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et cliquez sur **messages utilisateur** pour afficher uniquement les messages provenant du JavaScript de la page.</span><span class="sxs-lookup"><span data-stu-id="b0948-170">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Afficher les messages des utilisateurs" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="b0948-172">Afficher les messages des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b0948-172">View user messages</span></span>  
:::image-end:::  

### <span data-ttu-id="b0948-173">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="b0948-173">Filter by log level</span></span>   

<span data-ttu-id="b0948-174">DevTools affecte chaque `console.*` méthode un niveau de gravité.</span><span class="sxs-lookup"><span data-stu-id="b0948-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="b0948-175">Il y a 4 niveaux: `Verbose` ,, `Info` `Warning` et `Error` .</span><span class="sxs-lookup"><span data-stu-id="b0948-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="b0948-176">Par exemple, `console.log()` se trouve dans le `Info` groupe, alors qu’il `console.error()` se trouve dans le `Error` groupe.</span><span class="sxs-lookup"><span data-stu-id="b0948-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="b0948-177">La [référence de l’API console][DevToolsConsoleApi] décrit le niveau de gravité de chaque méthode applicable.</span><span class="sxs-lookup"><span data-stu-id="b0948-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="b0948-178">Les messages que le navigateur enregistre sur la console ont également un niveau de gravité.</span><span class="sxs-lookup"><span data-stu-id="b0948-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="b0948-179">Vous pouvez masquer tous les niveaux de messages qui ne vous intéressent pas.</span><span class="sxs-lookup"><span data-stu-id="b0948-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="b0948-180">Par exemple, si vous êtes intéressé uniquement par les `Error` messages, vous pouvez masquer les 3 autres groupes.</span><span class="sxs-lookup"><span data-stu-id="b0948-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="b0948-181">Cliquez sur la liste déroulante **niveaux du journal** pour activer ou désactiver ou `Verbose` `Info` `Warning` `Error` messages.</span><span class="sxs-lookup"><span data-stu-id="b0948-181">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Liste déroulante niveaux du journal" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="b0948-183">Liste déroulante **niveaux du journal**</span><span class="sxs-lookup"><span data-stu-id="b0948-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="b0948-184">Vous pouvez également filtrer par niveau de journal en [ouvrant la barre latérale de la console](#open-the-console-sidebar) , puis en cliquant sur **erreurs**, **avertissements**, **informations**ou **Commentaires**.</span><span class="sxs-lookup"><span data-stu-id="b0948-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Utiliser la barre latérale pour afficher les avertissements" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="b0948-186">Utiliser la barre latérale pour afficher les avertissements</span><span class="sxs-lookup"><span data-stu-id="b0948-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <span data-ttu-id="b0948-187">Filtrer les messages par URL</span><span class="sxs-lookup"><span data-stu-id="b0948-187">Filter messages by URL</span></span>   

<span data-ttu-id="b0948-188">Tapez `url:` suivi d’une URL pour afficher uniquement les messages provenant de cette URL.</span><span class="sxs-lookup"><span data-stu-id="b0948-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="b0948-189">Après que vous avez tapé `url:` devtools affiche toutes les URL pertinentes.</span><span class="sxs-lookup"><span data-stu-id="b0948-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="b0948-190">Les domaines fonctionnent également.</span><span class="sxs-lookup"><span data-stu-id="b0948-190">Domains also work.</span></span>  <span data-ttu-id="b0948-191">Par exemple, si `https://example.com/a.js` `https://example.com/b.js` vous consignez des messages, `url:https://example.com` vous pouvez vous concentrer sur les messages de ces deux scripts.</span><span class="sxs-lookup"><span data-stu-id="b0948-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Filtre d’URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="b0948-193">Filtre d’URL</span><span class="sxs-lookup"><span data-stu-id="b0948-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="b0948-194">Entrez `-url:` pour masquer les messages de cette URL.</span><span class="sxs-lookup"><span data-stu-id="b0948-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="b0948-195">Ce filtre est appelé filtre d’URL négatif.</span><span class="sxs-lookup"><span data-stu-id="b0948-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Un filtre d’URL négatif masquant tous les messages correspondant à l' https://b.wal.co URL;" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="b0948-197">Un filtre d’URL négatif masquant tous les messages correspondant à l' `https://b.wal.co` URL;</span><span class="sxs-lookup"><span data-stu-id="b0948-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="b0948-198">Vous pouvez également afficher les messages d’une URL unique en [ouvrant la barre latérale](#open-the-console-sidebar)de la console, en développant la section messages de l' **utilisateur** , puis en cliquant sur l’URL du script contenant les messages sur lesquels vous souhaitez vous concentrer.</span><span class="sxs-lookup"><span data-stu-id="b0948-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Afficher les messages issus de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="b0948-200">Afficher les messages de</span><span class="sxs-lookup"><span data-stu-id="b0948-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <span data-ttu-id="b0948-201">Filtrer les messages de différents contextes</span><span class="sxs-lookup"><span data-stu-id="b0948-201">Filter out messages from different contexts</span></span>   

<span data-ttu-id="b0948-202">Imaginons que vous ayez une annonce (publicité) sur votre page.</span><span class="sxs-lookup"><span data-stu-id="b0948-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="b0948-203">La publicité est incorporée dans un `<iframe>` et génère un grand nombre de messages dans votre console.</span><span class="sxs-lookup"><span data-stu-id="b0948-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="b0948-204">Dans la mesure où la publicité s’exécute dans un autre [contexte JavaScript](#select-javascript-context), une façon de masquer les messages consiste à [ouvrir les paramètres](#open-console-settings) de la console et à activer la case à cocher **contexte sélectionnée uniquement** .</span><span class="sxs-lookup"><span data-stu-id="b0948-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="b0948-205">Filtrer les messages qui ne correspondent pas à un modèle d’expression régulière</span><span class="sxs-lookup"><span data-stu-id="b0948-205">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="b0948-206">Tapez une expression régulière telle que `/[gm][ta][mi]/` dans la zone de texte de **filtre** pour filtrer les messages ne correspondant pas à ce modèle.</span><span class="sxs-lookup"><span data-stu-id="b0948-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="b0948-207">DevTools vérifie si le modèle se trouve dans le texte du message ou dans le script qui a entraîné la journalisation du message.</span><span class="sxs-lookup"><span data-stu-id="b0948-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrer les messages ne correspondant pas à l’expression Regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="b0948-209">Filtrer les messages ne correspondant pas à l' `/[gm][ta][mi]/` expression Regex</span><span class="sxs-lookup"><span data-stu-id="b0948-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <span data-ttu-id="b0948-210">Exécuter JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0948-210">Run JavaScript</span></span>   

<span data-ttu-id="b0948-211">Cette section contient des fonctionnalités relatives à l’exécution de JavaScript dans la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="b0948-212">Pour obtenir une procédure pas à pas, voir [exécuter JavaScript][DevToolsConsoleOverviewJavascript] .</span><span class="sxs-lookup"><span data-stu-id="b0948-212">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="b0948-213">Réexécuter des expressions à partir de l’historique</span><span class="sxs-lookup"><span data-stu-id="b0948-213">Re-run expressions from history</span></span>   

<span data-ttu-id="b0948-214">Appuyez sur la `Up Arrow` touche pour parcourir l’historique des expressions JavaScript que vous avez exécutées auparavant dans la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-214">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="b0948-215">Appuyez sur `Enter` pour réexécuter cette expression.</span><span class="sxs-lookup"><span data-stu-id="b0948-215">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="b0948-216">Regardez la valeur d’une expression en temps réel avec des expressions dynamiques</span><span class="sxs-lookup"><span data-stu-id="b0948-216">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="b0948-217">Si vous vous intentez de taper la même expression JavaScript dans la console à plusieurs reprises, il est possible que vous puissiez constater qu’il est plus facile de créer une **expression dynamique**.</span><span class="sxs-lookup"><span data-stu-id="b0948-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="b0948-218">Dans les **expressions dynamiques** , vous tapez une expression une seule fois, puis épinglez celle-ci en haut de votre console.</span><span class="sxs-lookup"><span data-stu-id="b0948-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="b0948-219">La valeur de l’expression est mise à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="b0948-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="b0948-220">Voir [valeurs d’expression JavaScript en temps réel avec des expressions dynamiques][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="b0948-220">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="b0948-221">Désactiver l’évaluation hâtif</span><span class="sxs-lookup"><span data-stu-id="b0948-221">Disable Eager Evaluation</span></span>   

<span data-ttu-id="b0948-222">Lorsque vous tapez des expressions JavaScript dans la console, l' **évaluation hâtif** affiche un aperçu de la valeur de retour pour cette expression.</span><span class="sxs-lookup"><span data-stu-id="b0948-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="b0948-223">[Ouvrez paramètres](#open-console-settings) de la console et désactivez la case à cocher **évaluation hâtif** pour désactiver les aperçus des valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="b0948-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="b0948-224">Désactiver la saisie semi-automatique dans l’historique</span><span class="sxs-lookup"><span data-stu-id="b0948-224">Disable autocomplete from history</span></span>   

<span data-ttu-id="b0948-225">Lors de la saisie d’une expression, la fenêtre contextuelle de saisie semi-automatique de la console affiche les expressions que vous avez exécutées auparavant.</span><span class="sxs-lookup"><span data-stu-id="b0948-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="b0948-226">Ces expressions sont précédées du `>` caractère.</span><span class="sxs-lookup"><span data-stu-id="b0948-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="b0948-227">[Ouvrez paramètres](#open-console-settings) de la console et désactivez l’option **saisie semi-automatique de l’historique** pour ne plus afficher les expressions de votre historique.</span><span class="sxs-lookup"><span data-stu-id="b0948-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="b0948-228">Dans l’illustration ci-dessous, `document.querySelector('a')` `document.querySelector('img')` sont des expressions évaluées auparavant.</span><span class="sxs-lookup"><span data-stu-id="b0948-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="La fenêtre contextuelle de saisie semi-automatique affiche les expressions de l’historique." lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="b0948-230">La fenêtre contextuelle de saisie semi-automatique affiche les expressions de l’historique.</span><span class="sxs-lookup"><span data-stu-id="b0948-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <span data-ttu-id="b0948-231">Sélectionner un contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0948-231">Select JavaScript context</span></span>   

<span data-ttu-id="b0948-232">Par défaut, la liste déroulante du **contexte JavaScript** est définie sur **Top**, qui représente le [contexte de navigation][MDNBrowsingContext] du document principal.</span><span class="sxs-lookup"><span data-stu-id="b0948-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Liste déroulante contextuelle JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="b0948-234">Liste déroulante **contextuelle JavaScript**</span><span class="sxs-lookup"><span data-stu-id="b0948-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="b0948-235">Imaginons que vous ayez une publicité sur votre page incorporée dans une `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="b0948-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="b0948-236">Vous souhaitez exécuter JavaScript afin de peaufiner le DOM de la publicité.</span><span class="sxs-lookup"><span data-stu-id="b0948-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="b0948-237">Vous devez tout d’abord sélectionner le contexte de navigation de la publicité dans la liste déroulante **contexte JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="b0948-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Sélectionner un autre contexte JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="b0948-239">Sélectionner un autre contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0948-239">Select a different JavaScript context</span></span>  
:::image-end:::  

## <span data-ttu-id="b0948-240">Effacement de la console</span><span class="sxs-lookup"><span data-stu-id="b0948-240">Clear the Console</span></span>   

<span data-ttu-id="b0948-241">Vous pouvez utiliser les flux de travail suivants pour effacer la console:</span><span class="sxs-lookup"><span data-stu-id="b0948-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="b0948-242">Cliquez sur **effacer la console** \ (effacer la ![ console ][ImageClearConsoleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b0948-242">Click **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="b0948-243">Cliquez avec le bouton droit sur un message, puis sélectionnez **effacer la console**.</span><span class="sxs-lookup"><span data-stu-id="b0948-243">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="b0948-244">Entrez `clear()` dans la console et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b0948-244">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="b0948-245">Appelez `console.clear()` depuis JavaScript pour votre page Web.</span><span class="sxs-lookup"><span data-stu-id="b0948-245">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="b0948-246">Appuyez une fois sur `Control` + `L` le focus de la console.</span><span class="sxs-lookup"><span data-stu-id="b0948-246">Press `Control`+`L` while the Console is in focus.</span></span>  
    
<!--
 

  
-->  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Affichage des messages enregistrés-vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleApi]: ./api.md "Référence sur les API de console | Documents Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "JavaScript en cours d’exécution-vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Commencer à utiliser JavaScript dans la console | Documents Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques | Documents Microsoft"  
[DevToolsConsoleLog]: ./log.md "Commencer à utiliser la journalisation des messages dans la console | Documents Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Référence sur l’API des utilitaires de console | Documents Microsoft"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexte de navigation | MDN"  

> [!NOTE]
> <span data-ttu-id="b0948-256">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0948-256">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b0948-257">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="b0948-257">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="b0948-259">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0948-259">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
