---
description: Fonctionnalités ajoutées au Microsoft Edge DevTools de la mise à jour de Windows 10 pour les créateurs du automne (EdgeHTML 16)
title: DevTools dans EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, edgehtml 16
ms.custom: seodec18
ms.openlocfilehash: 78ede81e022cc8f0f623ecd33fd2303314ec9cb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565505"
---
# <span data-ttu-id="f723e-104">DevTools de la mise à jour de reports de Windows 10 (EdgeHTML 16)</span><span class="sxs-lookup"><span data-stu-id="f723e-104">DevTools in the Windows 10 Fall Creators Update (EdgeHTML 16)</span></span>

<span data-ttu-id="f723e-105">Grâce à cette version, nous avons commencé un effort de refactorisation DevTools majeur pour une fiabilité et des performances améliorées, ainsi que les nouvelles fonctionnalités que vous pouvez commencer à utiliser dès maintenant.</span><span class="sxs-lookup"><span data-stu-id="f723e-105">With this release we started a major DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today!</span></span> 

<span data-ttu-id="f723e-106">Voici les fonctionnalités de Microsoft Edge DevTools fournies avec la [mise à jour de Windows 10](/windows/uwp/whats-new/windows-10-build-16299) pour les créateurs du automne ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span><span class="sxs-lookup"><span data-stu-id="f723e-106">Here are the Microsoft Edge DevTools features that shipped with the [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span></span>

## <span data-ttu-id="f723e-107">Écouteurs d’événements ancêtres</span><span class="sxs-lookup"><span data-stu-id="f723e-107">Ancestor event listeners</span></span> 

<span data-ttu-id="f723e-108">Le volet **Events** ajoute désormais l’option d’affichage des écouteurs d’événements inscrits sur n’importe quel ancêtre de l’élément actuellement sélectionné (dans le panneau **éléments** ), en plus de celles de l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="f723e-108">The **Events** pane now adds the option to view event listeners registered on any ancestor of the currently selected element (in the **Elements** panel), in addition to those on the element itself.</span></span> <span data-ttu-id="f723e-109">Par ailleurs, vous pouvez regrouper l’affichage d’un écouteur d’événements par *événement* ou *élément*.</span><span class="sxs-lookup"><span data-stu-id="f723e-109">Additionally, you can now group the event listener display by either *Event* or *Element*.</span></span> 

![Volet de vérification de l’écouteur d’événements](../media/elements_ancestor_events.png)

## <span data-ttu-id="f723e-111">Points d’arrêt de mutation DOM</span><span class="sxs-lookup"><span data-stu-id="f723e-111">DOM mutation breakpoints</span></span>

<span data-ttu-id="f723e-112">Vous pouvez désormais définir des points d’arrêt de mutation DOM pour qu’ils s’arrêtent dans le débogueur dès qu’un nœud d’élément sélectionné change.</span><span class="sxs-lookup"><span data-stu-id="f723e-112">You can now set DOM mutation breakpoints to break into the Debugger whenever a selected element node changes.</span></span> <span data-ttu-id="f723e-113">Dans le panneau **éléments** , cliquez sur n’importe quel élément de l’arborescence DOM et sélectionnez une ou plusieurs des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="f723e-113">From the **Elements** panel, rt-click on any element in the DOM tree view and select one or more of the following:</span></span>

 - <span data-ttu-id="f723e-114">Arrêt du nœud supprimé</span><span class="sxs-lookup"><span data-stu-id="f723e-114">Break on Node removed</span></span>
 - <span data-ttu-id="f723e-115">Saut de la sous-arborescence modifié</span><span class="sxs-lookup"><span data-stu-id="f723e-115">Break on Subtree modified</span></span>
 - <span data-ttu-id="f723e-116">Arrêt du saut sur l’attribut modifié</span><span class="sxs-lookup"><span data-stu-id="f723e-116">Break on Attribute modified</span></span>

<span data-ttu-id="f723e-117">Vous pouvez gérer vos points d’arrêt de mutation à partir du volet **points d’arrêt DOM** dans les panneaux **éléments** ou **débogueur** .</span><span class="sxs-lookup"><span data-stu-id="f723e-117">You can manage your mutation breakpoints from the **DOM breakpoints** pane in the **Elements** or **Debugger** panels.</span></span>

![Volet points d’arrêt DOM](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="f723e-119">CSS at-Rule support</span><span class="sxs-lookup"><span data-stu-id="f723e-119">CSS at-rule support</span></span>

<span data-ttu-id="f723e-120">Les règles CSS «at» (@) sont désormais représentées par d’autres déclarations de règles CSS dans le volet **styles** , y compris les `@keyframes` règles d’animation (actuellement limitées aux lecture seule), les `@supports` requêtes de fonctionnalités et les `@media` requêtes.</span><span class="sxs-lookup"><span data-stu-id="f723e-120">CSS "at" (@) rules are now represented among other CSS rule declarations on the **Styles** pane, including animation `@keyframes` rules (currently limited to read-only), `@supports` feature queries, and `@media` queries.</span></span>

![CSS at-inspection-règles du volet style de DevTools](../media/elements_at_rules.png)

## <span data-ttu-id="f723e-122">Volet polices CSS</span><span class="sxs-lookup"><span data-stu-id="f723e-122">CSS fonts pane</span></span>

<span data-ttu-id="f723e-123">`@font-face`Les règles CSS possèdent désormais leur propre volet **polices** dédiées qui indique l’emplacement de chargement de la police (*locale* ou *réseau*) et le nombre de caractères qui l’utilisent.</span><span class="sxs-lookup"><span data-stu-id="f723e-123">CSS `@font-face` rules now have their own dedicated **Fonts** pane that displays where the font is loaded from (*Local* or *Network*) and how many characters are using it.</span></span> <span data-ttu-id="f723e-124">Si une police est chargée à partir du réseau, DevTools affiche la règle qui s’en est importée avec son alias et son type de police.</span><span class="sxs-lookup"><span data-stu-id="f723e-124">If a font is loaded from the network,  DevTools will display the rule that imported it along with its alias and font type.</span></span>

![Informations sur la police CSS](../media/elements_fonts.png)

## <span data-ttu-id="f723e-126">Prise en charge de Pseudo-éléments CSS</span><span class="sxs-lookup"><span data-stu-id="f723e-126">CSS pseudo-element support</span></span>

<span data-ttu-id="f723e-127">Le volet **styles** permet de regrouper les Pseudo-éléments dans leurs propres titres et de ne pas afficher leur contenu comme barré.</span><span class="sxs-lookup"><span data-stu-id="f723e-127">The **Styles** pane now groups pseudo-elements under their own headings and no longer displays their content as crossed out.</span></span>

**<span data-ttu-id="f723e-128">Avant:</span><span class="sxs-lookup"><span data-stu-id="f723e-128">Before:</span></span>**
<br>
![Le contenu généré a été rayé.](../media/gc_before.png)

**<span data-ttu-id="f723e-130">Après:</span><span class="sxs-lookup"><span data-stu-id="f723e-130">After:</span></span>**
<br>
![Le contenu généré n’apparaît plus avec un barré](../media/gc_after.png)

## <span data-ttu-id="f723e-132">Améliorations de la console</span><span class="sxs-lookup"><span data-stu-id="f723e-132">Console improvements</span></span>

<span data-ttu-id="f723e-133">Le panneau de la **console** dispose d’une fonctionnalité d’expérience utilisateur améliorée pour une plus grande convivialité et une expérience IntelliSense plus riche et plus rapide.</span><span class="sxs-lookup"><span data-stu-id="f723e-133">The **Console** panel got a UX overhaul for improved usability and a faster, richer Intellisense experience.</span></span>

<span data-ttu-id="f723e-134">**Avant:** 
![ Console précédente</span><span class="sxs-lookup"><span data-stu-id="f723e-134">**Before:**
![Previous console</span></span>](../media/console_old.png)

<span data-ttu-id="f723e-135">**Après:** 
![ Nouvelle console</span><span class="sxs-lookup"><span data-stu-id="f723e-135">**After:**
![New console</span></span>](../media/console_new.png)

<span data-ttu-id="f723e-136">Nous avons également ajouté les améliorations suivantes:</span><span class="sxs-lookup"><span data-stu-id="f723e-136">We also added these improvements:</span></span>

 -  <span data-ttu-id="f723e-137">Utilisez `Shift + Enter` cette option pour ajouter une ligne supplémentaire à une commande avant de l’exécuter `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f723e-137">Use `Shift + Enter` to add an additional line to a command before executing it with `Enter`.</span></span> <span data-ttu-id="f723e-138">(Auparavant, il y a eu une *option de basculement vers le bouton bascule du mode multiligne/ligne unique* .)</span><span class="sxs-lookup"><span data-stu-id="f723e-138">(Formerly there was a *Switch to multiline/single-line mode* toggle button.)</span></span>

 - <span data-ttu-id="f723e-139">Les nouvelles API suivantes sont prises en charge:</span><span class="sxs-lookup"><span data-stu-id="f723e-139">The following new APIs are supported:</span></span>
    - <span data-ttu-id="f723e-140">méthode [**console. table (***objet***)**](../console/console-api.md#organizing-log-output)</span><span class="sxs-lookup"><span data-stu-id="f723e-140">[**console.table(***object***)**](../console/console-api.md#organizing-log-output) method</span></span>
    - <span data-ttu-id="f723e-141">commande [**getEventListeners (***objet***)**](../console/command-line.md#event-listeners)</span><span class="sxs-lookup"><span data-stu-id="f723e-141">[**getEventListeners(***object***)**](../console/command-line.md#event-listeners) command</span></span>
    - <span data-ttu-id="f723e-142">commande [**Keys (***objet***)**](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="f723e-142">[**keys(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="f723e-143">commande [**valeurs (***objet***)**](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="f723e-143">[**values(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="f723e-144">sélecteur d' [**$x (***expression XPath***)**](../console/command-line.md#dom-selectors)</span><span class="sxs-lookup"><span data-stu-id="f723e-144">[**$x(***xpath expression***)**](../console/command-line.md#dom-selectors) selector</span></span>

 - <span data-ttu-id="f723e-145">Le paramètre de mise en forme [**% c ()**](../console/console-api.md#logging-custom-messages) est désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="f723e-145">The [**%c()**](../console/console-api.md#logging-custom-messages) formatting parameter is now supported</span></span>

## <span data-ttu-id="f723e-146">Amélioration du débogage</span><span class="sxs-lookup"><span data-stu-id="f723e-146">Debugging improvements</span></span>

<span data-ttu-id="f723e-147">Outre une suite de nouvelles fonctionnalités pour le débogage des [travailleurs et du cache de votre service PWA](#progressive-web-app-debugging), le débogueur a ajouté les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="f723e-147">In addition to a suite of new features for debugging your [PWA service workers and cache](#progressive-web-app-debugging), the Debugger added these features:</span></span>

### <span data-ttu-id="f723e-148">Débogage consolidé des ressources partagées</span><span class="sxs-lookup"><span data-stu-id="f723e-148">Consolidated debugging for shared resources</span></span>

<span data-ttu-id="f723e-149">Même si une ressource, telle qu’un fichier chargé à partir du réseau de distribution de contenu (CDN), est référencée plusieurs fois dans votre code, DevTools fournit désormais une instance de débogage unique pour ce fichier, dans laquelle vous pouvez définir des points d’arrêt communs qui seront pris en compte, quel que soit l’endroit où ce fichier est référencé.</span><span class="sxs-lookup"><span data-stu-id="f723e-149">Even when a resource, such as a file loaded from CDN, is referenced multiple times throughout your code,  DevTools will now provide a single debugging instance for that file where you can then set common breakpoints which will be hit regardless of where that file is referenced.</span></span> <span data-ttu-id="f723e-150">(Auparavant, chaque référence de script était considérée comme une ressource unique mappée à un ensemble distinct de points d’arrêt.)</span><span class="sxs-lookup"><span data-stu-id="f723e-150">(Previously each script reference was considered a unique resource would map to a separate set of breakpoints.)</span></span>

### <span data-ttu-id="f723e-151">Modification dynamique JavaScript avec la *modification lors de l’inactivité*</span><span class="sxs-lookup"><span data-stu-id="f723e-151">Live edit JavaScript with *Edit-on-idle*</span></span>

<span data-ttu-id="f723e-152">Vous pouvez maintenant modifier votre code JavaScript live lors d’une session de débogage.</span><span class="sxs-lookup"><span data-stu-id="f723e-152">You can now edit your JavaScript live during a debugging session.</span></span> <span data-ttu-id="f723e-153">Cette fonctionnalité a fait l’expérience d’une expérimentation disponible (derrière un drapeau) dans l' [ancienne](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) version (*Windows 10 Creators Update*) et il s’agit maintenant d’une fonctionnalité permanente.</span><span class="sxs-lookup"><span data-stu-id="f723e-153">This feature was experimentally available (behind a flag) in the [previous](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) release and now its a permanent feature.</span></span> <span data-ttu-id="f723e-154">Il suffit de sélectionner n’importe quel fichier de script dans le volet **débogueur** , de modifier, puis de cliquer sur **Enregistrer** (ou `Ctrl+S` ) pour tester vos modifications lors de la prochaine exécution de la section de code.</span><span class="sxs-lookup"><span data-stu-id="f723e-154">Simply select any script file from the **Debugger** panel, edit, then click **Save** (or `Ctrl+S`) to test your changes next time that section of code runs.</span></span> 

![Le débogueur vous permet d’apporter des modifications aux scripts et de les différencier](../media/debugger_edit_buttons.png) 

<span data-ttu-id="f723e-156">Cliquez sur le bouton **comparer le document à l’original** pour afficher un aperçu de ce que vous avez modifié.</span><span class="sxs-lookup"><span data-stu-id="f723e-156">Click the **Compare document to original** button to view the diff of what you changed.</span></span>

![Vue diff du code modifié dans le débogueur](../media/debugger_edit_code.png) 

<span data-ttu-id="f723e-158">Tenez compte des contraintes suivantes:</span><span class="sxs-lookup"><span data-stu-id="f723e-158">Please be aware of the following constraints:</span></span>

- <span data-ttu-id="f723e-159">La modification des scripts ne fonctionne que dans les fichiers externes *. js* (et non incorporés `<script>` au *format. html*)</span><span class="sxs-lookup"><span data-stu-id="f723e-159">Script editing only works in external *.js* files (and not embedded `<script>` within *.html*)</span></span>
- <span data-ttu-id="f723e-160">Les modifications sont enregistrées en mémoire et vidées lors du rechargement du document, vous ne pourrez donc pas exécuter de modifications à l’intérieur d’un `DOMContentLoaded` Gestionnaire, par exemple</span><span class="sxs-lookup"><span data-stu-id="f723e-160">Edits are saved in memory and flushed when the document is reloaded, thus you won’t be able to run edits inside a `DOMContentLoaded` handler, for example</span></span>
- <span data-ttu-id="f723e-161">Il n’existe actuellement aucune méthode (par exemple, option **Enregistrer sous** ) pour enregistrer vos modifications sur un disque à partir de devtools</span><span class="sxs-lookup"><span data-stu-id="f723e-161">Currently there’s no way (such as a **Save As** option) to save your edits to disk from  DevTools</span></span>

## <span data-ttu-id="f723e-162">Associés</span><span class="sxs-lookup"><span data-stu-id="f723e-162">Shortcuts</span></span>

<span data-ttu-id="f723e-163">Vous pouvez à présent lancer DevTools vers le dernier panneau affiché ( `Ctrl+Shift+I` ) ou directement sur la console ( `Ctrl+Shift+J` ) comme sur d’autres navigateurs importants.</span><span class="sxs-lookup"><span data-stu-id="f723e-163">You can now launch DevTools to the last viewed panel (`Ctrl+Shift+I`) or directly to the Console (`Ctrl+Shift+J`) just like you would on other major browsers.</span></span>

## <span data-ttu-id="f723e-164">Débogage de l’application Web progressive</span><span class="sxs-lookup"><span data-stu-id="f723e-164">Progressive Web App debugging</span></span>

<span data-ttu-id="f723e-165">Testez la prise en charge expérimentale des applications Web progressives (PWAs) dans Microsoft Edge et DevTools en sélectionnant l’option **activer les travailleurs de service** dans `about:flags` (et en redémarrant Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="f723e-165">Test out the experimental support for Progressive Web Apps (PWAs) in Microsoft Edge and  DevTools by selecting the **Enable service workers** option from `about:flags` (and restarting Microsoft Edge).</span></span> <span data-ttu-id="f723e-166">Si un site utilise des **travailleurs de service** et/ou l’API de **cache** , les entrées du panneau du **débogueur** seront insérées dans chaque origine, de la même façon que dans le stockage Web et l’inspection des cookies.</span><span class="sxs-lookup"><span data-stu-id="f723e-166">If a site makes use of **Service Workers** and/or the **Cache** API,  will populate entries in the **Debugger** panel for each origin, similar to how web storage and cookie inspection work.</span></span>

<span data-ttu-id="f723e-167">Le fait de cliquer sur une entrée de service particulière entraîne l’ouverture de la **vue d’ensemble**du travailleur de service, dans laquelle vous pouvez gérer l’enregistrement du travailleur de service pour l’étendue donnée et forcer une notification de transmission de test.</span><span class="sxs-lookup"><span data-stu-id="f723e-167">Clicking on a specific service worker entry will open up the **Service Worker Overview**, where you can manage the service worker registration for the given scope and force a test push notification.</span></span> <span data-ttu-id="f723e-168">Vous pouvez également **arrêter** / de**lancer** des travailleurs de service individuels et les **inspecter** à partir d’une fenêtre de débogage séparée:</span><span class="sxs-lookup"><span data-stu-id="f723e-168">You can also **Stop**/**Start** individual service workers and **Inspect** them from a separate debugger window:</span></span>

![Volet vue d’ensemble des travailleurs de services](../media/debugger_sw_overview.png)

<span data-ttu-id="f723e-170">Veuillez noter ce qui suit le débogage du travailleur de services:</span><span class="sxs-lookup"><span data-stu-id="f723e-170">Please note the following about service worker debugging:</span></span>

 - <span data-ttu-id="f723e-171">Le débogage d’un ouvrier de service lancera une nouvelle instance du DevTools séparée des outils de la page, car les travailleurs de services peuvent être partagés entre plusieurs onglets.</span><span class="sxs-lookup"><span data-stu-id="f723e-171">Debugging a service worker will launch a new instance of the DevTools separate from the page's tools because service workers can be shared across multiple tabs.</span></span> 
 - <span data-ttu-id="f723e-172">Les [éléments](../elements.md) et les panneaux d' [émulation](../emulation.md) ne sont pas pris en tant que débogueur de service, car ils s’exécutent en arrière-plan et ne contrôlent pas directement le serveur principal de votre application.</span><span class="sxs-lookup"><span data-stu-id="f723e-172">The [Elements](../elements.md) and [Emulation](../emulation.md) panels are absent from the service worker debugger, given that service workers run in the background and do not directly control the front-end of your app.</span></span>
 - <span data-ttu-id="f723e-173">Pour le moment, le trafic réseau d’un ouvrier de service est uniquement signalé à partir de l’instance de débogage de DevTools pour ce travailleur et non à partir de l’instance centrale de la page elle-même.</span><span class="sxs-lookup"><span data-stu-id="f723e-173">Currently network traffic for a service worker is only reported from the DevTools debugging instance for that worker, and not from the central instance for the page itself.</span></span>

<span data-ttu-id="f723e-174">Le fait de cliquer sur une entrée de cache spécifique ouvre le gestionnaire de **cache** pour vous permettre d’inspecter et éventuellement de supprimer les entrées de cache (paires de*requête* et de clé de *réponse* /valeur).</span><span class="sxs-lookup"><span data-stu-id="f723e-174">Clicking on a specific cache entry will open up the **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs).</span></span>