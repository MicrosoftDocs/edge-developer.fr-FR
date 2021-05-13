---
description: Nouveaux outils de débogage grille CSS, outil Webauthn, outils moveables et panneau de barre latérale calculé.
title: Nouveautés de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c7859631327fc031909cd25736fddb8cff3cff45
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564895"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-87"></a><span data-ttu-id="2a778-104">Nouveautés de DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="2a778-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a><span data-ttu-id="2a778-105">Amélioration de la localisation de DevTools</span><span class="sxs-lookup"><span data-stu-id="2a778-105">Improving DevTools localization</span></span>  

<span data-ttu-id="2a778-106">Pour répondre à vos besoins en traduction, l Microsoft Edge’équipe DevTools se concentre sur l’amélioration de la qualité de la traduction.</span><span class="sxs-lookup"><span data-stu-id="2a778-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="2a778-107">À partir Microsoft Edge version 87, plusieurs chaînes et termes sont verrouillés et ne changent pas même lorsque le reste des DevTools sont affichés dans d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="2a778-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="2a778-108">La liste des chaînes et des termes affectés est la suivante.</span><span class="sxs-lookup"><span data-stu-id="2a778-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="2a778-109">Les chaînes de **l’outil Dente.**</span><span class="sxs-lookup"><span data-stu-id="2a778-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="2a778-110">Le terme `service worker` .</span><span class="sxs-lookup"><span data-stu-id="2a778-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="2a778-111">Certains filtres **de l’outil** réseau tels `URL` que , et `XHR` `JS` `CSS` .</span><span class="sxs-lookup"><span data-stu-id="2a778-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="2a778-112">API des utilitaires de console [$0.][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]</span><span class="sxs-lookup"><span data-stu-id="2a778-112">The [$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="2a778-113">[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] est désormais disponible dans la [console pour][DevtoolsConsoleIndex] les utilisateurs sur les versions localisées de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a778-113">[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] is now available in the [Console][DevtoolsConsoleIndex] for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="2a778-114">Merci à la communauté internationale de développeurs d’aider à améliorer la localisation du Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a778-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="2a778-115">Continuez à [envoyer des commentaires sur la qualité de](#getting-in-touch-with-microsoft-edge-devtools-team) localisation pour améliorer la prise en charge de DevTools dans tous les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="2a778-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="2a778-116">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="2a778-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  


:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Outil réseau avec filtres non localisées" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="2a778-118">**Volet** réseau avec filtres non localisées</span><span class="sxs-lookup"><span data-stu-id="2a778-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a><span data-ttu-id="2a778-119">Déplacer des outils entre les panneaux supérieur et inférieur</span><span class="sxs-lookup"><span data-stu-id="2a778-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="2a778-120">DevTools prend désormais en charge le déplacement d’outils entre les panneaux supérieur et inférieur.</span><span class="sxs-lookup"><span data-stu-id="2a778-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="2a778-121">Personnalisez vos DevTools et améliorez votre productivité en combinant deux outils en même temps.</span><span class="sxs-lookup"><span data-stu-id="2a778-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="2a778-122">Par exemple, affichez les outils **Éléments** et **Sources** en même temps \(en déplaçant l’outil **Sources** vers le bas\).</span><span class="sxs-lookup"><span data-stu-id="2a778-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="2a778-123">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="2a778-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2a778-124">Pour déplacer n’importe quel outil supérieur vers le bas, pointez sur un onglet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Déplacer vers le bas.**</span><span class="sxs-lookup"><span data-stu-id="2a778-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Déplacer vers le bas" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="2a778-126">Déplacer vers le bas</span><span class="sxs-lookup"><span data-stu-id="2a778-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2a778-127">Pour déplacer n’importe quel outil inférieur vers le haut, pointez sur un onglet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Déplacer vers le haut.**</span><span class="sxs-lookup"><span data-stu-id="2a778-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Se déplacer vers le haut" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="2a778-129">Se déplacer vers le haut</span><span class="sxs-lookup"><span data-stu-id="2a778-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a><span data-ttu-id="2a778-130">Enregistrer et exporter à l’aide de la console réseau</span><span class="sxs-lookup"><span data-stu-id="2a778-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="2a778-132">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="2a778-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="2a778-133">**L’outil Console** réseau a désormais une meilleure compatibilité avec les schémas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] et [OpenAPI v2.][SwaggerSpecificationV2]</span><span class="sxs-lookup"><span data-stu-id="2a778-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="2a778-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span><span class="sxs-lookup"><span data-stu-id="2a778-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="2a778-135">Pour plus d’informations sur la **console**réseau, accédez à [Activer la fonctionnalité Expérimentation de console réseau][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="2a778-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="2a778-136">Cette expérience prend désormais en charge les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2a778-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="2a778-137">Enregistrer et exporter des collections et des environnements.</span><span class="sxs-lookup"><span data-stu-id="2a778-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="2a778-138">Modifier et exporter des ensembles de variables d’environnement dans **l’outil Console** réseau.</span><span class="sxs-lookup"><span data-stu-id="2a778-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="2a778-139">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="2a778-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Entrez le nom du nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="2a778-141">Entrez le nom du nouvel environnement</span><span class="sxs-lookup"><span data-stu-id="2a778-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Choisir le format du nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="2a778-143">Choisir le format du nouvel environnement</span><span class="sxs-lookup"><span data-stu-id="2a778-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a><span data-ttu-id="2a778-144">Outils de grille CSS améliorés</span><span class="sxs-lookup"><span data-stu-id="2a778-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="2a778-146">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="2a778-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="2a778-147">Le Microsoft Edge DevTools permet désormais d’inspecter, d’afficher et de déboguer vos grilles CSS.</span><span class="sxs-lookup"><span data-stu-id="2a778-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="2a778-148">Affichez une superposition de grille simplifiée à l’aide de l’outil **Inspect** ou obtenez des informations plus détaillées avec des superpositions persistantes.</span><span class="sxs-lookup"><span data-stu-id="2a778-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="2a778-149">Pour activer les superpositions de grille persistantes, choisissez l’icône de grille en face d’un élément conteneur de grille dans l’outil **Éléments** ou choisissez la grille dans l’outil **De** disposition.</span><span class="sxs-lookup"><span data-stu-id="2a778-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="2a778-150">Vous pouvez activer les superpositions persistantes pour plusieurs grilles.</span><span class="sxs-lookup"><span data-stu-id="2a778-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="2a778-151">Le nouvel **outil de** disposition vous permet de facilement faire basculer les superpositions de grilles et de configurer l’apparence et le contenu de chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="2a778-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="2a778-152">Les fonctionnalités sont désactivées par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a778-152">The features are turned on by default.</span></span>  <span data-ttu-id="2a778-153">Pour plus d’informations sur les fonctionnalités, accédez à [grilles CSS][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="2a778-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="2a778-154">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="2a778-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="2a778-155">En outre, l’équipe Microsoft Edge DevTools collabore avec l’équipe Chrome DevTools et la communauté Chromium pour ajouter de nouvelles fonctionnalités d’outils flexbox à DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a778-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="2a778-156">Pour les mises à jour sur les outils flexbox dans Chromium projet open source, accédez à [Problème #1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="2a778-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Outil de disposition avec grilles" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="2a778-158">**Outil de** disposition avec grilles</span><span class="sxs-lookup"><span data-stu-id="2a778-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="2a778-159">Personnaliser les raccourcis clavier dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="2a778-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="2a778-161">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="2a778-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="2a778-162">Vous pouvez désormais personnaliser le raccourci clavier pour toute action dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a778-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="2a778-163">Depuis Microsoft Edge version 84, vous pouvez choisir entre les présets **Visual Studio Code** et **DevTools (par défaut)** pour les [raccourcis clavier.][DevtoolsCustomizeShortcuts]</span><span class="sxs-lookup"><span data-stu-id="2a778-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="2a778-164">À partir Microsoft Edge version 87, vous pouvez \*\*\*\* activer l’expérience d’éditeur de raccourci clavier pour personnaliser davantage les [raccourcis clavier.][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]</span><span class="sxs-lookup"><span data-stu-id="2a778-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span></span>  

<span data-ttu-id="2a778-165">Pour activer l’expérience, accédez à [Activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] et cochez la case en regard de l’éditeur de raccourci clavier. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2a778-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="2a778-166">Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à Modifier les raccourcis clavier pour toute action dans [DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span><span class="sxs-lookup"><span data-stu-id="2a778-166">For more information about customizing and editing shortcuts, navigate to [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span></span>  <span data-ttu-id="2a778-167">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="2a778-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Raccourci personnalisé pour la suspension d’un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="2a778-169">Raccourci personnalisé pour la suspension d’un script</span><span class="sxs-lookup"><span data-stu-id="2a778-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a><span data-ttu-id="2a778-170">Présentation des outils Microsoft Edge pour Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="2a778-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="2a778-171">Les **éléments pour Visual Studio Code** et réseau pour les extensions **Visual Studio Code** sont désormais fusionnés dans la nouvelle extension Outils de développement Microsoft Edge pour [Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] de développement.</span><span class="sxs-lookup"><span data-stu-id="2a778-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="2a778-172">Utilisez la Microsoft Edge DevTools pour les activités suivantes sans quitter Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="2a778-172">Use the Microsoft Edge DevTools for the following activities without leaving Microsoft Visual Studio Code.</span></span>  

*   <span data-ttu-id="2a778-173">Déboguer le DOM</span><span class="sxs-lookup"><span data-stu-id="2a778-173">Debug the DOM</span></span>  
*   <span data-ttu-id="2a778-174">Modifier CSS</span><span class="sxs-lookup"><span data-stu-id="2a778-174">Edit CSS</span></span>  
*   <span data-ttu-id="2a778-175">Inspecter le trafic réseau</span><span class="sxs-lookup"><span data-stu-id="2a778-175">Inspect network traffic</span></span>  

<span data-ttu-id="2a778-176">Avec l’extension, lancez Microsoft Edge, connectez-vous à une instance existante du navigateur ou utilisez un navigateur sans en-tête directement à partir de votre éditeur.</span><span class="sxs-lookup"><span data-stu-id="2a778-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="2a778-177">Pour commencer à contribuer et classer les problèmes avec vos commentaires sur cette extension, accédez au dépôt des outils de développement [Microsoft Edge][GithubMicrosoftVscodeEdgeDevtools] pour Visual Studio Code sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="2a778-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Utilisation de l’extension en mode navigateur complet" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="2a778-179">Utilisation de l’extension en mode navigateur complet</span><span class="sxs-lookup"><span data-stu-id="2a778-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Utilisation de l’extension en mode sans en-tête" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="2a778-181">Utilisation de l’extension en mode sans en-tête</span><span class="sxs-lookup"><span data-stu-id="2a778-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="2a778-182">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="2a778-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a><span data-ttu-id="2a778-183">Nouvel outil WebAuthn</span><span class="sxs-lookup"><span data-stu-id="2a778-183">New WebAuthn tool</span></span>  

<span data-ttu-id="2a778-184">Dans les versions antérieures de Microsoft Edge, il n’y avait aucune prise en charge du débogage WebAuthn natif.</span><span class="sxs-lookup"><span data-stu-id="2a778-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="2a778-185">Vous avez besoin d’authentifiés physiques pour tester votre application web avec [l’API d’authentification web.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="2a778-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="2a778-186">Avec le nouvel **outil WebAuthn,** vous pouvez faire les actions suivantes sans utiliser d’authentifiés physiques.</span><span class="sxs-lookup"><span data-stu-id="2a778-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="2a778-187">Émuler des authentifiés</span><span class="sxs-lookup"><span data-stu-id="2a778-187">Emulate authenticators</span></span>
*   <span data-ttu-id="2a778-188">Personnaliser les attributs des authentifiés</span><span class="sxs-lookup"><span data-stu-id="2a778-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="2a778-189">Inspecter les états des authentifiés</span><span class="sxs-lookup"><span data-stu-id="2a778-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="2a778-190">Pour plus d’informations sur la fonctionnalité **WebAuthn,** accédez à [Émuler les authentateurs et déboguer WebAuthn dans Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="2a778-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="2a778-191">Vous pouvez émuler les authentifiés et déboguer [l’API][GithubW3cWebauthn] d’authentification web avec le nouvel outil [WebAuthn][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="2a778-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="2a778-192">Pour ouvrir **l’outil WebAuthn,** choisissez l’icône Personnaliser et contrôler **DevTools** \( \) > `...` **outils**  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="2a778-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="2a778-193">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="2a778-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Ouvrir l’outil WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="2a778-195">Ouvrir **l’outil WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="2a778-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Outil WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="2a778-197">**Outil WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="2a778-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="2a778-198">Mises à jour de l’outil Éléments</span><span class="sxs-lookup"><span data-stu-id="2a778-198">Elements tool updates</span></span>  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a><span data-ttu-id="2a778-199">Afficher le volet De la barre latérale calculé dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="2a778-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="2a778-200">Basculez le **volet Calculé** dans le volet **Styles.**</span><span class="sxs-lookup"><span data-stu-id="2a778-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="2a778-201">Le **volet Calculé** dans le volet **Styles** est réduire par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a778-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="2a778-202">Pour le faire bascule, sélectionnez le bouton.</span><span class="sxs-lookup"><span data-stu-id="2a778-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="2a778-203">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="2a778-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Ouvrir le volet De la barre latérale calculé" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="2a778-205">Ouvrir le **volet De la barre latérale** calculé</span><span class="sxs-lookup"><span data-stu-id="2a778-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Volet de barre latérale calculé" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="2a778-207">**Volet de barre latérale** calculé</span><span class="sxs-lookup"><span data-stu-id="2a778-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a><span data-ttu-id="2a778-208">Regroupement des propriétés CSS dans le panneau calculé</span><span class="sxs-lookup"><span data-stu-id="2a778-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="2a778-209">Pour afficher votre feuille CSS appliquée avec moins de défilement, groupez les propriétés CSS par catégories dans le **volet** calculé.</span><span class="sxs-lookup"><span data-stu-id="2a778-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="2a778-210">Vous pouvez également vous concentrer de manière sélective sur un ensemble de propriétés associées pendant que vous inspectez votre CSS.</span><span class="sxs-lookup"><span data-stu-id="2a778-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="2a778-211">Dans **l’outil Éléments,** choisissez un élément.</span><span class="sxs-lookup"><span data-stu-id="2a778-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="2a778-212">Pour regrouper \(ou ungrouper\) les propriétés CSS, basculez la case **à** cocher Groupe.</span><span class="sxs-lookup"><span data-stu-id="2a778-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="2a778-213">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [#1096230,][CR1096230] [#1084673][CR1084673]et [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="2a778-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Regroupement des propriétés CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="2a778-215">Regroupement des propriétés CSS</span><span class="sxs-lookup"><span data-stu-id="2a778-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a><span data-ttu-id="2a778-216">Île 6.4 dans l’outil Îles</span><span class="sxs-lookup"><span data-stu-id="2a778-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="2a778-217">**L’outil Îles** exécute à présent Ce dernier 6.4.</span><span class="sxs-lookup"><span data-stu-id="2a778-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="2a778-218">Pour obtenir la liste complète des modifications, accédez aux notes de [publication de Cerr.][GithubGoogleChromeLighthouseReleasesV641]</span><span class="sxs-lookup"><span data-stu-id="2a778-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="2a778-219">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="2a778-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <a name="performancemark-events-in-the-timings-section"></a><span data-ttu-id="2a778-220">événements performance.mark() dans la section Timings</span><span class="sxs-lookup"><span data-stu-id="2a778-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="2a778-221">La **section Minutages** d’un enregistrement dans l’outil [Performance][DevtoolsEvaluatePerformanceReference] marque désormais les `performance.mark()` événements.</span><span class="sxs-lookup"><span data-stu-id="2a778-221">The **Timings section** of a recording in the [Performance][DevtoolsEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="2a778-222">Pour essayer cette fonctionnalité et mesurer les performances de votre code JavaScript, ajoutez des `performance.mark()` événements à votre code.</span><span class="sxs-lookup"><span data-stu-id="2a778-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="2a778-223">Par exemple, l’extrait de code suivant ajoute des marqueurs avant et après une boucle qui itérera de 0 à `for` 1 000 à l’aide d’incréments de 7.</span><span class="sxs-lookup"><span data-stu-id="2a778-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="2a778-224">Ensuite, ouvrez [l’outil Performance][DevtoolsEvaluatePerformanceReference] et accédez à la **section Minutages** pour enregistrer votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2a778-224">Then, open the [Performance][DevtoolsEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="2a778-225">Les `performance.mark()` événements que vous avez ajoutés sont désormais affichés dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2a778-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Événements Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="2a778-227">événements</span><span class="sxs-lookup"><span data-stu-id="2a778-227">events</span></span>  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a><span data-ttu-id="2a778-228">Nouveaux filtres de type de ressource et d’URL dans l’outil Réseau</span><span class="sxs-lookup"><span data-stu-id="2a778-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="2a778-229">Utilisez les mots clés et `resource-type` les nouveaux mots clés dans `url` **l’outil** Réseau pour filtrer les demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="2a778-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="2a778-230">Par exemple, utilisez cette fonction `resource-type:image` pour vous concentrer sur les demandes réseau qui sont des images.</span><span class="sxs-lookup"><span data-stu-id="2a778-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtre de type ressource" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="2a778-232">filtre de type ressource</span><span class="sxs-lookup"><span data-stu-id="2a778-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="2a778-233">Pour découvrir des mots clés plus spéciaux tels que et , accédez à [filtrer les demandes par `resource-type` `url` propriétés][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="2a778-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="2a778-234">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à Problèmes #1121141 [et][CR1121141] [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="2a778-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <a name="frame-details-view-updates"></a><span data-ttu-id="2a778-235">Mises à jour de l’affichage des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="2a778-235">Frame details view updates</span></span>  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a><span data-ttu-id="2a778-236">Afficher les rapports COEP et REPORTING sur le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2a778-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="2a778-237">Affichez le point de terminaison De la stratégie d’incorporation d’origine croisée \(COEP\) et de la stratégie d’ouverture d’origine croisée \(PRINCIPAL\) sous la section Isolation & `reporting to` sécurité. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2a778-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="2a778-238">[L’API][MdnReportingApi] De rapports définit , un nouvel en-tête HTTP, qui vous permet de spécifier les points de terminaison du serveur pour le navigateur pour envoyer des `Report-To` avertissements et des erreurs.</span><span class="sxs-lookup"><span data-stu-id="2a778-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="2a778-239">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="2a778-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Rapport au point de terminaison" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="2a778-241">Point `reporting to` de terminaison</span><span class="sxs-lookup"><span data-stu-id="2a778-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a><span data-ttu-id="2a778-242">Affichage du mode de rapport COEP et BIP uniquement</span><span class="sxs-lookup"><span data-stu-id="2a778-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="2a778-243">DevTools affiche désormais l’étiquette pour COEP et `report-only` PRINCIPAL qui sont définies en `report-only` mode.</span><span class="sxs-lookup"><span data-stu-id="2a778-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="2a778-244">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="2a778-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Étiquette du mode rapport uniquement" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="2a778-246">Étiquette `report-only` du mode</span><span class="sxs-lookup"><span data-stu-id="2a778-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a><span data-ttu-id="2a778-247">Afficher et résoudre les problèmes de contraste de couleur dans l’outil Vue d’ensemble du CSS</span><span class="sxs-lookup"><span data-stu-id="2a778-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="2a778-249">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="2a778-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="2a778-250">**L’outil Vue d’ensemble CSS** affiche désormais une liste d’éléments sur votre page qui ont des problèmes de contraste de couleur.</span><span class="sxs-lookup"><span data-stu-id="2a778-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="2a778-251">La page de démonstration suivante présente un exemple de problème de contraste de couleur.</span><span class="sxs-lookup"><span data-stu-id="2a778-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="2a778-252">Démonstration des couleurs accessibles de vue d’ensemble du CSS</span><span class="sxs-lookup"><span data-stu-id="2a778-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="2a778-253">Pour activer cette expérience, sous **Paramètres**expériences, activez la case à cocher Vue d’ensemble  >  \*\*\*\* **du CSS.**</span><span class="sxs-lookup"><span data-stu-id="2a778-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="2a778-254">Pour afficher la liste des éléments qui ont un problème de contraste de couleur, sur **les problèmes de contraste,** choisissez **Texte**.</span><span class="sxs-lookup"><span data-stu-id="2a778-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="2a778-255">Pour ouvrir l’élément dans **l’outil Elements,** choisissez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="2a778-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="2a778-256">Pour résoudre les problèmes de contraste, les Microsoft Edge DevTools fournissent [automatiquement des suggestions de couleur.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]</span><span class="sxs-lookup"><span data-stu-id="2a778-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="2a778-257">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="2a778-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problèmes de contraste de couleur faible" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="2a778-259">Problèmes de contraste de couleur faible</span><span class="sxs-lookup"><span data-stu-id="2a778-259">Low color contrast issues</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="2a778-260">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2a778-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="2a778-261">Si vous êtes sur Windows ou macOS, envisagez d’utiliser les canaux d Microsoft Edge [d’aperçu][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a778-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2a778-262">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a778-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="2a778-263">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2a778-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsTool]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Annulation du volet Propriétés dans l’outil Éléments - Nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS - Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Suggestion de couleurs accessibles dans le volet Styles - Nouveautés de DevTools (Microsoft Edge 86) | Documents Microsoft"  

[DevtoolsConsoleIndex]: ../../../console/index.md "Utiliser la console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]:  ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Élément ou objet JavaScript récemment choisi - Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Modifier les raccourcis clavier pour toute action dans la | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReference]: ../../../evaluate-performance/reference.md "Référence de l’analyse des performances | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: ../../../experimental-features/index.md#emulation-support-dual-screen-mode "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features.md#enable-experimental-apis "Activer les API expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: .. /.. /.. /experimental-features/index.md#enable-new-css-grid-debugging-features «Emulation: Support dual screen mode - Experimental features | Microsoft Docs »  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: .. /.. /.. /experimental-features/index.md#enable-network-console «Enable Network Console - Experimental features | Microsoft Docs »  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#enable-source-order-viewer «Enable Source Order Viewer - Experimental features | Microsoft Docs» [DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: .. /.. /.. /experimental-features/index.md#testing-on-foldable-and-dual-screen-devices «Testing on foldable and dual-screen devices - Experimental features | Microsoft Docs »  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features " Turn on Experimental features - Experimental features | Microsoft Docs »  
[DevtoolsConsoleApiTable]: .. /.. /.. /console/api.md#table «table - Référence api console | Microsoft Docs »  
[DevtoolsCoverageIndex]: .. /.. /.. /coverage/index.md " Rechercher du code JavaScript et CSS inutilisé avec l’onglet Couverture dans Microsoft Edge devTools | Microsoft Docs »  
[DevtoolsCssGrid]: .. /.. /.. /css/grid.md " Inspect CSS Grid | Microsoft Docs »  
[DevtoolsCustomizeIndexDrawer]: .. /.. /.. /customize/index.md#drawer «Drawer - Customize Microsoft Edge DevTools | Microsoft Docs »  
[DevtoolsCustomizeIndexSettings]: .. /.. /.. /customize/index.md#settings «Paramètres - Customize Microsoft Edge DevTools | Microsoft Docs »  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: .. /.. /.. /evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tab " Analyser les performances de rendu avec l’onglet Rendu - Référence de l’analyse des performances | Microsoft Docs »  
[DevtoolsMediaIndex]: .. /.. /.. /media/index.md « Afficher et déboguer les informations des joueurs multimédias | Microsoft Docs »  
[DevtoolsNetworkReferenceFilterRequestsProperties]: .. /.. /.. /network/reference.md#filter-requests-by-properties «Filter requests by properties - Network Analysis reference | Microsoft Docs »  
[DevtoolsWebauthnIndex]: .. /.. /.. /webauthn/index.md « Émuler les authentateurs et déboguer WebAuthn dans Microsoft Edge devTools | Microsoft Docs »  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils pour Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Chromium bogues"
[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Chromium bogues"  
[CR1034663]: https://crbug.com/1034663 "Créer un serveur frontal pour l’API de test WebAuthn | Chromium bogues"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Chromium bogues"  
[CR1051466]: https://crbug.com/1051466 "Prise en charge du débogage PUNAISE/COEP dans DevTools | Chromium bogues"  
[CR1073899]: https://crbug.com/1073899 "L’onglet Style calculé disparaît en mode | Chromium bogues"  
[CR1075732]: https://crbug.com/1075732 "Personnalisation de DevTools : onglets amovibles | Chromium bogues"  
[CR1084673]: https://crbug.com/1084673 "DevTools : améliorer la façon dont nous présentons les propriétés personnalisées CSS (également appelées). Variables CSS) et leurs valeurs | Chromium bogues"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil pour créer et relire des demandes de réseau synthétique | Chromium bogues"  
[CR1096230]: https://crbug.com/1096230 "Group CSS properties by categories in Computed Styles pane | Chromium bogues"  
[CR1104188]: https://crbug.com/1104188 "La recherche de l’outil réseau ne trouve pas de résultats lors de la recherche d’URL complètes | Chromium bogues"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools : améliorer l’onglet Styles calculés | Chromium bogues"  
[CR1120316]: https://crbug.com/1120316 "Mettre en surbrillez le mauvais contraste sous Vue d’ensemble de CSS > couleurs | Chromium Bogues"  
[CR1121141]: https://crbug.com/1121141 "Autoriser le filtrage par type de ressource dans les journaux | Chromium bogues"  
[CR1121312]: https://crbug.com/1121312 "Paramètres être supprimé du menu Plus d’outils | Chromium bogues"  
[CR1136394]: https://crbug.com/1136394 "Outils Flexbox | Chromium Bogues"  
[CR1136655]: https://crbug.com/1136655 "Devtools : localisation v2 | Chromium bogues"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Informations sur les API de | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 - GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Serveur d’authentification web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Bonjour ! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Postman Collection Format v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Spécification OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="2a778-316">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2a778-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2a778-317">La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-87) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="2a778-317">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-87) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2a778-319">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2a778-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
