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
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a>Analyser la prise en charge du clavier sur les formulaires à l’aide de DevTools

Cet article utilise **l’outil Inspect** et l’onglet **Écouteurs** d’événements pour analyser l’absence de prise en charge du clavier sur une page de démonstration qui possède des boutons qui utilisent l’élément. `div`

Sur le **formulaire Dente,** les boutons Montant et **Bouton Dente** ne fonctionnent pas avec un clavier.  Le débogage du formulaire de don nécessite de comprendre pourquoi le manque de style de mise au point n’est pas signalé comme un problème avec les outils de test automatique tels que **l’outil Problèmes.**  Dans cet exemple, les boutons sont implémentés à l’aide d’éléments qui ne sont pas reconnus par ces outils en tant que `div` contrôles sur un formulaire.

Pour utiliser l’outil Inspect et l’onglet Écouteurs d’événements pour analyser l’absence de prise en charge du clavier sur la page de démonstration :

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.
    
1.  Sélectionnez **le bouton Inspect** \( Inspect icon \) dans le coin supérieur gauche de DevTools afin que le bouton soit mis en ![ ](../media/inspect-icon.msft.png) surbrillant (bleu).

1.  Pointez sur **les boutons 50,** **100**et **200** dons.  L’outil Inspect s’affiche sur la page web, sous la mesure d’une superposition.  La ligne clavier **focusable** de la superposition Inspect indique qu’aucun des boutons de don n’est accessible au clavier, comme indiqué par un cercle gris avec une ligne diagonale.  Les boutons n’ont pas de nom et ont un rôle car il `generic` s’agit d’éléments, ce qui signifie que les boutons ne sont pas accessibles à la `div` technologie d’assistance.

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="L’inspection des boutons du formulaire indique qu’ils ne sont pas accessibles au clavier" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        L’inspection des boutons du formulaire indique qu’ils ne sont pas accessibles au clavier
    :::image-end:::
    
1.  Lorsque **l’outil Inspect** est actif, sur la page web, sélectionnez la boîte de texte d’entrée **Autre,** au-dessus du **bouton Bouton Dente.**  **L’outil Elements** s’ouvre, affichant l’arborescence DOM de la page web.  `<input id="freedonation" class="smallinput">`L’élément est sélectionné.

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

    L’utilisation des éléments dans la boîte de texte Autre est valide, ce qui signifie que l’étiquette Autre est correctement liée à la boîte de `label` `input` texte d’entrée. **** ****  La `input` boîte de texte est également accessible au clavier.  Le reste du markup du formulaire est un élément facile à mettre en forme, mais sans signification `div` sémantique.

    <!-- 2. Elements tool: Event Listeners tab -->

    La fonctionnalité du formulaire est créée avec JavaScript et vous **** pouvez la tester en vérifiant l’onglet Écouteurs d’événements, comme suit.

1.  Avec l’élément toujours sélectionné dans l’arborescence DOM, sélectionnez l’onglet Écouteurs d’événements à droite de l’onglet Styles, puis développez l’écouteur `<input id="freedonation" class="smallinput">` **** **** `click` d’événements.

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="L’outil d’écouteurs d’événements qui vous montre où se trouve JavaScript pour faire fonctionner le formulaire" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        L’outil d’écouteurs d’événements qui vous montre où se trouve JavaScript pour faire fonctionner le formulaire
    :::image-end:::

1.  Sélectionnez le `buttons.js:18` lien.  **L’outil Sources** s’ouvre, affichant le JavaScript appliqué.

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="JavaScript responsable de la fonctionnalité du formulaire de don, présentée dans l’outil Sources" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        JavaScript responsable de la fonctionnalité du formulaire de don, présentée dans l’outil Sources
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

L’utilisation d’un événement pour lire les boutons est une bonne pratique, car un événement se déclenche à la fois lors de l’interaction avec le pointeur de la `click` `click` souris et le clavier.  Toutefois, étant donné qu’un élément n’est pas accessible au clavier et que ce bouton Dente est implémenté en tant qu’élément ( ), cette fonctionnalité JavaScript ne s’exécute jamais, sauf si vous utilisez une souris ou une autre source d’événement, par exemple un bouton spécial disponible sur certains `div` **** `div` `<div class="submitbutton">Donate</div>` `click` claviers.

Il s’agit d’un exemple classique dans lequel JavaScript a été ajouté pour créer des fonctionnalités fournies en mode natif par `button` les éléments.  La simulation de la fonctionnalité des boutons avec des éléments a fini par `div` produire une expérience inaccessible.


## <a name="see-also"></a>Articles associés

*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
