---
title: Mapper le code prétraité au code source
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c791a4af4446a1209d6db77ca4787fee80d45e5c
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981768"
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





# Mapper le code prétraité au code source   




Gardez votre code côté client lisible et déboguable même après l’avoir combiné, minify défini ou compilé.  Utilisez les mappages sources pour mapper votre code source à votre code compilé.  

### Résumé  

*   Utilisez les mappages sources pour mapper le code minified au code source. Vous pouvez ensuite lire et déboguer du code compilé dans la source d’origine.  
*   Utilisez uniquement les pré-processeurs capables de produire des cartes sources.  
*   Vérifiez que votre serveur Web peut servir de cartes sources.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## Premiers pas avec les préprocesseurs  

Cet article explique comment interagir avec des cartes sources JavaScript dans le volet sources de DevTools.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## Utiliser un préprocesseur pris en charge  

Vous devez utiliser un Minifier capable de créer des mappages sources.  <!--For the most popular options, see the preprocessor support section.  -->  Pour un affichage étendu, voir la page [mappages de sources: langues, outils et autres informations][GitHubWikiSourceMapsLanguagesTools] wiki.  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Les types de préprocesseurs suivants sont couramment utilisés en association avec des cartes sources:  

*   Transpileurs \ ([Babel][BabelJS], [traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compileurs \ ([compilateur de fermeture][GitHubGoogleClosureCompiler], [dactylographié][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)  
*   Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)  
    
## Cartes sources dans le panneau sources de DevTools  

Les cartes sources des préprocesseurs entraînent le chargement de vos fichiers d’origine en plus de vos fichiers minified par DevTools.  Vous utilisez ensuite les originaux pour définir des points d’arrêt et parcourir le code.  Entre-temps, Microsoft Edge exécute actuellement votre code minified. Cela vous donne l’illusion d’exécuter un site de développement en production.  

Lorsque vous exécutez des mappages source dans DevTools, vous remarquerez que le JavaScript n’est pas compilé et que vous pouvez voir tous les fichiers JavaScript qu’il référence.  Cela utilise le mappage source, mais en coulisses, les scènes exécutent réellement le code compilé.  Les erreurs, journaux et points d’arrêt mappent au code de développement pour le débogage Isard.  En effet, il vous donne l’illusion que vous exécutez un site de développement en production.  

### Activer les cartes sources dans les paramètres  

Les cartes sources sont activées par défaut <!--\(as of Microsoft Edge 39\)-->, mais si vous voulez vérifier ou activer un contrôle; Commencez par ouvrir DevTools, cliquez sur le bouton **personnaliser et contrôler devtools** \ ( `...` \), puis sélectionnez **paramètres**.  Dans le volet **Préférences** , sous **sources**, activez la case à cocher **activer les mappages de sources JavaScript**.  Vous pouvez également activer la case à cocher **activer les mappages de sources CSS**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Activer les mappages sources" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   Activer les mappages sources  
:::image-end:::  

### Débogage avec des mappages sources  

Lors du débogage de votre code et des mappages de sources activés, les cartes sources apparaissent à deux emplacements:  

1.  Dans la console \ (le lien vers la source doit être le fichier d’origine, et non le fichier généré \)  
1.  Lorsque vous parcourez le code \ (les liens dans la pile d’appels doivent ouvrir le fichier source d’origine \)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/debug/breakpoints/step-code ""  -->  

## @sourceURL et displayName  

Si ce n’est pas le `@sourceURL` cas, vous pouvez simplifier le développement lors de l’utilisation d’eval.  Ce programme d’assistance se présente de manière très similaire à la `//# sourceMappingURL` propriété et est en fait mentionné dans les spécifications du mappage source v3.  

En incluant le commentaire spécial suivant dans votre code, qui est considéré comme étant Eval, vous pouvez nommer les évaluations et les scripts intralignes et les styles de sorte qu’ils apparaissent sous la forme de noms plus logiques dans votre DevTools.  

```javascript
//# sourceURL=source.coffee
```  

Accédez à la page suivante.  

*   [démonstration][CssNinjaDemoSourceMapping]
    
Procédez comme suit.  

1.  Ouvrez le DevTools et accédez au panneau **sources** .  
1.  Entrez un nom de fichier dans le champ **nom de votre code:** champ de saisie.  
1.  Cliquez sur le bouton **compiler** .  
1.  Une alerte apparaît avec la somme évaluée à partir de la source de CoffeeScript.  
    
Si vous développez le sous-panneau **sources** , vous voyez maintenant un nouveau fichier avec le nom de fichier personnalisé que vous avez entré précédemment.  Si vous double-cliquez sur le fichier pour l’afficher, il contient le code JavaScript compilé pour la source d’origine.  En revanche, la dernière ligne est un `// @sourceURL` Commentaire indiquant le fichier source d’origine.  Cela risque de vous aider à procéder au débogage lorsque vous travaillez avec des résumés de langue.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Utilisation de sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Utilisation de sourceURL  
:::image-end:::  

<!--  
## Feedback   


-->  

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Paul Bakaus][PaulBakaus] \ (Open Web Developer défenseur, Google: Tools, performance, animation et expérience utilisateur).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
