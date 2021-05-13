---
description: Gardez votre code côté client lisible et décomscriptible même après la combinaison, la minification ou la compilation.
title: Ma mappant le code prétraité au code source
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3240e437a917dd7074a0584b91dcc6c34576ca24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564048"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="map-preprocessed-code-to-source-code"></a><span data-ttu-id="cd111-104">Ma mappant le code prétraité au code source</span><span class="sxs-lookup"><span data-stu-id="cd111-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="cd111-105">Gardez votre code côté client lisible et décomscriptible même après la combinaison, la minification ou la compilation.</span><span class="sxs-lookup"><span data-stu-id="cd111-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="cd111-106">Utilisez des cartes sources pour ma cartographier votre code source avec votre code compilé.</span><span class="sxs-lookup"><span data-stu-id="cd111-106">Use source maps to map your source code to your compiled code.</span></span>  

### <a name="summary"></a><span data-ttu-id="cd111-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="cd111-107">Summary</span></span>  

*   <span data-ttu-id="cd111-108">Utilisez l’Cartes source pour ma cartographier le code minifié au code source.</span><span class="sxs-lookup"><span data-stu-id="cd111-108">Use Source Maps to map minified code to source code.</span></span>  <span data-ttu-id="cd111-109">Vous pouvez ensuite lire et déboguer le code compilé dans la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="cd111-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="cd111-110">Utilisez uniquement des pré-processeurs capables de produire des Cartes.</span><span class="sxs-lookup"><span data-stu-id="cd111-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="cd111-111">Vérifiez que votre serveur web est en mesure de servir le serveur source Cartes.</span><span class="sxs-lookup"><span data-stu-id="cd111-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a><span data-ttu-id="cd111-112">Mise en place des préprocesseurs</span><span class="sxs-lookup"><span data-stu-id="cd111-112">Get started with preprocessors</span></span>  

<span data-ttu-id="cd111-113">Cet article explique comment interagir avec les Cartes source JavaScript dans l’outil DevTools Sources.</span><span class="sxs-lookup"><span data-stu-id="cd111-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources tool.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a><span data-ttu-id="cd111-114">Utiliser un préprocesseur pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd111-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="cd111-115">Utilisez un minifier capable de créer des cartes sources.</span><span class="sxs-lookup"><span data-stu-id="cd111-115">Use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, navigate to preprocessor support section.  -->  <span data-ttu-id="cd111-116">Pour une vue étendue, accédez à [Cartes sources : langues, outils et autres][GitHubWikiSourceMapsLanguagesTools] pages Wiki d’informations.</span><span class="sxs-lookup"><span data-stu-id="cd111-116">For an extended view, navigate to [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="cd111-117">Les types de préprocesseurs suivants sont couramment utilisés en combinaison avec les Cartes source :</span><span class="sxs-lookup"><span data-stu-id="cd111-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="cd111-118">Transpilers[\(Mér,][BabelJS] [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="cd111-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="cd111-119">Compilers \([Compilateur de fermeture,][GitHubGoogleClosureCompiler] [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main] [,Script][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="cd111-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="cd111-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="cd111-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <a name="source-maps-in-devtools-sources-tool"></a><span data-ttu-id="cd111-121">Source Cartes dans l’outil Sources DevTools</span><span class="sxs-lookup"><span data-stu-id="cd111-121">Source Maps in DevTools Sources tool</span></span>  

<span data-ttu-id="cd111-122">Les Cartes sources provenant de préprocesseurs entraînent le chargement par DevTools de vos fichiers d’origine en plus de ceux qui sont minifiés.</span><span class="sxs-lookup"><span data-stu-id="cd111-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="cd111-123">Vous utilisez ensuite les originaux pour définir des points d’arrêt et coder pas à pas.</span><span class="sxs-lookup"><span data-stu-id="cd111-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="cd111-124">Pendant ce temps, Microsoft Edge exécute réellement votre code minifié.</span><span class="sxs-lookup"><span data-stu-id="cd111-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  <span data-ttu-id="cd111-125">L’exécution du code vous donne l’illusion d’exécution d’un site de développement en production.</span><span class="sxs-lookup"><span data-stu-id="cd111-125">The running of the code gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="cd111-126">Lorsque vous exécutez l’Cartes source dans DevTools, vous devez remarquer que javaScript n’est pas compilé et que tous les fichiers JavaScript qu’il référence sont affichés.</span><span class="sxs-lookup"><span data-stu-id="cd111-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and all of the individual JavaScript files it references are displayed.</span></span>  <span data-ttu-id="cd111-127">La Cartes source dans DevTools utilise le mappage de source, mais la fonctionnalité sous-jacente exécute en fait le code compilé.</span><span class="sxs-lookup"><span data-stu-id="cd111-127">Source Maps in DevTools is using source mapping, but the underlying functionality actually runs the compiled code.</span></span>  <span data-ttu-id="cd111-128">Les erreurs, les journaux et les points d’arrêt sont map to the dev code for awesome debugging.</span><span class="sxs-lookup"><span data-stu-id="cd111-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging.</span></span>  <span data-ttu-id="cd111-129">Ainsi, elle vous donne l’illusion que vous exécutez un site dev en production.</span><span class="sxs-lookup"><span data-stu-id="cd111-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <a name="enable-source-maps-in-settings"></a><span data-ttu-id="cd111-130">Activer l’Cartes source dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="cd111-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="cd111-131">Les Cartes sources sont activées par défaut</span><span class="sxs-lookup"><span data-stu-id="cd111-131">Source Maps are enabled by default</span></span><!-- \(as of Microsoft Edge 39\)--><span data-ttu-id="cd111-132">, mais si vous souhaitez les vérifier ou les activer ; tout d’abord, ouvrez DevTools, choisissez Personnaliser et contrôler **DevTools** \( `...` \) > **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="cd111-132">, but if you want to double-check or enable them; first open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="cd111-133">Dans le **volet Préférences,** sous **Sources,** activez **Activer javaScript source Cartes**.</span><span class="sxs-lookup"><span data-stu-id="cd111-133">On the **Preferences** pane, under **Sources**, turn on **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="cd111-134">Vous pouvez également activer **l' enable CSS Source Cartes**.</span><span class="sxs-lookup"><span data-stu-id="cd111-134">You may also turn on the **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Activer l’Cartes" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="cd111-136">Activer l’Cartes source JavaScript</span><span class="sxs-lookup"><span data-stu-id="cd111-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a><span data-ttu-id="cd111-137">Débogage avec source Cartes</span><span class="sxs-lookup"><span data-stu-id="cd111-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="cd111-138">Lors du débogage de votre code et de l’Cartes source activée, l’Cartes source s’affiche à deux endroits :</span><span class="sxs-lookup"><span data-stu-id="cd111-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="cd111-139">Dans la console \(le lien vers la source doit être le fichier d’origine, et non le fichier généré\)</span><span class="sxs-lookup"><span data-stu-id="cd111-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="cd111-140">Lorsque vous pas à pas dans le code \(les liens dans la pile d’appels doivent ouvrir le fichier source d’origine\)</span><span class="sxs-lookup"><span data-stu-id="cd111-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a><span data-ttu-id="cd111-141">@sourceURL et displayName</span><span class="sxs-lookup"><span data-stu-id="cd111-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="cd111-142">Bien qu’elle ne fait pas partie des spécifications de carte source, elle vous permet de faciliter le développement lorsque vous `@sourceURL` travaillez avec des evals.</span><span class="sxs-lookup"><span data-stu-id="cd111-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="cd111-143">L’aide s’affiche comme la propriété et est mentionnée dans les spécifications de carte `//# sourceMappingURL` source V3.</span><span class="sxs-lookup"><span data-stu-id="cd111-143">The helper is displayed similar to the `//# sourceMappingURL` property and is mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="cd111-144">En incluant le commentaire spécial suivant dans votre code, qui est supprimé, vous êtes en mesure de nommer des scripts et des styles inline afin que chacun apparaisse en tant que noms plus logiques dans vos DevTools.</span><span class="sxs-lookup"><span data-stu-id="cd111-144">By including the following special comment in your code, which is evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="cd111-145">Accédez à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="cd111-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="cd111-146">démonstration</span><span class="sxs-lookup"><span data-stu-id="cd111-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="cd111-147">Effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="cd111-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="cd111-148">Ouvrez DevTools et accédez à **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="cd111-148">Open DevTools and navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="cd111-149">Entrez un nom de fichier dans le **champ Nom de votre code :** entrée.</span><span class="sxs-lookup"><span data-stu-id="cd111-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="cd111-150">Choisissez le **bouton compiler.**</span><span class="sxs-lookup"><span data-stu-id="cd111-150">Choose the **compile** button.</span></span>  
1.  <span data-ttu-id="cd111-151">Une alerte s’affiche, montrant la somme évaluée à partir de la source CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="cd111-151">An alert appears, showing the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="cd111-152">Si vous développez le sous-panneau **Sources,** vous affichez maintenant un nouveau fichier avec le nom de fichier personnalisé que vous avez entré précédemment.</span><span class="sxs-lookup"><span data-stu-id="cd111-152">If you expand the **Sources** sub-panel you now display a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="cd111-153">Si vous double-cliquez pour afficher ce fichier, il contient le JavaScript compilé pour la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="cd111-153">If you double-click to view this file, it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="cd111-154">Toutefois, sur la dernière ligne, un commentaire indique `// @sourceURL` le fichier source d’origine.</span><span class="sxs-lookup"><span data-stu-id="cd111-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="cd111-155">Cela peut vous aider lors du débogage lors de l’exploitation des abstractions de langage.</span><span class="sxs-lookup"><span data-stu-id="cd111-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Travailler avec sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="cd111-157">Travailler avec</span><span class="sxs-lookup"><span data-stu-id="cd111-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="cd111-158">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="cd111-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Il s’agit d’un compilateur JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Exemple simple d’appellation d’eval sourceURL //#"  

[DartMain]: https://www.dartlang.org "Langage de programmation Der"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "google/fermeture-compilateur | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "erreur/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Cartes sources : langues, outils et autres informations | GitHub wiki"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Getting Started - google/traceur-compiler | GitHub wiki"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> <span data-ttu-id="cd111-168">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cd111-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cd111-169">La page d’origine est trouvée ici et est rédigé par [Meggin Kearney][MegginKearney] \(Tech Writer\) et [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\). [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps)</span><span class="sxs-lookup"><span data-stu-id="cd111-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="cd111-171">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cd111-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
