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
# <a name="map-preprocessed-code-to-source-code"></a>Ma mappant le code prétraité au code source  

Gardez votre code côté client lisible et décomscriptible même après la combinaison, la minification ou la compilation.  Utilisez des cartes sources pour ma cartographier votre code source avec votre code compilé.  

### <a name="summary"></a>Résumé  

*   Utilisez l’Cartes source pour ma cartographier le code minifié au code source.  Vous pouvez ensuite lire et déboguer le code compilé dans la source d’origine.  
*   Utilisez uniquement des pré-processeurs capables de produire des Cartes.  
*   Vérifiez que votre serveur web est en mesure de servir le serveur source Cartes.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a>Mise en place des préprocesseurs  

Cet article explique comment interagir avec les Cartes source JavaScript dans l’outil DevTools Sources.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a>Utiliser un préprocesseur pris en charge  

Utilisez un minifier capable de créer des cartes sources.  <!--For the most popular options, navigate to preprocessor support section.  -->  Pour une vue étendue, accédez à [Cartes sources : langues, outils et autres][GitHubWikiSourceMapsLanguagesTools] pages Wiki d’informations.  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Les types de préprocesseurs suivants sont couramment utilisés en combinaison avec les Cartes source :  

*   Transpilers[\(Mér,][BabelJS] [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compilers \([Compilateur de fermeture,][GitHubGoogleClosureCompiler] [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main] [,Script][DartMain]\)  
*   Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)  
    
## <a name="source-maps-in-devtools-sources-tool"></a>Source Cartes dans l’outil Sources DevTools  

Les Cartes sources provenant de préprocesseurs entraînent le chargement par DevTools de vos fichiers d’origine en plus de ceux qui sont minifiés.  Vous utilisez ensuite les originaux pour définir des points d’arrêt et coder pas à pas.  Pendant ce temps, Microsoft Edge exécute réellement votre code minifié.  L’exécution du code vous donne l’illusion d’exécution d’un site de développement en production.  

Lorsque vous exécutez l’Cartes source dans DevTools, vous devez remarquer que javaScript n’est pas compilé et que tous les fichiers JavaScript qu’il référence sont affichés.  La Cartes source dans DevTools utilise le mappage de source, mais la fonctionnalité sous-jacente exécute en fait le code compilé.  Les erreurs, les journaux et les points d’arrêt sont map to the dev code for awesome debugging.  Ainsi, elle vous donne l’illusion que vous exécutez un site dev en production.  

### <a name="enable-source-maps-in-settings"></a>Activer l’Cartes source dans les paramètres  

Les Cartes sources sont activées par défaut<!-- \(as of Microsoft Edge 39\)-->, mais si vous souhaitez les vérifier ou les activer ; tout d’abord, ouvrez DevTools, choisissez Personnaliser et contrôler **DevTools** \( `...` \) > **Paramètres**.  Dans le **volet Préférences,** sous **Sources,** activez **Activer javaScript source Cartes**.  Vous pouvez également activer **l' enable CSS Source Cartes**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Activer l’Cartes" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Activer l’Cartes source JavaScript**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a>Débogage avec source Cartes  

Lors du débogage de votre code et de l’Cartes source activée, l’Cartes source s’affiche à deux endroits :  

1.  Dans la console \(le lien vers la source doit être le fichier d’origine, et non le fichier généré\)  
1.  Lorsque vous pas à pas dans le code \(les liens dans la pile d’appels doivent ouvrir le fichier source d’origine\)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a>@sourceURL et displayName  

Bien qu’elle ne fait pas partie des spécifications de carte source, elle vous permet de faciliter le développement lorsque vous `@sourceURL` travaillez avec des evals.  L’aide s’affiche comme la propriété et est mentionnée dans les spécifications de carte `//# sourceMappingURL` source V3.  

En incluant le commentaire spécial suivant dans votre code, qui est supprimé, vous êtes en mesure de nommer des scripts et des styles inline afin que chacun apparaisse en tant que noms plus logiques dans vos DevTools.  

```javascript
//# sourceURL=source.coffee
```  

Accédez à la page suivante.  

*   [démonstration][CssNinjaDemoSourceMapping]

Effectuer les actions suivantes.  

1.  Ouvrez DevTools et accédez à **l’outil Sources.**  
1.  Entrez un nom de fichier dans le **champ Nom de votre code :** entrée.  
1.  Choisissez le **bouton compiler.**  
1.  Une alerte s’affiche, montrant la somme évaluée à partir de la source CoffeeScript.  
    
Si vous développez le sous-panneau **Sources,** vous affichez maintenant un nouveau fichier avec le nom de fichier personnalisé que vous avez entré précédemment.  Si vous double-cliquez pour afficher ce fichier, il contient le JavaScript compilé pour la source d’origine.  Toutefois, sur la dernière ligne, un commentaire indique `// @sourceURL` le fichier source d’origine.  Cela peut vous aider lors du débogage lors de l’exploitation des abstractions de langage.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Travailler avec sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Travailler avec `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est trouvée ici et est rédigé par [Meggin Kearney][MegginKearney] \(Tech Writer\) et [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\). [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
