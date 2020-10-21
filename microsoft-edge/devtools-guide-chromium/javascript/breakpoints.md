---
description: Découvrez toutes les manières dont vous pouvez mettre votre code en pause dans Microsoft Edge DevTools.
title: Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 98c0e42657d9b0900d3eaca8af69f1c17abfcf06
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124809"
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

# <span data-ttu-id="164ab-104">Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="164ab-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="164ab-105">Utilisez des points d’arrêt pour suspendre votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="164ab-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="164ab-106">Ce guide décrit chaque type de point d’arrêt disponible dans DevTools, ainsi que le mode d’utilisation et la définition de chaque type.</span><span class="sxs-lookup"><span data-stu-id="164ab-106">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="164ab-107">Pour un didacticiel d’exécution du processus de débogage, accédez à la section [prendre en main le débogage JavaScript dans Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="164ab-107">For a hands-on tutorial of the debugging process, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="164ab-108">Vue d’ensemble de l’utilisation de chaque type de point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="164ab-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="164ab-109">Le type de point d’arrêt le plus connu est le type de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="164ab-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="164ab-110">Toutefois, en revanche, si vous ne savez pas exactement où il est possible de définir l’aspect exact du jeu de points d’arrêt et si vous travaillez avec un grand code base,</span><span class="sxs-lookup"><span data-stu-id="164ab-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="164ab-111">Vous pouvez gagner du temps lors du débogage en connaissant le mode d’utilisation des autres types de points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="164ab-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="164ab-112">Type de point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="164ab-112">Breakpoint Type</span></span> | <span data-ttu-id="164ab-113">Utilisez cette opération lorsque vous souhaitez suspendre...</span><span class="sxs-lookup"><span data-stu-id="164ab-113">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="164ab-114">Code de ligne</span><span class="sxs-lookup"><span data-stu-id="164ab-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="164ab-115">Sur une zone de code exacte.</span><span class="sxs-lookup"><span data-stu-id="164ab-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="164ab-116">Ligne de code conditionnelle</span><span class="sxs-lookup"><span data-stu-id="164ab-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="164ab-117">Sur une zone de code exacte, mais uniquement quand une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="164ab-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="164ab-118">DOM</span><span class="sxs-lookup"><span data-stu-id="164ab-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="164ab-119">Sur le code qui modifie ou supprime un nœud DOM spécifique ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="164ab-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="164ab-120">XHR</span><span class="sxs-lookup"><span data-stu-id="164ab-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="164ab-121">Lorsqu’une URL XHR contient un modèle de chaîne.</span><span class="sxs-lookup"><span data-stu-id="164ab-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="164ab-122">Écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="164ab-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="164ab-123">Sur le code exécuté après un événement, par exemple `click` , s’exécute.</span><span class="sxs-lookup"><span data-stu-id="164ab-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="164ab-124">Sauf</span><span class="sxs-lookup"><span data-stu-id="164ab-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="164ab-125">Sur la ligne de code qui lève une exception interceptée ou non interceptée.</span><span class="sxs-lookup"><span data-stu-id="164ab-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="164ab-126">Fonction</span><span class="sxs-lookup"><span data-stu-id="164ab-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="164ab-127">L’exécution d’une commande, d’une fonction ou d’une méthode spécifique.</span><span class="sxs-lookup"><span data-stu-id="164ab-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="164ab-128">Points d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="164ab-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="164ab-129">Utilisez un point d’arrêt de code de ligne lorsque vous connaissez la région exacte de code que vous devez examiner.</span><span class="sxs-lookup"><span data-stu-id="164ab-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="164ab-130">DevTools interrompt toujours l’exécution de cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="164ab-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="164ab-131">Pour définir un point d’arrêt de code de ligne dans DevTools:</span><span class="sxs-lookup"><span data-stu-id="164ab-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="164ab-132">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="164ab-132">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="164ab-133">Ouvrez le fichier contenant la ligne de code que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="164ab-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="164ab-134">Accédez à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="164ab-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="164ab-135">À gauche de la ligne de code se trouve la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="164ab-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="164ab-136">Cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="164ab-136">Click on it.</span></span>  <span data-ttu-id="164ab-137">Une icône rouge apparaît en regard de la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="164ab-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="164ab-139">Un point d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="164ab-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="164ab-140">Points d’arrêt de code de ligne dans votre code</span><span class="sxs-lookup"><span data-stu-id="164ab-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="164ab-141">Exécutez la `debugger` méthode à partir de votre code pour suspendre cette ligne.</span><span class="sxs-lookup"><span data-stu-id="164ab-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="164ab-142">Cela équivaut à un [point d’arrêt de ligne de code](#line-of-code-breakpoints), sauf que le point d’arrêt est défini dans votre code, et non dans l’interface utilisateur devtools.</span><span class="sxs-lookup"><span data-stu-id="164ab-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="164ab-143">Points d’arrêt conditionnels de ligne de code</span><span class="sxs-lookup"><span data-stu-id="164ab-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="164ab-144">Utilisez un point d’arrêt de ligne de code conditionnel lorsque vous connaissez la région exacte de code que vous devez examiner, mais que vous ne voulez mettre en pause que si une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="164ab-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="164ab-145">Pour définir un point d’arrêt de code de ligne conditionnelle:</span><span class="sxs-lookup"><span data-stu-id="164ab-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="164ab-146">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="164ab-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="164ab-147">Ouvrez le fichier contenant la ligne de code que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="164ab-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="164ab-148">Accédez à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="164ab-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="164ab-149">À gauche de la ligne de code se trouve la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="164ab-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="164ab-150">Cliquez avec le bouton droit sur le numéro de la ligne.</span><span class="sxs-lookup"><span data-stu-id="164ab-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="164ab-151">Choisissez **Ajouter un point d’arrêt conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="164ab-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="164ab-152">Une boîte de dialogue s’affiche sous la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="164ab-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="164ab-153">Entrez votre condition dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="164ab-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="164ab-154">Activez `Enter` cette option pour activer le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="164ab-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="164ab-155">Une icône en regard de la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="164ab-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="164ab-157">Un point d’arrêt conditionnel de code de ligne</span><span class="sxs-lookup"><span data-stu-id="164ab-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="164ab-158">Gérer les points d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="164ab-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="164ab-159">Utilisez le volet **points d’arrêt** pour désactiver ou supprimer des points d’arrêt de code de ligne à partir d’un emplacement unique.</span><span class="sxs-lookup"><span data-stu-id="164ab-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="164ab-161">Panneau **points d’arrêt**</span><span class="sxs-lookup"><span data-stu-id="164ab-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="164ab-162">Activez la case à cocher en regard d’une entrée pour désactiver ce point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="164ab-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="164ab-163">Cliquez avec le bouton droit sur une entrée pour supprimer ce point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="164ab-163">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="164ab-164">Cliquez avec le bouton droit n’importe où dans le volet **points d’arrêt** pour désactiver tous les points d’arrêt, désactiver tous les points d’arrêt ou supprimer tous les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="164ab-164">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="164ab-165">La désactivation de tous les points d’arrêt revient à décocher chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="164ab-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="164ab-166">La désactivation de tous les points d’arrêt prescrit à DevTools d’ignorer tous les points d’arrêt de la ligne de code, mais de maintenir l’état activé de façon à ce qu’ils soient dans le même État qu’avant lorsque vous les réactivez chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="164ab-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="164ab-168">Points d’arrêt désactivé dans le volet **points d’arrêt**</span><span class="sxs-lookup"><span data-stu-id="164ab-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="164ab-169">DOM modifier les points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="164ab-169">DOM change breakpoints</span></span>  

<span data-ttu-id="164ab-170">Utilisez un point d’arrêt de modification DOM lorsque vous souhaitez suspendre le code qui modifie un nœud DOM ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="164ab-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="164ab-171">Pour définir un point d’arrêt de modification DOM:</span><span class="sxs-lookup"><span data-stu-id="164ab-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="164ab-172">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="164ab-172">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="164ab-173">Accédez à l’élément sur lequel vous voulez définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="164ab-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="164ab-174">Cliquez avec le bouton droit sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="164ab-174">Right-click the element.</span></span>  
1.  <span data-ttu-id="164ab-175">Placez le pointeur de la souris **sur arrêt**, puis sélectionnez **modifications de sous-arbres**, modifications d' **attributs**ou **Suppression de nœud**.</span><span class="sxs-lookup"><span data-stu-id="164ab-175">Hover over **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="164ab-177">Menu contextuel pour la création d’un point d’arrêt de modification DOM</span><span class="sxs-lookup"><span data-stu-id="164ab-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="164ab-178">Types d’arrêts de modification de DOM</span><span class="sxs-lookup"><span data-stu-id="164ab-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="164ab-179">**Modifications**de la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="164ab-179">**Subtree modifications**.</span></span>  <span data-ttu-id="164ab-180">Déclenché lorsqu’un enfant du nœud actuellement sélectionné est supprimé ou ajouté, ou que le contenu d’un enfant a changé.</span><span class="sxs-lookup"><span data-stu-id="164ab-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="164ab-181">Ne sont pas déclenchées sur les changements d’attribut de nœud enfant ou sur les modifications apportées au nœud actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="164ab-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="164ab-182">**Modifications d’attributs**: déclenché lors de l’ajout ou de la suppression d’un attribut sur le nœud actuellement sélectionné, ou en cas de modification d’une valeur d’attribut.</span><span class="sxs-lookup"><span data-stu-id="164ab-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="164ab-183">**Suppression de nœud**: déclenchée lors de la suppression du nœud actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="164ab-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="164ab-184">Points d’arrêt XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="164ab-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="164ab-185">Utilisez un point d’arrêt XHR lorsque vous souhaitez arrêter lorsque l’URL de requête d’un XHR contient une chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="164ab-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="164ab-186">DevTools s’arrête sur la ligne de code où XHR exécute la `send()` méthode.</span><span class="sxs-lookup"><span data-stu-id="164ab-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="164ab-187">Cette fonctionnalité est également compatible avec les demandes d' [API FETCH][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="164ab-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="164ab-188">C’est le cas, par exemple, lorsque vous constatez qu’il s’agit d’une URL incorrecte et que vous voulez rapidement trouver le code source AJAX ou FETCH à l’origine de la demande incorrecte.</span><span class="sxs-lookup"><span data-stu-id="164ab-188">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="164ab-189">Pour définir un point d’arrêt XHR:</span><span class="sxs-lookup"><span data-stu-id="164ab-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="164ab-190">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="164ab-190">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="164ab-191">Développez le volet **points d’arrêt XHR** .</span><span class="sxs-lookup"><span data-stu-id="164ab-191">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="164ab-192">Choisissez **Ajouter un point d’arrêt**.</span><span class="sxs-lookup"><span data-stu-id="164ab-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="164ab-193">Entrez la chaîne que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="164ab-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="164ab-194">DevTools s’interrompt lorsque cette chaîne est présente n’importe où dans une URL de requête XHR.</span><span class="sxs-lookup"><span data-stu-id="164ab-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="164ab-195">Sélectionnez `Enter` pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="164ab-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="164ab-197">Créer un point d’arrêt XHR</span><span class="sxs-lookup"><span data-stu-id="164ab-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="164ab-198">Points d’arrêt de l’écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="164ab-198">Event listener breakpoints</span></span>   

<span data-ttu-id="164ab-199">Utilisez des points d’arrêt de l’écouteur d’événements lorsque vous souhaitez suspendre le code de l’écouteur d’événements qui s’exécute après le déclenchement d’un événement.</span><span class="sxs-lookup"><span data-stu-id="164ab-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="164ab-200">Vous pouvez sélectionner des événements spécifiques, tels que `click` des catégories d’événements, tels que tous les événements de souris.</span><span class="sxs-lookup"><span data-stu-id="164ab-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="164ab-201">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="164ab-201">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="164ab-202">Développez le volet de **points d’arrêt du détecteur d’événements** .</span><span class="sxs-lookup"><span data-stu-id="164ab-202">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="164ab-203">DevTools affiche une liste de catégories d’événements, par exemple une **animation**.</span><span class="sxs-lookup"><span data-stu-id="164ab-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="164ab-204">Activez une de ces catégories pour suspendre chaque événement de cette catégorie ou développer la catégorie et vérifier un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="164ab-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="164ab-206">Créer un point d’arrêt d’écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="164ab-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="164ab-207">Points d’arrêt d’exception</span><span class="sxs-lookup"><span data-stu-id="164ab-207">Exception breakpoints</span></span>  

<span data-ttu-id="164ab-208">Utilisez des points d’arrêt d’exception lorsque vous voulez mettre en pause la ligne de code qui lève une exception interceptée ou non interceptée.</span><span class="sxs-lookup"><span data-stu-id="164ab-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="164ab-209">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="164ab-209">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="164ab-210">Sélectionnez **suspendre sur les exceptions** \ ( ![ suspendre sur les exceptions ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="164ab-210">Choose **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="164ab-211">L’icône devient bleu lorsque l’option est activée.</span><span class="sxs-lookup"><span data-stu-id="164ab-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="164ab-213">Bouton **suspendre sur les exceptions**</span><span class="sxs-lookup"><span data-stu-id="164ab-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="164ab-214">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="164ab-214">**Optional**.</span></span>  <span data-ttu-id="164ab-215">Activez la case à cocher **suspendre les exceptions interceptées** si vous souhaitez également suspendre les exceptions interceptées, en plus de celles qui ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="164ab-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="164ab-217">Suspendu sur une exception non interceptée</span><span class="sxs-lookup"><span data-stu-id="164ab-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="164ab-218">Points d’arrêt de fonction</span><span class="sxs-lookup"><span data-stu-id="164ab-218">Function breakpoints</span></span>  

<span data-ttu-id="164ab-219">Exécutez la `debug(method)` méthode, où `method` se trouve la commande, la fonction ou la méthode que vous voulez déboguer lorsque vous voulez faire dérouler chaque fois qu’une fonction spécifique est exécutée.</span><span class="sxs-lookup"><span data-stu-id="164ab-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="164ab-220">Vous pouvez insérer `debug()` dans votre code (par exemple `console.log()` , une instruction) ou exécuter la méthode à partir de la console devtools.</span><span class="sxs-lookup"><span data-stu-id="164ab-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="164ab-221">équivaut à définir un [point d’arrêt de ligne de code](#line-of-code-breakpoints) sur la première ligne de la fonction.</span><span class="sxs-lookup"><span data-stu-id="164ab-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="164ab-222">Vérifier que la fonction cible se trouve dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="164ab-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="164ab-223">DevTools lève une exception `ReferenceError` si la fonction que vous souhaitez déboguer n’est pas dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="164ab-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="164ab-224">Il est difficile de garantir que la fonction cible se trouve dans l’étendue si vous exécutez la `debug()` méthode à partir de la console devtools.</span><span class="sxs-lookup"><span data-stu-id="164ab-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="164ab-225">Voici une stratégie:</span><span class="sxs-lookup"><span data-stu-id="164ab-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="164ab-226">Définissez un [point d’arrêt de ligne de code](#line-of-code-breakpoints) à un emplacement où la fonction est dans Scope.</span><span class="sxs-lookup"><span data-stu-id="164ab-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="164ab-227">Déclenchez le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="164ab-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="164ab-228">Exécutez la `debug()` méthode dans la console devtools lorsque le code est toujours suspendu sur le point d’arrêt de votre code.</span><span class="sxs-lookup"><span data-stu-id="164ab-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <span data-ttu-id="164ab-229">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="164ab-229">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "API Fetch | MDN"  

> [!NOTE]
> <span data-ttu-id="164ab-232">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="164ab-232">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="164ab-233">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="164ab-233">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="164ab-235">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="164ab-235">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
