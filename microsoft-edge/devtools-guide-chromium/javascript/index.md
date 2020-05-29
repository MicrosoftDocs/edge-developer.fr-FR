---
title: Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 06df1fd4d6457a3f02be85b95959bdc353865495
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581823"
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







# <span data-ttu-id="62272-103">Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="62272-103">Get Started with Debugging JavaScript in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="62272-104">Ce didacticiel décrit le flux de travail de base pour le débogage d’un problème JavaScript dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="62272-104">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="62272-105">Étape 1: reproduire le bogue</span><span class="sxs-lookup"><span data-stu-id="62272-105">Step 1: Reproduce the bug</span></span>   

<span data-ttu-id="62272-106">La recherche d’une série d’actions qui reproduit régulièrement un bogue est toujours la première étape du débogage.</span><span class="sxs-lookup"><span data-stu-id="62272-106">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="62272-107">Cliquez sur **ouvrir la démonstration**.</span><span class="sxs-lookup"><span data-stu-id="62272-107">Click **Open Demo**.</span></span>  <span data-ttu-id="62272-108">Maintenez `Control` \ (Windows \) ou `Command` \ (MacOS \) et ouvrez la démonstration dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="62272-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  

    <span data-ttu-id="62272-109">[Ouvrir la démonstration] [OpenDebugJSDemo]</span><span class="sxs-lookup"><span data-stu-id="62272-109">[Open Demo][OpenDebugJSDemo]</span></span>  

1.  <span data-ttu-id="62272-110">Entrez `5` dans la zone de texte **numéro 1** .</span><span class="sxs-lookup"><span data-stu-id="62272-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="62272-111">Entrez `1` dans la zone de texte **numéro 2** .</span><span class="sxs-lookup"><span data-stu-id="62272-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="62272-112">Cliquez sur **Ajouter un numéro 1 et sur numéro 2**.</span><span class="sxs-lookup"><span data-stu-id="62272-112">Click **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="62272-113">L’étiquette sous le bouton indique `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="62272-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="62272-114">Le résultat doit être `6` .</span><span class="sxs-lookup"><span data-stu-id="62272-114">The result should be `6`.</span></span>  <span data-ttu-id="62272-115">Voici le bogue que vous allez résoudre.</span><span class="sxs-lookup"><span data-stu-id="62272-115">This is the bug you are going to fix.</span></span>  
    
    > ##### <span data-ttu-id="62272-116">Figure1</span><span class="sxs-lookup"><span data-stu-id="62272-116">Figure 1</span></span>  
    > <span data-ttu-id="62272-117">Le résultat de la valeur `5 + 1` `51` , mais doit être</span><span class="sxs-lookup"><span data-stu-id="62272-117">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    > ![Le résultat de 5 + 1 est 51, mais devrait être 6][ImageJSBugs]  

## <span data-ttu-id="62272-119">Étape 2: Familiarisez-vous avec l’interface utilisateur du panneau sources</span><span class="sxs-lookup"><span data-stu-id="62272-119">Step 2: Get familiar with the Sources panel UI</span></span>   

<span data-ttu-id="62272-120">DevTools fournit un grand nombre d’outils différents pour différentes tâches, comme le changement de CSS, la performance de chargement de la page de profil et la surveillance des requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="62272-120">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="62272-121">Le panneau **sources** vous permet de déboguer JavaScript.</span><span class="sxs-lookup"><span data-stu-id="62272-121">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="62272-122">Ouvrez devtools en appuyant sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="62272-122">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="62272-123">Ce raccourci ouvre le panneau de la **console** .</span><span class="sxs-lookup"><span data-stu-id="62272-123">This shortcut opens the **Console** panel.</span></span>  
    
    > ##### <span data-ttu-id="62272-124">Figure 2</span><span class="sxs-lookup"><span data-stu-id="62272-124">Figure 2</span></span>  
    > <span data-ttu-id="62272-125">Panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="62272-125">The **Console** panel</span></span>  
    > ![Panneau de la console][ImageJSConsole]  

1.  <span data-ttu-id="62272-127">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="62272-127">Click the **Sources** tab.</span></span>  
    
    > ##### <span data-ttu-id="62272-128">Figure3</span><span class="sxs-lookup"><span data-stu-id="62272-128">Figure 3</span></span>  
    > <span data-ttu-id="62272-129">Panneau **sources**</span><span class="sxs-lookup"><span data-stu-id="62272-129">The **Sources** panel</span></span>  
    > ![Panneau sources][ImageJSSources]  

<span data-ttu-id="62272-131">L’interface utilisateur du panneau **sources** comporte 3 parties:</span><span class="sxs-lookup"><span data-stu-id="62272-131">The **Sources** panel UI has 3 parts:</span></span>  

> ##### <span data-ttu-id="62272-132">Figure 4</span><span class="sxs-lookup"><span data-stu-id="62272-132">Figure 4</span></span>  
> <span data-ttu-id="62272-133">Les 3 parties de l’interface utilisateur du panneau **sources**</span><span class="sxs-lookup"><span data-stu-id="62272-133">The 3 parts of the **Sources** panel UI</span></span>  
> ![Les 3 parties de l’interface utilisateur du panneau sources][ImageJSSourcesAnnotated]  

1.  <span data-ttu-id="62272-135">Le volet **navigateur de fichiers** \ (section 1 dans la [figure 4](#figure-4)\).</span><span class="sxs-lookup"><span data-stu-id="62272-135">The **File Navigator** pane \(Section 1 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="62272-136">Chaque fichier mentionné dans la page est répertorié ici.</span><span class="sxs-lookup"><span data-stu-id="62272-136">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="62272-137">Le volet de l' **éditeur de code** (section 2 dans la [figure 4](#figure-4)\).</span><span class="sxs-lookup"><span data-stu-id="62272-137">The **Code Editor** pane \(Section 2 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="62272-138">Après avoir sélectionné un fichier dans le volet **navigateur de fichiers** , le contenu de ce fichier est affiché ici.</span><span class="sxs-lookup"><span data-stu-id="62272-138">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="62272-139">Le volet de **débogage JavaScript** \ (section 3 de la [figure 4](#figure-4)\).</span><span class="sxs-lookup"><span data-stu-id="62272-139">The **JavaScript Debugging** pane \(Section 3 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="62272-140">Différents outils d’examen du code JavaScript pour la page.</span><span class="sxs-lookup"><span data-stu-id="62272-140">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="62272-141">Si votre fenêtre DevTools est large, ce volet est affiché à droite du volet de l' **éditeur de code** .</span><span class="sxs-lookup"><span data-stu-id="62272-141">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  

## <span data-ttu-id="62272-142">Étape 3: mettre en pause le code avec un point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="62272-142">Step 3: Pause the code with a breakpoint</span></span>   

<span data-ttu-id="62272-143">Une méthode courante pour le débogage d’un problème comme celui-ci consiste à insérer un grand nombre d' `console.log()` instructions dans le code afin d’inspecter les valeurs lors de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="62272-143">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="62272-144">Exemple:</span><span class="sxs-lookup"><span data-stu-id="62272-144">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="62272-145">La `console.log()` méthode peut être exécutée, mais les **points d’arrêt** peuvent être plus productifs.</span><span class="sxs-lookup"><span data-stu-id="62272-145">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="62272-146">Un point d’arrêt vous permet d’interrompre votre code au milieu du runtime et d’examiner toutes les valeurs à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="62272-146">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="62272-147">Les points d’arrêt présentent quelques avantages par rapport à la `console.log()` méthode:</span><span class="sxs-lookup"><span data-stu-id="62272-147">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="62272-148">Avec `console.log()` , vous devez ouvrir manuellement le code source, Rechercher le code approprié, insérer les `console.log()` instructions, puis recharger la page pour afficher les messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="62272-148">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="62272-149">Avec les points d’arrêt, vous pouvez mettre en pause le code concerné sans même savoir comment le code est structuré.</span><span class="sxs-lookup"><span data-stu-id="62272-149">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="62272-150">Dans vos `console.log()` instructions, vous devez spécifier explicitement chaque valeur que vous voulez inspecter.</span><span class="sxs-lookup"><span data-stu-id="62272-150">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="62272-151">Les points d’arrêt DevTools vous montrent les valeurs de toutes les variables à ce moment précis.</span><span class="sxs-lookup"><span data-stu-id="62272-151">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="62272-152">Parfois, il existe des variables affectant votre code.</span><span class="sxs-lookup"><span data-stu-id="62272-152">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="62272-153">En bref, les points d’arrêt permettent de rechercher et de résoudre les bogues plus rapidement que la `console.log()` méthode.</span><span class="sxs-lookup"><span data-stu-id="62272-153">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="62272-154">Si vous vous prenez reculer et réfléchir au fonctionnement de l’application, vous pouvez faire en sorte que la somme incorrecte ( `5 + 1 = 51` ) soit calculée dans l' `click` écouteur d’événements associé au bouton **Ajouter un numéro 1 et 2** .</span><span class="sxs-lookup"><span data-stu-id="62272-154">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="62272-155">Par conséquent, il est probable que vous souhaitiez suspendre le code au bout du temps d’exécution de l' `click` écouteur.</span><span class="sxs-lookup"><span data-stu-id="62272-155">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="62272-156">Les **points d’arrêt écouteur d’événements** vous permettent d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="62272-156">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="62272-157">Dans le volet **débogage JavaScript** , cliquez sur **points d’arrêt de l’écouteur d’événements** pour développer la section.</span><span class="sxs-lookup"><span data-stu-id="62272-157">In the **JavaScript Debugging** pane, click **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="62272-158">DevTools affiche une liste des catégories d’événements pouvant être développés, telles que l' **animation** et le **presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="62272-158">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="62272-159">En regard de la catégorie d’événement de **souris** , cliquez sur **développer** l' ![ icône développer ][ImageExpandIcon] .</span><span class="sxs-lookup"><span data-stu-id="62272-159">Next to the **Mouse** event category, click **Expand** ![Expand icon][ImageExpandIcon].</span></span>  <span data-ttu-id="62272-160">DevTools révèle une liste d’événements de souris tels que **Click** et **MouseDown**.</span><span class="sxs-lookup"><span data-stu-id="62272-160">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="62272-161">Une case à cocher est associée à chaque événement.</span><span class="sxs-lookup"><span data-stu-id="62272-161">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="62272-162">Cochez la case **cliquez sur** .</span><span class="sxs-lookup"><span data-stu-id="62272-162">Check the **click** checkbox.</span></span>  <span data-ttu-id="62272-163">DevTools est désormais configuré pour s’arrêter automatiquement lors *de l’exécution d’un* `click` écouteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="62272-163">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    > ##### <span data-ttu-id="62272-164">Figure 5</span><span class="sxs-lookup"><span data-stu-id="62272-164">Figure 5</span></span>  
    > <span data-ttu-id="62272-165">La case à cocher **Cliquer** est activée</span><span class="sxs-lookup"><span data-stu-id="62272-165">The **click** checkbox is enabled</span></span>  
    > ![La case à cocher cliquer est activée][ImageJSClickCheckbox]  
    
1.  <span data-ttu-id="62272-167">Dans la démonstration, cliquez à nouveau sur **Ajouter un numéro 1 et sur numéro 2** .</span><span class="sxs-lookup"><span data-stu-id="62272-167">Back on the demo, click **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="62272-168">DevTools met en pause la démonstration et surligne une ligne de code dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="62272-168">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="62272-169">DevTools doit suspendre la ligne 16 `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="62272-169">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="62272-170">Si vous placez le pointeur sur une autre ligne de code, appuyez sur la touche reprise de l' **exécution** du script ![ ][ImageResumeIcon] jusqu’à ce que vous pointiez sur la ligne appropriée.</span><span class="sxs-lookup"><span data-stu-id="62272-170">If you pause on a different line of code, press **Resume Script Execution** ![Resume Script Execution][ImageResumeIcon] until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="62272-171">Si vous avez interrompu une autre ligne, vous disposez d’une extension de navigateur permettant d’inscrire un `click` écouteur d’événements sur chaque page que vous visitez.</span><span class="sxs-lookup"><span data-stu-id="62272-171">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="62272-172">Vous avez été suspendu dans l' `click` écouteur de l’extension.</span><span class="sxs-lookup"><span data-stu-id="62272-172">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="62272-173">Si vous utilisez le mode InPrivate pour effectuer une **recherche dans Private**, qui désactive toutes les extensions, il est possible que vous deviez suspendre chaque fois la ligne de code souhaitée.</span><span class="sxs-lookup"><span data-stu-id="62272-173">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="62272-174">Les **points d’arrêt écouteur d’événements** ne sont qu’un type de nombreux types de points d’arrêt disponibles dans devtools.</span><span class="sxs-lookup"><span data-stu-id="62272-174">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="62272-175">Il est recommandé de mémoriser tous les types différents, car chaque type de fichier vous permet de déboguer différents scénarios le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="62272-175">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="62272-176">Étape 4: parcourir le code</span><span class="sxs-lookup"><span data-stu-id="62272-176">Step 4: Step through the code</span></span>   

<span data-ttu-id="62272-177">L’une des causes les plus fréquentes est qu’un script s’exécute dans un ordre incorrect.</span><span class="sxs-lookup"><span data-stu-id="62272-177">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="62272-178">Le passage en revue de votre code vous permet de parcourir le runtime de votre code, une ligne à la fois, et de rechercher exactement à l’endroit où il s’exécute dans un ordre différent de ce que vous attendiez.</span><span class="sxs-lookup"><span data-stu-id="62272-178">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="62272-179">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="62272-179">Try it now:</span></span>  

1.  <span data-ttu-id="62272-180">Cliquez sur passer à la fonction **suivante lors** d’un ![ appel de fonction ][ImageOverIcon] .</span><span class="sxs-lookup"><span data-stu-id="62272-180">Click **Step over next function call** ![Step over next function call][ImageOverIcon].</span></span>  <span data-ttu-id="62272-181">DevTools exécute le code suivant sans s’y exécuter.</span><span class="sxs-lookup"><span data-stu-id="62272-181">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  

    > [!NOTE]
    > <span data-ttu-id="62272-182">DevTools ignore quelques lignes de code.</span><span class="sxs-lookup"><span data-stu-id="62272-182">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="62272-183">Étant donné que l’argument `inputsAreEmpty()` évalue la valeur false, le bloc de code de l' `if` instruction ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="62272-183">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  

1.  <span data-ttu-id="62272-184">Dans le panneau **sources** de devtools, cliquez sur passer à la **fonction suivante** dans le ![ cadre de l’appel de fonction suivante ][ImageIntoIcon] pour passer d' `updateLabel()` une ligne à l’autre au moment de l’exécution de la fonction.</span><span class="sxs-lookup"><span data-stu-id="62272-184">On the **Sources** panel of DevTools, click **Step into next function call** ![Step into next function call][ImageIntoIcon] to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  

<span data-ttu-id="62272-185">Il s’agit de l’idée de base de l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="62272-185">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="62272-186">Si vous examinez le code dans `get-started.js` , vous constatez que le bogue est probablement quelque part dans la `updateLabel()` fonction.</span><span class="sxs-lookup"><span data-stu-id="62272-186">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="62272-187">Au lieu de parcourir chaque ligne de code, vous pouvez utiliser un autre type de point d’arrêt pour mettre le code plus près de l’emplacement probable du bogue.</span><span class="sxs-lookup"><span data-stu-id="62272-187">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="62272-188">Étape 5: définir un point d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="62272-188">Step 5: Set a line-of-code breakpoint</span></span>   

<span data-ttu-id="62272-189">Les points d’arrêt de la ligne sont le type le plus courant de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="62272-189">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="62272-190">Lorsque vous obtenez la ligne de code spécifique sur laquelle vous voulez mettre en pause, utilisez un point d’arrêt de ligne de code:</span><span class="sxs-lookup"><span data-stu-id="62272-190">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="62272-191">Regardez la dernière ligne de code dans `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="62272-191">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="62272-192">À gauche du code figure le numéro de ligne de cette ligne de code particulière, qui est **33**.</span><span class="sxs-lookup"><span data-stu-id="62272-192">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="62272-193">Cliquez sur **33**.</span><span class="sxs-lookup"><span data-stu-id="62272-193">Click on **33**.</span></span>  <span data-ttu-id="62272-194">DevTools place une icône rouge à gauche de **33**.</span><span class="sxs-lookup"><span data-stu-id="62272-194">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="62272-195">Cela signifie qu’il y a un point d’arrêt de ligne de code sur ce trait.</span><span class="sxs-lookup"><span data-stu-id="62272-195">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="62272-196">DevTools est à présent mis en pause pour pouvoir exécuter cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="62272-196">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="62272-197">Cliquez **sur reprise de l’exécution** du script de ![ reprise ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="62272-197">Click **Resume script execution** ![Resume script execution][ImageResumeIcon].</span></span>  <span data-ttu-id="62272-198">Le script continue de s’exécuter jusqu’à ce qu’il atteigne la ligne 33.</span><span class="sxs-lookup"><span data-stu-id="62272-198">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="62272-199">Sur les lignes 30, 31 et 32, DevTools affiche les valeurs de `addend1` , `addend2` et `sum` à droite du point-virgule sur chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="62272-199">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    > ##### <span data-ttu-id="62272-200">Figure 6</span><span class="sxs-lookup"><span data-stu-id="62272-200">Figure 6</span></span>  
    > <span data-ttu-id="62272-201">DevTools s’arrête sur le point d’arrêt de ligne de code de la ligne 32</span><span class="sxs-lookup"><span data-stu-id="62272-201">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    > ![DevTools s’arrête sur le point d’arrêt de ligne de code de la ligne 32][ImageJSLineOfCodeBreakpoint]  

## <span data-ttu-id="62272-203">Étape 6: vérifier les valeurs des variables</span><span class="sxs-lookup"><span data-stu-id="62272-203">Step 6: Check variable values</span></span>   

<span data-ttu-id="62272-204">Les valeurs de `addend1` , `addend2` et il est `sum` suspect.</span><span class="sxs-lookup"><span data-stu-id="62272-204">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="62272-205">Ils sont encapsulés entre guillemets, ce qui signifie qu’il s’agit de chaînes.</span><span class="sxs-lookup"><span data-stu-id="62272-205">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="62272-206">C’est une bonne hypothèse d’expliquer la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="62272-206">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="62272-207">Maintenant, il est temps de recueillir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="62272-207">Now it is time to gather more information.</span></span>  <span data-ttu-id="62272-208">DevTools offre un grand nombre d’outils d’examen des valeurs des variables.</span><span class="sxs-lookup"><span data-stu-id="62272-208">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="62272-209">Méthode 1: volet d’étendue</span><span class="sxs-lookup"><span data-stu-id="62272-209">Method 1: The Scope pane</span></span>   

<span data-ttu-id="62272-210">Lorsque vous placez le pointeur sur une ligne de code, le volet de l' **étendue** vous indique quelles variables locales et globales sont actuellement définies, ainsi que la valeur de chaque variable.</span><span class="sxs-lookup"><span data-stu-id="62272-210">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="62272-211">Il affiche également les variables de fermeture, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="62272-211">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="62272-212">Double-cliquez sur une valeur de variable pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="62272-212">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="62272-213">Lorsque vous n’êtes pas en pause sur une ligne de code, le volet **étendue** est vide.</span><span class="sxs-lookup"><span data-stu-id="62272-213">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

> ##### <span data-ttu-id="62272-214">Figure 7</span><span class="sxs-lookup"><span data-stu-id="62272-214">Figure 7</span></span>  
> <span data-ttu-id="62272-215">Volet **cadre**</span><span class="sxs-lookup"><span data-stu-id="62272-215">The **Scope** pane</span></span>  
> ![Volet cadre][ImageJSScope]  

### <span data-ttu-id="62272-217">Méthode 2: espionner les expressions</span><span class="sxs-lookup"><span data-stu-id="62272-217">Method 2: Watch Expressions</span></span>   

<span data-ttu-id="62272-218">L’onglet **expressions espionnes** vous permet de surveiller les valeurs des variables dans le temps.</span><span class="sxs-lookup"><span data-stu-id="62272-218">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="62272-219">Comme son nom l’indique, les expressions espionnes ne sont pas simplement limitées aux variables.</span><span class="sxs-lookup"><span data-stu-id="62272-219">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="62272-220">Vous pouvez stocker toute expression JavaScript valide dans une expression espionne.</span><span class="sxs-lookup"><span data-stu-id="62272-220">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="62272-221">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="62272-221">Try it now:</span></span>  

1.  <span data-ttu-id="62272-222">Cliquez sur l’onglet **Espion** .</span><span class="sxs-lookup"><span data-stu-id="62272-222">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="62272-223">Cliquez sur **Ajouter** une expression ![ ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="62272-223">Click **Add Expression** ![Add Expression][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="62272-224">Entrez `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="62272-224">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="62272-225">Appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="62272-225">Press `Enter`.</span></span>  <span data-ttu-id="62272-226">DevTools affiche `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="62272-226">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="62272-227">La valeur à droite des deux-points est le résultat de l’expression espionne.</span><span class="sxs-lookup"><span data-stu-id="62272-227">The value to the right of the colon is the result of your Watch Expression.</span></span>  

> [!NOTE]
> <span data-ttu-id="62272-228">Dans le volet des expressions espionnes (en bas à droite) de la [figure 8](#figure-8), l' `typeof sum` expression espionne est affichée.</span><span class="sxs-lookup"><span data-stu-id="62272-228">In the Watch Expression pane \(bottom-right\) in [Figure 8](#figure-8), the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="62272-229">S’il s’agit d’une fenêtre de DevTools de grande taille, le volet d’expressions espionnes se trouve à droite au-dessus du volet de **points d’arrêt du détecteur d’événements** .</span><span class="sxs-lookup"><span data-stu-id="62272-229">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

> ##### <span data-ttu-id="62272-230">Figure8</span><span class="sxs-lookup"><span data-stu-id="62272-230">Figure 8</span></span>  
> <span data-ttu-id="62272-231">Volet expression espionner</span><span class="sxs-lookup"><span data-stu-id="62272-231">The Watch Expression pane</span></span>  
> ![Volet expression espionner][ImageJSWatchExpression]  

<span data-ttu-id="62272-233">Comme soupçonné, `sum` est évaluée en tant que chaîne, lorsqu’il devrait s’agir d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="62272-233">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="62272-234">Vous avez vérifié qu’il s’agit de la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="62272-234">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="62272-235">Méthode 3: la console</span><span class="sxs-lookup"><span data-stu-id="62272-235">Method 3: The Console</span></span>   

<span data-ttu-id="62272-236">En plus de l’affichage des `console.log()` messages, vous pouvez également utiliser la console pour évaluer des instructions JavaScript arbitraires.</span><span class="sxs-lookup"><span data-stu-id="62272-236">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="62272-237">En termes de débogage, vous pouvez utiliser la console pour tester les correctifs potentiels pour les bogues.</span><span class="sxs-lookup"><span data-stu-id="62272-237">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="62272-238">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="62272-238">Try it now:</span></span>  

1.  <span data-ttu-id="62272-239">Si le tiroir de la console n’est pas ouvert, appuyez sur `Escape` pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="62272-239">If you do not have the Console drawer open, press `Escape` to open it.</span></span>  <span data-ttu-id="62272-240">Il s’ouvre en bas de la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="62272-240">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="62272-241">Dans la console, tapez `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="62272-241">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="62272-242">Cette instruction fonctionne, car vous êtes en pause sur une ligne de code où vous vous `addend1` `addend2` trouvez dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="62272-242">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="62272-243">Appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="62272-243">Press `Enter`.</span></span>  <span data-ttu-id="62272-244">DevTools évalue l’instruction et imprime `6` , ce qui correspond au résultat attendu que la démonstration produira.</span><span class="sxs-lookup"><span data-stu-id="62272-244">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  

> ##### <span data-ttu-id="62272-245">Figure9</span><span class="sxs-lookup"><span data-stu-id="62272-245">Figure 9</span></span>  
> <span data-ttu-id="62272-246">Le tiroir de la console, après évaluation</span><span class="sxs-lookup"><span data-stu-id="62272-246">The Console drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
> ![Le tiroir de la console, après avoir évalué le sein de l’arborescence (addend1) + sein (addend2)][ImageJSConsoleEvaluated]  

## <span data-ttu-id="62272-248">Étape 7: appliquer un correctif</span><span class="sxs-lookup"><span data-stu-id="62272-248">Step 7: Apply a fix</span></span>   

<span data-ttu-id="62272-249">Si vous trouvez un correctif pour le bogue, essayez de résoudre le problème en modifiant le code et en exécutant de nouveau la démonstration.</span><span class="sxs-lookup"><span data-stu-id="62272-249">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="62272-250">Vous n’avez pas besoin de quitter DevTools pour appliquer le correctif.</span><span class="sxs-lookup"><span data-stu-id="62272-250">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="62272-251">Vous pouvez modifier le code JavaScript directement dans l’interface utilisateur DevTools.</span><span class="sxs-lookup"><span data-stu-id="62272-251">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="62272-252">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="62272-252">Try it now:</span></span>  

1.  <span data-ttu-id="62272-253">Cliquez **sur reprise de l’exécution** du script de ![ reprise ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="62272-253">Click **Resume script execution** ![Resume script execution][ImageResumeIcon].</span></span>  
1.  <span data-ttu-id="62272-254">Dans l' **éditeur de code**, remplacez ligne 32, `var sum = addend1 + addend2` par `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="62272-254">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="62272-255">Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="62272-255">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="62272-256">Cliquez sur désactiver les points d' **arrêt** ![ Désactiver les points d’arrêt ][ImageDeactivateIcon] .</span><span class="sxs-lookup"><span data-stu-id="62272-256">Click **Deactivate breakpoints** ![Deactivate breakpoints][ImageDeactivateIcon].</span></span>  <span data-ttu-id="62272-257">Il change de bleu pour indiquer qu’il est actif.</span><span class="sxs-lookup"><span data-stu-id="62272-257">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="62272-258">Si cette valeur est définie, DevTools ignore les points d’arrêt que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="62272-258">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="62272-259">Testez la démonstration avec des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="62272-259">Try out the demo with different values.</span></span>  <span data-ttu-id="62272-260">La démonstration est désormais correctement calculée.</span><span class="sxs-lookup"><span data-stu-id="62272-260">The demo now calculates correctly.</span></span>  

> [!CAUTION]
> <span data-ttu-id="62272-261">Ce flux de travail s’applique uniquement au code exécuté dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="62272-261">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="62272-262">Cela ne résout pas le code de tous les utilisateurs visitant votre page.</span><span class="sxs-lookup"><span data-stu-id="62272-262">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="62272-263">Pour ce faire, vous devez résoudre le code qui se trouve sur vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="62272-263">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="62272-264">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="62272-264">Next steps</span></span>   

<span data-ttu-id="62272-265">Félicitations!</span><span class="sxs-lookup"><span data-stu-id="62272-265">Congratulations!</span></span>  <span data-ttu-id="62272-266">Vous savez maintenant comment tirer le meilleur parti de Microsoft Edge DevTools lors du débogage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="62272-266">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="62272-267">Les outils et méthodes que vous avez appris dans ce didacticiel pourront vous épargner des heures de comptage.</span><span class="sxs-lookup"><span data-stu-id="62272-267">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="62272-268">Ce didacticiel ne vous a montré que deux manières de définir des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="62272-268">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="62272-269">DevTools offre de nombreuses autres manières, notamment:</span><span class="sxs-lookup"><span data-stu-id="62272-269">DevTools offers many other ways, including:</span></span>  

*   <span data-ttu-id="62272-270">Les points d’arrêt conditionnel qui sont uniquement déclenchés lorsque la condition que vous spécifiez est vrai.</span><span class="sxs-lookup"><span data-stu-id="62272-270">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="62272-271">Points d’arrêt sur les exceptions interceptées ou non capturées.</span><span class="sxs-lookup"><span data-stu-id="62272-271">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="62272-272">XHR points d’arrêt qui sont déclenchés lorsque l’URL demandée correspond à une sous-chaîne que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="62272-272">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  

<!-- See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

<!--There are a couple of code stepping controls that were not explained in this tutorial.  See [Step over line of code][JSReferenceStepping] to learn more.  -->  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: /microsoft-edge/devtools-guide-chromium/media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageResumeIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  

[ImageJSBugs]: /microsoft-edge/devtools-guide-chromium/media/javascript-js-demo-bad.msft.png "Figure 1: le résultat de 5 + 1 est 51, mais devrait être 6"  
[ImageJSConsole]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-empty.msft.png "Figure 2: panneau de la console"  
[ImageJSSources]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections.msft.png "Figure 3: panneau sources"  
[ImageJSSourcesAnnotated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections-annotated.msft.png "Figure 4:3 parties de l’interface utilisateur du panneau sources"  
[ImageJSClickCheckbox]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png "Figure 5: la case à cocher Click est activée"  
[ImageJSLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused.msft.png "Figure 6: DevTools s’arrête sur le point d’arrêt de la ligne de code de la ligne 32"  
[ImageJSScope]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-scope.msft.png "Figure 7: volet d’étendue"  
[ImageJSWatchExpression]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-watch.msft.png "Figure 8: volet expression espionner"  
[ImageJSConsoleEvaluated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-console.msft.png "Le tiroir de la console, après avoir évalué le sein de l’arborescence (addend1) + sein (addend2)"  

<!-- links -->  

<!--[JSBreakpoints]: breakpoints.md "JavaScript Breakpoints"  -->  
<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->
[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "ouvrir une démonstration"  
<!--[JSReferenceStepping]: reference.md#stepping "Reference Stepping"  -->

> [!NOTE]
> <span data-ttu-id="62272-283">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="62272-283">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="62272-284">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="62272-284">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="62272-286">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="62272-286">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
