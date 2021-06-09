---
description: Analyse de l’absence de prise en charge du clavier sur un formulaire qui utilise l’élément div avec l’outil Inspect et l’onglet Écouteurs d’événements.
title: Analyser la prise en charge du clavier sur les formulaires à l’aide de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 16ec030ed433fc24d3b2b88bfb423a2479996dfe
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597372"
---
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a><span data-ttu-id="5115f-104">Analyser la prise en charge du clavier sur les formulaires à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="5115f-104">Analyze keyboard support on forms using the DevTools</span></span>

<span data-ttu-id="5115f-105">Cet article utilise **l’outil Inspect** et l’onglet **Écouteurs** d’événements pour analyser l’absence de prise en charge du clavier sur une page de démonstration qui possède des boutons qui utilisent l’élément. `div`</span><span class="sxs-lookup"><span data-stu-id="5115f-105">This article uses the **Inspect** tool and **Event Listeners** tab to analyze the lack of keyboard support on a demo page which has buttons that use the `div` element.</span></span>

<span data-ttu-id="5115f-106">Sur le **formulaire Dente,** les boutons Montant et **Bouton Dente** ne fonctionnent pas avec un clavier.</span><span class="sxs-lookup"><span data-stu-id="5115f-106">On the **Donate** form, the amount buttons and **Donate** button doesn't work with a keyboard.</span></span>  <span data-ttu-id="5115f-107">Le débogage du formulaire de don nécessite de comprendre pourquoi le manque de style de mise au point n’est pas signalé comme un problème avec les outils de test automatique tels que **l’outil Problèmes.**</span><span class="sxs-lookup"><span data-stu-id="5115f-107">Debugging the donation form requires understanding why the lack of focus styling isn't flagged as a problem with automatic testing tools like the **Issues** tool.</span></span>  <span data-ttu-id="5115f-108">Dans cet exemple, les boutons sont implémentés à l’aide d’éléments qui ne sont pas reconnus par ces outils en tant que `div` contrôles sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="5115f-108">In this example, the buttons are implemented using `div` elements, which are not recognized by these tools as a control on a form.</span></span>

<span data-ttu-id="5115f-109">Pour utiliser l’outil Inspect et l’onglet Écouteurs d’événements pour analyser l’absence de prise en charge du clavier sur la page de démonstration :</span><span class="sxs-lookup"><span data-stu-id="5115f-109">To use the Inspect tool and Event Listeners tab to analyze the lack of keyboard support on the demo page:</span></span>

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  <span data-ttu-id="5115f-110">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="5115f-110">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>
    
1.  <span data-ttu-id="5115f-111">Sélectionnez **le bouton Inspect** \( Inspect icon \) dans le coin supérieur gauche de DevTools afin que le bouton soit mis en ![ ](../media/inspect-icon.msft.png) surbrillant (bleu).</span><span class="sxs-lookup"><span data-stu-id="5115f-111">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="5115f-112">Pointez sur **les boutons 50,** **100**et **200** dons.</span><span class="sxs-lookup"><span data-stu-id="5115f-112">Hover over the **50**, **100**, and **200** donation buttons.</span></span>  <span data-ttu-id="5115f-113">L’outil Inspect s’affiche sur la page web, sous la mesure d’une superposition.</span><span class="sxs-lookup"><span data-stu-id="5115f-113">The Inspect tool appears on the webpage, as an overlay.</span></span>  <span data-ttu-id="5115f-114">La ligne clavier **focusable** de la superposition Inspect indique qu’aucun des boutons de don n’est accessible au clavier, comme indiqué par un cercle gris avec une ligne diagonale.</span><span class="sxs-lookup"><span data-stu-id="5115f-114">The **keyboard-focusable** row of the Inspect overlay shows that none of the donation amount buttons are keyboard-accessible, as indicated by a gray circle with diagonal line.</span></span>  <span data-ttu-id="5115f-115">Les boutons n’ont pas de nom et ont un rôle car il `generic` s’agit d’éléments, ce qui signifie que les boutons ne sont pas accessibles à la `div` technologie d’assistance.</span><span class="sxs-lookup"><span data-stu-id="5115f-115">The buttons have no name, and have a role of `generic` because they are `div` elements, which means that the buttons aren't accessible to assistive technology.</span></span>

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="L’inspection des boutons du formulaire indique qu’ils ne sont pas accessibles au clavier" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        <span data-ttu-id="5115f-117">L’inspection des boutons du formulaire indique qu’ils ne sont pas accessibles au clavier</span><span class="sxs-lookup"><span data-stu-id="5115f-117">Inspecting the buttons of the form shows that they aren't keyboard-accessible</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="5115f-118">Lorsque **l’outil Inspect** est actif, sur la page web, sélectionnez la boîte de texte d’entrée **Autre,** au-dessus du **bouton Bouton Dente.**</span><span class="sxs-lookup"><span data-stu-id="5115f-118">When the **Inspect** tool is active, on the webpage, select the **Other** input textbox, above the **Donate** button.</span></span>  <span data-ttu-id="5115f-119">**L’outil Elements** s’ouvre, affichant l’arborescence DOM de la page web.</span><span class="sxs-lookup"><span data-stu-id="5115f-119">The **Elements** tool opens, showing the DOM tree for the webpage.</span></span>  <span data-ttu-id="5115f-120">`<input id="freedonation" class="smallinput">`L’élément est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5115f-120">The element `<input id="freedonation" class="smallinput">` is selected.</span></span>

    ```html
    <div class="donationrow">
        <div class="donationbutton">50</div>
        <div class="donationbutton">100</div>
        <div class="donationbutton">200</div>
    </div>
    <div class="donationrow">
        <label for="freedonation">Other</label>
        <input id="freedonation" class="smallinput">
    </div>
    <div class="donationrow">
        <div class="submitbutton">Donate</div>
    </div>
    ```

    <span data-ttu-id="5115f-121">L’utilisation des éléments dans la boîte de texte Autre est valide, ce qui signifie que l’étiquette Autre est correctement liée à la boîte de `label` `input` texte d’entrée. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5115f-121">The use of the `label` and `input` elements on the **Other** textbox is valid, which means that the **Other** label is correctly linked with the input textbox.</span></span>  <span data-ttu-id="5115f-122">La `input` boîte de texte est également accessible au clavier.</span><span class="sxs-lookup"><span data-stu-id="5115f-122">The `input` textbox is also keyboard-accessible.</span></span>  <span data-ttu-id="5115f-123">Le reste du markup du formulaire est un élément facile à mettre en forme, mais sans signification `div` sémantique.</span><span class="sxs-lookup"><span data-stu-id="5115f-123">The rest of the form's markup are `div` elements, which are easy to style, but have no semantic meaning.</span></span>

    <!-- 2. Elements tool: Event Listeners tab -->

    <span data-ttu-id="5115f-124">La fonctionnalité du formulaire est créée avec JavaScript et vous \*\*\*\* pouvez la tester en vérifiant l’onglet Écouteurs d’événements, comme suit.</span><span class="sxs-lookup"><span data-stu-id="5115f-124">The form's functionality is created with JavaScript, and you can test this by checking the **Event Listeners** tab, as follows.</span></span>

1.  <span data-ttu-id="5115f-125">Avec l’élément toujours sélectionné dans l’arborescence DOM, sélectionnez l’onglet Écouteurs d’événements à droite de l’onglet Styles, puis développez l’écouteur `<input id="freedonation" class="smallinput">` \*\*\*\* \*\*\*\* `click` d’événements.</span><span class="sxs-lookup"><span data-stu-id="5115f-125">With the element `<input id="freedonation" class="smallinput">` still selected in the DOM tree, select the **Event Listeners** tab to the right of the **Styles** tab, and then expand the `click` event listener.</span></span>

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="L’outil d’écouteurs d’événements qui vous montre où se trouve JavaScript pour faire fonctionner le formulaire" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        <span data-ttu-id="5115f-127">L’outil d’écouteurs d’événements qui vous montre où se trouve JavaScript pour faire fonctionner le formulaire</span><span class="sxs-lookup"><span data-stu-id="5115f-127">The Event listeners tool showing you where the JavaScript is that makes the form work</span></span>
    :::image-end:::

1.  <span data-ttu-id="5115f-128">Sélectionnez le `buttons.js:18` lien.</span><span class="sxs-lookup"><span data-stu-id="5115f-128">Select the `buttons.js:18` link.</span></span>  <span data-ttu-id="5115f-129">**L’outil Sources** s’ouvre, affichant le JavaScript appliqué.</span><span class="sxs-lookup"><span data-stu-id="5115f-129">The **Sources** tool opens, showing the applied JavaScript.</span></span>

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="JavaScript responsable de la fonctionnalité du formulaire de don, présentée dans l’outil Sources" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        <span data-ttu-id="5115f-131">JavaScript responsable de la fonctionnalité du formulaire de don, présentée dans l’outil Sources</span><span class="sxs-lookup"><span data-stu-id="5115f-131">The JavaScript responsible for the donation form's functionality, shown in the Sources tool</span></span>
    :::image-end:::

```javascript
donations.addEventListener('click', e => {
  let t = e.target;
  if (t.classList.contains('donationbutton')) {
    if (currentbutton) { currentbutton.classList.remove('current'); }
    t.classList.add('current');
    currentbutton = t;
    e.preventDefault();
  }
  if (t.classList.contains('submitbutton')) {
    alert('Thanks for your donation!')
  } 
})
```

<span data-ttu-id="5115f-132">L’utilisation d’un événement pour lire les boutons est une bonne pratique, car un événement se déclenche à la fois lors de l’interaction avec le pointeur de la `click` `click` souris et le clavier.</span><span class="sxs-lookup"><span data-stu-id="5115f-132">Using a `click` event to read the buttons is good practice, because a `click` event fires both on mouse pointer and keyboard interaction.</span></span>  <span data-ttu-id="5115f-133">Toutefois, étant donné qu’un élément n’est pas accessible au clavier et que ce bouton Dente est implémenté en tant qu’élément ( ), cette fonctionnalité JavaScript ne s’exécute jamais, sauf si vous utilisez une souris ou une autre source d’événement, par exemple un bouton spécial disponible sur certains `div` \*\*\*\* `div` `<div class="submitbutton">Donate</div>` `click` claviers.</span><span class="sxs-lookup"><span data-stu-id="5115f-133">However, because a `div` element isn't keyboard-accessible, and this **Donate** button is implemented as a `div` element (`<div class="submitbutton">Donate</div>`), this JavaScript functionality never runs unless you use a mouse or another source of a `click` event, such as a special button available on some keyboards.</span></span>

<span data-ttu-id="5115f-134">Il s’agit d’un exemple classique dans lequel JavaScript a été ajouté pour créer des fonctionnalités fournies en mode natif par `button` les éléments.</span><span class="sxs-lookup"><span data-stu-id="5115f-134">This is a classic example where JavaScript was added to create functionality that `button` elements provide natively.</span></span>  <span data-ttu-id="5115f-135">La simulation de la fonctionnalité des boutons avec des éléments a fini par `div` produire une expérience inaccessible.</span><span class="sxs-lookup"><span data-stu-id="5115f-135">Simulating the functionality of buttons with `div` elements ended up producing an inaccessible experience.</span></span>


## <a name="see-also"></a><span data-ttu-id="5115f-136">Articles associés</span><span class="sxs-lookup"><span data-stu-id="5115f-136">See also</span></span>

*  [<span data-ttu-id="5115f-137">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="5115f-137">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5115f-138">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="5115f-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
