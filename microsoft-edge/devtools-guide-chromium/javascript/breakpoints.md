---
title: Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 804e864ee3029a49ba1ef2ac1f2deb61c3ba5ec3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983185"
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







# <span data-ttu-id="64b62-103">Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="64b62-103">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="64b62-104">Utilisez des points d’arrêt pour suspendre votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64b62-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="64b62-105">Ce guide décrit chaque type de point d’arrêt disponible dans DevTools, ainsi que le mode d’utilisation et la définition de chaque type.</span><span class="sxs-lookup"><span data-stu-id="64b62-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="64b62-106">Pour un didacticiel d’exécution du processus de débogage, voir [commencer à déboguer JavaScript dans Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="64b62-106">For a hands-on tutorial of the debugging process, see [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="64b62-107">Vue d’ensemble de l’utilisation de chaque type de point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="64b62-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="64b62-108">Le type de point d’arrêt le plus connu est le type de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="64b62-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="64b62-109">Toutefois, en revanche, si vous ne savez pas exactement où il est possible de définir l’aspect exact du jeu de points d’arrêt et si vous travaillez avec un grand code base,</span><span class="sxs-lookup"><span data-stu-id="64b62-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="64b62-110">Vous pouvez gagner du temps lors du débogage en connaissant le mode d’utilisation des autres types de points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="64b62-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="64b62-111">Type de point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="64b62-111">Breakpoint Type</span></span> | <span data-ttu-id="64b62-112">Utilisez cette opération lorsque vous souhaitez suspendre...</span><span class="sxs-lookup"><span data-stu-id="64b62-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="64b62-113">Code de ligne</span><span class="sxs-lookup"><span data-stu-id="64b62-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="64b62-114">Sur une zone de code exacte.</span><span class="sxs-lookup"><span data-stu-id="64b62-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="64b62-115">Ligne de code conditionnelle</span><span class="sxs-lookup"><span data-stu-id="64b62-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="64b62-116">Sur une zone de code exacte, mais uniquement quand une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="64b62-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="64b62-117">DOM</span><span class="sxs-lookup"><span data-stu-id="64b62-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="64b62-118">Sur le code qui modifie ou supprime un nœud DOM spécifique ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="64b62-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="64b62-119">XHR</span><span class="sxs-lookup"><span data-stu-id="64b62-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="64b62-120">Lorsqu’une URL XHR contient un modèle de chaîne.</span><span class="sxs-lookup"><span data-stu-id="64b62-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="64b62-121">Écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="64b62-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="64b62-122">Sur le code exécuté après un événement, par exemple `click` , s’exécute.</span><span class="sxs-lookup"><span data-stu-id="64b62-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="64b62-123">Sauf</span><span class="sxs-lookup"><span data-stu-id="64b62-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="64b62-124">Sur la ligne de code qui lève une exception interceptée ou non interceptée.</span><span class="sxs-lookup"><span data-stu-id="64b62-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="64b62-125">Fonction</span><span class="sxs-lookup"><span data-stu-id="64b62-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="64b62-126">L’exécution d’une commande, d’une fonction ou d’une méthode spécifique.</span><span class="sxs-lookup"><span data-stu-id="64b62-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="64b62-127">Points d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="64b62-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="64b62-128">Utilisez un point d’arrêt de code de ligne lorsque vous connaissez la région exacte de code que vous devez examiner.</span><span class="sxs-lookup"><span data-stu-id="64b62-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="64b62-129">DevTools interrompt toujours l’exécution de cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="64b62-129">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="64b62-130">Pour définir un point d’arrêt de code de ligne dans DevTools:</span><span class="sxs-lookup"><span data-stu-id="64b62-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="64b62-131">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="64b62-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="64b62-132">Ouvrez le fichier contenant la ligne de code que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="64b62-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="64b62-133">Accédez à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="64b62-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="64b62-134">À gauche de la ligne de code se trouve la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="64b62-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="64b62-135">Cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="64b62-135">Click on it.</span></span>  <span data-ttu-id="64b62-136">Une icône rouge apparaît en regard de la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="64b62-136">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="64b62-138">Un point d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="64b62-138">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="64b62-139">Points d’arrêt de code de ligne dans votre code</span><span class="sxs-lookup"><span data-stu-id="64b62-139">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="64b62-140">Exécutez la `debugger` méthode à partir de votre code pour suspendre cette ligne.</span><span class="sxs-lookup"><span data-stu-id="64b62-140">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="64b62-141">Cela équivaut à un [point d’arrêt de ligne de code](#line-of-code-breakpoints), sauf que le point d’arrêt est défini dans votre code, et non dans l’interface utilisateur devtools.</span><span class="sxs-lookup"><span data-stu-id="64b62-141">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="64b62-142">Points d’arrêt conditionnels de ligne de code</span><span class="sxs-lookup"><span data-stu-id="64b62-142">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="64b62-143">Utilisez un point d’arrêt de ligne de code conditionnel lorsque vous connaissez la région exacte de code que vous devez examiner, mais que vous ne voulez mettre en pause que si une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="64b62-143">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="64b62-144">Pour définir un point d’arrêt de code de ligne conditionnelle:</span><span class="sxs-lookup"><span data-stu-id="64b62-144">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="64b62-145">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="64b62-145">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="64b62-146">Ouvrez le fichier contenant la ligne de code que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="64b62-146">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="64b62-147">Accédez à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="64b62-147">Go the line of code.</span></span>  
1.  <span data-ttu-id="64b62-148">À gauche de la ligne de code se trouve la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="64b62-148">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="64b62-149">Cliquez avec le bouton droit sur le numéro de la ligne.</span><span class="sxs-lookup"><span data-stu-id="64b62-149">Right-click the line number.</span></span>  
1.  <span data-ttu-id="64b62-150">Sélectionnez **Ajouter un point d’arrêt conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="64b62-150">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="64b62-151">Une boîte de dialogue s’affiche sous la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="64b62-151">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="64b62-152">Entrez votre condition dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="64b62-152">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="64b62-153">Appuyez `Enter` pour activer le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="64b62-153">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="64b62-154">Une icône en regard de la colonne numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="64b62-154">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Un point d’arrêt conditionnel de code de ligne" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="64b62-156">Un point d’arrêt conditionnel de code de ligne</span><span class="sxs-lookup"><span data-stu-id="64b62-156">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="64b62-157">Gérer les points d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="64b62-157">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="64b62-158">Utilisez le volet **points d’arrêt** pour désactiver ou supprimer des points d’arrêt de code de ligne à partir d’un emplacement unique.</span><span class="sxs-lookup"><span data-stu-id="64b62-158">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Panneau points d’arrêt" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="64b62-160">Panneau **points d’arrêt**</span><span class="sxs-lookup"><span data-stu-id="64b62-160">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="64b62-161">Activez la case à cocher en regard d’une entrée pour désactiver ce point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="64b62-161">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="64b62-162">Cliquez avec le bouton droit sur une entrée pour supprimer ce point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="64b62-162">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="64b62-163">Cliquez avec le bouton droit n’importe où dans le volet **points d’arrêt** pour désactiver tous les points d’arrêt, désactiver tous les points d’arrêt ou supprimer tous les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="64b62-163">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="64b62-164">La désactivation de tous les points d’arrêt revient à décocher chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="64b62-164">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="64b62-165">La désactivation de tous les points d’arrêt prescrit à DevTools d’ignorer tous les points d’arrêt de la ligne de code, mais de maintenir l’état activé de façon à ce qu’ils soient dans le même État qu’avant lorsque vous les réactivez chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="64b62-165">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Points d’arrêt désactivé dans le volet points d’arrêt" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="64b62-167">Points d’arrêt désactivé dans le volet **points d’arrêt**</span><span class="sxs-lookup"><span data-stu-id="64b62-167">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="64b62-168">DOM modifier les points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="64b62-168">DOM change breakpoints</span></span>   

<span data-ttu-id="64b62-169">Utilisez un point d’arrêt de modification DOM lorsque vous souhaitez suspendre le code qui modifie un nœud DOM ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="64b62-169">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="64b62-170">Pour définir un point d’arrêt de modification DOM:</span><span class="sxs-lookup"><span data-stu-id="64b62-170">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="64b62-171">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="64b62-171">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="64b62-172">Accédez à l’élément sur lequel vous voulez définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="64b62-172">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="64b62-173">Cliquez avec le bouton droit sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="64b62-173">Right-click the element.</span></span>  
1.  <span data-ttu-id="64b62-174">Placez le pointeur de la souris **sur arrêt**, puis sélectionnez modifications de **sous-arborescences**, **modifications d’attributs**ou suppression de **nœud**.</span><span class="sxs-lookup"><span data-stu-id="64b62-174">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Menu contextuel pour la création d’un point d’arrêt de modification DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="64b62-176">Menu contextuel pour la création d’un point d’arrêt de modification DOM</span><span class="sxs-lookup"><span data-stu-id="64b62-176">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="64b62-177">Types d’arrêts de modification de DOM</span><span class="sxs-lookup"><span data-stu-id="64b62-177">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="64b62-178">**Modifications**de la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="64b62-178">**Subtree modifications**.</span></span>  <span data-ttu-id="64b62-179">Déclenché lorsqu’un enfant du nœud actuellement sélectionné est supprimé ou ajouté, ou que le contenu d’un enfant a changé.</span><span class="sxs-lookup"><span data-stu-id="64b62-179">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="64b62-180">Ne sont pas déclenchées sur les changements d’attribut de nœud enfant ou sur les modifications apportées au nœud actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64b62-180">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="64b62-181">**Modifications d’attributs**: déclenché lors de l’ajout ou de la suppression d’un attribut sur le nœud actuellement sélectionné, ou en cas de modification d’une valeur d’attribut.</span><span class="sxs-lookup"><span data-stu-id="64b62-181">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="64b62-182">**Suppression de nœud**: déclenchée lors de la suppression du nœud actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64b62-182">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="64b62-183">Points d’arrêt XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="64b62-183">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="64b62-184">Utilisez un point d’arrêt XHR lorsque vous souhaitez arrêter lorsque l’URL de requête d’un XHR contient une chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64b62-184">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="64b62-185">DevTools s’arrête sur la ligne de code où XHR exécute la `send()` méthode.</span><span class="sxs-lookup"><span data-stu-id="64b62-185">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="64b62-186">Cette fonctionnalité est également compatible avec les demandes d' [API FETCH][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="64b62-186">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="64b62-187">C’est le cas, par exemple, lorsque vous constatez qu’il s’agit d’une URL incorrecte et que vous voulez rapidement trouver le code source AJAX ou FETCH à l’origine de la demande incorrecte.</span><span class="sxs-lookup"><span data-stu-id="64b62-187">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="64b62-188">Pour définir un point d’arrêt XHR:</span><span class="sxs-lookup"><span data-stu-id="64b62-188">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="64b62-189">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="64b62-189">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="64b62-190">Développez le volet **points d’arrêt XHR** .</span><span class="sxs-lookup"><span data-stu-id="64b62-190">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="64b62-191">Cliquez sur **Ajouter un point d’arrêt**.</span><span class="sxs-lookup"><span data-stu-id="64b62-191">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="64b62-192">Entrez la chaîne que vous voulez rompre.</span><span class="sxs-lookup"><span data-stu-id="64b62-192">Enter the string which you want to break on.</span></span>  <span data-ttu-id="64b62-193">DevTools s’interrompt lorsque cette chaîne est présente n’importe où dans une URL de requête XHR.</span><span class="sxs-lookup"><span data-stu-id="64b62-193">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="64b62-194">Appuyez sur `Enter` pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="64b62-194">Press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Créer un point d’arrêt XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="64b62-196">Créer un point d’arrêt XHR</span><span class="sxs-lookup"><span data-stu-id="64b62-196">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="64b62-197">Points d’arrêt de l’écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="64b62-197">Event listener breakpoints</span></span> 

<span data-ttu-id="64b62-198">Utilisez des points d’arrêt de l’écouteur d’événements lorsque vous souhaitez suspendre le code de l’écouteur d’événements qui s’exécute après le déclenchement d’un événement.</span><span class="sxs-lookup"><span data-stu-id="64b62-198">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="64b62-199">Vous pouvez sélectionner des événements spécifiques, tels que `click` des catégories d’événements, tels que tous les événements de souris.</span><span class="sxs-lookup"><span data-stu-id="64b62-199">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="64b62-200">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="64b62-200">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="64b62-201">Développez le volet de **points d’arrêt du détecteur d’événements** .</span><span class="sxs-lookup"><span data-stu-id="64b62-201">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="64b62-202">DevTools affiche une liste de catégories d’événements, par exemple une **animation**.</span><span class="sxs-lookup"><span data-stu-id="64b62-202">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="64b62-203">Activez une de ces catégories pour suspendre chaque événement de cette catégorie ou développer la catégorie et vérifier un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="64b62-203">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Créer un point d’arrêt d’écouteur d’événements" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="64b62-205">Créer un point d’arrêt d’écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="64b62-205">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="64b62-206">Points d’arrêt d’exception</span><span class="sxs-lookup"><span data-stu-id="64b62-206">Exception breakpoints</span></span>   

<span data-ttu-id="64b62-207">Utilisez des points d’arrêt d’exception lorsque vous voulez mettre en pause la ligne de code qui lève une exception interceptée ou non interceptée.</span><span class="sxs-lookup"><span data-stu-id="64b62-207">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="64b62-208">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="64b62-208">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="64b62-209">Cliquez sur **suspendre sur les exceptions** \ ( ![ Placez le pointeur sur les exceptions ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="64b62-209">Click **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="64b62-210">L’icône devient bleu lorsque l’option est activée.</span><span class="sxs-lookup"><span data-stu-id="64b62-210">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Bouton suspendre sur les exceptions" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="64b62-212">Bouton **suspendre sur les exceptions**</span><span class="sxs-lookup"><span data-stu-id="64b62-212">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="64b62-213">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="64b62-213">**Optional**.</span></span>  <span data-ttu-id="64b62-214">Activez la case à cocher **suspendre les exceptions interceptées** si vous souhaitez également suspendre les exceptions interceptées, en plus de celles qui ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="64b62-214">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Suspendu sur une exception non interceptée" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="64b62-216">Suspendu sur une exception non interceptée</span><span class="sxs-lookup"><span data-stu-id="64b62-216">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="64b62-217">Points d’arrêt de fonction</span><span class="sxs-lookup"><span data-stu-id="64b62-217">Function breakpoints</span></span>   

<span data-ttu-id="64b62-218">Exécutez la `debug(method)` méthode, où `method` se trouve la commande, la fonction ou la méthode que vous voulez déboguer lorsque vous voulez faire dérouler chaque fois qu’une fonction spécifique est exécutée.</span><span class="sxs-lookup"><span data-stu-id="64b62-218">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="64b62-219">Vous pouvez insérer `debug()` dans votre code (par exemple `console.log()` , une instruction) ou exécuter la méthode à partir de la console devtools.</span><span class="sxs-lookup"><span data-stu-id="64b62-219">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="64b62-220">équivaut à définir un [point d’arrêt de ligne de code](#line-of-code-breakpoints) sur la première ligne de la fonction.</span><span class="sxs-lookup"><span data-stu-id="64b62-220">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="64b62-221">Vérifier que la fonction cible se trouve dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="64b62-221">Make sure the target function is in scope</span></span>   

<span data-ttu-id="64b62-222">DevTools lève une exception `ReferenceError` si la fonction que vous souhaitez déboguer n’est pas dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="64b62-222">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="64b62-223">Il est difficile de garantir que la fonction cible se trouve dans l’étendue si vous exécutez la `debug()` méthode à partir de la console devtools.</span><span class="sxs-lookup"><span data-stu-id="64b62-223">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="64b62-224">Voici une stratégie:</span><span class="sxs-lookup"><span data-stu-id="64b62-224">Here is one strategy:</span></span>  

1.  <span data-ttu-id="64b62-225">Définissez un [point d’arrêt de ligne de code](#line-of-code-breakpoints) à un emplacement où la fonction est dans Scope.</span><span class="sxs-lookup"><span data-stu-id="64b62-225">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="64b62-226">Déclenchez le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="64b62-226">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="64b62-227">Exécutez la `debug()` méthode dans la console devtools lorsque le code est toujours suspendu sur le point d’arrêt de votre code.</span><span class="sxs-lookup"><span data-stu-id="64b62-227">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "API Fetch | MDN"  

> [!NOTE]
> <span data-ttu-id="64b62-230">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="64b62-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="64b62-231">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools & phare \).</span><span class="sxs-lookup"><span data-stu-id="64b62-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="64b62-233">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="64b62-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
