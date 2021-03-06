---
description: Découvrez les nouveaux flux de travail de débogage dans cette référence complète des fonctionnalités de débogage Microsoft Edge DevTools.
title: Référence de débogage JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 09a2d61269b2fe3a23a57ce58eb1c89b12a7639c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398475"
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

# <a name="javascript-debugging-reference"></a><span data-ttu-id="ff4b3-104">Référence de débogage JavaScript</span><span class="sxs-lookup"><span data-stu-id="ff4b3-104">JavaScript debugging reference</span></span>  

<span data-ttu-id="ff4b3-105">Découvrez les nouveaux flux de travail de débogage avec la référence complète suivante des fonctionnalités de débogage Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-105">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="ff4b3-106">Pour découvrir les principes de base du débogage, accédez à La mise en place du débogage JavaScript dans [Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span><span class="sxs-lookup"><span data-stu-id="ff4b3-106">To learn the basics of debugging, navigate to [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span></span>  

## <a name="pause-code-with-breakpoints"></a><span data-ttu-id="ff4b3-107">Suspendre le code avec des points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="ff4b3-107">Pause code with breakpoints</span></span>  

<span data-ttu-id="ff4b3-108">Définissez un point d’arrêt afin de pouvoir suspendre votre code au milieu de l’runtime.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-108">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="ff4b3-109">Pour découvrir comment définir des points d’arrêt, accédez à [Suspendre votre code avec des points d’arrêt.][DevToolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="ff4b3-109">To learn how to set breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="step-through-code"></a><span data-ttu-id="ff4b3-110">Code pas à pas</span><span class="sxs-lookup"><span data-stu-id="ff4b3-110">Step through code</span></span>  

<span data-ttu-id="ff4b3-111">Une fois que votre code est suspendu, pas à pas, une ligne à la fois, en enquêtant sur le flux de contrôle et les valeurs des propriétés en cours de route.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="ff4b3-112">Pas à pas avant la ligne de code</span><span class="sxs-lookup"><span data-stu-id="ff4b3-112">Step over line of code</span></span>  

<span data-ttu-id="ff4b3-113">Lorsqu’il est suspendu sur une ligne de code contenant une fonction qui n’est pas pertinente pour le problème que vous déboguer, choisissez le bouton Pas à pas principal **\(** Pas-à-pas \) pour exécuter la fonction sans y aller pas à ![ ][ImageStepOverIcon] pas.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, choose the **Step over** \(![Step over][ImageStepOverIcon]\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Choose Step over" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="ff4b3-115">Choose **Step over**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-115">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="ff4b3-116">Par exemple, supposons que vous déboguer l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-116">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="ff4b3-117">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-117">You are paused on `A`.</span></span>  <span data-ttu-id="ff4b3-118">Une fois que vous avez choisi **Pas**à pas, DevTools exécute tout le code dans la fonction que vous exécutez pas à pas, c’est-à-dire `B` et `C` .</span><span class="sxs-lookup"><span data-stu-id="ff4b3-118">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="ff4b3-119">DevTools s’interrompt ensuite sur `D` .</span><span class="sxs-lookup"><span data-stu-id="ff4b3-119">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="ff4b3-120">Pas à pas dans la ligne de code</span><span class="sxs-lookup"><span data-stu-id="ff4b3-120">Step into line of code</span></span>  

<span data-ttu-id="ff4b3-121">Lorsqu’il est suspendu sur une ligne de code contenant un appel de fonction lié au problème que vous déboguer, choisissez le bouton Pas à pas dans **\(** Pas à pas dans \) pour examiner cette fonction plus ![ en ][ImageStepIntoIcon] détail.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-121">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into][ImageStepIntoIcon]\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Choose Step into" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="ff4b3-123">Choose **Step into**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-123">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="ff4b3-124">Par exemple, supposons que vous déboguer l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-124">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="ff4b3-125">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-125">You are paused on `A`.</span></span>  <span data-ttu-id="ff4b3-126">Une fois que **vous avez choisi Pas à**pas, DevTools exécute cette ligne de code, puis s’interrompt. `B`</span><span class="sxs-lookup"><span data-stu-id="ff4b3-126">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="ff4b3-127">Sortir de la ligne de code</span><span class="sxs-lookup"><span data-stu-id="ff4b3-127">Step out of line of code</span></span>  

<span data-ttu-id="ff4b3-128">Lorsqu’il est suspendu à l’intérieur d’une fonction qui n’est pas liée au problème que vous déboguer, choisissez le bouton Pas **à** pas principal \( Pas à pas sortant \) pour exécuter le reste du code de la ![ ][ImageStepOutIcon] fonction.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-128">When paused inside of a function that is not related to the problem you are debugging, choose the **Step out** \(![Step out][ImageStepOutIcon]\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Choose Step out" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="ff4b3-130">Choose **Step out**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-130">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="ff4b3-131">Par exemple, supposons que vous déboguer l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-131">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="ff4b3-132">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-132">You are paused on `A`.</span></span>  <span data-ttu-id="ff4b3-133">Une fois que vous avez choisi Pas **à**pas, DevTools exécute le reste du code dans , qui se trouve juste dans cet exemple, puis `getName()` `B` s’interrompt. `C`</span><span class="sxs-lookup"><span data-stu-id="ff4b3-133">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="ff4b3-134">Exécuter tout le code jusqu’à une ligne spécifique</span><span class="sxs-lookup"><span data-stu-id="ff4b3-134">Run all code up to a specific line</span></span>  

<span data-ttu-id="ff4b3-135">Lors du débogage d’une fonction longue, il peut y avoir un grand nombre de code qui n’est pas lié au problème que vous déboguer.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="ff4b3-136">Vous pouvez choisir d’aller dans toutes les lignes, mais cela est fastidieux.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="ff4b3-137">Vous pouvez choisir de définir un point d’arrêt de ligne de code sur la ligne qui vous intéresse, puis de choisir le bouton Reprendre l’exécution de **script** \( Reprendre l’exécution de script \), mais il existe un moyen plus ![ ][ImageResumeScriptExecutionIcon] rapide.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button, but there is a faster way.</span></span>  

<span data-ttu-id="ff4b3-138">Pointez sur la ligne de code qui vous intéresse, ouvrez le menu contextuel \(clic droit\), puis choisissez **Continuer ici.**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-138">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="ff4b3-139">DevTools exécute l’ensemble du code jusqu’à ce point, puis s’interrompt sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Choose Continue to here" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="ff4b3-141">Choose **Continue to here**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-141">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="ff4b3-142">Redémarrer la fonction supérieure de la pile d’appels</span><span class="sxs-lookup"><span data-stu-id="ff4b3-142">Restart the top function of the call stack</span></span>  

<span data-ttu-id="ff4b3-143">Pour suspendre la première ligne de la fonction supérieure de votre pile d’appels, puis sur une ligne de code, pointez n’importe où dans le volet Pile des appels, ouvrez le menu contextuel \(clic droit\), puis choisissez Redémarrer le **cadre.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ff4b3-143">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart Frame**.</span></span>  <span data-ttu-id="ff4b3-144">La fonction supérieure est la dernière fonction qui a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="ff4b3-145">L’extrait de code suivant est un exemple de procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-145">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="ff4b3-146">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-146">You are paused on `A`.</span></span>  <span data-ttu-id="ff4b3-147">Après avoir choisi **l’image**de redémarrage, vous devez être suspendu, sans jamais définir de point d’arrêt ou choisir reprendre l’exécution `B` **du script.**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-147">After choosing **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Choisir un cadre de redémarrage" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="ff4b3-149">Choisir **un cadre de redémarrage**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-149">Choose **Restart Frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="ff4b3-150">Reprise du runtime de script</span><span class="sxs-lookup"><span data-stu-id="ff4b3-150">Resume script runtime</span></span>  

<span data-ttu-id="ff4b3-151">Pour poursuivre l’exécution après une pause de votre script, choisissez le bouton Reprendre l’exécution du **script** \( Reprendre l’exécution ![ du script ][ImageResumeScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ff4b3-151">To continue the runtime after a pause of your script, choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button.</span></span>  <span data-ttu-id="ff4b3-152">DevTools exécute le script jusqu’au point d’arrêt suivant, s’il y en a.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Choose Resume script execution" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="ff4b3-154">Choose **Resume script execution**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-154">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="ff4b3-155">Forcer le runtime du script</span><span class="sxs-lookup"><span data-stu-id="ff4b3-155">Force script runtime</span></span>  

<span data-ttu-id="ff4b3-156">Pour ignorer tous les points d’arrêt et forcer votre script à reprendre l’exécution, choisissez et maintenez le bouton Reprendre l’exécution du script **\(** Reprendre l’exécution du script \), puis choisissez le bouton Forcer l’exécution du script \( Forcer l’exécution du ![ ][ImageResumeScriptExecutionIcon] **script** ![ ][ImageForceScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ff4b3-156">To ignore all breakpoints and force your script to resume running, choose and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button and then choose the **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Choose Force script execution" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="ff4b3-158">Choose **Force script execution**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-158">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="ff4b3-159">Modifier le contexte du thread</span><span class="sxs-lookup"><span data-stu-id="ff4b3-159">Change thread context</span></span>  

<span data-ttu-id="ff4b3-160">Lorsque vous travaillez avec des travailleurs du web ou des travailleurs de service, choisissez un contexte répertorié dans le volet **Threads** pour basculer vers ce contexte.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-160">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="ff4b3-161">L’icône de flèche bleue représente le contexte actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Volet Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="ff4b3-163">Volet **Threads**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="ff4b3-164">Par exemple, supposons que vous êtes suspendu sur un point d’arrêt dans votre script principal et votre script de travail de service.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="ff4b3-165">Vous souhaitez afficher les propriétés locales et globales pour le contexte de travail de service, mais le panneau **Sources** affiche le contexte de script principal.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="ff4b3-166">En choisissant l’entrée de travail de service dans le volet **Threads,** vous devriez pouvoir basculer vers ce contexte.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-166">By choosing on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <a name="view-and-edit-local-closure-and-global-properties"></a><span data-ttu-id="ff4b3-167">Afficher et modifier les propriétés locales, de fermeture et globales</span><span class="sxs-lookup"><span data-stu-id="ff4b3-167">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="ff4b3-168">Bien qu’il soit suspendu sur \*\*\*\* une ligne de code, utilisez le volet Étendue pour afficher et modifier les valeurs des propriétés et des variables dans les étendues locale, de fermeture et globale.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="ff4b3-169">Double-cliquez sur une valeur de propriété pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="ff4b3-170">Les propriétés non éumables sont grisées.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Volet d’étendue" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="ff4b3-172">Volet **d’étendue**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-172">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="view-the-current-call-stack"></a><span data-ttu-id="ff4b3-173">Afficher la pile d’appels actuelle</span><span class="sxs-lookup"><span data-stu-id="ff4b3-173">View the current call stack</span></span>  

<span data-ttu-id="ff4b3-174">Bien qu’il soit suspendu sur \*\*\*\* une ligne de code, utilisez le volet Pile des appels pour afficher la pile d’appels qui vous a mis à ce point.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="ff4b3-175">Choisissez une entrée pour passer à la ligne de code où cette fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-175">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="ff4b3-176">L’icône de flèche bleue représente la fonction DevTools actuellement mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Volet Pile des appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="ff4b3-178">Volet **Pile des** appels</span><span class="sxs-lookup"><span data-stu-id="ff4b3-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ff4b3-179">Lorsqu’il n’est pas suspendu sur une ligne de code, le volet **Pile** des appels est vide.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="ff4b3-180">Copier la trace de pile</span><span class="sxs-lookup"><span data-stu-id="ff4b3-180">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="ff4b3-181">pour copier la pile d’appels actuelle dans \*\*\*\* le Presse-papiers, pointez n’importe où dans le volet Pile des appels, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier la trace de **pile.**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-181">to copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Choose Copy Stack Trace" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="ff4b3-183">Choose **Copy Stack Trace**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-183">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="ff4b3-184">L’extrait de code suivant est un exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-184">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="ff4b3-185">Ignorer un script ou un modèle de scripts</span><span class="sxs-lookup"><span data-stu-id="ff4b3-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="ff4b3-186">Marquez un script en tant que code de bibliothèque lorsque vous souhaitez ignorer ce script lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="ff4b3-187">Lorsqu’il est marqué comme code de \*\*\*\* bibliothèque, un script est masqué dans le volet Pile des appels et vous n’entrez jamais dans les fonctions du script lorsque vous avancez dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="ff4b3-188">L’extrait de code suivant est un exemple de procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-188">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="ff4b3-189">est une bibliothèque tierce de confiance.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="ff4b3-190">Si vous êtes certain que le problème que vous déboguer n’est pas lié à la bibliothèque tierce, il est logique de marquer le script comme du **code de bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="ff4b3-191">Marquer un script en tant que code de bibliothèque à partir du volet Éditeur</span><span class="sxs-lookup"><span data-stu-id="ff4b3-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="ff4b3-192">Effectuer les actions suivantes pour marquer un script en tant **que code de bibliothèque** à partir du volet Éditeur. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ff4b3-192">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="ff4b3-193">Ouvrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-193">Open the file.</span></span>  
1.  <span data-ttu-id="ff4b3-194">Pointez n’importe où et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="ff4b3-194">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="ff4b3-195">Choose **Mark as Library code**.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-195">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet Éditeur" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="ff4b3-197">Marquer un script en tant **que code de bibliothèque** à partir du volet Éditeur \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ff4b3-197">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="ff4b3-198">Marquer un script en tant que code de bibliothèque à partir du volet Pile des appels</span><span class="sxs-lookup"><span data-stu-id="ff4b3-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="ff4b3-199">Effectuer les actions suivantes pour marquer un script en tant que **code de** bibliothèque à partir du volet **Pile** des appels.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-199">Complete the following actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="ff4b3-200">Pointez sur une fonction à partir du script et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="ff4b3-200">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="ff4b3-201">Choose **Mark as Library code**.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-201">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet Pile des appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="ff4b3-203">Marquer un script en tant **que code de bibliothèque** à partir du volet **Pile** des appels</span><span class="sxs-lookup"><span data-stu-id="ff4b3-203">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="ff4b3-204">Marquer un script comme code de bibliothèque à partir des paramètres</span><span class="sxs-lookup"><span data-stu-id="ff4b3-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="ff4b3-205">Effectuer les actions suivantes pour marquer un seul script ou modèle de scripts à partir **des paramètres**.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-205">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="ff4b3-206">Ouvrez [Paramètres.][DevToolsCustomize]</span><span class="sxs-lookup"><span data-stu-id="ff4b3-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="ff4b3-207">Accédez au **paramètre de code** Bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-207">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="ff4b3-208">Choose **Add pattern**.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-208">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="ff4b3-209">Entrez le nom du script ou un modèle regex de noms de script à marquer en tant **que code de bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="ff4b3-210">Choose **Add**.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-210">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marquer un script comme code de bibliothèque à partir des paramètres" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="ff4b3-212">Marquer un script comme **code de bibliothèque** à partir des **paramètres**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-212">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="ff4b3-213">Exécuter des extraits de code de débogage à partir de n’importe quelle page</span><span class="sxs-lookup"><span data-stu-id="ff4b3-213">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="ff4b3-214">Si vous vous trouvez en cours d’exécution du même code de débogage dans la console, pensez à des extraits de code.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="ff4b3-215">Les extraits de code sont des scripts d’runtime que vous pouvez écrire, stocker et exécuter dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="ff4b3-216">Pour en savoir plus, accédez à Exécuter des extraits de code à [partir d’une page][DevToolsJavascriptSnippets]quelconque.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-216">To learn more, navigate to [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets].</span></span>  

## <a name="watch-the-values-of-custom-javascript-expressions"></a><span data-ttu-id="ff4b3-217">Regardez les valeurs des expressions JavaScript personnalisées</span><span class="sxs-lookup"><span data-stu-id="ff4b3-217">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="ff4b3-218">Utilisez le **volet** d’observation pour observer les valeurs des expressions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="ff4b3-219">Vous pouvez regarder n’importe quelle expression JavaScript valide.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Volet d’observation" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="ff4b3-221">Volet **d’observation**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="ff4b3-222">Sélectionnez **le bouton Ajouter une expression** \( Ajouter une expression ![ ][ImageAddExpressionIcon] \) pour créer une expression d’observation.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-222">Choose the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="ff4b3-223">Sélectionnez **le bouton Actualiser** \( Actualiser \) pour actualiser les ![ ][ImageRefreshIcon] valeurs de toutes les expressions existantes.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-223">Choose the **Refresh** \(![Refresh][ImageRefreshIcon]\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="ff4b3-224">Les valeurs s’actualisent automatiquement lors du code pas à pas.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="ff4b3-225">Pointez sur une expression et choisissez le bouton **Supprimer l’expression** \( ![ Supprimer l’expression ][ImageDeleteExpressionIcon] \) pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-225">Hover on an expression and choose the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) button to delete it.</span></span>  

## <a name="make-a-minified-file-readable"></a><span data-ttu-id="ff4b3-226">Rendre un fichier minifié lisible</span><span class="sxs-lookup"><span data-stu-id="ff4b3-226">Make a minified file readable</span></span>  

<span data-ttu-id="ff4b3-227">Choisissez le **bouton Format** \( Format \) pour rendre un fichier ![ ][ImageFormatIcon] minifié lisible par l’homme.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-227">Choose the **Format** \(![Format][ImageFormatIcon]\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Bouton Format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="ff4b3-229">Bouton **Format**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-229">The **Format** button</span></span>  
:::image-end:::  

## <a name="edit-a-script"></a><span data-ttu-id="ff4b3-230">Modifier un script</span><span class="sxs-lookup"><span data-stu-id="ff4b3-230">Edit a script</span></span>  

<span data-ttu-id="ff4b3-231">Lorsque vous corrigez un bogue, vous souhaitez souvent tester certaines modifications apportées à votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="ff4b3-232">Vous n’avez pas besoin d’apporter les modifications dans un éditeur externe ou IDE, puis d’actualiser la page.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-232">You do not need to make the changes in an external editor or IDE and then refresh the page.</span></span>  <span data-ttu-id="ff4b3-233">Vous pouvez modifier votre script dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="ff4b3-234">Effectuer les actions suivantes pour modifier un script.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-234">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="ff4b3-235">Ouvrez le fichier **dans** le volet Éditeur du panneau **Sources.**</span><span class="sxs-lookup"><span data-stu-id="ff4b3-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="ff4b3-236">A apporté vos modifications **dans** le volet Éditeur.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="ff4b3-237">Sélectionnez `Ctrl` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-237">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="ff4b3-238">DevTools correctifs tout le fichier JS dans le moteur JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Volet Éditeur" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="ff4b3-240">Volet \*\*\*\* Éditeur</span><span class="sxs-lookup"><span data-stu-id="ff4b3-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="disable-javascript"></a><span data-ttu-id="ff4b3-241">Désactiver JavaScript</span><span class="sxs-lookup"><span data-stu-id="ff4b3-241">Disable JavaScript</span></span>  

<span data-ttu-id="ff4b3-242">Accédez [à Désactiver JavaScript avec Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="ff4b3-242">Navigate to [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ff4b3-243">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ff4b3-243">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
[DevToolsJavascriptGetStarted]: ./index.md "Commencer à déboguer JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavascriptSnippets]: ./snippets.md "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCustomize]: ../customize/index.md "Personnaliser microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="ff4b3-249">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ff4b3-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ff4b3-250">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="ff4b3-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ff4b3-252">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ff4b3-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
