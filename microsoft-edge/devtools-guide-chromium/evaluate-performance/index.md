---
title: Commencer à analyser les performances de l’exécution
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611740"
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
> Pour plus d’informations sur le chargement plus rapide de vos pages, voir [optimiser le site Web][DevtoolsSpeedGetStarted] .  

La performance du runtime correspond à la façon dont votre page s’exécute lorsque celle-ci est en cours d’exécution.  Ce didacticiel vous explique comment utiliser le panneau performances de Microsoft Edge DevTools pour analyser les performances de l’exécution.  En ce qui concerne le modèle **ferroviaire** , les compétences que vous apprenez dans ce didacticiel sont utiles pour analyser les phases de réponse, d’animation et d’inactivité de votre page.  

<!--todo: add rail link when section is ready -->  

## Prise en main   

Dans ce didacticiel, vous ouvrez DevTools sur une page active, puis utilisez le volet performance pour trouver un goulet d’étranglement de performance dans la page.  

1.  Ouvrez Microsoft Edge en **mode InPrivate**.  Le mode InPrivate vérifie que Microsoft Edge s’exécute dans un état propre.  Par exemple, si vous avez un grand nombre d’extensions installées, ces extensions peuvent créer un bruit dans vos mesures de performances.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Chargez la page suivante dans votre fenêtre InPrivate.  Il s’agit de la démonstration que vous allez Profiler.  La page affiche un grand nombre d’icônes déplacées vers le haut et vers le bas.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  Appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \) pour ouvrir devtools.  
    
    > ###### Figure1  
    > La démonstration à gauche et DevTools sur la droite  
    > ![La démonstration à gauche et DevTools sur la droite][ImageGetStarted]  
    
    > [!NOTE]
    > Pour le reste des captures d’écran, DevTools est [ancré dans une fenêtre séparée][DevtoolsCustomizePlacement] pour que vous puissiez mieux voir le contenu.  
    
### Simuler une UC mobile  

Les appareils mobiles disposent d’une puissance UC plus réduite que les ordinateurs de bureau et les ordinateurs portables.  Dès lors que vous profilez une page, utilisez la limitation de l’UC pour simuler l’exécution de votre page sur les appareils mobiles.  

1.  Dans DevTools, cliquez sur l’onglet **performance** .  
1.  Vérifiez que la case à cocher **captures d’écran** est activée.  
1.  Cliquez sur paramètres de capture **paramètres de capture** ![ ][ImageCaptureSettingsIcon] .  DevTools révèle les paramètres liés à la manière dont il capture les métriques de performances.  
1.  Pour **processeur**, sélectionnez **4x Slowdown**.  DevTools limite votre processeur de sorte qu’il soit 4 fois plus lent que d’habitude.  
    
    > ###### Figure 2  
    > Limitation de l’UC  
    > ![Limitation de l’UC][ImageCPUThrottling]  
    
    > [!NOTE]
    > Lorsque vous testez d’autres pages, si vous voulez vous assurer qu’elles fonctionnent bien sur les appareils mobiles de bas niveau, définissez une limitation d’UC de **6 à 6 ralentissements**.  Cette démonstration ne fonctionne pas correctement avec 6 fois, de sorte qu’elle utilise uniquement 4x Slowdown à des fins d’instructions.  
    
### Configurer la démonstration  

Il est difficile de créer une démonstration de performance d’exécution qui fonctionne de façon cohérente pour tous les lecteurs de ce site Web.  Dans cette section, vous pouvez personnaliser la démonstration pour vous assurer que votre interface est relativement cohérente avec les captures d’écran et les descriptions qui s’affichent dans ce didacticiel, quelle que soit la configuration de votre compte.

1.  Continuez à cliquer sur **Ajouter 10** jusqu’à ce que l’icône bleue se déplace sensiblement plus lentement qu’auparavant.  Sur une machine haut de gamme, il est possible qu’il y ait plus de 20 clics.  
1.  Cliquez sur **optimiser**.  Les icônes bleues doivent se déplacer plus rapidement et plus facilement.  

    > [!NOTE]
    > Si vous ne voyez pas une différence notable entre les versions optimisées et non optimisées, essayez de cliquer sur **soustraire 10** fois et de réessayer.  
    > Si vous ajoutez un trop grand nombre d’icônes bleues, vous allez simplement augmenter la capacité du processeur et vous ne verrez pas une différence majeure dans les résultats pour les deux versions.  

1.  Cliquez sur **supprimer**.  Les icônes bleues se déplacent plus lentement et Jank.  

### Enregistrer les performances d’exécution   

Lorsque vous avez exécuté la version optimisée de la page, les icônes bleu se déplacent plus vite.  
Pourquoi?  Les deux versions sont supposées déplacer les icônes de la même quantité d’espace sur une même durée.  Prenez un enregistrement dans le panneau performance pour découvrir comment détecter le goulet d’étranglement de performance dans la version non optimisée.  

1.  Dans DevTools, cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .  
    DevTools capture les métriques de performances lors de l’exécution de la page.  
    
    > ###### Figure3 
    > Profil de la page  
    > ![Profil de la page][ImagePageProfiling]  
    
1.  Patientez quelques secondes.  
1.  Cliquez sur **arrêter**.  DevTools arrête d’enregistrer, traite les données, puis affiche les résultats dans le panneau performance.  
    
    > ###### Figure 4  
    > Résultats du profil  
    > ![Résultats du profil][ImageProfileResults]  

C’est un volume de données énorme.  Ne vous inquiétez pas, c’est bien plus clair.  

## Analyser les résultats   

Une fois que vous avez enregistré les performances de la page, vous pouvez mesurer l’efficacité de la page et trouver les causes éventuelles.  

### Analyser les images par seconde  

Le principal indicateur de mesure des performances d’une animation est le nombre d’images par seconde (FPS).  Les utilisateurs sont satisfaits lorsque les animations s’exécutent à 60 ips.  

1.  Regardez le graphique **fps** .  Dès lors que vous voyez une barre rouge au-dessus de fps, cela signifie que la fréquence d' **images**a été déplacée et qu’elle est probablement à l’abri de l’utilisation de l’utilisateur.  En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.  
    
    > ###### Figure 5  
    > Graphique FPS  
    > ![Graphique FPS][ImageFPSChart]  

1.  Sous le graphique **fps** , vous pouvez voir le graphique **CPU** .  Les couleurs du graphique **UC** correspondent aux couleurs sous l’onglet **Résumé** , au bas du panneau de performance.  Le fait que le graphique **UC** est plein de couleur signifie que le processeur a été épuisé lors de l’enregistrement.  Chaque fois que vous voyez le processeur épuisé pour des périodes longues, il s’agit d’un indicateur pour trouver des moyens d’effectuer moins de tâches.  
    
    > ###### Figure 6  
    > Onglet graphique UC et synthèse  
    > ![Onglet graphique UC et synthèse][ImageCPUSummary]  

1.  Positionnez le pointeur de la souris sur le graphique **fps**, **UC**ou **net** .  DevTools affiche une capture d’écran de la page à ce moment.  Déplacez votre souris vers la gauche ou la droite pour relire l’enregistrement.  Il s’agit de la fonction de nettoyage, qui est utile pour analyser manuellement la progression des animations.  
    
    > ###### Figure 7  
    > Affichage d’une capture d’écran de la page entourant la marque 2500ms de l’enregistrement  
    > ![Affichage d’une capture d’écran de la page entourant la marque 2500ms de l’enregistrement][ImageViewingScreenshot]  

1.  Dans la section **trames** , placez le pointeur de la souris sur l’un des carrés verts.  DevTools vous indique les FPS pour cette image particulière.  Chaque image est probablement bien en dessous de la cible de 60 images par seconde.  
    
    > ###### Figure8  
    > Survol d’un cadre  
    > ![Survol d’un cadre][ImageFrameHover]  

Bien entendu, avec cette démonstration, il est très évident que la page ne fonctionne pas correctement.  Néanmoins, dans de véritables scénarios, il est possible qu’il n’y ait pas de clarté.  

#### Bonus: Ouvrez la jauge FPS  

Un autre outil pratique est le Vumètre d’FPS, qui fournit des estimations en temps réel pour les images par seconde lors de l’exécution de la page.  

1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Commencez `Rendering` à taper dans le menu de commandes et sélectionnez **afficher le rendu**.  
1.  Dans l’onglet **rendu** , activez l' **indicateur fps**.  Une nouvelle superposition s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.  
    
    > ###### Figure9  
    > Vumètre FPS  
    > ![Vumètre FPS][ImageFPSMeter]  

1.  Désactivez la **jauge fps** et appuyez `Escape` pour fermer l’onglet **rendu** .  Dans ce didacticiel, vous ne pourrez pas l’utiliser.  

### Détecter le goulet d’étranglement  

À présent que vous avez mesuré et vérifié que l’animation ne fonctionne pas correctement, la question suivante consiste à vous répondre: pourquoi?  

1.  Notez l’onglet Résumé.  Si aucun événement n’est sélectionné, cet onglet vous montre une répartition des activités.  La page a dépensé la majeure partie de son temps de rendu.  Étant donné que les performances constituent une idée d’avoir moins de travail, vous pouvez réduire la durée du travail de rendu.  
    
    > ###### Figure10  
    > Onglet Résumé  
    > ![Onglet Résumé][ImageSummaryTab]  

1.  Développez la section **principale** .  DevTools affiche un graphique d’activité sur le thread principal, au fil du temps.  L’axe x représente l’enregistrement au fil du temps.  Chaque barre représente un événement.  Une barre plus large signifie que l’événement a duré plus longtemps.  L’axe y représente la pile d’appels.  Lorsque des événements sont empilés les uns sur les autres, cela signifie que les événements supérieurs ont entraîné des événements plus faibles.  
    
    > ##### Figure11  
    > Section principale  
    > ![Section principale][ImageMainSection]  

1.  L’enregistrement comporte un grand nombre de données.  Effectuez un zoom avant sur un seul événement en cliquant, en maintenant le bouton enfoncé et en faisant glisser le pointeur de la souris sur la **vue d’ensemble**, qui est la section incluant les graphiques **fps**, **UC**et **net** .  Les onglets **principales** section et **Résumé** affichent uniquement les informations relatives à la partie sélectionnée de l’enregistrement.  
    
    > ###### Figure12  
    > Zoom avant sur un seul événement  
    > ![Zoom avant sur un événement][ImageZoomedAnimation]  
    
    > [!NOTE]
    > Pour effectuer un zoom, vous pouvez également mettre au point la section **principale** en cliquant sur son arrière-plan ou en sélectionnant un événement, et en appuyant sur les `W` `A` touches,, `S` et `D` .  
    
    1.  Notez le triangle rouge dans le coin supérieur droit du **cadre d’animation** qui a déclenché l’événement.  Dès lors que vous voyez un triangle rouge, il s’agit d’un avertissement indiquant qu’il y a peut-être un problème lié à cet événement.  
    
    > [!NOTE]
    > Le **Frame d’animation déclenché est déclenché** chaque fois qu’un [ `requestAnimationFrame()` rappel][MDNWebRequestAnimationFrame] est exécuté.  
    
1.  Cliquez sur l’événement déclenché par le cadre de l' **animation** .  L’onglet **Résumé** affiche maintenant des informations sur cet événement.  Notez le lien d' **affichage** .  Le fait de cliquer sur cela amène DevTools à mettre en surbrillance l’événement qui a déclenché l’événement déclenché par le cadre de l' **animation** .  Notez également le lien **app. js: 95** .  Un clic vous permet d’atteindre la ligne appropriée dans le code source.
    
    > ##### Figure13  
    > Plus d’informations sur l’événement déclenché par le cadre d’animation  
    > ![Plus d’informations sur l’événement déclenché par le cadre d’animation][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > Après avoir sélectionné un événement, utilisez les touches de direction pour sélectionner les événements en regard de celui-ci.  

1.  Sous l’événement **app. Update** , il existe un ensemble d’événements Purple.  S’ils étaient plus larges, il semble que chacun d’eux dispose d’un triangle rouge.  Cliquez sur l’un des événements de **disposition** Purple désormais.  DevTools fournit des informations supplémentaires sur l’événement sous l’onglet **Résumé** .  En effet, il y a un avertissement sur les flux forcés \ (un autre mot pour la disposition \).  

1.  Sous l’onglet **Résumé** , cliquez sur le lien **app. js: 71** sous **disposition forcée**.  DevTools vous permet d’accéder à la ligne de code qui force la mise en page.  
    
    > ##### Figure14  
    > Ligne de code à l’origine de la disposition forcée.  
    > ![Ligne de code à l’origine de la disposition forcée.][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > Le problème lié à ce code est le suivant: dans chaque cadre d’animation, il modifie le style de chaque icône, puis interroge la position de chaque icône de la page.  Dans la mesure où les styles ont changé, le navigateur ne sait pas si chaque position de l’icône a changé, donc il doit redisposer l’icône afin de calculer sa position.  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

Phew!  C’est un grand nombre d’entre eux, mais vous avez à présent une base solide dans le flux de travail de base pour analyser les performances de l’exécution.  Bien fait.  

### Bonus: analysez la version optimisée  

À l’aide des flux de travail et des outils que vous venez d’apprendre, cliquez sur **optimiser** dans la démonstration pour activer le code optimisé, effectuer un autre enregistrement de performance, puis analyser les résultats.  À partir de la fréquence d’affichage améliorée des événements dans le graphique de flamme de la section **principale** , vous pouvez constater que la version optimisée de l’application présente une plus grande quantité de travail, ce qui améliore les performances.  

> [!NOTE]
> Même la version «optimisée» n’est pas idéale, car elle manipule toujours la `top` propriété de chaque icône.  Une meilleure approche consiste à respecter les propriétés qui affectent uniquement la composition.  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Étapes suivantes

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Pour plus de confort grâce au panneau performances, vous pouvez faire des exercices pratiques.  Essayez de Profiler vos propres pages et d’analyser les résultats.  Si vous avez des questions sur les résultats, utilisez l’icône de **Commentaires** , appuyez `Alt`  +  `Shift`  +  `I` sur Windows ( `Option`  +  `Shift`  +  `I` sur MacOS) ou [Tweet][TwitterEdgeDevtools].  Incluez des captures d’écran ou des liens vers des pages reproductibles, le cas échéant.

> ##### Figure15
> Icône de **Commentaires** dans le Microsoft Edge devtools  
> ![L’icône * * Feedback * * dans Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Enfin, il existe de nombreuses façons d’améliorer les performances de l’exécution.  Ce didacticiel est axé sur un goulet d’étranglement d’animation particulier qui vous permet d’effectuer une visite guidée du panneau performance, mais ce n’est qu’un des nombreux goulets d’étranglement que vous pouvez rencontrer.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Figure 1: démonstration à gauche et DevTools sur la droite"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Figure 2: limitation d’UC"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Figure 3: profil de la page"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Figure 4: résultats du profil"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Figure 5: graphique FPS"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Figure 6: affichage du graphique UC et de l’onglet synthèse, en bleu"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Figure 7: affichage d’une capture d’écran de la page avec la marque 2500ms de l’enregistrement"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Figure 8: survol d’un cadre"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Figure 9: vumètre d’FPS"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Figure 10: onglet Résumé"  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "Figure 11: section principale"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figure 12: zoom avant sur une seule image d’animation déclenchée"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Figure 13: informations supplémentaires sur l’événement déclenché par le cadre d’une animation"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Figure 14: ligne de code à l’origine de la disposition forcée"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Figure 15: icône * * Feedback * * dans Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools"  

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
