---
description: Découvrez de nouveaux flux de travail de débogage dans cette référence complète des fonctionnalités de débogage de Microsoft Edge DevTools.
title: Référence de débogage JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f11dfb52e97dcec20d1e6c4f3adeee7010857a33
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993421"
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

# Référence febugging JavaScript  

Découvrez les nouveaux flux de travail de débogage avec la référence complète suivante des fonctionnalités de débogage de Microsoft Edge DevTools.  

Pour en savoir plus sur le [débogage, voir prendre en main le langage JavaScript dans Microsoft Edge devtools][DevToolsJavascriptGetStarted] .  

## Suspendre le code avec des points d’arrêt  

Définissez un point d’arrêt pour pouvoir mettre en pause votre code au milieu de l’exécution.  

Pour plus d’informations sur la façon de définir des points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints] .  

## Parcourir le code  

Une fois votre code interrompu, parcourez-le, une ligne à la fois, en analysant le flux de contrôle et les valeurs de propriétés.  

### Étape au-dessus de la ligne de code  

Lorsqu’elle est suspendue sur une ligne de code contenant une fonction qui n’est pas pertinente pour le problème que vous déboguez **Step over** , cliquez sur le ![ bouton pas ][ImageStepOverIcon] à pas pour exécuter la fonction sans vous mettre à niveau.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Sélectionner pas à pas" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Sélectionner **pas à pas**  
:::image-end:::  

Par exemple, supposons que vous déboguez l’extrait de code suivant.  

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

Lorsque vous êtes en pause sur une ligne de code contenant un appel de fonction associé au problème que vous déboguez, cliquez sur le bouton pas à pas détaillé **dans** \ ( ![ étape en ][ImageStepIntoIcon] \) pour examiner davantage cette fonction.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Sélectionnez la procédure dans" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Sélectionnez la **procédure dans**  
:::image-end:::  

Par exemple, supposons que vous déboguez l’extrait de code suivant.  

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

Lorsque vous êtes en pause dans une fonction qui n’est pas associée au problème que vous déboguez, cliquez sur le bouton pas à pas **détaillé** \ ( ![ extraire ][ImageStepOutIcon] \) pour exécuter le reste du code de la fonction.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Sélectionner sortir" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Sélectionner **sortir**  
:::image-end:::  

Par exemple, supposons que vous déboguez l’extrait de code suivant.  

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

Vous pouvez passer d’une ligne à l’autres, mais cela est laborieux.  Vous pouvez décider de définir un point d’arrêt de ligne de code sur la ligne qui vous intéresse, puis de cliquer sur le bouton de reprise de l' **exécution du script** \ (Resume du ![ script d’exécution ][ImageResumeScriptExecutionIcon] \), mais il existe une méthode plus rapide.  

Cliquez avec le bouton droit sur la ligne de code qui vous intéresse, puis sélectionnez **continuer pour accéder à la page suivante**.  DevTools exécute tout le code jusqu’à ce point, puis le met en pause.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Sélectionnez toujours" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Sélectionnez **toujours**  
:::image-end:::  

### Redémarrez la fonction Top de la pile d’appels.  

Lorsque vous êtes en pause sur une ligne de code, cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez **redémarrer le cadre** pour suspendre la première ligne de la fonction Top dans votre pile d’appels.  La fonction Top est la dernière fonction exécutée.  

L’extrait de code suivant est un exemple qui vous permet de passer en revue.  

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

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Sélectionner redémarrer le cadre" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Sélectionner **redémarrer le cadre**  
:::image-end:::  

### Exécution du script de reprise  

Pour continuer à exécuter le runtime après une pause de votre script, cliquez sur le bouton de reprise de l' **exécution du script** ![ ][ImageResumeScriptExecutionIcon]  DevTools exécute le script jusqu’au prochain point d’arrêt, le cas échéant.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Sélectionner l’exécution du script de reprise" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Sélectionner **l’exécution du script de reprise**  
:::image-end:::  

#### Forcer le runtime de script  

Pour ignorer tous les points d’arrêt et forcer votre script à s’exécuter, cliquez de façon prolongée sur le bouton **reprendre l’exécution du script** \ (Resume du script d' ![ exécution \), puis ][ImageResumeScriptExecutionIcon] sélectionnez le bouton **forcer** l' ![ exécution du script ][ImageForceScriptExecutionIcon]  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Sélectionner forcer l’exécution du script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Sélectionner **forcer l’exécution du script**  
:::image-end:::  

### Modification du contexte de thread  

Lorsque vous travaillez avec des travailleurs Web ou des travailleurs de service, cliquez sur un contexte répertorié dans le volet **Threads** pour basculer vers ce contexte.  L’icône de flèche bleue représente le contexte actuellement sélectionné.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Le volet threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Le volet **Threads**  
:::image-end:::  

Par exemple, supposons que vous soyez suspendu sur un point d’arrêt dans votre script principal et votre script de travailleur de service.  Vous voulez afficher les propriétés locales et globales du contexte du travailleur de service, mais le panneau **sources** affiche le contexte de script principal.  En cliquant sur l’entrée du travailleur de service dans le volet **Threads** , vous devez être en mesure de basculer vers ce contexte.  

## Afficher et modifier les propriétés locales, de fermeture et globales  

En pause sur une ligne de code, utilisez le volet **scope** pour afficher et modifier les valeurs des propriétés et variables des étendues locales, de fermeture et globales.  

*   Double-cliquez sur une valeur de propriété pour la modifier.  
*   Les propriétés non Enumerable sont grisées.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Volet cadre" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   Volet **cadre**  
:::image-end:::  

## Afficher la pile d’appels actuelle  

Lorsque vous avez interrompu une ligne de code, utilisez le volet **pile d’appels** pour afficher la pile d’appels qui vous a donné ce point.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Cliquez sur une entrée pour accéder à la ligne de code où cette fonction a été appelée.  L’icône de flèche bleue représente quelle fonction DevTools est actuellement en surbrillance.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Volet pile d’appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Volet **pile d’appels**  
:::image-end:::  

> [!NOTE]
> Lorsque vous n’êtes pas en pause sur une ligne de code, le volet **pile d’appels** est vide.  

### Copier la trace de pile  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez Copier la **trace de pile** pour copier la pile d’appels actuelle dans le presse-papiers.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Sélectionner copier la trace de pile" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Sélectionner **copier la trace de pile**  
:::image-end:::  

L’extrait de code suivant est un exemple de la sortie.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Ignorer un script ou un modèle de scripts  

Marquez un script en tant que code de bibliothèque quand vous voulez ignorer ce script lors du débogage.  Lorsqu’il est marqué comme code de la bibliothèque, un script est masqué dans le volet **pile d’appels** et vous n’êtes pas encore dans les fonctions du script lorsque vous parcourez votre code.  

L’extrait de code suivant est un exemple qui vous permet de passer en revue.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` est une bibliothèque tierce digne de confiance.  Si vous êtes sûr que le problème que vous déboguez n’est pas lié à la bibliothèque tierce, il est préférable de marquer le script en tant que **code**de la bibliothèque.  

### Marquer un script en tant que code de bibliothèque à partir du volet éditeur  

Pour marquer un script en tant que code de **bibliothèque** à partir du volet **éditeur** , vous pouvez effectuer les actions suivantes.  

1.  Ouvrez le fichier.  
1.  Cliquez avec le bouton droit n’importe où.  
1.  Sélectionnez **marquer en tant que code de la bibliothèque**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet éditeur" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Marquer un script en tant que **Code de bibliothèque** à partir du volet **éditeur**  
    :::image-end:::  
    
### Marquer un script en tant que code de bibliothèque à partir du volet pile d’appels  

Composez les actions folliwng pour marquer un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels** .  

1.  Cliquez avec le bouton droit sur une fonction à partir du script.  
1.  Sélectionnez **marquer en tant que code de la bibliothèque**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet pile d’appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Marquer un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels**  
    :::image-end:::  
    
### Marquer un script en tant que code de bibliothèque à partir des paramètres  

Pour marquer un script ou un modèle de scripts à partir de **paramètres**, procédez comme suit.  

1.  Ouvrez [paramètres][DevToolsCustomize].  
1.  Accédez à l’onglet Code de la **bibliothèque** .  
1.  Cliquez sur **Ajouter un modèle**.  
1.  Entrez le nom du script ou un modèle Regex de noms de script pour le marquer comme code de la **bibliothèque**.  
1.  Cliquez sur **Ajouter**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir des paramètres" lightbox="../media/javascript-framework-library-code.msft.png":::
       Marquer un script en tant que **Code de bibliothèque** à partir des **paramètres**  
    :::image-end:::  
    
## Exécuter des extraits de code de débogage à partir de n’importe quelle page   

Si vous vous retrouvez vous exécutez le même code de débogage dans la console que sur et sur le passé, considérez les extraits de code.  Les extraits sont des scripts d’exécution que vous créez, stockez et exécutez dans DevTools.  

Pour en savoir plus, voir [exécution d’extraits de code à partir de n’importe quelle page][DevToolsJavascriptSnippets] .  

## Regardez les valeurs des expressions JavaScript personnalisées  

Utilisez le volet **Espion** pour surveiller les valeurs des expressions personnalisées.  Vous pouvez voir une expression JavaScript valide.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Volet espion" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   Volet **Espion**  
:::image-end:::  

*   Cliquez sur le bouton **Ajouter une expression** \ ( ![ Ajouter une expression ][ImageAddExpressionIcon] \) pour créer une expression espionne.  
*   Cliquez sur le bouton **Actualiser** pour actualiser ![ ][ImageRefreshIcon] les valeurs de toutes les expressions existantes.  Les valeurs sont automatiquement actualisées lors de l’exécution du code.  
*   Positionnez le pointeur sur une expression et cliquez sur le bouton **Supprimer l’expression** \ ( ![ Supprimer l’expression ][ImageDeleteExpressionIcon] \) pour la supprimer.  

## Rendre un fichier minified lisible  

Cliquez sur le bouton **mettre en forme** \ ( ![ format ][ImageFormatIcon] \) pour rendre un fichier minified lisible par l’utilisateur.  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Bouton format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   Bouton **format**  
:::image-end:::  

## Modification d’un script   

Lors de la résolution d’un bogue, il est souvent préférable d’effectuer des tests dans votre code JavaScript.  Vous n’avez pas besoin d’apporter des modifications dans un éditeur externe ou un IDE, puis de recharger la page.  Vous pouvez modifier votre script dans DevTools.  

Effectuez les opérations suivantes pour modifier un script.  

1.  Ouvrez le fichier dans le volet de l' **éditeur** du panneau **sources** .  
1.  Apportez les modifications souhaitées dans le volet de l' **éditeur** .  
1.  Appuyez sur `Ctrl` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.  DevTools corrige le fichier JS complet dans le moteur JavaScript de Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Volet éditeur" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Volet **éditeur**  
    :::image-end:::  
     
## Désactiver JavaScript   

[Pour plus d’devtools, voir Disable JavaScript with Microsoft Edge][DevToolsJavascriptDisable].  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavascriptDisable]: ./disable.md "Désactiver JavaScript avec Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavascriptGetStarted]: ./index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavascriptSnippets]: ./snippets.md "Exécution d’extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCustomize]: ../customize/index.md "Personnaliser Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
