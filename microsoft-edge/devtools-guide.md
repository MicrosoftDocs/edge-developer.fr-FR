---
description: Découvrir les outils de développement Microsoft Edge (EdgeHTML)
title: Outils de développement Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, outils F12, devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 1abc01af5c1b058687d9ba1402911d4367b6e2b3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565586"
---
# <span data-ttu-id="5541f-104">Outils de développement Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="5541f-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

<span data-ttu-id="5541f-105">Microsoft Edge \ (EdgeHTML \) DevTools est [conçu avec la méthode de frappe][|::ref1::|Index], optimisée par une [source ouverte][GithubMicrosoftChakracore], optimisée pour les flux de travail frontal modernes et désormais disponible sous la forme d’une [application Windows 10 autonome][MicrosoftStoreEdgeDevtoolsPreview] sur le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5541f-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="5541f-106">Pour plus d’informations sur les dernières fonctionnalités, consultez [devtools la dernière mise à jour de Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="5541f-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="5541f-107">Outils principaux</span><span class="sxs-lookup"><span data-stu-id="5541f-107">Core tools</span></span>  

![Microsoft Edge \ (EdgeHTML \) DevTools][ImageDevtoolsEdgehtml]  

<span data-ttu-id="5541f-109">Microsoft Edge \ (EdgeHTML \) DevTools inclut les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="5541f-109">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="5541f-110">Panneau d' [éléments][DevtoolsGuideEdgehtml|::ref2::|] permettant de modifier les propriétés d’accessibilité, d’afficher les détecteurs d’événements et de définir des points d’arrêt de mutation DOM</span><span class="sxs-lookup"><span data-stu-id="5541f-110">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="5541f-111">Une [console][DevtoolsGuideEdgehtml|::ref3::|] pour afficher et filtrer des messages de journaux, inspecter des objets JavaScript et des nœuds DOM et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5541f-111">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="5541f-112">Le [débogueur][DevtoolsGuideEdgehtml|::ref4::|] pour parcourir le code, définir des espions et des points d’arrêt, modifier votre code et inspecter les caches de stockage et de cookies Web</span><span class="sxs-lookup"><span data-stu-id="5541f-112">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="5541f-113">Panneau [réseau][DevtoolsGuideEdgehtml|::ref5::|] permettant de surveiller et d’inspecter les demandes et les réponses du réseau et du cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="5541f-113">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="5541f-114">Panneau [performance][DevtoolsGuideEdgehtml|::ref6::|] pour le profil du temps et des ressources système requis par votre site</span><span class="sxs-lookup"><span data-stu-id="5541f-114">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="5541f-115">Panneau [mémoire][DevtoolsGuideEdgehtml|::ref7::|] permettant de mesurer votre utilisation des ressources mémoire et de comparer les instantanés de tas à différents États du runtime du code</span><span class="sxs-lookup"><span data-stu-id="5541f-115">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="5541f-116">Panneau de [stockage][DevtoolsGuideEdgehtml|::ref8::|] permettant d’inspecter et de gérer votre stockage Web, IndexedDB, les cookies et les données du cache</span><span class="sxs-lookup"><span data-stu-id="5541f-116">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="5541f-117">Panneau des [travailleurs de services][DevtoolsGuideEdgehtmlServiceworkers] pour gérer et déboguer vos travailleurs de service</span><span class="sxs-lookup"><span data-stu-id="5541f-117">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="5541f-118">Panneau d' [émulation][DevtoolsGuideEdgehtml|::ref9::|] pour tester votre site avec différents profils de navigateur, résolutions d’écran et coordonnées d’emplacement GPS</span><span class="sxs-lookup"><span data-stu-id="5541f-118">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="5541f-119">Continuez à envoyer vos [commentaires et demandes de fonctionnalité](#feedback).</span><span class="sxs-lookup"><span data-stu-id="5541f-119">Please keep sending your [feedback and feature requests](#feedback)!</span></span>  

> [!TIP]
> <span data-ttu-id="5541f-120">[Test sur Microsoft Edge \ (EdgeHTML \) gratuit depuis n’importe quel navigateur][BrowserstackEdgehtml]:</span><span class="sxs-lookup"><span data-stu-id="5541f-120">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml]:</span></span>  
> <span data-ttu-id="5541f-121">Nous nous sommes associés à [BrowserStack][BrowserstackEdgehtml] pour proposer des tests gratuits en temps réel et automatisés sur Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="5541f-121">We partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="5541f-122">Application du MicrosoftStore</span><span class="sxs-lookup"><span data-stu-id="5541f-122">Microsoft Store app</span></span>  

<span data-ttu-id="5541f-123">Le **Microsoft Edge \ (EdgeHTML \) devtools** est [désormais disponible][DevtoolsGuideEdgehtmlWhatsnew] sous la forme d’une [application Windows 10 autonome à partir du Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], en plus de l’outil`F12`de navigation intégré dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="5541f-123">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="5541f-124">La version du Windows Store est une fenêtre de **sélection** qui permet de joindre des cibles de page locales et distantes ouvertes et une disposition avec onglets pour faciliter le basculement entre les instances devtools.</span><span class="sxs-lookup"><span data-stu-id="5541f-124">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="5541f-125">Débogage local</span><span class="sxs-lookup"><span data-stu-id="5541f-125">Local debugging</span></span>  

<span data-ttu-id="5541f-126">Pour déboguer une page en local, lancez simplement l’application Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5541f-126">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="5541f-127">Le panneau **local** du sélecteur affiche tous les processus du contenu EdgeHTML actif, y compris les onglets du navigateur ouverts, en exécutant [PWAS][PwasEdgehtmlIndex] \`WWAHost.exe\` (processus \) et les contrôles [WebView][HostingWebview] .</span><span class="sxs-lookup"><span data-stu-id="5541f-127">The **Local** panel of the chooser will display all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="5541f-128">Cliquez sur la cible souhaitée pour joindre et ouvrir une nouvelle instance de l’onglet du DevTools.</span><span class="sxs-lookup"><span data-stu-id="5541f-128">Click on your desired target to attach and open a new tab instance of the DevTools.</span></span>  

![Panneau local de l’application DevTools][ImageDevtoolsGuideEdgehtmlChooselocal]  

### <span data-ttu-id="5541f-130">Débogage à distance</span><span class="sxs-lookup"><span data-stu-id="5541f-130">Remote debugging</span></span>  

<span data-ttu-id="5541f-131">L’application Microsoft Edge DevTools présente une prise en charge de base pour le débogage de pages sur un ordinateur distant par le biais de notre [protocole devtools][DevtoolsProtocolEdgehtmlIndex]nouvellement publiée.</span><span class="sxs-lookup"><span data-stu-id="5541f-131">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="5541f-132">La version la plus récente est l’accès distant aux fonctionnalités principales du [débogueur][DevtoolsGuideEdgehtml|::ref10::|], des [éléments][DevtoolsGuideEdgehtml|::ref11::|] \ (pour les opérations en lecture seule \) et des panneaux de [console][DevtoolsGuideEdgehtml|::ref12::|] .</span><span class="sxs-lookup"><span data-stu-id="5541f-132">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="5541f-133">Le débogage à distance est limité à Microsoft Edge \ (EdgeHTML \) sur l’exécution des hôtes de bureau, avec la prise en charge d’autres hôtes EdgeHTML et des appareils Windows 10 dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5541f-133">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="5541f-134">Pour commencer, consultez la section [*Microsoft Edge devtools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] des documents du [protocole devtools][DevtoolsProtocolEdgehtmlIndex] .</span><span class="sxs-lookup"><span data-stu-id="5541f-134">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

![Panneau distant de l’application DevTools][DevtoolsGuideEdgehtmlRemote]  

## <span data-ttu-id="5541f-136">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5541f-136">Feedback</span></span>  

<span data-ttu-id="5541f-137">Envoyez-nous vos commentaires pour que nous puissions continuer à améliorer Microsoft Edge \ (EdgeHTML \) DevTools pour vous.</span><span class="sxs-lookup"><span data-stu-id="5541f-137">Please send us your feedback so we can continue improving the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="5541f-138">Il suffit d’ouvrir le`F12`menu Outils () et de cliquer sur le bouton [Envoyer des commentaires](#microsoft-edge-edgehtml-developer-tools) .</span><span class="sxs-lookup"><span data-stu-id="5541f-138">Simply open the tools (`F12`) and click the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="5541f-139">Participez au programme [Windows Insider][WindowsInsiderProgram] pour prévisualiser les [fonctionnalités les plus récentes disponibles dans le devtools][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="5541f-139">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="5541f-140">Utilisez l’application Hub de commentaires Windows pour publier, faire un vote, suivre et obtenir de l’aide sur les suggestions et problèmes généraux dans Windows.</span><span class="sxs-lookup"><span data-stu-id="5541f-140">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

## <span data-ttu-id="5541f-141">Raccourcis clavier généraux</span><span class="sxs-lookup"><span data-stu-id="5541f-141">General Shortcuts</span></span>  

<span data-ttu-id="5541f-142">Ces raccourcis contrôlent la fenêtre principale de DevTools et doivent fonctionner sur tous les outils.</span><span class="sxs-lookup"><span data-stu-id="5541f-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="5541f-143">Action</span><span class="sxs-lookup"><span data-stu-id="5541f-143">Action</span></span> | <span data-ttu-id="5541f-144">Raccourci</span><span class="sxs-lookup"><span data-stu-id="5541f-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="5541f-145">Afficher/masquer DevTools \ (s’ouvre au dernier panneau affiché \)</span><span class="sxs-lookup"><span data-stu-id="5541f-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="5541f-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="5541f-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="5541f-147">Basculer entre l’ancrage \ (déconnexion</span><span class="sxs-lookup"><span data-stu-id="5541f-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="5541f-148">Ouvrir un fichier</span><span class="sxs-lookup"><span data-stu-id="5541f-148">Open file</span></span> | `Ctrl`<span data-ttu-id="5541f-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="5541f-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="5541f-150">Afficher le code source HTML non modifiable dans le débogueur</span><span class="sxs-lookup"><span data-stu-id="5541f-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="5541f-151">Afficher/masquer la console en bas de n’importe quel autre outil</span><span class="sxs-lookup"><span data-stu-id="5541f-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="5541f-152">Basculer vers les éléments \ (Explorateur DOM \)</span><span class="sxs-lookup"><span data-stu-id="5541f-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="5541f-153">Basculer vers la console</span><span class="sxs-lookup"><span data-stu-id="5541f-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="5541f-154">Basculer vers le débogueur</span><span class="sxs-lookup"><span data-stu-id="5541f-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="5541f-155">Basculer en réseau</span><span class="sxs-lookup"><span data-stu-id="5541f-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="5541f-156">Basculer vers performance</span><span class="sxs-lookup"><span data-stu-id="5541f-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="5541f-157">Basculer en mémoire</span><span class="sxs-lookup"><span data-stu-id="5541f-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="5541f-158">Basculer vers l’émulation</span><span class="sxs-lookup"><span data-stu-id="5541f-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="5541f-159">Document d’aide</span><span class="sxs-lookup"><span data-stu-id="5541f-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="5541f-160">Outil suivant</span><span class="sxs-lookup"><span data-stu-id="5541f-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="5541f-161">Outil précédent</span><span class="sxs-lookup"><span data-stu-id="5541f-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="5541f-162">Outil précédent \ (de l’historique \)</span><span class="sxs-lookup"><span data-stu-id="5541f-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="5541f-163">Outil suivant \ (de l’historique \)</span><span class="sxs-lookup"><span data-stu-id="5541f-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="5541f-164">Sous-image suivante</span><span class="sxs-lookup"><span data-stu-id="5541f-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="5541f-165">Sous-cadre précédent</span><span class="sxs-lookup"><span data-stu-id="5541f-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="5541f-166">Résultat suivant dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="5541f-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="5541f-167">Résultat précédent dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="5541f-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="5541f-168">Rechercher dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="5541f-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="5541f-169">Mettre le focus sur la console en bas</span><span class="sxs-lookup"><span data-stu-id="5541f-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="5541f-170">Lancer DevTools vers la console</span><span class="sxs-lookup"><span data-stu-id="5541f-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="5541f-171">Actualiser la page</span><span class="sxs-lookup"><span data-stu-id="5541f-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="5541f-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="5541f-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="5541f-173">Si vous effectuez un débogage et une pause à un point d’arrêt, l’action **Actualiser la page** réactive d’abord le Runtime.</span><span class="sxs-lookup"><span data-stu-id="5541f-173">If you're debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>

<!-- image links  -->  

[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  
[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "Panneau local de l’application DevTools"  
[DevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "Panneau distant de l’application DevTools"  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Console"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Débogueur"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elément"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Émulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Mémoires"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Équilibrage"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Les"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Travailleurs de service"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Capacité"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools la dernière mise à jour de Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocole DevTools de Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clients du protocole Microsoft Edge DevTools Preview-DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) pour les applications Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Applications Web progressives (EdgeHTML) sur Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools preview"  

[WindowsInsiderProgram]: https://insider.windows.com "Programme Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Test du navigateur Microsoft Edge gratuitement | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "Dactylographié"  
