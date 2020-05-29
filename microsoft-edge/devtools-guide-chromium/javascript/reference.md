---
title: Référence de débogage JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581739"
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







# Référence de débogage JavaScript   



Découvrez les nouveaux flux de travail de débogage grâce à cette référence complète des fonctionnalités de débogage de Microsoft Edge DevTools.  

Pour en savoir plus sur le [débogage, voir prendre en main le langage JavaScript dans Microsoft Edge devtools][DevToolsJavascriptGetStarted] .  

## Suspendre le code avec des points d’arrêt   

Définissez un point d’arrêt pour pouvoir mettre en pause votre code au milieu de l’exécution.  

Pour plus d’informations sur la façon de définir des points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints] .  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools"  

## Parcourir le code   

Une fois votre code interrompu, parcourez-le, une ligne à la fois, en analysant le flux de contrôle et les valeurs de propriétés.  

### Étape au-dessus de la ligne de code   

Lorsque le curseur est en pause sur une ligne de code contenant une fonction qui n’est pas pertinente pour le problème que vous déboguez, cliquez **sur l’icône déplacée** ![ ][ImageStepOverIcon] au-dessus pour exécuter la fonction sans vous mettre à niveau.  

> ##### Figure1  
> Sélectionner **pas à pas**  
> ![Sélectionner pas à pas][ImageSelectingStepOver]  

Par exemple, supposons que vous déboguez le code suivant:  

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

Vous êtes en pause `A` .  En appuyant sur la touche de **progression**, devtools exécute tout le code de la fonction que vous êtes en passe, c’est-à-dire `B` et `C` .  DevTools puis s’interrompt `D` .  

### Passer à la ligne de code   

Lorsqu’il est suspendu sur une ligne de code contenant un appel de fonction associé au problème que vous déboguez, cliquez sur l’icône **pas** à pas détaillé ![ ][ImageStepIntoIcon] pour examiner davantage cette fonction.  

> ##### Figure 2  
> Sélection de la phase de mise **en forme**  
> ![Sélection de la phase de mise en forme][ImageSelectingStepInto]  

Par exemple, supposons que vous déboguez le code suivant:  

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

Vous êtes en pause `A` .  En appuyant sur la touche **pas à pas**, devtools exécute cette ligne de code, puis arrête le suivi `B` .  

### Pas à pas hors ligne de code   

Lorsque vous êtes interrompu à l’intérieur d’une fonction qui n’est pas associée au problème que vous déboguez, cliquez **sur l'** ![ icône Déconnexion en mode hors connexion ][ImageStepOutIcon] pour exécuter le reste du code de la fonction.  

> ##### Figure3  
> Sélection d’une **étape**  
> ![Sélection d’une étape][ImageSelectingStepOut]  

Par exemple, supposons que vous déboguez le code suivant:  

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

Vous êtes en pause `A` .  En appuyant sur **sortir**, devtools exécute le reste du code dans `getName()` , qui est uniquement `B` dans cet exemple, puis il s’interrompt `C` .  

### Exécuter tout le code jusqu’à une ligne spécifique   

Lors du débogage d’une fonction longue, il peut y avoir un grand nombre de code qui n’est pas lié au problème que vous déboguez.  

Vous pouvez passer d’une ligne à l’autres, mais cela est laborieux.  Vous pouvez décider de définir un point d’arrêt de ligne de code sur la ligne qui vous intéresse, puis de cliquer sur l’icône d’exécution du script de reprise d' **exécution** du script ![ ][ImageResumeScriptExecutionIcon] , mais il existe une méthode plus rapide.  

Cliquez avec le bouton droit sur la ligne de code qui vous intéresse, puis sélectionnez **continuer pour accéder à la page suivante**.  DevTools exécute tout le code jusqu’à ce point, puis le met en pause.  

> ##### Figure 4  
> Sélectionner **toujours**  
> ![Sélectionner toujours][ImageSelectingContinueToHere]  

### Redémarrez la fonction Top de la pile d’appels.   

Lorsque vous êtes en pause sur une ligne de code, cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez **redémarrer le cadre** pour suspendre la première ligne de la fonction Top dans votre pile d’appels.  La fonction Top est la dernière fonction qui a été appelée.  

Par exemple, supposons que vous effectuiez le code suivant:  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Vous êtes en pause `A` .  Après avoir cliqué sur **redémarrage**de l’image, vous devez être suspendu `B` , sans définir de point d’arrêt ou en appuyant sur **l’exécution du script de reprise**.  

> ##### Figure 5  
> Sélection du **cadre de reprise**  
> ![Sélection du cadre de reprise][ImageSelectingRestartFrame]  

### Exécution du script de reprise   

Pour poursuivre le runtime suite à une pause de votre script, cliquez sur l’icône d’exécution du script **de reprise d'** exécution du script ![ ][ImageResumeScriptExecutionIcon] .  DevTools exécute le script jusqu’au prochain point d’arrêt, le cas échéant.  

> ##### Figure 6  
> Sélection de **l’exécution du script de reprise**  
> ![Sélection de l’exécution du script de reprise][ImageSelectingResumeScriptExecution]  

#### Forcer le runtime de script   

Pour ignorer tous les points d’arrêt et forcer votre script à s’exécuter, cliquez de façon prolongée sur l’icône d’exécution du script de reprise de l' **exécution** du script ![ ][ImageResumeScriptExecutionIcon] **Force script execution** ![ ][ImageForceScriptExecutionIcon]  

> ##### Figure 7  
> Sélectionner **forcer l’exécution du script**  
> ![Sélectionner forcer l’exécution du script][ImageSelectingForceScriptExecution]  

### Modification du contexte de thread   

Lorsque vous travaillez avec des travailleurs Web ou des travailleurs de service, cliquez sur un contexte répertorié dans le volet **Threads** pour basculer vers ce contexte.  L’icône de flèche bleue représente le contexte actuellement sélectionné.  

> ##### Figure8  
> Le volet **Threads**  
> ![Le volet threads][ImageThreadsPane]  

Par exemple, supposons que vous soyez suspendu sur un point d’arrêt dans votre script principal et votre script de travailleur de service.  Vous voulez afficher les propriétés locales et globales du contexte du travailleur de service, mais le panneau **sources** affiche le contexte de script principal.  En cliquant sur l’entrée du travailleur de service dans le volet **Threads** , vous devez être en mesure de basculer vers ce contexte.  

## Afficher et modifier les propriétés locales, de fermeture et globales   

En pause sur une ligne de code, utilisez le volet **scope** pour afficher et modifier les valeurs des propriétés et variables des étendues locales, de fermeture et globales.  

*   Double-cliquez sur une valeur de propriété pour la modifier.  
*   Les propriétés non Enumerable sont grisées.  

> ##### Figure9  
> Volet **cadre**  
> ![Volet cadre][ImageScopePane]  

## Afficher la pile d’appels actuelle   

Lorsque vous avez interrompu une ligne de code, utilisez le volet **pile d’appels** pour afficher la pile d’appels qui vous a donné ce point.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Cliquez sur une entrée pour accéder à la ligne de code où cette fonction a été appelée.  L’icône de flèche bleue représente quelle fonction DevTools est actuellement en surbrillance.  

> ##### Figure10  
> Volet **pile d’appels**  
> ![Volet pile d’appels][ImageCallStackPane]  

> [!NOTE]
> Lorsque vous n’êtes pas en pause sur une ligne de code, le volet **pile d’appels** est vide.  

### Copier la trace de pile   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez Copier la **trace de pile** pour copier la pile d’appels actuelle dans le presse-papiers.  

> ##### Figure11  
> Sélection de l’option **copier la trace de pile**  
> ![Sélection de l’option copier la trace de pile][ImageSelectingCopyStackTrace]  

Vous trouverez ci-dessous un exemple de sortie:  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Ignorer un script ou un modèle de scripts  

Marquez un script en tant que code de bibliothèque quand vous voulez ignorer ce script lors du débogage.  Lorsqu’il est marqué comme code de la bibliothèque, un script est masqué dans le volet **pile d’appels** et vous n’êtes pas encore dans les fonctions du script lorsque vous parcourez votre code.  

Par exemple, supposons que vous vous résoyez en exécutant ce code:  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` est une bibliothèque tierce digne de confiance.  Si vous êtes sûr que le problème que vous déboguez n’est pas lié à la bibliothèque tierce, il est préférable de marquer le script en tant que **code**de la bibliothèque.  

### Marquer un script en tant que code de bibliothèque à partir du volet éditeur  

Pour marquer un script en tant que **Code de bibliothèque** à partir du volet **éditeur** :  

1.  Ouvrez le fichier.  
1.  Cliquez avec le bouton droit n’importe où.  
1.  Sélectionnez **marquer en tant que code de la bibliothèque**.  

> ##### Figure12  
> Marquage d’un script en tant que **Code de bibliothèque** à partir du volet **éditeur**  
> ![Marquage d’un script en tant que code de bibliothèque à partir du volet éditeur][ImageMarkEditorPane]  

### Marquer un script en tant que code de bibliothèque à partir du volet pile d’appels  

Pour marquer un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels** :  

1.  Cliquez avec le bouton droit sur une fonction à partir du script.  
1.  Sélectionnez **marquer en tant que code de la bibliothèque**.  

> ##### Figure13  
> Marquage d’un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels**  
> ![Marquage d’un script en tant que code de bibliothèque à partir du volet pile d’appels][ImageMarkCallStackPane]  

### Marquer un script en tant que code de bibliothèque à partir des paramètres  

Pour marquer un script unique ou un modèle de scripts dans les paramètres:  

1.  Ouvrez [paramètres][DevToolsCustomize].  
1.  Accédez à l’onglet Code de la **bibliothèque** .  
1.  Cliquez sur **Ajouter un modèle**.  
1.  Entrez le nom du script ou un modèle Regex de noms de script pour le marquer comme code de la **bibliothèque**.  
1.  Cliquez sur **Ajouter**.  

> ##### Figure14  
> Marquage d’un script en tant que **Code de bibliothèque** à partir des paramètres  
> ![Marquage d’un script en tant que code de bibliothèque à partir des paramètres][ImageMarkScriptSettings]  

## Exécuter des extraits de code de débogage à partir de n’importe quelle page   

Si vous vous retrouvez vous exécutez le même code de débogage dans la console que sur et sur le passé, considérez les extraits de code.  Les extraits sont des scripts d’exécution que vous créez, stockez et exécutez dans DevTools.  

Pour en savoir plus, voir [exécution d’extraits de code à partir de n’importe quelle page][DevToolsJavascriptSnippets] .  

## Regardez les valeurs des expressions JavaScript personnalisées   

Utilisez le volet **Espion** pour surveiller les valeurs des expressions personnalisées.  Vous pouvez voir une expression JavaScript valide.  

> ##### Figure15  
> Volet **Espion**  
> ![Volet espion][ImageWatchPane]  

*   Cliquez sur l' **Add Expression** ![ icône Ajouter une expression ][ImageAddExpressionIcon] d’expression pour créer une expression espionne.  
*   Cliquez sur l’icône Actualiser **Actualiser** ![ ][ImageRefreshIcon] pour actualiser les valeurs de toutes les expressions existantes.  Les valeurs sont automatiquement actualisées lors de l’exécution du code.  
*   Pointez sur une expression et cliquez sur l’icône Supprimer l' **expression** ![ ][ImageDeleteExpressionIcon] pour la supprimer.  

## Rendre un fichier minified lisible   

Cliquez **sur l'** ![ icône mise en forme du format ][ImageFormatIcon] pour rendre un fichier minified lisible par l’homme.  

> ##### Figure16  
> Bouton **format**  
> ![Bouton format][ImageFormat]  

## Modification d’un script   

Lors de la résolution d’un bogue, il est souvent préférable d’effectuer des tests dans votre code JavaScript.  Vous n’avez pas besoin d’apporter des modifications dans un éditeur externe ou un IDE, puis de recharger la page.  Vous pouvez modifier votre script dans DevTools.  

Pour modifier un script:  

1.  Ouvrez le fichier dans le volet de l' **éditeur** du panneau **sources** .  
1.  Apportez les modifications souhaitées dans le volet de l' **éditeur** .  
1.  Appuyez sur `Ctrl` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.  DevTools corrige le fichier JS complet dans le moteur JavaScript de Microsoft Edge.  

> ##### Figure17  
> Volet **éditeur**  
> ![Volet éditeur][ImageEditorPane]  

## Désactiver JavaScript   

[Pour plus d’devtools, voir Disable JavaScript with Microsoft Edge][DevToolsJavascriptDisable].  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Figure 1: sélection d’une étape au-dessus"  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Figure 2: sélection des étapes dans"  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Figure 3: sélection des étapes"  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Figure 4: sélection de l’option continuer ici"  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Figure 5: sélectionnez redémarrer le cadre"  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Figure 6: sélectionner l’exécution du script de reprise"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Figure 7: sélection de forcer l’exécution du script"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Figure 8: volet de threads"  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Figure 9: volet d’étendue"  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Figure 10: volet pile d’appels"  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Figure 11: sélection de l’option copier la trace de pile"  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Figure 12: marquage d’un script en tant que code de bibliothèque à partir du volet éditeur"  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Figure 13: marquage d’un script en tant que code de bibliothèque à partir du volet pile d’appels"  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Figure 14: marquage d’un script en tant que code de bibliothèque à partir des paramètres"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Figure 15: volet espion"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Figure 16: bouton format"  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Figure 17: volet éditeur"  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Désactiver JavaScript avec Microsoft Edge DevTools"  
[DevToolsJavascriptGetStarted]: index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools"  
[DevToolsJavascriptSnippets]: snippets.md "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools"  

[DevToolsCustomize]: ../customize/index.md "Personnaliser Microsoft Edge DevTools"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
