---
description: Découvrez les nouveaux flux de travail de débogage dans cette référence complète des fonctionnalités de débogage Microsoft Edge DevTools.
title: Utiliser les fonctionnalités du débogger
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6fb90a70e0aac9f556fa9f5f02afee1fd5b4962e
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519603"
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

# <a name="use-the-debugger-features"></a>Utiliser les fonctionnalités du débogger

Cet article explique comment utiliser le débogueur dans Microsoft Edge DevTools, notamment comment définir un point d'arrêt de ligne de code.  Pour définir d'autres types de points d'arrêt, voir [Suspendre votre code avec des points d'arrêt.][DevToolsJavascriptBreakpoints]  

Pour découvrir les principes de base du débogage, accédez à Commencer à déboguer JavaScript dans [Microsoft Edge DevTools,][DevToolsJavascriptGetStarted]qui est un didacticiel qui utilise une page web existante basée sur un formulaire.  Le didacticiel insérez des captures d'écran, afin que vous pouvez l'skim.  Vous pouvez facilement tester les fonctionnalités du débogger à l'aide de la page web de démonstration.

## <a name="view-and-edit-javascript-code"></a>Afficher et modifier du code JavaScript

Lorsque vous corrigez un bogue, vous souhaitez souvent essayer quelques modifications apportées à votre code JavaScript.  Vous n'avez pas besoin d'apporter les modifications dans un éditeur externe ou un IDE, de charger à nouveau le fichier sur le serveur, puis d'actualiser la page . Au lieu de cela, pour tester les modifications, vous pouvez modifier votre code JavaScript directement dans DevTools et voir le résultat immédiatement.  

Pour afficher et modifier un fichier JavaScript :  

1.  Accédez à **l'outil Sources.**  
1.  Dans le **volet Navigateur,** sélectionnez votre fichier pour l'ouvrir dans **le** volet Éditeur.
1.  Dans le **volet** Éditeur, modifiez votre fichier.  
1.  Sélectionnez `Ctrl` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) à enregistrer.  DevTools charge ensuite le fichier JavaScript dans le moteur JavaScript de Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Volet Éditeur" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Volet **** Éditeur  
    :::image-end:::  
     
## <a name="reformat-a-minified-javascript-file-with-pretty-print"></a>Reformater un fichier JavaScript minifié avec une impression assez grande

Pour rendre un fichier minifié lisible par l'homme, sélectionnez le bouton **Format** \( Format \) en bas du volet ![ ](../media/format-icon.msft.png) Éditeur. ****

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Bouton Format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   Bouton **Format**  
:::image-end:::  

## <a name="set-a-breakpoint-to-pause-code"></a>Définir un point d'arrêt pour suspendre le code

Pour suspendre votre code au milieu de l'runtime, définissez un point d'arrêt.  Le type de point d'arrêt le plus simple et le plus connu est un point d'arrêt de ligne de code.

Utilisez un point d'arrêt de ligne de code lorsque vous connaissez la région exacte du code que vous devez examiner.  DevTools s'interrompt toujours à la ligne de code spécifiée avant de l'exécute.

Pour définir un point d'arrêt de ligne de code :  

1.  Accédez à **l'outil Sources.**  
1.  Ouvrez le fichier qui contient la ligne de code.  
1.  Sélectionnez la zone à gauche du numéro de ligne pour la ligne de code.  Vous pouvez également cliquer avec le bouton droit sur le numéro de ligne, puis choisir **Ajouter un point d'arrêt.**  Un cercle rouge apparaît ensuite à côté du numéro de ligne, indiquant un point d'arrêt.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un point d'arrêt de ligne de code" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Un point d'arrêt de ligne de code  
    :::image-end:::  

Les points d'arrêt de ligne de code peuvent être inefficaces à définir, en particulier si vous ne savez pas exactement où rechercher, ou si votre base de code est grande.  Pour gagner du temps lors du débogage, découvrez comment et quand utiliser les autres types de points d'arrêt.  Pour plus d'informations, [accédez à Suspendre votre code avec des points d'arrêt.][DevToolsJavascriptBreakpoints]

## <a name="step-through-code"></a>Code pas à pas  

Une fois que votre code est suspendu à un point d'arrêt, pas à pas dans le code, une ligne à la fois, en enquêtant sur le flux de contrôle et les valeurs des propriétés en cours de route.  

### <a name="step-over-line-of-code"></a>Ligne de code pas à pas  

Lorsqu'il est suspendu sur une ligne de code contenant une fonction qui n'est pas pertinente pour le problème que vous déboguer, choisissez le bouton Pas à pas principal **\(** Pas à pas principal \) pour exécuter la fonction sans y aller pas à ![ ](../media/step-over-icon.msft.png) pas.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Choose Step over" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Choose **Step over**  
:::image-end:::  

Par exemple, supposons que vous déboguer l'extrait de code suivant.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

Vous êtes `A` suspendu.  Une fois que vous avez choisi **Pas**à pas, DevTools exécute tout le code dans la fonction que vous exécutez pas à pas, c'est-à-dire. `B` `C`  DevTools s'interrompt ensuite sur `D` .  

### <a name="step-into-line-of-code"></a>Pas à pas dans la ligne de code  

Lorsqu'il est suspendu sur une ligne de code contenant un appel de fonction lié au problème que vous déboguer, choisissez le bouton Pas à pas dans **\(** Pas à pas dans \) pour examiner cette fonction plus ![ en ](../media/step-into-icon.msft.png) détail.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Choose Step into" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Choose **Step into**  
:::image-end:::  

Par exemple, supposons que vous déboguer l'extrait de code suivant.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

Vous êtes `A` suspendu.  Une fois que **vous avez choisi Pas à**pas, DevTools exécute cette ligne de code, puis s'interrompt. `B`  

### <a name="step-out-of-line-of-code"></a>Sortir de la ligne de code  

Lorsqu'il est suspendu à l'intérieur d'une fonction qui n'est pas liée au problème que vous déboguer, choisissez le bouton Pas **à** pas principal \( Pas à pas sortant \) pour exécuter le reste du code de la ![ ](../media/step-out-icon.msft.png) fonction.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Choose Step out" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Choose **Step out**  
:::image-end:::  

Par exemple, supposons que vous déboguer l'extrait de code suivant.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

Vous êtes `A` suspendu.  Une fois que vous avez choisi Pas **à**pas, DevTools exécute le reste du code dans , qui se trouve juste dans cet exemple, puis `getName()` `B` s'interrompt. `C`  

### <a name="run-all-code-up-to-a-specific-line"></a>Exécuter tout le code jusqu'à une ligne spécifique  

Lors du débogage d'une fonction longue, il peut y avoir un grand nombre de code qui n'est pas lié au problème que vous déboguer.  

Vous pouvez choisir d'aller dans toutes les lignes, mais cela est fastidieux.  Vous pouvez choisir de définir un point d'arrêt de ligne de code sur la ligne qui vous intéresse, puis de choisir le bouton Reprendre l'exécution du **script** \( Reprendre l'exécution du script \), mais il existe un moyen plus ![ ](../media/resume-script-run-icon.msft.png) rapide.  

Pointez sur la ligne de code qui vous intéresse, ouvrez le menu contextuel \(clic droit\), puis choisissez **Continuer ici.**  DevTools exécute l'ensemble du code jusqu'à ce point, puis s'interrompt sur cette ligne.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Choose Continue to here" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Choose **Continue to here**  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a>Redémarrer la fonction supérieure de la pile d'appels  

Pour suspendre la première ligne de la fonction supérieure de votre pile d'appels, sur une ligne de code, pointez n'importe où dans le volet Pile des appels, ouvrez le menu contextuel \(clic droit\), puis choisissez Image de **** redémarrage. ****  La fonction supérieure est la dernière fonction qui a été exécuté.  

L'extrait de code suivant est un exemple de procédure pas à pas.  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Vous êtes `A` suspendu.  Après avoir choisi **l'image**Redémarrer, vous devez être suspendu, sans jamais définir de point d'arrêt ni choisir reprendre l'exécution `B` **du script.**  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Choisir un cadre de redémarrage" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Choisir **un cadre de redémarrage**  
:::image-end:::  

### <a name="resume-script-runtime"></a>Reprise du runtime de script  

Pour poursuivre l'exécution après une pause de votre script, choisissez le bouton Reprendre l'exécution du **script** \( Reprendre l'exécution ![ du script ](../media/resume-script-run-icon.msft.png) \).  DevTools exécute le script jusqu'au point d'arrêt suivant, s'il y en a.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Choose Resume script execution" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Choose **Resume script execution**  
:::image-end:::  

#### <a name="force-script-runtime"></a>Forcer le runtime du script  

Pour ignorer tous les points d'arrêt et forcer votre script à continuer à s'exécuter, choisissez et maintenez le bouton Reprendre l'exécution du **script** \( Reprendre l'exécution du script \), puis choisissez le bouton Forcer l'exécution du script \( Forcer l'exécution du ![ ](../media/resume-script-run-icon.msft.png) **script** ![ ](../media/force-script-run-icon.msft.png) \).  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Choose Force script execution" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Choose **Force script execution**  
:::image-end:::  

### <a name="change-thread-context"></a>Modifier le contexte du thread  

Lorsque vous travaillez avec des travailleurs du web ou des travailleurs de service, choisissez un contexte répertorié dans le volet **Threads** pour basculer vers ce contexte.  L'icône de flèche bleue représente le contexte actuellement sélectionné.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Volet Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Volet **Threads**  
:::image-end:::  

Par exemple, supposons que vous êtes suspendu sur un point d'arrêt dans votre script principal et votre script de travail de service.  Vous souhaitez afficher les propriétés locales et globales pour le contexte de travail de service, mais l'outil **Sources** affiche le contexte de script principal.  Pour basculer vers le contexte de travail de service, dans le volet **Threads,** choisissez l'entrée de travail de service.  

## <a name="view-and-edit-properties-and-variables"></a>Afficher et modifier des propriétés et des variables

Bien qu'il soit suspendu sur **** une ligne de code, utilisez le volet Étendue pour afficher et modifier les valeurs des propriétés et des variables dans les étendues locale, de fermeture et globale.  

*   Double-cliquez sur une valeur de propriété pour la modifier.  
*   Les propriétés non éumables sont grisées.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Volet d'étendue" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   Volet **d'étendue**  
:::image-end:::  

## <a name="watch-the-values-of-javascript-expressions"></a>Regardez les valeurs des expressions JavaScript  

Utilisez le **volet** d'observation pour observer les valeurs des expressions personnalisées.  Vous pouvez regarder n'importe quelle expression JavaScript valide.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Volet d'observation" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   Volet **d'observation**  
:::image-end:::  

*   Pour créer une expression d'observation, sélectionnez le bouton Ajouter une **expression d'observation** \( ![ Ajouter une expression ](../media/add-expression-icon.msft.png) d'observation \).  
*   Pour actualiser les valeurs de toutes les expressions existantes, sélectionnez le bouton **Actualiser** \( ![ Actualiser ](../media/refresh-icon.msft.png) \).  Les valeurs s'actualisent automatiquement lors du code pas à pas.  
*   Pour supprimer une expression d'observation, cliquez avec le bouton droit sur l'expression, puis sélectionnez **Supprimer l'expression d'observation** \( ![ Supprimer l'expression ](../media/delete-expression-icon.msft.png) d'observation \).  

## <a name="view-the-call-stack"></a>Afficher la pile d'appels  

Bien qu'il soit suspendu sur **** une ligne de code, utilisez le volet Pile des appels pour afficher la pile d'appels qui vous a mis à ce point.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Choisissez une entrée pour passer à la ligne de code où cette fonction a été appelée.  L'icône de flèche bleue représente la fonction DevTools actuellement mise en surbrillance.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Volet Pile des appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Volet **Pile des** appels  
:::image-end:::  

> [!NOTE]
> Lorsqu'il n'est pas suspendu sur une ligne de code, le volet **Pile** des appels est vide.  

### <a name="copy-stack-trace"></a>Copier la trace de pile  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Pour copier la pile d'appels actuelle dans **** le Presse-papiers, pointez n'importe où dans le volet Pile des appels, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier la **trace**de pile.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Choose Copy Stack Trace" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Choose **Copy Stack Trace**  
:::image-end:::  

L'extrait de code suivant est un exemple de sortie.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a>Ignorer un script ou un modèle de scripts  

Marquez un script en tant que code de bibliothèque lorsque vous souhaitez ignorer ce script lors du débogage.  Lorsqu'il est marqué comme code de **** bibliothèque, un script est masqué dans le volet Pile des appels et vous n'entrez jamais dans les fonctions du script lorsque vous avancez dans votre code.  

Par exemple, dans l'extrait de code suivant, la ligne utilise , qui `A` `lib` est une bibliothèque tierce.  Si vous êtes certain que le problème que vous déboguer n'est pas lié à cette bibliothèque tierce, il est logique de marquer le script en tant que **code de bibliothèque.**  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a>Marquer un script en tant que code de bibliothèque à partir du volet Éditeur  

Pour marquer un script en tant **que code de bibliothèque** à partir du volet Éditeur : ****  

1.  Ouvrez le fichier.  
1.  Pointez n'importe où et ouvrez le menu contextuel \(clic droit\).  
1.  Choose **Add script to ignore list** (previously shown as Mark as Library **code**).  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet Éditeur" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Marquer un script en tant **que code de bibliothèque** à partir du volet Éditeur ****  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a>Marquer un script en tant que code de bibliothèque à partir du volet Pile des appels  

Pour marquer un script en tant **que code de bibliothèque** à partir du volet **Pile** des appels :  

1.  Pointez sur une fonction à partir du script et ouvrez le menu contextuel \(clic droit\).  
1.  Choose **Add script to ignore list** (previously shown as Mark as Library **code**).  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet Pile des appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Marquer un script en tant **que code de bibliothèque** à partir du volet **Pile** des appels  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a>Marquer un script comme code de bibliothèque à partir des paramètres  

Pour marquer un seul script ou modèle de scripts à partir des **paramètres**:  

1.  Ouvrez [Paramètres.][DevToolsCustomize]  
1.  Accédez au **paramètre de code** Bibliothèque.  
1.  Choose **Add pattern**.  
1.  Entrez le nom du script ou un modèle regex de noms de script à marquer en tant **que code de bibliothèque.**  
1.  Choose **Add**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marquer un script comme code de bibliothèque à partir des paramètres" lightbox="../media/javascript-framework-library-code.msft.png":::
       Marquer un script comme **code de bibliothèque** à partir des **paramètres**  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a>Exécuter des extraits de code de débogage à partir de n'importe quelle page  

Si vous vous trouvez en cours d'exécution du même code de débogage dans la console, pensez à des extraits de code.  Les extraits de code sont des scripts d'runtime que vous pouvez écrire, stocker et exécuter dans DevTools.  

Voir [Exécuter des extraits de code JavaScript sur n'importe quelle page web.][DevToolsJavascriptSnippets]  

## <a name="see-also"></a>Voir également  

*   [Prise en route du débogage de JavaScript dans Microsoft Edge DevTools][DevToolsJavascriptGetStarted] - Didacticiel simple et court utilisant du code existant, avec captures d'écran.
*   [Vue d'ensemble][DevToolsSourcesIndex] de l'outil **Sources :** l'outil Sources inclut le débogger et l'éditeur JavaScript.
*   [Désactivez JavaScript avec Microsoft Edge DevTools.][DevToolsJavascriptDisable]

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d'arrêt dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavascriptDisable]: ./disable.md "Désactiver JavaScript avec Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavascriptGetStarted]: ./index.md "Commencer à déboguer JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavascriptSnippets]: ./snippets.md "Exécuter des extraits de code JavaScript sur n'importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsSourcesIndex]: ../sources/index.md "Vue d'ensemble de l'outil Sources | Documents Microsoft"  
[DevToolsCustomize]: ../customize/index.md "Personnaliser microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
