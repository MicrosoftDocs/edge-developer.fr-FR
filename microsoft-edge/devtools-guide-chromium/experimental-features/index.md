---
description: Les dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, expérimentation
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: 82d547c8c1ed0606bda9ade27d0dbddbfa2ca800
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11596998"
---
# <a name="experimental-features"></a><span data-ttu-id="4f205-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="4f205-104">Experimental features</span></span>  

<span data-ttu-id="4f205-105">Microsoft Edge DevTools permet d’accéder aux fonctionnalités expérimentales qui sont encore en développement.</span><span class="sxs-lookup"><span data-stu-id="4f205-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="4f205-106">Vous pouvez tester et [fournir des commentaires](#providing-feedback-on-experimental-features) avant la publication de chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4f205-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="4f205-107">Bien que les fonctionnalités expérimentales soient disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide canal Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="4f205-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="4f205-108">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="4f205-108">Turn on experimental features</span></span>  

<span data-ttu-id="4f205-109">Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f205-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="4f205-110">[Ouvrez DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="4f205-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="4f205-111">Sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="4f205-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="4f205-112">Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="4f205-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="4f205-113">Ouvrez [Paramètres][DevToolsCustomizeIndexSettings] volet.</span><span class="sxs-lookup"><span data-stu-id="4f205-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="4f205-114">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="4f205-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="4f205-115">Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="4f205-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="4f205-116">Sur le côté gauche du volet **Paramètres,** choisissez la section **Expériences.**</span><span class="sxs-lookup"><span data-stu-id="4f205-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Page Expériences dans Paramètres" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="4f205-118">Page **Expériences** dans **Paramètres**</span><span class="sxs-lookup"><span data-stu-id="4f205-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f205-119">Dans la page **Expériences,** parcourez la liste de toutes les fonctionnalités expérimentales disponibles et cochez la case en regard de chaque fonctionnalité à tester.</span><span class="sxs-lookup"><span data-stu-id="4f205-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="4f205-120">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="4f205-121">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="4f205-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="4f205-122">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **Expériences** et cochez la case de la fonctionnalité expérimentale que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="4f205-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="4f205-123">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="4f205-123">Highlighted experimental features</span></span>  

<span data-ttu-id="4f205-124">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4f205-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="4f205-125">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="4f205-125">Experimental feature</span></span> | <span data-ttu-id="4f205-126">Microsoft Edge version</span><span class="sxs-lookup"><span data-stu-id="4f205-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | <span data-ttu-id="4f205-127">85 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-127">85 or later</span></span> |  
| [Enable Network Console](#enable-network-console) | <span data-ttu-id="4f205-128">85 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-128">85 or later</span></span> |  
| [Source Order Viewer](#source-order-viewer) | <span data-ttu-id="4f205-129">86 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-129">86 or later</span></span> |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | <span data-ttu-id="4f205-130">87 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-130">87 or later</span></span> |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="4f205-131">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-131">89 or later</span></span> |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="4f205-132">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-132">89 or later</span></span> |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="4f205-133">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-133">89 or later</span></span> |  
| [Enable Welcome tab](#enable-welcome-tab) | <span data-ttu-id="4f205-134">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f205-134">89 or later</span></span> |  

### Enable webhint  

<span data-ttu-id="4f205-135">[webhint est][WebhintMain] un outil open source qui fournit des commentaires en temps réel pour les sites web et les pages web locales.</span><span class="sxs-lookup"><span data-stu-id="4f205-135">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="4f205-136">Type de commentaires fourni par [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="4f205-136">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="4f205-137">accessibilité</span><span class="sxs-lookup"><span data-stu-id="4f205-137">accessibility</span></span>  
*   <span data-ttu-id="4f205-138">compatibilité entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="4f205-138">cross-browser compatibility</span></span>  
*   <span data-ttu-id="4f205-139">sécurité</span><span class="sxs-lookup"><span data-stu-id="4f205-139">security</span></span>  
*   <span data-ttu-id="4f205-140">performance</span><span class="sxs-lookup"><span data-stu-id="4f205-140">performance</span></span>  
*   <span data-ttu-id="4f205-141">Applications web progressives (P.A.S.)</span><span class="sxs-lookup"><span data-stu-id="4f205-141">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="4f205-142">autres problèmes courants de développement web</span><span class="sxs-lookup"><span data-stu-id="4f205-142">other common web development issues</span></span>  
    
<span data-ttu-id="4f205-143">[L’expérience webhint][WebhintMain] affiche les commentaires sur le web dans le [panneau Problèmes.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="4f205-143">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="4f205-144">Choisissez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site web.</span><span class="sxs-lookup"><span data-stu-id="4f205-144">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="4f205-145">Choisissez un lien de ressource pour ouvrir \*\*\*\* le volet **Réseau,** **Sources**ou Éléments approprié dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-145">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="commentaires webhint dans le panneau Problèmes" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="4f205-147">commentaires webhint dans le **panneau Problèmes**</span><span class="sxs-lookup"><span data-stu-id="4f205-147">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

<span data-ttu-id="4f205-148">**Network Console est** le titre de travail d’une expérience pour effectuer des demandes de réseau synthétiques sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f205-148">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="4f205-149">Vous pouvez utiliser l’expérience **console** réseau pour envoyer des demandes d’API web.</span><span class="sxs-lookup"><span data-stu-id="4f205-149">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="4f205-150">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-150">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="4f205-151">Pour utiliser la **console réseau,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f205-151">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="4f205-152">Ouvrez **le volet** Réseau.</span><span class="sxs-lookup"><span data-stu-id="4f205-152">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="4f205-153">Recherchez la demande réseau que vous souhaitez modifier et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="4f205-153">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="4f205-154">Ouvrez le menu contextuel \(clic droit\), puis choisissez **Modifier et relire.**</span><span class="sxs-lookup"><span data-stu-id="4f205-154">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="4f205-155">Lorsque la **console réseau s’ouvre,** modifiez les informations de demande réseau.</span><span class="sxs-lookup"><span data-stu-id="4f205-155">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="4f205-156">Choose **Send**.</span><span class="sxs-lookup"><span data-stu-id="4f205-156">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console réseau dans le caisse de la console" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="4f205-158">**Console réseau dans** le caisse **de la** console</span><span class="sxs-lookup"><span data-stu-id="4f205-158">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

<span data-ttu-id="4f205-159">**Source Order Viewer** est une expérience qui affiche l’ordre des éléments dans la source de la page web.</span><span class="sxs-lookup"><span data-stu-id="4f205-159">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="4f205-160">L’ordre d’affichage à l’écran peut différer de l’ordre de la source, ce qui peut dérouter les utilisateurs du lecteur d’écran et du clavier.</span><span class="sxs-lookup"><span data-stu-id="4f205-160">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="4f205-161">Utilisez l’expérience pour rechercher les différences entre l’ordre d’affichage à l’écran **Source Order Viewer** et l’ordre de la source.</span><span class="sxs-lookup"><span data-stu-id="4f205-161">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="4f205-162">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-162">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="4f205-163">Pour utiliser **Source Order Viewer** , complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f205-163">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="4f205-164">Ouvrez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="4f205-164">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="4f205-165">À droite de l’onglet **Styles,** sélectionnez **l’onglet** Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="4f205-165">To the right of the **Styles** tab, select the **Accessibility** tab.</span></span>  
1.  <span data-ttu-id="4f205-166">Sous la **Source Order Viewer** section, cochez **la case Afficher** la commande source.</span><span class="sxs-lookup"><span data-stu-id="4f205-166">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="4f205-167">Mettez en surbrillez n’importe quel élément HTML pour afficher une superposition que l’ordre dans la source de la page web.</span><span class="sxs-lookup"><span data-stu-id="4f205-167">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text=":::<span data-ttu-id="4f205-168">no-loc(Source Order Viewer) ::: in the Accessibility pane» lightbox=».. /media/experiments-source-order-viewer.msft.png»::: dans le volet **Source Order Viewer** Accessibilité \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4f205-168">no-loc(Source Order Viewer)::: in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png"::: **Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

<span data-ttu-id="4f205-169">Vous pouvez maintenant visualiser calques avec les index z et le modèle objet de document \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="4f205-169">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="4f205-170">Cette fonctionnalité vous permet de déboguer sans changer de contexte aussi souvent.</span><span class="sxs-lookup"><span data-stu-id="4f205-170">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="4f205-171">Vous avez identifié que la réduction du basculement de contexte était un problème majeur.</span><span class="sxs-lookup"><span data-stu-id="4f205-171">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="4f205-172">Il n’est pas toujours évident de savoir comment le code que vous écrivez affecte votre application web.</span><span class="sxs-lookup"><span data-stu-id="4f205-172">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="4f205-173">Pour une expérience de débogage visuel complète, les couches composites et les couches 3D View composites sont désormais combinées.</span><span class="sxs-lookup"><span data-stu-id="4f205-173">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="4f205-174">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-174">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="4f205-175">Pour utiliser **les couches composites,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f205-175">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="4f205-176">Dans le caisse, choisissez **3D View** l’outil.</span><span class="sxs-lookup"><span data-stu-id="4f205-176">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="4f205-177">Ouvrez **le volet Calques composites.**</span><span class="sxs-lookup"><span data-stu-id="4f205-177">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="4f205-178">Toutes les couches peints de l’application sont affichées.</span><span class="sxs-lookup"><span data-stu-id="4f205-178">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="4f205-179">Essayez cette fonctionnalité avec vos propres applications web.</span><span class="sxs-lookup"><span data-stu-id="4f205-179">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Volet des couches composites" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="4f205-181">Volet des **couches composites**</span><span class="sxs-lookup"><span data-stu-id="4f205-181">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

<span data-ttu-id="4f205-182">Vous pouvez désormais utiliser le nouvel éditeur de [polices][DevtoolsInspectStylesEditFonts] visuel pour modifier les polices.</span><span class="sxs-lookup"><span data-stu-id="4f205-182">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="4f205-183">Utilisez-la pour définir les polices et les caractéristiques de police.</span><span class="sxs-lookup"><span data-stu-id="4f205-183">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="4f205-184">Visual **Font Editor vous** aide à effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f205-184">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="4f205-185">Basculer entre les unités concernant différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="4f205-185">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="4f205-186">Basculer entre les mots clés de différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="4f205-186">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="4f205-187">Convertir des unités</span><span class="sxs-lookup"><span data-stu-id="4f205-187">Convert units</span></span>  
*   <span data-ttu-id="4f205-188">Générer un code CSS précis</span><span class="sxs-lookup"><span data-stu-id="4f205-188">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="4f205-189">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-189">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="4f205-190">Pour utiliser le nouvel éditeur de **polices**visuel, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f205-190">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="4f205-191">Ouvrez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="4f205-191">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="4f205-192">Ouvrez **le volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="4f205-192">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="4f205-193">Sélectionnez **l’icône Éditeur de** polices.</span><span class="sxs-lookup"><span data-stu-id="4f205-193">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="4f205-194">Pour plus d’informations sur le nouvel éditeur de polices **visuel,** accédez à Modifier les styles de police CSS et les paramètres dans le volet Styles dans [DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="4f205-194">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Le volet Visual Font Editor est mis en surbrill" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="4f205-196">Le volet **Visual Font Editor** est mis en surbrill</span><span class="sxs-lookup"><span data-stu-id="4f205-196">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

<span data-ttu-id="4f205-197">Cette fonctionnalité expérimentale fournit de nombreuses nouvelles visualisations pour vous aider à déboguer les dispositions flexbox CSS.</span><span class="sxs-lookup"><span data-stu-id="4f205-197">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="4f205-198">Pour afficher un aperçu des dernières fonctionnalités expérimentales, [allumez cette expérience](#turn-on-experimental-features) et rechargez DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-198">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="4f205-199">Afficher des superpositions persistantes sur les dispositions Flexbox à l’aide de l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="4f205-199">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="4f205-200">**L’outil Inspect** permet d’identifier et de visualiser rapidement les dispositions flexbox CSS dans un site web en pointant dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="4f205-200">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="4f205-201">Choisissez **l’icône Inspect** \( Inspect \) dans le ![ coin supérieur gauche de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-201">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="4f205-202">Ensuite, lors du débogage du site web, pointez sur un conteneur flexible pour afficher les contours autour du conteneur flexible.</span><span class="sxs-lookup"><span data-stu-id="4f205-202">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Afficher les conteneurs Flexbox avec l’outil Inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="4f205-204">Afficher les conteneurs Flexbox avec **l’outil Inspect**</span><span class="sxs-lookup"><span data-stu-id="4f205-204">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="4f205-205">Afficher des superpositions persistantes sur les dispositions Flexbox</span><span class="sxs-lookup"><span data-stu-id="4f205-205">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="4f205-206">Dans Microsoft Edge version 89 ou ultérieure, la fonctionnalité expérimentale CSS Flexbox offre également la possibilité d’activer les superpositions persistantes sur les dispositions Flexbox.</span><span class="sxs-lookup"><span data-stu-id="4f205-206">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="4f205-207">Les superpositions persistantes offrent les avantages suivants.</span><span class="sxs-lookup"><span data-stu-id="4f205-207">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="4f205-208">Les superpositions persistantes restent visibles sur la page web lorsque vous faites défiler, déplacez votre souris et utilisez d’autres fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-208">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="4f205-209">Plusieurs superpositions persistantes peuvent être utilisées en même temps, pour vous permettre de passer en revue plusieurs dispositions Flexbox à la fois.</span><span class="sxs-lookup"><span data-stu-id="4f205-209">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="4f205-210">Les superpositions persistantes offrent des options de configuration des couleurs.</span><span class="sxs-lookup"><span data-stu-id="4f205-210">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="4f205-211">Pour faire bascule les superpositions persistantes sur la disposition Flexbox, utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f205-211">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="4f205-212">Choisissez **l’icône ovale Flexbox** en face de n’importe quel conteneur Flexbox affiché dans l’arborescence DOM de **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="4f205-212">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="4f205-213">Ouvrez le nouveau **panneau de** disposition situé dans l’outil **Éléments,** puis cochez la case en regard de chaque conteneur Flexbox à mettre en surbrillion.</span><span class="sxs-lookup"><span data-stu-id="4f205-213">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Icônes flexibles et panneau de disposition dans DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="4f205-215">Icônes flexibles et **panneau de** disposition dans DevTools</span><span class="sxs-lookup"><span data-stu-id="4f205-215">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="4f205-216">Configurer des superpositions persistantes</span><span class="sxs-lookup"><span data-stu-id="4f205-216">Configure persistent overlays</span></span>  

<span data-ttu-id="4f205-217">Pour configurer les options des superpositions persistantes pour les grilles CSS ou les dispositions Flexbox, utilisez **le** volet Disposition.</span><span class="sxs-lookup"><span data-stu-id="4f205-217">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="4f205-218">Le **volet** Disposition se trouve dans l’outil **Éléments** en plus des **volets Styles** **et** Calculés.</span><span class="sxs-lookup"><span data-stu-id="4f205-218">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panneau de disposition" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="4f205-220">Panneau de disposition</span><span class="sxs-lookup"><span data-stu-id="4f205-220">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

<span data-ttu-id="4f205-221">Vous pouvez maintenant ouvrir d’autres outils à l’aide de la nouvelle icône **Plus d’outils** `+` \( \).</span><span class="sxs-lookup"><span data-stu-id="4f205-221">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="4f205-222">Une fois que vous avez turn on the experiment and reload DevTools, un signe plus \( \) s’affiche à droite du groupe d’onglets en haut de **Enable + button tab menus to open more tools** `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-222">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="4f205-223">Pour afficher la liste des autres outils que vous pouvez ajouter à la barre d’onglets, choisissez la nouvelle icône Outils plus **\(** `+` \).</span><span class="sxs-lookup"><span data-stu-id="4f205-223">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Autres outils dans le volet supérieur" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="4f205-225">**Autres outils** dans le volet supérieur</span><span class="sxs-lookup"><span data-stu-id="4f205-225">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

<span data-ttu-id="4f205-226">Cette expérience remplace **l’outil Nouveautés** par le nouvel outil **Welcome.**</span><span class="sxs-lookup"><span data-stu-id="4f205-226">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="4f205-227">Il affiche une conception actualisée pour le contenu suivant.</span><span class="sxs-lookup"><span data-stu-id="4f205-227">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="4f205-228">Liens vers des documents de développement</span><span class="sxs-lookup"><span data-stu-id="4f205-228">Links to developer docs</span></span>  
*   <span data-ttu-id="4f205-229">fonctionnalités les plus récentes</span><span class="sxs-lookup"><span data-stu-id="4f205-229">the latest features</span></span>  
*   <span data-ttu-id="4f205-230">notes de publication</span><span class="sxs-lookup"><span data-stu-id="4f205-230">release notes</span></span>  
*   <span data-ttu-id="4f205-231">Option pour contacter l’Microsoft Edge devTools</span><span class="sxs-lookup"><span data-stu-id="4f205-231">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="4f205-232">**L’outil** Welcome s’ouvre automatiquement après chaque mise à jour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4f205-232">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="4f205-233">Pour empêcher l’affichage de l’outil **d’accueil** \*\*\*\* après chaque mise à jour, cochez la case en regard de l’onglet Ouvrir après chaque mise à jour sous le titre de **l’outil** d’accueil.</span><span class="sxs-lookup"><span data-stu-id="4f205-233">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="4f205-234">Si vous préférez **l’outil Nouveautés d’origine,** accédez [à Paramètres][DevtoolsCustomizeIndexSettings]Expériences et supprimez la case à cocher en  >  \*\*\*\* regard **Enable Welcome tab** de .</span><span class="sxs-lookup"><span data-stu-id="4f205-234">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Outil d’accueil" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="4f205-236">**Outil d’accueil**</span><span class="sxs-lookup"><span data-stu-id="4f205-236">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="4f205-237">Fonctionnalités expérimentales précédentes</span><span class="sxs-lookup"><span data-stu-id="4f205-237">Previous experimental features</span></span>  

*   <span data-ttu-id="4f205-238">[3D View][Devtools3dViewIndex]est désormais disponible et est allumé par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f205-238">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="4f205-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex]est désormais disponible et est allumé par défaut dans Microsoft Edge version 85 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f205-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="4f205-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]est désormais disponible et est allumé par défaut dans Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f205-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="4f205-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]est désormais disponible et est allumé par défaut dans Microsoft Edge version 89 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f205-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="4f205-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid]est désormais disponible et est allumé par défaut dans Microsoft Edge version 89 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f205-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="4f205-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables]est désormais disponible et est allumé par défaut dans Microsoft Edge version 90 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f205-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="4f205-244">Commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="4f205-244">Providing feedback on experimental features</span></span>  

<span data-ttu-id="4f205-245">Pour fournir des commentaires sur Microsoft Edge expériences DevTools ou sur tout autre sujet lié à DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f205-245">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="4f205-246">Envoyez vos commentaires à l’aide **de l’icône** Envoyer des commentaires dans DevTools</span><span class="sxs-lookup"><span data-stu-id="4f205-246">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="4f205-247">Tweet à [l'@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="4f205-247">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="L’Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="4f205-249">L’Icône **Envoyer des commentaires** dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4f205-249">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "3D View | Documents Microsoft"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Personnalisez Microsoft Edge devTools | Documents Microsoft"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Paramètres - Personnaliser Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edit keyboard shortcuts for any action in the DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code | Documents Microsoft"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Émuler les appareils à double écran et pliables dans Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode Microsoft Edge devTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpenIndex]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge Raccourcis clavier DevTools | Documents Microsoft"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
