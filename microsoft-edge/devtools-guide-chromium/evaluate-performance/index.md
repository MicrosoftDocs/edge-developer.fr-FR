---
description: Découvrez comment évaluer les performances d’exécution dans Microsoft Edge DevTools.
title: Commencer à analyser les performances d’exécution
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f40f23c4ac9fcc0bb0186ddb96956f691890c0c0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564272"
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
# <a name="get-started-with-analyzing-runtime-performance"></a>Commencer à analyser les performances d’exécution  

> [!NOTE]
> Pour découvrir comment accélérer le chargement de vos pages, accédez à Optimiser la vitesse [du site web.][DevtoolsSpeedGetStarted]  

Les performances d’exécution sont les performances de votre page lorsqu’elle est en cours d’exécution, par opposition au chargement.  L’article de didacticiel suivant vous explique comment utiliser Microsoft Edge panneau Performance de DevTools pour analyser les performances d’exécution.  En ce qui concerne le modèle **RAIL,** les compétences que vous apprenez dans ce didacticiel sont utiles pour analyser les phases de réponse, d’animation et d’inactivité de votre page.  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a>Prise en main  

Dans le didacticiel suivant, vous ouvrez DevTools sur une page en direct et utilisez le panneau Performances pour trouver un goulot d’étranglement des performances sur la page. ****  

1.  Ouvrez Microsoft Edge en **mode InPrivate.**  Le mode InPrivate garantit que Microsoft Edge s’exécute dans un état propre.  Par exemple, si un grand nombre d’extensions sont installées, elles peuvent créer du bruit dans vos mesures de performances.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Chargez la page suivante dans votre fenêtre InPrivate.  La page est la démonstration que vous allez profiler.  La page affiche un grand nombre de petites icônes qui se déplacent vers le haut et vers le bas.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\) pour ouvrir DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Démonstration à gauche et DevTools à droite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       Démonstration à gauche et DevTools à droite  
    :::image-end:::  
    
    > [!NOTE]
    > Pour le reste des figures, DevTools [n’est][DevtoolsCustomizePlacement] pas retenté dans une fenêtre distincte pour mieux se concentrer sur le contenu.  
    
### <a name="simulate-a-mobile-cpu"></a>Simuler une UC mobile  

Les appareils mobiles ont beaucoup moins de puissance processeur que les ordinateurs de bureau et les ordinateurs portables.  Chaque fois que vous profilez une page, utilisez la limitation du processeur pour simuler le fonctionnement de votre page sur les appareils mobiles.  

1.  Dans DevTools, choisissez **l’outil Performance.**  
1.  Assurez-vous que vous choisissez la case à cocher en regard des **captures d’écran.**  
1.  Choose **Capture Paramètres** \( Capture Paramètres ![ ](../media/capture-settings-icon.msft.png) \).  DevTools révèle les paramètres liés à la façon dont il capture les mesures de performances.  
1.  Pour **l’UC,** choisissez **un ralentissement 4x.**  DevTools permet de limiter votre processeur de sorte qu’il soit 4 fois plus lent que d’habitude.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Limitation du processeur" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Limitation du processeur  
    :::image-end:::  
    
    > [!NOTE]
    > Lors du test d’autres pages ; si vous souhaitez vous assurer que chaque page fonctionne bien sur les appareils mobiles bas de gamme, définissez la limitation de l’UC sur un ralentissement **de 6x**.  La démonstration ne fonctionne pas bien avec un ralentissement 6x, donc elle utilise simplement un ralentissement 4x à des fins d’instruction.  
    
### <a name="set-up-the-demo"></a>Configurer la démonstration  

Il est difficile de créer une démonstration des performances d’exécution qui fonctionne de manière cohérente pour tous les lecteurs du site web.  La section suivante vous permet de personnaliser la démonstration pour vous assurer que votre expérience est relativement cohérente avec les captures d’écran et les descriptions, quelle que soit votre disposition particulière.

1.  Choisissez le **bouton Ajouter 10** jusqu’à ce que les icônes bleues se déplacent sensiblement plus lentement qu’auparavant.  Sur un ordinateur haut de gamme, vous pouvez le choisir environ 20 fois.  
1.  Choose **Optimize**.  Les icônes bleues doivent se déplacer plus rapidement et plus harmonieusement.  
    
    > [!NOTE]
    > Pour mieux afficher une différence entre les versions optimisées et non optimisées, sélectionnez le bouton **Soustraction 10** plusieurs fois et essayez à nouveau.  
    > Si vous ajoutez trop d’icônes bleues, il se peut que vous n’observiez pas de différence majeure dans les résultats pour les deux versions.  
    
1.  Choose **Un-Optimize**.  Les icônes bleues se déplacent plus lentement et sont de nouveau plus lentes.  
    
### <a name="record-runtime-performance"></a>Enregistrer les performances d’exécution  

Lorsque vous avez publié la version optimisée de la page, les icônes bleues se déplacent plus rapidement.  Pourquoi?  Les deux versions sont supposées déplacer les icônes de la même quantité d’espace dans la même durée.  Prenez un enregistrement dans le panneau Performances pour découvrir comment détecter le goulot d’étranglement des performances dans la version non optimisée.  

1.  Dans DevTools, choisissez **Record** \( ![ Record ](../media/record-icon.msft.png) \).  DevTools capture les mesures de performances au cours de l’exécution de la page.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Profiler la page" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Profiler la page  
    :::image-end:::  
    
1.  Patientez quelques secondes.  
1.  Choose **Stop**.  DevTools arrête l’enregistrement, traite les données, puis affiche les résultats dans le panneau Performances.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Résultats du profil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Résultats du profil  
    :::image-end:::  
    
Wow, il s’agit d’une quantité considérable de données.  ne vous inquiétez pas, le processus sera bientôt plus logique.  

## <a name="analyze-the-results"></a>Analyser les résultats  

Après avoir enregistré les performances de la page, mesurez la qualité des performances de la page et trouvez les causes.  

### <a name="analyze-frames-per-second"></a>Analyser des images par seconde  

La mesure principale pour mesurer les performances d’une animation est l’image par seconde \(FPS\).  Les utilisateurs sont satisfaits lorsque les animations s’exécutent à 60 FPS.  

1.  Examinez **le graphique FPS.**  Chaque fois qu’une barre rouge est affichée au-dessus de **FPS,** cela signifie que la vitesse d’images est si basse qu’elle nuit probablement à l’expérience utilisateur.  En règle générale, plus la barre verte est élevée, plus le FPS est élevé.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Graphique FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       Graphique **FPS**  
    :::image-end:::  
    
1.  Sous le **graphique FPS,** le **graphique UC** s’affiche.  Les couleurs du **graphique UC** correspondent **** aux couleurs du panneau Résumé, en bas du panneau Performances.  Le fait que le **graphique de l’UC** soit plein de couleurs signifie que l’UC a été maximale pendant l’enregistrement.  Chaque fois que l’UC a été maximale pendant de longues périodes, il s’agit d’un indicateur qui vous permet de trouver des moyens de faire moins de travail.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Graphique de l’UC et panneau De synthèse" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Graphique **de l’UC** **et panneau De** synthèse  
    :::image-end:::  
    
1.  Pointez sur **les graphiques FPS,** **CPU** **ou NET.**  DevTools affiche une capture d’écran de la page à ce stade.  Déplacez votre souris vers la gauche et la droite pour relire l’enregistrement.  L’action est référencé en tant que nettoyage et est utile pour analyser manuellement la progression des animations.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Afficher une capture d’écran de la page autour de la marque de 2 500 ms de l’enregistrement" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Afficher une capture d’écran de la page autour de la marque de 2 500 ms de l’enregistrement  
    :::image-end:::  
    
1.  Dans la section **Cadres,** pointez sur l’un des carrés verts.  DevTools vous montre le FPS pour ce cadre particulier.  Chaque image est probablement bien en dessous de la cible de 60 FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Pointer sur un cadre" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Pointer sur un cadre  
    :::image-end:::  
    
Bien entendu, l’affichage indique que la page web ne s’exécute pas bien.  Toutefois, dans les scénarios réels, il peut ne pas être aussi clair, donc avoir tous les outils pour effectuer des mesures est utile.  

#### <a name="bonus-open-the-fps-meter"></a>Bonus : ouvrir la jauge FPS  

Un autre outil pratique est la jauge FPS, qui fournit des estimations en temps réel pour FPS lors de l’application de la page.  

1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
1.  Commencez à taper `Rendering` dans le menu Commande **et** choisissez Afficher **le rendu.**  
1.  Dans **l’outil de** rendu, allumez **la jauge FPS.**  Une nouvelle superposition apparaît dans le haut à droite de votre vue.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="La jauge FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       La **jauge FPS**  
        :::image-end:::  
    
1.  Désactiver la jauge **FPS** et choisir de `Escape` fermer l’outil **de** rendu.  Vous n’utilisez pas la **jauge FPS** dans ce didacticiel.  
    
### <a name="find-the-bottleneck"></a>Rechercher le goulot d’étranglement  

Une fois que vous avez mesuré et vérifié que l’animation ne s’exécute pas bien, l’étape suivante consiste à répondre à la question « pourquoi ? ».  

1.  Lorsqu’aucun événement n’est choisi, le **panneau Résumé** vous présente une répartition de l’activité.  La page a passé la plupart du temps à être rendu.  Étant donné que les performances sont l’art d’avoir moins de travail, votre objectif est de réduire le temps consacré au travail de rendu.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Le panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       Le **panneau Résumé**  
    :::image-end:::  
    
1.  Développez **la** section Main.  DevTools vous présente un graphique d’activité sur le thread principal, au fil du temps.  L’axe X représente l’enregistrement, au fil du temps.  Chaque barre représente un événement.  Une barre plus large signifie que l’événement a pris plus de temps.  L’axe Y représente la pile d’appels.  Lorsque les événements sont empilés les uns sur les autres, cela signifie que les événements supérieurs ont provoqué les événements inférieurs.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Section Main" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       Section **Main**  
    :::image-end:::  
    
1.  Il y a beaucoup de données dans l’enregistrement.  Pour effectuer un zoom sur un seul événement ; choisissez, maintenez votre curseur sur **** la vue d’ensemble, qui est la section qui inclut les graphiques **FPS,** **CPU**et **NET.**  La section **Principale** et **le volet Résumé** affichent uniquement les informations de la partie sélectionnée de l’enregistrement.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Zoom sur un événement" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Zoom sur un événement  
    :::image-end:::  
    
    > [!NOTE]
    > Une autre façon de zoomer, de focuser la section **Main,** de choisir l’arrière-plan ou un événement, et de sélectionner `W` , ou `A` `S` `D` .  
    
    1.  Focus sur le triangle rouge dans le haut à droite de l’événement de **tir du cadre d’animation.**  Chaque fois qu’un triangle rouge est affiché, il s’agit d’un avertissement signalant qu’il peut y avoir un problème lié à l’événement.  
    
    > [!NOTE]
    > **L’événement Animation Frame Fired** se produit chaque fois qu’un rappel [requestAnimationFrame()][MDNWebRequestAnimationFrame] est exécuté.  
    
1.  Choisissez **l’événement De cadre d’animation** déclenché.  Le **panneau Résumé** vous présente désormais des informations sur cet événement.  Notez le **lien Révéler.**  Une fois que vous l’avez choisi, DevTools met en évidence l’événement qui a initié l’événement Animation **Frame Fired.**  En outre, concentrez-vous **surapp.js:95.**  Une fois que vous l’avez choisi, la ligne pertinente dans le code source s’affiche.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Plus d’informations sur l’événement Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Plus d’informations sur **l’événement Animation Frame Fired**  
    :::image-end:::  
    
    > [!NOTE]
    > Après avoir choisi un événement, utilisez les touches de direction pour sélectionner les événements en de côté.  
    
1.  Sous **l’événement app.update,** il y a un grand nombre d’événements violets.  Si chaque événement violet était plus large, il semble que chacun d’eux puisse avoir un triangle rouge.  
1.  Choisissez l’un des événements **de disposition violet.**  DevTools fournit plus d’informations sur l’événement dans le **panneau Résumé.**  En effet, il existe un avertissement concernant les réaflows forcés \(un autre mot pour la disposition\).  
    
1.  Dans le **panneau Résumé,** choisissez le ** lienapp.js:71 sous** Disposition **forcée**.  DevTools vous permet d’aller à la ligne de code qui a forcé la disposition.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Ligne de code à l’origine de la disposition forcée" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       Ligne de code à l’origine de la disposition forcée  
    :::image-end:::  
    
    > [!NOTE]
    > Le problème avec le code est que, dans chaque cadre d’animation, il modifie le style de chaque icône, puis interroge la position de chaque icône sur la page.  Étant donné que les styles ont été modifiés, le navigateur ne sait pas si chaque position d’icône a changé, il doit donc ré-agencer l’icône afin de calculer la nouvelle position.  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

Cela a été beaucoup à apprendre.  Vous avez maintenant une base solide dans le flux de travail de base pour l’analyse des performances d’exécution.  Bien fait.  

### <a name="bonus-analyze-the-optimized-version"></a>Bonus : analyser la version optimisée  

À l’aide des flux de **** travail et des outils que vous venons d’apprendre, sélectionnez Optimiser sur la démonstration pour activer le code optimisé, prendre un autre enregistrement des performances, puis analyser les résultats.  De la trame améliorée à la réduction du nombre d’événements dans le graphique de graphique graphique dans la section **Main,** la version optimisée de l’application fait beaucoup moins de travail, ce qui se produit de meilleures performances.  

> [!NOTE]
> Même la version optimisée n’est pas très bonne, car elle manipule la `top` propriété de chaque icône.  Une meilleure approche consiste à s’en tenir aux propriétés qui affectent uniquement la composition.  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a>Étapes suivantes

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

Pour vous mettre à l’aise avec **l’outil Performance,** la pratique est parfaite.  Essayez de profiler vos pages et d’analyser les résultats.  Si vous avez des questions sur **** vos résultats, utilisez l’icône Envoyer des commentaires, sélectionnez `Alt` + `Shift` + `I` \(Windows, Linux\), `Option` + `Shift` + `I` sélectionnez \(macOS\) ou tweetez l’équipe [DevTools.][TwitterEdgeDevtools]  Incluez des captures d’écran ou des liens vers des pages reproductibles, si possible.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Icône **Commentaires** dans la Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   Icône **Envoyer des commentaires** dans le Microsoft Edge DevTools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Enfin, il existe de nombreuses façons d’améliorer les performances d’exécution.  Cet article s’est concentré sur un goulot d’étranglement d’animation particulier pour vous offrir une visite guidée du panneau Performances, mais il ne s’agit que de l’un des nombreux goulots d’étranglement que vous pouvez rencontrer.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Modifier Microsoft Edge placement de DevTools (Undock, Dock To Bottom, Dock To Left)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse du site web avec Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools - Publier un tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\(\) | MDN"  

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
