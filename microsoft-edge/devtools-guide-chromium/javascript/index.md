---
description: Découvrez comment utiliser Microsoft Edge DevTools pour rechercher et corriger les bogues JavaScript.
title: Commencer à déboguer JavaScript dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a60bd0c734df18ba7424cde6a828abbd9e7135a9
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519372"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a><span data-ttu-id="83ead-104">Commencer à déboguer JavaScript dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="83ead-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="83ead-105">Cet article vous apprend le flux de travail de base pour le débogage d'un problème JavaScript dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="83ead-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <a name="step-1-reproduce-the-bug"></a><span data-ttu-id="83ead-106">Étape 1 : Reproduire le bogue</span><span class="sxs-lookup"><span data-stu-id="83ead-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="83ead-107">La recherche d'une série d'actions qui reproduisent systématiquement un bogue est toujours la première étape du débogage.</span><span class="sxs-lookup"><span data-stu-id="83ead-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="83ead-108">Choisissez le lien **Ouvrir la démonstration** suivant et ouvrez la page web dans un nouvel onglet.  Pour ouvrir la démonstration dans un nouvel onglet, sélectionnez et maintenez `Ctrl` \(Windows, Linux\) ou `Command` \(macOS\), puis choisissez Ouvrir la **démonstration.**</span><span class="sxs-lookup"><span data-stu-id="83ead-108">Choose the following **Open Demo** link and open the webpage in a new tab.  To open the demo in a new tab, select and hold `Ctrl` \(Windows, Linux\) or `Command` \(macOS\), and then choose **Open Demo**.</span></span>  
    
    [<span data-ttu-id="83ead-109">Ouvrir la démonstration</span><span class="sxs-lookup"><span data-stu-id="83ead-109">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="83ead-110">Entrez `5` dans la zone de texte Numéro **1.**</span><span class="sxs-lookup"><span data-stu-id="83ead-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="83ead-111">Entrez `1` dans la zone de texte Numéro **2.**</span><span class="sxs-lookup"><span data-stu-id="83ead-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="83ead-112">Choose **Add Number 1 and Number 2**.</span><span class="sxs-lookup"><span data-stu-id="83ead-112">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="83ead-113">L'étiquette sous le bouton indique `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="83ead-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="83ead-114">Le résultat doit être `6` .</span><span class="sxs-lookup"><span data-stu-id="83ead-114">The result should be `6`.</span></span>  <span data-ttu-id="83ead-115">Ensuite, corrigez l'erreur d'ajout qui est le bogue.</span><span class="sxs-lookup"><span data-stu-id="83ead-115">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 entraîne 51, mais doit être 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="83ead-117">résultats `51` dans , mais doit être</span><span class="sxs-lookup"><span data-stu-id="83ead-117">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a><span data-ttu-id="83ead-118">Étape 2 : Familiarisez-vous avec l'interface utilisateur de l'outil Sources</span><span class="sxs-lookup"><span data-stu-id="83ead-118">Step 2: Get familiar with the Sources tool UI</span></span>  

<span data-ttu-id="83ead-119">DevTools fournit de nombreux outils différents pour différentes tâches.</span><span class="sxs-lookup"><span data-stu-id="83ead-119">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="83ead-120">Les différentes tâches incluent la modification du CSS, le profilage des performances de chargement de page et la surveillance des demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="83ead-120">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="83ead-121">**L'outil Sources** vous permet de déboguer JavaScript.</span><span class="sxs-lookup"><span data-stu-id="83ead-121">The **Sources** tool is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="83ead-122">Pour ouvrir **l'outil Console** dans DevTools, sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="83ead-122">To open the **Console** tool in DevTools, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="L'outil Console" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="83ead-124">**L'outil Console**</span><span class="sxs-lookup"><span data-stu-id="83ead-124">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83ead-125">Choisissez **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="83ead-125">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Outil Sources" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="83ead-127">Outil **Sources**</span><span class="sxs-lookup"><span data-stu-id="83ead-127">The **Sources** tool</span></span>  
    :::image-end:::  
    
<span data-ttu-id="83ead-128">**L'interface utilisateur** de l'outil Sources est en trois parties.</span><span class="sxs-lookup"><span data-stu-id="83ead-128">The **Sources** tool UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Les 3 parties de l'interface utilisateur de l'outil Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="83ead-130">Les 3 parties de l'interface utilisateur de l'outil **Sources**</span><span class="sxs-lookup"><span data-stu-id="83ead-130">The 3 parts of the **Sources** tool UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="83ead-131">Volet **Navigateur** \(Section 1 dans la figure précédente\).</span><span class="sxs-lookup"><span data-stu-id="83ead-131">The **Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="83ead-132">Chaque fichier demandé par la page web est répertorié ici.</span><span class="sxs-lookup"><span data-stu-id="83ead-132">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="83ead-133">Volet **Éditeur** \(Section 2 dans la figure précédente\).</span><span class="sxs-lookup"><span data-stu-id="83ead-133">The **Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="83ead-134">Une fois que vous avez choisi un fichier dans le volet **Navigateur,** ce volet affiche le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="83ead-134">After you choose a file in the **Navigator** pane, this pane displays the contents of the file.</span></span>  
1.  <span data-ttu-id="83ead-135">Volet **Débogger** \(Section 3 dans la figure précédente\).</span><span class="sxs-lookup"><span data-stu-id="83ead-135">The **Debugger** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="83ead-136">Ce volet fournit des outils permettant d'inspecter le JavaScript de la page web.</span><span class="sxs-lookup"><span data-stu-id="83ead-136">This pane provides tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="83ead-137">Si votre fenêtre DevTools est large, ce volet s'affiche à droite du **volet** Éditeur.</span><span class="sxs-lookup"><span data-stu-id="83ead-137">If your DevTools window is wide, this pane is displayed to the right of the **Editor** pane.</span></span>  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a><span data-ttu-id="83ead-138">Étape 3 : Suspendre le code avec un point d'arrêt</span><span class="sxs-lookup"><span data-stu-id="83ead-138">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="83ead-139">Une méthode courante pour le débogage de ce type de problème consiste à insérer plusieurs instructions dans le code, puis à inspecter les valeurs à mesure que `console.log()` le script s'exécute.</span><span class="sxs-lookup"><span data-stu-id="83ead-139">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="83ead-140">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="83ead-140">For example:</span></span>  

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

<span data-ttu-id="83ead-141">La méthode peut faire le travail, mais les points d'arrêt `console.log()` le sont plus rapidement. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="83ead-141">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="83ead-142">Un point d'arrêt vous permet de suspendre votre code au milieu de l'runtime et d'examiner toutes les valeurs à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="83ead-142">A breakpoint allows you to pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="83ead-143">Les points d'arrêt ont les avantages suivants par rapport à la `console.log()` méthode.</span><span class="sxs-lookup"><span data-stu-id="83ead-143">Breakpoints have the following advantages over the `console.log()` method.</span></span>  

*   <span data-ttu-id="83ead-144">Avec , vous devez ouvrir manuellement le code source, trouver le code approprié, insérer les instructions, puis actualiser la page web pour afficher les messages dans `console.log()` `console.log()` la **console**.</span><span class="sxs-lookup"><span data-stu-id="83ead-144">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="83ead-145">Avec les points d'arrêt, vous pouvez suspendre le code pertinent sans même savoir comment le code est structuré.</span><span class="sxs-lookup"><span data-stu-id="83ead-145">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="83ead-146">Dans vos `console.log()` instructions, vous devez spécifier explicitement chaque valeur que vous souhaitez inspecter.</span><span class="sxs-lookup"><span data-stu-id="83ead-146">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="83ead-147">Avec les points d'arrêt, DevTools vous montre les valeurs de toutes les variables à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="83ead-147">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="83ead-148">Parfois, les variables qui affectent votre code sont masquées et obscurcies.</span><span class="sxs-lookup"><span data-stu-id="83ead-148">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="83ead-149">En bref, les points d'arrêt peuvent vous aider à trouver et corriger les bogues plus rapidement que la `console.log()` méthode.</span><span class="sxs-lookup"><span data-stu-id="83ead-149">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="83ead-150">Si vous revenir en arrière et réfléchissez au fonctionnement de l'application, vous pouvez deviner que la somme incorrecte \( \) est calculée dans l'écoute d'événements associée au bouton Ajouter le numéro 1 et le numéro `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="83ead-150">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="83ead-151">Ainsi, vous souhaitez probablement suspendre le code au moment où `click` l'écoute s'exécute.</span><span class="sxs-lookup"><span data-stu-id="83ead-151">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="83ead-152">**Les points d'arrêt du lanceur d'événements** vous permet d'y faire exactement les choses :</span><span class="sxs-lookup"><span data-stu-id="83ead-152">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="83ead-153">Dans le **volet Débogger,** sélectionnez Points d'arrêt de l'écoute d'événements pour développer la section. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="83ead-153">In the **Debugger** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="83ead-154">DevTools révèle une liste de catégories d'événements ex expandables, telles que **l'animation** et **le Presse-papiers.**</span><span class="sxs-lookup"><span data-stu-id="83ead-154">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="83ead-155">En de côté de la **catégorie d'événement Mouse,** choisissez **Expand** \( Expand ![ icon ](../media/expand-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ead-155">Next to the **Mouse** event category, choose **Expand** \(![Expand icon](../media/expand-icon.msft.png)\).</span></span>  <span data-ttu-id="83ead-156">DevTools révèle une liste d'événements de souris, tels que **le** clic et **le clic avec la souris.**</span><span class="sxs-lookup"><span data-stu-id="83ead-156">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="83ead-157">Chaque événement dispose d'une case à cocher en regard.</span><span class="sxs-lookup"><span data-stu-id="83ead-157">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="83ead-158">Cochez la case en regard de **cliquer.**</span><span class="sxs-lookup"><span data-stu-id="83ead-158">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="83ead-159">DevTools est désormais installé pour être automatiquement suspendu lors de l'erreur `click` d'événements.</span><span class="sxs-lookup"><span data-stu-id="83ead-159">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Sélectionnez la case à cocher en regard de cliquer" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="83ead-161">Sélectionnez la case à cocher en regard de **cliquer**</span><span class="sxs-lookup"><span data-stu-id="83ead-161">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83ead-162">De retour à la démonstration, choisissez de nouveau **Ajouter le numéro 1 et le numéro 2.**</span><span class="sxs-lookup"><span data-stu-id="83ead-162">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="83ead-163">DevTools interrompt la démonstration et met en évidence une ligne de code dans **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="83ead-163">DevTools pauses the demo and highlights a line of code in the **Sources** tool.</span></span>  <span data-ttu-id="83ead-164">DevTools doit s'interrompre sur la ligne 16 dans `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="83ead-164">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="83ead-165">Si vous faites une pause sur une autre ligne de code, sélectionnez Reprendre l'exécution du **script** \( Reprendre l'exécution du script \) jusqu'à ce que vous arrêtiez ![ sur la ligne ](../media/resume-script-run-icon.msft.png) correcte.</span><span class="sxs-lookup"><span data-stu-id="83ead-165">If you pause on a different line of code, choose **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="83ead-166">Si vous avez suspendu sur une autre ligne, vous avez une extension de navigateur qui inscrit un listener d'événement sur chaque `click` page web que vous visitez.</span><span class="sxs-lookup"><span data-stu-id="83ead-166">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="83ead-167">Vous êtes suspendu dans `click` l'écoute de l'extension.</span><span class="sxs-lookup"><span data-stu-id="83ead-167">You are paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="83ead-168">Si vous utilisez le mode InPrivate pour parcourir en privé **,** ce qui désactive toutes les extensions, vous pouvez voir que vous mettez en pause la ligne de code souhaitée à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="83ead-168">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="83ead-169">**Les points d'arrêt d'écoute d'événements** ne sont qu'un des nombreux types de points d'arrêt disponibles dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="83ead-169">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="83ead-170">Mémorisez tous les différents types pour vous aider à déboguer les différents scénarios aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="83ead-170">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--  To learn when and how to use each type, navigate to [Pause your code with breakpoints][JSBreakpoints].  -->  

## <a name="step-4-step-through-the-code"></a><span data-ttu-id="83ead-171">Étape 4 : Procédure pas à pas dans le code</span><span class="sxs-lookup"><span data-stu-id="83ead-171">Step 4: Step through the code</span></span>  

<span data-ttu-id="83ead-172">Une cause courante de bogues est lorsqu'un script s'exécute dans un mauvais ordre.</span><span class="sxs-lookup"><span data-stu-id="83ead-172">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="83ead-173">La procédure pas à pas de votre code vous permet de parcourir l'runtime de votre code.</span><span class="sxs-lookup"><span data-stu-id="83ead-173">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="83ead-174">Vous pouvez parcourir une ligne à la fois pour déterminer exactement où votre code s'exécute dans un ordre différent de celui prévu.</span><span class="sxs-lookup"><span data-stu-id="83ead-174">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="83ead-175">Essayez maintenant :</span><span class="sxs-lookup"><span data-stu-id="83ead-175">Try it now:</span></span>  

1.  <span data-ttu-id="83ead-176">Choose **Step over next function call** \( Step over next function call ![ ](../media/step-over-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ead-176">Choose **Step over next function call** \(![Step over next function call](../media/step-over-icon.msft.png)\).</span></span>  <span data-ttu-id="83ead-177">DevTools exécute le code suivant sans y aller pas à pas.</span><span class="sxs-lookup"><span data-stu-id="83ead-177">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="83ead-178">DevTools ignore quelques lignes de code.</span><span class="sxs-lookup"><span data-stu-id="83ead-178">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="83ead-179">En effet, étant donné que la qualité est false, le `inputsAreEmpty()` bloc de code de l'instruction ne `if` s'exécute pas.</span><span class="sxs-lookup"><span data-stu-id="83ead-179">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="83ead-180">Dans l'outil **Sources** de DevTools, sélectionnez Pas à pas dans l'appel de fonction suivante **\(** Pas à pas dans l'appel de fonction suivant \) pour exécuter la fonction, une ligne à la ![ ](../media/step-into-icon.msft.png) `updateLabel()` fois.</span><span class="sxs-lookup"><span data-stu-id="83ead-180">On the **Sources** tool of DevTools, choose **Step into next function call** \(![Step into next function call](../media/step-into-icon.msft.png)\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="83ead-181">Passer en revue une ligne à la fois est l'idée de base qui consiste à passer en revue le code pas à pas.</span><span class="sxs-lookup"><span data-stu-id="83ead-181">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="83ead-182">Si vous examinez le code `get-started.js` dans , le bogue se trouve probablement quelque part dans la `updateLabel()` fonction.</span><span class="sxs-lookup"><span data-stu-id="83ead-182">If you review the code in `get-started.js`, the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="83ead-183">Au lieu d'aller pas à pas dans chaque ligne de code, vous pouvez utiliser un autre type de point d'arrêt pour suspendre le code plus près de l'emplacement probable du bogue.</span><span class="sxs-lookup"><span data-stu-id="83ead-183">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <a name="step-5-set-a-line-of-code-breakpoint"></a><span data-ttu-id="83ead-184">Étape 5 : Définir un point d'arrêt de ligne de code</span><span class="sxs-lookup"><span data-stu-id="83ead-184">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="83ead-185">Les points d'arrêt de ligne de code sont le type de point d'arrêt le plus courant.</span><span class="sxs-lookup"><span data-stu-id="83ead-185">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="83ead-186">Lorsque vous arrivez à la ligne de code spécifique que vous souhaitez suspendre, utilisez un point d'arrêt de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="83ead-186">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="83ead-187">Regardez la dernière ligne de code dans `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="83ead-187">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="83ead-188">À gauche, le numéro de cette ligne de code particulière s'affiche sous la couleur **34**.</span><span class="sxs-lookup"><span data-stu-id="83ead-188">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="83ead-189">Choisissez la **ligne 34**.</span><span class="sxs-lookup"><span data-stu-id="83ead-189">Choose line **34**.</span></span>  <span data-ttu-id="83ead-190">DevTools affiche une icône rouge à gauche de **34**.</span><span class="sxs-lookup"><span data-stu-id="83ead-190">DevTools displays a red icon to the left of **34**.</span></span>  <span data-ttu-id="83ead-191">L'icône rouge indique qu'un point d'arrêt de ligne de code se trouve sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="83ead-191">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="83ead-192">DevTools s'interrompt toujours avant l'utilisation de cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="83ead-192">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="83ead-193">Choose **Resume script execution** \( Resume script execution ![ ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ead-193">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  <span data-ttu-id="83ead-194">Le script continue à s'exécuter jusqu'à atteindre la ligne 33.</span><span class="sxs-lookup"><span data-stu-id="83ead-194">The script continues to run until it reaches line 33.</span></span>  <span data-ttu-id="83ead-195">Sur les lignes 31, 32 et 33, DevTools imprime les valeurs de , et à droite du point-virgule sur `addend1` `addend2` chaque `sum` ligne.</span><span class="sxs-lookup"><span data-stu-id="83ead-195">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools s'interrompt sur le point d'arrêt de ligne de code sur la ligne 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="83ead-197">DevTools s'interrompt sur le point d'arrêt de ligne de code sur la ligne 34</span><span class="sxs-lookup"><span data-stu-id="83ead-197">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a><span data-ttu-id="83ead-198">Étape 6 : Vérifier les valeurs des variables</span><span class="sxs-lookup"><span data-stu-id="83ead-198">Step 6: Check variable values</span></span>  

<span data-ttu-id="83ead-199">Les valeurs `addend1` de , `addend2` et `sum` semblent suspectes.</span><span class="sxs-lookup"><span data-stu-id="83ead-199">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="83ead-200">Les valeurs sont wrapped entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="83ead-200">The values are wrapped in quotes.</span></span>  <span data-ttu-id="83ead-201">Les guillemets signifient que la valeur est une chaîne, ce qui constitue une bonne hypothèse pour expliquer la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="83ead-201">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="83ead-202">Recueillez plus d'informations sur la situation.</span><span class="sxs-lookup"><span data-stu-id="83ead-202">Gather more information about the situation.</span></span>  <span data-ttu-id="83ead-203">DevTools fournit de nombreux outils pour examiner les valeurs des variables.</span><span class="sxs-lookup"><span data-stu-id="83ead-203">DevTools provides many tools for examining variable values.</span></span>  

### <a name="method-1-the-scope-pane"></a><span data-ttu-id="83ead-204">Méthode 1 : volet d'étendue</span><span class="sxs-lookup"><span data-stu-id="83ead-204">Method 1: The Scope pane</span></span>  

<span data-ttu-id="83ead-205">Si vous faites une pause \*\*\*\* sur une ligne de code, le volet Étendue affiche les variables locales et globales actuellement définies, ainsi que la valeur de chaque variable.</span><span class="sxs-lookup"><span data-stu-id="83ead-205">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="83ead-206">Il affiche également les variables de fermeture, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="83ead-206">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="83ead-207">Double-cliquez sur une valeur de variable pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="83ead-207">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="83ead-208">Si vous ne faites pas de pause sur une ligne de code, **le** volet d'étendue est vide.</span><span class="sxs-lookup"><span data-stu-id="83ead-208">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Volet d'étendue" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="83ead-210">Volet **d'étendue**</span><span class="sxs-lookup"><span data-stu-id="83ead-210">The **Scope** pane</span></span>  
:::image-end:::  

### <a name="method-2-watch-expressions"></a><span data-ttu-id="83ead-211">Méthode 2 : Expressions d'observation</span><span class="sxs-lookup"><span data-stu-id="83ead-211">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="83ead-212">Le **volet** Observateur vous permet de surveiller les valeurs de variables (par exemple) ou `sum` d'expressions (telles que `typeof sum` ).</span><span class="sxs-lookup"><span data-stu-id="83ead-212">The **Watch** pane allows you to monitor the values of variables (such as `sum`) or expressions (such as `typeof sum`).</span></span>  <span data-ttu-id="83ead-213">Vous pouvez stocker n'importe quelle expression JavaScript valide dans une expression d'observation.</span><span class="sxs-lookup"><span data-stu-id="83ead-213">You may store any valid JavaScript expression in a Watch Expression.</span></span>  

1.  <span data-ttu-id="83ead-214">Choisissez le **volet** d'observation.</span><span class="sxs-lookup"><span data-stu-id="83ead-214">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="83ead-215">Choose **Add watch expression** \( Add watch expression ![ ](../media/add-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ead-215">Choose **Add watch expression** \(![Add watch expression](../media/add-expression-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="83ead-216">Tapez `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="83ead-216">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="83ead-217">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="83ead-217">Select `Enter`.</span></span>  <span data-ttu-id="83ead-218">DevTools `typeof sum: "string"` s'affiche.</span><span class="sxs-lookup"><span data-stu-id="83ead-218">DevTools displays `typeof sum: "string"`.</span></span>  <span data-ttu-id="83ead-219">La valeur à droite du deux-points est le résultat de votre Expression d'observation.</span><span class="sxs-lookup"><span data-stu-id="83ead-219">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="83ead-220">Dans la figure suivante, `typeof sum` l'Expression d'observation s'affiche dans le **volet** d'observation.</span><span class="sxs-lookup"><span data-stu-id="83ead-220">In the following figure, the `typeof sum` Watch Expression is displayed in the **Watch** pane.</span></span>  <span data-ttu-id="83ead-221">Si votre fenêtre DevTools \*\*\*\* est large, le volet \*\*\*\* Montre s'affiche dans le volet Débogueur, qui apparaît ensuite à droite.</span><span class="sxs-lookup"><span data-stu-id="83ead-221">If your DevTools window is wide, the **Watch** pane is displayed within the **Debugger** pane, which then appears on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Volet d'observation" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="83ead-223">Volet **d'observation**</span><span class="sxs-lookup"><span data-stu-id="83ead-223">The **Watch** pane</span></span>  
:::image-end:::  

<span data-ttu-id="83ead-224">Comme on le suspecte, `sum` est évalué en tant que chaîne, lorsqu'il doit s'agit d'un nombre.</span><span class="sxs-lookup"><span data-stu-id="83ead-224">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="83ead-225">Vous avez maintenant confirmé que le type de valeur est la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="83ead-225">You now confirmed value type is the cause of the bug.</span></span>  

### <a name="method-3-the-console"></a><span data-ttu-id="83ead-226">Méthode 3 : Console</span><span class="sxs-lookup"><span data-stu-id="83ead-226">Method 3: The Console</span></span>  

<span data-ttu-id="83ead-227">La **console** vous permet d'afficher la `console.log()` sortie.</span><span class="sxs-lookup"><span data-stu-id="83ead-227">The **Console** allows you to view `console.log()` output.</span></span>  <span data-ttu-id="83ead-228">Vous pouvez également utiliser la **console pour** évaluer des instructions JavaScript arbitraires pendant que le débogger est suspendu au niveau d'une instruction de code.</span><span class="sxs-lookup"><span data-stu-id="83ead-228">You can also use the **Console** to evaluate arbitrary JavaScript statements while the debugger is paused at a code statement.</span></span>  <span data-ttu-id="83ead-229">Pour le débogage, vous pouvez utiliser la **console** pour tester les correctifs potentiels pour les bogues.</span><span class="sxs-lookup"><span data-stu-id="83ead-229">For debugging, you can use the **Console** to test potential fixes for bugs.</span></span>

1.  <span data-ttu-id="83ead-230">Si **l'outil Console** est fermé, `Esc` sélectionnez-le pour l'ouvrir.</span><span class="sxs-lookup"><span data-stu-id="83ead-230">If the **Console** tool is closed, select `Esc` to open it.</span></span>  <span data-ttu-id="83ead-231">**L'outil** Console s'ouvre dans le volet inférieur de la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="83ead-231">The **Console** tool opens in the lower pane of the DevTools window.</span></span>  
1.  <span data-ttu-id="83ead-232">Dans la **console,** tapez `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="83ead-232">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="83ead-233">L'instruction de l'outil est suspendue sur une ligne de code où `addend1` et se trouve dans `addend2` l'étendue.</span><span class="sxs-lookup"><span data-stu-id="83ead-233">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="83ead-234">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="83ead-234">Select `Enter`.</span></span>  <span data-ttu-id="83ead-235">DevTools évalue l'instruction et imprime, ce qui est le résultat que vous attendez de `6` la démonstration.</span><span class="sxs-lookup"><span data-stu-id="83ead-235">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="L'outil Console, après avoir évalué parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="83ead-237">**L'outil Console,** après évaluation</span><span class="sxs-lookup"><span data-stu-id="83ead-237">The **Console** tool, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a><span data-ttu-id="83ead-238">Étape 7 : Appliquer un correctif</span><span class="sxs-lookup"><span data-stu-id="83ead-238">Step 7: Apply a fix</span></span>  

<span data-ttu-id="83ead-239">Nous avons identifié un correctif possible pour le bogue.</span><span class="sxs-lookup"><span data-stu-id="83ead-239">We've identified a possible fix for the bug.</span></span>  <span data-ttu-id="83ead-240">Ensuite, modifiez le code JavaScript directement dans l'interface utilisateur de DevTools, puis réexécutez la démonstration pour tester le correctif, comme suit.</span><span class="sxs-lookup"><span data-stu-id="83ead-240">Next, edit the JavaScript code directly within the DevTools UI and then rerun the demo to test the fix, as follows.</span></span>

1.  <span data-ttu-id="83ead-241">Choose **Resume script execution** \( Resume script execution ![ ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ead-241">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="83ead-242">Dans le **volet** Éditeur, remplacez la `var sum = addend1 + addend2` ligne par `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="83ead-242">In the **Editor** pane, replace the line `var sum = addend1 + addend2` with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="83ead-243">Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer votre modification.</span><span class="sxs-lookup"><span data-stu-id="83ead-243">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="83ead-244">Choisissez **Désactiver les points d'arrêt** \( Désactiver les points ![ d'arrêt ](../media/deactivate-breakpoints-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ead-244">Choose **Deactivate breakpoints** \(![Deactivate breakpoints](../media/deactivate-breakpoints-button-icon.msft.png)\).</span></span>  <span data-ttu-id="83ead-245">Il change de bleu pour indiquer que l'option est active.</span><span class="sxs-lookup"><span data-stu-id="83ead-245">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="83ead-246">Lorsque **les points d'arrêt Deactivate sont définies,** DevTools ignore les points d'arrêt que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="83ead-246">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="83ead-247">Essayez la démonstration avec des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="83ead-247">Try out the demo with different values.</span></span>  <span data-ttu-id="83ead-248">La démonstration calcule maintenant correctement.</span><span class="sxs-lookup"><span data-stu-id="83ead-248">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="83ead-249">Ce flux de travail applique uniquement un correctif à une copie locale du code envoyé à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="83ead-249">This workflow only applies a fix to a local copy of the code sent from the server.</span></span>  <span data-ttu-id="83ead-250">Lors du débogage de votre projet, après avoir identifié le correctif, vous devez appliquer ce correctif au code sur le serveur, par exemple en éditant votre code source local, puis en déployant à nouveau votre code fixe sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="83ead-250">When debugging your project, after you identify the fix, you still need to apply that fix to the code on the server, such as by editing your local source code and then re-deploying your fixed code to the server.</span></span>

## <a name="next-steps"></a><span data-ttu-id="83ead-251">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="83ead-251">Next steps</span></span>  

<span data-ttu-id="83ead-252">Félicitations!</span><span class="sxs-lookup"><span data-stu-id="83ead-252">Congratulations!</span></span>  <span data-ttu-id="83ead-253">Vous savez maintenant comment utiliser microsoft Edge DevTools lors du débogage de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="83ead-253">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="83ead-254">Les outils et méthodes que vous avez appris dans cet article peuvent vous faire gagner un nombre d'heures.</span><span class="sxs-lookup"><span data-stu-id="83ead-254">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="83ead-255">Cet article a présenté deux façons de définir des points d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="83ead-255">This article showed two ways to set breakpoints.</span></span>  <span data-ttu-id="83ead-256">DevTools fournit également des moyens de définir des points d'arrêt pour suspendre votre code lorsque certaines conditions sont remplies, telles que :</span><span class="sxs-lookup"><span data-stu-id="83ead-256">DevTools also provides ways to set breakpoints to pause your code when certain conditions are met, such as:</span></span>

*   <span data-ttu-id="83ead-257">Points d'arrêt conditionnels qui ne sont déclenchés que lorsque la condition que vous fournissez est vraie.</span><span class="sxs-lookup"><span data-stu-id="83ead-257">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="83ead-258">Points d'arrêt sur les exceptions capturées ou non.</span><span class="sxs-lookup"><span data-stu-id="83ead-258">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="83ead-259">Points d'arrêt XHR déclenchés lorsque l'URL demandée correspond à une sous-stration que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="83ead-259">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="83ead-260">Pour plus d'informations sur le moment et la façon d'utiliser chaque type, accédez à [Suspendre votre code avec des points d'arrêt.][DevToolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="83ead-260">For more information about when and how to use each type, navigate to [Pause your code with breakpoints][DevToolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="83ead-261">Quelques contrôles de code pas à pas ne sont pas expliqués dans cet article.</span><span class="sxs-lookup"><span data-stu-id="83ead-261">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="83ead-262">Pour plus d'informations, accédez à la ligne pas à pas dans l'article « Utiliser les fonctionnalités du débogger ». [][DevToolsJavascriptReferenceStepThroughCode]</span><span class="sxs-lookup"><span data-stu-id="83ead-262">For more information, navigate to [Step over line of code][DevToolsJavascriptReferenceStepThroughCode] in the "Use the debugger features" article.</span></span>

### <a name="see-also"></a><span data-ttu-id="83ead-263">Voir également</span><span class="sxs-lookup"><span data-stu-id="83ead-263">See also</span></span>

*   <span data-ttu-id="83ead-264">[Utilisez les fonctionnalités du débogger][DevToolsJavascriptReference] : à l'aide de l'interface utilisateur du débogger dans l'outil Sources.</span><span class="sxs-lookup"><span data-stu-id="83ead-264">[Use the debugger features][DevToolsJavascriptReference] - Using the UI of the debugger in the Sources tool.</span></span>
*   <span data-ttu-id="83ead-265">[Vue d'ensemble][DevToolsSourcesIndex] de l'outil Sources : présente le débogger JavaScript et l'éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="83ead-265">[Sources tool overview][DevToolsSourcesIndex] - Introduces the JavaScript debugger and code editor.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="83ead-266">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="83ead-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptReference]: ./reference.md "Utiliser les fonctionnalités de débogger | Documents Microsoft"  
[DevToolsSourcesIndex]: ../sources/index.md "Vue d'ensemble de l'outil Sources | Documents Microsoft"  
[DevToolsJavscriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d'arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevToolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Code pas à pas : utiliser les fonctionnalités de débogger | Documents Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Ouvrir le | Glitch"  

> [!NOTE]
> <span data-ttu-id="83ead-272">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83ead-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="83ead-273">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="83ead-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="83ead-275">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83ead-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
