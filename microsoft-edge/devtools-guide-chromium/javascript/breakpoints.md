---
description: Découvrez toutes les façons dont vous pouvez suspendre votre code dans Microsoft Edge DevTools.
title: Comment suspendre votre code avec des points d'arrêt dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: dd865f346046cb6706e71fdb3cc869950b2b4352
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519358"
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

# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a><span data-ttu-id="a146c-104">Comment suspendre votre code avec des points d'arrêt dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a146c-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="a146c-105">Utilisez des points d'arrêt pour suspendre votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a146c-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="a146c-106">Cet article explique chaque type de point d'arrêt disponible dans DevTools, ainsi que le moment où utiliser et comment définir chaque type.</span><span class="sxs-lookup"><span data-stu-id="a146c-106">This article explains each type of breakpoint available in DevTools, as well as when to use and how to set each type.</span></span>

<span data-ttu-id="a146c-107">Pour un didacticiel d'introduction utilisant une page web existante, accédez à Commencer à déboguer JavaScript dans [Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="a146c-107">For an introductory tutorial using an existing webpage, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>

## <a name="overview-of-when-to-use-each-breakpoint-type"></a><span data-ttu-id="a146c-108">Vue d'ensemble de l'utilisation de chaque type de point d'arrêt</span><span class="sxs-lookup"><span data-stu-id="a146c-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="a146c-109">Le type de point d'arrêt le plus connu est la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="a146c-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="a146c-110">Toutefois, les points d'arrêt de ligne de code peuvent être inefficaces à définir, en particulier si vous ne savez pas exactement où rechercher, ou si vous travaillez avec une base de code de grande taille.</span><span class="sxs-lookup"><span data-stu-id="a146c-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="a146c-111">Vous pouvez gagner du temps lors du débogage en sachant comment et quand utiliser les autres types de points d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="a146c-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="a146c-112">Type de point d'arrêt</span><span class="sxs-lookup"><span data-stu-id="a146c-112">Breakpoint Type</span></span> | <span data-ttu-id="a146c-113">Utilisez-le lorsque vous souhaitez suspendre...</span><span class="sxs-lookup"><span data-stu-id="a146c-113">Use This When You Want To Pause...</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="a146c-114">Ligne de code</span><span class="sxs-lookup"><span data-stu-id="a146c-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="a146c-115">Sur une zone de code exacte.</span><span class="sxs-lookup"><span data-stu-id="a146c-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="a146c-116">Ligne de code conditionnelle</span><span class="sxs-lookup"><span data-stu-id="a146c-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="a146c-117">Sur une zone de code exacte, mais uniquement lorsqu'une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="a146c-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="a146c-118">DOM</span><span class="sxs-lookup"><span data-stu-id="a146c-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="a146c-119">Sur le code qui modifie ou supprime un nœud DOM spécifique, ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="a146c-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="a146c-120">XHR</span><span class="sxs-lookup"><span data-stu-id="a146c-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="a146c-121">Lorsqu'une URL XHR contient un modèle de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a146c-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="a146c-122">Listener d'événements</span><span class="sxs-lookup"><span data-stu-id="a146c-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="a146c-123">Sur le code qui s'exécute après un événement, tel `click` que , s'exécute.</span><span class="sxs-lookup"><span data-stu-id="a146c-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="a146c-124">Exception</span><span class="sxs-lookup"><span data-stu-id="a146c-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="a146c-125">Sur la ligne de code qui lance une exception capturée ou non.</span><span class="sxs-lookup"><span data-stu-id="a146c-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="a146c-126">Fonction</span><span class="sxs-lookup"><span data-stu-id="a146c-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="a146c-127">Chaque fois qu'une commande, une fonction ou une méthode spécifique est exécuté.</span><span class="sxs-lookup"><span data-stu-id="a146c-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <a name="line-of-code-breakpoints"></a><span data-ttu-id="a146c-128">Points d'arrêt de ligne de code</span><span class="sxs-lookup"><span data-stu-id="a146c-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="a146c-129">Utilisez un point d'arrêt de ligne de code lorsque vous connaissez la région exacte du code que vous devez examiner.</span><span class="sxs-lookup"><span data-stu-id="a146c-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="a146c-130">DevTools s'interrompt toujours avant l'utilisation de cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="a146c-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="a146c-131">Pour définir un point d'arrêt de ligne de code dans DevTools :</span><span class="sxs-lookup"><span data-stu-id="a146c-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="a146c-132">Choisissez **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="a146c-132">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="a146c-133">Ouvrez le fichier contenant la ligne de code sur laquelle vous souhaitez rompre.</span><span class="sxs-lookup"><span data-stu-id="a146c-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="a146c-134">Aller à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="a146c-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="a146c-135">À gauche de la ligne de code se trouve la colonne de numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="a146c-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="a146c-136">Sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="a146c-136">Choose it.</span></span>  <span data-ttu-id="a146c-137">Une icône rouge s'affiche en côté de la colonne de numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="a146c-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un point d'arrêt de ligne de code" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="a146c-139">Un point d'arrêt de ligne de code</span><span class="sxs-lookup"><span data-stu-id="a146c-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a><span data-ttu-id="a146c-140">Points d'arrêt de ligne de code dans votre code</span><span class="sxs-lookup"><span data-stu-id="a146c-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="a146c-141">Exécutez `debugger` la méthode à partir de votre code pour suspendre cette ligne.</span><span class="sxs-lookup"><span data-stu-id="a146c-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="a146c-142">Cela équivaut à un point d'arrêt de ligne de [code,](#line-of-code-breakpoints)sauf que le point d'arrêt est définie dans votre code, et non dans l'interface utilisateur de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a146c-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a><span data-ttu-id="a146c-143">Points d'arrêt de ligne de code conditionnels</span><span class="sxs-lookup"><span data-stu-id="a146c-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="a146c-144">Utilisez un point d'arrêt de ligne de code conditionnel lorsque vous connaissez la région exacte du code que vous devez examiner, mais que vous souhaitez suspendre uniquement lorsqu'une autre condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="a146c-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="a146c-145">Pour définir un point d'arrêt de ligne de code conditionnel :</span><span class="sxs-lookup"><span data-stu-id="a146c-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="a146c-146">Choisissez **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="a146c-146">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="a146c-147">Ouvrez le fichier contenant la ligne de code sur laquelle vous souhaitez rompre.</span><span class="sxs-lookup"><span data-stu-id="a146c-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="a146c-148">Aller à la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="a146c-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="a146c-149">À gauche de la ligne de code se trouve la colonne de numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="a146c-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="a146c-150">Pointez sur le numéro de ligne et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="a146c-150">Hover on the line number and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="a146c-151">Choisissez **Ajouter un point d'arrêt conditionnel.**</span><span class="sxs-lookup"><span data-stu-id="a146c-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="a146c-152">Une boîte de dialogue s'affiche sous la ligne de code.</span><span class="sxs-lookup"><span data-stu-id="a146c-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="a146c-153">Entrez votre condition dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a146c-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="a146c-154">Activez `Enter` le point d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="a146c-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="a146c-155">Icône en de côté de la colonne de numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="a146c-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Un point d'arrêt de ligne de code conditionnel" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="a146c-157">Un point d'arrêt de ligne de code conditionnel</span><span class="sxs-lookup"><span data-stu-id="a146c-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a><span data-ttu-id="a146c-158">Gérer les points d'arrêt de ligne de code</span><span class="sxs-lookup"><span data-stu-id="a146c-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="a146c-159">Utilisez le **volet Points d'arrêt** pour désactiver ou supprimer des points d'arrêt de ligne de code à partir d'un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="a146c-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Panneau Points d'arrêt" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="a146c-161">Panneau **Points d'arrêt**</span><span class="sxs-lookup"><span data-stu-id="a146c-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="a146c-162">Cochez la case en regard d'une entrée pour désactiver ce point d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="a146c-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="a146c-163">Pointez sur une entrée et ouvrez le menu contextuel \(clic droit\) pour supprimer ce point d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="a146c-163">Hover on an entry and open the contextual menu \(right-click\) to remove that breakpoint.</span></span>  
*   <span data-ttu-id="a146c-164">Pointez n'importe où dans le volet Points d'arrêt et ouvrez le menu contextuel \(clic droit\) pour désactiver tous les points d'arrêt, désactiver tous les points d'arrêt ou supprimer tous les points d'arrêt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a146c-164">Hover anywhere in the **Breakpoints** pane and open the contextual menu \(right-click\) to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="a146c-165">La désactivation de tous les points d'arrêt équivaut à désactiver chacun d'eux.</span><span class="sxs-lookup"><span data-stu-id="a146c-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="a146c-166">La désactivation de tous les points d'arrêt indique à DevTools d'ignorer tous les points d'arrêt de ligne de code, mais de maintenir également l'état activé afin que chacun d'eux soit dans le même état qu'auparavant lorsque vous réactivez chacun d'eux.</span><span class="sxs-lookup"><span data-stu-id="a146c-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Points d'arrêt désactivés dans le volet Points d'arrêt" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="a146c-168">Points d'arrêt désactivés dans le volet Points **d'arrêt**</span><span class="sxs-lookup"><span data-stu-id="a146c-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a><span data-ttu-id="a146c-169">Points d'arrêt des changements DOM</span><span class="sxs-lookup"><span data-stu-id="a146c-169">DOM change breakpoints</span></span>  

<span data-ttu-id="a146c-170">Utilisez un point d'arrêt de modification DOM lorsque vous souhaitez suspendre le code qui modifie un nœud DOM ou les enfants.</span><span class="sxs-lookup"><span data-stu-id="a146c-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="a146c-171">Pour définir un point d'arrêt de modification DOM :</span><span class="sxs-lookup"><span data-stu-id="a146c-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="a146c-172">Choisissez **l'outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="a146c-172">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="a146c-173">Go the element on which you want to set the breakpoint.</span><span class="sxs-lookup"><span data-stu-id="a146c-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="a146c-174">Pointez sur l'élément et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="a146c-174">Hover on the element and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="a146c-175">Pointez sur **Pause,** puis choisissez **Modifications de sous-arbre,** **Modifications d'attribut**ou suppression **de nœud.**</span><span class="sxs-lookup"><span data-stu-id="a146c-175">Hover on **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Menu contexté pour la création d'un point d'arrêt de modification DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="a146c-177">Menu contexté pour la création d'un point d'arrêt de modification DOM</span><span class="sxs-lookup"><span data-stu-id="a146c-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a><span data-ttu-id="a146c-178">Types de points d'arrêt de modification DOM</span><span class="sxs-lookup"><span data-stu-id="a146c-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="a146c-179">**Modifications de sous-arbre**.</span><span class="sxs-lookup"><span data-stu-id="a146c-179">**Subtree modifications**.</span></span>  <span data-ttu-id="a146c-180">Déclenché lorsqu'un enfant du nœud actuellement sélectionné est supprimé ou ajouté, ou lorsque le contenu d'un enfant est modifié.</span><span class="sxs-lookup"><span data-stu-id="a146c-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="a146c-181">Ne se déclenche pas lors des modifications de l'attribut de nœud enfant ou des modifications apportées au nœud actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a146c-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="a146c-182">**Modifications des attributs**: déclenchées lorsqu'un attribut est ajouté ou supprimé sur le nœud actuellement sélectionné, ou lorsqu'une valeur d'attribut change.</span><span class="sxs-lookup"><span data-stu-id="a146c-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="a146c-183">**Suppression de nœud**: déclenchée lorsque le nœud actuellement sélectionné est supprimé.</span><span class="sxs-lookup"><span data-stu-id="a146c-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <a name="xhrfetch-breakpoints"></a><span data-ttu-id="a146c-184">Points d'arrêt XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="a146c-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="a146c-185">Utilisez un point d'arrêt XHR lorsque vous souhaitez rompre lorsque l'URL de demande d'un XHR contient une chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a146c-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="a146c-186">DevTools s'interrompt sur la ligne de code où le XHR exécute la `send()` méthode.</span><span class="sxs-lookup"><span data-stu-id="a146c-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="a146c-187">Cette fonctionnalité fonctionne également avec les [demandes d'API Fetch.][MDNFetchApi]</span><span class="sxs-lookup"><span data-stu-id="a146c-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="a146c-188">Par exemple, cela est utile lorsque votre page web demande une URL incorrecte et que vous souhaitez trouver rapidement le code source AJAX ou Fetch à l'origine de la demande incorrecte.</span><span class="sxs-lookup"><span data-stu-id="a146c-188">One example of when this is helpful is when your webpage is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="a146c-189">Pour définir un point d'arrêt XHR :</span><span class="sxs-lookup"><span data-stu-id="a146c-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="a146c-190">Choisissez **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="a146c-190">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="a146c-191">Développez le **panneau Points d'arrêt XHR.**</span><span class="sxs-lookup"><span data-stu-id="a146c-191">Expand the **XHR Breakpoints** panel.</span></span>  
1.  <span data-ttu-id="a146c-192">Choisissez **Ajouter un point d'arrêt.**</span><span class="sxs-lookup"><span data-stu-id="a146c-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="a146c-193">Entrez la chaîne sur laquelle vous souhaitez rompre.</span><span class="sxs-lookup"><span data-stu-id="a146c-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="a146c-194">DevTools s'interrompt lorsque cette chaîne est présente n'importe où dans une URL de demande XHR.</span><span class="sxs-lookup"><span data-stu-id="a146c-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="a146c-195">Sélectionnez `Enter` pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="a146c-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Créer un point d'arrêt XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="a146c-197">Créer un point d'arrêt XHR</span><span class="sxs-lookup"><span data-stu-id="a146c-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a><span data-ttu-id="a146c-198">Points d'arrêt du lanceur d'événements</span><span class="sxs-lookup"><span data-stu-id="a146c-198">Event listener breakpoints</span></span>  

<span data-ttu-id="a146c-199">Utilisez des points d'arrêt de l'écoute d'événements lorsque vous souhaitez suspendre le code de l'écoute d'événement qui s'exécute après le déclenché d'un événement.</span><span class="sxs-lookup"><span data-stu-id="a146c-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="a146c-200">Vous pouvez sélectionner des événements spécifiques, tels que, ou des catégories d'événements, tels que tous `click` les événements de souris.</span><span class="sxs-lookup"><span data-stu-id="a146c-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="a146c-201">Choisissez **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="a146c-201">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="a146c-202">Développez le **panneau Points d'arrêt de l'écoute d'événements.**</span><span class="sxs-lookup"><span data-stu-id="a146c-202">Expand the **Event Listener Breakpoints** panel.</span></span>  <span data-ttu-id="a146c-203">DevTools affiche une liste de catégories d'événements, **telles**que Animation .</span><span class="sxs-lookup"><span data-stu-id="a146c-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="a146c-204">Vérifiez l'une de ces catégories pour suspendre chaque fois qu'un événement de cette catégorie est déclenché, ou développez la catégorie et vérifiez un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="a146c-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Créer un point d'arrêt de l'écoute d'événements" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="a146c-206">Créer un point d'arrêt de l'écoute d'événements</span><span class="sxs-lookup"><span data-stu-id="a146c-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a><span data-ttu-id="a146c-207">Points d'arrêt d'exception</span><span class="sxs-lookup"><span data-stu-id="a146c-207">Exception breakpoints</span></span>  

<span data-ttu-id="a146c-208">Utilisez des points d'arrêt d'exception lorsque vous souhaitez suspendre la ligne de code qui lance une exception capturée ou non.</span><span class="sxs-lookup"><span data-stu-id="a146c-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="a146c-209">Choisissez **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="a146c-209">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="a146c-210">Choose **Pause on exceptions** \( ![ Pause on exceptions ](../media/pause-on-exceptions-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="a146c-210">Choose **Pause on exceptions** \(![Pause on exceptions](../media/pause-on-exceptions-icon.msft.png)\).</span></span>  <span data-ttu-id="a146c-211">L'icône devient bleue lorsqu'elle est activée.</span><span class="sxs-lookup"><span data-stu-id="a146c-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Bouton Pause sur les exceptions" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="a146c-213">Bouton **Pause sur les exceptions**</span><span class="sxs-lookup"><span data-stu-id="a146c-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a146c-214">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="a146c-214">**Optional**.</span></span>  <span data-ttu-id="a146c-215">Cochez la case Pause sur les **exceptions** capturées si vous souhaitez également suspendre les exceptions capturées, en plus des exceptions non capturées.</span><span class="sxs-lookup"><span data-stu-id="a146c-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Suspendu sur une exception non importante" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="a146c-217">Suspendu sur une exception non importante</span><span class="sxs-lookup"><span data-stu-id="a146c-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <a name="function-breakpoints"></a><span data-ttu-id="a146c-218">Points d'arrêt des fonctions</span><span class="sxs-lookup"><span data-stu-id="a146c-218">Function breakpoints</span></span>  

<span data-ttu-id="a146c-219">Exécutez la méthode, où se trouve la commande, la fonction ou la méthode que vous souhaitez déboguer, lorsque vous souhaitez suspendre chaque fois qu'une `debug(method)` `method` fonction spécifique est exécuté.</span><span class="sxs-lookup"><span data-stu-id="a146c-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="a146c-220">Vous pouvez insérer dans votre code (comme une instruction) ou exécuter la méthode à partir `debug()` `console.log()` de la console DevTools.</span><span class="sxs-lookup"><span data-stu-id="a146c-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="a146c-221">équivaut à définir un [point d'arrêt de ligne de code](#line-of-code-breakpoints) sur la première ligne de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a146c-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a><span data-ttu-id="a146c-222">Assurez-vous que la fonction cible est dans l'étendue</span><span class="sxs-lookup"><span data-stu-id="a146c-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="a146c-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span><span class="sxs-lookup"><span data-stu-id="a146c-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="a146c-224">S'assurer que la fonction cible est dans l'étendue est difficile si vous exécutez la méthode à partir `debug()` de la console DevTools.</span><span class="sxs-lookup"><span data-stu-id="a146c-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="a146c-225">Voici une stratégie :</span><span class="sxs-lookup"><span data-stu-id="a146c-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="a146c-226">Définissez [un point d'arrêt de ligne](#line-of-code-breakpoints) de code quelque part où la fonction est dans l'étendue.</span><span class="sxs-lookup"><span data-stu-id="a146c-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="a146c-227">Déclenchez le point d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="a146c-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="a146c-228">Exécutez `debug()` la méthode dans la console DevTools alors que le code est toujours suspendu sur votre point d'arrêt de ligne de code.</span><span class="sxs-lookup"><span data-stu-id="a146c-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <a name="related-articles"></a><span data-ttu-id="a146c-229">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a146c-229">Related articles</span></span>

*   <span data-ttu-id="a146c-230">[Utilisez les fonctionnalités du débogger][DevtoolsJavascriptReference] : à l'aide de l'interface utilisateur du débogger dans **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="a146c-230">[Use the debugger features][DevtoolsJavascriptReference] - Using the UI of the debugger in the **Sources** tool.</span></span>
*   <span data-ttu-id="a146c-231">[Commencer à déboguer JavaScript dans Microsoft Edge DevTools][DevtoolsJavascriptIndex] - Didacticiel d'introduction à l'aide d'une page web existante.</span><span class="sxs-lookup"><span data-stu-id="a146c-231">[Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex] - An introductory tutorial using an existing webpage.</span></span>
*   <span data-ttu-id="a146c-232">[Vue d'ensemble][DevtoolsSourcesIndex] de l'outil Sources : le débogger fait partie de l'outil **Sources,** qui inclut un éditeur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a146c-232">[Sources tool overview][DevtoolsSourcesIndex] - The debugger is part of the **Sources** tool, which includes a JavaScript editor.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a146c-233">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a146c-233">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavascriptReference]: ./reference.md "Utiliser les fonctionnalités de débogger | Documents Microsoft"  

[DevtoolsJavascriptIndex]: index.md "Commencer à déboguer JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

[DevtoolsSourcesIndex]: ../sources/index.md "Vue d'ensemble de l'outil Sources | Documents Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Récupérer les | API MDN"  

> [!NOTE]
> <span data-ttu-id="a146c-238">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a146c-238">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a146c-239">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="a146c-239">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a146c-241">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a146c-241">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
