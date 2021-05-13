---
description: Découvrez les nouveaux flux de travail de débogage dans cette référence complète Microsoft Edge fonctionnalités de débogage DevTools.
title: Utiliser les fonctionnalités du débogueur
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6b15d317d4c720ab5ad76b7047532df101f69376
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564125"
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
# <a name="use-the-debugger-features"></a><span data-ttu-id="dd7a9-104">Utiliser les fonctionnalités du débogueur</span><span class="sxs-lookup"><span data-stu-id="dd7a9-104">Use the debugger features</span></span>

<span data-ttu-id="dd7a9-105">Cet article explique comment utiliser le débogueur dans Microsoft Edge DevTools, notamment comment définir un point d’arrêt de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-105">This article covers how to use the debugger in Microsoft Edge DevTools, including how to set a line-of-code breakpoint.</span></span>  <span data-ttu-id="dd7a9-106">Pour définir d’autres types de points d’arrêt, voir [Suspendre votre code avec des points d’arrêt.][DevToolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="dd7a9-106">To set other types of breakpoints, see [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

<span data-ttu-id="dd7a9-107">Pour découvrir les principes de base du débogage, accédez à Commencer à déboguer JavaScript dans [Microsoft Edge DevTools,][DevToolsJavascriptGetStarted]qui est un didacticiel qui utilise une page web existante basée sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-107">To learn the basics of debugging, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted], which is a tutorial that uses an existing, form-based webpage.</span></span>  <span data-ttu-id="dd7a9-108">Le didacticiel insérez des captures d’écran, afin que vous pouvez l’skim.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-108">The tutorial has screen captures, so you can skim it.</span></span>  <span data-ttu-id="dd7a9-109">Vous pouvez facilement tester les fonctionnalités du débogger à l’aide de la page web de démonstration.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-109">You can easily try out the debugger features by using the demo webpage.</span></span>

## <a name="view-and-edit-javascript-code"></a><span data-ttu-id="dd7a9-110">Afficher et modifier du code JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd7a9-110">View and edit JavaScript code</span></span>

<span data-ttu-id="dd7a9-111">Lorsque vous corrigez un bogue, vous souhaitez souvent essayer quelques modifications apportées à votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-111">When fixing a bug, you often want to try out some changes to your JavaScript code.</span></span>  <span data-ttu-id="dd7a9-112">Vous n’avez pas besoin d’apporter les modifications dans un éditeur externe ou un IDE, de charger à nouveau le fichier sur le serveur, puis d’actualiser la page . Au lieu de cela, pour tester les modifications, vous pouvez modifier votre code JavaScript directement dans DevTools et voir le résultat immédiatement.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-112">You don't need to make the changes in an external editor or IDE, re-upload the file to the server, and then refresh the page; instead, to test changes, you can edit your JavaScript code directly in DevTools and see the result immediately.</span></span>  

<span data-ttu-id="dd7a9-113">Pour afficher et modifier un fichier JavaScript :</span><span class="sxs-lookup"><span data-stu-id="dd7a9-113">To view and edit a JavaScript file:</span></span>  

1.  <span data-ttu-id="dd7a9-114">Accédez à **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-114">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="dd7a9-115">Dans le **volet Navigateur,** sélectionnez votre fichier pour l’ouvrir dans **le** volet Éditeur.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-115">In the **Navigator** pane, select your file, to open it in the **Editor** pane.</span></span>
1.  <span data-ttu-id="dd7a9-116">Dans le **volet** Éditeur, modifiez votre fichier.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-116">In the **Editor** pane, edit your file.</span></span>  
1.  <span data-ttu-id="dd7a9-117">Sélectionnez `Ctrl` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-117">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="dd7a9-118">DevTools charge ensuite le fichier JavaScript dans le moteur JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-118">DevTools then loads the JavaScript file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Volet Éditeur" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="dd7a9-120">Volet \*\*\*\* Éditeur</span><span class="sxs-lookup"><span data-stu-id="dd7a9-120">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="reformat-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="dd7a9-121">Reformater un fichier JavaScript minifié avec une impression assez grande</span><span class="sxs-lookup"><span data-stu-id="dd7a9-121">Reformat a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="dd7a9-122">Pour rendre un fichier minifié lisible par l’homme, sélectionnez le bouton **Format** \( Format \) en bas du volet ![ ](../media/format-icon.msft.png) Éditeur. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd7a9-122">To make a minified file human-readable, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button at the bottom of the **Editor** pane.</span></span>

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Bouton Format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="dd7a9-124">Bouton **Format**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-124">The **Format** button</span></span>  
:::image-end:::  

## <a name="set-a-breakpoint-to-pause-code"></a><span data-ttu-id="dd7a9-125">Définir un point d’arrêt pour suspendre le code</span><span class="sxs-lookup"><span data-stu-id="dd7a9-125">Set a breakpoint, to pause code</span></span>

<span data-ttu-id="dd7a9-126">Pour suspendre votre code au milieu de l’runtime, définissez un point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-126">To pause your code in the middle of the runtime, set a breakpoint.</span></span>  <span data-ttu-id="dd7a9-127">Le type de point d’arrêt le plus simple et le plus connu est un point d’arrêt de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-127">The most basic and well-known type of breakpoint is a line-of-code breakpoint.</span></span>

<span data-ttu-id="dd7a9-128">Utilisez un point d’arrêt de ligne de code lorsque vous connaissez la région exacte du code que vous devez examiner.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="dd7a9-129">DevTools s’interrompt toujours à la ligne de code spécifiée avant de l’exécute.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-129">DevTools always pauses at the specified line of code, before running it.</span></span>

<span data-ttu-id="dd7a9-130">Pour définir un point d’arrêt de ligne de code :</span><span class="sxs-lookup"><span data-stu-id="dd7a9-130">To set a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="dd7a9-131">Accédez à **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-131">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="dd7a9-132">Ouvrez le fichier qui contient la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-132">Open the file that contains the line of code.</span></span>  
1.  <span data-ttu-id="dd7a9-133">Sélectionnez la zone à gauche du numéro de ligne pour la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-133">Select the area to the left of the line number for the line of code.</span></span>  <span data-ttu-id="dd7a9-134">Vous pouvez également cliquer avec le bouton droit sur le numéro de ligne, puis choisir **Ajouter un point d’arrêt.**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-134">Or, right-click the line number and then choose **Add breakpoint**.</span></span>  <span data-ttu-id="dd7a9-135">Un cercle rouge apparaît ensuite à côté du numéro de ligne, indiquant un point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-135">A red circle then appears next to the line number, indicating a breakpoint.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un point d’arrêt de ligne de code" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="dd7a9-137">Un point d’arrêt de ligne de code</span><span class="sxs-lookup"><span data-stu-id="dd7a9-137">A line-of-code breakpoint</span></span>  
    :::image-end:::  

<span data-ttu-id="dd7a9-138">Les points d’arrêt de ligne de code peuvent être inefficaces à définir, en particulier si vous ne savez pas exactement où rechercher ou si votre base de code est grande.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-138">Line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if your codebase is large.</span></span>  <span data-ttu-id="dd7a9-139">Pour gagner du temps lors du débogage, découvrez comment et quand utiliser les autres types de points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-139">To save time when debugging, learn how and when to use the other types of breakpoints.</span></span>  <span data-ttu-id="dd7a9-140">Pour plus d’informations, [accédez à Suspendre votre code avec des points d’arrêt.][DevToolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="dd7a9-140">For more information, navigate to [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>

## <a name="step-through-code"></a><span data-ttu-id="dd7a9-141">Code pas à pas</span><span class="sxs-lookup"><span data-stu-id="dd7a9-141">Step through code</span></span>  

<span data-ttu-id="dd7a9-142">Une fois que votre code est suspendu à un point d’arrêt, pas à pas dans le code, une ligne à la fois, en enquêtant sur le flux de contrôle et les valeurs des propriétés en cours de route.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-142">After your code is paused at a breakpoint, step through the code, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="dd7a9-143">Ligne de code pas à pas</span><span class="sxs-lookup"><span data-stu-id="dd7a9-143">Step over line of code</span></span>  

<span data-ttu-id="dd7a9-144">Lorsqu’il est suspendu sur une ligne de code contenant une fonction qui n’est pas pertinente pour le problème que vous déboguer, choisissez le bouton Pas à pas principal **\(** Pas à pas principal \) pour exécuter la fonction sans y aller pas à ![ ](../media/step-over-icon.msft.png) pas.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-144">When paused on a line of code containing a function that isn't relevant to the problem you are debugging, choose the **Step over** \(![Step over](../media/step-over-icon.msft.png)\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Choose Step over" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="dd7a9-146">Choose **Step over**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-146">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="dd7a9-147">Par exemple, supposons que vous déboguer l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-147">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="dd7a9-148">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-148">You are paused on `A`.</span></span>  <span data-ttu-id="dd7a9-149">Une fois que vous avez choisi **Pas**à pas, DevTools exécute tout le code dans la fonction que vous exécutez pas à pas, c’est-à-dire. `B` `C`</span><span class="sxs-lookup"><span data-stu-id="dd7a9-149">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="dd7a9-150">DevTools s’interrompt ensuite sur `D` .</span><span class="sxs-lookup"><span data-stu-id="dd7a9-150">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="dd7a9-151">Pas à pas dans la ligne de code</span><span class="sxs-lookup"><span data-stu-id="dd7a9-151">Step into line of code</span></span>  

<span data-ttu-id="dd7a9-152">Lorsqu’il est suspendu sur une ligne de code contenant un appel de fonction lié au problème que vous déboguer, choisissez le bouton Pas à pas dans **\(** Pas à pas dans \) pour examiner cette ![ fonction plus en ](../media/step-into-icon.msft.png) détail.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-152">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into](../media/step-into-icon.msft.png)\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Choose Step into" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="dd7a9-154">Choose **Step into**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-154">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="dd7a9-155">Par exemple, supposons que vous déboguer l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-155">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="dd7a9-156">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-156">You are paused on `A`.</span></span>  <span data-ttu-id="dd7a9-157">Une fois que **vous avez choisi Pas à**pas, DevTools exécute cette ligne de code, puis s’interrompt. `B`</span><span class="sxs-lookup"><span data-stu-id="dd7a9-157">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="dd7a9-158">Sortir de la ligne de code</span><span class="sxs-lookup"><span data-stu-id="dd7a9-158">Step out of line of code</span></span>  

<span data-ttu-id="dd7a9-159">Lorsqu’il est suspendu à l’intérieur d’une fonction qui n’est pas liée au problème que vous déboguer, choisissez le bouton Pas **à** pas principal \( Pas à pas sortant \) pour exécuter le reste du code de la ![ ](../media/step-out-icon.msft.png) fonction.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-159">When paused inside of a function that isn't related to the problem you are debugging, choose the **Step out** \(![Step out](../media/step-out-icon.msft.png)\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Choose Step out" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="dd7a9-161">Choose **Step out**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-161">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="dd7a9-162">Par exemple, supposons que vous déboguer l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-162">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="dd7a9-163">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-163">You are paused on `A`.</span></span>  <span data-ttu-id="dd7a9-164">Une fois que vous avez choisi Pas **à**pas, DevTools exécute le reste du code dans , qui se trouve juste dans cet exemple, puis `getName()` `B` s’interrompt. `C`</span><span class="sxs-lookup"><span data-stu-id="dd7a9-164">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="dd7a9-165">Exécuter tout le code jusqu’à une ligne spécifique</span><span class="sxs-lookup"><span data-stu-id="dd7a9-165">Run all code up to a specific line</span></span>  

<span data-ttu-id="dd7a9-166">Lors du débogage d’une fonction longue, il peut y avoir un grand nombre de code qui n’est pas lié au problème que vous déboguer.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-166">When debugging a long function, there may be a lot of code that isn't related to the problem you are debugging.</span></span>  

<span data-ttu-id="dd7a9-167">Vous pouvez choisir d’aller dans toutes les lignes, mais cela est fastidieux.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-167">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="dd7a9-168">Vous pouvez choisir de définir un point d’arrêt de ligne de code sur la ligne qui vous intéresse, puis de choisir le bouton Reprendre l’exécution du **script** \( Reprendre l’exécution du script \), mais il existe un moyen plus ![ ](../media/resume-script-run-icon.msft.png) rapide.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-168">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button, but there is a faster way.</span></span>  

<span data-ttu-id="dd7a9-169">Pointez sur la ligne de code qui vous intéresse, ouvrez le menu contextuel \(clic droit\), puis choisissez **Continuer ici.**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-169">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="dd7a9-170">DevTools exécute l’ensemble du code jusqu’à ce point, puis s’interrompt sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-170">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Choose Continue to here" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="dd7a9-172">Choose **Continue to here**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-172">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="dd7a9-173">Redémarrer la fonction supérieure de la pile d’appels</span><span class="sxs-lookup"><span data-stu-id="dd7a9-173">Restart the top function of the call stack</span></span>  

<span data-ttu-id="dd7a9-174">Pour suspendre la première ligne de la fonction supérieure de votre pile d’appels, sur une ligne de code, pointez n’importe où dans le volet Pile des appels, ouvrez le menu contextuel \(clic droit\), puis choisissez Image de \*\*\*\* redémarrage. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd7a9-174">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart frame**.</span></span>  <span data-ttu-id="dd7a9-175">La fonction supérieure est la dernière fonction qui a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-175">The top function is the last function that was run.</span></span>  

<span data-ttu-id="dd7a9-176">L’extrait de code suivant est un exemple de procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-176">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="dd7a9-177">Vous êtes `A` suspendu.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-177">You are paused on `A`.</span></span>  <span data-ttu-id="dd7a9-178">Après avoir choisi **l’image**Redémarrer, vous devez être suspendu, sans jamais définir de point d’arrêt ni choisir reprendre l’exécution `B` **du script.**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-178">After choosing **Restart frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Choisir un cadre de redémarrage" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="dd7a9-180">Choisir **un cadre de redémarrage**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-180">Choose **Restart frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="dd7a9-181">Reprendre le runtime de script</span><span class="sxs-lookup"><span data-stu-id="dd7a9-181">Resume script runtime</span></span>  

<span data-ttu-id="dd7a9-182">Pour poursuivre l’exécution après une pause de votre script, choisissez le bouton Reprendre l’exécution du **script** \( Reprendre l’exécution ![ du script ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-182">To continue the runtime after a pause of your script, choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button.</span></span>  <span data-ttu-id="dd7a9-183">DevTools exécute le script jusqu’au point d’arrêt suivant, s’il y en a.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-183">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Choose Resume script execution" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="dd7a9-185">Choose **Resume script execution**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-185">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="dd7a9-186">Forcer le runtime de script</span><span class="sxs-lookup"><span data-stu-id="dd7a9-186">Force script runtime</span></span>  

<span data-ttu-id="dd7a9-187">Pour ignorer tous les points d’arrêt et forcer votre script à continuer à s’exécuter, choisissez et maintenez le bouton Reprendre l’exécution du **script** \( Reprendre l’exécution du script \), puis choisissez le bouton Forcer l’exécution du script \( Forcer l’exécution du ![ ](../media/resume-script-run-icon.msft.png) **script** ![ ](../media/force-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-187">To ignore all breakpoints and force your script to continue to run, choose and hold the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button and then choose the **Force script execution** \(![Force script execution](../media/force-script-run-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Choose Force script execution" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="dd7a9-189">Choose **Force script execution**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-189">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="dd7a9-190">Modifier le contexte du thread</span><span class="sxs-lookup"><span data-stu-id="dd7a9-190">Change thread context</span></span>  

<span data-ttu-id="dd7a9-191">Lorsque vous travaillez avec des travailleurs du web ou des travailleurs de service, choisissez un contexte répertorié dans le volet **Threads** pour basculer vers ce contexte.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-191">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="dd7a9-192">L’icône de flèche bleue représente le contexte actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-192">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Volet Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="dd7a9-194">Volet **Threads**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-194">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="dd7a9-195">Par exemple, supposons que vous êtes suspendu sur un point d’arrêt dans votre script principal et votre script de travail de service.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-195">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="dd7a9-196">Vous souhaitez afficher les propriétés locales et globales pour le contexte de travail de service, mais l’outil **Sources** affiche le contexte de script principal.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-196">You want to view the local and global properties for the service worker context, but the **Sources** tool is showing the main script context.</span></span>  <span data-ttu-id="dd7a9-197">Pour basculer vers le contexte de travail de service, dans le volet **Threads,** choisissez l’entrée de travail de service.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-197">To switch to the service worker context, in the **Threads** pane, choose the service worker entry.</span></span>  

## <a name="view-and-edit-properties-and-variables"></a><span data-ttu-id="dd7a9-198">Afficher et modifier des propriétés et des variables</span><span class="sxs-lookup"><span data-stu-id="dd7a9-198">View and edit properties and variables</span></span>

<span data-ttu-id="dd7a9-199">Bien qu’il soit suspendu sur \*\*\*\* une ligne de code, utilisez le volet Étendue pour afficher et modifier les valeurs des propriétés et des variables dans les étendues locale, de fermeture et globale.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-199">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="dd7a9-200">Double-cliquez sur une valeur de propriété pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-200">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="dd7a9-201">Les propriétés non éumables sont grisées.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-201">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Volet d’étendue" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="dd7a9-203">Volet **d’étendue**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-203">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="watch-the-values-of-javascript-expressions"></a><span data-ttu-id="dd7a9-204">Regardez les valeurs des expressions JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd7a9-204">Watch the values of JavaScript expressions</span></span>  

<span data-ttu-id="dd7a9-205">Utilisez le **volet** d’observation pour observer les valeurs des expressions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-205">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="dd7a9-206">Vous pouvez regarder n’importe quelle expression JavaScript valide.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-206">You can watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Volet d’observation" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="dd7a9-208">Volet **d’observation**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-208">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="dd7a9-209">Pour créer une expression d’observation, sélectionnez le bouton Ajouter une **expression d’observation** \( ![ Ajouter une expression ](../media/add-expression-icon.msft.png) d’observation \).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-209">To create a new watch expression, select the **Add watch expression** \(![Add watch expression](../media/add-expression-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="dd7a9-210">Pour actualiser les valeurs de toutes les expressions existantes, sélectionnez le bouton **Actualiser** \( ![ Actualiser ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-210">To refresh the values of all existing expressions, select the **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\) button.</span></span>  <span data-ttu-id="dd7a9-211">Les valeurs s’actualisent automatiquement lors du code pas à pas.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-211">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="dd7a9-212">Pour supprimer une expression d’observation, cliquez avec le bouton droit sur l’expression, puis sélectionnez **Supprimer l’expression d’observation** \( ![ Supprimer l’expression ](../media/delete-expression-icon.msft.png) d’observation \).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-212">To delete a watch expression, right-click the expression and then select **Delete watch expression** \(![Delete watch expression](../media/delete-expression-icon.msft.png)\).</span></span>  

## <a name="view-the-call-stack"></a><span data-ttu-id="dd7a9-213">Afficher la pile d’appels</span><span class="sxs-lookup"><span data-stu-id="dd7a9-213">View the call stack</span></span>  

<span data-ttu-id="dd7a9-214">Bien qu’il soit suspendu sur \*\*\*\* une ligne de code, utilisez le volet Pile des appels pour afficher la pile d’appels qui vous a mis à ce point.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-214">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="dd7a9-215">Choisissez une entrée pour passer à la ligne de code où cette fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-215">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="dd7a9-216">L’icône de flèche bleue représente la fonction DevTools actuellement mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-216">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Volet Pile des appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="dd7a9-218">Volet **Pile des** appels</span><span class="sxs-lookup"><span data-stu-id="dd7a9-218">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="dd7a9-219">Lorsqu’il n’est pas suspendu sur une ligne de code, le volet **Pile** des appels est vide.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-219">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="dd7a9-220">Copier la trace de pile</span><span class="sxs-lookup"><span data-stu-id="dd7a9-220">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="dd7a9-221">Pour copier la pile d’appels actuelle dans \*\*\*\* le Presse-papiers, pointez n’importe où dans le volet Pile des appels, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier la **trace**de pile.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-221">To copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Choose Copy Stack Trace" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="dd7a9-223">Choose **Copy Stack Trace**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-223">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="dd7a9-224">L’extrait de code suivant est un exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-224">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="dd7a9-225">Ignorer un script ou un modèle de scripts</span><span class="sxs-lookup"><span data-stu-id="dd7a9-225">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="dd7a9-226">Marquez un script en tant que code de bibliothèque lorsque vous souhaitez ignorer ce script lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-226">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="dd7a9-227">Lorsqu’il est marqué comme code de \*\*\*\* bibliothèque, un script est masqué dans le volet Pile des appels et vous n’entrez jamais dans les fonctions du script lorsque vous avancez dans votre code.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-227">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="dd7a9-228">Par exemple, dans l’extrait de code suivant, la ligne utilise , qui est `A` `lib` une bibliothèque tierce.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-228">For example, in the following code snippet, line `A` uses `lib`, which is a third-party library.</span></span>  <span data-ttu-id="dd7a9-229">Si vous êtes certain que le problème que vous déboguer n’est pas lié à cette bibliothèque tierce, il est logique de marquer le script en tant que **code de bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-229">If you are confident that the problem you are debugging is not related to that third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="dd7a9-230">Marquer un script en tant que code de bibliothèque à partir du volet Éditeur</span><span class="sxs-lookup"><span data-stu-id="dd7a9-230">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="dd7a9-231">Pour marquer un script en tant **que code de bibliothèque** à partir du volet Éditeur : \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd7a9-231">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="dd7a9-232">Ouvrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-232">Open the file.</span></span>  
1.  <span data-ttu-id="dd7a9-233">Pointez n’importe où et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-233">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="dd7a9-234">Choose **Add script to ignore list** (previously shown as Mark as Library **code**).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-234">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet Éditeur" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="dd7a9-236">Marquer un script en tant **que code de bibliothèque** à partir du volet Éditeur \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd7a9-236">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="dd7a9-237">Marquer un script en tant que code de bibliothèque à partir du volet Pile des appels</span><span class="sxs-lookup"><span data-stu-id="dd7a9-237">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="dd7a9-238">Pour marquer un script en tant **que code de bibliothèque** à partir du volet **Pile** des appels :</span><span class="sxs-lookup"><span data-stu-id="dd7a9-238">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="dd7a9-239">Pointez sur une fonction à partir du script et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-239">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="dd7a9-240">Choose **Add script to ignore list** (previously shown as Mark as Library **code**).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-240">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir du volet Pile des appels" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="dd7a9-242">Marquer un script en tant **que code de bibliothèque** à partir du volet **Pile** des appels</span><span class="sxs-lookup"><span data-stu-id="dd7a9-242">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="dd7a9-243">Marquer un script en tant que code de bibliothèque à partir Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd7a9-243">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="dd7a9-244">Pour marquer un seul script ou modèle de scripts à partir de **Paramètres**:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-244">To mark a single script or pattern of scripts from **Settings**:</span></span>  

1.  <span data-ttu-id="dd7a9-245">Ouvrez [Paramètres][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="dd7a9-245">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="dd7a9-246">Accédez au **paramètre de code** Bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-246">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="dd7a9-247">Choose **Add pattern**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-247">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="dd7a9-248">Entrez le nom du script ou un modèle regex de noms de script à marquer en tant **que code de bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-248">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="dd7a9-249">Choose **Add**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-249">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marquer un script en tant que code de bibliothèque à partir Paramètres" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="dd7a9-251">Marquer un script en **tant que code de bibliothèque** à partir **Paramètres**</span><span class="sxs-lookup"><span data-stu-id="dd7a9-251">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="dd7a9-252">Exécuter des extraits de code de débogage à partir de n’importe quelle page</span><span class="sxs-lookup"><span data-stu-id="dd7a9-252">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="dd7a9-253">Si vous vous trouvez en cours d’exécution du même code de débogage dans la console, pensez à des extraits de code.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-253">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="dd7a9-254">Les extraits de code sont des scripts d’runtime que vous pouvez écrire, stocker et exécuter dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-254">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="dd7a9-255">Voir [Exécuter des extraits de code JavaScript sur n’importe quelle page web.][DevToolsJavascriptSnippets]</span><span class="sxs-lookup"><span data-stu-id="dd7a9-255">See [Run snippets of JavaScript on any webpage][DevToolsJavascriptSnippets].</span></span>  

## <a name="see-also"></a><span data-ttu-id="dd7a9-256">Voir également</span><span class="sxs-lookup"><span data-stu-id="dd7a9-256">See also</span></span>  

*   <span data-ttu-id="dd7a9-257">[Prise en main avec débogage de JavaScript dans Microsoft Edge DevTools][DevToolsJavascriptGetStarted] : didacticiel simple et court utilisant du code existant, avec captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-257">[Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] - A simple, short tutorial using existing code, with screen captures.</span></span>
*   <span data-ttu-id="dd7a9-258">[Vue d’ensemble][DevToolsSourcesIndex] de l’outil **Sources :** l’outil Sources inclut le débogger et l’éditeur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-258">[Sources tool overview][DevToolsSourcesIndex] - The **Sources** tool includes the JavaScript debugger and editor.</span></span>
*   <span data-ttu-id="dd7a9-259">[Désactivez JavaScript avec Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="dd7a9-259">[Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="dd7a9-260">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="dd7a9-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d’arrêt Microsoft Edge devTools | Documents Microsoft"  
[DevToolsJavascriptDisable]: ./disable.md "Désactiver JavaScript avec Microsoft Edge devTools | Documents Microsoft"  
[DevToolsJavascriptGetStarted]: ./index.md "Commencer à déboguer JavaScript dans Microsoft Edge devTools | Documents Microsoft"  
[DevToolsJavascriptSnippets]: ./snippets.md "Exécutez des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsSourcesIndex]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
[DevToolsCustomize]: ../customize/index.md "Personnalisez Microsoft Edge devTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="dd7a9-267">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd7a9-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dd7a9-268">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="dd7a9-270">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd7a9-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
