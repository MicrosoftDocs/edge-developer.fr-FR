---
description: Gardez votre code côté client lisible et déboguable même après l’avoir combiné, minify défini ou compilé.
title: Mapper le code prétraité au code source
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bd04c7bae6f57d4fe3f9b293d70775aa99db3dd1
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993232"
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

# <span data-ttu-id="320b3-104">Mapper le code prétraité au code source</span><span class="sxs-lookup"><span data-stu-id="320b3-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="320b3-105">Gardez votre code côté client lisible et déboguable même après l’avoir combiné, minify défini ou compilé.</span><span class="sxs-lookup"><span data-stu-id="320b3-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="320b3-106">Utilisez les mappages sources pour mapper votre code source à votre code compilé.</span><span class="sxs-lookup"><span data-stu-id="320b3-106">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="320b3-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="320b3-107">Summary</span></span>  

*   <span data-ttu-id="320b3-108">Utilisez les mappages sources pour mapper le code minified au code source.</span><span class="sxs-lookup"><span data-stu-id="320b3-108">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="320b3-109">Vous pouvez ensuite lire et déboguer du code compilé dans la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="320b3-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="320b3-110">Utilisez uniquement les pré-processeurs capables de produire des cartes sources.</span><span class="sxs-lookup"><span data-stu-id="320b3-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="320b3-111">Vérifiez que votre serveur Web peut servir de cartes sources.</span><span class="sxs-lookup"><span data-stu-id="320b3-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="320b3-112">Premiers pas avec les préprocesseurs</span><span class="sxs-lookup"><span data-stu-id="320b3-112">Get started with preprocessors</span></span>  

<span data-ttu-id="320b3-113">Cet article explique comment interagir avec des cartes sources JavaScript dans le volet sources de DevTools.</span><span class="sxs-lookup"><span data-stu-id="320b3-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="320b3-114">Utiliser un préprocesseur pris en charge</span><span class="sxs-lookup"><span data-stu-id="320b3-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="320b3-115">Vous devez utiliser un Minifier capable de créer des mappages sources.</span><span class="sxs-lookup"><span data-stu-id="320b3-115">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="320b3-116">Pour un affichage étendu, voir la page [mappages de sources: langues, outils et autres informations][GitHubWikiSourceMapsLanguagesTools] wiki.</span><span class="sxs-lookup"><span data-stu-id="320b3-116">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="320b3-117">Les types de préprocesseurs suivants sont couramment utilisés en association avec des cartes sources:</span><span class="sxs-lookup"><span data-stu-id="320b3-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="320b3-118">Transpileurs \ ([Babel][BabelJS], [traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="320b3-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="320b3-119">Compileurs \ ([compilateur de fermeture][GitHubGoogleClosureCompiler], [dactylographié][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="320b3-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="320b3-120">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="320b3-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <span data-ttu-id="320b3-121">Cartes sources dans le panneau sources de DevTools</span><span class="sxs-lookup"><span data-stu-id="320b3-121">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="320b3-122">Les cartes sources des préprocesseurs entraînent le chargement de vos fichiers d’origine en plus de vos fichiers minified par DevTools.</span><span class="sxs-lookup"><span data-stu-id="320b3-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="320b3-123">Vous utilisez ensuite les originaux pour définir des points d’arrêt et parcourir le code.</span><span class="sxs-lookup"><span data-stu-id="320b3-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="320b3-124">Entre-temps, Microsoft Edge exécute actuellement votre code minified.</span><span class="sxs-lookup"><span data-stu-id="320b3-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="320b3-125">Cela vous donne l’illusion d’exécuter un site de développement en production.</span><span class="sxs-lookup"><span data-stu-id="320b3-125">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="320b3-126">Lorsque vous exécutez des mappages source dans DevTools, vous remarquerez que le JavaScript n’est pas compilé et que vous pouvez voir tous les fichiers JavaScript qu’il référence.</span><span class="sxs-lookup"><span data-stu-id="320b3-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="320b3-127">Cela utilise le mappage source, mais en coulisses, les scènes exécutent réellement le code compilé.</span><span class="sxs-lookup"><span data-stu-id="320b3-127">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="320b3-128">Les erreurs, journaux et points d’arrêt mappent au code de développement pour le débogage Isard.</span><span class="sxs-lookup"><span data-stu-id="320b3-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="320b3-129">En effet, il vous donne l’illusion que vous exécutez un site de développement en production.</span><span class="sxs-lookup"><span data-stu-id="320b3-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="320b3-130">Activer les cartes sources dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="320b3-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="320b3-131">Les cartes sources sont activées par défaut</span><span class="sxs-lookup"><span data-stu-id="320b3-131">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="320b3-132">, mais si vous voulez vérifier ou activer un contrôle; Commencez par ouvrir DevTools, cliquez sur le bouton **personnaliser et contrôler devtools** \ ( `...` \), puis sélectionnez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="320b3-132">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** \(`...`\) button, and select **Settings**.</span></span>  <span data-ttu-id="320b3-133">Dans le volet **Préférences** , sous **sources**, activez la case à cocher **activer les mappages de sources JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="320b3-133">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="320b3-134">Vous pouvez également activer la case à cocher **activer les mappages de sources CSS**.</span><span class="sxs-lookup"><span data-stu-id="320b3-134">You may also check **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Activer les mappages sources" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="320b3-136">Activer les mappages de sources JavaScript</span><span class="sxs-lookup"><span data-stu-id="320b3-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <span data-ttu-id="320b3-137">Débogage avec des mappages sources</span><span class="sxs-lookup"><span data-stu-id="320b3-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="320b3-138">Lors du débogage de votre code et des mappages de sources activés, les cartes sources apparaissent à deux emplacements:</span><span class="sxs-lookup"><span data-stu-id="320b3-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="320b3-139">Dans la console \ (le lien vers la source doit être le fichier d’origine, et non le fichier généré \)</span><span class="sxs-lookup"><span data-stu-id="320b3-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="320b3-140">Lorsque vous parcourez le code \ (les liens dans la pile d’appels doivent ouvrir le fichier source d’origine \)</span><span class="sxs-lookup"><span data-stu-id="320b3-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <span data-ttu-id="320b3-141">@sourceURL et displayName</span><span class="sxs-lookup"><span data-stu-id="320b3-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="320b3-142">Si ce n’est pas le `@sourceURL` cas, vous pouvez simplifier le développement lors de l’utilisation d’eval.</span><span class="sxs-lookup"><span data-stu-id="320b3-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="320b3-143">Ce programme d’assistance se présente de manière très similaire à la `//# sourceMappingURL` propriété et est en fait mentionné dans les spécifications du mappage source v3.</span><span class="sxs-lookup"><span data-stu-id="320b3-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="320b3-144">En incluant le commentaire spécial suivant dans votre code, qui est considéré comme étant Eval, vous pouvez nommer les évaluations et les scripts intralignes et les styles de sorte qu’ils apparaissent sous la forme de noms plus logiques dans votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="320b3-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="320b3-145">Accédez à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="320b3-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="320b3-146">démonstration</span><span class="sxs-lookup"><span data-stu-id="320b3-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="320b3-147">Effectuez les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="320b3-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="320b3-148">Ouvrez le DevTools et accédez au panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="320b3-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="320b3-149">Entrez un nom de fichier dans le champ **nom de votre code:** champ de saisie.</span><span class="sxs-lookup"><span data-stu-id="320b3-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="320b3-150">Cliquez sur le bouton **compiler** .</span><span class="sxs-lookup"><span data-stu-id="320b3-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="320b3-151">Une alerte apparaît avec la somme évaluée à partir de la source de CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="320b3-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="320b3-152">Si vous développez le sous-panneau **sources** , vous voyez maintenant un nouveau fichier avec le nom de fichier personnalisé que vous avez entré précédemment.</span><span class="sxs-lookup"><span data-stu-id="320b3-152">If you expand the **Sources** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="320b3-153">Si vous double-cliquez sur le fichier pour l’afficher, il contient le code JavaScript compilé pour la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="320b3-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="320b3-154">En revanche, la dernière ligne est un `// @sourceURL` Commentaire indiquant le fichier source d’origine.</span><span class="sxs-lookup"><span data-stu-id="320b3-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="320b3-155">Cela risque de vous aider à procéder au débogage lorsque vous travaillez avec des résumés de langue.</span><span class="sxs-lookup"><span data-stu-id="320b3-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Utiliser sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="320b3-157">Utiliser</span><span class="sxs-lookup"><span data-stu-id="320b3-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <span data-ttu-id="320b3-158">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="320b3-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel est un compilateur JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Voici un exemple simple d’utilisation de l’appellation eval"  

[DartMain]: https://www.dartlang.org "Langage de programmation DART"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/Closure-compilateur | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Cartes sources: langues, outils et autres informations | Wiki GitHub"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Mise en route-Google/traceur-compilateur | Wiki GitHub"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> <span data-ttu-id="320b3-168">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="320b3-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="320b3-169">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Paul Bakaus][PaulBakaus] \ (Open Web Developer défenseur, Google: Tools, performance, animation et expérience utilisateur).</span><span class="sxs-lookup"><span data-stu-id="320b3-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="320b3-171">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="320b3-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
