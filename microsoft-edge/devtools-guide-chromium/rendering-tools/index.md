---
description: Les utilisateurs s’attendent à disposer d’une page interactive et lisse.  Chaque étape du pipeline de pixels représente une opportunité de présenter Jank.  Apprenez-en davantage sur les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances de l’exécution.
title: Analyser les performances du Runtime
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d42ac5e7a7456971d48198a1f362eebe7156bbce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230606"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Analyser les performances du Runtime 

Les utilisateurs s’attendent à disposer d’une page interactive et lisse.  Chaque étape du pipeline de pixels représente une opportunité de présenter Jank.  Apprenez-en davantage sur les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances de l’exécution.  

### Résumé  

*   N’écrivez pas de code JavaScript qui force le navigateur à recalculer la mise en page.  Séparez les fonctions de lecture et d’écriture, et effectuez d’abord les lectures.  
*   Ne surchargez pas votre CSS.  Utilisez moins de feuilles de style CSS et conservez les sélecteurs CSS en toute simplicité.  
*   Evitez autant que possible une disposition.  Sélectionnez CSS qui ne déclenche aucun déclenchement de disposition.  
*   Le dessin a pu prendre plus de temps que d’autres activités de rendu.  Méfiez-vous des goulets d’étranglement.  
    
## JavaScript  

Les calculs JavaScript, en particulier ceux qui déclenchent de nombreuses modifications visuelles, risquent de bloquer les performances de l’application.  Ne laissez pas du temps trop chronométré ou un code JavaScript en cours d’exécution pour les interactions utilisateur.  

### JavaScript: outils  

Prenez un enregistrement dans le panneau **performance** et recherchez des événements suspects longs `Evaluate Script` .  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

Si vous vous injankz dans votre langage JavaScript, il est possible que vous deviez effectuer votre analyse à un niveau avancé et obtenir un profil d’UC JavaScript.  Les profils d’UC indiquent où le runtime est passé dans les fonctions de votre page.  Apprenez à créer des profils d’UC pour [accélérer le runtime JavaScript][DevtoolsRenderingToolsJavascriptRuntime].

### JavaScript: problèmes  

Le tableau suivant décrit certains problèmes courants liés à JavaScript et aux solutions potentielles:  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Gestionnaires d’entrée coûteux affectant la réponse ou l’animation.  | Défilement du son et de la parallaxe.  | Laissez le navigateur manipuler les fonctions d’interécouter et de faire défiler ou lier l’écouteur le plus tard possible.  Pour plus d' [informations, voir gestionnaires d’entrée coûteux dans la liste de contrôle des performances d’exécution de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].  |  
| JavaScript ayant une temporisation médiocre affectant la réponse, l’animation ou le chargement.  | Un utilisateur fait défiler vers la droite après le chargement de la page, setTimeout/setInterval.  | Optimiser le runtime JavaScript: utilisez la `requestAnimationFrame` manipulation de Dom par rapport aux trames, utilisez des [travailleurs Web][MDNUsingWebWorkers].  |  
| JavaScript à exécution longue affectant la réponse.  | L' [événement DOMContentLoaded][MDNUsingWebWorkers] se bloque car il est libérer avec JS Work.  | Déplacez le travail de calcul pur vers des [travailleurs Web][MDNUsingWebWorkers].  Si vous avez besoin d’un accès DOM, utilisez `requestAnimationFrame` .  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Scripts de garbage-y affectant la réponse ou l’animation.  | Le nettoyage de la mémoire est susceptible de se produire n’importe où.  | Écrire moins de scripts de nettoyage de la mémoire.  Pour plus d’en voir la [liste de vérification de performance du runtime, voir Nettoyage de][WebPerformanceCalendarRuntimeChecklist]la mémoire dans l’animation.  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## Style  

Les changements de style sont coûteux, en particulier si ces modifications affectent plusieurs éléments du DOM.  Chaque fois que vous appliquez des styles à un élément, le navigateur détermine l’impact sur tous les éléments associés, recalcule la disposition et redessine.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### Style: outils  

Prenez un enregistrement dans le panneau **performance** .  Vérifiez si l’enregistrement comporte des `Recalculate Style` événements volumineux \ (affiché dans Purple \).  

<!--todo: add Recording section when available  -->  

Cliquez sur un `Recalculate Style` événement pour afficher des informations supplémentaires le concernant dans le volet **Détails** .  Si les modifications apportées au style prennent du temps, il s’agit d’un impact sur les performances.  Si les calculs de style affectent un grand nombre d’éléments, il s’agit d’une autre zone permettant d’améliorer l’espace.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Nouveau style de recalcul" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Nouveau style de recalcul  
:::image-end:::  

Pour réduire l’impact des `Recalculate Style` événements:  

*   Utilisez les [déclencheurs CSS][CssTriggers] pour découvrir les propriétés CSS déclenchant la mise en page, Paint et composite.  Ces propriétés présentent le moins d’impact sur les performances de rendu.  
*   Basculez vers les propriétés qui ont moins d’impact.  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### Style: problèmes  

Le tableau suivant décrit certains problèmes de style courants et les solutions possibles:  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Calculs de styles coûteux affectant la réponse ou l’animation.  | Toute propriété CSS qui modifie la géométrie d’un élément, comme la largeur, la hauteur ou la position; le navigateur vérifie tous les autres éléments et recalcule la disposition.  | Éviter les feuilles CSS qui déclenchent des dispositions |  
| Les sélecteurs complexes affectant la réponse ou l’animation;  | Les sélecteurs imbriqués forcent le navigateur à savoir tout ce qui se passe sur tous les autres éléments, y compris les parents et les enfants.  | Référencez un élément de votre feuille de style CSS en une seule classe.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## Disposition  

Le processus de mise en page (ou de réorganisation en Firefox) consiste à faire en sorte que le navigateur calcule les positions et tailles de tous les éléments d’une page.  Le modèle de disposition du Web signifie qu’un élément est susceptible d’affecter d’autres personnes; par exemple, la largeur de l' `<body>` élément affecte en général la largeur de tout élément enfant, et ainsi de suite, vers le haut et le bas de l’arborescence.  Le processus risque d’être relativement important pour le navigateur.  

En règle générale, si vous demandez une valeur géométrique à partir du DOM avant la fin de l’opération, vous devez vous trouver avec les «dispositions asynchrones forcées», ce qui peut s’avérer un goulet d’étranglement important des performances s’il est répété fréquemment ou exécuté pour une grande arborescence DOM.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### Mise en page: outils  

Le volet **performances** détermine quand une page génère des dispositions asynchrones forcées.  Ces `Layout` événements sont signalés par des barres rouges.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Disposition asynchrone forcée" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Disposition asynchrone forcée  
:::image-end:::  

«La surcharge de disposition» est une répétition de conditions de disposition asynchrones forcées.  Cela se produit lorsque JavaScript écrit et lit à plusieurs reprises du DOM, ce qui force le navigateur à recalculer la mise en page.  Pour identifier la surcharge de la disposition, recherchez un modèle de multiples avertissements relatifs à la disposition asynchrone forcés.  Voir la figure précédente.  

### Mise en page: problèmes  

Le tableau suivant décrit certains problèmes courants liés à la mise en page et les solutions potentielles:  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Disposition asynchrone forcée affectant une réponse ou une animation.  | Forcer le navigateur à effectuer une disposition antérieure dans le pipeline de pixels, ce qui se traduit par des étapes répétées dans le processus de rendu.  | Par lot, le style est lu en premier, puis les écritures éventuelles.  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Surcharge de disposition affectant la réponse ou l’animation.  | Boucle qui place le navigateur dans un cycle en lecture/écriture en lecture/écriture, ce qui force le navigateur à recalculer la mise en page.  | Effectuer automatiquement des opérations par lot en lecture/écriture à l’aide de la [bibliothèque FastDom][GitHubWilsonpageFastdom].  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## Peintures et composites  

Paint est le processus de remplissage en pixels.  Il s’agit souvent de la partie la plus coûteuse du processus de rendu.  Si vous avez remarqué que votre page est Janky de quelque manière que ce soit, il est probable que vous rencontriez des problèmes de peintures.  

La composition consiste à placer les parties peintes de la page pour l’affichage à l’écran.  Dans la plupart des cas, si vous respectez les propriétés de composition unique et que vous n’êtes pas obligé de peindre entièrement, vous devriez constater une amélioration majeure de la performance, mais vous devez prendre en compte pour un nombre excessif de couches.  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### Peintures et composites: outils  

Vous voulez connaître le nombre de fois que le dessin a lieu ou la fréquence à laquelle le dessin se produit?  Activez le paramètre [activer l’instrumentation avancée de peinture][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] dans le panneau de **performance** , puis prenez un enregistrement.  Si la plupart du temps de rendu est dépensé, vous rencontrez des problèmes de peinture.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### Peintures et composites: problèmes  

Le tableau suivant décrit certains problèmes courants liés aux peintures et composites et aux solutions potentielles:  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Les orages de peintures affectant la réponse ou l’animation.  | Des grandes zones de peinture ou des peintures onéreuses affectant une réponse ou une animation.  | Evitez de peindre, promouvez des éléments qui se déplacent vers leur propre calque, utilisez les transformations et l’opacité.  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Explosions de couches affectant les animations.  | La promotion d’un trop grand nombre d’éléments `translateZ(0)` affectait sensiblement les performances de l’animation.  | Promouvez vos couches avec modération, et ce n’est qu’une seule fois que vous savez qu’elle offre des améliorations tangibles.  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Accélérer le runtime JavaScript | Documents Microsoft"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Activer l’instrumentation avancée de Paint-référence d’analyse des performances | Documents Microsoft"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Déclencheurs CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Utilisation des travailleurs sur le Web | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Liste de contrôle de performance du runtime-calendrier des performances du Web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Meggin Kearney][MegginKearney] \ (Technical Writer \).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
