---
description: Testez automatiquement une page web pour les problèmes d’accessibilité à l’aide de la section Accessibilité de l’outil Problèmes.
title: Tester automatiquement une page web pour les problèmes d’accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 986a021d2fd390cd45bd53dcfc37a83d58ed2338
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597334"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a><span data-ttu-id="54292-104">Tester automatiquement une page web pour les problèmes d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="54292-104">Automatically test a webpage for accessibility issues</span></span>

<span data-ttu-id="54292-105">**L’outil** Problèmes inclut une **section** Accessibilité qui signale automatiquement des problèmes tels que l’absence de texte de remplacement sur les images, l’absence d’étiquettes dans les champs du formulaire et le contraste insuffisant des couleurs du texte.</span><span class="sxs-lookup"><span data-stu-id="54292-105">The **Issues** tool includes an **Accessibility** section that automatically reports issues such as missing alternative text on images, missing labels on form fields, and insufficient contrast of text colors.</span></span>  <span data-ttu-id="54292-106">**L’outil Problèmes** se trouve dans le **caisse** en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-106">The **Issues** tool is within the **Drawer** at the bottom of DevTools.</span></span>  <span data-ttu-id="54292-107">Cet article utilise la page web de démonstration des tests d’accessibilité pour passer pas à pas à l’aide de la section **Accessibilité** de **l’outil** Problèmes.</span><span class="sxs-lookup"><span data-stu-id="54292-107">This article uses the accessibility-testing demo webpage to step through using the **Accessibility** section of the **Issues** tool.</span></span>

<span data-ttu-id="54292-108">Il existe plusieurs façons d’ouvrir **l’outil Problèmes, telles** que :</span><span class="sxs-lookup"><span data-stu-id="54292-108">There are several ways to open the **Issues** tool, such as:</span></span>
*  <span data-ttu-id="54292-109">Sélectionnez **le compteur Problèmes** \( Compteur de problèmes \) dans le coin supérieur droit de ![ ](../media/issues-counter-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-109">Select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) in the upper right of DevTools.</span></span>
*  <span data-ttu-id="54292-110">Dans **l’outil Elements,** dans l’arborescence DOM, **cliquez** sur un soulignement ondulé sur un élément.</span><span class="sxs-lookup"><span data-stu-id="54292-110">In the **Elements** tool, in the DOM tree, **Shift+click** a wavy underline on an element.</span></span>
*  <span data-ttu-id="54292-111">Dans le **menu Commande,** `issues` tapez, puis sélectionnez **Afficher les problèmes.**</span><span class="sxs-lookup"><span data-stu-id="54292-111">In the **Command Menu**, type `issues`, and then select **Show Issues**.</span></span>


## <a name="view-the-accessibility-section-of-the-issues-tool"></a><span data-ttu-id="54292-112">Afficher la section Accessibilité de l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="54292-112">View the Accessibility section of the Issues tool</span></span>

1.  <span data-ttu-id="54292-113">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>  <span data-ttu-id="54292-114">Dans le coin supérieur droit, le compteur Problèmes **\(** Compteur de problèmes \) apparaît sous la forme d’une icône de bulle vocale avec le nombre de problèmes ![ ](../media/issues-counter-icon.msft.png) détectés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="54292-114">In the upper right, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, as a speech-bubble icon along with the number of automatically detected issues.</span></span>  <span data-ttu-id="54292-115">Un autre numéro peut apparaître dans votre navigateur et le numéro peut être mis à jour lorsque vous utilisez DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-115">A different number might appear in your browser, and the number might update as you use DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="Compteur Problèmes dans DevTools, indiquant le nombre de problèmes présents dans le document actuel" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        <span data-ttu-id="54292-117">Compteur **Problèmes dans** DevTools, indiquant le nombre de problèmes présents dans le document actuel</span><span class="sxs-lookup"><span data-stu-id="54292-117">The **Issues counter** in DevTools, indicating how many problems there are in the current document</span></span>
    :::image-end:::

1.  <span data-ttu-id="54292-118">Sélectionnez **le compteur Problèmes.**</span><span class="sxs-lookup"><span data-stu-id="54292-118">Select the **Issues counter**.</span></span>  <span data-ttu-id="54292-119">**L’outil** Problèmes s’ouvre, dans le **caisse** en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-119">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Avertissements d’accessibilité affichés dans l’outil Problèmes" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        <span data-ttu-id="54292-121">Avertissements d’accessibilité affichés dans l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="54292-121">Accessibility warnings displayed in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="54292-122">Sous **l’onglet Problèmes,** développez la section **Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="54292-122">On the **Issues** tab, expand the **Accessibility** section.</span></span>


## <a name="verify-that-input-fields-have-labels"></a><span data-ttu-id="54292-123">Vérifier que les champs d’entrée ont des étiquettes</span><span class="sxs-lookup"><span data-stu-id="54292-123">Verify that input fields have labels</span></span>

<span data-ttu-id="54292-124">Pour vérifier si des étiquettes sont **connectées** aux champs d’entrée, utilisez l’outil Problèmes, qui vérifie automatiquement l’intégralité de la page web et signale ce problème dans la **section** Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="54292-124">To check whether input fields have labels connected to them, use the **Issues** tool, which automatically checks the entire webpage and reports this issue in the **Accessibility** section.</span></span>

1.  <span data-ttu-id="54292-125">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-125">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="54292-126">Dans le coin supérieur droit, sélectionnez le compteur **Problèmes** \( ![ Compteur de problèmes ](../media/issues-counter-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="54292-126">In the upper right, select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>  <span data-ttu-id="54292-127">**L’outil** Problèmes s’ouvre, dans le **caisse** en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-127">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="54292-128">Sous **l’onglet Problèmes,** développez la section **Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="54292-128">On the **Issues** tab, expand the **Accessibility** section.</span></span>

1.  <span data-ttu-id="54292-129">Développez **l’avertissement** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .</span><span class="sxs-lookup"><span data-stu-id="54292-129">Expand the **Warning** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute`.</span></span>

1. <span data-ttu-id="54292-130">Sélectionnez **le lien Ouvrir dans les éléments.**</span><span class="sxs-lookup"><span data-stu-id="54292-130">Select the **Open in Elements** link.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Outil Éléments affichant le code HTML problématique après la sélection du lien dans l’outil Problèmes" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        <span data-ttu-id="54292-132">Outil Éléments affichant le code HTML problématique après la sélection du lien dans **l’outil** Problèmes</span><span class="sxs-lookup"><span data-stu-id="54292-132">Elements tool showing the problematic HTML after selecting the link in the **Issues** tool</span></span> :::image-end:::

    <span data-ttu-id="54292-133">**L’outil Elements** s’ouvre, avec l’élément mis en surbrillant dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="54292-133">The **Elements** tool opens, with the element highlighted in the DOM tree.</span></span>  <span data-ttu-id="54292-134">Le **volet Styles** affiche les règles CSS appliquées pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="54292-134">The **Styles** pane displays the applied CSS rules for the element.</span></span>  <span data-ttu-id="54292-135">Le code suivant s’affiche maintenant.</span><span class="sxs-lookup"><span data-stu-id="54292-135">The following code is now displayed.</span></span>

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    <span data-ttu-id="54292-136">Dans le code ci-dessus, l’élément est utilisé de manière incorrecte, car il n’existe aucune connexion entre l’élément `label` `label` et un élément `input` particulier.</span><span class="sxs-lookup"><span data-stu-id="54292-136">In the above code, the `label` element is used incorrectly, because there is no connection between the `label` element and a particular `input` element.</span></span>  <span data-ttu-id="54292-137">Pour connecter `label` l’élément à un élément `input` spécifique, utilisez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="54292-137">To connect the `label` element to a specific `input` element, use any of the following options.</span></span>
    *   <span data-ttu-id="54292-138">Imbribrier `input` l’élément dans `label` l’élément.</span><span class="sxs-lookup"><span data-stu-id="54292-138">Nest the `input` element within the `label` element.</span></span>
    *   <span data-ttu-id="54292-139">Dans `label` l’élément, ajoutez `for` un attribut qui correspond à un attribut de `id` `input` l’élément.</span><span class="sxs-lookup"><span data-stu-id="54292-139">In the `label` element, add a `for` attribute that matches an `id` attribute of the `input` element.</span></span>

    <span data-ttu-id="54292-140">Il existe également une autre façon de tester l’absence de connexions entre les éléments.</span><span class="sxs-lookup"><span data-stu-id="54292-140">There's also another way to test for lack of connections between elements.</span></span> <span data-ttu-id="54292-141">Dans **l’outil Elements,** sélectionnez `<label>Search</label>` l’élément dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="54292-141">In the **Elements** tool, select the `<label>Search</label>` element in the DOM tree.</span></span>  <span data-ttu-id="54292-142">Sur la page web, notez que le focus apparaît uniquement sur l’étiquette **de** recherche, et non sur la zone de texte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="54292-142">On the webpage, notice that focus only appears on the **Search** label, and not the input textbox.</span></span>  <span data-ttu-id="54292-143">L’implémentation correcte met le focus sur la zone `search` de texte d’entrée et **l’étiquette** de recherche.</span><span class="sxs-lookup"><span data-stu-id="54292-143">The correct implementation would put focus on the `search` input textbox and the **Search** label.</span></span>

1.  <span data-ttu-id="54292-144">Comme exemple de connexion correcte, sélectionnez **l’étiquette Other** dans le formulaire de don.</span><span class="sxs-lookup"><span data-stu-id="54292-144">As an example of a correct connection, select the **Other** label on the donation form.</span></span>  <span data-ttu-id="54292-145">Une zone d’indicateur de focus s’affiche correctement dans la zone de texte d’entrée à côté de l’étiquette **Autre,** car il existe des valeurs de correspondance et `for` `id` d’attribut.</span><span class="sxs-lookup"><span data-stu-id="54292-145">A focus-indicator box correctly appears on the input textbox next to the **Other** label, because there are matching `for` and `id` attribute values.</span></span>

1.  <span data-ttu-id="54292-146">Dans **l’outil Problèmes,** sélectionnez **Lecture supplémentaire** pour en savoir plus sur le problème.</span><span class="sxs-lookup"><span data-stu-id="54292-146">In the **Issues tool**, select **Further reading** to learn more about the issue.</span></span>  <span data-ttu-id="54292-147">Pour ouvrir le lien dans un nouvel onglet, **Ctrl**cliquez sur le lien sur Windows/Linux, ou commande cliquez sur le lien + \*\*\*\* \*\*\*\* + \*\*\*\* sur macOS.</span><span class="sxs-lookup"><span data-stu-id="54292-147">To open the link in a new tab, **Ctrl**+**click** the link on Windows/Linux, or **Command**+**click** the link on macOS.</span></span>

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Lien sous l’onglet Problèmes pointant vers des informations plus détaillées sur le problème" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        <span data-ttu-id="54292-149">Lien sous **l’onglet Problèmes** pointant vers des informations plus détaillées sur le problème</span><span class="sxs-lookup"><span data-stu-id="54292-149">Link on the **Issues** tab pointing to more in-depth information about the issue</span></span>
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a><span data-ttu-id="54292-150">Vérifier que les images ont un texte de alt</span><span class="sxs-lookup"><span data-stu-id="54292-150">Verify that images have alt text</span></span>

<span data-ttu-id="54292-151">Le test d’accessibilité de base nécessite de s’assurer que du texte de remplacement (également appelé _texte_de remplacement) est fourni pour les images.</span><span class="sxs-lookup"><span data-stu-id="54292-151">Basic accessibility testing requires making sure alternative text (also called _alt text_) is provided for images.</span></span>

<span data-ttu-id="54292-152">Pour vérifier automatiquement si un texte de alt est fourni pour les images, utilisez l’outil **Problèmes,** qui contient une section **Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="54292-152">To automatically check whether alt text is provided for images, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="54292-153">**L’outil Problèmes** se trouve dans le **caisse** en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-153">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="54292-154">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-154">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="54292-155">Pour ouvrir **l’outil Problèmes,** sélectionnez le compteur **Problèmes** dans le coin supérieur droit de DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-155">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>

1.  <span data-ttu-id="54292-156">Sous **l’onglet Problèmes,** développez `Images must have alternate text: Element has no title attribute` l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="54292-156">On the **Issues** tab, expand the warning `Images must have alternate text: Element has no title attribute`.</span></span>  <span data-ttu-id="54292-157">Il existe quatre instances d’images qui n’ont pas de texte de alt.</span><span class="sxs-lookup"><span data-stu-id="54292-157">There are four instances of images that lack alt text.</span></span>

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="L’outil Problèmes signalant des images qui ne manquent pas de texte de remplacement" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        <span data-ttu-id="54292-159">L’outil Problèmes signalant des images qui ne manquent pas de texte de remplacement</span><span class="sxs-lookup"><span data-stu-id="54292-159">The Issues tool reporting images that are missing alternative text</span></span>
    :::image-end:::

<span data-ttu-id="54292-160">Pour plus d’informations, [accédez à Images qui doivent avoir un texte de remplacement.](https://dequeuniversity.com/rules/axe/4.1/image-alt)</span><span class="sxs-lookup"><span data-stu-id="54292-160">For more information, navigate to [Images must have alternate text](https://dequeuniversity.com/rules/axe/4.1/image-alt).</span></span>


## <a name="verify-that-text-colors-have-enough-contrast"></a><span data-ttu-id="54292-161">Vérifier que le contraste des couleurs du texte est suffisant</span><span class="sxs-lookup"><span data-stu-id="54292-161">Verify that text colors have enough contrast</span></span>

<span data-ttu-id="54292-162">Pour vérifier automatiquement si les couleurs de texte ont un contraste suffisant, utilisez l’outil **Problèmes,** qui possède une section **Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="54292-162">To automatically check whether text colors have enough contrast, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="54292-163">**L’outil Problèmes** se trouve dans le **caisse** en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-163">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="54292-164">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-164">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="54292-165">Pour ouvrir **l’outil Problèmes,** sélectionnez le compteur **Problèmes** dans le coin supérieur droit de DevTools.</span><span class="sxs-lookup"><span data-stu-id="54292-165">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>  <span data-ttu-id="54292-166">Vous pouvez recevoir des avertissements signalant que deux éléments de la page web de démonstration ne sont pas assez contrastés.</span><span class="sxs-lookup"><span data-stu-id="54292-166">You may receive warnings that two elements on the demo webpage don't have enough contrast.</span></span>

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problèmes de contraste signalés dans l’outil Problèmes" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        <span data-ttu-id="54292-168">Problèmes de contraste signalés dans l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="54292-168">Contrast problems reported in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="54292-169">En fonction de vos paramètres, l’onglet Problèmes peut avoir un avertissement, car les **utilisateurs** peuvent avoir des difficultés à lire le contenu du texte en raison d’un **contraste de couleur insuffisant.**</span><span class="sxs-lookup"><span data-stu-id="54292-169">Depending on your settings, the **Issues** tab might have a warning like **Users may have difficulties reading text content due to insufficient color contrast**.</span></span>   <span data-ttu-id="54292-170">Vous pouvez développer cet avertissement, puis développer les **ressources affectées.**</span><span class="sxs-lookup"><span data-stu-id="54292-170">You can expand that warning, and then expand **Affected resources**.</span></span>  <span data-ttu-id="54292-171">Une liste d’éléments apparaît avec une liste d’éléments qui n’ont pas assez de contraste.</span><span class="sxs-lookup"><span data-stu-id="54292-171">A list of elements appears with a list of elements that don't have enough contrast.</span></span>


1.  <span data-ttu-id="54292-172">Sélectionnez `li.high` l’élément.</span><span class="sxs-lookup"><span data-stu-id="54292-172">Select the `li.high` element.</span></span>  <span data-ttu-id="54292-173">Dans la page web rendue, le lien **Chiens** de la section **Tronçon** est mis en surbrillence, affichant une petite superposition d’informations.</span><span class="sxs-lookup"><span data-stu-id="54292-173">In the rendered webpage, the **Dogs** link in the **Donate** section is highlighted, displaying a small information overlay.</span></span>  <span data-ttu-id="54292-174">Il s’agit de la même superposition qui s’affiche lorsque vous pointez sur un élément dans l’arborescence DOM de **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="54292-174">This is the same overlay that appears when you hover over an element in the DOM tree in the **Elements** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Élément de la page web mis en évidence après la sélection d’un lien dans la section Ressources affectées" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        <span data-ttu-id="54292-176">Élément de la page web mis en évidence après la sélection d’un lien dans la section **Ressources** affectées</span><span class="sxs-lookup"><span data-stu-id="54292-176">Element in the webpage highlighted after selecting a link in the **Affected Resources** section</span></span>
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a><span data-ttu-id="54292-177">Les soulignements ondulés dans l’arborescence DOM indiquent des problèmes détectés automatiquement</span><span class="sxs-lookup"><span data-stu-id="54292-177">Wavy underlines in the DOM tree indicate automatically detected issues</span></span> 

<span data-ttu-id="54292-178">L’arborescence DOM de l’outil **Éléments** indicateur les problèmes directement dans le code HTML avec des soulignements ondulés.</span><span class="sxs-lookup"><span data-stu-id="54292-178">The DOM tree in the **Elements** tool flags issues directly in the HTML with wavy underlines.</span></span>  <span data-ttu-id="54292-179">Ces problèmes sont signalés par **l’outil Problèmes.**</span><span class="sxs-lookup"><span data-stu-id="54292-179">These issues are reported by the **Issues** tool.</span></span>  <span data-ttu-id="54292-180">Lorsque vous cliquez sur Un élément avec un soulignement **ondulé,** l’outil Problèmes \*\*\*\* s’affiche.</span><span class="sxs-lookup"><span data-stu-id="54292-180">When you **Shift+click** any element with a wavy underline, the **Issues tool** is displayed.</span></span>

1.  <span data-ttu-id="54292-181">Dans **l’outil Elements,** dans l’arborescence DOM, **Shift+cliquez** sur l’élément, qui a une ligne ondulée sous `<input type="search">` `input` .</span><span class="sxs-lookup"><span data-stu-id="54292-181">In the **Elements** tool, in the DOM tree, **Shift+click** the element `<input type="search">`, which has a wavy line under `input`.</span></span>  <span data-ttu-id="54292-182">**L’outil Problèmes s’affiche** et indique le problème pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="54292-182">The **Issues tool** is displayed, and shows the issue for that element.</span></span>

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Un élément avec un soulignement ondulé dans l’affichage DOM présente un problème" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        <span data-ttu-id="54292-184">Un élément avec un soulignement ondulé dans l’affichage DOM présente un problème</span><span class="sxs-lookup"><span data-stu-id="54292-184">An element that has a wavy underline in the DOM view has an issue</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="54292-185">Articles associés</span><span class="sxs-lookup"><span data-stu-id="54292-185">See also</span></span>

*  [<span data-ttu-id="54292-186">Rechercher et résoudre les problèmes liés à Microsoft Edge’outil Problèmes de DevTools</span><span class="sxs-lookup"><span data-stu-id="54292-186">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>][DevToolsIssuesTool]
*  [<span data-ttu-id="54292-187">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="54292-187">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="54292-188">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="54292-188">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
