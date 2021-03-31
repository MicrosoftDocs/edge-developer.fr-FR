---
description: Découvrez comment modifier les styles et paramètres de police CSS à l’aide du volet Styles dans Microsoft Edge DevTools.
title: Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
no-loc:
- Enable new font editor tool within the Styles pane
ms.openlocfilehash: 5d9074ca65f9cb98662a1bc181f70ead4c4232e1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439492"
---
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a><span data-ttu-id="dcade-104">Modifier les styles et paramètres de police CSS dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="dcade-104">Edit CSS font styles and settings in the Styles pane</span></span>  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

<span data-ttu-id="dcade-105">La typographie sur le web est une partie importante de l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dcade-105">Typography on the web is an important part of the user experience.</span></span>  <span data-ttu-id="dcade-106">Vous souhaitez vous assurer que vous respectez les directives de la marque d’entreprise et que votre contenu s’affiche comme prévu sur différents appareils.</span><span class="sxs-lookup"><span data-stu-id="dcade-106">You want to ensure you meet corporate brand guidelines, and your content displays as expected on various devices.</span></span>  <span data-ttu-id="dcade-107">Le texte doit être facile à lire à l’aide de la taille et de la hauteur de ligne.</span><span class="sxs-lookup"><span data-stu-id="dcade-107">Text must be easy to read using size and line-height.</span></span>  <span data-ttu-id="dcade-108">Les utilisateurs peuvent re tailler des polices pour répondre à des besoins individuels.</span><span class="sxs-lookup"><span data-stu-id="dcade-108">Users may resize fonts to meet individual needs.</span></span>  <span data-ttu-id="dcade-109">Lorsque des polices spécifiques ne sont pas disponibles sur un appareil utilisateur, vous devez fournir des options de police de base.</span><span class="sxs-lookup"><span data-stu-id="dcade-109">For situations when specific fonts are not available on a user device, you should provide fallback font options.</span></span>  

<span data-ttu-id="dcade-110">CSS offre une meilleure prise en charge de la typographie au cours des dernières années.</span><span class="sxs-lookup"><span data-stu-id="dcade-110">CSS provides better support for typography in recent years.</span></span>  <span data-ttu-id="dcade-111">Des dizaines d’unités CSS différentes sont disponibles pour définir la taille du texte.</span><span class="sxs-lookup"><span data-stu-id="dcade-111">Dozens of different CSS units are available to define the size of text.</span></span>  <span data-ttu-id="dcade-112">Vous disposez également de plusieurs propriétés CSS qui affectent la taille de police, l’espacement, la hauteur de ligne et d’autres fonctionnalités typographiques.</span><span class="sxs-lookup"><span data-stu-id="dcade-112">You also have several CSS properties that affect font-size, spacing, line height, and other typographic features.</span></span>  

<span data-ttu-id="dcade-113">Pour faciliter l’travail avec la typographie, un **éditeur** de polices visuel se trouve désormais dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="dcade-113">To make it easier when working with typography, a visual **Font Editor** is now in the **Styles** pane.</span></span>  <span data-ttu-id="dcade-114">Vous pouvez modifier vos paramètres de police et les modifications sont restituer immédiatement dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="dcade-114">You may change your font settings, and the changes are rendered immediately in the browser.</span></span>  <span data-ttu-id="dcade-115">Tout cela sans connaissances approfondies du CSS.</span><span class="sxs-lookup"><span data-stu-id="dcade-115">All without in-depth knowledge of CSS.</span></span>  

<span data-ttu-id="dcade-116">Actuellement, **Enable new font editor tool within the Styles pane** la fonctionnalité est expérimentale et vous devez [l’activer pour les outils de développement Microsoft Edge.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="dcade-116">Currently the **Enable new font editor tool within the Styles pane** feature is experimental and you need to [turn it on for Microsoft Edge Developer Tools][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures].</span></span>  

<span data-ttu-id="dcade-117">Toute CSS dans le volet **Styles,** définitions de police ou styles inline, affiche automatiquement une icône qui ouvre l’éditeur de **polices visuel.**</span><span class="sxs-lookup"><span data-stu-id="dcade-117">Any CSS in the **Styles** pane, either font definitions or inline styles, automatically displays an icon that opens the visual **Font Editor**.</span></span>  <span data-ttu-id="dcade-118">Pour ouvrir Visual **Font Editor,** sélectionnez l’icône **Éditeur de** polices.</span><span class="sxs-lookup"><span data-stu-id="dcade-118">To open the visual **Font Editor**, choose the **Font Editor** icon.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Icône du volet Styles pour modifier les paramètres de police" lightbox="../media/font-editor-icon.msft.png":::
         <span data-ttu-id="dcade-120">Icône du volet **Styles** pour modifier les paramètres de police</span><span class="sxs-lookup"><span data-stu-id="dcade-120">The icon in the **Styles** pane to edit font settings</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles" lightbox="../media/font-editor-open.msft.png":::
         <span data-ttu-id="dcade-122">Éditeur **de polices** ouvert en haut du volet **Styles**</span><span class="sxs-lookup"><span data-stu-id="dcade-122">The **Font Editor** open on top of the **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="dcade-123">Tous les champs de l’éditeur **de police** visuel sont remplis à partir des valeurs du CSS dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="dcade-123">All fields in the visual **Font Editor** are populated from the values in the CSS in the **Styles** pane.</span></span>  <span data-ttu-id="dcade-124">Par exemple, la définition est définie sur dans le volet Styles, de sorte que le champ de texte de hauteur de ligne s’affiche et que la zone de texte d’unité `line-height` `160%`  `160` s’affiche. `%`</span><span class="sxs-lookup"><span data-stu-id="dcade-124">For example, the `line-height` definition is set to `160%` in the **Styles** pane, so the line height text field displays `160`, and the unit dropdown displays `%`.</span></span>  <span data-ttu-id="dcade-125">En outre, le curseur est automatiquement définie pour correspondre aux valeurs du champ de texte.</span><span class="sxs-lookup"><span data-stu-id="dcade-125">Also, the slider is automatically set to match the values of the text field.</span></span>  

<span data-ttu-id="dcade-126">**L’éditeur de** polices se compose de deux parties : le sélecteur de la famille de polices et l’éditeur de propriétés CSS.</span><span class="sxs-lookup"><span data-stu-id="dcade-126">The **Font Editor** consists of two parts:  the Font Family selector, and the CSS Properties editor.</span></span>  

## <a name="the-font-family-selector"></a><span data-ttu-id="dcade-127">Sélecteur de la famille de polices</span><span class="sxs-lookup"><span data-stu-id="dcade-127">The Font Family selector</span></span>  

<span data-ttu-id="dcade-128">Le sélecteur de la famille de polices est la partie supérieure de l’éditeur **de polices visuel.**</span><span class="sxs-lookup"><span data-stu-id="dcade-128">The Font Family selector is the upper part of the visual **Font Editor**.</span></span>  <span data-ttu-id="dcade-129">Pour choisir les polices de la règle CSS, dans l’éditeur CSS, utilisez le sélecteur **de** la famille de polices.</span><span class="sxs-lookup"><span data-stu-id="dcade-129">To choose the fonts of the CSS rule, in the CSS editor, use the **Font Family** selector.</span></span>  <span data-ttu-id="dcade-130">Vous pouvez choisir des polices principales et de base pour chaque règle CSS.</span><span class="sxs-lookup"><span data-stu-id="dcade-130">You may choose main and fallback fonts for each CSS rule.</span></span>  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles avec le sélecteur de la famille de polices mis en évidence" lightbox="../media/font-editor-font-family.msft.png":::
   <span data-ttu-id="dcade-132">Éditeur **de polices** ouvert en haut du volet **Styles** avec le sélecteur **de** la famille de polices mis en évidence</span><span class="sxs-lookup"><span data-stu-id="dcade-132">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="dcade-133">Utilisez la **liste finale Famille** de polices pour choisir parmi une liste de polices.</span><span class="sxs-lookup"><span data-stu-id="dcade-133">Use the **Font Family** dropdown to choose from a list of fonts.</span></span>  <span data-ttu-id="dcade-134">Les polices sont organisées en quatre groupes.</span><span class="sxs-lookup"><span data-stu-id="dcade-134">Fonts are organized into four groups.</span></span>  

1.  <span data-ttu-id="dcade-135">Polices calculées, qui sont les polices disponibles dans la feuille de style dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="dcade-135">Computed fonts, which are the fonts available in the stylesheet in the **Styles** pane.</span></span>  
1.  <span data-ttu-id="dcade-136">Polices système, qui sont les polices disponibles sur le système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="dcade-136">System fonts, which are the fonts that are available on the current operating system.</span></span>  
1.  <span data-ttu-id="dcade-137">Familles de polices génériques, `serif` telles que ou `sans-serif` .</span><span class="sxs-lookup"><span data-stu-id="dcade-137">Generic font families, such as `serif` or `sans-serif`.</span></span>  
1.  <span data-ttu-id="dcade-138">Valeurs globales, telles `inherit` `initial` que , et `unset` .</span><span class="sxs-lookup"><span data-stu-id="dcade-138">Global values, such as `inherit`, `initial`, and `unset`.</span></span>  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles avec le sélecteur de la famille de polices mis en évidence" lightbox="../media/font-editor-font-family-list.msft.png":::
   <span data-ttu-id="dcade-140">Éditeur **de polices** ouvert en haut du volet **Styles** avec le sélecteur **de** la famille de polices mis en évidence</span><span class="sxs-lookup"><span data-stu-id="dcade-140">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="dcade-141">Une fois que vous avez choisi une police, un autre menu déroulant s’affiche pour que vous choisissiez des polices de fallback.</span><span class="sxs-lookup"><span data-stu-id="dcade-141">After you choose a font, another dropdown menu is displayed for you to choose fallback fonts.</span></span>  <span data-ttu-id="dcade-142">Vous pouvez choisir jusqu’à huit polices de fallback.</span><span class="sxs-lookup"><span data-stu-id="dcade-142">You may choose up to eight fallback fonts.</span></span>  <span data-ttu-id="dcade-143">Pour supprimer une police, sélectionnez **l’icône Supprimer la famille de polices.**</span><span class="sxs-lookup"><span data-stu-id="dcade-143">To remove a font, choose the **Delete Font Family** icon.</span></span>  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> <span data-ttu-id="dcade-144">Si vous choisissez une valeur globale pour la famille de polices, vous n’obtenez pas une autre dropdown, car il n’y a pas de retour pour elle dans CSS.</span><span class="sxs-lookup"><span data-stu-id="dcade-144">If you choose a global value for font family, you do not get another dropdown since there is no fallback for it in CSS.</span></span>  

## <a name="the-css-properties-editor"></a><span data-ttu-id="dcade-145">Éditeur de propriétés CSS</span><span class="sxs-lookup"><span data-stu-id="dcade-145">The CSS Properties editor</span></span>  

<span data-ttu-id="dcade-146">Vous pouvez modifier les propriétés de police CSS dans la partie inférieure de Visual **Font Editor**.</span><span class="sxs-lookup"><span data-stu-id="dcade-146">You may change CSS font properties in the lower part of the visual **Font Editor**.</span></span>  <span data-ttu-id="dcade-147">Vous pouvez modifier la taille de la police, la hauteur de ligne, le poids de la police et l’espacement des lettres à l’aide de l’un des contrôles d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dcade-147">You may change the font size, line height, font weight, and letter spacing using any of the UI controls.</span></span>  <span data-ttu-id="dcade-148">Vos modifications sont appliquées immédiatement dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="dcade-148">Your changes are applied immediately in the browser.</span></span>  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles avec les propriétés CSS mises en surbrill" lightbox="../media/font-editor-css-properties.msft.png":::
   <span data-ttu-id="dcade-150">Éditeur **de polices** ouvert en haut du volet **Styles** avec les propriétés CSS mises en surbrill</span><span class="sxs-lookup"><span data-stu-id="dcade-150">The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="dcade-151">Vous pouvez également convertir des unités CSS à l’aide de Visual **Font Editor**.</span><span class="sxs-lookup"><span data-stu-id="dcade-151">You may also convert CSS units using the visual **Font Editor**.</span></span>  <span data-ttu-id="dcade-152">Par exemple, vous pouvez utiliser l’outil sur  une règle CSS où le curseur de taille de police est initialement définie sur `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="dcade-152">For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels`.</span></span>  <span data-ttu-id="dcade-153">Maintenant, utilisez la dropdown d’unité et choisissez la valeur `em` .</span><span class="sxs-lookup"><span data-stu-id="dcade-153">Now, use the unit dropdown and choose the value `em`.</span></span>  <span data-ttu-id="dcade-154">`1 em`L’affichage est égal à `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="dcade-154">The `1 em` displayed is equal to `16 pixels`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Modifier la taille de police à 16 pixels" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         <span data-ttu-id="dcade-156">Modifier la taille de la police en</span><span class="sxs-lookup"><span data-stu-id="dcade-156">Change the font size to</span></span> `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Ouvrir la dropdown d’unité pour la convertir en em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         <span data-ttu-id="dcade-158">Ouvrir la dropdown d’unités pour la convertir en</span><span class="sxs-lookup"><span data-stu-id="dcade-158">Open the unit dropdown to convert to</span></span> `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="dcade-159">La dropdown d’unité fournit toutes les unités CSS numériques disponibles.</span><span class="sxs-lookup"><span data-stu-id="dcade-159">The unit dropdown provides all the numeric CSS units that are available.</span></span>  <span data-ttu-id="dcade-160">La taille de police, la hauteur des lignes, l’importance de la police et l’espacement utilisent des unités différentes.</span><span class="sxs-lookup"><span data-stu-id="dcade-160">Font size, line height, font weight, and spacing all use different units.</span></span>  <span data-ttu-id="dcade-161">Lorsque les zones de texte sont sélectionnées, vous pouvez sélectionner les touches et les touches pour `arrow up` `arrow down` affiner vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="dcade-161">When the text boxes have focus, you may select the `arrow up` and `arrow down` keys to fine-tune your settings.</span></span>  <span data-ttu-id="dcade-162">Pour utiliser les curseurs avec un clavier, sélectionnez les `arrow left` touches et les `arrow down` touches.</span><span class="sxs-lookup"><span data-stu-id="dcade-162">To use the sliders with a keyboard, select the `arrow left` and `arrow down` keys.</span></span>  

<span data-ttu-id="dcade-163">L’éditeur de propriétés CSS inclut également des mots clés prédéfincis.</span><span class="sxs-lookup"><span data-stu-id="dcade-163">The CSS Properties editor also includes preset keywords.</span></span>  <span data-ttu-id="dcade-164">Pour utiliser les mots clés prédéfins, sur le côté droit, sélectionnez `Toggle Input Type` l’icône.</span><span class="sxs-lookup"><span data-stu-id="dcade-164">To use the preset keywords, on the right-hand side, choose the `Toggle Input Type` icon.</span></span>  <span data-ttu-id="dcade-165">L’interface utilisateur change et une liste liste des mots clés prédéfini s’affiche.</span><span class="sxs-lookup"><span data-stu-id="dcade-165">The UI changes, and a dropdown of preset keywords are displayed.</span></span>  <span data-ttu-id="dcade-166">Pour revenir à l’interface utilisateur avec le curseur et d’autres contrôles d’interface utilisateur, choisissez de nouveau `Toggle Input Type` l’icône.</span><span class="sxs-lookup"><span data-stu-id="dcade-166">To return to the UI with the slider and other UI controls, choose the `Toggle Input Type` icon again.</span></span>  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Ouvrir l’interface de mot clé prédéfiny" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   <span data-ttu-id="dcade-168">Ouvrir l’interface de mot clé prédéfiny</span><span class="sxs-lookup"><span data-stu-id="dcade-168">Open the preset keyword interface</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="dcade-169">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="dcade-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Activer les fonctionnalités expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
