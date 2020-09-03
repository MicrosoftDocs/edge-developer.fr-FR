---
description: Découvrez comment évaluer les performances d’exécution dans Microsoft Edge DevTools.
title: Commencer à analyser les performances de l’exécution
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 65351f3846ed76ef8a27dbff2cfb08c497282d15
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992945"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Commencer à analyser les performances de l’exécution  

> [!NOTE]
> Pour plus d’informations sur le chargement plus rapide de vos pages, voir [optimiser la vitesse du site Web][DevtoolsSpeedGetStarted].  

La performance du runtime correspond à la façon dont votre page s’exécute lorsque celle-ci est en cours d’exécution.  L’article suivant explique comment utiliser le panneau performances de Microsoft Edge DevTools pour analyser les performances de l’exécution.  En ce qui concerne le modèle **ferroviaire** , les compétences que vous apprenez dans ce didacticiel sont utiles pour analyser les phases de réponse, d’animation et d’inactivité de votre page.  

<!--todo: add rail link when section is ready -->  

## Prise en main  

Dans le didacticiel suivant, vous pouvez ouvrir DevTools sur une page en direct et utiliser le volet **performance** pour trouver un goulet d’étranglement de performance dans la page.  

1.  Ouvrez Microsoft Edge en **mode InPrivate**.  Le mode InPrivate vérifie que Microsoft Edge s’exécute dans un état propre.  Par exemple, si de nombreuses extensions sont installées, les extensions peuvent créer un bruit dans vos mesures de performance.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Chargez la page suivante dans votre fenêtre InPrivate.  Il s’agit de la démonstration que vous allez Profiler.  La page affiche un grand nombre d’icônes déplacées vers le haut et vers le bas.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Sélectionnez `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \) pour ouvrir devtools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       La démonstration à gauche et DevTools sur la droite  
    :::image-end:::  
    
    > [!NOTE]
    > Pour les autres figures, DevTools est ancré dans [une fenêtre séparée][DevtoolsCustomizePlacement] pour mieux vous concentrer sur le contenu.  
    
### Simuler une UC mobile  

Les appareils mobiles disposent d’une puissance UC plus réduite que les ordinateurs de bureau et les ordinateurs portables.  Dès lors que vous profilez une page, utilisez la limitation de l’UC pour simuler l’exécution de votre page sur les appareils mobiles.  

1.  Dans DevTools, sélectionnez l’onglet **performances** .  
1.  Vérifiez que la case à cocher **captures d’écran** est activée.  
1.  Choisir les **paramètres de capture** Paramètres de capture] [ImageCaptureSettingsIcon] \).  DevTools révèle les paramètres liés à la manière dont il capture les métriques de performances.  
1.  Pour **processeur**, sélectionnez **4x Slowdown**.  DevTools limite votre processeur de sorte qu’il soit 4 fois plus lent que d’habitude.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Accélérateur d’UC" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Accélérateur d’UC  
    :::image-end:::  
    
    > [!NOTE]
    > Lors du test d’autres pages; Si vous souhaitez garantir le fonctionnement correct de chaque page sur les appareils mobiles de bas de gamme, définissez la limitation de processeur à **6**fois.  La démonstration ne fonctionne pas correctement avec 6 fois, ce qui signifie qu’elle utilise uniquement 4x pour les opérations d’instructions.  
    
### Configurer la démonstration  

Il est difficile de créer une démonstration de performance d’exécution qui fonctionne de façon cohérente pour tous les utilisateurs du site Web.  La section suivante vous permet de personnaliser la démonstration pour vous assurer que votre interface est relativement cohérente avec les captures d’écran et les descriptions, quelle que soit la configuration de votre choix.

1.  Choisissez le bouton **Ajouter 10** jusqu’à ce que les icônes bleues se déplacent sensiblement plus lentement.  Sur une machine haut de gamme, il est possible que vous le choisissiez 20 fois.  
1.  Sélectionnez **optimiser**.  Les icônes bleues doivent se déplacer plus rapidement et plus facilement.  
    
    > [!NOTE]
    > Pour mieux afficher une différence entre les versions optimisées et non optimisées, cliquez sur le bouton **soustraire 10** quelques fois et réessayez.  
    > Si vous ajoutez un trop grand nombre d’icônes bleues, il est possible que vous ayez épuisé le processeur, et que vous n’ayez pas à observer une différence majeure dans les résultats pour les deux versions.  
    
1.  Sélectionnez **Annuler l’optimisation**.  Les icônes bleues se déplacent plus lentement et plus lente.  
    
### Enregistrer les performances d’exécution  

Lorsque vous avez exécuté la version optimisée de la page, les icônes bleu se déplacent plus vite.  Pourquoi?  Les deux versions sont supposées déplacer les icônes de la même quantité d’espace sur une même durée.  Prenez un enregistrement dans le panneau performance pour découvrir comment détecter le goulet d’étranglement de performance dans la version non optimisée.  

1.  Dans DevTools, sélectionnez **Enregistrer** \ (! [ Record] [ImageRecordIcon] \).  DevTools capture les métriques de performances lors de l’exécution de la page.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Profil de la page" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Profil de la page  
    :::image-end:::  
    
1.  Patientez quelques secondes.  
1.  Cliquez sur **arrêter**.  DevTools arrête d’enregistrer, traite les données, puis affiche les résultats dans le panneau performance.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Résultats du profil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Résultats du profil  
    :::image-end:::  
    
C’est un volume de données énorme.  ne vous inquiétez pas, le processus va bientôt être plus évocateur.  

## Analyser les résultats  

Après avoir enregistré les performances de la page, mesurez la qualité des performances de celle-ci et recherchez les causes éventuelles.  

### Analyser les images par seconde  

Le principal indicateur de mesure des performances d’une animation est le nombre d’images par seconde (FPS).  Les utilisateurs sont satisfaits lorsque les animations s’exécutent à 60 ips.  

1.  Regardez le graphique **fps** .  Dès lors que vous voyez une barre rouge au-dessus de fps, cela signifie que la fréquence d' **images**a été déplacée et qu’elle est probablement à l’abri de l’utilisation de l’utilisateur.  En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Graphique FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       Graphique **fps**  
    :::image-end:::  
    
1.  Sous le graphique **fps** , vous pouvez voir le graphique **CPU** .  Les couleurs du graphique **UC** correspondent aux couleurs sous l’onglet **Résumé** , au bas du panneau de performance.  Le fait que le graphique **UC** est plein de couleur signifie que le processeur a été épuisé lors de l’enregistrement.  Chaque fois que vous voyez le processeur épuisé pour des périodes longues, il s’agit d’un indicateur pour trouver des moyens d’effectuer moins de tâches.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Onglet graphique UC et synthèse" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Onglet graphique **UC** et **synthèse**  
    :::image-end:::  
    
1.  Pointez sur les graphiques **fps**, **UC**ou **net** .  DevTools affiche une capture d’écran de la page à ce moment.  Déplacez votre souris vers la gauche ou la droite pour relire l’enregistrement.  L’action est référencée en tant que défilement et est utile pour analyser manuellement la progression des animations.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Affichage d’une capture d’écran de la page de l' 2500ms marque de l’enregistrement" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Affichage d’une capture d’écran de la page de l' 2500ms marque de l’enregistrement  
    :::image-end:::  
    
1.  Dans la section **trames** , pointez sur l’un des carrés verts.  DevTools vous indique les FPS pour cette image particulière.  Chaque image est probablement bien en dessous de la cible de 60 images par seconde.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Pointer sur un cadre" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Pointer sur un cadre  
    :::image-end:::  
    
Bien entendu, vous devez constater que la page ne fonctionne pas correctement.  Néanmoins, dans de véritables scénarios, il est possible qu’il n’y ait pas de clarté, de sorte que tous les outils de mesure soient utiles.  

#### Bonus: Ouvrez la jauge FPS  

Un autre outil pratique est le Vumètre d’FPS, qui fournit des estimations en temps réel pour les images par seconde lors de l’exécution de la page.  

1.  Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
1.  Commencez `Rendering` à taper dans le **menu de commandes** et sélectionnez Afficher le **rendu**.  
1.  Dans l’onglet **rendu** , activez l' **indicateur fps**.  Une nouvelle superposition s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Vumètre FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       **Vumètre fps**  
        :::image-end:::  
    
1.  Désactivez le **compteur fps** et sélectionnez `Escape` pour fermer l’onglet **rendu** .  Dans ce didacticiel, vous n’utilisez pas le **compteur fps** .  
    
### Détecter le goulet d’étranglement  

Après avoir mesuré et vérifié que l’animation ne fonctionne pas correctement, l’étape suivante consiste à répondre à la question «pourquoi?».  

1.  Lorsque l’option aucun événement n’est sélectionnée, l’onglet **Résumé** affiche une répartition des activités.  Page ayant consacré la plupart des heures de rendu.  Étant donné que les performances constituent une idée d’avoir moins de travail, vous pouvez réduire la durée du travail de rendu.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Onglet Résumé" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       Onglet **Résumé**  
    :::image-end:::  
    
1.  Développez la section **principale** .  DevTools affiche un graphique d’activité sur le thread principal, au fil du temps.  L’axe x représente l’enregistrement au fil du temps.  Chaque barre représente un événement.  Une barre plus large signifie que l’événement a duré plus longtemps.  L’axe y représente la pile d’appels.  Lorsque des événements sont empilés les uns sur les autres, cela signifie que les événements supérieurs ont entraîné des événements plus faibles.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Section principale" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       Section **principale**  
    :::image-end:::  
    
1.  L’enregistrement comporte un grand nombre de données.  Pour effectuer un zoom avant sur un seul événement; Maintenez la touche enfoncée, puis faites glisser le curseur sur la **vue d’ensemble**, qui est la section incluant les graphiques **fps**, **UC**et **net** .  Les onglets **principales** section et **Résumé** affichent uniquement les informations relatives à la partie sélectionnée de l’enregistrement.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Effectuer un zoom avant sur un événement" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Effectuer un zoom avant sur un événement  
    :::image-end:::  
    
    > [!NOTE]
    > Pour effectuer un zoom, vous pouvez également mettre le focus sur la section **principale** , sélectionner l’arrière-plan ou un événement, puis sélectionner `W` ,, `A` `S` ou `D` .  
    
    1.  Focalisez-vous sur le triangle rouge dans le coin supérieur droit du **cadre d’animation** qui a déclenché l’événement.  Dès lors que vous voyez un triangle rouge, il s’agit d’un avertissement indiquant qu’il y a peut-être un problème lié à l’événement.  
    
    > [!NOTE]
    > Le **Frame d’animation déclenché est déclenché** chaque fois qu’un [ `requestAnimationFrame()` rappel][MDNWebRequestAnimationFrame] est exécuté.  
    
1.  Choisissez le **cadre d’animation** qui a déclenché l’événement.  L’onglet **Résumé** affiche maintenant des informations sur cet événement.  Notez le lien d' **affichage** .  Après l’avoir sélectionnée, DevTools met en surbrillance l’événement qui a déclenché l’événement déclenché par le cadre de l' **animation** .  Par ailleurs, le focus se trouve sur le lien **app.js:95** .  Une fois que vous avez choisi, la ligne appropriée dans le code source s’affiche.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Plus d’informations sur l’événement déclenché par le cadre d’animation" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Plus d’informations sur l’événement déclenché par le **cadre d’animation**  
    :::image-end:::  
    
    > [!NOTE]
    > Après avoir sélectionné un événement, utilisez les touches de direction pour sélectionner les événements en regard de celui-ci.  
    
1.  Sous l’événement **app. Update** , il existe un ensemble d’événements Purple.  Si chaque événement pourpre était plus large, il semblerait que chacun d’entre eux ait un triangle rouge.  
1.  Choisissez l’un des événements de **disposition** Purple.  DevTools fournit des informations supplémentaires sur l’événement sous l’onglet **Résumé** .  En effet, il y a un avertissement sur les flux forcés \ (un autre mot pour la disposition \).  
    
1.  Sous l’onglet **Résumé** , sélectionnez le lien **app.js:71** sous **disposition forcée**.  DevTools vous permet d’accéder à la ligne de code qui force la mise en page.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Ligne de code à l’origine de la disposition forcée." lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       Ligne de code à l’origine de la disposition forcée.  
    :::image-end:::  
    
    > [!NOTE]
    > Le problème lié au code consiste à modifier le style de chaque icône dans chaque cadre d’animation, puis à interroger la position de chaque icône de la page.  Étant donné que les styles ont changé, le navigateur ne sait pas si chaque position de l’icône a changé, donc il doit redisposer l’icône afin de calculer la nouvelle position.  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

C’est beaucoup plus important.  Vous avez à présent une base solide dans le flux de travail de base pour analyser les performances de l’exécution.  Bien fait.  

### Bonus: analysez la version optimisée  

À l’aide des flux de travail et des outils que vous venez d’apprendre, sélectionnez **optimiser** dans la démonstration pour activer le code optimisé, effectuer un autre enregistrement de performance, puis analyser les résultats.  À partir de la fréquence améliorée pour la réduction des événements dans le graphique de flamme de la section **principale** , vous pouvez voir que la version optimisée de l’application est beaucoup moins importante, ce qui améliore les performances.  

> [!NOTE]
> Même la version optimisée n’est pas idéale, car elle manipule la `top` propriété de chaque icône.  Une meilleure approche consiste à respecter les propriétés qui affectent uniquement la composition.  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Étapes suivantes

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Pour plus de confort grâce au panneau performances, vous pouvez faire des exercices pratiques.  Essayez de Profiler vos pages et d’analyser les résultats.  Si vous avez des questions sur les résultats, utilisez l’icône d' **envoi de commentaires** , sélectionnez `Alt` + `Shift` + `I` \ (Windows \), `Option` + `Shift` + `I` \ (MacOS \) ou [tweeter l’équipe devtools][TwitterEdgeDevtools].  Incluez des captures d’écran ou des liens vers des pages reproductibles, le cas échéant.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="L’icône * * Feedback * * dans Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   Icône **Envoyer des commentaires** dans Microsoft Edge devtools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Enfin, il existe de nombreuses façons d’améliorer les performances de l’exécution.  Cet article a été axé sur un goulet d’étranglement d’animation particulier pour vous permettre d’effectuer une visite guidée dans le panneau performance, mais ce n’est qu’un des nombreux goulets d’étranglement que vous pouvez rencontrer.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-publiez un tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
