---
title: Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 2afa4b7dbe96b65747ec17b147f0a82c16efa288
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581802"
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







# <span data-ttu-id="5976b-103">Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5976b-103">How To Pause Your Code With Breakpoints In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="5976b-104">Utilisez des points d’arrêt pour suspendre votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5976b-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="5976b-105">Ce guide décrit chaque type de point d’arrêt disponible dans DevTools, ainsi que le mode d’utilisation et la définition de chaque type.</span><span class="sxs-lookup"><span data-stu-id="5976b-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="5976b-106">Pour un didacticiel d’exécution du processus de débogage, voir [commencer à déboguer JavaScript dans Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="5976b-106">For a hands-on tutorial of the debugging process, see [Get Started with Debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="5976b-107">Vue d’ensemble de l’utilisation de chaque type de point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="5976b-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="5976b-108">Le type de point d’arrêt le plus connu est le type de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="5976b-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="5976b-109">Toutefois, en revanche, si vous ne savez pas exactement où il est possible de définir l’aspect exact du jeu de points d’arrêt et si vous travaillez avec un grand code base,</span><span class="sxs-lookup"><span data-stu-id="5976b-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="5976b-110">Vous pouvez gagner du temps lors du débogage en connaissant le mode d’utilisation des autres types de points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5976b-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="5976b-111">Type de point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="5976b-111">Breakpoint Type</span></span> | <span data-ttu-id="5976b-112">Utilisez cette opération lorsque vous souhaitez suspendre...</span><span class="sxs-lookup"><span data-stu-id="5976b-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="5976b-113">Code de ligne</span><span class="sxs-lookup"><span data-stu-id="5976b-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="5976b-114">Sur une zone de code exacte.</span><span class="sxs-lookup"><span data-stu-id="5976b-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="5976b-115">Ligne de code conditionnelle</span><span class="sxs-lookup"><span data-stu-id="5976b-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="5976b-116">Sur une zone de code exacte, mais uniquement quand une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="5976b-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="5976b-117">DOM</span><span class="sxs-lookup"><span data-stu-id="5976b-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="5976b-118">Sur le code qui modifie ou supprime un nœud DOM spécifique ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="5976b-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="5976b-119">XHR</span><span class="sxs-lookup"><span data-stu-id="5976b-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="5976b-120">Lorsqu’une URL XHR contient un modèle de chaîne.</span><span class="sxs-lookup"><span data-stu-id="5976b-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="5976b-121">Écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="5976b-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="5976b-122">Sur le code exécuté après un événement, par exemple `click` , s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5976b-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="5976b-123">Sauf</span><span class="sxs-lookup"><span data-stu-id="5976b-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="5976b-124">Sur la ligne de code qui lève une exception interceptée ou non interceptée.</span><span class="sxs-lookup"><span data-stu-id="5976b-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="5976b-125">Fonction</span><span class="sxs-lookup"><span data-stu-id="5976b-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="5976b-126">L’exécution d’une commande, d’une fonction ou d’une méthode spécifique.</span><span class="sxs-lookup"><span data-stu-id="5976b-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="5976b-127">Points d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="5976b-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="5976b-128">Utilisez un point d’arrêt de code de ligne lorsque vous connaissez la région exacte de code que vous devez examiner.</span><span class="sxs-lookup"><span data-stu-id="5976b-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="5976b-129">DevTools interrompt **toujours** l’exécution de cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="5976b-129">DevTools **always** pauses before this line of code is run.</span></span>  

<span data-ttu-id="5976b-130">Pour définir un point d’arrêt de code de ligne dans DevTools:</span><span class="sxs-lookup"><span data-stu-id="5976b-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="5976b-131">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="5976b-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="5976b-132">Ouvrez le fichier contenant la ligne de code que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="5976b-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="5976b-133">Accédez à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="5976b-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="5976b-134">À gauche de la ligne de code se trouve la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="5976b-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="5976b-135">Cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="5976b-135">Click on it.</span></span>  <span data-ttu-id="5976b-136">Une icône rouge apparaît en regard de la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="5976b-136">A red icon appears next to the line number column.</span></span>  

> ##### <span data-ttu-id="5976b-137">Figure1</span><span class="sxs-lookup"><span data-stu-id="5976b-137">Figure 1</span></span>  
> <span data-ttu-id="5976b-138">Un point d’arrêt de ligne de code défini à la ligne 30</span><span class="sxs-lookup"><span data-stu-id="5976b-138">A line-of-code breakpoint set on line 30</span></span>  
> ![Un point d’arrêt de code de ligne][ImageLocBreakpoint]  

### <span data-ttu-id="5976b-140">Points d’arrêt de code de ligne dans votre code</span><span class="sxs-lookup"><span data-stu-id="5976b-140">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="5976b-141">Exécutez la `debugger` méthode à partir de votre code pour suspendre cette ligne.</span><span class="sxs-lookup"><span data-stu-id="5976b-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="5976b-142">Cela équivaut à un [point d’arrêt de ligne de code](#line-of-code-breakpoints), sauf que le point d’arrêt est défini dans votre code, et non dans l’interface utilisateur devtools.</span><span class="sxs-lookup"><span data-stu-id="5976b-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="5976b-143">Points d’arrêt conditionnels de ligne de code</span><span class="sxs-lookup"><span data-stu-id="5976b-143">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="5976b-144">Utilisez un point d’arrêt de ligne de code conditionnel lorsque vous connaissez la région exacte de code que vous devez examiner, mais que vous ne voulez mettre en pause que si une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="5976b-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="5976b-145">Pour définir un point d’arrêt de code de ligne conditionnelle:</span><span class="sxs-lookup"><span data-stu-id="5976b-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="5976b-146">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="5976b-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="5976b-147">Ouvrez le fichier contenant la ligne de code que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="5976b-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="5976b-148">Accédez à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="5976b-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="5976b-149">À gauche de la ligne de code se trouve la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="5976b-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="5976b-150">Cliquez avec le bouton droit sur le numéro de la ligne.</span><span class="sxs-lookup"><span data-stu-id="5976b-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="5976b-151">Sélectionnez **Ajouter un point d’arrêt conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="5976b-151">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="5976b-152">Une boîte de dialogue s’affiche sous la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="5976b-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="5976b-153">Entrez votre condition dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5976b-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="5976b-154">Appuyez `Enter` pour activer le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5976b-154">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="5976b-155">Une icône en regard de la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="5976b-155">An icon next to the line number column.</span></span>  

> ##### <span data-ttu-id="5976b-156">Figure 2</span><span class="sxs-lookup"><span data-stu-id="5976b-156">Figure 2</span></span>  
> <span data-ttu-id="5976b-157">Un point d’arrêt conditionnel de ligne de code défini sur la ligne 34</span><span class="sxs-lookup"><span data-stu-id="5976b-157">A conditional line-of-code breakpoint set on line 34</span></span>  
> ![Un point d’arrêt conditionnel de code de ligne][ImageConditionalLocBreakpoint]  

### <span data-ttu-id="5976b-159">Gérer les points d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="5976b-159">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="5976b-160">Utilisez le volet **points d’arrêt** pour désactiver ou supprimer des points d’arrêt de code de ligne à partir d’un emplacement unique.</span><span class="sxs-lookup"><span data-stu-id="5976b-160">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

> ##### <span data-ttu-id="5976b-161">Figure3</span><span class="sxs-lookup"><span data-stu-id="5976b-161">Figure 3</span></span>  
> <span data-ttu-id="5976b-162">Le volet **points d’arrêt** présentant deux points d’arrêt de ligne de code: un sur une ligne `16` `get-started.js` , un autre en ligne</span><span class="sxs-lookup"><span data-stu-id="5976b-162">The **Breakpoints** panel showing two line-of-code breakpoints: one on line `16` of `get-started.js`, another on line</span></span> `33`  
> ![Panneau points d’arrêt][ImageBreakpointsPanel]  

*   <span data-ttu-id="5976b-164">Activez la case à cocher en regard d’une entrée pour désactiver ce point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5976b-164">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="5976b-165">Cliquez avec le bouton droit sur une entrée pour supprimer ce point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5976b-165">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="5976b-166">Cliquez avec le bouton droit n’importe où dans le volet **points d’arrêt** pour désactiver tous les points d’arrêt, désactiver tous les points d’arrêt ou supprimer tous les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5976b-166">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="5976b-167">La désactivation de tous les points d’arrêt revient à décocher chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5976b-167">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="5976b-168">La désactivation de tous les points d’arrêt prescrit à DevTools d’ignorer tous les points d’arrêt de la ligne de code, mais de maintenir l’état activé de façon à ce qu’ils soient dans le même État qu’avant lorsque vous les réactivez chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5976b-168">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  

> ##### <span data-ttu-id="5976b-169">Figure 4</span><span class="sxs-lookup"><span data-stu-id="5976b-169">Figure 4</span></span>  
> <span data-ttu-id="5976b-170">Les points d’arrêt désactivés dans le volet **points d’arrêt** sont désactivés et transparents</span><span class="sxs-lookup"><span data-stu-id="5976b-170">Deactivated breakpoints in the **Breakpoints** pane are disabled and transparent</span></span>  
> ![Points d’arrêt désactivé dans le volet points d’arrêt][ImageDeactivatedBreakpoints]  

## <span data-ttu-id="5976b-172">DOM modifier les points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="5976b-172">DOM change breakpoints</span></span>   

<span data-ttu-id="5976b-173">Utilisez un point d’arrêt de modification DOM lorsque vous souhaitez suspendre le code qui modifie un nœud DOM ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="5976b-173">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="5976b-174">Pour définir un point d’arrêt de modification DOM:</span><span class="sxs-lookup"><span data-stu-id="5976b-174">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="5976b-175">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="5976b-175">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="5976b-176">Accédez à l’élément sur lequel vous voulez définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5976b-176">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="5976b-177">Cliquez avec le bouton droit sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="5976b-177">Right-click the element.</span></span>  
1.  <span data-ttu-id="5976b-178">Placez le pointeur de la souris **sur arrêt**, puis sélectionnez modifications de **sous-arborescences**, **modifications d’attributs**ou suppression de **nœud**.</span><span class="sxs-lookup"><span data-stu-id="5976b-178">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  

> ##### <span data-ttu-id="5976b-179">Figure 5</span><span class="sxs-lookup"><span data-stu-id="5976b-179">Figure 5</span></span>  
> <span data-ttu-id="5976b-180">Menu contextuel pour la création d’un point d’arrêt de modification DOM</span><span class="sxs-lookup"><span data-stu-id="5976b-180">The context menu for creating a DOM change breakpoint</span></span>  
> ![Menu contextuel pour la création d’un point d’arrêt de modification DOM][ImageDomChangeBreakpoint]  

### <span data-ttu-id="5976b-182">Types d’arrêts de modification de DOM</span><span class="sxs-lookup"><span data-stu-id="5976b-182">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="5976b-183">**Modifications**de la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="5976b-183">**Subtree modifications**.</span></span>  <span data-ttu-id="5976b-184">Déclenché lorsqu’un enfant du nœud actuellement sélectionné est supprimé ou ajouté, ou que le contenu d’un enfant a changé.</span><span class="sxs-lookup"><span data-stu-id="5976b-184">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="5976b-185">Ne sont pas déclenchées sur les changements d’attribut de nœud enfant ou sur les modifications apportées au nœud actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5976b-185">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  

*   <span data-ttu-id="5976b-186">**Modifications d’attributs**: déclenché lors de l’ajout ou de la suppression d’un attribut sur le nœud actuellement sélectionné, ou en cas de modification d’une valeur d’attribut.</span><span class="sxs-lookup"><span data-stu-id="5976b-186">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  

*   <span data-ttu-id="5976b-187">**Suppression de nœud**: déclenchée lors de la suppression du nœud actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5976b-187">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  

## <span data-ttu-id="5976b-188">Points d’arrêt XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="5976b-188">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="5976b-189">Utilisez un point d’arrêt XHR lorsque vous souhaitez arrêter lorsque l’URL de requête d’un XHR contient une chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5976b-189">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="5976b-190">DevTools s’arrête sur la ligne de code où XHR exécute la `send()` méthode.</span><span class="sxs-lookup"><span data-stu-id="5976b-190">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="5976b-191">Cette fonctionnalité est également compatible avec les demandes d' [API FETCH][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="5976b-191">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="5976b-192">C’est le cas, par exemple, lorsque vous constatez qu’il s’agit d’une URL incorrecte et que vous voulez rapidement trouver le code source AJAX ou FETCH à l’origine de la demande incorrecte.</span><span class="sxs-lookup"><span data-stu-id="5976b-192">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="5976b-193">Pour définir un point d’arrêt XHR:</span><span class="sxs-lookup"><span data-stu-id="5976b-193">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="5976b-194">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="5976b-194">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="5976b-195">Développez le volet **points d’arrêt XHR** .</span><span class="sxs-lookup"><span data-stu-id="5976b-195">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="5976b-196">Cliquez sur **Ajouter un point d’arrêt**.</span><span class="sxs-lookup"><span data-stu-id="5976b-196">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="5976b-197">Entrez la chaîne que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="5976b-197">Enter the string which you want to break on.</span></span>  <span data-ttu-id="5976b-198">DevTools s’interrompt lorsque cette chaîne est présente n’importe où dans une URL de requête XHR.</span><span class="sxs-lookup"><span data-stu-id="5976b-198">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="5976b-199">Appuyez sur `Enter` pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="5976b-199">Press `Enter` to confirm.</span></span>  

> ##### <span data-ttu-id="5976b-200">Figure 6</span><span class="sxs-lookup"><span data-stu-id="5976b-200">Figure 6</span></span>  
> <span data-ttu-id="5976b-201">Création d’un point d’arrêt XHR dans les **points d’arrêt XHR** pour toute requête qui contient `org` dans l’URL;</span><span class="sxs-lookup"><span data-stu-id="5976b-201">Creating an XHR breakpoint in the **XHR Breakpoints** for any request that contains `org` in the URL</span></span>  
> ![Création d’un point d’arrêt XHR][ImageXhrBreakpoint]  

## <span data-ttu-id="5976b-203">Points d’arrêt de l’écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="5976b-203">Event listener breakpoints</span></span> 

<span data-ttu-id="5976b-204">Utilisez des points d’arrêt de l’écouteur d’événements lorsque vous souhaitez suspendre le code de l’écouteur d’événements qui s’exécute après le déclenchement d’un événement.</span><span class="sxs-lookup"><span data-stu-id="5976b-204">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="5976b-205">Vous pouvez sélectionner des événements spécifiques, tels que `click` des catégories d’événements, tels que tous les événements de souris.</span><span class="sxs-lookup"><span data-stu-id="5976b-205">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="5976b-206">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="5976b-206">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="5976b-207">Développez le volet de **points d’arrêt du détecteur d’événements** .</span><span class="sxs-lookup"><span data-stu-id="5976b-207">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="5976b-208">DevTools affiche une liste de catégories d’événements, par exemple une **animation**.</span><span class="sxs-lookup"><span data-stu-id="5976b-208">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="5976b-209">Activez une de ces catégories pour suspendre chaque événement de cette catégorie ou développer la catégorie et vérifier un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="5976b-209">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  

> ##### <span data-ttu-id="5976b-210">Figure 7</span><span class="sxs-lookup"><span data-stu-id="5976b-210">Figure 7</span></span>  
> <span data-ttu-id="5976b-211">Création d’un point d’arrêt de l’écouteur d’événements pour</span><span class="sxs-lookup"><span data-stu-id="5976b-211">Creating an event listener breakpoint for</span></span> `deviceorientation`  
> ![Création du point d’arrêt d’un écouteur d’événements][ImageEventListenerBreakpoint]  

## <span data-ttu-id="5976b-213">Points d’arrêt d’exception</span><span class="sxs-lookup"><span data-stu-id="5976b-213">Exception breakpoints</span></span>   

<span data-ttu-id="5976b-214">Utilisez des points d’arrêt d’exception lorsque vous voulez mettre en pause la ligne de code qui lève une exception interceptée ou non interceptée.</span><span class="sxs-lookup"><span data-stu-id="5976b-214">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="5976b-215">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="5976b-215">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="5976b-216">Cliquez sur **suspendre sur les exceptions** ![ suspendre les exceptions ][ImagePauseOnExceptionsIcon] .</span><span class="sxs-lookup"><span data-stu-id="5976b-216">Click **Pause on exceptions** ![Pause on exceptions][ImagePauseOnExceptionsIcon].</span></span>  <span data-ttu-id="5976b-217">L’icône devient bleu lorsque l’option est activée.</span><span class="sxs-lookup"><span data-stu-id="5976b-217">The icon turns blue when enabled.</span></span>  
    
    > ##### <span data-ttu-id="5976b-218">Figure8</span><span class="sxs-lookup"><span data-stu-id="5976b-218">Figure 8</span></span>  
    > <span data-ttu-id="5976b-219">Bouton **suspendre sur les exceptions**</span><span class="sxs-lookup"><span data-stu-id="5976b-219">The **Pause on exceptions** button</span></span>  
    > ![Bouton suspendre sur les exceptions][ImagePauseExceptionsHighlight]  

1.  <span data-ttu-id="5976b-221">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="5976b-221">**Optional**.</span></span> <span data-ttu-id="5976b-222">Activez la case à cocher **suspendre les exceptions interceptées** si vous souhaitez également suspendre les exceptions interceptées, en plus de celles qui ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="5976b-222">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  

> ##### <span data-ttu-id="5976b-223">Figure9</span><span class="sxs-lookup"><span data-stu-id="5976b-223">Figure 9</span></span>  
> <span data-ttu-id="5976b-224">Suspendu sur une exception non interceptée</span><span class="sxs-lookup"><span data-stu-id="5976b-224">Paused on an uncaught exception</span></span>  
> ![Suspendu sur une exception non interceptée][ImageUncaughtException]  

## <span data-ttu-id="5976b-226">Points d’arrêt de fonction</span><span class="sxs-lookup"><span data-stu-id="5976b-226">Function breakpoints</span></span>   

<span data-ttu-id="5976b-227">Exécutez la `debug(method)` méthode, où `method` se trouve la commande, la fonction ou la méthode que vous voulez déboguer lorsque vous voulez faire dérouler chaque fois qu’une fonction spécifique est exécutée.</span><span class="sxs-lookup"><span data-stu-id="5976b-227">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="5976b-228">Vous pouvez insérer `debug()` dans votre code (par exemple `console.log()` , une instruction) ou exécuter la méthode à partir de la console devtools.</span><span class="sxs-lookup"><span data-stu-id="5976b-228">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="5976b-229">équivaut à définir un [point d’arrêt de ligne de code](#line-of-code-breakpoints) sur la première ligne de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5976b-229">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="5976b-230">Vérifier que la fonction cible se trouve dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="5976b-230">Make sure the target function is in scope</span></span>   

<span data-ttu-id="5976b-231">DevTools lève une exception `ReferenceError` si la fonction que vous souhaitez déboguer n’est pas dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="5976b-231">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

<span data-ttu-id="5976b-232">Il est difficile de garantir que la fonction cible se trouve dans l’étendue si vous exécutez la `debug()` méthode à partir de la console devtools.</span><span class="sxs-lookup"><span data-stu-id="5976b-232">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="5976b-233">Voici une stratégie:</span><span class="sxs-lookup"><span data-stu-id="5976b-233">Here is one strategy:</span></span>  

1.  <span data-ttu-id="5976b-234">Définissez un [point d’arrêt de ligne de code](#line-of-code-breakpoints) à un emplacement où la fonction est dans Scope.</span><span class="sxs-lookup"><span data-stu-id="5976b-234">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="5976b-235">Déclenchez le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5976b-235">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="5976b-236">Exécutez la `debug()` méthode dans la console devtools lorsque le code est toujours suspendu sur le point d’arrêt de votre code.</span><span class="sxs-lookup"><span data-stu-id="5976b-236">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  

 



<!-- image links -->  

[ImagePauseOnExceptionsIcon]: /microsoft-edge/devtools-guide-chromium/media/pause-on-exceptions-icon.msft.png  

[ImageLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoint-30.msft.png "Figure 1: point d’arrêt de la ligne de code"  
[ImageConditionalLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-conditional-breakpoint.msft.png "Figure 2: point d’arrêt du code de la ligne conditionnelle"  
[ImageBreakpointsPanel]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-16-33.msft.png "Figure 3: volet points d’arrêt"  
[ImageDeactivatedBreakpoints]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png "Figure 4: points d’arrêt désactivé dans le volet points d’arrêt"  
[ImageDomChangeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-elements-break-on-subtree-modifications.msft.png "Figure 5: menu contextuel de création d’un point d’arrêt de modification DOM"  
[ImageXhrBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png "Figure 6: création d’un point d’arrêt XHR"  
[ImageEventListenerBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png "Figure 7: création d’un point d’arrêt d’un écouteur d’événements"  
[ImagePauseExceptionsHighlight]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-pause-on-exceptions.msft.png "Figure 8: bouton pause sur les exceptions"  
[ImageUncaughtException]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-paused-on-exception.msft.png "Figure 9: interruption d’une exception non interceptée"  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "API Fetch | MDN"  

> [!NOTE]
> <span data-ttu-id="5976b-248">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5976b-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5976b-249">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools & phare \).</span><span class="sxs-lookup"><span data-stu-id="5976b-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  
[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="5976b-251">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5976b-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
