---
title: Référence de débogage JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a6ec2438457c81ed527154af30c9642d5c287d3c
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991219"
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

# <span data-ttu-id="7161f-103">Référence febugging JavaScript</span><span class="sxs-lookup"><span data-stu-id="7161f-103">JavaScript febugging reference</span></span>  

<span data-ttu-id="7161f-104">Découvrez les nouveaux flux de travail de débogage avec la référence complète suivante des fonctionnalités de débogage de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7161f-104">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="7161f-105">Pour en savoir plus sur le [débogage, voir prendre en main le langage JavaScript dans Microsoft Edge devtools][DevToolsJavascriptGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="7161f-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="7161f-106">Suspendre le code avec des points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="7161f-106">Pause code with breakpoints</span></span>  

<span data-ttu-id="7161f-107">Définissez un point d’arrêt pour pouvoir mettre en pause votre code au milieu de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7161f-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="7161f-108">Pour plus d’informations sur la façon de définir des points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="7161f-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

## <span data-ttu-id="7161f-109">Parcourir le code</span><span class="sxs-lookup"><span data-stu-id="7161f-109">Step through code</span></span>  

<span data-ttu-id="7161f-110">Une fois votre code interrompu, parcourez-le, une ligne à la fois, en analysant le flux de contrôle et les valeurs de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7161f-110">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="7161f-111">Étape au-dessus de la ligne de code</span><span class="sxs-lookup"><span data-stu-id="7161f-111">Step over line of code</span></span>  

<span data-ttu-id="7161f-112">Lorsqu’elle est suspendue sur une ligne de code contenant une fonction qui n’est pas pertinente pour le problème que vous déboguez **Step over** , cliquez sur le ![ bouton pas ][ImageStepOverIcon] à pas pour exécuter la fonction sans vous mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="7161f-112">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click the **Step over** \(![Step over][ImageStepOverIcon]\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Sélectionner pas à pas" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="7161f-114">Sélectionner **pas à pas**</span><span class="sxs-lookup"><span data-stu-id="7161f-114">Select **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="7161f-115">Par exemple, supposons que vous déboguez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7161f-115">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="7161f-116">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="7161f-116">You are paused on `A`.</span></span>  <span data-ttu-id="7161f-117">En appuyant sur la touche de **progression**, devtools exécute tout le code de la fonction que vous êtes en passe, c’est-à-dire `B` et `C` .</span><span class="sxs-lookup"><span data-stu-id="7161f-117">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="7161f-118">DevTools puis s’interrompt `D` .</span><span class="sxs-lookup"><span data-stu-id="7161f-118">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="7161f-119">Passer à la ligne de code</span><span class="sxs-lookup"><span data-stu-id="7161f-119">Step into line of code</span></span>  

<span data-ttu-id="7161f-120">Lorsque vous êtes en pause sur une ligne de code contenant un appel de fonction associé au problème que vous déboguez, cliquez sur le bouton pas à pas détaillé **dans** \ ( ![ étape en ][ImageStepIntoIcon] \) pour examiner davantage cette fonction.</span><span class="sxs-lookup"><span data-stu-id="7161f-120">When paused on a line of code containing a function call that is related to the problem you are debugging, click the **Step into** \(![Step into][ImageStepIntoIcon]\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Sélectionnez la procédure dans" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="7161f-122">Sélectionnez la **procédure dans**</span><span class="sxs-lookup"><span data-stu-id="7161f-122">Select **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="7161f-123">Par exemple, supposons que vous déboguez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7161f-123">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="7161f-124">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="7161f-124">You are paused on `A`.</span></span>  <span data-ttu-id="7161f-125">En appuyant sur la touche **pas à pas**, devtools exécute cette ligne de code, puis arrête le suivi `B` .</span><span class="sxs-lookup"><span data-stu-id="7161f-125">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="7161f-126">Pas à pas hors ligne de code</span><span class="sxs-lookup"><span data-stu-id="7161f-126">Step out of line of code</span></span>  

<span data-ttu-id="7161f-127">Lorsque vous êtes en pause dans une fonction qui n’est pas associée au problème que vous déboguez, cliquez sur le bouton pas à pas **détaillé** \ ( ![ extraire ][ImageStepOutIcon] \) pour exécuter le reste du code de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7161f-127">When paused inside of a function that is not related to the problem you are debugging, click the **Step out** \(![Step out][ImageStepOutIcon]\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Sélectionner sortir" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="7161f-129">Sélectionner **sortir**</span><span class="sxs-lookup"><span data-stu-id="7161f-129">Select **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="7161f-130">Par exemple, supposons que vous déboguez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7161f-130">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="7161f-131">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="7161f-131">You are paused on `A`.</span></span>  <span data-ttu-id="7161f-132">En appuyant sur **sortir**, devtools exécute le reste du code dans `getName()` , qui est uniquement `B` dans cet exemple, puis il s’interrompt `C` .</span><span class="sxs-lookup"><span data-stu-id="7161f-132">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="7161f-133">Exécuter tout le code jusqu’à une ligne spécifique</span><span class="sxs-lookup"><span data-stu-id="7161f-133">Run all code up to a specific line</span></span>  

<span data-ttu-id="7161f-134">Lors du débogage d’une fonction longue, il peut y avoir un grand nombre de code qui n’est pas lié au problème que vous déboguez.</span><span class="sxs-lookup"><span data-stu-id="7161f-134">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="7161f-135">Vous pouvez passer d’une ligne à l’autres, mais cela est laborieux.</span><span class="sxs-lookup"><span data-stu-id="7161f-135">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="7161f-136">Vous pouvez décider de définir un point d’arrêt de ligne de code sur la ligne qui vous intéresse, puis de cliquer sur le bouton de reprise de l' **exécution du script** \ (Resume du ![ script d’exécution ][ImageResumeScriptExecutionIcon] \), mais il existe une méthode plus rapide.</span><span class="sxs-lookup"><span data-stu-id="7161f-136">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button, but there is a faster way.</span></span>  

<span data-ttu-id="7161f-137">Cliquez avec le bouton droit sur la ligne de code qui vous intéresse, puis sélectionnez **continuer pour accéder à la page suivante**.</span><span class="sxs-lookup"><span data-stu-id="7161f-137">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="7161f-138">DevTools exécute tout le code jusqu’à ce point, puis le met en pause.</span><span class="sxs-lookup"><span data-stu-id="7161f-138">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Sélectionnez toujours" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="7161f-140">Sélectionnez **toujours**</span><span class="sxs-lookup"><span data-stu-id="7161f-140">Select **Continue to here**</span></span>  
:::image-end:::  

### <span data-ttu-id="7161f-141">Redémarrez la fonction Top de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="7161f-141">Restart the top function of the call stack</span></span>  

<span data-ttu-id="7161f-142">Lorsque vous êtes en pause sur une ligne de code, cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez **redémarrer le cadre** pour suspendre la première ligne de la fonction Top dans votre pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="7161f-142">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="7161f-143">La fonction Top est la dernière fonction exécutée.</span><span class="sxs-lookup"><span data-stu-id="7161f-143">The top function is the last function that was run.</span></span>  

<span data-ttu-id="7161f-144">L’extrait de code suivant est un exemple qui vous permet de passer en revue.</span><span class="sxs-lookup"><span data-stu-id="7161f-144">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="7161f-145">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="7161f-145">You are paused on `A`.</span></span>  <span data-ttu-id="7161f-146">Après avoir cliqué sur **redémarrage**de l’image, vous devez être suspendu `B` , sans définir de point d’arrêt ou en appuyant sur **l’exécution du script de reprise**.</span><span class="sxs-lookup"><span data-stu-id="7161f-146">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Sélectionner redémarrer le cadre" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="7161f-148">Sélectionner **redémarrer le cadre**</span><span class="sxs-lookup"><span data-stu-id="7161f-148">Select **Restart Frame**</span></span>  
:::image-end:::  

### <span data-ttu-id="7161f-149">Exécution du script de reprise</span><span class="sxs-lookup"><span data-stu-id="7161f-149">Resume script runtime</span></span>  

<span data-ttu-id="7161f-150">Pour continuer à exécuter le runtime après une pause de votre script, cliquez sur le bouton de reprise de l' **exécution du script** ![ ][ImageResumeScriptExecutionIcon]</span><span class="sxs-lookup"><span data-stu-id="7161f-150">To continue the runtime after a pause of your script, click the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button.</span></span>  <span data-ttu-id="7161f-151">DevTools exécute le script jusqu’au prochain point d’arrêt, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7161f-151">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Sélectionner l’exécution du script de reprise" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="7161f-153">Sélectionner **l’exécution du script de reprise**</span><span class="sxs-lookup"><span data-stu-id="7161f-153">Select **Resume script execution**</span></span>  
:::image-end:::  

#### <span data-ttu-id="7161f-154">Forcer le runtime de script</span><span class="sxs-lookup"><span data-stu-id="7161f-154">Force script runtime</span></span>  

<span data-ttu-id="7161f-155">Pour ignorer tous les points d’arrêt et forcer votre script à s’exécuter, cliquez de façon prolongée sur le bouton **reprendre l’exécution du script** \ (Resume du script d' ![ exécution \), puis ][ImageResumeScriptExecutionIcon] sélectionnez le bouton **forcer** l' ![ exécution du script ][ImageForceScriptExecutionIcon]</span><span class="sxs-lookup"><span data-stu-id="7161f-155">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button and then select the **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Sélectionner forcer l’exécution du script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="7161f-157">Sélectionner **forcer l’exécution du script**</span><span class="sxs-lookup"><span data-stu-id="7161f-157">Select **Force script execution**</span></span>  
:::image-end:::  

### <span data-ttu-id="7161f-158">Modification du contexte de thread</span><span class="sxs-lookup"><span data-stu-id="7161f-158">Change thread context</span></span>  

<span data-ttu-id="7161f-159">Lorsque vous travaillez avec des travailleurs Web ou des travailleurs de service, cliquez sur un contexte répertorié dans le volet **Threads** pour basculer vers ce contexte.</span><span class="sxs-lookup"><span data-stu-id="7161f-159">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="7161f-160">L’icône de flèche bleue représente le contexte actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7161f-160">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Le volet threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="7161f-162">Le volet **Threads**</span><span class="sxs-lookup"><span data-stu-id="7161f-162">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="7161f-163">Par exemple, supposons que vous soyez suspendu sur un point d’arrêt dans votre script principal et votre script de travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="7161f-163">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="7161f-164">Vous voulez afficher les propriétés locales et globales du contexte du travailleur de service, mais le panneau **sources** affiche le contexte de script principal.</span><span class="sxs-lookup"><span data-stu-id="7161f-164">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="7161f-165">En cliquant sur l’entrée du travailleur de service dans le volet **Threads** , vous devez être en mesure de basculer vers ce contexte.</span><span class="sxs-lookup"><span data-stu-id="7161f-165">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="7161f-166">Afficher et modifier les propriétés locales, de fermeture et globales</span><span class="sxs-lookup"><span data-stu-id="7161f-166">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="7161f-167">En pause sur une ligne de code, utilisez le volet **scope** pour afficher et modifier les valeurs des propriétés et variables des étendues locales, de fermeture et globales.</span><span class="sxs-lookup"><span data-stu-id="7161f-167">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="7161f-168">Double-cliquez sur une valeur de propriété pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="7161f-168">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="7161f-169">Les propriétés non Enumerable sont grisées.</span><span class="sxs-lookup"><span data-stu-id="7161f-169">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Volet cadre" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="7161f-171">Volet **cadre**</span><span class="sxs-lookup"><span data-stu-id="7161f-171">The **Scope** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="7161f-172">Afficher la pile d’appels actuelle</span><span class="sxs-lookup"><span data-stu-id="7161f-172">View the current call stack</span></span>  

<span data-ttu-id="7161f-173">Lorsque vous avez interrompu une ligne de code, utilisez le volet **pile d’appels** pour afficher la pile d’appels qui vous a donné ce point.</span><span class="sxs-lookup"><span data-stu-id="7161f-173">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="7161f-174">Cliquez sur une entrée pour accéder à la ligne de code où cette fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="7161f-174">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="7161f-175">L’icône de flèche bleue représente quelle fonction DevTools est actuellement en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7161f-175">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Volet pile d’appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="7161f-177">Volet **pile d’appels**</span><span class="sxs-lookup"><span data-stu-id="7161f-177">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7161f-178">Lorsque vous n’êtes pas en pause sur une ligne de code, le volet **pile d’appels** est vide.</span><span class="sxs-lookup"><span data-stu-id="7161f-178">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="7161f-179">Copier la trace de pile</span><span class="sxs-lookup"><span data-stu-id="7161f-179">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="7161f-180">Cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez Copier la **trace de pile** pour copier la pile d’appels actuelle dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="7161f-180">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Sélectionner copier la trace de pile" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="7161f-182">Sélectionner **copier la trace de pile**</span><span class="sxs-lookup"><span data-stu-id="7161f-182">Select **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="7161f-183">L’extrait de code suivant est un exemple de la sortie.</span><span class="sxs-lookup"><span data-stu-id="7161f-183">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="7161f-184">Ignorer un script ou un modèle de scripts</span><span class="sxs-lookup"><span data-stu-id="7161f-184">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="7161f-185">Marquez un script en tant que code de bibliothèque quand vous voulez ignorer ce script lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="7161f-185">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="7161f-186">Lorsqu’il est marqué comme code de la bibliothèque, un script est masqué dans le volet **pile d’appels** et vous n’êtes pas encore dans les fonctions du script lorsque vous parcourez votre code.</span><span class="sxs-lookup"><span data-stu-id="7161f-186">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="7161f-187">L’extrait de code suivant est un exemple qui vous permet de passer en revue.</span><span class="sxs-lookup"><span data-stu-id="7161f-187">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="7161f-188">est une bibliothèque tierce digne de confiance.</span><span class="sxs-lookup"><span data-stu-id="7161f-188">is a third-party library that you trust.</span></span>  <span data-ttu-id="7161f-189">Si vous êtes sûr que le problème que vous déboguez n’est pas lié à la bibliothèque tierce, il est préférable de marquer le script en tant que **code**de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="7161f-189">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="7161f-190">Marquer un script en tant que code de bibliothèque à partir du volet éditeur</span><span class="sxs-lookup"><span data-stu-id="7161f-190">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="7161f-191">Pour marquer un script en tant que code de **bibliothèque** à partir du volet **éditeur** , vous pouvez effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="7161f-191">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="7161f-192">Ouvrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="7161f-192">Open the file.</span></span>  
1.  <span data-ttu-id="7161f-193">Cliquez avec le bouton droit n’importe où.</span><span class="sxs-lookup"><span data-stu-id="7161f-193">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="7161f-194">Sélectionnez **marquer en tant que code de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="7161f-194">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet éditeur" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="7161f-196">Marquer un script en tant que **Code de bibliothèque** à partir du volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="7161f-196">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="7161f-197">Marquer un script en tant que code de bibliothèque à partir du volet pile d’appels</span><span class="sxs-lookup"><span data-stu-id="7161f-197">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="7161f-198">Composez les actions folliwng pour marquer un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels** .</span><span class="sxs-lookup"><span data-stu-id="7161f-198">Compelte the folliwng actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="7161f-199">Cliquez avec le bouton droit sur une fonction à partir du script.</span><span class="sxs-lookup"><span data-stu-id="7161f-199">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="7161f-200">Sélectionnez **marquer en tant que code de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="7161f-200">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet pile d’appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="7161f-202">Marquer un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels**</span><span class="sxs-lookup"><span data-stu-id="7161f-202">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="7161f-203">Marquer un script en tant que code de bibliothèque à partir des paramètres</span><span class="sxs-lookup"><span data-stu-id="7161f-203">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="7161f-204">Pour marquer un script ou un modèle de scripts à partir de **paramètres**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="7161f-204">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="7161f-205">Ouvrez [paramètres][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="7161f-205">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="7161f-206">Accédez à l’onglet Code de la **bibliothèque** .</span><span class="sxs-lookup"><span data-stu-id="7161f-206">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="7161f-207">Cliquez sur **Ajouter un modèle**.</span><span class="sxs-lookup"><span data-stu-id="7161f-207">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="7161f-208">Entrez le nom du script ou un modèle Regex de noms de script pour le marquer comme code de la **bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="7161f-208">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="7161f-209">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7161f-209">Click **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir des paramètres" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="7161f-211">Marquer un script en tant que **Code de bibliothèque** à partir des **paramètres**</span><span class="sxs-lookup"><span data-stu-id="7161f-211">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7161f-212">Exécuter des extraits de code de débogage à partir de n’importe quelle page</span><span class="sxs-lookup"><span data-stu-id="7161f-212">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="7161f-213">Si vous vous retrouvez vous exécutez le même code de débogage dans la console que sur et sur le passé, considérez les extraits de code.</span><span class="sxs-lookup"><span data-stu-id="7161f-213">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="7161f-214">Les extraits sont des scripts d’exécution que vous créez, stockez et exécutez dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="7161f-214">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="7161f-215">Pour en savoir plus, voir [exécution d’extraits de code à partir de n’importe quelle page][DevToolsJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="7161f-215">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="7161f-216">Regardez les valeurs des expressions JavaScript personnalisées</span><span class="sxs-lookup"><span data-stu-id="7161f-216">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="7161f-217">Utilisez le volet **Espion** pour surveiller les valeurs des expressions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7161f-217">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="7161f-218">Vous pouvez voir une expression JavaScript valide.</span><span class="sxs-lookup"><span data-stu-id="7161f-218">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Volet espion" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="7161f-220">Volet **Espion**</span><span class="sxs-lookup"><span data-stu-id="7161f-220">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="7161f-221">Cliquez sur le bouton **Ajouter une expression** \ ( ![ Ajouter une expression ][ImageAddExpressionIcon] \) pour créer une expression espionne.</span><span class="sxs-lookup"><span data-stu-id="7161f-221">Click the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="7161f-222">Cliquez sur le bouton **Actualiser** pour actualiser ![ ][ImageRefreshIcon] les valeurs de toutes les expressions existantes.</span><span class="sxs-lookup"><span data-stu-id="7161f-222">Click the **Refresh** \(![Refresh][ImageRefreshIcon]\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="7161f-223">Les valeurs sont automatiquement actualisées lors de l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="7161f-223">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="7161f-224">Positionnez le pointeur sur une expression et cliquez sur le bouton **Supprimer l’expression** \ ( ![ Supprimer l’expression ][ImageDeleteExpressionIcon] \) pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="7161f-224">Hover over an expression and click the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) button to delete it.</span></span>  

## <span data-ttu-id="7161f-225">Rendre un fichier minified lisible</span><span class="sxs-lookup"><span data-stu-id="7161f-225">Make a minified file readable</span></span>  

<span data-ttu-id="7161f-226">Cliquez sur le bouton **mettre en forme** \ ( ![ format ][ImageFormatIcon] \) pour rendre un fichier minified lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7161f-226">Click the **Format** \(![Format][ImageFormatIcon]\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Bouton format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="7161f-228">Bouton **format**</span><span class="sxs-lookup"><span data-stu-id="7161f-228">The **Format** button</span></span>  
:::image-end:::  

## <span data-ttu-id="7161f-229">Modification d’un script</span><span class="sxs-lookup"><span data-stu-id="7161f-229">Edit a script</span></span>   

<span data-ttu-id="7161f-230">Lors de la résolution d’un bogue, il est souvent préférable d’effectuer des tests dans votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7161f-230">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="7161f-231">Vous n’avez pas besoin d’apporter des modifications dans un éditeur externe ou un IDE, puis de recharger la page.</span><span class="sxs-lookup"><span data-stu-id="7161f-231">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="7161f-232">Vous pouvez modifier votre script dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="7161f-232">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="7161f-233">Effectuez les opérations suivantes pour modifier un script.</span><span class="sxs-lookup"><span data-stu-id="7161f-233">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="7161f-234">Ouvrez le fichier dans le volet de l' **éditeur** du panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="7161f-234">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="7161f-235">Apportez les modifications souhaitées dans le volet de l' **éditeur** .</span><span class="sxs-lookup"><span data-stu-id="7161f-235">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="7161f-236">Appuyez sur `Ctrl` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.</span><span class="sxs-lookup"><span data-stu-id="7161f-236">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="7161f-237">DevTools corrige le fichier JS complet dans le moteur JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7161f-237">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Volet éditeur" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="7161f-239">Volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="7161f-239">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <span data-ttu-id="7161f-240">Désactiver JavaScript</span><span class="sxs-lookup"><span data-stu-id="7161f-240">Disable JavaScript</span></span>   

<span data-ttu-id="7161f-241">[Pour plus d’devtools, voir Disable JavaScript with Microsoft Edge][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="7161f-241">See [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <span data-ttu-id="7161f-242">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7161f-242">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="7161f-248">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7161f-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7161f-249">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="7161f-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="7161f-251">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7161f-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
