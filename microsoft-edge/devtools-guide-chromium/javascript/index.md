---
description: Découvrez comment utiliser Microsoft Edge DevTools pour rechercher et corriger les bogues JavaScript.
title: Commencer à utiliser le débogage de JavaScript dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325946"
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
# <span data-ttu-id="d97c3-104">Commencer à déboguer JavaScript dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d97c3-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d97c3-105">Cet article vous apprend le flux de travail de base pour le débogage d’un problème JavaScript dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="d97c3-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="d97c3-106">Étape 1 : Reproduire le bogue</span><span class="sxs-lookup"><span data-stu-id="d97c3-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="d97c3-107">La recherche d’une série d’actions qui reproduisent systématiquement un bogue est toujours la première étape du débogage.</span><span class="sxs-lookup"><span data-stu-id="d97c3-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="d97c3-108">Choose **Open Demo**.</span><span class="sxs-lookup"><span data-stu-id="d97c3-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="d97c3-109">Maintenez `Control` \(Windows, Linux\) ou `Command` \(macOS\) et ouvrez la démonstration dans un nouvel onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="d97c3-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="d97c3-110">Démonstration ouverte</span><span class="sxs-lookup"><span data-stu-id="d97c3-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="d97c3-111">Entrez `5` dans la zone de texte Numéro **1.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="d97c3-112">Entrez `1` dans la zone de texte Numéro **2.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="d97c3-113">Choose **Add Number 1 and Number 2**.</span><span class="sxs-lookup"><span data-stu-id="d97c3-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="d97c3-114">L’étiquette sous le bouton indique `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="d97c3-115">Le résultat doit être `6` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-115">The result should be `6`.</span></span>  <span data-ttu-id="d97c3-116">Ensuite, corrigez l’erreur d’ajout qui est le bogue.</span><span class="sxs-lookup"><span data-stu-id="d97c3-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 entraîne 51, mais doit être 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="d97c3-118">résultats `51` dans , mais doit être</span><span class="sxs-lookup"><span data-stu-id="d97c3-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="d97c3-119">Étape 2 : Familiarisez-vous avec l’interface utilisateur du panneau Sources</span><span class="sxs-lookup"><span data-stu-id="d97c3-119">Step 2: Get familiar with the Sources panel UI</span></span>  

<span data-ttu-id="d97c3-120">DevTools fournit de nombreux outils différents pour différentes tâches.</span><span class="sxs-lookup"><span data-stu-id="d97c3-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="d97c3-121">Les différentes tâches incluent la modification du CSS, le profilage des performances de chargement de page et la surveillance des demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="d97c3-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="d97c3-122">Le **panneau Sources** est l’endroit où vous déboguer JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d97c3-122">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="d97c3-123">Ouvrez DevTools en appuyant sur `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="d97c3-123">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="d97c3-124">Ce raccourci ouvre le panneau **Console.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-124">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Panneau console" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="d97c3-126">**L’outil Console**</span><span class="sxs-lookup"><span data-stu-id="d97c3-126">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d97c3-127">Choisissez **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-127">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Panneau Sources" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="d97c3-129">Panneau **Sources**</span><span class="sxs-lookup"><span data-stu-id="d97c3-129">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d97c3-130">**L’interface utilisateur** du panneau Sources est en trois parties.</span><span class="sxs-lookup"><span data-stu-id="d97c3-130">The **Sources** panel UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Les 3 parties de l’interface utilisateur du panneau Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="d97c3-132">Les 3 parties de l’interface utilisateur **du panneau Sources**</span><span class="sxs-lookup"><span data-stu-id="d97c3-132">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="d97c3-133">Volet **Navigateur de** fichiers \(Section 1 dans la figure précédente\).</span><span class="sxs-lookup"><span data-stu-id="d97c3-133">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="d97c3-134">Chaque fichier demandé par la page web est répertorié ici.</span><span class="sxs-lookup"><span data-stu-id="d97c3-134">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="d97c3-135">Volet **Éditeur** de code \(Section 2 dans la figure précédente\).</span><span class="sxs-lookup"><span data-stu-id="d97c3-135">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="d97c3-136">Après avoir sélectionné un fichier dans **le** volet Navigateur de fichiers, le contenu de ce fichier s’affiche ici.</span><span class="sxs-lookup"><span data-stu-id="d97c3-136">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="d97c3-137">Volet **Debugging JavaScript** \(Section 3 dans la figure précédente\).</span><span class="sxs-lookup"><span data-stu-id="d97c3-137">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="d97c3-138">Divers outils permettant d’inspecter javaScript pour la page web.</span><span class="sxs-lookup"><span data-stu-id="d97c3-138">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="d97c3-139">Si votre fenêtre DevTools est large, ce volet s’affiche à droite du volet Éditeur **de** code.</span><span class="sxs-lookup"><span data-stu-id="d97c3-139">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="d97c3-140">Étape 3 : Suspendre le code avec un point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="d97c3-140">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="d97c3-141">Une méthode courante pour le débogage de ce type de problème consiste à insérer plusieurs instructions dans le code, puis à inspecter les valeurs à mesure que `console.log()` le script s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d97c3-141">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="d97c3-142">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="d97c3-142">For example:</span></span>  

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

<span data-ttu-id="d97c3-143">La méthode peut faire le travail, mais les points d’arrêt `console.log()` le sont plus rapidement. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d97c3-143">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="d97c3-144">Un point d’arrêt vous permet de suspendre votre code au milieu de l’runtime et d’examiner toutes les valeurs à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="d97c3-144">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="d97c3-145">Les points d’arrêt ont quelques avantages par rapport à la `console.log()` méthode :</span><span class="sxs-lookup"><span data-stu-id="d97c3-145">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="d97c3-146">Avec , vous devez ouvrir manuellement le code source, trouver le code approprié, insérer les instructions, puis actualiser la page web pour afficher les messages dans `console.log()` `console.log()` la **console**.</span><span class="sxs-lookup"><span data-stu-id="d97c3-146">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="d97c3-147">Avec les points d’arrêt, vous pouvez suspendre le code pertinent sans même savoir comment le code est structuré.</span><span class="sxs-lookup"><span data-stu-id="d97c3-147">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="d97c3-148">Dans vos `console.log()` instructions, vous devez spécifier explicitement chaque valeur que vous souhaitez inspecter.</span><span class="sxs-lookup"><span data-stu-id="d97c3-148">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="d97c3-149">Avec les points d’arrêt, DevTools affiche les valeurs de toutes les variables à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="d97c3-149">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="d97c3-150">Parfois, les variables qui affectent votre code sont masquées et obscurcies.</span><span class="sxs-lookup"><span data-stu-id="d97c3-150">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="d97c3-151">En bref, les points d’arrêt peuvent vous aider à trouver et corriger les bogues plus rapidement que la `console.log()` méthode.</span><span class="sxs-lookup"><span data-stu-id="d97c3-151">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="d97c3-152">Si vous revenir en arrière et réfléchissez au fonctionnement de l’application, vous pouvez deviner que la somme incorrecte \( \) est calculée dans l’écoute d’événements associée au bouton Ajouter le numéro 1 et le numéro `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-152">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="d97c3-153">Ainsi, vous souhaitez probablement suspendre le code au moment où `click` l’écoute s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d97c3-153">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="d97c3-154">**Les points d’arrêt du lanceur d’événements** vous permet d’y faire exactement les choses :</span><span class="sxs-lookup"><span data-stu-id="d97c3-154">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="d97c3-155">Dans le **volet Débogage JavaScript,** sélectionnez Points d’arrêt de l’écoute d’événements pour développer la section. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d97c3-155">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="d97c3-156">DevTools révèle une liste de catégories d’événements ex expandables, telles que **Animation** et **Presse-papiers.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-156">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="d97c3-157">En de côté de la **catégorie d’événement Mouse,** choisissez **Expand** \( Expand ![ icon ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d97c3-157">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="d97c3-158">DevTools révèle une liste d’événements de souris, tels que **le** clic et **le clic avec la souris.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-158">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="d97c3-159">Chaque événement dispose d’une case à cocher en regard.</span><span class="sxs-lookup"><span data-stu-id="d97c3-159">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="d97c3-160">Cochez la case en regard de **cliquer.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-160">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="d97c3-161">DevTools est désormais installé pour être automatiquement suspendu lors de l’erreur `click` d’événements.</span><span class="sxs-lookup"><span data-stu-id="d97c3-161">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Sélectionnez la case à cocher en regard de cliquer" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="d97c3-163">Sélectionnez la case à cocher en regard de **cliquer**</span><span class="sxs-lookup"><span data-stu-id="d97c3-163">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d97c3-164">De retour à la démonstration, choisissez de nouveau **Ajouter le numéro 1 et le numéro 2.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-164">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="d97c3-165">DevTools interrompt la démonstration et met en évidence une ligne de code dans le **panneau Sources.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-165">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="d97c3-166">DevTools doit s’interrompre sur la ligne 16 dans `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-166">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="d97c3-167">Si vous faites une pause sur une autre ligne de code, appuyez sur Reprendre l’exécution du **script** \( Reprendre l’exécution du script \) jusqu’à ce que vous arrêtiez ![ sur la ligne ][ImageResumeIcon] correcte.</span><span class="sxs-lookup"><span data-stu-id="d97c3-167">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d97c3-168">Si vous avez suspendu sur une autre ligne, vous avez une extension de navigateur qui inscrit un listener d’événement sur chaque `click` page web que vous visitez.</span><span class="sxs-lookup"><span data-stu-id="d97c3-168">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="d97c3-169">Vous avez été suspendu dans `click` l’écoute de l’extension.</span><span class="sxs-lookup"><span data-stu-id="d97c3-169">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="d97c3-170">Si vous utilisez le mode InPrivate pour parcourir en privé **,** ce qui désactive toutes les extensions, vous pouvez voir que vous mettez en pause la ligne de code souhaitée à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="d97c3-170">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="d97c3-171">**Les points d’arrêt de l’écoute** d’événements ne sont qu’un des nombreux types de points d’arrêt disponibles dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="d97c3-171">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="d97c3-172">Mémorisez tous les différents types pour vous aider à déboguer les différents scénarios aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="d97c3-172">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="d97c3-173">Étape 4 : Procédure pas à pas dans le code</span><span class="sxs-lookup"><span data-stu-id="d97c3-173">Step 4: Step through the code</span></span>  

<span data-ttu-id="d97c3-174">Une cause courante de bogues est lorsqu’un script s’exécute dans un mauvais ordre.</span><span class="sxs-lookup"><span data-stu-id="d97c3-174">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="d97c3-175">La procédure pas à pas de votre code vous permet de parcourir l’runtime de votre code.</span><span class="sxs-lookup"><span data-stu-id="d97c3-175">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="d97c3-176">Vous pouvez parcourir une ligne à la fois pour déterminer exactement où votre code s’exécute dans un ordre différent de celui prévu.</span><span class="sxs-lookup"><span data-stu-id="d97c3-176">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="d97c3-177">Essayez maintenant :</span><span class="sxs-lookup"><span data-stu-id="d97c3-177">Try it now:</span></span>  

1.  <span data-ttu-id="d97c3-178">Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d97c3-178">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="d97c3-179">DevTools exécute le code suivant sans y aller pas à pas.</span><span class="sxs-lookup"><span data-stu-id="d97c3-179">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="d97c3-180">DevTools ignore quelques lignes de code.</span><span class="sxs-lookup"><span data-stu-id="d97c3-180">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="d97c3-181">En effet, étant donné que la qualité est false, le `inputsAreEmpty()` bloc de code de l’instruction ne `if` s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="d97c3-181">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="d97c3-182">Dans le panneau **Sources** de DevTools, sélectionnez Pas à pas dans l’appel de fonction suivante **\(** Pas à pas dans l’appel de fonction suivant \) pour exécuter la fonction, ligne par ![ ][ImageIntoIcon] `updateLabel()` ligne.</span><span class="sxs-lookup"><span data-stu-id="d97c3-182">On the **Sources** panel of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="d97c3-183">Passer en revue une ligne à la fois est l’idée de base qui consiste à passer en revue le code pas à pas.</span><span class="sxs-lookup"><span data-stu-id="d97c3-183">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="d97c3-184">Si vous regardez le code dans , vous voyez que le bogue se trouve probablement quelque `get-started.js` part dans la `updateLabel()` fonction.</span><span class="sxs-lookup"><span data-stu-id="d97c3-184">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="d97c3-185">Au lieu d’aller pas à pas dans chaque ligne de code, vous pouvez utiliser un autre type de point d’arrêt pour suspendre le code plus près de l’emplacement probable du bogue.</span><span class="sxs-lookup"><span data-stu-id="d97c3-185">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="d97c3-186">Étape 5 : Définir un point d’arrêt de ligne de code</span><span class="sxs-lookup"><span data-stu-id="d97c3-186">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="d97c3-187">Les points d’arrêt de ligne de code sont le type de point d’arrêt le plus courant.</span><span class="sxs-lookup"><span data-stu-id="d97c3-187">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="d97c3-188">Lorsque vous arrivez à la ligne de code spécifique que vous souhaitez suspendre, utilisez un point d’arrêt de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="d97c3-188">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="d97c3-189">Regardez la dernière ligne de code dans `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="d97c3-189">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="d97c3-190">À gauche, le numéro de cette ligne de code particulière s’affiche sous la couleur **34**.</span><span class="sxs-lookup"><span data-stu-id="d97c3-190">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="d97c3-191">Choisissez la **ligne 34**.</span><span class="sxs-lookup"><span data-stu-id="d97c3-191">Choose line **34**.</span></span>  <span data-ttu-id="d97c3-192">DevTools place une icône rouge à gauche de **34**.</span><span class="sxs-lookup"><span data-stu-id="d97c3-192">DevTools puts a red icon to the left of **34**.</span></span>  <span data-ttu-id="d97c3-193">L’icône rouge indique qu’un point d’arrêt de ligne de code se trouve sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="d97c3-193">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="d97c3-194">DevTools s’interrompt toujours avant l’utilisation de cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="d97c3-194">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="d97c3-195">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d97c3-195">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="d97c3-196">Le script continue d’être en cours d’exécution jusqu’à atteindre la ligne 33.</span><span class="sxs-lookup"><span data-stu-id="d97c3-196">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="d97c3-197">Sur les lignes 31, 32 et 33, DevTools imprime les valeurs de , et à droite du point-virgule sur `addend1` `addend2` chaque `sum` ligne.</span><span class="sxs-lookup"><span data-stu-id="d97c3-197">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools s’interrompt sur le point d’arrêt de ligne de code sur la ligne 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="d97c3-199">DevTools s’interrompt sur le point d’arrêt de ligne de code sur la ligne 34</span><span class="sxs-lookup"><span data-stu-id="d97c3-199">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d97c3-200">Étape 6 : Vérifier les valeurs des variables</span><span class="sxs-lookup"><span data-stu-id="d97c3-200">Step 6: Check variable values</span></span>  

<span data-ttu-id="d97c3-201">Les valeurs `addend1` de , `addend2` et `sum` semblent suspectes.</span><span class="sxs-lookup"><span data-stu-id="d97c3-201">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="d97c3-202">Les valeurs sont wrapped entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="d97c3-202">The values are wrapped in quotes.</span></span>  <span data-ttu-id="d97c3-203">Les guillemets signifient que la valeur est une chaîne, ce qui constitue une bonne hypothèse pour expliquer la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="d97c3-203">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="d97c3-204">Recueillez plus d’informations sur la situation.</span><span class="sxs-lookup"><span data-stu-id="d97c3-204">Gather more information about the situation.</span></span>  <span data-ttu-id="d97c3-205">DevTools fournit de nombreux outils pour examiner les valeurs des variables.</span><span class="sxs-lookup"><span data-stu-id="d97c3-205">DevTools provides many tools for examining variable values.</span></span>  

### <span data-ttu-id="d97c3-206">Méthode 1 : volet d’étendue</span><span class="sxs-lookup"><span data-stu-id="d97c3-206">Method 1: The Scope pane</span></span>  

<span data-ttu-id="d97c3-207">Si vous faites une pause \*\*\*\* sur une ligne de code, le volet Étendue affiche les variables locales et globales actuellement définies, ainsi que la valeur de chaque variable.</span><span class="sxs-lookup"><span data-stu-id="d97c3-207">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="d97c3-208">Il affiche également les variables de fermeture, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d97c3-208">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="d97c3-209">Double-cliquez sur une valeur de variable pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="d97c3-209">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="d97c3-210">Si vous ne faites pas de pause sur une ligne de code, **le** volet d’étendue est vide.</span><span class="sxs-lookup"><span data-stu-id="d97c3-210">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Volet d’étendue" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="d97c3-212">Volet **d’étendue**</span><span class="sxs-lookup"><span data-stu-id="d97c3-212">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="d97c3-213">Méthode 2 : Expressions d’observation</span><span class="sxs-lookup"><span data-stu-id="d97c3-213">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="d97c3-214">Le **volet Expressions** observateurs vous permet de surveiller les valeurs des variables au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="d97c3-214">The **Watch Expressions** pane lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="d97c3-215">Comme son nom l’indique, les **expressions** d’observation ne sont pas limitées aux variables.</span><span class="sxs-lookup"><span data-stu-id="d97c3-215">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="d97c3-216">Vous pouvez stocker n’importe quelle expression JavaScript valide dans une **expression d’observation.**</span><span class="sxs-lookup"><span data-stu-id="d97c3-216">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="d97c3-217">Essayez maintenant.</span><span class="sxs-lookup"><span data-stu-id="d97c3-217">Try it now.</span></span>  

1.  <span data-ttu-id="d97c3-218">Choisissez le **volet** d’observation.</span><span class="sxs-lookup"><span data-stu-id="d97c3-218">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="d97c3-219">Choose **Add Expression** \( Add Expression ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d97c3-219">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="d97c3-220">Entrez `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="d97c3-220">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="d97c3-221">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-221">Select `Enter`.</span></span>  <span data-ttu-id="d97c3-222">DevTools affiche `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-222">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="d97c3-223">La valeur à droite du deux-points est le résultat de votre Expression d’observation.</span><span class="sxs-lookup"><span data-stu-id="d97c3-223">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="d97c3-224">Dans le **volet Expression** de l’observation \(en bas à droite\) de la figure suivante, l’Expression `typeof sum` d’observation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d97c3-224">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="d97c3-225">Si votre fenêtre DevTools est grande, le volet **Expression** d’observation se trouve à droite au-dessus du volet Points d’arrêt de l’écoute d’événements. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d97c3-225">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Volet d’expression d’observation" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="d97c3-227">Volet **d’expression** d’observation</span><span class="sxs-lookup"><span data-stu-id="d97c3-227">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="d97c3-228">Comme on le suspecte, `sum` est évalué en tant que chaîne, lorsqu’il doit s’agit d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="d97c3-228">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="d97c3-229">Vous avez maintenant confirmé que le type de valeur est la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="d97c3-229">You now confirmed value type is the cause of the bug.</span></span>  

### <span data-ttu-id="d97c3-230">Méthode 3 : Console</span><span class="sxs-lookup"><span data-stu-id="d97c3-230">Method 3: The Console</span></span>  

<span data-ttu-id="d97c3-231">La **console** vous permet d’afficher les messages et vous pouvez également l’utiliser pour évaluer des `console.log()` instructions JavaScript arbitraires.</span><span class="sxs-lookup"><span data-stu-id="d97c3-231">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="d97c3-232">Pour le débogage, vous pouvez utiliser la **console** pour tester les correctifs potentiels pour les bogues.</span><span class="sxs-lookup"><span data-stu-id="d97c3-232">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="d97c3-233">Essayez maintenant.</span><span class="sxs-lookup"><span data-stu-id="d97c3-233">Try it now.</span></span>  

1.  <span data-ttu-id="d97c3-234">Si le caisse de la **console** est fermé, `Escape` sélectionnez-le pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="d97c3-234">If the **Console** drawer is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="d97c3-235">Le **panneau** console s’ouvre dans le panneau inférieur de la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="d97c3-235">The **Console** drawer opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="d97c3-236">Dans la **console,** tapez `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-236">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="d97c3-237">L’instruction de l’outil est suspendue sur une ligne de code où `addend1` et se trouve dans `addend2` l’étendue.</span><span class="sxs-lookup"><span data-stu-id="d97c3-237">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="d97c3-238">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-238">Select `Enter`.</span></span>  <span data-ttu-id="d97c3-239">DevTools évalue l’instruction et imprime, ce qui est le résultat que vous attendez de `6` la démonstration.</span><span class="sxs-lookup"><span data-stu-id="d97c3-239">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Le caisse de la console, après avoir évalué parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="d97c3-241">Le caisse **de** la console, après évaluation</span><span class="sxs-lookup"><span data-stu-id="d97c3-241">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="d97c3-242">Étape 7 : Appliquer un correctif</span><span class="sxs-lookup"><span data-stu-id="d97c3-242">Step 7: Apply a fix</span></span>  

<span data-ttu-id="d97c3-243">Si vous trouvez un correctif pour le bogue, essayez votre correctif en éditant le code et en réruisant la démonstration.</span><span class="sxs-lookup"><span data-stu-id="d97c3-243">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="d97c3-244">Vous pouvez modifier le code JavaScript directement dans l’interface utilisateur de DevTools et appliquer le correctif.</span><span class="sxs-lookup"><span data-stu-id="d97c3-244">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="d97c3-245">Essayez maintenant.</span><span class="sxs-lookup"><span data-stu-id="d97c3-245">Try it now.</span></span>  

1.  <span data-ttu-id="d97c3-246">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d97c3-246">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="d97c3-247">Dans **l’Éditeur de code,** remplacez la ligne 32, `var sum = addend1 + addend2` par `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="d97c3-247">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="d97c3-248">Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer votre modification.</span><span class="sxs-lookup"><span data-stu-id="d97c3-248">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="d97c3-249">Choisissez **Désactiver les points d’arrêt** \( Désactiver les points ![ d’arrêt ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d97c3-249">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="d97c3-250">Il change de bleu pour indiquer que l’option est active.</span><span class="sxs-lookup"><span data-stu-id="d97c3-250">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="d97c3-251">Lorsque **les points d’arrêt Deactivate sont définies,** DevTools ignore les points d’arrêt que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="d97c3-251">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="d97c3-252">Essayez la démonstration avec des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="d97c3-252">Try out the demo with different values.</span></span>  <span data-ttu-id="d97c3-253">La démonstration calcule maintenant correctement.</span><span class="sxs-lookup"><span data-stu-id="d97c3-253">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="d97c3-254">Ce flux de travail applique uniquement un correctif au code en cours d’exécution dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="d97c3-254">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="d97c3-255">Il ne corrige pas le code pour tous les utilisateurs qui visitent votre page web.</span><span class="sxs-lookup"><span data-stu-id="d97c3-255">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="d97c3-256">Pour ce faire, vous devez corriger le code qui se trouve sur vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="d97c3-256">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="d97c3-257">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d97c3-257">Next steps</span></span>  

<span data-ttu-id="d97c3-258">Félicitations!</span><span class="sxs-lookup"><span data-stu-id="d97c3-258">Congratulations!</span></span>  <span data-ttu-id="d97c3-259">Vous savez maintenant comment utiliser microsoft Edge DevTools lors du débogage de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d97c3-259">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="d97c3-260">Les outils et méthodes que vous avez appris dans cet article peuvent vous faire gagner un nombre d’heures.</span><span class="sxs-lookup"><span data-stu-id="d97c3-260">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="d97c3-261">Cet article vous a appris uniquement deux façons de définir des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="d97c3-261">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="d97c3-262">DevTools offre de nombreuses autres façons, y compris les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="d97c3-262">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="d97c3-263">Points d’arrêt conditionnels qui ne sont déclenchés que lorsque la condition que vous fournissez est vraie.</span><span class="sxs-lookup"><span data-stu-id="d97c3-263">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="d97c3-264">Points d’arrêt sur les exceptions capturées ou non.</span><span class="sxs-lookup"><span data-stu-id="d97c3-264">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="d97c3-265">Points d’arrêt XHR déclenchés lorsque l’URL demandée correspond à une sous-stration que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="d97c3-265">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="d97c3-266">Pour plus d’informations sur le moment et la façon d’utiliser chaque type, accédez à [Suspendre votre code avec des points d’arrêt.][DevtoolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="d97c3-266">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="d97c3-267">Quelques contrôles de code pas à pas ne sont pas expliqués dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d97c3-267">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="d97c3-268">Pour plus d’informations, [accédez à la ligne de code][DevtoolsJavascriptReferenceStepThroughCode]Pas à pas.</span><span class="sxs-lookup"><span data-stu-id="d97c3-268">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <span data-ttu-id="d97c3-269">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="d97c3-269">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Code pas à pas : référence de débogage JavaScript | Documents Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Ouvrir le | Glitch"  

> [!NOTE]
> <span data-ttu-id="d97c3-273">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d97c3-273">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d97c3-274">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="d97c3-274">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="d97c3-276">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d97c3-276">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
