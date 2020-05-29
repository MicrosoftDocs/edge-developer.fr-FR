---
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601783"
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





# <span data-ttu-id="4e109-103">Référence de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-103">Console Reference</span></span>   



<span data-ttu-id="4e109-104">Cette page est une référence des fonctionnalités liées à la console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="4e109-104">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="4e109-105">Il part du principe que vous connaissez déjà l’utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e109-105">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="4e109-106">Si ce n’est pas le cas, voir [prendre en main JavaScript dans la console][DevToolsConsoleJavascript] et [commencer à utiliser les messages de journalisation dans la console][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="4e109-106">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="4e109-107">Si vous recherchez la référence de l’API sur des fonctions telles que voir référence sur l’API de la `console.log()` [console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="4e109-107">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="4e109-108">Pour obtenir une référence sur les fonctions telles que `monitorEvents()` Voir la référence des API d’utilitaires de [console][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="4e109-108">For the reference on functions like `monitorEvents()` see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="4e109-109">Ouvrez la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-109">Open the Console</span></span>   

<span data-ttu-id="4e109-110">Vous pouvez ouvrir la console en tant que [panneau](#open-the-console-panel) ou en tant qu' [onglet dans le tiroir](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="4e109-110">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="4e109-111">Ouvrir l’écran de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-111">Open the Console panel</span></span>   

<span data-ttu-id="4e109-112">Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="4e109-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

> ##### <span data-ttu-id="4e109-113">Figure1</span><span class="sxs-lookup"><span data-stu-id="4e109-113">Figure 1</span></span>  
> <span data-ttu-id="4e109-114">Panneau de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-114">The Console panel</span></span>  
> ![Panneau de la console][ImageConsolePanel]  

<span data-ttu-id="4e109-116">Pour ouvrir le panneau console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande Afficher la **console** contenant le badge du **panneau** .</span><span class="sxs-lookup"><span data-stu-id="4e109-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

> ##### <span data-ttu-id="4e109-117">Figure 2</span><span class="sxs-lookup"><span data-stu-id="4e109-117">Figure 2</span></span>  
> <span data-ttu-id="4e109-118">Commande d’affichage de l’écran de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-118">The command for showing the Console panel</span></span>  
> ![Commande d’affichage de l’écran de la console][ImageCommandShowConsole]  

### <span data-ttu-id="4e109-120">Ouvrir l’onglet de console dans le tiroir</span><span class="sxs-lookup"><span data-stu-id="4e109-120">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="4e109-121">Appuyez `Escape` ou cliquez sur **personnaliser et contrôler devtools** `...` puis sélectionnez **afficher le tiroir**de la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-121">Press `Escape` or click **Customize And Control DevTools** `...` and then select **Show console drawer**.</span></span>  

> ##### <span data-ttu-id="4e109-122">Figure3</span><span class="sxs-lookup"><span data-stu-id="4e109-122">Figure 3</span></span>  
> <span data-ttu-id="4e109-123">Afficher le tiroir de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-123">Show console drawer</span></span>  
> ![Afficher le tiroir de la console][ImageShowConsoleDrawer]  

<span data-ttu-id="4e109-125">Le tiroir apparaît en bas de la fenêtre de DevTools, avec l’onglet **console** ouvert.</span><span class="sxs-lookup"><span data-stu-id="4e109-125">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

> ##### <span data-ttu-id="4e109-126">Figure 4</span><span class="sxs-lookup"><span data-stu-id="4e109-126">Figure 4</span></span>  
> <span data-ttu-id="4e109-127">Onglet Console du tiroir</span><span class="sxs-lookup"><span data-stu-id="4e109-127">The Console tab in the Drawer</span></span>  
> ![Onglet Console du tiroir][ImageDrawerConsole]  

<span data-ttu-id="4e109-129">Pour ouvrir l’onglet de la console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande **afficher la console** dont le badge est associé au **tiroir** .</span><span class="sxs-lookup"><span data-stu-id="4e109-129">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

> ##### <span data-ttu-id="4e109-130">Figure 5</span><span class="sxs-lookup"><span data-stu-id="4e109-130">Figure 5</span></span>  
> <span data-ttu-id="4e109-131">Commande d’affichage de l’onglet de console dans le tiroir</span><span class="sxs-lookup"><span data-stu-id="4e109-131">The command for showing the Console tab in the Drawer</span></span>  
> ![Commande d’affichage de l’onglet de console dans le tiroir][ImageShowDrawerCommand]  

### <span data-ttu-id="4e109-133">Ouvrir les paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-133">Open Console Settings</span></span>   

<span data-ttu-id="4e109-134">Cliquez sur paramètres de la console **paramètres** de la console ![ ][ImageSettingsButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="4e109-134">Click **Console Settings** ![Console Settings][ImageSettingsButtonIcon].</span></span>  

> ##### <span data-ttu-id="4e109-135">Figure 6</span><span class="sxs-lookup"><span data-stu-id="4e109-135">Figure 6</span></span>  
> <span data-ttu-id="4e109-136">Paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-136">Console Settings</span></span>  
> ![Paramètres de la console][ImageConsoleSettings]  

<span data-ttu-id="4e109-138">Les liens ci-dessous décrivent chaque paramètre:</span><span class="sxs-lookup"><span data-stu-id="4e109-138">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="4e109-139">Masquer le réseau</span><span class="sxs-lookup"><span data-stu-id="4e109-139">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="4e109-140">Conserver le journal</span><span class="sxs-lookup"><span data-stu-id="4e109-140">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="4e109-141">Contexte sélectionné uniquement</span><span class="sxs-lookup"><span data-stu-id="4e109-141">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="4e109-142">Groupe similaire</span><span class="sxs-lookup"><span data-stu-id="4e109-142">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="4e109-143">Enregistrer les fichiers XmlHttpRequest</span><span class="sxs-lookup"><span data-stu-id="4e109-143">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="4e109-144">Évaluation hâtif</span><span class="sxs-lookup"><span data-stu-id="4e109-144">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="4e109-145">Saisie semi-automatique dans l’historique</span><span class="sxs-lookup"><span data-stu-id="4e109-145">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  

### <span data-ttu-id="4e109-146">Ouvrir la barre latérale de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-146">Open the Console Sidebar</span></span>   

<span data-ttu-id="4e109-147">Cliquez sur **Afficher** ![ la barre latérale ][ImageShowConsoleSidebarIcon] de la console pour afficher la barre latérale, qui est utile pour le filtrage.</span><span class="sxs-lookup"><span data-stu-id="4e109-147">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon] to show the Sidebar, which is useful for filtering.</span></span>  

> ##### <span data-ttu-id="4e109-148">Figure 7</span><span class="sxs-lookup"><span data-stu-id="4e109-148">Figure 7</span></span>  
> <span data-ttu-id="4e109-149">Barre latérale de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-149">Console Sidebar</span></span>  
> ![Barre latérale de la console][ImageConsoleSidebar]  

## <span data-ttu-id="4e109-151">Afficher des messages</span><span class="sxs-lookup"><span data-stu-id="4e109-151">View messages</span></span>   

<span data-ttu-id="4e109-152">Cette section contient des fonctionnalités qui changent le mode d’affichage des messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-152">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="4e109-153">Pour obtenir une procédure pas à pas, voir [afficher les messages][DevToolsConsoleViewMessages] .</span><span class="sxs-lookup"><span data-stu-id="4e109-153">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="4e109-154">Désactiver le regroupement des messages</span><span class="sxs-lookup"><span data-stu-id="4e109-154">Disable message grouping</span></span>   

<span data-ttu-id="4e109-155">[Ouvrez les paramètres](#open-console-settings) de la console et désactivez l’option groupe, de la **même façon** que le comportement de regroupement des messages par défaut de la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-155">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="4e109-156">Pour obtenir un exemple [, voir journaux de XHR et récupérer des requêtes](#log-xhr-and-fetch-requests) .</span><span class="sxs-lookup"><span data-stu-id="4e109-156">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="4e109-157">Journalisation des requêtes XHR et FETCH</span><span class="sxs-lookup"><span data-stu-id="4e109-157">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="4e109-158">[Ouvrez les paramètres](#open-console-settings) de la console et activez le **Journal** des utilisateurs pour enregistrer toutes les `XMLHttpRequest` `Fetch` demandes de la console en temps réel.</span><span class="sxs-lookup"><span data-stu-id="4e109-158">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

> ##### <span data-ttu-id="4e109-159">Figure8</span><span class="sxs-lookup"><span data-stu-id="4e109-159">Figure 8</span></span>  
> <span data-ttu-id="4e109-160">Journalisation `XMLHttpRequest` et `Fetch` demandes</span><span class="sxs-lookup"><span data-stu-id="4e109-160">Logging `XMLHttpRequest` and `Fetch` requests</span></span>  
> ![Journalisation des requêtes XMLHttpRequest et FETCH][ImageXhrGrouped]  

<span data-ttu-id="4e109-162">Le message principal de la [figure 8](#figure-8) montre le comportement de regroupement par défaut de la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-162">The top message in [Figure 8](#figure-8) shows the default grouping behavior of the Console.</span></span>  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="4e109-163">Faire persister des messages au chargement de la page</span><span class="sxs-lookup"><span data-stu-id="4e109-163">Persist messages across page loads</span></span>   

<span data-ttu-id="4e109-164">Par défaut, la console est effacée dès que vous chargez une nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="4e109-164">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="4e109-165">Pour conserver les messages au cours du chargement de la page, [cliquez sur paramètres](#open-console-settings) de la console, puis activez la case à cocher conserver le **Journal** .</span><span class="sxs-lookup"><span data-stu-id="4e109-165">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="4e109-166">Masquer les messages réseau</span><span class="sxs-lookup"><span data-stu-id="4e109-166">Hide network messages</span></span>   

<span data-ttu-id="4e109-167">Par défaut, le navigateur enregistre les messages réseau sur la **console**.</span><span class="sxs-lookup"><span data-stu-id="4e109-167">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="4e109-168">Par exemple, le message sélectionné dans [figure 9](#figure-9) représente un code d’état de `429` .</span><span class="sxs-lookup"><span data-stu-id="4e109-168">For example, the selected message in [Figure 9](#figure-9) represents a status code of `429`.</span></span>  

> ##### <span data-ttu-id="4e109-169">Figure9</span><span class="sxs-lookup"><span data-stu-id="4e109-169">Figure 9</span></span>  
> <span data-ttu-id="4e109-170">Message 429 dans la console</span><span class="sxs-lookup"><span data-stu-id="4e109-170">A 429 message in the Console</span></span>  
> <span data-ttu-id="4e109-171">! [Un message 429 dans la console] [Image429Message]</span><span class="sxs-lookup"><span data-stu-id="4e109-171">![A 429 message in the Console][Image429Message]</span></span>  

<span data-ttu-id="4e109-172">Pour masquer les messages réseau:</span><span class="sxs-lookup"><span data-stu-id="4e109-172">To hide network messages:</span></span>  

1.  <span data-ttu-id="4e109-173">[Ouvrez paramètres](#open-console-settings)de la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-173">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="4e109-174">Activez la case à cocher **masquer le réseau** .</span><span class="sxs-lookup"><span data-stu-id="4e109-174">Enable the **Hide Network** checkbox.</span></span>  

## <span data-ttu-id="4e109-175">Filtrer les messages</span><span class="sxs-lookup"><span data-stu-id="4e109-175">Filter messages</span></span>   

<span data-ttu-id="4e109-176">Il existe de nombreuses façons de filtrer les messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-176">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="4e109-177">Filtrer les messages du navigateur</span><span class="sxs-lookup"><span data-stu-id="4e109-177">Filter out browser messages</span></span>   

<span data-ttu-id="4e109-178">[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et cliquez sur **messages utilisateur** pour afficher uniquement les messages provenant du JavaScript de la page.</span><span class="sxs-lookup"><span data-stu-id="4e109-178">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

> ##### <span data-ttu-id="4e109-179">Figure10</span><span class="sxs-lookup"><span data-stu-id="4e109-179">Figure 10</span></span>  
> <span data-ttu-id="4e109-180">Affichage des messages des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4e109-180">Viewing user messages</span></span>  
> <span data-ttu-id="4e109-181">! [Affichage des messages des utilisateurs] [ImageUserMessages]</span><span class="sxs-lookup"><span data-stu-id="4e109-181">![Viewing user messages][ImageUserMessages]</span></span>  

### <span data-ttu-id="4e109-182">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="4e109-182">Filter by log level</span></span>   

<span data-ttu-id="4e109-183">DevTools affecte chaque `console.*` méthode un niveau de gravité.</span><span class="sxs-lookup"><span data-stu-id="4e109-183">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="4e109-184">Il y a 4 niveaux: `Verbose` ,, `Info` `Warning` et `Error` .</span><span class="sxs-lookup"><span data-stu-id="4e109-184">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="4e109-185">Par exemple, `console.log()` se trouve dans le `Info` groupe, alors qu’il `console.error()` se trouve dans le `Error` groupe.</span><span class="sxs-lookup"><span data-stu-id="4e109-185">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="4e109-186">La [référence de l’API console][DevToolsConsoleApi] décrit le niveau de gravité de chaque méthode applicable.</span><span class="sxs-lookup"><span data-stu-id="4e109-186">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="4e109-187">Les messages que le navigateur enregistre sur la console ont également un niveau de gravité.</span><span class="sxs-lookup"><span data-stu-id="4e109-187">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="4e109-188">Vous pouvez masquer tous les niveaux de messages qui ne vous intéressent pas.</span><span class="sxs-lookup"><span data-stu-id="4e109-188">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="4e109-189">Par exemple, si vous êtes intéressé uniquement par les `Error` messages, vous pouvez masquer les 3 autres groupes.</span><span class="sxs-lookup"><span data-stu-id="4e109-189">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="4e109-190">Cliquez sur la liste déroulante **niveaux du journal** pour activer ou désactiver ou `Verbose` `Info` `Warning` `Error` messages.</span><span class="sxs-lookup"><span data-stu-id="4e109-190">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

> ##### <span data-ttu-id="4e109-191">Figure11</span><span class="sxs-lookup"><span data-stu-id="4e109-191">Figure 11</span></span>  
> <span data-ttu-id="4e109-192">Liste déroulante **niveaux du journal**</span><span class="sxs-lookup"><span data-stu-id="4e109-192">The **Log Levels** dropdown</span></span>  
> <span data-ttu-id="4e109-193">! [Liste déroulante des niveaux de journaux] [ImageLogLevels]</span><span class="sxs-lookup"><span data-stu-id="4e109-193">![The Log Levels dropdown][ImageLogLevels]</span></span>  

<span data-ttu-id="4e109-194">Vous pouvez également filtrer par niveau de journal en [ouvrant la barre latérale de la console](#open-the-console-sidebar) , puis en cliquant sur **erreurs**, **avertissements**, **informations**ou **Commentaires**.</span><span class="sxs-lookup"><span data-stu-id="4e109-194">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

> ##### <span data-ttu-id="4e109-195">Figure12</span><span class="sxs-lookup"><span data-stu-id="4e109-195">Figure 12</span></span>  
> <span data-ttu-id="4e109-196">Utiliser la barre latérale pour afficher les avertissements</span><span class="sxs-lookup"><span data-stu-id="4e109-196">Using the Sidebar to view warnings</span></span>  
> <span data-ttu-id="4e109-197">! [Utilisation de la barre latérale pour afficher les avertissements] [ImageSidebarWarnings]</span><span class="sxs-lookup"><span data-stu-id="4e109-197">![Using the Sidebar to view warnings][ImageSidebarWarnings]</span></span>  

### <span data-ttu-id="4e109-198">Filtrer les messages par URL</span><span class="sxs-lookup"><span data-stu-id="4e109-198">Filter messages by URL</span></span>   

<span data-ttu-id="4e109-199">Tapez `url:` suivi d’une URL pour afficher uniquement les messages provenant de cette URL.</span><span class="sxs-lookup"><span data-stu-id="4e109-199">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="4e109-200">Après que vous avez tapé `url:` devtools affiche toutes les URL pertinentes.</span><span class="sxs-lookup"><span data-stu-id="4e109-200">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="4e109-201">Les domaines fonctionnent également.</span><span class="sxs-lookup"><span data-stu-id="4e109-201">Domains also work.</span></span>  <span data-ttu-id="4e109-202">Par exemple, si `https://example.com/a.js` `https://example.com/b.js` vous consignez des messages, `url:https://example.com` vous pouvez vous concentrer sur les messages de ces deux scripts.</span><span class="sxs-lookup"><span data-stu-id="4e109-202">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

> ##### <span data-ttu-id="4e109-203">Figure13</span><span class="sxs-lookup"><span data-stu-id="4e109-203">Figure 13</span></span>  
> <span data-ttu-id="4e109-204">Filtre d’URL</span><span class="sxs-lookup"><span data-stu-id="4e109-204">A URL filter</span></span>  
> <span data-ttu-id="4e109-205">! [Filtre d’URL] [ImageUrlFilter]</span><span class="sxs-lookup"><span data-stu-id="4e109-205">![A URL filter][ImageUrlFilter]</span></span>  

<span data-ttu-id="4e109-206">Entrez `-url:` pour masquer les messages de cette URL.</span><span class="sxs-lookup"><span data-stu-id="4e109-206">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="4e109-207">Ce filtre est appelé filtre d’URL négatif.</span><span class="sxs-lookup"><span data-stu-id="4e109-207">This is called a negative URL filter.</span></span>  

> ##### <span data-ttu-id="4e109-208">Figure14</span><span class="sxs-lookup"><span data-stu-id="4e109-208">Figure 14</span></span>  
> <span data-ttu-id="4e109-209">Un filtre d’URL négatif masquant tous les messages correspondant à l’URL;</span><span class="sxs-lookup"><span data-stu-id="4e109-209">A negative URL filter that hides all messages matching the URL</span></span> `https://b.wal.co`  
> <span data-ttu-id="4e109-210">! [Filtre d’URL négatif masquant tous les messages correspondant à l’URL https://b.wal.co ] [ImageNegativeUrlFilter1]</span><span class="sxs-lookup"><span data-stu-id="4e109-210">![A negative URL filter that hides all messages matching the URL https://b.wal.co][ImageNegativeUrlFilter1]</span></span>  

<span data-ttu-id="4e109-211">Vous pouvez également afficher les messages d’une URL unique en [ouvrant la barre latérale](#open-the-console-sidebar)de la console, en développant la section messages de l' **utilisateur** , puis en cliquant sur l’URL du script contenant les messages sur lesquels vous souhaitez vous concentrer.</span><span class="sxs-lookup"><span data-stu-id="4e109-211">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

> ##### <span data-ttu-id="4e109-212">Figure15</span><span class="sxs-lookup"><span data-stu-id="4e109-212">Figure 15</span></span>  
> <span data-ttu-id="4e109-213">Affichage des messages de</span><span class="sxs-lookup"><span data-stu-id="4e109-213">Viewing the messages that came from</span></span> `wp-ad.min.js`  
> <span data-ttu-id="4e109-214">! [Affichage des messages issus de WP-ad. min. js] [ImageNegativeUrlFilter2]</span><span class="sxs-lookup"><span data-stu-id="4e109-214">![Viewing the messages that came from wp-ad.min.js][ImageNegativeUrlFilter2]</span></span>  

### <span data-ttu-id="4e109-215">Filtrer les messages de différents contextes</span><span class="sxs-lookup"><span data-stu-id="4e109-215">Filter out messages from different contexts</span></span>   

<span data-ttu-id="4e109-216">Imaginons que vous ayez une annonce (publicité) sur votre page.</span><span class="sxs-lookup"><span data-stu-id="4e109-216">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="4e109-217">La publicité est incorporée dans un `<iframe>` et génère un grand nombre de messages dans votre console.</span><span class="sxs-lookup"><span data-stu-id="4e109-217">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="4e109-218">Dans la mesure où la publicité s’exécute dans un autre [contexte JavaScript](#select-javascript-context), une façon de masquer les messages consiste à [ouvrir les paramètres](#open-console-settings) de la console et à activer la case à cocher **contexte sélectionnée uniquement** .</span><span class="sxs-lookup"><span data-stu-id="4e109-218">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="4e109-219">Filtrer les messages qui ne correspondent pas à un modèle d’expression régulière</span><span class="sxs-lookup"><span data-stu-id="4e109-219">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="4e109-220">Tapez une expression régulière telle que `/[gm][ta][mi]/` dans la zone de texte de **filtre** pour filtrer les messages ne correspondant pas à ce modèle.</span><span class="sxs-lookup"><span data-stu-id="4e109-220">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="4e109-221">DevTools vérifie si le modèle se trouve dans le texte du message ou dans le script qui a entraîné la journalisation du message.</span><span class="sxs-lookup"><span data-stu-id="4e109-221">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

> ##### <span data-ttu-id="4e109-222">Figure16</span><span class="sxs-lookup"><span data-stu-id="4e109-222">Figure 16</span></span>  
> <span data-ttu-id="4e109-223">Filtrage des messages ne correspondant pas</span><span class="sxs-lookup"><span data-stu-id="4e109-223">Filtering out any messages that do not match</span></span> `/[gm][ta][mi]/`  
> <span data-ttu-id="4e109-224">! [En filtrant les messages ne correspondant pas à l’expression Regex] [ImageRegExFilter]</span><span class="sxs-lookup"><span data-stu-id="4e109-224">![Filtering out any messages that do not match regex expression][ImageRegExFilter]</span></span>  

## <span data-ttu-id="4e109-225">Exécuter JavaScript</span><span class="sxs-lookup"><span data-stu-id="4e109-225">Run JavaScript</span></span>   

<span data-ttu-id="4e109-226">Cette section contient des fonctionnalités relatives à l’exécution de JavaScript dans la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-226">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="4e109-227">Pour obtenir une procédure pas à pas, voir [exécuter JavaScript][DevToolsConsoleOverviewJavascript] .</span><span class="sxs-lookup"><span data-stu-id="4e109-227">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="4e109-228">Réexécuter des expressions à partir de l’historique</span><span class="sxs-lookup"><span data-stu-id="4e109-228">Re-run expressions from history</span></span>   

<span data-ttu-id="4e109-229">Appuyez sur la `Up Arrow` touche pour parcourir l’historique des expressions JavaScript que vous avez exécutées auparavant dans la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-229">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="4e109-230">Appuyez sur `Enter` pour réexécuter cette expression.</span><span class="sxs-lookup"><span data-stu-id="4e109-230">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="4e109-231">Regardez la valeur d’une expression en temps réel avec des expressions dynamiques</span><span class="sxs-lookup"><span data-stu-id="4e109-231">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="4e109-232">Si vous vous intentez de taper la même expression JavaScript dans la console à plusieurs reprises, il est possible que vous puissiez constater qu’il est plus facile de créer une **expression dynamique**.</span><span class="sxs-lookup"><span data-stu-id="4e109-232">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="4e109-233">Dans les **expressions dynamiques** , vous tapez une expression une seule fois, puis épinglez celle-ci en haut de votre console.</span><span class="sxs-lookup"><span data-stu-id="4e109-233">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="4e109-234">La valeur de l’expression est mise à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="4e109-234">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="4e109-235">Voir [valeurs d’expression JavaScript en temps réel avec des expressions dynamiques][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="4e109-235">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="4e109-236">Désactiver l’évaluation hâtif</span><span class="sxs-lookup"><span data-stu-id="4e109-236">Disable Eager Evaluation</span></span>   

<span data-ttu-id="4e109-237">Lorsque vous tapez des expressions JavaScript dans la console, l' **évaluation hâtif** affiche un aperçu de la valeur de retour pour cette expression.</span><span class="sxs-lookup"><span data-stu-id="4e109-237">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="4e109-238">[Ouvrez paramètres](#open-console-settings) de la console et désactivez la case à cocher **évaluation hâtif** pour désactiver les aperçus des valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="4e109-238">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="4e109-239">Désactiver la saisie semi-automatique dans l’historique</span><span class="sxs-lookup"><span data-stu-id="4e109-239">Disable autocomplete from history</span></span>   

<span data-ttu-id="4e109-240">Lors de la saisie d’une expression, la fenêtre contextuelle de saisie semi-automatique de la console affiche les expressions que vous avez exécutées auparavant.</span><span class="sxs-lookup"><span data-stu-id="4e109-240">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="4e109-241">Ces expressions sont précédées du `>` caractère.</span><span class="sxs-lookup"><span data-stu-id="4e109-241">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="4e109-242">[Ouvrez paramètres](#open-console-settings) de la console et désactivez l’option **saisie semi-automatique de l’historique** pour ne plus afficher les expressions de votre historique.</span><span class="sxs-lookup"><span data-stu-id="4e109-242">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="4e109-243">Dans la [figure 17](#figure-17), `document.querySelector('a')` et `document.querySelector('img')` sont des expressions évaluées auparavant.</span><span class="sxs-lookup"><span data-stu-id="4e109-243">In [Figure 17](#figure-17), `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

> ##### <span data-ttu-id="4e109-244">Figure17</span><span class="sxs-lookup"><span data-stu-id="4e109-244">Figure 17</span></span>  
> <span data-ttu-id="4e109-245">Fenêtre contextuelle de saisie semi-automatique montrant des expressions de l’historique</span><span class="sxs-lookup"><span data-stu-id="4e109-245">The autocomplete popup showing expressions from history</span></span>  
> <span data-ttu-id="4e109-246">! [Fenêtre de saisie semi-automatique montrant des expressions de l’historique] [ImageHistoryAutocomplete]</span><span class="sxs-lookup"><span data-stu-id="4e109-246">![The autocomplete popup showing expressions from history][ImageHistoryAutocomplete]</span></span>  

### <span data-ttu-id="4e109-247">Sélectionner un contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="4e109-247">Select JavaScript context</span></span>   

<span data-ttu-id="4e109-248">Par défaut, la liste déroulante du **contexte JavaScript** est définie sur **Top**, qui représente le [contexte de navigation][MDNBrowsingContext] du document principal.</span><span class="sxs-lookup"><span data-stu-id="4e109-248">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

> ##### <span data-ttu-id="4e109-249">Figure 18</span><span class="sxs-lookup"><span data-stu-id="4e109-249">Figure 18</span></span>  
> <span data-ttu-id="4e109-250">Liste déroulante **contextuelle JavaScript**</span><span class="sxs-lookup"><span data-stu-id="4e109-250">The **JavaScript Context** dropdown</span></span>  
> <span data-ttu-id="4e109-251">! [Zone de liste déroulante de contexte JavaScript] [ImageJavascriptContext]</span><span class="sxs-lookup"><span data-stu-id="4e109-251">![The JavaScript Context dropdown][ImageJavascriptContext]</span></span>  

<span data-ttu-id="4e109-252">Imaginons que vous ayez une publicité sur votre page incorporée dans une `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="4e109-252">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="4e109-253">Vous souhaitez exécuter JavaScript afin de peaufiner le DOM de la publicité.</span><span class="sxs-lookup"><span data-stu-id="4e109-253">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="4e109-254">Vous devez tout d’abord sélectionner le contexte de navigation de la publicité dans la liste déroulante **contexte JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="4e109-254">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

> ##### <span data-ttu-id="4e109-255">Figure 19</span><span class="sxs-lookup"><span data-stu-id="4e109-255">Figure 19</span></span>  
> <span data-ttu-id="4e109-256">Sélection d’un autre contexte JavaScript</span><span class="sxs-lookup"><span data-stu-id="4e109-256">Selecting a different JavaScript context</span></span>  
> <span data-ttu-id="4e109-257">! [Sélection d’un autre contexte JavaScript] [ImageSelectContext]</span><span class="sxs-lookup"><span data-stu-id="4e109-257">![Selecting a different JavaScript context][ImageSelectContext]</span></span>  

## <span data-ttu-id="4e109-258">Effacement de la console</span><span class="sxs-lookup"><span data-stu-id="4e109-258">Clear the Console</span></span>   

<span data-ttu-id="4e109-259">Vous pouvez utiliser les flux de travail suivants pour effacer la console:</span><span class="sxs-lookup"><span data-stu-id="4e109-259">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="4e109-260">Cliquez sur **Effacer** la console effacer la console ![ ][ImageClearConsoleIcon] .</span><span class="sxs-lookup"><span data-stu-id="4e109-260">Click **Clear Console** ![Clear Console][ImageClearConsoleIcon].</span></span>  
*   <span data-ttu-id="4e109-261">Cliquez avec le bouton droit sur un message, puis sélectionnez **effacer la console**.</span><span class="sxs-lookup"><span data-stu-id="4e109-261">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="4e109-262">Entrez `clear()` dans la console et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4e109-262">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="4e109-263">Appelez `console.clear()` depuis JavaScript pour votre page Web.</span><span class="sxs-lookup"><span data-stu-id="4e109-263">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="4e109-264">Appuyez une fois sur `Control` + `L` le focus de la console.</span><span class="sxs-lookup"><span data-stu-id="4e109-264">Press `Control`+`L` while the Console is in focus.</span></span>  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Figure 1: panneau de la console"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figure 2: commande d’affichage du panneau de la console"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Figure 3: afficher le tiroir de la console"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Figure 4: onglet de la console dans le tiroir"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figure 5: commande d’affichage de l’onglet de console dans le tiroir"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Figure 6: paramètres de la console"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Figure 7: barre latérale de la console"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Figure 8: enregistrement des demandes de fichiers XMLHttpRequest et FETCH"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Show-Network.msft.png "figure 9: message 429 dans la console"  
[ImageUserMessages]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-Drawer-user-messages.msft.png "figure 10: affichage des messages des utilisateurs"  
[ImageLogLevels]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-Level-default-Levels.msft.png "figure 11: liste déroulante des niveaux de journaux"  
[ImageSidebarWarnings]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-Warnings.msft.png "figure 12: utilisation de la barre latérale pour afficher les avertissements"  
[ImageUrlFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text.msft.png "figure 13: filtre d’URL"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Negative-Filter-Text.msft.png "figure 14: filtre d’URL négatif masquant tous les messages correspondant à l’URL https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text-specified.msft.png "figure 15: affichage des messages livrés avec WP-ad. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Regex.msft.png "figure 16: filtrage des messages ne correspondant pas à l’expression Regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text-AutoFilter-History.msft.png "figure 17: fenêtre contextuelle de saisie semi-automatique avec expressions de l’historique"  
[ImageJavascriptContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-DOM-Level-Top.msft.png "figure 18: liste déroulante de contexte JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-DOM-Level-multiple.msft.png "figure 19: sélection d’un autre contexte JavaScript"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Affichage des messages enregistrés-vue d’ensemble de la console"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence sur les API de la console"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "JavaScript en cours d’exécution-vue d’ensemble de la console"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Commencer à utiliser JavaScript sur la console"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Commencer à utiliser la journalisation des messages dans la console"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "XXXXXX xxxxxxx xxx xxxxxxxxx"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexte de navigation | MDN"  

> [!NOTE]
> <span data-ttu-id="4e109-293">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e109-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4e109-294">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="4e109-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="4e109-296">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e109-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
