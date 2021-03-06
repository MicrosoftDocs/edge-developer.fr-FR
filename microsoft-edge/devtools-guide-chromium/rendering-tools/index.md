---
description: Les utilisateurs s’attendent à des pages interactives et fluides.  Chaque étape du pipeline de pixels représente une opportunité de présenter jank.  Découvrez les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances d’exécution.
title: Analyser les performances d’exécution
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 646db5b2e88e33b109e5eb3ae01a296bf3a4fb46
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397999"
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

# <a name="analyze-runtime-performance"></a>Analyser les performances d’exécution  

Les utilisateurs s’attendent à des pages interactives et fluides.  Chaque étape du pipeline de pixels représente une opportunité de présenter jank.  Découvrez les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances d’exécution.  

### <a name="summary"></a>Résumé  

*   N’écrivez pas javaScript qui force le navigateur à recalculer la disposition.  Séparez les fonctions de lecture et d’écriture, puis effectuez d’abord les lectures.  
*   Ne compliquez pas trop votre CSS.  Utilisez moins de CSS et maintenez vos sélecteurs CSS simples.  
*   Évitez autant que possible la disposition.  Choisissez CSS qui ne déclenche pas du tout la disposition.  
*   Le dessin peut prendre plus de temps que toute autre activité de rendu.  Surveillez les goulots d’étranglement de la couleur.  
    
## <a name="javascript"></a>JavaScript  

Les calculs JavaScript, en particulier ceux qui déclenchent des modifications visuelles étendues, peuvent entraîner un blocage des performances de l’application.  Ne laissez pas un JavaScript mal timeé ou de longue durée interférer avec les interactions utilisateur.  

### <a name="javascript-tools"></a>JavaScript : Outils  

Prenez un enregistrement dans l’outil **Performance** et recherchez des événements de longue `Evaluate Script` durée suspects.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

si vous notez un peu de jank dans votre javaScript, vous devrez peut-être prendre votre analyse au niveau suivant et collecter un profil de processeur JavaScript.  Les profils de processeur indiquent où le runtime est passé dans les fonctions de votre page.  Découvrez comment créer des profils d’UC [dans Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].

### <a name="javascript-problems"></a>JavaScript : problèmes  

Le tableau suivant décrit certains problèmes JavaScript courants et les solutions potentielles.  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Des handlers d’entrée coûteux affectent la réponse ou l’animation.  | Tactile, défilement parallaxe.  | Laissez le navigateur gérer les effets tactiles et les défilements, ou lier l’écoute aussi tard que possible.  Accédez à [Des handlers d’entrée coûteux dans la liste][WebPerformanceCalendarRuntimeChecklist]de contrôle des performances d’exécution de Paul Contrôle.  |  
| JavaScript mal timed affectant la réponse, l’animation, le chargement.  | L’utilisateur défile immédiatement après le chargement de la page, setTimeout/setInterval.  | Optimiser le runtime JavaScript : utiliser `requestAnimationFrame` , répartir la manipulation DOM sur des images, utiliser les travailleurs [web][MDNUsingWebWorkers].  |  
| JavaScript de longue durée affectant la réponse.  | [L’événement DOMContentLoaded][MDNUsingWebWorkers] se bloque au cours de son travail JS.  | Déplacez le travail de calcul pur vers les [travailleurs web.][MDNUsingWebWorkers]  Si vous avez besoin d’un accès DOM, utilisez `requestAnimationFrame` .  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Scripts garbage-y affectant la réponse ou l’animation.  | Le garbage collection peut se produire n’importe où.  | Écrivez moins de scripts garbage-y.  Accédez au garbage collection dans Animation dans la liste de contrôle des [performances runtime de Paul Contrôle.][WebPerformanceCalendarRuntimeChecklist]  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a>Style  

Les modifications de style sont coûteuses, en particulier si ces modifications affectent plusieurs éléments du DOM.  Chaque fois que vous appliquez des styles à un élément, le navigateur calcule l’impact sur tous les éléments associés, recalcule la disposition et les repessaint.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a>Style : Outils  

Prenez un enregistrement dans **l’outil Performance.**  Vérifiez l’enregistrement des grands `Recalculate Style` événements \(affichés en violet\).  

<!--todo: add Recording section when available  -->  

Choisissez un `Recalculate Style` événement pour afficher plus d’informations à son sujet dans le volet **d’informations.**  Si les modifications de style prennent beaucoup de temps, cela a un effet sur les performances.  Si les calculs de style affectent un grand nombre d’éléments, il s’agit d’un autre domaine qui peut être amélioré.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Style recalcul long" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Style recalcul long  
:::image-end:::  

Pour réduire l’impact des `Recalculate Style` événements :  

*   Utilisez les [déclencheurs CSS][CssTriggers] pour savoir quelles propriétés CSS déclenchent la disposition, la couleur et la composite.  Ces propriétés ont le pire impact sur les performances de rendu.  
*   Basculez vers des propriétés qui ont moins d’impact.  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a>Style : problèmes  

Le tableau suivant décrit certains problèmes de style courants et les solutions potentielles.  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Calculs de style coûteux affectant la réponse ou l’animation.  | Toute propriété CSS qui modifie la géométrie d’un élément, comme la largeur, la hauteur ou la position ; le navigateur vérifie tous les autres éléments et recalcule la disposition.  | Éviter les CSS qui déclenchent des dispositions |  
| Sélecteurs complexes affectant la réponse ou l’animation.  | Les sélecteurs imbrmbrés forcent le navigateur à tout savoir sur tous les autres éléments, y compris les parents et les enfants.  | Référencez un élément dans votre CSS avec une simple classe.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a>Disposition  

La disposition (ou le réaflow dans Firefox) est le processus par lequel le navigateur calcule les positions et les tailles de tous les éléments d’une page.  Le modèle de disposition du site web signifie qu’un élément peut affecter d’autres éléments ; Par exemple, la largeur de l’élément affecte généralement la largeur des éléments enfants, et ainsi de suite, tout en haut et en bas de `<body>` l’arborescence.  Le processus peut être assez complexe pour le navigateur.  

En règle générale, si vous demandez une valeur géométrique à partir du DOM avant la fin d’une image, vous allez vous retrouver avec des « dispositions synchrones forcées », ce qui peut être un goulot d’étranglement important en cas de répétition fréquente ou d’exécution pour une arborescence DOM de grande taille.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a>Disposition : outils  

Le **volet Performances** identifie quand une page provoque des mises en page synchrones forcées.  Ces `Layout` événements sont marqués avec des barres rouges.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Disposition synchrone forcée" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Disposition synchrone forcée  
:::image-end:::  

La « disposition de disposition » est une répétition de conditions de disposition synchrones forcées.  Cela se produit lorsque JavaScript écrit et lit le DOM à plusieurs reprises, ce qui force le navigateur à recalculer la disposition à plusieurs reprises.  Pour identifier la disposition, recherchez un modèle de plusieurs avertissements de disposition synchrone forcés.  Examinez la figure précédente.  

### <a name="layout-problems"></a>Disposition : problèmes  

Le tableau suivant décrit certains problèmes de disposition courants et les solutions potentielles.  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Disposition synchrone forcée affectant la réponse ou l’animation.  | Forcer le navigateur à effectuer la disposition plus tôt dans le pipeline de pixels, ce qui entraîne des étapes répétées dans le processus de rendu.  | Traitement par lots des premières lectures de votre style, puis écritures.  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Disposition affectant la réponse ou l’animation.  | Boucle qui place le navigateur dans un cycle de lecture-écriture-lecture-écriture, ce qui oblige le navigateur à recalculer encore et encore la disposition.  | Traitement par lot automatique des opérations de lecture-écriture à [l’aide de la bibliothèque FastDom.][GitHubWilsonpageFastdom]  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a>Paint et composite  

Paint est le processus de remplissage des pixels.  Il s’agit souvent de la partie la plus coûteuse du processus de rendu.  Si vous avez remarqué que votre page ne fonctionne pas comme prévu, il est probable que vous avez des problèmes de pinceau.  

La composition est l’endroit où les parties peints de la page sont rassemblées pour s’afficher à l’écran.  En grande partie, si vous vous entenez aux propriétés de composition uniquement et que vous évitez de peindre complètement, vous devez remarquer une amélioration majeure des performances, mais vous devez surveiller les nombres excessifs de calques.  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a>Paint et composite : outils  

Vous souhaitez savoir combien de temps la peinture prend ou à quelle fréquence le dessin se produit-il ?  Vérifiez le [paramètre Activer l’instrumentation de pinceau][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] avancée dans le panneau **Performances,** puis prenez un enregistrement.  Si la majeure partie de votre temps de rendu est consacrée à la peinture, vous avez des problèmes de dessin.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a>Paint et composite : problèmes  

Le tableau suivant décrit certains problèmes courants liés aux images et aux composites, ainsi que les solutions potentielles.  

| Problème | Exemple | Solution |  
|:--- |:--- |:--- |  
| Les tempêtes de couleurs affectent la réponse ou l’animation.  | Les grandes zones de dessin ou les pinceaux coûteux affectant la réponse ou l’animation.  | Évitez de peindre, promouvoir les éléments qui se déplacent vers leur propre couche, utiliser des transformations et l’opacité.  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Explosions de couches affectant les animations.  | La surpromotion d’un trop grand nombre d’éléments `translateZ(0)` avec une incidence importante sur les performances de l’animation.  | Faites une promotion aux couches avec parcimonie, et uniquement lorsque vous savez qu’elle offre des améliorations concrètes.  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Accélérer le runtime JavaScript | Documents Microsoft"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Activer l’instrumentation de pinceau avancée : référence de l’analyse des performances | Documents Microsoft"

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

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Utilisation des outils de | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Liste de vérification des performances d’exécution - Calendrier des performances web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est trouvée ici et est co-auteure par [Les Basques DeCénais (Rédacteur][KayceBasques] technique, Chrome DevTools \& Writer\) et [Meggin Kearney][MegginKearney] \(Tech Writer\). [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
