---
description: Nouveaux outils de débogage de grille CSS, outil webauthn, outils mobiles et volet barre latérale calculée.
title: Nouveautés de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b972468ad21f3a64985a00aecbe29836032b3334
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190004"
---
# <span data-ttu-id="3c41e-104">Nouveautés de DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="3c41e-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="3c41e-105">Amélioration de la localisation DevTools</span><span class="sxs-lookup"><span data-stu-id="3c41e-105">Improving DevTools localization</span></span>  

<span data-ttu-id="3c41e-106">Pour répondre à vos besoins en matière de traduction, l’équipe Microsoft Edge DevTools est axée sur l’amélioration de la qualité de la traduction.</span><span class="sxs-lookup"><span data-stu-id="3c41e-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="3c41e-107">À partir de la version 87 de Microsoft Edge, plusieurs chaînes et termes sont verrouillés et ne changent pas même lorsque le reste du DevTools est affiché dans d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="3c41e-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="3c41e-108">La liste des chaînes et termes concernés est la suivante.</span><span class="sxs-lookup"><span data-stu-id="3c41e-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="3c41e-109">Les chaînes dans l’outil **phare** .</span><span class="sxs-lookup"><span data-stu-id="3c41e-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="3c41e-110">Le terme `service worker` .</span><span class="sxs-lookup"><span data-stu-id="3c41e-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="3c41e-111">Certains filtres d’outils **réseau** tels que `URL` ,, `XHR` `JS` et `CSS` .</span><span class="sxs-lookup"><span data-stu-id="3c41e-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="3c41e-112">API de la console [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .</span><span class="sxs-lookup"><span data-stu-id="3c41e-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="3c41e-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] est désormais disponible dans la [console](/microsoft-edge/devtools-guide-chromium/console/index.md) pour les utilisateurs des versions localisées du devtools.</span><span class="sxs-lookup"><span data-stu-id="3c41e-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="3c41e-114">Nous vous remercions de la communauté globale des développeurs pour vous aider à améliorer la localisation de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c41e-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="3c41e-115">Continuez à [Envoyer des commentaires sur la qualité](#getting-in-touch-with-microsoft-edge-devtools-team) de la localisation pour améliorer la prise en charge de devtools dans tous les pays.</span><span class="sxs-lookup"><span data-stu-id="3c41e-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="3c41e-116">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1136655][CR1136655]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Outil réseau avec filtres non localisés" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="3c41e-118">Volet **réseau** avec des filtres non localisés</span><span class="sxs-lookup"><span data-stu-id="3c41e-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <span data-ttu-id="3c41e-119">Déplacer des outils entre les volets supérieur et inférieur</span><span class="sxs-lookup"><span data-stu-id="3c41e-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="3c41e-120">DevTools prend désormais en charge le déplacement d’outils entre les volets supérieur et inférieur.</span><span class="sxs-lookup"><span data-stu-id="3c41e-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="3c41e-121">Personnalisez votre DevTools et améliorez votre productivité en affichant n’importe quelle combinaison de deux outils en même temps.</span><span class="sxs-lookup"><span data-stu-id="3c41e-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="3c41e-122">Par exemple, vous pouvez afficher les **éléments** et les outils **sources** en même temps (en déplaçant l’outil **sources** vers le bas).</span><span class="sxs-lookup"><span data-stu-id="3c41e-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="3c41e-123">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à [#1075732][CR1075732]problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3c41e-124">Pour déplacer un outil du haut vers le bas, pointez sur un onglet, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le bas**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Déplacer vers le bas" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="3c41e-126">Déplacer vers le bas</span><span class="sxs-lookup"><span data-stu-id="3c41e-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="3c41e-127">Pour déplacer n’importe quel outil inférieur vers le haut, pointez sur un onglet, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le haut**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Déplacer vers le haut" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="3c41e-129">Déplacer vers le haut</span><span class="sxs-lookup"><span data-stu-id="3c41e-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="3c41e-130">Enregistrer et exporter à l’aide de la console réseau</span><span class="sxs-lookup"><span data-stu-id="3c41e-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="3c41e-132">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="3c41e-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3c41e-133">L’outil de la **console réseau** dispose désormais d’une compatibilité améliorée avec les schémas [post-v 2.1][PostmanSchemaJsonCollectionv210Index] et [openapi v2][SwaggerSpecificationV2] .</span><span class="sxs-lookup"><span data-stu-id="3c41e-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="3c41e-134">Pour activer l’expérience, naviguez jusqu’à [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis cochez la case en regard de **activer la console réseau**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="3c41e-135">Pour plus d’informations sur la **console réseau**, voir [activer la fonctionnalité expérimentive Network console][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="3c41e-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="3c41e-136">Cette expérience prend désormais en charge les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c41e-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="3c41e-137">Enregistrer et exporter des collections et des environnements;</span><span class="sxs-lookup"><span data-stu-id="3c41e-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="3c41e-138">Edit et export d’ensembles de variables d’environnement dans l’outil **Network console** .</span><span class="sxs-lookup"><span data-stu-id="3c41e-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="3c41e-139">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1093687][CR1093687]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Entrez le nom du nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="3c41e-141">Entrez le nom du nouvel environnement</span><span class="sxs-lookup"><span data-stu-id="3c41e-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Choisir la mise en forme pour le nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="3c41e-143">Choisir la mise en forme pour le nouvel environnement</span><span class="sxs-lookup"><span data-stu-id="3c41e-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="3c41e-144">Outils de grille CSS améliorés</span><span class="sxs-lookup"><span data-stu-id="3c41e-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="3c41e-146">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="3c41e-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3c41e-147">Microsoft Edge DevTools prend désormais en charge les fonctionnalités suivantes pour inspecter, afficher et déboguer vos grilles CSS.</span><span class="sxs-lookup"><span data-stu-id="3c41e-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="3c41e-148">Affichez une superposition de grille simplifiée à l’aide de l’outil **Inspect** ou obtenez des informations plus détaillées avec des superpositions persistantes.</span><span class="sxs-lookup"><span data-stu-id="3c41e-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="3c41e-149">Pour activer les superpositions de grille persistante, sélectionnez l’icône de grille en regard d’un élément de conteneur de grille dans l’outil **éléments** ou sélectionnez la grille dans l’outil de **disposition** .</span><span class="sxs-lookup"><span data-stu-id="3c41e-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="3c41e-150">Vous pouvez activer les superpositions persistantes pour plusieurs grilles.</span><span class="sxs-lookup"><span data-stu-id="3c41e-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="3c41e-151">Le nouvel outil **mise en page** vous permet d’activer ou de désactiver facilement les superpositions de grille et de configurer son apparence et son contenu.</span><span class="sxs-lookup"><span data-stu-id="3c41e-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="3c41e-152">Les fonctionnalités sont activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="3c41e-152">The features are turned on by default.</span></span>  <span data-ttu-id="3c41e-153">Pour plus d’informations sur les fonctionnalités, accédez à [grilles CSS][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="3c41e-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="3c41e-154">Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à [#1047356][CR1047356]problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="3c41e-155">Par ailleurs, l’équipe Microsoft Edge DevTools collabore avec la communauté de l’équipe chrome DevTools et la communauté de chrome pour ajouter de nouvelles fonctionnalités d’outils Flexbox à DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c41e-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="3c41e-156">Pour les mises à jour apportées à l’outil Flexbox dans le projet open-source de chrome, accédez à [#1136394][CR1136394]problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Outil disposition avec des grilles" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="3c41e-158">Outil **disposition** avec des grilles</span><span class="sxs-lookup"><span data-stu-id="3c41e-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <span data-ttu-id="3c41e-159">Personnaliser les raccourcis clavier dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="3c41e-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="3c41e-161">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="3c41e-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3c41e-162">Vous pouvez désormais personnaliser le raccourci clavier pour n’importe quelle action dans le DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c41e-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="3c41e-163">Depuis la version 84 de Microsoft Edge, vous pouvez choisir entre les prédéfinis de **code Visual Studio** et **devtools (par défaut)** pour les [raccourcis clavier][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="3c41e-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="3c41e-164">À partir de la version 87 de Microsoft Edge, vous pouvez activer l’expérience d’activation de l' **éditeur de raccourcis** clavier pour personnaliser davantage les [raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="3c41e-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="3c41e-165">Pour activer l’expérience, naviguez jusqu’à [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis activez la case à cocher en regard de **activer l’éditeur de raccourcis clavier**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="3c41e-166">Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à [activer la fonctionnalité expérience de l’éditeur de raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="3c41e-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="3c41e-167">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#174309][CR174309]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Raccourci personnalisé pour suspendre un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="3c41e-169">Raccourci personnalisé pour suspendre un script</span><span class="sxs-lookup"><span data-stu-id="3c41e-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <span data-ttu-id="3c41e-170">Présentation de l’extension de code Microsoft Edge Tools pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c41e-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="3c41e-171">Les éléments du code et du réseau **Visual Studio** pour les extensions **de code Visual Studio** sont désormais fusionnés dans le nouvel [outil de développement Microsoft Edge pour l’extension de code Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .</span><span class="sxs-lookup"><span data-stu-id="3c41e-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="3c41e-172">Utilisez Microsoft Edge DevTools pour les activités suivantes sans quitter le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3c41e-172">Use the Microsoft Edge DevTools for the following activities without leaving Visual Studio Code.</span></span>  

*   <span data-ttu-id="3c41e-173">Déboguer le DOM</span><span class="sxs-lookup"><span data-stu-id="3c41e-173">Debug the DOM</span></span>  
*   <span data-ttu-id="3c41e-174">Modifier CSS</span><span class="sxs-lookup"><span data-stu-id="3c41e-174">Edit CSS</span></span>  
*   <span data-ttu-id="3c41e-175">Inspecter le trafic réseau</span><span class="sxs-lookup"><span data-stu-id="3c41e-175">Inspect network traffic</span></span>  

<span data-ttu-id="3c41e-176">Avec l’extension, lancez Microsoft Edge, connectez-vous à une instance existante du navigateur, ou utilisez un navigateur headless directement de votre éditeur.</span><span class="sxs-lookup"><span data-stu-id="3c41e-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="3c41e-177">Pour vous familiariser avec les commentaires concernant cette extension, accédez au [Microsoft Edge développeurs Tools pour Visual Studio code][GithubMicrosoftVscodeEdgeDevtools] référentiel Samples sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="3c41e-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Utilisation de l’extension dans la capture d’écran du mode navigateur complet" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="3c41e-179">Utilisation de l’extension dans la capture d’écran du mode navigateur complet</span><span class="sxs-lookup"><span data-stu-id="3c41e-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Utilisation de l’extension dans la capture d’écran du mode headless" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="3c41e-181">Utilisation de l’extension dans la capture d’écran du mode headless</span><span class="sxs-lookup"><span data-stu-id="3c41e-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="3c41e-182">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="3c41e-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="3c41e-183">Nouvel outil webauthn</span><span class="sxs-lookup"><span data-stu-id="3c41e-183">New WebAuthn tool</span></span>  

<span data-ttu-id="3c41e-184">Dans les versions antérieures de Microsoft Edge, il n’y a pas de prise en charge du débogage de webauthn natif.</span><span class="sxs-lookup"><span data-stu-id="3c41e-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="3c41e-185">Vous avez besoin d’authentificateurs physiques pour tester votre application Web à l’aide de l' [API d’authentification Web][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="3c41e-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="3c41e-186">Grâce au nouvel outil **Webauthn** , vous pouvez effectuer les actions suivantes sans utiliser d’authentificateurs physiques.</span><span class="sxs-lookup"><span data-stu-id="3c41e-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="3c41e-187">Émuler des authentificateurs</span><span class="sxs-lookup"><span data-stu-id="3c41e-187">Emulate authenticators</span></span>
*   <span data-ttu-id="3c41e-188">Personnaliser les attributs des authentificateurs</span><span class="sxs-lookup"><span data-stu-id="3c41e-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="3c41e-189">Inspecter les États des authentificateurs</span><span class="sxs-lookup"><span data-stu-id="3c41e-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="3c41e-190">Pour plus d’informations sur la fonctionnalité **Webauthn** , accédez à [émuler les authentificateurs et déboguer webauthn dans Microsoft Edge devtools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="3c41e-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="3c41e-191">Vous pouvez émuler les authentificateurs et déboguer l' [API d’authentification Web][GithubW3cWebauthn] avec le nouvel outil [webauthn][DevtoolsWebauthnIndex] .</span><span class="sxs-lookup"><span data-stu-id="3c41e-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="3c41e-192">Pour ouvrir l’outil **webauthn** , sélectionnez **l’icône personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **webauth**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="3c41e-193">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1034663][CR1034663]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Ouvrir l’outil webauthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="3c41e-195">Ouvrir l’outil **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="3c41e-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Outil webauthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="3c41e-197">Outil **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="3c41e-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="3c41e-198">Mises à jour de l’outil d’éléments</span><span class="sxs-lookup"><span data-stu-id="3c41e-198">Elements tool updates</span></span>  

#### <span data-ttu-id="3c41e-199">Afficher le volet de barre latérale calculé dans le volet styles</span><span class="sxs-lookup"><span data-stu-id="3c41e-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="3c41e-200">Activer/désactiver le volet **calculé** dans le volet **styles**</span><span class="sxs-lookup"><span data-stu-id="3c41e-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="3c41e-201">Le volet **calculé** dans le volet **styles** est réduit par défaut.</span><span class="sxs-lookup"><span data-stu-id="3c41e-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="3c41e-202">Pour le faire basculer, cliquez sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="3c41e-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="3c41e-203">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1073899][CR1073899]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Ouvrir le volet de barre latérale calculée" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="3c41e-205">Ouvrir le volet de **barre latérale calculée**</span><span class="sxs-lookup"><span data-stu-id="3c41e-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Volet barre latérale calculée" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="3c41e-207">Volet **barre latérale calculée**</span><span class="sxs-lookup"><span data-stu-id="3c41e-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="3c41e-208">Regroupement des propriétés CSS dans le panneau calculé</span><span class="sxs-lookup"><span data-stu-id="3c41e-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="3c41e-209">Pour afficher une feuille de style CSS appliquée moins de défilement, regrouper les propriétés CSS par catégories dans le volet **calculé** .</span><span class="sxs-lookup"><span data-stu-id="3c41e-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="3c41e-210">Vous pouvez également vous concentrer sur un ensemble de propriétés associées lorsque vous examinez votre CSS.</span><span class="sxs-lookup"><span data-stu-id="3c41e-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="3c41e-211">Dans l’outil **éléments** , sélectionnez un élément.</span><span class="sxs-lookup"><span data-stu-id="3c41e-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="3c41e-212">Pour regrouper \ (ou dissocier \) les propriétés CSS, activez la case à cocher du **groupe** .</span><span class="sxs-lookup"><span data-stu-id="3c41e-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="3c41e-213">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [#1096230][CR1096230], [#1084673][CR1084673]et [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="3c41e-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Regroupement des propriétés CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="3c41e-215">Regroupement des propriétés CSS</span><span class="sxs-lookup"><span data-stu-id="3c41e-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <span data-ttu-id="3c41e-216">Phare 6,4 dans l’outil phare</span><span class="sxs-lookup"><span data-stu-id="3c41e-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="3c41e-217">L’outil **phare** s’exécute maintenant sur le phare 6,4.</span><span class="sxs-lookup"><span data-stu-id="3c41e-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="3c41e-218">Pour obtenir la liste complète des modifications, accédez aux [notes de publication de phare][GithubGoogleChromeLighthouseReleasesV641].</span><span class="sxs-lookup"><span data-stu-id="3c41e-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="3c41e-219">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#772558][CR772558]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <span data-ttu-id="3c41e-220">performance. Mark () événements dans la section minutage</span><span class="sxs-lookup"><span data-stu-id="3c41e-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="3c41e-221">La **section minutage** d’un enregistrement dans l’outil de [performance][DevtoolsGuideChromiumEvaluatePerformanceReference] marque désormais des `performance.mark()` événements.</span><span class="sxs-lookup"><span data-stu-id="3c41e-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="3c41e-222">Pour utiliser cette fonctionnalité et mesurer les performances de votre code JavaScript, ajoutez des `performance.mark()` événements à votre code.</span><span class="sxs-lookup"><span data-stu-id="3c41e-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="3c41e-223">Par exemple, l’extrait de code suivant ajoute des marqueurs avant et après une `for` boucle qui itère de 0 à 1000 à l’aide d’incréments de 7.</span><span class="sxs-lookup"><span data-stu-id="3c41e-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="3c41e-224">Ensuite, ouvrez l’outil [performance][DevtoolsGuideChromiumEvaluatePerformanceReference] et naviguez jusqu’à la **section minutage** pour enregistrer votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3c41e-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="3c41e-225">Les `performance.mark()` événements que vous avez ajoutés apparaissent désormais dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3c41e-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Performance. marquer des événements" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="3c41e-227">venu</span><span class="sxs-lookup"><span data-stu-id="3c41e-227">events</span></span>  
:::image-end:::  

### <span data-ttu-id="3c41e-228">Nouveaux filtres d’URL et de types de ressources dans l’outil réseau</span><span class="sxs-lookup"><span data-stu-id="3c41e-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="3c41e-229">Utilisez les nouveaux `resource-type` et `url` Mots clés de l’outil **réseau** pour filtrer les requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="3c41e-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="3c41e-230">Par exemple, utilisez `resource-type:image` pour vous concentrer sur les requêtes réseau qui sont des images.</span><span class="sxs-lookup"><span data-stu-id="3c41e-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtre de type de ressource" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="3c41e-232">filtre de type de ressource</span><span class="sxs-lookup"><span data-stu-id="3c41e-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="3c41e-233">Pour en savoir plus sur les mots-clés spéciaux, tels que `resource-type` et `url` , accédez aux [demandes de filtre par propriétés][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="3c41e-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="3c41e-234">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [#1121141][CR1121141] et [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="3c41e-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <span data-ttu-id="3c41e-235">Mises à jour de l’affichage des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="3c41e-235">Frame details view updates</span></span>  

#### <span data-ttu-id="3c41e-236">Afficher les COEP et COOP la création de rapports au point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3c41e-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="3c41e-237">Affichez le point de terminaison de la stratégie d’intégrateur à l’origine \ (COEP \) et de la stratégie d’ouverture de la stratégie d’ouverture de la stratégie d’ouverture de fichiers \ (COOP \) `reporting to` dans la section **isolement du & de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="3c41e-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="3c41e-238">L' [API de création de rapports][MdnReportingApi] définit `Report-To` un nouvel en-tête http, qui vous permet de spécifier les points de terminaison du serveur pour le navigateur et d’envoyer des avertissements et des erreurs.</span><span class="sxs-lookup"><span data-stu-id="3c41e-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="3c41e-239">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1051466][CR1051466]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Rapport au point de terminaison" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="3c41e-241">Le `reporting to` point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3c41e-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <span data-ttu-id="3c41e-242">Afficher le mode de rapport COEP et COOP</span><span class="sxs-lookup"><span data-stu-id="3c41e-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="3c41e-243">DevTools affiche maintenant l' `report-only` étiquette pour COEP et Coop définies sur `report-only` mode.</span><span class="sxs-lookup"><span data-stu-id="3c41e-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="3c41e-244">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1051466][CR1051466]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Étiquette du mode rapport uniquement" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="3c41e-246">`report-only`Étiquette mode</span><span class="sxs-lookup"><span data-stu-id="3c41e-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <span data-ttu-id="3c41e-247">Afficher et résoudre les problèmes de contraste des couleurs dans l’outil vue d’ensemble CSS</span><span class="sxs-lookup"><span data-stu-id="3c41e-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="3c41e-249">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="3c41e-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3c41e-250">L’outil de **vue d’ensemble CSS** affiche désormais une liste des éléments de votre page qui présentent des problèmes de contraste des couleurs.</span><span class="sxs-lookup"><span data-stu-id="3c41e-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="3c41e-251">La page de démonstration suivante présente un exemple de problème de contraste de couleur.</span><span class="sxs-lookup"><span data-stu-id="3c41e-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="3c41e-252">Présentation CSS-vue d’ensemble des couleurs accessibles</span><span class="sxs-lookup"><span data-stu-id="3c41e-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="3c41e-253">Pour activer cette expérience, sous **Settings**  >  **expériences**de configuration, sélectionnez la case à cocher **vue d’ensemble CSS** .</span><span class="sxs-lookup"><span data-stu-id="3c41e-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="3c41e-254">Pour afficher une liste des éléments présentant un problème de contraste de couleurs, dans la liste **problèmes de contraste**, sélectionnez **texte**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="3c41e-255">Pour ouvrir l’élément dans l’outil **éléments** , sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="3c41e-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="3c41e-256">Pour vous aider à résoudre les problèmes de contraste, le Microsoft Edge DevTools [fournit automatiquement des suggestions de couleurs][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span><span class="sxs-lookup"><span data-stu-id="3c41e-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="3c41e-257">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1120316][CR1120316]du problème.</span><span class="sxs-lookup"><span data-stu-id="3c41e-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problèmes de contraste de faible couleur" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="3c41e-259">Problèmes de contraste de faible couleur</span><span class="sxs-lookup"><span data-stu-id="3c41e-259">Low color contrast issues</span></span>  
:::image-end:::  

## <span data-ttu-id="3c41e-260">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="3c41e-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="3c41e-261">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3c41e-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="3c41e-262">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c41e-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="3c41e-263">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3c41e-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Désapprobation du volet Propriétés dans l’outil éléments-nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS-nouveautés dans DevTools (Microsoft Edge 85) | Documents Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Suggestions de couleurs accessibles dans le volet styles-nouveautés de DevTools (Microsoft Edge 86) | Documents Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Éléments récemment sélectionnés ou JavaScript objet-référence des API des utilitaires de la console | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Référence d’analyse des performances | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Activer les API expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Activer l’éditeur de raccourcis clavier-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Activer la console réseau-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Activer la visionneuse de commandes sources-fonctionnalités expérimentales | Documents Microsoft"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Tests sur les périphériques pliants et à deux écrans-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "référence sur les API table-console | Documents Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspecter la grille CSS | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu-référence d’analyse des performances | Documents Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Afficher et déboguer les informations sur les lecteurs multimédias | Documents Microsoft"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Demandes de filtre par propriétés-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux Microsoft Edge preview"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools pour le code Visual Studio | Code Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR174309]: https://crbug.com/174309 "DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"
[CR772558]: https://crbug.com/772558 "DevTools: mise à jour vers la dernière version de phare | Bugs du chrome"  
[CR1034663]: https://crbug.com/1034663 "Créer un frontal pour l’API de tests webauthn | Bugs du chrome"  
[CR1047356]: https://crbug.com/1047356 "Outils CSS Grid/Flexbox/tableau | Bugs du chrome"  
[CR1051466]: https://crbug.com/1051466 "Prendre en charge le débogage COOP/COEP dans DevTools | Bugs du chrome"  
[CR1073899]: https://crbug.com/1073899 "L’onglet style calculé disparaît en mode réactif | Bugs du chrome"  
[CR1075732]: https://crbug.com/1075732 "Personnalisation de DevTools-onglets mobiles | Bugs du chrome"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Améliorez la présentation des propriétés personnalisées CSS ((c’est-à-dire). Variables CSS) et leurs valeurs | Bugs du chrome"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil permettant de créer et de relire des demandes de réseau synthétique Bugs du chrome"  
[CR1096230]: https://crbug.com/1096230 "Grouper les propriétés CSS par catégories dans le volet styles calculés | Bugs du chrome"  
[CR1104188]: https://crbug.com/1104188 "La recherche d’outils réseau ne trouve aucun résultat lors de la recherche d’URL complète | Bugs du chrome"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: onglet améliorer les styles calculés | Bugs du chrome"  
[CR1120316]: https://crbug.com/1120316 "Mettez en surbrillance le contraste de votre application dans la vue d’ensemble CSS > couleurs | Bugs du chrome"  
[CR1121141]: https://crbug.com/1121141 "Autoriser le filtrage par type de ressource dans le journal réseau | Bugs du chrome"  
[CR1121312]: https://crbug.com/1121312 "Les paramètres doivent être supprimés du menu autres outils | Bugs du chrome"  
[CR1136394]: https://crbug.com/1136394 "Outils Flexbox | Bugs du chrome"  
[CR1136655]: https://crbug.com/1136655 "DevTools: localisation v2 | Bugs du chrome"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API de création de rapports | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/phare | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Authentification Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Bonjour! | Problème"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Mise en forme de collection 2.1.0 v Poste"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Spécification OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="3c41e-316">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3c41e-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3c41e-317">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/10/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="3c41e-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="3c41e-319">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3c41e-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  