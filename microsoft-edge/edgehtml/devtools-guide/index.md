---
description: Découvrir les outils de développement Microsoft Edge (EdgeHTML)
title: Outils de développement Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 89fdbcdf10d10c57836067ca7d02afa3fd48cbc9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233033"
---
# <span data-ttu-id="d7045-104">Outils de développement Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="d7045-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](../includes/new-devtools-version-note.md)]  

<span data-ttu-id="d7045-105">DevTools de Microsoft Edge \ (EdgeHTML \) sont conçus avec [TypeScript][|::ref1::|Index], avec [Open source][GithubMicrosoftChakracore], optimisés pour les flux de travail frontaux modernes et désormais disponible sous la forme d'[application Windows10 autonome][MicrosoftStoreEdgeDevtoolsPreview] dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d7045-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="d7045-106">Pour plus d’informations sur les fonctionnalités les plus récentes, consultez [DevTools dans la dernière mise à jour de Windows10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="d7045-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="d7045-107">Outils principaux</span><span class="sxs-lookup"><span data-stu-id="d7045-107">Core tools</span></span>  

:::image type="complex" source="./media/devtools.png" alt-text="DevTools Microsoft Edge (EdgeHTML)":::
   <span data-ttu-id="d7045-109">DevTools Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="d7045-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="d7045-110">La DevTools Microsoft Edge (EdgeHTML) inclut:</span><span class="sxs-lookup"><span data-stu-id="d7045-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="d7045-111">Un panneau [Éléments][DevtoolsGuideEdgehtml|::ref2::|] permettant de modifier les codes HTML et CSS, d’inspecter les propriétés d’accessibilité, d’afficher les écouteurs d’événement et de créer des points d’arrêt de mutation DOM</span><span class="sxs-lookup"><span data-stu-id="d7045-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="d7045-112">Une [Console][DevtoolsGuideEdgehtml|::ref3::|] pour afficher et filtrer les messages journaux, examiner les objets JavaScript et les nœuds DOM et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d7045-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="d7045-113">Un [Débogueur][DevtoolsGuideEdgehtml|::ref4::|] pour parcourir le code, mettre en place des surveillances et des points d'arrêt, modifier en direct votre code et inspecter vos caches de stockage web et de cookies</span><span class="sxs-lookup"><span data-stu-id="d7045-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="d7045-114">Un panneau [Réseau][DevtoolsGuideEdgehtml|::ref5::|] permettant de contrôler et d’inspecter les demandes et les réponses à partir du réseau et du cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="d7045-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="d7045-115">Un panneau [Performance][DevtoolsGuideEdgehtml|::ref6::|] pour profiler l’heure et les ressources système requises par votre site</span><span class="sxs-lookup"><span data-stu-id="d7045-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="d7045-116">Un panneau [Mémoire][DevtoolsGuideEdgehtml|::ref7::|] pour mesurer l’utilisation des ressources de mémoire et comparer les instantanés de tas aux différents états du runtime de code</span><span class="sxs-lookup"><span data-stu-id="d7045-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="d7045-117">Un panneau [Stockage][DevtoolsGuideEdgehtml|::ref8::|] permettant d’inspecter et de gérer vos données de stockage web, de IndexedDB, de cookies et de cache</span><span class="sxs-lookup"><span data-stu-id="d7045-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="d7045-118">Un panneau [Travailleurs de services][DevtoolsGuideEdgehtmlServiceworkers]pour gérer et déboguer vos travailleurs de services</span><span class="sxs-lookup"><span data-stu-id="d7045-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="d7045-119">Un panneau [Émulation][DevtoolsGuideEdgehtml|::ref9::|] pour tester votre site avec différents profils de navigateur, des résolutions d’écran et des coordonnées d’emplacement GPS</span><span class="sxs-lookup"><span data-stu-id="d7045-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="d7045-120">N’hésitez pas à nous envoyer vos [commentaires et demandes de fonctionnalité](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="d7045-120">Please keep sending your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>  

> [!TIP]
> <span data-ttu-id="d7045-121">[Test sur Microsoft Edge \(EdgeHTML\) gratuit à partir de n'importe quel navigateur][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="d7045-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="d7045-122">L’équipe Microsoft Edge a collaboré avec [BrowserStack][BrowserstackEdgehtml] pour vous permettre d’effectuer des tests en ligne et automatisés gratuitement sur Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="d7045-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="d7045-123">Application du MicrosoftStore</span><span class="sxs-lookup"><span data-stu-id="d7045-123">Microsoft Store app</span></span>  

<span data-ttu-id="d7045-124">Les **DevTools Microsoft Edge \(EdgeHTML\)** sont [désormais disponibles][DevtoolsGuideEdgehtmlWhatsnew] sous la forme d’une application autonome [Windows10 à partir du Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], en plus de l’expérience d’outils dans le navigateur \ (`F12`\).</span><span class="sxs-lookup"><span data-stu-id="d7045-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="d7045-125">La version store est accompagnée d'un panneau de **Sélecteur** permettant d'associer des cibles de pages locales et distantes ouvertes et d'une mise en page à onglets permettant de passer facilement d'une instance DevTools à l'autre.</span><span class="sxs-lookup"><span data-stu-id="d7045-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="d7045-126">Débogage local</span><span class="sxs-lookup"><span data-stu-id="d7045-126">Local debugging</span></span>  

<span data-ttu-id="d7045-127">Pour déboguer une page localement, lancez simplement l’application DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d7045-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="d7045-128">Le panneau **Local** du sélecteur affiche tous les processus de contenu EdgeHTML actifs, y compris les onglets de navigateur ouvert, exécutant [PWAs][PwasEdgehtmlIndex] \ (`WWAHost.exe` processus \), et les contrôles de panneau [vue web][HostingWebview].</span><span class="sxs-lookup"><span data-stu-id="d7045-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="d7045-129">Sélectionnez la cible souhaitée à joindre et ouvrez une nouvelle instance d’onglet de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d7045-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source=".//media/chooser_local.png" alt-text="Panneau local de l’application DevTools":::
   <span data-ttu-id="d7045-131">Panneau local de l’application DevTools</span><span class="sxs-lookup"><span data-stu-id="d7045-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="d7045-132">Débogage à distance</span><span class="sxs-lookup"><span data-stu-id="d7045-132">Remote debugging</span></span>  

<span data-ttu-id="d7045-133">L’application DevTools Microsoft Edge présente la prise en charge de base pour le débogage de pages sur un ordinateur distant via le [Protocole DevTools][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="d7045-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="d7045-134">La dernière version inclut l’accès à distance aux fonctionnalités principales dans les panneaux [Débogage][DevtoolsGuideEdgehtml|::ref10::|],[Éléments][DevtoolsGuideEdgehtml|::ref11::|] \ (pour les opérations en lecture seule \) et [Console][DevtoolsGuideEdgehtml|::ref12::|].</span><span class="sxs-lookup"><span data-stu-id="d7045-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="d7045-135">Le débogage distant est limité à Microsoft Edge \(EdgeHTML\) qui exécute les hôtes de bureau, avec la prise en charge d’autres hôtes EdgeHTML et de périphériques Windows10 dans les versions à venir.</span><span class="sxs-lookup"><span data-stu-id="d7045-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="d7045-136">Pour commencer, consultez la section [*DevTools Microsoft Edge*][DevtoolsProtocolEdgehtmlClientsEdgePreview] de la documentation sur le [protocole DevTools][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="d7045-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./media/chooser_remote.png" alt-text="Panneau distant de l’application DevTools":::
   <span data-ttu-id="d7045-138">Panneau distant de l’application DevTools</span><span class="sxs-lookup"><span data-stu-id="d7045-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="d7045-139">Raccourcis généraux</span><span class="sxs-lookup"><span data-stu-id="d7045-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d7045-140">Tous les raccourcis ont été vérifiés dans la version la plus récente de Windows.</span><span class="sxs-lookup"><span data-stu-id="d7045-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="d7045-141">Si vous ne parvenez pas à utiliser un raccourci, veuillez mettre à jour votre copie de Windows.</span><span class="sxs-lookup"><span data-stu-id="d7045-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="d7045-142">Ces raccourcis contrôlent la fenêtre principale DevTools et doivent fonctionner sur tous les outils.</span><span class="sxs-lookup"><span data-stu-id="d7045-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="d7045-143">Action</span><span class="sxs-lookup"><span data-stu-id="d7045-143">Action</span></span> | <span data-ttu-id="d7045-144">Raccourci</span><span class="sxs-lookup"><span data-stu-id="d7045-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="d7045-145">Afficher/masquer DevTools \ (s’ouvre sur le panneau dernier affichage\)</span><span class="sxs-lookup"><span data-stu-id="d7045-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="d7045-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="d7045-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="d7045-147">Basculer la station d’Accueil \ (annuler la station d’accueil/bas/droite \)</span><span class="sxs-lookup"><span data-stu-id="d7045-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="d7045-148">Ouvrir un fichier</span><span class="sxs-lookup"><span data-stu-id="d7045-148">Open file</span></span> | `Ctrl`<span data-ttu-id="d7045-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="d7045-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="d7045-150">Afficher le code source HTML non modifiable dans le débogueur</span><span class="sxs-lookup"><span data-stu-id="d7045-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="d7045-151">Afficher/masquer la console en bas de tout autre outil</span><span class="sxs-lookup"><span data-stu-id="d7045-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="d7045-152">Basculer vers les éléments \(Explorateur DOM\)</span><span class="sxs-lookup"><span data-stu-id="d7045-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="d7045-153">Basculer vers la console</span><span class="sxs-lookup"><span data-stu-id="d7045-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="d7045-154">Basculer vers le débogueur</span><span class="sxs-lookup"><span data-stu-id="d7045-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="d7045-155">Basculer vers le réseau</span><span class="sxs-lookup"><span data-stu-id="d7045-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="d7045-156">Basculer vers les performances</span><span class="sxs-lookup"><span data-stu-id="d7045-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="d7045-157">Basculer vers la mémoire</span><span class="sxs-lookup"><span data-stu-id="d7045-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="d7045-158">Basculer vers l’émulation</span><span class="sxs-lookup"><span data-stu-id="d7045-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="d7045-159">Document d’aide</span><span class="sxs-lookup"><span data-stu-id="d7045-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="d7045-160">Outil suivant</span><span class="sxs-lookup"><span data-stu-id="d7045-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="d7045-161">Outil précédent</span><span class="sxs-lookup"><span data-stu-id="d7045-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="d7045-162">Outil précédent \(à partir de l’historique\)</span><span class="sxs-lookup"><span data-stu-id="d7045-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="d7045-163">Outil suivant \(à partir de l’historique\)</span><span class="sxs-lookup"><span data-stu-id="d7045-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="d7045-164">Sous-cadre suivant</span><span class="sxs-lookup"><span data-stu-id="d7045-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="d7045-165">Sous-cadre précédent</span><span class="sxs-lookup"><span data-stu-id="d7045-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="d7045-166">Correspondance suivante dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="d7045-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="d7045-167">Correspondance précédente dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="d7045-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="d7045-168">Rechercher dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="d7045-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="d7045-169">Placer le focus sur la console en bas</span><span class="sxs-lookup"><span data-stu-id="d7045-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="d7045-170">Démarrer DevTools à la console</span><span class="sxs-lookup"><span data-stu-id="d7045-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="d7045-171">Actualiser la page.</span><span class="sxs-lookup"><span data-stu-id="d7045-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="d7045-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="d7045-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="d7045-173">Si vous déboguez un point d’arrêt et que vous l’avez suspendu, l’action **Actualiser la page** reprend l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d7045-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="d7045-174">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="d7045-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="d7045-175">Envoyez-nous vos commentaires pour améliorer la DevTools de Microsoft Edge \ (EdgeHTML \) pour vous.</span><span class="sxs-lookup"><span data-stu-id="d7045-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="d7045-176">Il vous suffit d’ouvrir les outils \ (`F12`\) et de sélectionner le bouton [Envoyer des commentaires](#microsoft-edge-edgehtml-developer-tools).</span><span class="sxs-lookup"><span data-stu-id="d7045-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="d7045-177">Devenez un [Windows Insider][WindowsInsiderProgram] pour prévisualiser le [dernières fonctionnalités en provenance de la DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="d7045-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="d7045-178">Utilisez l’application Hub de commentaires Windows pour publier, voter, effectuer le suivi et obtenir de l’aide sur les suggestions et problèmes généraux de Windows.</span><span class="sxs-lookup"><span data-stu-id="d7045-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Console"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Débogueur"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elément"  Éléments
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Émulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Mémoire"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Réseau"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Niveau de performance"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Travailleurs de service"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Sauvegarde"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools dans la dernière mise à jour de Windows10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocole DevTools Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Aperçu DevTools Microsoft Edge - Clients de protocole DevTools "  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) pour les applications Windows10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Applications web progressives (EdgeHTML) sur Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Aperçu de DevTools Microsoft Edge"  

[WindowsInsiderProgram]: https://insider.windows.com "Programme WindowsInsider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Test du navigateur Microsoft Edge gratuit | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
