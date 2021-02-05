---
description: L’outil Nouveautés est désormais welcome, Visual Font Editor dans le volet Styles, outils de débogage CSS Flexbox, etc.
title: Nouveautés de DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0a8a5e69281ced9421733059b554bd8cb997c7cd
ms.sourcegitcommit: 085046a5885c68243b763aaf6809fea43452403a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313775"
---
# <span data-ttu-id="2b024-104">Nouveautés de DevTools (Microsoft Edge 89)</span><span class="sxs-lookup"><span data-stu-id="2b024-104">What's New In DevTools (Microsoft Edge 89)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="2b024-105">Nouveautés : bienvenue</span><span class="sxs-lookup"><span data-stu-id="2b024-105">What's New is now Welcome</span></span>  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="2b024-106">**L’outil Nouveautés** de Microsoft Edge DevTools a désormais une nouvelle apparence et un nouveau nom : **Bienvenue**.</span><span class="sxs-lookup"><span data-stu-id="2b024-106">The **What's New** tool in the Microsoft Edge DevTools now has a new appearance and a new name:  **Welcome**.</span></span>  <span data-ttu-id="2b024-107">**L’outil Welcome** affiche toujours les dernières actualités et mises à jour DevTools.</span><span class="sxs-lookup"><span data-stu-id="2b024-107">The **Welcome** tool still displays the latest DevTools news and updates.</span></span>  <span data-ttu-id="2b024-108">Il inclut désormais également des liens vers la documentation DevTools de Microsoft Edge, des méthodes pour envoyer des commentaires, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="2b024-108">It now also includes links to Microsoft Edge DevTools documentation, ways to submit feedback, and more.</span></span>  <span data-ttu-id="2b024-109">Pour afficher **l’outil d’accueil** après chaque mise à jour de Microsoft Edge, cochez la case en regard de l’onglet Ouvrir après **chaque** mise à jour sous le titre.</span><span class="sxs-lookup"><span data-stu-id="2b024-109">To display the **Welcome** tool after each update to Microsoft Edge, choose the checkbox next to **Open tab after each update** under the title.</span></span>  <span data-ttu-id="2b024-110">Pour fermer **l’outil Bienvenue,** choisissez **le X** sur le côté droit du titre de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="2b024-110">To close the **Welcome** tool, choose the **X** on the right-side of the tab title.</span></span>  <span data-ttu-id="2b024-111">Si vous préférez **l’outil Nouveautés d’origine,** accédez à [Expériences][DevtoolsCustomizeIndexSettings]de paramètres et supprimez la case à cocher en regard de  >  \*\*\*\* l’onglet **Activer l’accueil.**</span><span class="sxs-lookup"><span data-stu-id="2b024-111">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="L’outil Bienvenue est mis en surbrill" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   <span data-ttu-id="2b024-113">**L’outil Bienvenue** est mis en surbrill</span><span class="sxs-lookup"><span data-stu-id="2b024-113">The **Welcome** tool is highlighted</span></span>  
:::image-end:::  

## <span data-ttu-id="2b024-114">Visual Font Editor dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="2b024-114">Visual Font Editor in the Styles pane</span></span>  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="2b024-115">Lorsque vous utilisez des polices dans CSS, utilisez le nouvel éditeur de [polices visuel.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="2b024-115">When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="2b024-116">Vous pouvez définir des polices de secours et utiliser des curseurs pour définir le poids, la taille, la hauteur de ligne et l’espacement de la police.</span><span class="sxs-lookup"><span data-stu-id="2b024-116">You may define fallback fonts, and use sliders to define font weight, size, line-height, and spacing.</span></span>  <span data-ttu-id="2b024-117">**L’éditeur de** polices vous aide à effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2b024-117">The **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="2b024-118">Basculer entre les unités pour différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="2b024-118">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="2b024-119">Basculer entre les mots clés pour différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="2b024-119">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="2b024-120">Convertir des unités</span><span class="sxs-lookup"><span data-stu-id="2b024-120">Convert units</span></span>  
*   <span data-ttu-id="2b024-121">Générer un code CSS précis</span><span class="sxs-lookup"><span data-stu-id="2b024-121">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="2b024-122">Pour activer cette expérience, accédez à Expériences de [paramètres][DevtoolsCustomizeIndexSettings]et cochez la case en regard d’Activer les nouveaux outils Éditeur de polices  >  \*\*\*\* dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="2b024-122">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new Font Editor tools within Styles pane**.</span></span>  <span data-ttu-id="2b024-123">Pour plus d’informations, accédez à Modifier les styles et paramètres de police CSS dans le volet [Styles de DevTools.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="2b024-123">For more information, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="2b024-124">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1093229][CR1093229].</span><span class="sxs-lookup"><span data-stu-id="2b024-124">To review the history of this feature in the Chromium open-source project, navigate to Issue [1093229][CR1093229].</span></span>  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="L’éditeur de police visuel est mis en surbrillon dans le volet Styles" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   <span data-ttu-id="2b024-126">L’éditeur **de police visuel** est mis en surbrillon dans le volet **Styles**</span><span class="sxs-lookup"><span data-stu-id="2b024-126">The visual **Font editor** is highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="2b024-127">Outils de débogage CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="2b024-127">CSS Flexbox debugging tools</span></span>  

<span data-ttu-id="2b024-128">Les fonctionnalités de débogage Flexbox sont en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="2b024-128">Flexbox debugging features are in active development.</span></span>  <span data-ttu-id="2b024-129">Pour activer l’expérience pour les deux [fonctionnalités suivantes,][DevtoolsCustomizeIndexSettings]accédez à Expériences de paramètres et activez la case à cocher en regard de activer les nouvelles fonctionnalités de débogage de la boîte de réception  >  \*\*\*\* **Flexbox CSS.**</span><span class="sxs-lookup"><span data-stu-id="2b024-129">To turn on the experiment for the following two features, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new CSS Flexbox debugging features**.</span></span>  <span data-ttu-id="2b024-130">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1136394][CR1136394] et [1139949][CR1139949].</span><span class="sxs-lookup"><span data-stu-id="2b024-130">To review the history of this feature in the Chromium open-source project, navigate to Issues [1136394][CR1136394] and [1139949][CR1139949].</span></span>  

### <span data-ttu-id="2b024-131">La nouvelle icône Flexbox (flex) permet d’identifier et d’afficher les conteneurs flex</span><span class="sxs-lookup"><span data-stu-id="2b024-131">New Flexbox (flex) icon helps identify and display flex containers</span></span>  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="2b024-132">Dans **l’outil Elements,** la nouvelle icône Flexbox (flex) vous permet d’identifier les conteneurs Flexbox dans votre code.</span><span class="sxs-lookup"><span data-stu-id="2b024-132">In the **Elements** tool, the new Flexbox (flex) icon helps you identify Flexbox containers in your code.</span></span>  <span data-ttu-id="2b024-133">Sélectionnez l’icône Flexbox \(flex\) pour activer ou désactiver l’effet de superposition qui contoure un conteneur Flexbox.</span><span class="sxs-lookup"><span data-stu-id="2b024-133">Choose the Flexbox \(flex\) icon to turn on or off the overlay effect that outlines a Flexbox container.</span></span>  <span data-ttu-id="2b024-134">Vous pouvez personnaliser la couleur de \*\*\*\* la superposition dans le volet De disposition, qui se trouve à côté de **Styles** et **calculé**.</span><span class="sxs-lookup"><span data-stu-id="2b024-134">You may customize the color of the overlay in the **Layout** pane, which is located next to **Styles** and **Computed**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2b024-135">Pour activer et désactiver l’effet de superposition qui contoure le conteneur Flexbox, choisissez l’icône Flexbox \( `flex` \).</span><span class="sxs-lookup"><span data-stu-id="2b024-135">To turn on and off the overlay effect that outlines the Flexbox container, choose the Flexbox \(`flex`\) icon.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2b024-136">Vous pouvez personnaliser la couleur de \*\*\*\* la superposition dans le volet De disposition en côté de **Styles** et **calculé .**</span><span class="sxs-lookup"><span data-stu-id="2b024-136">You may customize the color of the overlay in the **Layout** pane next to **Styles** and **Computed**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Icône Flexbox (flex) et page web mises en surbrill" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         <span data-ttu-id="2b024-138">Icône **Flexbox** \( `flex` \) et page web mises en surbrillion</span><span class="sxs-lookup"><span data-stu-id="2b024-138">The **Flexbox** \(`flex`\) icon and webpage highlighted</span></span> :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Superpositions Flexbox mises en évidence dans le volet De disposition" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         <span data-ttu-id="2b024-140">**Superpositions Flexbox mises** en évidence dans **le** volet De disposition</span><span class="sxs-lookup"><span data-stu-id="2b024-140">The **Flexbox overlays** highlighted in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="2b024-141">Afficher les icônes d’alignement et le quadrillage lorsque les dispositions de Flexbox changent à l’aide des propriétés CSS</span><span class="sxs-lookup"><span data-stu-id="2b024-141">Display alignment icons and gridlines when Flexbox layouts change using CSS properties</span></span>  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="2b024-142">Lorsque vous modifiez CSS pour votre disposition Flexbox, les mises à jour automatiques CSS dans le volet **Styles** affichent désormais des icônes utiles en plus des propriétés Flexbox pertinentes.</span><span class="sxs-lookup"><span data-stu-id="2b024-142">When you edit CSS for your Flexbox layout, CSS autocompletes in the **Styles** pane now displays helpful icons next to relevant Flexbox properties.</span></span>  <span data-ttu-id="2b024-143">Pour essayer cette nouvelle fonctionnalité, ouvrez **l’outil Éléments** et sélectionnez un conteneur flexible.</span><span class="sxs-lookup"><span data-stu-id="2b024-143">To try this new feature, open the **Elements** tool and select a flex container.</span></span>  <span data-ttu-id="2b024-144">Ensuite, ajoutez ou modifiez une propriété sur ce conteneur dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="2b024-144">Then add or change a property on that container in the **Styles** pane.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2b024-145">Le menu de la mise à jour automatique affiche désormais des icônes qui indiquent l’effet des propriétés d’alignement telles `align-content` que et `align-items` .</span><span class="sxs-lookup"><span data-stu-id="2b024-145">The autocomplete menu now displays icons that indicate the effect of alignment properties such as `align-content` and `align-items`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2b024-146">De plus, DevTools affiche désormais une ligne de guid pour vous aider à mieux examiner la `align-items` propriété CSS.</span><span class="sxs-lookup"><span data-stu-id="2b024-146">Additionally, DevTools now displays a guiding line to help you better review the `align-items` CSS property.</span></span>  <span data-ttu-id="2b024-147">La `gap` propriété CSS est également prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2b024-147">The `gap` CSS property is supported as well.</span></span>  <span data-ttu-id="2b024-148">Dans la figure suivante, la propriété CSS est définie sur et le modèle d’effet de hachage `gap` `gap: 12px;` pour chaque intervalle s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2b024-148">In the following figure, the `gap` CSS property is set to `gap: 12px;` and the hatching pattern for each gap is displayed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menu de la mise en surbrillence automatique mis en surbrillence pour les propriétés CSS qui commencent par align-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         <span data-ttu-id="2b024-150">Menu de la mise à jour automatique mis en surbrillence pour les propriétés CSS qui commencent par</span><span class="sxs-lookup"><span data-stu-id="2b024-150">Autocomplete menu highlighted for CSS properties that start with</span></span> `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Espace flexbox dans les propriétés CSS et la page web mis en surbrillion" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         <span data-ttu-id="2b024-152">Flexbox `gap` dans les propriétés CSS et la page web mises en surbrillion</span><span class="sxs-lookup"><span data-stu-id="2b024-152">Flexbox `gap` in CSS properties and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="2b024-153">Ajouter rapidement des outils avec le nouveau bouton Plus d’outils</span><span class="sxs-lookup"><span data-stu-id="2b024-153">Add tools quickly with new More Tools button</span></span>  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="2b024-154">Vous avez maintenant une nouvelle façon d’ouvrir d’autres outils dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2b024-154">You now have a new way to open more tools in the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="2b024-155">Une fois que vous \*\*\*\* avez activer cette expérience, l’icône Plus d’outils s’affiche sous la forme d’un signe plus ( ) à droite `+` du panneau principal.</span><span class="sxs-lookup"><span data-stu-id="2b024-155">After you turn on this experiment, the **More Tools** icon displays as a plus sign (`+`) to the right of the main panel.</span></span>  <span data-ttu-id="2b024-156">Pour afficher la liste des autres outils à ajouter au panneau principal, sélectionnez l’icône Plus d’outils **\(** `+` \).</span><span class="sxs-lookup"><span data-stu-id="2b024-156">To display a list of other tools to add to the main panel, choose the **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="2b024-157">Pour activer cette expérience, accédez à Expériences de [paramètres,][DevtoolsCustomizeIndexSettings]puis activez la case à cocher en regard de l’onglet Activer + bouton pour ouvrir  >  **d’autres\*\*\*\*outils.**</span><span class="sxs-lookup"><span data-stu-id="2b024-157">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**, and then choose the checkbox next to **Enable + button tab menus to open more tools**.</span></span>  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Autres outils mis en évidence dans DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   <span data-ttu-id="2b024-159">**Autres outils** mis en évidence dans DevTools</span><span class="sxs-lookup"><span data-stu-id="2b024-159">**More Tools** highlighted in DevTools</span></span>  
:::image-end:::  

## <span data-ttu-id="2b024-160">Les technologies d’assistance annoncent désormais la position et le nombre de suggestions CSS</span><span class="sxs-lookup"><span data-stu-id="2b024-160">Assistive technologies now announce position and count of CSS suggestions</span></span>  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

<span data-ttu-id="2b024-161">Lorsque vous modifiez CSS, vous obtenez une dropdown de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2b024-161">When you edit CSS, you get a dropdown of features.</span></span>  <span data-ttu-id="2b024-162">Cette fonctionnalité n’était pas disponible pour les utilisateurs de technologies d’assistance, car elle est annoncée dans Microsoft Edge version 89.</span><span class="sxs-lookup"><span data-stu-id="2b024-162">This feature was not available to users of assistive technologies, since it is announced in Microsoft Edge version 89.</span></span>  <span data-ttu-id="2b024-163">Un utilisateur de technologies d’assistance peut désormais parcourir les suggestions CSS dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="2b024-163">A user of assistive technologies may now navigate CSS suggestions in the **Styles** pane.</span></span>  <span data-ttu-id="2b024-164">Dans Microsoft Edge version 88 et versions antérieures, la technologie d’assistance annoncée en tant qu’utilisateur a accédé à la liste des suggestions lors de la modification de CSS dans le volet `Suggestion` **Styles.**</span><span class="sxs-lookup"><span data-stu-id="2b024-164">In Microsoft Edge version 88 and earlier, assistive technology announced `Suggestion` as a user navigated through the list of suggestions when editing CSS in the **Styles** pane.</span></span>  <span data-ttu-id="2b024-165">Dans Microsoft Edge version 89, un utilisateur de technologie d’assistance entend désormais la position et le nombre de suggestions actuelles.</span><span class="sxs-lookup"><span data-stu-id="2b024-165">In Microsoft Edge version 89, a user of assistive technology now hears the position and count of the current suggestion.</span></span>  <span data-ttu-id="2b024-166">Chaque suggestion est annoncée lorsque l’utilisateur navigue dans la liste des suggestions, telles que la suggestion 3 sur 5.</span><span class="sxs-lookup"><span data-stu-id="2b024-166">Each suggestion is announced as the user navigates through the list of suggestions, such as Suggestion 3 of 5.</span></span>  <span data-ttu-id="2b024-167">Pour en savoir plus sur l’écriture de CSS dans DevTools, accédez à [Modifier CSS][DevtoolsCssReferenceChangeCss].</span><span class="sxs-lookup"><span data-stu-id="2b024-167">To learn more about writing CSS in the DevTools, navigate to [Change CSS][DevtoolsCssReferenceChangeCss].</span></span>  <span data-ttu-id="2b024-168">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1157329][CR1157329].</span><span class="sxs-lookup"><span data-stu-id="2b024-168">To review the history of this feature in the Chromium open-source project, navigate to Issue [1157329][CR1157329].</span></span>  

<span data-ttu-id="2b024-169">Pour afficher une vidéo qui affiche et lit plusieurs suggestions avec cette expérience, accédez à Voiceover pour annoncer les [options devtools](https://youtu.be/9TcUpleEwwA) sur YouTube.</span><span class="sxs-lookup"><span data-stu-id="2b024-169">To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.</span></span>  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Suggestion mise en évidence dans le volet Styles" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   <span data-ttu-id="2b024-171">Liste `suggestion` mise en évidence dans le volet **Styles**</span><span class="sxs-lookup"><span data-stu-id="2b024-171">The `suggestion` list highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="2b024-172">Émuler Surface Duo et Samsung Samsung Fold</span><span class="sxs-lookup"><span data-stu-id="2b024-172">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

<span data-ttu-id="2b024-173">Testez l’apparence de votre site web ou de votre application sur les appareils suivants dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2b024-173">Test the appearance of your website or app on the following devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="2b024-174">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b024-174">Surface Duo</span></span>][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [<span data-ttu-id="2b024-175">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="2b024-175">Samsung Galaxy Fold</span></span>][SamsungUsMobileGalaxyFold]  
    
<span data-ttu-id="2b024-176">Activer les **fonctionnalités de** plateforme Web expérimentale pour accéder à la nouvelle fonctionnalité multimédia [CSS][DualScreenWebCssMediaSpanning] couvrant l’écran et à [l’API JavaScript getWindowSegments.][DualScreenWebJavascriptGetwindowsegments]</span><span class="sxs-lookup"><span data-stu-id="2b024-176">Turn on **Experimental Web Platform features** to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [getWindowSegments JavaScript API][DualScreenWebJavascriptGetwindowsegments].</span></span>  <span data-ttu-id="2b024-177">Accédez à `edge://flags` l’indicateur et basculez-le en de côté des **fonctionnalités de plateforme Web expérimentale.**</span><span class="sxs-lookup"><span data-stu-id="2b024-177">Navigate to `edge://flags` and toggle the flag next to **Experimental Web Platform features**.</span></span>  <span data-ttu-id="2b024-178">Pour améliorer votre site web ou votre application pour les appareils à double écran et pliables, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil.][DevtoolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="2b024-178">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="2b024-179">[Couvrant,][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]c’est-à-dit lorsque votre site web \(ou application\) apparaît sur les deux écrans.</span><span class="sxs-lookup"><span data-stu-id="2b024-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>  
*   <span data-ttu-id="2b024-180">[Rendu de la séam,][DualScreenIntroductionHowToWorkWithSeam]qui est l’espace entre les deux écrans.</span><span class="sxs-lookup"><span data-stu-id="2b024-180">[Rendering the seam][DualScreenIntroductionHowToWorkWithSeam], which is the space between the two screens.</span></span>  
    
<span data-ttu-id="2b024-181">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1054281][CR1054281].</span><span class="sxs-lookup"><span data-stu-id="2b024-181">To review the history of this feature in the Chromium open-source project, navigate to Issue [1054281][CR1054281].</span></span>  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Émuler double écran" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   <span data-ttu-id="2b024-183">Émuler double écran</span><span class="sxs-lookup"><span data-stu-id="2b024-183">Emulate dual-screen</span></span>  
:::image-end:::  

## <span data-ttu-id="2b024-184">Outils de développement Microsoft Edge Visual Studio Code version 1.1.2</span><span class="sxs-lookup"><span data-stu-id="2b024-184">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span></span>  

<span data-ttu-id="2b024-185">Les outils de développement [Microsoft Edge pour Visual Studio l’extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de code version 1.1.2 pour Microsoft Visual Studio Code ont les modifications suivantes depuis la version précédente.</span><span class="sxs-lookup"><span data-stu-id="2b024-185">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="2b024-186">Microsoft Visual Studio code met automatiquement à jour les extensions.</span><span class="sxs-lookup"><span data-stu-id="2b024-186">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="2b024-187">Pour mettre à jour manuellement la version 1.1.2, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="2b024-187">To manually update to version 1.1.2, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

*   <span data-ttu-id="2b024-188">Ajout **d’un bouton Fermer l’instance** à chaque élément de la liste cible \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span><span class="sxs-lookup"><span data-stu-id="2b024-188">Added a **Close instance** button to each item on the target list \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span></span>  
*   <span data-ttu-id="2b024-189">Version de [Microsoft Edge DevTools][DevtoolsMain] déversée de 84.0.522.63 à [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span><span class="sxs-lookup"><span data-stu-id="2b024-189">Bumped [Microsoft Edge DevTools][DevtoolsMain] version from 84.0.522.63 to [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span></span>  
*   <span data-ttu-id="2b024-190">[Débogger inclus pour Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] en tant que dépendance \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span><span class="sxs-lookup"><span data-stu-id="2b024-190">Included [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] as a dependency  \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span></span>  
*   <span data-ttu-id="2b024-191">Option de paramètres implémentée pour modifier les thèmes d’extension \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span><span class="sxs-lookup"><span data-stu-id="2b024-191">Implemented settings option to change extension themes \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span></span>  
    
<span data-ttu-id="2b024-192">Vous pouvez déposer des problèmes et contribuer à l’extension sur le référentiel [GitHub vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]</span><span class="sxs-lookup"><span data-stu-id="2b024-192">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <span data-ttu-id="2b024-193">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="2b024-193">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="2b024-194">Capture d’écran du nœud au-delà de la vue</span><span class="sxs-lookup"><span data-stu-id="2b024-194">Capture node screenshot beyond viewport</span></span>  

<span data-ttu-id="2b024-195">Dans Microsoft Edge version 89, les captures d’écran de nœud sont plus précises, ce qui permet de capturer le nœud complet même si le contenu du nœud n’est pas visible dans la vue.</span><span class="sxs-lookup"><span data-stu-id="2b024-195">In Microsoft Edge version 89, node screenshots are more accurate, capturing the full node even if content from the node is not visible in the viewport.</span></span>  <span data-ttu-id="2b024-196">Dans **l’outil Éléments,** pointez sur un élément, ouvrez le menu contextuel \(clic droit\), puis choisissez **Capture d’écran du nœud .**</span><span class="sxs-lookup"><span data-stu-id="2b024-196">In the **Elements** tool, hover  on an element, open the contextual menu \(right-click\), and choose **Capture node screenshot**.</span></span>  <span data-ttu-id="2b024-197">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1003629][CR1003629].</span><span class="sxs-lookup"><span data-stu-id="2b024-197">To review the history of this feature in the Chromium open-source project, navigate to Issue [1003629][CR1003629].</span></span>  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Capture d’écran du nœud mis en évidence dans le menu contextique de l’outil Éléments" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   <span data-ttu-id="2b024-199">**Capture d’écran du nœud** mis en évidence dans le menu contextique de **l’outil Éléments**</span><span class="sxs-lookup"><span data-stu-id="2b024-199">**Capture node screenshot** highlighted on the context menu in the **Elements** tool</span></span>  
:::image-end:::  

### <span data-ttu-id="2b024-200">Mises à jour de l’outil Éléments</span><span class="sxs-lookup"><span data-stu-id="2b024-200">Elements tool updates</span></span>  

#### <span data-ttu-id="2b024-201">Prise en charge du forçage de l’état CSS cible</span><span class="sxs-lookup"><span data-stu-id="2b024-201">Support forcing the :target CSS state</span></span>  

<span data-ttu-id="2b024-202">Vous pouvez désormais utiliser DevTools pour forcer [la][MdnDocsWebCssTarget] pseudo-classe CSS cible.</span><span class="sxs-lookup"><span data-stu-id="2b024-202">You may now use DevTools to force the [:target][MdnDocsWebCssTarget] CSS pseudo-class.</span></span>  <span data-ttu-id="2b024-203">La pseudo-classe est déclenchée lorsqu’un élément unique \(l’élément cible\) a un élément qui correspond à un `:target` `id` fragment de l’URL.</span><span class="sxs-lookup"><span data-stu-id="2b024-203">The `:target` pseudo-class is triggered when a unique element \(the target element\) has an `id` that matches a fragment of the URL.</span></span>  <span data-ttu-id="2b024-204">Par exemple, `http://www.example.com/index.html#section1` l’URL déclenche la `:target` pseudo-classe sur un élément HTML avec `id="section1"` .</span><span class="sxs-lookup"><span data-stu-id="2b024-204">For example, the `http://www.example.com/index.html#section1` URL triggers the `:target` pseudo-class on an HTML element with `id="section1"`.</span></span>  <span data-ttu-id="2b024-205">Pour essayer une démonstration avec la section 1 mise en évidence, accédez à [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span><span class="sxs-lookup"><span data-stu-id="2b024-205">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span></span>  <span data-ttu-id="2b024-206">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1156628][CR1156628].</span><span class="sxs-lookup"><span data-stu-id="2b024-206">To review the history of this feature in the Chromium open-source project, navigate to Issue [1156628][CR1156628].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Page web mise en surbrillant sans CSS forcé" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         <span data-ttu-id="2b024-208">Page web mise en surbrillant sans CSS forcé</span><span class="sxs-lookup"><span data-stu-id="2b024-208">Webpage highlighted with no forced CSS</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forcé et page web mise en surbrill" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` <span data-ttu-id="2b024-210">CSS forcé et page web mise en surbrill</span><span class="sxs-lookup"><span data-stu-id="2b024-210">CSS forced and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="2b024-211">Utiliser des éléments dupliqués pour copier des éléments</span><span class="sxs-lookup"><span data-stu-id="2b024-211">Use Duplicate elements to copy elements</span></span>  

<span data-ttu-id="2b024-212">Utilisez le raccourci du nouvel élément **Duplicate** pour cloner un élément.</span><span class="sxs-lookup"><span data-stu-id="2b024-212">Use the new **Duplicate element** shortcut to clone an element.</span></span>  <span data-ttu-id="2b024-213">Dans **l’outil Éléments,** pointez sur un élément, ouvrez le menu contextuel \(clic droit\), choisissez **Élément dupliqué**.</span><span class="sxs-lookup"><span data-stu-id="2b024-213">In the **Elements** tool, hover on an element, open the contextual menu \(right-click\), choose **Duplicate element**.</span></span>  <span data-ttu-id="2b024-214">Un nouvel élément est créé sous l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2b024-214">A new element is created under the selected element.</span></span>  <span data-ttu-id="2b024-215">Pour dupliquer l’élément à l’aide d’un raccourci clavier, sélectionnez `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) ou `Shift` + `Option` + `Down Arrow` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="2b024-215">To duplicate the element with a keyboard shortcut, select `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) or `Shift`+`Option`+`Down Arrow` \(macOS\).</span></span>  <span data-ttu-id="2b024-216">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1150797][CR1150797].</span><span class="sxs-lookup"><span data-stu-id="2b024-216">To review the history of this feature in the Chromium open-source project, navigate to Issue [1150797][CR1150797].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="L’élément Duplicate est mis en surbrillon dans le menu contextique d’un élément de l’outil Elements" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   <span data-ttu-id="2b024-218">**L’élément Duplicate** est mis en surbrillon dans le menu contextique d’un élément de **l’outil Elements**</span><span class="sxs-lookup"><span data-stu-id="2b024-218">The **Duplicate element** is highlighted in the context menu on an element in the **Elements** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="2b024-219">S sélectionneurs de couleurs pour les propriétés CSS personnalisées</span><span class="sxs-lookup"><span data-stu-id="2b024-219">Color pickers for custom CSS properties</span></span>  

<span data-ttu-id="2b024-220">Le **volet Styles** affiche désormais les soches de couleur pour les propriétés CSS personnalisées.</span><span class="sxs-lookup"><span data-stu-id="2b024-220">The **Styles** pane now displays color pickers for custom CSS properties.</span></span>  <span data-ttu-id="2b024-221">Pour passer en cycle dans les formats RGBA, HSLA et Hex de la valeur de couleur, maintenez et choisissez le s `Shift` sélectionneur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="2b024-221">To cycle through the RGBA, HSLA, and Hex formats of the color value, hold `Shift` and choose the color picker.</span></span>  <span data-ttu-id="2b024-222">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1147016.][CR1147016]</span><span class="sxs-lookup"><span data-stu-id="2b024-222">To review the history of this feature in the Chromium open-source project, navigate to Issue [1147016][CR1147016].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="S sélectionneurs de couleurs pour les propriétés CSS personnalisées" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   <span data-ttu-id="2b024-224">S sélectionneurs de couleurs pour les propriétés CSS personnalisées</span><span class="sxs-lookup"><span data-stu-id="2b024-224">Color pickers for custom CSS properties</span></span>  
:::image-end:::  

#### <span data-ttu-id="2b024-225">Copier les classes et propriétés CSS</span><span class="sxs-lookup"><span data-stu-id="2b024-225">Copy CSS classes and properties</span></span>  

<span data-ttu-id="2b024-226">Vous pouvez maintenant copier les propriétés CSS plus rapidement avec quelques nouvelles options dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="2b024-226">You may now copy CSS properties quicker with a few new options in the contextual menu.</span></span>  <span data-ttu-id="2b024-227">Dans **l’outil Elements,** choisissez un élément.</span><span class="sxs-lookup"><span data-stu-id="2b024-227">In the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="2b024-228">Pour copier la valeur, dans le volet **Styles,** pointez sur une classe CSS ou une propriété CSS, ouvrez un menu contextuel \(clic droit\), puis choisissez l’option de copie.</span><span class="sxs-lookup"><span data-stu-id="2b024-228">To copy the value, in the **Styles** pane, hover on a CSS class or a CSS property, open a contextual menu \(right-click\), and choose the copy option.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2b024-229">Copiez les options d’une classe CSS.</span><span class="sxs-lookup"><span data-stu-id="2b024-229">Copy options for a CSS class.</span></span>  
      
      | <span data-ttu-id="2b024-230">Option</span><span class="sxs-lookup"><span data-stu-id="2b024-230">Option</span></span> | <span data-ttu-id="2b024-231">Détails</span><span class="sxs-lookup"><span data-stu-id="2b024-231">Details</span></span> |  
      |:--- |:--- |  
      | **<span data-ttu-id="2b024-232">Sélecteur de copie</span><span class="sxs-lookup"><span data-stu-id="2b024-232">Copy selector</span></span>** | <span data-ttu-id="2b024-233">Copiez le nom du sélecteur actuel.</span><span class="sxs-lookup"><span data-stu-id="2b024-233">Copy the current selector name.</span></span> |  
      | **<span data-ttu-id="2b024-234">Règle de copie</span><span class="sxs-lookup"><span data-stu-id="2b024-234">Copy rule</span></span>** | <span data-ttu-id="2b024-235">Copiez la règle du sélecteur actuel.</span><span class="sxs-lookup"><span data-stu-id="2b024-235">Copy the rule of the current selector.</span></span> |  
      | **<span data-ttu-id="2b024-236">Copier toutes les déclarations</span><span class="sxs-lookup"><span data-stu-id="2b024-236">Copy all declarations</span></span>** | <span data-ttu-id="2b024-237">Copiez toutes les déclarations sous la règle actuelle, y compris les propriétés non valides et préfixées.</span><span class="sxs-lookup"><span data-stu-id="2b024-237">Copy all declarations under the current rule, including non-valid and prefixed properties.</span></span> |  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2b024-238">Options de copie pour une propriété CSS.</span><span class="sxs-lookup"><span data-stu-id="2b024-238">Copy options for a CSS property.</span></span>  
      
      | <span data-ttu-id="2b024-239">Option</span><span class="sxs-lookup"><span data-stu-id="2b024-239">Option</span></span> | <span data-ttu-id="2b024-240">Détails</span><span class="sxs-lookup"><span data-stu-id="2b024-240">Details</span></span> |      
      |:--- |:--- |  
      | **<span data-ttu-id="2b024-241">Déclaration de copie</span><span class="sxs-lookup"><span data-stu-id="2b024-241">Copy declaration</span></span>** | <span data-ttu-id="2b024-242">Copiez la déclaration de la ligne actuelle.</span><span class="sxs-lookup"><span data-stu-id="2b024-242">Copy the declaration of the current line.</span></span> |  
      | **<span data-ttu-id="2b024-243">Copy, propriété</span><span class="sxs-lookup"><span data-stu-id="2b024-243">Copy property</span></span>** | <span data-ttu-id="2b024-244">Copiez la propriété de la ligne actuelle.</span><span class="sxs-lookup"><span data-stu-id="2b024-244">Copy the property of the current line.</span></span> |  
      | **<span data-ttu-id="2b024-245">Valeur de copie</span><span class="sxs-lookup"><span data-stu-id="2b024-245">Copy value</span></span>** | <span data-ttu-id="2b024-246">Copiez la valeur de la ligne actuelle.</span><span class="sxs-lookup"><span data-stu-id="2b024-246">Copy the value of the current line.</span></span> |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Copier les options d’une classe CSS dans le menu contextuel" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         <span data-ttu-id="2b024-248">Copier les options d’une classe CSS dans le menu contextuel</span><span class="sxs-lookup"><span data-stu-id="2b024-248">Copy options for a CSS class in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Copier les options d’une propriété CSS dans le menu contextuel" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         <span data-ttu-id="2b024-250">Copier les options d’une propriété CSS dans le menu contextuel</span><span class="sxs-lookup"><span data-stu-id="2b024-250">Copy options for a CSS property in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="2b024-251">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1152391][CR1152391].</span><span class="sxs-lookup"><span data-stu-id="2b024-251">To review the history of this feature in the Chromium open-source project, navigate to Issue [1152391][CR1152391].</span></span>  

### <span data-ttu-id="2b024-252">Mises à jour des cookies</span><span class="sxs-lookup"><span data-stu-id="2b024-252">Cookies updates</span></span>  

#### <span data-ttu-id="2b024-253">Nouvelle option pour afficher les cookies décodés par l’URL</span><span class="sxs-lookup"><span data-stu-id="2b024-253">New option to display URL-decoded cookies</span></span>  

<span data-ttu-id="2b024-254">Vous pouvez maintenant choisir d’afficher la valeur des cookies décodés par l’URL dans le **volet Cookies.**</span><span class="sxs-lookup"><span data-stu-id="2b024-254">You may now opt to display the URL-decoded cookies value in the **Cookies** pane.</span></span>  <span data-ttu-id="2b024-255">Pour afficher le cookie décodé, accédez au volet Cookies de **l’application,** choisissez un cookie dans la liste, puis cochez la case en regard de  >  \*\*\*\* **l’url décodée.**</span><span class="sxs-lookup"><span data-stu-id="2b024-255">To display the decoded cookie, navigate to **Application** > **Cookies** pane, choose any cookie on the list, and choose the checkbox next to **Show URL decoded**.</span></span>  <span data-ttu-id="2b024-256">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 997625][CR997625].</span><span class="sxs-lookup"><span data-stu-id="2b024-256">To review the history of this feature in the Chromium open-source project, navigate to Issue [997625][CR997625].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Option d’affichage des cookies décodés par l’URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   <span data-ttu-id="2b024-258">Option d’affichage des cookies décodés par l’URL</span><span class="sxs-lookup"><span data-stu-id="2b024-258">Option to display URL decoded cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="2b024-259">Filtrer et effacer les cookies visibles</span><span class="sxs-lookup"><span data-stu-id="2b024-259">Filter and clear visible cookies</span></span>  

<span data-ttu-id="2b024-260">Dans Microsoft Edge version 88 ou antérieure, l’outil **Application** fournissait uniquement un moyen d’effacer tous les cookies avec le bouton Effacer **tous les cookies.**</span><span class="sxs-lookup"><span data-stu-id="2b024-260">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span></span>  <span data-ttu-id="2b024-261">Dans Microsoft Edge version 89, vous pouvez désormais choisir Effacer les **cookies filtrés** pour supprimer uniquement les cookies filtrés.</span><span class="sxs-lookup"><span data-stu-id="2b024-261">In Microsoft Edge version 89, you may now choose **Clear filtered cookies** to delete only the filtered cookies.</span></span>  <span data-ttu-id="2b024-262">Pour filtrer les \*\*\*\* cookies, accédez à  >  **Cookies d’application**et tapez dans la **boîte** de texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="2b024-262">To filter cookies, navigate to **Application** > **Cookies**, and type in the **Filter** textbox.</span></span>  <span data-ttu-id="2b024-263">Pour supprimer les cookies affichés, sélectionnez le bouton Effacer **les cookies filtrés.**</span><span class="sxs-lookup"><span data-stu-id="2b024-263">To delete the displayed cookies, choose the **Clear filtered cookies** button.</span></span>  <span data-ttu-id="2b024-264">Pour afficher tous les autres cookies, effacer le texte du filtre.</span><span class="sxs-lookup"><span data-stu-id="2b024-264">To display all other cookies, clear the filter text.</span></span>  <span data-ttu-id="2b024-265">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 978059][CR978059].</span><span class="sxs-lookup"><span data-stu-id="2b024-265">To review the history of this feature in the Chromium open-source project, navigate to Issue [978059][CR978059].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Effacer uniquement les cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   <span data-ttu-id="2b024-267">Effacer uniquement les cookies visibles</span><span class="sxs-lookup"><span data-stu-id="2b024-267">Clear only visible cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="2b024-268">Nouvelle option pour effacer les cookies tiers dans le volet stockage</span><span class="sxs-lookup"><span data-stu-id="2b024-268">New option to clear third-party cookies in the Storage pane</span></span>  

<span data-ttu-id="2b024-269">DevTools n’effacera désormais que les cookies de première partie par défaut.</span><span class="sxs-lookup"><span data-stu-id="2b024-269">DevTools now clear only first-party cookies by default.</span></span>  <span data-ttu-id="2b024-270">Pour effacer les données du site web \*\*\*\* et les cookies de première partie uniquement, accédez au stockage d’applications, puis choisissez  >  \*\*\*\* Effacer les données **de site.**</span><span class="sxs-lookup"><span data-stu-id="2b024-270">To clear website data and first-party cookies only, navigate to **Application** > **Storage**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="2b024-271">Pour effacer les données du site web et tous les cookies, accédez à **Stockage**  >  **d’applications.**</span><span class="sxs-lookup"><span data-stu-id="2b024-271">To clear website data and all cookies, navigate to **Application** > **Storage**.</span></span>  <span data-ttu-id="2b024-272">Cochez la case en regard de **l’utilisation de cookies tiers,** puis **sélectionnez Effacer les données du site.**</span><span class="sxs-lookup"><span data-stu-id="2b024-272">Choose the checkbox next to **including third-party cookies**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="2b024-273">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1012337][CR1012337].</span><span class="sxs-lookup"><span data-stu-id="2b024-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1012337][CR1012337].</span></span>  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Option pour effacer les cookies tiers" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   <span data-ttu-id="2b024-275">Option pour effacer les cookies tiers</span><span class="sxs-lookup"><span data-stu-id="2b024-275">Option to clear third-party cookies</span></span>  
:::image-end:::  

### <span data-ttu-id="2b024-276">Mises à jour de l’outil réseau</span><span class="sxs-lookup"><span data-stu-id="2b024-276">Network tool updates</span></span>  

#### <span data-ttu-id="2b024-277">Paramètre du journal réseau d’enregistrement persistant</span><span class="sxs-lookup"><span data-stu-id="2b024-277">Persist Record network log setting</span></span>  

<span data-ttu-id="2b024-278">Dans Microsoft Edge version 88 ou antérieure, DevTools réinitialise le paramètre enregistrer le journal réseau lors de l’actualisation d’une page web. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2b024-278">In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log** setting when a webpage refreshes.</span></span>  <span data-ttu-id="2b024-279">Dans Microsoft Edge version 89, DevTools fait désormais persister le paramètre Enregistrer le **journal réseau.**</span><span class="sxs-lookup"><span data-stu-id="2b024-279">In Microsoft Edge version 89, DevTools now persist the **Record network log** setting.</span></span>  <span data-ttu-id="2b024-280">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1122580][CR1122580].</span><span class="sxs-lookup"><span data-stu-id="2b024-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122580][CR1122580].</span></span>  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Enregistrer le journal réseau" lightbox="../../media/2021/01/network-log.msft.png":::
   <span data-ttu-id="2b024-282">Enregistrer le journal réseau</span><span class="sxs-lookup"><span data-stu-id="2b024-282">Record network log</span></span>  
:::image-end:::  

#### <span data-ttu-id="2b024-283">L’option en ligne n’est plus une option de limitation</span><span class="sxs-lookup"><span data-stu-id="2b024-283">Online option is now No throttling option</span></span>  

<span data-ttu-id="2b024-284">L’option d’émulation réseau **en ligne** est désormais renommée **No Throttling**.</span><span class="sxs-lookup"><span data-stu-id="2b024-284">The network emulation option **Online** is now renamed to **No Throttling**.</span></span>  <span data-ttu-id="2b024-285">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1028078][CR1028078].</span><span class="sxs-lookup"><span data-stu-id="2b024-285">To review the history of this feature in the Chromium open-source project, navigate to Issue [1028078][CR1028078].</span></span>  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Aucune option de limitation" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   <span data-ttu-id="2b024-287">**Aucune** option de limitation</span><span class="sxs-lookup"><span data-stu-id="2b024-287">**No throttling** option</span></span>  
:::image-end:::  

### <span data-ttu-id="2b024-288">Nouvelles options de copie dans l’outil Console, l’outil Sources et le volet Styles</span><span class="sxs-lookup"><span data-stu-id="2b024-288">New copy options in the Console tool, Sources tool, and Styles pane</span></span>

#### <span data-ttu-id="2b024-289">Copier un objet dans l’outil Console et Sources</span><span class="sxs-lookup"><span data-stu-id="2b024-289">Copy object in the Console and Sources tool</span></span>  

<span data-ttu-id="2b024-290">Vous pouvez maintenant copier des valeurs d’objet dans les outils **Console** **et Sources.**</span><span class="sxs-lookup"><span data-stu-id="2b024-290">You may now copy object values in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="2b024-291">La possibilité de copier des valeurs d’objet est utile lorsque vous travaillez avec des objets de grande taille.</span><span class="sxs-lookup"><span data-stu-id="2b024-291">The ability to copy object values is useful when working with large objects.</span></span>  <span data-ttu-id="2b024-292">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1148353][CR1148353] et [1149859][CR1149859].</span><span class="sxs-lookup"><span data-stu-id="2b024-292">To review the history of this feature in the Chromium open-source project, navigate to Issues [1148353][CR1148353] and [1149859][CR1149859].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2b024-293">Dans **l’outil Console,** pointez sur un objet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier l’objet**.</span><span class="sxs-lookup"><span data-stu-id="2b024-293">In the **Console** tool, hover on an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2b024-294">Dans l’outil **Sources,** sur un point d’arrêt, pointez sur un objet, dans la fenêtre contextuelle Objet, sélectionnez un objet, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier l’objet **.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2b024-294">In the **Sources** tool, on a breakpoint, hover on an object, in the **Object** popup window, highlight an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copier un objet dans la console" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         <span data-ttu-id="2b024-296">Copier un objet dans la **console**</span><span class="sxs-lookup"><span data-stu-id="2b024-296">Copy object in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copier un objet dans les sources" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         <span data-ttu-id="2b024-298">Copier un objet dans les **sources**</span><span class="sxs-lookup"><span data-stu-id="2b024-298">Copy object in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="2b024-299">Copier le nom de fichier dans l’outil Sources et le volet Styles</span><span class="sxs-lookup"><span data-stu-id="2b024-299">Copy file name in the Sources tool and Styles pane</span></span>  

<span data-ttu-id="2b024-300">Vous pouvez maintenant copier un nom de fichier à l’aide du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="2b024-300">You may now copy a file name using the contextual menu.</span></span>  <span data-ttu-id="2b024-301">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1155120][CR1155120].</span><span class="sxs-lookup"><span data-stu-id="2b024-301">To review the history of this feature in the Chromium open-source project, navigate to Issues [1155120][CR1155120].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2b024-302">Dans **l’outil Sources,** pointez sur un nom de fichier, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier le nom **du fichier.**</span><span class="sxs-lookup"><span data-stu-id="2b024-302">In the **Sources** tool, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2b024-303">Dans **le** volet Styles \*\*\*\* de l’outil >, pointez sur un nom de fichier, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier le nom **du fichier.**</span><span class="sxs-lookup"><span data-stu-id="2b024-303">In the **Elements** tool > **Styles** pane, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copier le nom du fichier dans les sources" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         <span data-ttu-id="2b024-305">Copier le nom du fichier dans les **sources**</span><span class="sxs-lookup"><span data-stu-id="2b024-305">Copy file name in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copier le nom de fichier dans le volet Styles" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         <span data-ttu-id="2b024-307">Copier le nom de fichier dans **le volet Styles**</span><span class="sxs-lookup"><span data-stu-id="2b024-307">Copy file name in **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="2b024-308">Mises à jour des détails du cadre</span><span class="sxs-lookup"><span data-stu-id="2b024-308">Updates to Frame details</span></span>  

#### <span data-ttu-id="2b024-309">Informations sur les employés de service dans les détails de l’image</span><span class="sxs-lookup"><span data-stu-id="2b024-309">Service Workers information in Frame details</span></span>  

<span data-ttu-id="2b024-310">DevTools répertorie désormais un service de travail dédié sous le cadre parent.</span><span class="sxs-lookup"><span data-stu-id="2b024-310">DevTools now lists a dedicated service worker under the parent frame.</span></span>  <span data-ttu-id="2b024-311">Dans la figure suivante, les détails du service de travail sont affichés.</span><span class="sxs-lookup"><span data-stu-id="2b024-311">In the following figure, service worker details are displayed.</span></span>  <span data-ttu-id="2b024-312">Pour afficher les détails du travail de service, accédez aux travailleurs du service Cadres **d’application,**  >  \*\*\*\*  >  `top`  >  \*\*\*\* puis choisissez un service de travail.</span><span class="sxs-lookup"><span data-stu-id="2b024-312">To display the service worker details, navigate to **Application** > **Frames** > `top` > **Service Workers** and then choose a service worker.</span></span>  <span data-ttu-id="2b024-313">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1122507][CR1122507].</span><span class="sxs-lookup"><span data-stu-id="2b024-313">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122507][CR1122507].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informations sur les employés de service dans les détails des cadres" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   <span data-ttu-id="2b024-315">**Informations sur les employés** de service dans les **détails des** cadres</span><span class="sxs-lookup"><span data-stu-id="2b024-315">**Service Workers** information in the **Frames** details</span></span>  
:::image-end:::  

#### <span data-ttu-id="2b024-316">Mesurer les informations de mémoire dans les détails de l’image</span><span class="sxs-lookup"><span data-stu-id="2b024-316">Measure Memory information in Frame details</span></span>  

<span data-ttu-id="2b024-317">`performance.measureMemory()`L’état de l’API s’affiche désormais sous la section **disponibilité de l’API.**</span><span class="sxs-lookup"><span data-stu-id="2b024-317">The `performance.measureMemory()` API status is now displayed under the **API availability** section.</span></span>  <span data-ttu-id="2b024-318">La nouvelle `performance.measureMemory()` API estime l’utilisation de la mémoire de la page web entière.</span><span class="sxs-lookup"><span data-stu-id="2b024-318">The new `performance.measureMemory()` API estimates the memory usage of the entire webpage.</span></span>  <span data-ttu-id="2b024-319">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="2b024-319">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Mesurer la mémoire" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   <span data-ttu-id="2b024-321">Mesurer la mémoire</span><span class="sxs-lookup"><span data-stu-id="2b024-321">Measure Memory</span></span>  
:::image-end:::  

### <span data-ttu-id="2b024-322">Images abandonnées dans l’outil Performances</span><span class="sxs-lookup"><span data-stu-id="2b024-322">Dropped frames in the Performance tool</span></span>  

<span data-ttu-id="2b024-323">Lorsque vous [analysez les performances de chargement dans l’outil Performance,][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]la section **Frames** marque désormais les images abandonnées en rouge.</span><span class="sxs-lookup"><span data-stu-id="2b024-323">When you [analyze load performance in the Performance tool][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], the **Frames** section now marks dropped frames as red.</span></span>  <span data-ttu-id="2b024-324">Pour afficher la fréquence d’images, pointez sur une image abandonnée.</span><span class="sxs-lookup"><span data-stu-id="2b024-324">To display the frame rate, hover on a dropped frame.</span></span>  <span data-ttu-id="2b024-325">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 1075865][CR1075865].</span><span class="sxs-lookup"><span data-stu-id="2b024-325">To review the history of this feature in the Chromium open-source project, navigate to Issue [1075865][CR1075865].</span></span>  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Cadres supprimés" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   <span data-ttu-id="2b024-327">Cadres supprimés</span><span class="sxs-lookup"><span data-stu-id="2b024-327">Dropped frames</span></span>  
:::image-end:::  

#### <span data-ttu-id="2b024-328">Nouveau calcul de contraste de couleur - Algorithme de contraste perceptif avancé (APCA)</span><span class="sxs-lookup"><span data-stu-id="2b024-328">New color contrast calculation - Advanced Perceptual Contrast Algorithm (APCA)</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="2b024-329">[L’algorithme de contraste perceptif avancé (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] remplace le coefficient de contraste des recommandations [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] dans le [s picker de couleur.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]</span><span class="sxs-lookup"><span data-stu-id="2b024-329">The [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] replaces the [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] guidelines contrast ratio in the [Color Picker][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span></span>  <span data-ttu-id="2b024-330">APCA est une nouvelle façon de calculer le contraste.</span><span class="sxs-lookup"><span data-stu-id="2b024-330">APCA is a new way to compute contrast.</span></span>  <span data-ttu-id="2b024-331">Il est basé sur des recherches modernes sur la perception des couleurs.</span><span class="sxs-lookup"><span data-stu-id="2b024-331">It is based on modern research on color perception.</span></span>  <span data-ttu-id="2b024-332">Par rapport aux directives AA/AAA, APCA dépend davantage du contexte.</span><span class="sxs-lookup"><span data-stu-id="2b024-332">Compared to AA/AAA guidelines, APCA is more context-dependent.</span></span>  <span data-ttu-id="2b024-333">Le contraste est calculé en fonction des propriétés spatiales suivantes du texte, de la couleur et du contexte.</span><span class="sxs-lookup"><span data-stu-id="2b024-333">The contrast is calculated based on the following spatial properties of the text, color, and context.</span></span>  

*   <span data-ttu-id="2b024-334">Propriétés spatiales du texte qui incluent le poids et la taille de la police.</span><span class="sxs-lookup"><span data-stu-id="2b024-334">Spatial properties of text that include font weight and size.</span></span>  
*   <span data-ttu-id="2b024-335">Propriétés spatiales de couleur qui incluent le contraste perçu entre le texte et l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="2b024-335">Spatial properties of color that include perceived contrast between text and background.</span></span>  
*   <span data-ttu-id="2b024-336">Propriétés spatiales du contexte qui incluent la lumière ambiante, l’environnement et l’objectif prévu.</span><span class="sxs-lookup"><span data-stu-id="2b024-336">Spatial properties of context that include ambient light, surroundings, and intended purpose.</span></span>  
    
<span data-ttu-id="2b024-337">Pour activer cette expérience, accédez à Expériences de paramètres et cochez la case en regard de Activer le nouvel algorithme de contraste perceptif avancé (APCA) en remplaçant le coefficient de contraste précédent et les [directives][DevtoolsCustomizeIndexSettings]  >  \*\*\*\* **AA/AAA.**</span><span class="sxs-lookup"><span data-stu-id="2b024-337">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable new Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.</span></span>  <span data-ttu-id="2b024-338">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1121900][CR1121900].</span><span class="sxs-lookup"><span data-stu-id="2b024-338">To review the history of this feature in the Chromium open-source project, navigate to Issue [1121900][CR1121900].</span></span>  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA dans le s picker de couleurs" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   <span data-ttu-id="2b024-340">APCA dans le s picker de couleurs</span><span class="sxs-lookup"><span data-stu-id="2b024-340">APCA in the Color Picker</span></span>  
:::image-end:::  

## <span data-ttu-id="2b024-341">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2b024-341">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="2b024-342">Si vous utilisez Windows, Linux ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2b024-342">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2b024-343">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2b024-343">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="2b024-344">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2b024-344">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Afficher le coefficient de contraste d’un élément de texte dans le s picker de couleurs - Référence d’accessibilité | Documents Microsoft"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Modifier la référence CSS - CSS | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans l'| Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Test sur les appareils pliables et à double écran : émuler les appareils à double écran et pliables dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une port d’affichage mobile : émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Performances de charge d’enregistrement : référence de l’analyse des performances | Documents Microsoft"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Documents Microsoft"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Présentation des outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment travailler avec le seam : introduction aux appareils à double écran | Documents Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité d’écran multimédia CSS pour la détection à double écran | Documents Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "L’API JavaScript getWindowSegments pour les appareils à double écran | Documents Microsoft"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Section 1 - Démonstration CSS :target pour les nouveautés de DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229 : mise en œuvre de la dropdown dans les paramètres pour modifier les thèmes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233 : inclure le débogger pour Microsoft Edge en tant que | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235 : mise à niveau de la version Edge DevTools vers 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248 : ajouter des boutons de fermeture unique au panneau instances | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Sélectionnez les caractéristiques de police et les couleurs d’arrière-plan pour fournir un contraste suffisant pour une | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Types d'| W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouveau modèle Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogger pour Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR978059]: https://crbug.com/978059 "Problème 978059 : suppression des cookies lors de leur filtrage, supprimez tous les cookies et pas seulement ceux filtrés | Bogues Chromium"  
[CR997625]: https://crbug.com/997625 "Problème 997625 : nouvelle fonctionnalité req | Option nécessaire pour afficher la valeur décodée url dans les cookies | Bogues Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problème 1003629 : le nœud de capture ne capture plus le nœud sous la pliage. | Bogues Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problème 1012337 : effacer les données de site détruit une session Google sur des sites autres que Google | Bogues Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problème 1028078 : Mettre en ligne et hors connexion les uns à côté des autres dans la liste | Bogues Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problème 1054281 : Demande de fonctionnalité : DevTools doit émuler les appareils pliables et à double écran | Bogues Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problème 1075865 : afficher les images abandonnées dans la chronologie des devtools | Bogues Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problème 1093229 : DevTools : offre une interface utilisateur d’éditeur de police spécialisée | Bogues Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problème 1121900 : DevTools : mettre à jour la logique de calcul du contraste par nouvelle spécification | Bogues Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problème 1122507: Informations sur le travailleur de surface dans l’affichage de l’arborescence de cadre | Bogues Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problème 1122580 : Impossible de désactiver l’enregistrement réseau lors du rechargement | Bogues Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problème 1136394: outils Flexbox | Bogues Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problème 1139899: Signaler la disponibilité des API contrôlées dans l’affichage des détails du cadre | Bogues Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problème 1139949 : superposition flexbox | Bogues Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problème 1147016 : le s sélectionneur de couleurs n’est pas affiché dans la fonction var(). | Bogues Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problème 1148353 : Demande de fonctionnalité : copier l’objet à partir de la console devtools | Bogues Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problème 1149859: [feature request][Console] add copy object to clipboard item to contextual menu | Bogues Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problème 1150797 : ajouter un menu contextif d’élément dupliqué dans le panneau d'| Bogues Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problème 1152391 : prise en charge de la copie du menu contextux CSS dans le panneau de styles | Bogues Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problème 1155120 : [FR]Nom du fichier de copie de support et numéro de ligne | Bogues Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problème 1156628 : DevTools : ajoutez la prise en charge de la fonctionnalité d’état d’élément :target en force | Bogues Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problème 1157329 : Accessibilité - Narrateur : le Narrateur n’annonce pas le nombre et la position des suggestions disponibles pour le code dans l’onglet Styles | Bogues Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "| Samsung (États-Unis)"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (amélioré) : comment répondre aux exigences WCAG (référence rapide) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (minimum) : comment répondre aux exigences WCAG (référence rapide) | W3C"  

> [!NOTE]
> <span data-ttu-id="2b024-399">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2b024-399">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2b024-400">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2021/01/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="2b024-400">The original page is found [here](https://developers.google.com/web/updates/2021/01/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2b024-402">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2b024-402">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Espace réservé couvrant"  
