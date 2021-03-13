---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, expérimentation
ms.openlocfilehash: 612b3b83aee1ee9035982e58e008395ec3645b2b
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408303"
---
# <a name="experimental-features"></a><span data-ttu-id="bb711-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="bb711-104">Experimental features</span></span>  

<span data-ttu-id="bb711-105">Microsoft Edge DevTools permet d’accéder aux fonctionnalités expérimentales qui sont encore en développement.</span><span class="sxs-lookup"><span data-stu-id="bb711-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="bb711-106">Vous pouvez tester et [fournir des commentaires](#providing-feedback-on-experimental-features) avant la publication de chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bb711-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="bb711-107">Bien que les fonctionnalités expérimentales soient disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal Canary de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bb711-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="bb711-108">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="bb711-108">Turn on experimental features</span></span>  

<span data-ttu-id="bb711-109">Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb711-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="bb711-110">[Ouvrez DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="bb711-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="bb711-111">Sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="bb711-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="bb711-112">Pour plus d’informations, accédez aux raccourcis clavier de [Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="bb711-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="bb711-113">Ouvrez [le volet Paramètres.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="bb711-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="bb711-114">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="bb711-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="bb711-115">Pour plus d’informations, accédez aux raccourcis clavier de [Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="bb711-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="bb711-116">Sur le côté gauche du volet **Paramètres,** choisissez la section **Expériences.**</span><span class="sxs-lookup"><span data-stu-id="bb711-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Page Expériences dans Paramètres" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="bb711-118">Page **Expériences** dans **Paramètres**</span><span class="sxs-lookup"><span data-stu-id="bb711-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb711-119">Dans la page Expériences, parcourez la liste de toutes les **fonctionnalités expérimentales** disponibles et cochez la case en regard de chaque fonctionnalité que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="bb711-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="bb711-120">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="bb711-121">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="bb711-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="bb711-122">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **Expériences** et cochez la case de la fonctionnalité expérimentale que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="bb711-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="bb711-123">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="bb711-123">Highlighted experimental features</span></span>  

<span data-ttu-id="bb711-124">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bb711-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="bb711-125">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="bb711-125">Experimental feature</span></span> | <span data-ttu-id="bb711-126">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bb711-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="bb711-127">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="bb711-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="bb711-128">85 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-128">85 or later</span></span> |  
| [<span data-ttu-id="bb711-129">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="bb711-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="bb711-130">85 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-130">85 or later</span></span> |  
| [<span data-ttu-id="bb711-131">Visionneuse de commandes source</span><span class="sxs-lookup"><span data-stu-id="bb711-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="bb711-132">86 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-132">86 or later</span></span> |  
| [<span data-ttu-id="bb711-133">Activer les couches composites en vue 3D</span><span class="sxs-lookup"><span data-stu-id="bb711-133">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="bb711-134">87 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-134">87 or later</span></span> |  
| [<span data-ttu-id="bb711-135">Activer le nouvel outil Éditeur de polices dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="bb711-135">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="bb711-136">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-136">89 or later</span></span> |  
| [<span data-ttu-id="bb711-137">Activer les nouvelles fonctionnalités de débogage Flexbox CSS</span><span class="sxs-lookup"><span data-stu-id="bb711-137">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="bb711-138">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-138">89 or later</span></span> |  
| [<span data-ttu-id="bb711-139">Activer + les menus onglet de bouton pour ouvrir d’autres outils</span><span class="sxs-lookup"><span data-stu-id="bb711-139">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="bb711-140">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-140">89 or later</span></span> |  
| [<span data-ttu-id="bb711-141">Activer l’onglet Bienvenue</span><span class="sxs-lookup"><span data-stu-id="bb711-141">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="bb711-142">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb711-142">89 or later</span></span> |  

### <a name="enable-webhint"></a><span data-ttu-id="bb711-143">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="bb711-143">Enable webhint</span></span>  

<span data-ttu-id="bb711-144">[webhint est][WebhintMain] un outil open source qui fournit des commentaires en temps réel pour les sites web et les pages web locales.</span><span class="sxs-lookup"><span data-stu-id="bb711-144">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="bb711-145">Type de commentaires fourni par [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="bb711-145">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="bb711-146">accessibilité</span><span class="sxs-lookup"><span data-stu-id="bb711-146">accessibility</span></span>  
*   <span data-ttu-id="bb711-147">compatibilité entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="bb711-147">cross-browser compatibility</span></span>  
*   <span data-ttu-id="bb711-148">sécurité</span><span class="sxs-lookup"><span data-stu-id="bb711-148">security</span></span>  
*   <span data-ttu-id="bb711-149">performance</span><span class="sxs-lookup"><span data-stu-id="bb711-149">performance</span></span>  
*   <span data-ttu-id="bb711-150">Applications web progressives (P.A.S.)</span><span class="sxs-lookup"><span data-stu-id="bb711-150">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="bb711-151">autres problèmes de développement web courants</span><span class="sxs-lookup"><span data-stu-id="bb711-151">other common web development issues</span></span>  
    
<span data-ttu-id="bb711-152">[L’expérience webhint][WebhintMain] affiche les commentaires sur le web dans le [panneau Problèmes.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="bb711-152">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="bb711-153">Choisissez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site web.</span><span class="sxs-lookup"><span data-stu-id="bb711-153">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="bb711-154">Choisissez un lien de ressource pour ouvrir \*\*\*\* le volet **Réseau,** **Sources**ou Éléments approprié dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-154">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="commentaires webhint dans le panneau Problèmes" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="bb711-156">commentaires webhint dans le **panneau Problèmes**</span><span class="sxs-lookup"><span data-stu-id="bb711-156">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="bb711-157">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="bb711-157">Enable Network Console</span></span>  

<span data-ttu-id="bb711-158">**Network Console est** le titre de travail d’une expérience pour effectuer des demandes de réseau synthétiques sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="bb711-158">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="bb711-159">Vous pouvez utiliser l’expérience **console** réseau pour envoyer des demandes d’API web.</span><span class="sxs-lookup"><span data-stu-id="bb711-159">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="bb711-160">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-160">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bb711-161">Pour utiliser la **console réseau,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb711-161">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bb711-162">Ouvrez **le volet** Réseau.</span><span class="sxs-lookup"><span data-stu-id="bb711-162">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="bb711-163">Recherchez la demande réseau que vous souhaitez modifier et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="bb711-163">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="bb711-164">Ouvrez le menu contextuel \(clic droit\), puis choisissez **Modifier et relire.**</span><span class="sxs-lookup"><span data-stu-id="bb711-164">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="bb711-165">Lorsque la **console réseau s’ouvre,** modifiez les informations de demande réseau.</span><span class="sxs-lookup"><span data-stu-id="bb711-165">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="bb711-166">Choose **Send**.</span><span class="sxs-lookup"><span data-stu-id="bb711-166">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console réseau dans le caisse de la console" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="bb711-168">**Console réseau dans** le caisse **de la** console</span><span class="sxs-lookup"><span data-stu-id="bb711-168">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="bb711-169">Visionneuse de commandes source</span><span class="sxs-lookup"><span data-stu-id="bb711-169">Source Order Viewer</span></span>  

<span data-ttu-id="bb711-170">**L’Afficheur des** commandes source est une expérience qui affiche l’ordre des éléments dans la source de la page web.</span><span class="sxs-lookup"><span data-stu-id="bb711-170">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="bb711-171">L’ordre d’affichage à l’écran peut différer de l’ordre de la source, ce qui peut dérouter les utilisateurs du lecteur d’écran et du clavier.</span><span class="sxs-lookup"><span data-stu-id="bb711-171">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="bb711-172">Utilisez **l’expérience de l’Observateur** d’ordre de commandes source pour rechercher les différences entre l’ordre d’affichage à l’écran et l’ordre de la source.</span><span class="sxs-lookup"><span data-stu-id="bb711-172">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="bb711-173">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-173">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bb711-174">Pour utiliser **l’Observateur de commandes source,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb711-174">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bb711-175">Ouvrez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="bb711-175">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="bb711-176">Ouvrez **le volet Accessibilité** dans le panneau de caisse \(bas\).</span><span class="sxs-lookup"><span data-stu-id="bb711-176">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="bb711-177">Sous la section **Visionneuse de commandes** source, cochez la case Afficher la **commande source.**</span><span class="sxs-lookup"><span data-stu-id="bb711-177">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="bb711-178">Mettez en surbrillez n’importe quel élément HTML pour afficher une superposition que l’ordre dans la source de la page web.</span><span class="sxs-lookup"><span data-stu-id="bb711-178">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet Accessibilité" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="bb711-180">**Visionneuse de commandes source** **dans le volet** Accessibilité</span><span class="sxs-lookup"><span data-stu-id="bb711-180">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="bb711-181">Activer les couches composites en vue 3D</span><span class="sxs-lookup"><span data-stu-id="bb711-181">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="bb711-182">Vous pouvez maintenant visualiser calques avec les index z et le modèle objet de document \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="bb711-182">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="bb711-183">Cette fonctionnalité vous permet de déboguer sans changer de contexte aussi souvent.</span><span class="sxs-lookup"><span data-stu-id="bb711-183">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="bb711-184">Vous avez identifié que la réduction du basculement de contexte était un problème majeur.</span><span class="sxs-lookup"><span data-stu-id="bb711-184">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="bb711-185">Il n’est pas toujours clair comment le code que vous écrivez affecte votre application web.</span><span class="sxs-lookup"><span data-stu-id="bb711-185">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="bb711-186">Pour une expérience complète de débogage, l’affichage 3D et les couches composites sont désormais combinés.</span><span class="sxs-lookup"><span data-stu-id="bb711-186">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="bb711-187">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-187">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bb711-188">Pour utiliser **les couches composites,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb711-188">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bb711-189">Dans le caisse, choisissez **l’outil d’affichage 3D.**</span><span class="sxs-lookup"><span data-stu-id="bb711-189">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="bb711-190">Ouvrez **le volet Calques composites.**</span><span class="sxs-lookup"><span data-stu-id="bb711-190">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="bb711-191">Toutes les couches peints de l’application sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bb711-191">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="bb711-192">Essayez cette fonctionnalité avec vos propres applications web.</span><span class="sxs-lookup"><span data-stu-id="bb711-192">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Volet des couches composites" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="bb711-194">Volet des **couches composites**</span><span class="sxs-lookup"><span data-stu-id="bb711-194">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="bb711-195">Activer le nouvel outil Éditeur de polices dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="bb711-195">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="bb711-196">Vous pouvez désormais utiliser le nouvel éditeur de [polices][DevtoolsInspectStylesEditFonts] visuel pour modifier les polices.</span><span class="sxs-lookup"><span data-stu-id="bb711-196">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="bb711-197">Utilisez-la pour définir les polices et les caractéristiques de police.</span><span class="sxs-lookup"><span data-stu-id="bb711-197">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="bb711-198">Visual **Font Editor vous** aide à effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb711-198">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="bb711-199">Basculer entre les unités pour différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="bb711-199">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="bb711-200">Basculer entre les mots clés pour différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="bb711-200">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="bb711-201">Convertir des unités</span><span class="sxs-lookup"><span data-stu-id="bb711-201">Convert units</span></span>  
*   <span data-ttu-id="bb711-202">Générer un code CSS précis</span><span class="sxs-lookup"><span data-stu-id="bb711-202">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="bb711-203">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-203">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bb711-204">Pour utiliser le nouvel éditeur de **polices**visuel, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb711-204">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bb711-205">Ouvrez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="bb711-205">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="bb711-206">Ouvrez **le volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="bb711-206">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="bb711-207">Sélectionnez **l’icône Éditeur de** polices.</span><span class="sxs-lookup"><span data-stu-id="bb711-207">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="bb711-208">Pour plus d’informations sur le nouvel éditeur de **polices**visuel, accédez à Modifier les styles de police CSS et les paramètres dans le volet Styles dans [DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="bb711-208">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Le volet Visual Font Editor est mis en surbrill" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="bb711-210">Le volet **Visual Font Editor** est mis en surbrill</span><span class="sxs-lookup"><span data-stu-id="bb711-210">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="bb711-211">Activer les nouvelles fonctionnalités de débogage Flexbox CSS</span><span class="sxs-lookup"><span data-stu-id="bb711-211">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="bb711-212">Cette fonctionnalité expérimentale fournit de nombreuses nouvelles visualisations pour vous aider à déboguer les dispositions flexbox CSS.</span><span class="sxs-lookup"><span data-stu-id="bb711-212">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="bb711-213">Pour afficher un aperçu des dernières fonctionnalités expérimentales, [activer cette expérience](#turn-on-experimental-features) et recharger DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-213">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="bb711-214">Afficher des superpositions persistantes sur les dispositions Flexbox à l’aide de l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="bb711-214">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="bb711-215">**L’outil Inspect** permet d’identifier et de visualiser rapidement les dispositions flexbox CSS dans un site web en pointant dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="bb711-215">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="bb711-216">Choisissez **l’icône Inspect** \( Inspect \) dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-216">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="bb711-217">Ensuite, lors du débogage du site web, pointez sur un conteneur flexible pour afficher les contours autour du conteneur flexible.</span><span class="sxs-lookup"><span data-stu-id="bb711-217">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Afficher les conteneurs Flexbox avec l’outil Inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="bb711-219">Afficher les conteneurs Flexbox avec **l’outil Inspect**</span><span class="sxs-lookup"><span data-stu-id="bb711-219">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="bb711-220">Afficher des superpositions persistantes sur les dispositions Flexbox</span><span class="sxs-lookup"><span data-stu-id="bb711-220">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="bb711-221">Dans Microsoft Edge version 89 ou ultérieure, la fonctionnalité expérimentale CSS Flexbox offre également la possibilité d’activer les superpositions persistantes sur les dispositions Flexbox.</span><span class="sxs-lookup"><span data-stu-id="bb711-221">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="bb711-222">Les superpositions persistantes offrent les avantages suivants.</span><span class="sxs-lookup"><span data-stu-id="bb711-222">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="bb711-223">Les superpositions persistantes restent visibles sur la page web lorsque vous faites défiler, déplacez votre souris et utilisez d’autres fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-223">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="bb711-224">Plusieurs superpositions persistantes peuvent être utilisées en même temps, pour vous permettre de passer en revue plusieurs dispositions Flexbox à la fois.</span><span class="sxs-lookup"><span data-stu-id="bb711-224">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="bb711-225">Les superpositions persistantes offrent des options de configuration des couleurs.</span><span class="sxs-lookup"><span data-stu-id="bb711-225">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="bb711-226">Pour faire bascule les superpositions persistantes sur la disposition Flexbox, utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb711-226">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="bb711-227">Choisissez **l’icône ovale Flexbox** en face de n’importe quel conteneur Flexbox affiché dans l’arborescence DOM de **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="bb711-227">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="bb711-228">Ouvrez le nouveau **panneau de** disposition situé dans l’outil **Éléments,** puis cochez la case en regard de chaque conteneur Flexbox à mettre en surbrillion.</span><span class="sxs-lookup"><span data-stu-id="bb711-228">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Icônes flexibles et panneau de disposition dans DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="bb711-230">Icônes flexibles et **panneau de** disposition dans DevTools</span><span class="sxs-lookup"><span data-stu-id="bb711-230">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="bb711-231">Configurer des superpositions persistantes</span><span class="sxs-lookup"><span data-stu-id="bb711-231">Configure persistent overlays</span></span>  

<span data-ttu-id="bb711-232">Pour configurer les options des superpositions persistantes pour les grilles CSS ou les dispositions Flexbox, utilisez **le** volet Disposition.</span><span class="sxs-lookup"><span data-stu-id="bb711-232">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="bb711-233">Le **volet** Disposition se trouve dans l’outil **Éléments** en plus des **volets Styles** **et** Calculés.</span><span class="sxs-lookup"><span data-stu-id="bb711-233">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panneau de disposition" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="bb711-235">Panneau de disposition</span><span class="sxs-lookup"><span data-stu-id="bb711-235">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="bb711-236">Activer + les menus onglet de bouton pour ouvrir d’autres outils</span><span class="sxs-lookup"><span data-stu-id="bb711-236">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="bb711-237">Vous pouvez maintenant ouvrir d’autres outils à l’aide de la nouvelle icône **Plus d’outils** `+` \( \).</span><span class="sxs-lookup"><span data-stu-id="bb711-237">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="bb711-238">Une fois que vous avez activé les menus Onglet Activer **+** bouton pour ouvrir d’autres outils et recharger DevTools, un signe plus \( \) s’affiche à droite du groupe d’onglets en haut de `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-238">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="bb711-239">Pour afficher la liste des autres outils que vous pouvez ajouter à la barre d’onglets, choisissez la nouvelle icône Outils plus **\(** `+` \).</span><span class="sxs-lookup"><span data-stu-id="bb711-239">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Autres outils dans le volet supérieur" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="bb711-241">**Autres outils** dans le volet supérieur</span><span class="sxs-lookup"><span data-stu-id="bb711-241">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="bb711-242">Activer l’outil d’accueil</span><span class="sxs-lookup"><span data-stu-id="bb711-242">Enable Welcome tool</span></span>

<span data-ttu-id="bb711-243">Cette expérience remplace **l’outil Nouveautés** par le nouvel **outil Welcome.**</span><span class="sxs-lookup"><span data-stu-id="bb711-243">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="bb711-244">Il affiche une conception actualisée pour le contenu suivant.</span><span class="sxs-lookup"><span data-stu-id="bb711-244">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="bb711-245">Liens vers des documents de développement</span><span class="sxs-lookup"><span data-stu-id="bb711-245">Links to developer docs</span></span>  
*   <span data-ttu-id="bb711-246">fonctionnalités les plus récentes</span><span class="sxs-lookup"><span data-stu-id="bb711-246">the latest features</span></span>  
*   <span data-ttu-id="bb711-247">notes de publication</span><span class="sxs-lookup"><span data-stu-id="bb711-247">release notes</span></span>  
*   <span data-ttu-id="bb711-248">Option de contact de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bb711-248">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="bb711-249">**L’outil** Welcome s’ouvre automatiquement après chaque mise à jour de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bb711-249">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="bb711-250">Pour empêcher l’affichage de l’outil **Welcome** après \*\*\*\* chaque mise à jour, cochez la case en regard de l’onglet Ouvrir après chaque mise à jour sous le titre de **l’outil** Welcome.</span><span class="sxs-lookup"><span data-stu-id="bb711-250">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="bb711-251">Si vous préférez **l’outil Nouveautés d’origine,** accédez à [Expériences][DevtoolsCustomizeIndexSettings]de paramètres et supprimez la case à cocher en regard de l’onglet  >  \*\*\*\* **Activer l’accueil.**</span><span class="sxs-lookup"><span data-stu-id="bb711-251">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Outil d’accueil" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="bb711-253">**Outil d’accueil**</span><span class="sxs-lookup"><span data-stu-id="bb711-253">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="bb711-254">Fonctionnalités expérimentales précédentes</span><span class="sxs-lookup"><span data-stu-id="bb711-254">Previous experimental features</span></span>  

*   <span data-ttu-id="bb711-255">[L’affichage 3D][Devtools3dViewIndex] est désormais disponible et est allumé par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb711-255">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="bb711-256">[Activer la prise en charge pour déplacer des onglets][DevtoolsCustomizeIndex] entre les panneaux est désormais disponible et est désactivée par défaut dans Microsoft Edge version 85 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb711-256">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="bb711-257">Faire correspondre les raccourcis clavier de [DevTools][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] à Microsoft Visual Studio Code est désormais disponible et est allumé par défaut dans Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb711-257">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="bb711-258">La modification des raccourcis clavier pour toute action dans [DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] est désormais disponible et est désactivée par défaut dans Microsoft Edge version 89 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb711-258">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="bb711-259">[L’option Activer les nouvelles][DevtoolsCssGrid] fonctionnalités de débogage de grille CSS est désormais disponible et est désactivée par défaut dans Microsoft Edge version 89 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb711-259">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="bb711-260">[Émulation : le mode double écran][DevtoolsDeviceModeDualScreenAndFoldables] de prise en charge est désormais disponible et est allumé par défaut dans Microsoft Edge version 90 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb711-260">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="bb711-261">Commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="bb711-261">Providing feedback on experimental features</span></span>  

<span data-ttu-id="bb711-262">Pour fournir des commentaires sur les expériences DevTools de Microsoft Edge ou sur tout autre point lié à DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb711-262">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="bb711-263">Envoyez vos commentaires à l’aide **de l’icône** Envoyer des commentaires dans DevTools</span><span class="sxs-lookup"><span data-stu-id="bb711-263">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="bb711-264">Tweet à [l'@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="bb711-264">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="L’Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="bb711-266">L’Icône **Envoyer des commentaires** dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bb711-266">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Personnaliser microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Modifier les raccourcis clavier pour toute action dans le | Documents Microsoft"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Faire correspondre les raccourcis clavier des DevTools à microsoft Visual Studio Code | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Documents Microsoft"  
[DevtoolsIssuesIndex]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpenIndex]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Raccourcis clavier Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools | Documents Microsoft"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
