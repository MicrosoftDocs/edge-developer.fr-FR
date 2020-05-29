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







# <span data-ttu-id="caa23-103">Référence de débogage JavaScript</span><span class="sxs-lookup"><span data-stu-id="caa23-103">JavaScript Debugging Reference</span></span>   



<span data-ttu-id="caa23-104">Découvrez les nouveaux flux de travail de débogage grâce à cette référence complète des fonctionnalités de débogage de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="caa23-104">Discover new debugging workflows with this comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="caa23-105">Pour en savoir plus sur le [débogage, voir prendre en main le langage JavaScript dans Microsoft Edge devtools][DevToolsJavascriptGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="caa23-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="caa23-106">Suspendre le code avec des points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="caa23-106">Pause code with breakpoints</span></span>   

<span data-ttu-id="caa23-107">Définissez un point d’arrêt pour pouvoir mettre en pause votre code au milieu de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="caa23-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="caa23-108">Pour plus d’informations sur la façon de définir des points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="caa23-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools"  

## <span data-ttu-id="caa23-110">Parcourir le code</span><span class="sxs-lookup"><span data-stu-id="caa23-110">Step through code</span></span>   

<span data-ttu-id="caa23-111">Une fois votre code interrompu, parcourez-le, une ligne à la fois, en analysant le flux de contrôle et les valeurs de propriétés.</span><span class="sxs-lookup"><span data-stu-id="caa23-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="caa23-112">Étape au-dessus de la ligne de code</span><span class="sxs-lookup"><span data-stu-id="caa23-112">Step over line of code</span></span>   

<span data-ttu-id="caa23-113">Lorsque le curseur est en pause sur une ligne de code contenant une fonction qui n’est pas pertinente pour le problème que vous déboguez, cliquez **sur l’icône déplacée** ![ ][ImageStepOverIcon] au-dessus pour exécuter la fonction sans vous mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="caa23-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click on the **Step over** ![Step over][ImageStepOverIcon] icon to run the function without stepping into it.</span></span>  

> ##### <span data-ttu-id="caa23-114">Figure1</span><span class="sxs-lookup"><span data-stu-id="caa23-114">Figure 1</span></span>  
> <span data-ttu-id="caa23-115">Sélectionner **pas à pas**</span><span class="sxs-lookup"><span data-stu-id="caa23-115">Selecting **Step over**</span></span>  
> ![Sélectionner pas à pas][ImageSelectingStepOver]  

<span data-ttu-id="caa23-117">Par exemple, supposons que vous déboguez le code suivant:</span><span class="sxs-lookup"><span data-stu-id="caa23-117">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="caa23-118">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="caa23-118">You are paused on `A`.</span></span>  <span data-ttu-id="caa23-119">En appuyant sur la touche de **progression**, devtools exécute tout le code de la fonction que vous êtes en passe, c’est-à-dire `B` et `C` .</span><span class="sxs-lookup"><span data-stu-id="caa23-119">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="caa23-120">DevTools puis s’interrompt `D` .</span><span class="sxs-lookup"><span data-stu-id="caa23-120">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="caa23-121">Passer à la ligne de code</span><span class="sxs-lookup"><span data-stu-id="caa23-121">Step into line of code</span></span>   

<span data-ttu-id="caa23-122">Lorsqu’il est suspendu sur une ligne de code contenant un appel de fonction associé au problème que vous déboguez, cliquez sur l’icône **pas** à pas détaillé ![ ][ImageStepIntoIcon] pour examiner davantage cette fonction.</span><span class="sxs-lookup"><span data-stu-id="caa23-122">When paused on a line of code containing a function call that is related to the problem you are debugging, click on the **Step into** ![Step into][ImageStepIntoIcon] icon to investigate that function further.</span></span>  

> ##### <span data-ttu-id="caa23-123">Figure 2</span><span class="sxs-lookup"><span data-stu-id="caa23-123">Figure 2</span></span>  
> <span data-ttu-id="caa23-124">Sélection de la phase de mise **en forme**</span><span class="sxs-lookup"><span data-stu-id="caa23-124">Selecting **Step into**</span></span>  
> ![Sélection de la phase de mise en forme][ImageSelectingStepInto]  

<span data-ttu-id="caa23-126">Par exemple, supposons que vous déboguez le code suivant:</span><span class="sxs-lookup"><span data-stu-id="caa23-126">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="caa23-127">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="caa23-127">You are paused on `A`.</span></span>  <span data-ttu-id="caa23-128">En appuyant sur la touche **pas à pas**, devtools exécute cette ligne de code, puis arrête le suivi `B` .</span><span class="sxs-lookup"><span data-stu-id="caa23-128">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="caa23-129">Pas à pas hors ligne de code</span><span class="sxs-lookup"><span data-stu-id="caa23-129">Step out of line of code</span></span>   

<span data-ttu-id="caa23-130">Lorsque vous êtes interrompu à l’intérieur d’une fonction qui n’est pas associée au problème que vous déboguez, cliquez **sur l'** ![ icône Déconnexion en mode hors connexion ][ImageStepOutIcon] pour exécuter le reste du code de la fonction.</span><span class="sxs-lookup"><span data-stu-id="caa23-130">When paused inside of a function that is not related to the problem you are debugging, click on the **Step out** ![Step out][ImageStepOutIcon] icon to run the rest of the code of the function.</span></span>  

> ##### <span data-ttu-id="caa23-131">Figure3</span><span class="sxs-lookup"><span data-stu-id="caa23-131">Figure 3</span></span>  
> <span data-ttu-id="caa23-132">Sélection d’une **étape**</span><span class="sxs-lookup"><span data-stu-id="caa23-132">Selecting **Step out**</span></span>  
> ![Sélection d’une étape][ImageSelectingStepOut]  

<span data-ttu-id="caa23-134">Par exemple, supposons que vous déboguez le code suivant:</span><span class="sxs-lookup"><span data-stu-id="caa23-134">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="caa23-135">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="caa23-135">You are paused on `A`.</span></span>  <span data-ttu-id="caa23-136">En appuyant sur **sortir**, devtools exécute le reste du code dans `getName()` , qui est uniquement `B` dans cet exemple, puis il s’interrompt `C` .</span><span class="sxs-lookup"><span data-stu-id="caa23-136">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="caa23-137">Exécuter tout le code jusqu’à une ligne spécifique</span><span class="sxs-lookup"><span data-stu-id="caa23-137">Run all code up to a specific line</span></span>   

<span data-ttu-id="caa23-138">Lors du débogage d’une fonction longue, il peut y avoir un grand nombre de code qui n’est pas lié au problème que vous déboguez.</span><span class="sxs-lookup"><span data-stu-id="caa23-138">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="caa23-139">Vous pouvez passer d’une ligne à l’autres, mais cela est laborieux.</span><span class="sxs-lookup"><span data-stu-id="caa23-139">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="caa23-140">Vous pouvez décider de définir un point d’arrêt de ligne de code sur la ligne qui vous intéresse, puis de cliquer sur l’icône d’exécution du script de reprise d' **exécution** du script ![ ][ImageResumeScriptExecutionIcon] , mais il existe une méthode plus rapide.</span><span class="sxs-lookup"><span data-stu-id="caa23-140">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon, but there is a faster way.</span></span>  

<span data-ttu-id="caa23-141">Cliquez avec le bouton droit sur la ligne de code qui vous intéresse, puis sélectionnez **continuer pour accéder à la page suivante**.</span><span class="sxs-lookup"><span data-stu-id="caa23-141">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="caa23-142">DevTools exécute tout le code jusqu’à ce point, puis le met en pause.</span><span class="sxs-lookup"><span data-stu-id="caa23-142">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

> ##### <span data-ttu-id="caa23-143">Figure 4</span><span class="sxs-lookup"><span data-stu-id="caa23-143">Figure 4</span></span>  
> <span data-ttu-id="caa23-144">Sélectionner **toujours**</span><span class="sxs-lookup"><span data-stu-id="caa23-144">Selecting **Continue to here**</span></span>  
> ![Sélectionner toujours][ImageSelectingContinueToHere]  

### <span data-ttu-id="caa23-146">Redémarrez la fonction Top de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="caa23-146">Restart the top function of the call stack</span></span>   

<span data-ttu-id="caa23-147">Lorsque vous êtes en pause sur une ligne de code, cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez **redémarrer le cadre** pour suspendre la première ligne de la fonction Top dans votre pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="caa23-147">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="caa23-148">La fonction Top est la dernière fonction qui a été appelée.</span><span class="sxs-lookup"><span data-stu-id="caa23-148">The top function is the last function that was called.</span></span>  

<span data-ttu-id="caa23-149">Par exemple, supposons que vous effectuiez le code suivant:</span><span class="sxs-lookup"><span data-stu-id="caa23-149">For example, suppose you are stepping through the following code:</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="caa23-150">Vous êtes en pause `A` .</span><span class="sxs-lookup"><span data-stu-id="caa23-150">You are paused on `A`.</span></span>  <span data-ttu-id="caa23-151">Après avoir cliqué sur **redémarrage**de l’image, vous devez être suspendu `B` , sans définir de point d’arrêt ou en appuyant sur **l’exécution du script de reprise**.</span><span class="sxs-lookup"><span data-stu-id="caa23-151">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

> ##### <span data-ttu-id="caa23-152">Figure 5</span><span class="sxs-lookup"><span data-stu-id="caa23-152">Figure 5</span></span>  
> <span data-ttu-id="caa23-153">Sélection du **cadre de reprise**</span><span class="sxs-lookup"><span data-stu-id="caa23-153">Selecting **Restart Frame**</span></span>  
> ![Sélection du cadre de reprise][ImageSelectingRestartFrame]  

### <span data-ttu-id="caa23-155">Exécution du script de reprise</span><span class="sxs-lookup"><span data-stu-id="caa23-155">Resume script runtime</span></span>   

<span data-ttu-id="caa23-156">Pour poursuivre le runtime suite à une pause de votre script, cliquez sur l’icône d’exécution du script **de reprise d'** exécution du script ![ ][ImageResumeScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="caa23-156">To continue the runtime after a pause of your script, click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon.</span></span>  <span data-ttu-id="caa23-157">DevTools exécute le script jusqu’au prochain point d’arrêt, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="caa23-157">DevTools runs the script up until the next breakpoint, if any.</span></span>  

> ##### <span data-ttu-id="caa23-158">Figure 6</span><span class="sxs-lookup"><span data-stu-id="caa23-158">Figure 6</span></span>  
> <span data-ttu-id="caa23-159">Sélection de **l’exécution du script de reprise**</span><span class="sxs-lookup"><span data-stu-id="caa23-159">Selecting **Resume script execution**</span></span>  
> ![Sélection de l’exécution du script de reprise][ImageSelectingResumeScriptExecution]  

#### <span data-ttu-id="caa23-161">Forcer le runtime de script</span><span class="sxs-lookup"><span data-stu-id="caa23-161">Force script runtime</span></span>   

<span data-ttu-id="caa23-162">Pour ignorer tous les points d’arrêt et forcer votre script à s’exécuter, cliquez de façon prolongée sur l’icône d’exécution du script de reprise de l' **exécution** du script ![ ][ImageResumeScriptExecutionIcon] **Force script execution** ![ ][ImageForceScriptExecutionIcon]</span><span class="sxs-lookup"><span data-stu-id="caa23-162">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon and then select **Force script execution** ![Force script execution][ImageForceScriptExecutionIcon].</span></span>  

> ##### <span data-ttu-id="caa23-163">Figure 7</span><span class="sxs-lookup"><span data-stu-id="caa23-163">Figure 7</span></span>  
> <span data-ttu-id="caa23-164">Sélectionner **forcer l’exécution du script**</span><span class="sxs-lookup"><span data-stu-id="caa23-164">Selecting **Force script execution**</span></span>  
> ![Sélectionner forcer l’exécution du script][ImageSelectingForceScriptExecution]  

### <span data-ttu-id="caa23-166">Modification du contexte de thread</span><span class="sxs-lookup"><span data-stu-id="caa23-166">Change thread context</span></span>   

<span data-ttu-id="caa23-167">Lorsque vous travaillez avec des travailleurs Web ou des travailleurs de service, cliquez sur un contexte répertorié dans le volet **Threads** pour basculer vers ce contexte.</span><span class="sxs-lookup"><span data-stu-id="caa23-167">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="caa23-168">L’icône de flèche bleue représente le contexte actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="caa23-168">The blue arrow icon represents which context is currently selected.</span></span>  

> ##### <span data-ttu-id="caa23-169">Figure8</span><span class="sxs-lookup"><span data-stu-id="caa23-169">Figure 8</span></span>  
> <span data-ttu-id="caa23-170">Le volet **Threads**</span><span class="sxs-lookup"><span data-stu-id="caa23-170">The **Threads** pane</span></span>  
> ![Le volet threads][ImageThreadsPane]  

<span data-ttu-id="caa23-172">Par exemple, supposons que vous soyez suspendu sur un point d’arrêt dans votre script principal et votre script de travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="caa23-172">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="caa23-173">Vous voulez afficher les propriétés locales et globales du contexte du travailleur de service, mais le panneau **sources** affiche le contexte de script principal.</span><span class="sxs-lookup"><span data-stu-id="caa23-173">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="caa23-174">En cliquant sur l’entrée du travailleur de service dans le volet **Threads** , vous devez être en mesure de basculer vers ce contexte.</span><span class="sxs-lookup"><span data-stu-id="caa23-174">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="caa23-175">Afficher et modifier les propriétés locales, de fermeture et globales</span><span class="sxs-lookup"><span data-stu-id="caa23-175">View and edit local, closure, and global properties</span></span>   

<span data-ttu-id="caa23-176">En pause sur une ligne de code, utilisez le volet **scope** pour afficher et modifier les valeurs des propriétés et variables des étendues locales, de fermeture et globales.</span><span class="sxs-lookup"><span data-stu-id="caa23-176">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="caa23-177">Double-cliquez sur une valeur de propriété pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="caa23-177">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="caa23-178">Les propriétés non Enumerable sont grisées.</span><span class="sxs-lookup"><span data-stu-id="caa23-178">Non-enumerable properties are greyed out.</span></span>  

> ##### <span data-ttu-id="caa23-179">Figure9</span><span class="sxs-lookup"><span data-stu-id="caa23-179">Figure 9</span></span>  
> <span data-ttu-id="caa23-180">Volet **cadre**</span><span class="sxs-lookup"><span data-stu-id="caa23-180">The **Scope** pane</span></span>  
> ![Volet cadre][ImageScopePane]  

## <span data-ttu-id="caa23-182">Afficher la pile d’appels actuelle</span><span class="sxs-lookup"><span data-stu-id="caa23-182">View the current call stack</span></span>   

<span data-ttu-id="caa23-183">Lorsque vous avez interrompu une ligne de code, utilisez le volet **pile d’appels** pour afficher la pile d’appels qui vous a donné ce point.</span><span class="sxs-lookup"><span data-stu-id="caa23-183">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="caa23-184">Cliquez sur une entrée pour accéder à la ligne de code où cette fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="caa23-184">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="caa23-185">L’icône de flèche bleue représente quelle fonction DevTools est actuellement en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="caa23-185">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

> ##### <span data-ttu-id="caa23-186">Figure10</span><span class="sxs-lookup"><span data-stu-id="caa23-186">Figure 10</span></span>  
> <span data-ttu-id="caa23-187">Volet **pile d’appels**</span><span class="sxs-lookup"><span data-stu-id="caa23-187">The **Call Stack** pane</span></span>  
> ![Volet pile d’appels][ImageCallStackPane]  

> [!NOTE]
> <span data-ttu-id="caa23-189">Lorsque vous n’êtes pas en pause sur une ligne de code, le volet **pile d’appels** est vide.</span><span class="sxs-lookup"><span data-stu-id="caa23-189">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="caa23-190">Copier la trace de pile</span><span class="sxs-lookup"><span data-stu-id="caa23-190">Copy stack trace</span></span>   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="caa23-191">Cliquez avec le bouton droit n’importe où dans le volet **pile d’appels** et sélectionnez Copier la **trace de pile** pour copier la pile d’appels actuelle dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="caa23-191">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

> ##### <span data-ttu-id="caa23-192">Figure11</span><span class="sxs-lookup"><span data-stu-id="caa23-192">Figure 11</span></span>  
> <span data-ttu-id="caa23-193">Sélection de l’option **copier la trace de pile**</span><span class="sxs-lookup"><span data-stu-id="caa23-193">Selecting **Copy Stack Trace**</span></span>  
> ![Sélection de l’option copier la trace de pile][ImageSelectingCopyStackTrace]  

<span data-ttu-id="caa23-195">Vous trouverez ci-dessous un exemple de sortie:</span><span class="sxs-lookup"><span data-stu-id="caa23-195">Below is an example of the output:</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="caa23-196">Ignorer un script ou un modèle de scripts</span><span class="sxs-lookup"><span data-stu-id="caa23-196">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="caa23-197">Marquez un script en tant que code de bibliothèque quand vous voulez ignorer ce script lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="caa23-197">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="caa23-198">Lorsqu’il est marqué comme code de la bibliothèque, un script est masqué dans le volet **pile d’appels** et vous n’êtes pas encore dans les fonctions du script lorsque vous parcourez votre code.</span><span class="sxs-lookup"><span data-stu-id="caa23-198">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="caa23-199">Par exemple, supposons que vous vous résoyez en exécutant ce code:</span><span class="sxs-lookup"><span data-stu-id="caa23-199">For example, suppose you are stepping through this code:</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="caa23-200">est une bibliothèque tierce digne de confiance.</span><span class="sxs-lookup"><span data-stu-id="caa23-200">is a third-party library that you trust.</span></span>  <span data-ttu-id="caa23-201">Si vous êtes sûr que le problème que vous déboguez n’est pas lié à la bibliothèque tierce, il est préférable de marquer le script en tant que **code**de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="caa23-201">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="caa23-202">Marquer un script en tant que code de bibliothèque à partir du volet éditeur</span><span class="sxs-lookup"><span data-stu-id="caa23-202">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="caa23-203">Pour marquer un script en tant que **Code de bibliothèque** à partir du volet **éditeur** :</span><span class="sxs-lookup"><span data-stu-id="caa23-203">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="caa23-204">Ouvrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="caa23-204">Open the file.</span></span>  
1.  <span data-ttu-id="caa23-205">Cliquez avec le bouton droit n’importe où.</span><span class="sxs-lookup"><span data-stu-id="caa23-205">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="caa23-206">Sélectionnez **marquer en tant que code de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="caa23-206">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="caa23-207">Figure12</span><span class="sxs-lookup"><span data-stu-id="caa23-207">Figure 12</span></span>  
> <span data-ttu-id="caa23-208">Marquage d’un script en tant que **Code de bibliothèque** à partir du volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="caa23-208">Marking a script as **Library code** from the **Editor** pane</span></span>  
> ![Marquage d’un script en tant que code de bibliothèque à partir du volet éditeur][ImageMarkEditorPane]  

### <span data-ttu-id="caa23-210">Marquer un script en tant que code de bibliothèque à partir du volet pile d’appels</span><span class="sxs-lookup"><span data-stu-id="caa23-210">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="caa23-211">Pour marquer un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels** :</span><span class="sxs-lookup"><span data-stu-id="caa23-211">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="caa23-212">Cliquez avec le bouton droit sur une fonction à partir du script.</span><span class="sxs-lookup"><span data-stu-id="caa23-212">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="caa23-213">Sélectionnez **marquer en tant que code de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="caa23-213">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="caa23-214">Figure13</span><span class="sxs-lookup"><span data-stu-id="caa23-214">Figure 13</span></span>  
> <span data-ttu-id="caa23-215">Marquage d’un script en tant que **Code de bibliothèque** à partir du volet **pile d’appels**</span><span class="sxs-lookup"><span data-stu-id="caa23-215">Marking a script as **Library code** from the **Call Stack** pane</span></span>  
> ![Marquage d’un script en tant que code de bibliothèque à partir du volet pile d’appels][ImageMarkCallStackPane]  

### <span data-ttu-id="caa23-217">Marquer un script en tant que code de bibliothèque à partir des paramètres</span><span class="sxs-lookup"><span data-stu-id="caa23-217">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="caa23-218">Pour marquer un script unique ou un modèle de scripts dans les paramètres:</span><span class="sxs-lookup"><span data-stu-id="caa23-218">To mark a single script or pattern of scripts from Settings:</span></span>  

1.  <span data-ttu-id="caa23-219">Ouvrez [paramètres][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="caa23-219">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="caa23-220">Accédez à l’onglet Code de la **bibliothèque** .</span><span class="sxs-lookup"><span data-stu-id="caa23-220">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="caa23-221">Cliquez sur **Ajouter un modèle**.</span><span class="sxs-lookup"><span data-stu-id="caa23-221">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="caa23-222">Entrez le nom du script ou un modèle Regex de noms de script pour le marquer comme code de la **bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="caa23-222">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="caa23-223">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="caa23-223">Click **Add**.</span></span>  

> ##### <span data-ttu-id="caa23-224">Figure14</span><span class="sxs-lookup"><span data-stu-id="caa23-224">Figure 14</span></span>  
> <span data-ttu-id="caa23-225">Marquage d’un script en tant que **Code de bibliothèque** à partir des paramètres</span><span class="sxs-lookup"><span data-stu-id="caa23-225">Marking a script as **Library code** from Settings</span></span>  
> ![Marquage d’un script en tant que code de bibliothèque à partir des paramètres][ImageMarkScriptSettings]  

## <span data-ttu-id="caa23-227">Exécuter des extraits de code de débogage à partir de n’importe quelle page</span><span class="sxs-lookup"><span data-stu-id="caa23-227">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="caa23-228">Si vous vous retrouvez vous exécutez le même code de débogage dans la console que sur et sur le passé, considérez les extraits de code.</span><span class="sxs-lookup"><span data-stu-id="caa23-228">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="caa23-229">Les extraits sont des scripts d’exécution que vous créez, stockez et exécutez dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="caa23-229">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="caa23-230">Pour en savoir plus, voir [exécution d’extraits de code à partir de n’importe quelle page][DevToolsJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="caa23-230">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="caa23-231">Regardez les valeurs des expressions JavaScript personnalisées</span><span class="sxs-lookup"><span data-stu-id="caa23-231">Watch the values of custom JavaScript expressions</span></span>   

<span data-ttu-id="caa23-232">Utilisez le volet **Espion** pour surveiller les valeurs des expressions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="caa23-232">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="caa23-233">Vous pouvez voir une expression JavaScript valide.</span><span class="sxs-lookup"><span data-stu-id="caa23-233">You may watch any valid JavaScript expression.</span></span>  

> ##### <span data-ttu-id="caa23-234">Figure15</span><span class="sxs-lookup"><span data-stu-id="caa23-234">Figure 15</span></span>  
> <span data-ttu-id="caa23-235">Volet **Espion**</span><span class="sxs-lookup"><span data-stu-id="caa23-235">The **Watch** pane</span></span>  
> ![Volet espion][ImageWatchPane]  

*   <span data-ttu-id="caa23-237">Cliquez sur l' **Add Expression** ![ icône Ajouter une expression ][ImageAddExpressionIcon] d’expression pour créer une expression espionne.</span><span class="sxs-lookup"><span data-stu-id="caa23-237">Click on the **Add Expression** ![Add Expression][ImageAddExpressionIcon] icon to create a new watch expression.</span></span>  
*   <span data-ttu-id="caa23-238">Cliquez sur l’icône Actualiser **Actualiser** ![ ][ImageRefreshIcon] pour actualiser les valeurs de toutes les expressions existantes.</span><span class="sxs-lookup"><span data-stu-id="caa23-238">Click on the **Refresh** ![Refresh][ImageRefreshIcon] icon to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="caa23-239">Les valeurs sont automatiquement actualisées lors de l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="caa23-239">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="caa23-240">Pointez sur une expression et cliquez sur l’icône Supprimer l' **expression** ![ ][ImageDeleteExpressionIcon] pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="caa23-240">Hover over an expression and click on the **Delete Expression** ![Delete Expression][ImageDeleteExpressionIcon] icon to delete it.</span></span>  

## <span data-ttu-id="caa23-241">Rendre un fichier minified lisible</span><span class="sxs-lookup"><span data-stu-id="caa23-241">Make a minified file readable</span></span>   

<span data-ttu-id="caa23-242">Cliquez **sur l'** ![ icône mise en forme du format ][ImageFormatIcon] pour rendre un fichier minified lisible par l’homme.</span><span class="sxs-lookup"><span data-stu-id="caa23-242">Click on the **Format** ![Format][ImageFormatIcon] icon to make a minified file human-readable.</span></span>  

> ##### <span data-ttu-id="caa23-243">Figure16</span><span class="sxs-lookup"><span data-stu-id="caa23-243">Figure 16</span></span>  
> <span data-ttu-id="caa23-244">Bouton **format**</span><span class="sxs-lookup"><span data-stu-id="caa23-244">The **Format** button</span></span>  
> ![Bouton format][ImageFormat]  

## <span data-ttu-id="caa23-246">Modification d’un script</span><span class="sxs-lookup"><span data-stu-id="caa23-246">Edit a script</span></span>   

<span data-ttu-id="caa23-247">Lors de la résolution d’un bogue, il est souvent préférable d’effectuer des tests dans votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="caa23-247">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="caa23-248">Vous n’avez pas besoin d’apporter des modifications dans un éditeur externe ou un IDE, puis de recharger la page.</span><span class="sxs-lookup"><span data-stu-id="caa23-248">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="caa23-249">Vous pouvez modifier votre script dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="caa23-249">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="caa23-250">Pour modifier un script:</span><span class="sxs-lookup"><span data-stu-id="caa23-250">To edit a script:</span></span>  

1.  <span data-ttu-id="caa23-251">Ouvrez le fichier dans le volet de l' **éditeur** du panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="caa23-251">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="caa23-252">Apportez les modifications souhaitées dans le volet de l' **éditeur** .</span><span class="sxs-lookup"><span data-stu-id="caa23-252">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="caa23-253">Appuyez sur `Ctrl` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.</span><span class="sxs-lookup"><span data-stu-id="caa23-253">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="caa23-254">DevTools corrige le fichier JS complet dans le moteur JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="caa23-254">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  

> ##### <span data-ttu-id="caa23-255">Figure17</span><span class="sxs-lookup"><span data-stu-id="caa23-255">Figure 17</span></span>  
> <span data-ttu-id="caa23-256">Volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="caa23-256">The **Editor** pane</span></span>  
> ![Volet éditeur][ImageEditorPane]  

## <span data-ttu-id="caa23-258">Désactiver JavaScript</span><span class="sxs-lookup"><span data-stu-id="caa23-258">Disable JavaScript</span></span>   

<span data-ttu-id="caa23-259">[Pour plus d’devtools, voir Disable JavaScript with Microsoft Edge][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="caa23-259">See [Disable JavaScript With Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

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
> <span data-ttu-id="caa23-281">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="caa23-281">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="caa23-282">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="caa23-282">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="caa23-284">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="caa23-284">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
