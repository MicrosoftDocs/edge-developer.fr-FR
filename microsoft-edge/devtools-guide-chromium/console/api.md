---
description: Utilisez l’API console pour écrire des messages dans la console.
title: Référence de l’API de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 08a29db4dec05de0a21a0e6a9de9a0fb6e0d3f56
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564510"
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
# <a name="console-api-reference"></a><span data-ttu-id="aa0ab-104">Référence de l’API de console</span><span class="sxs-lookup"><span data-stu-id="aa0ab-104">Console API reference</span></span>  

<span data-ttu-id="aa0ab-105">**L’outil** Console est utile lorsque vous terminez plusieurs tâches dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-105">The **Console** tool is helpful when you complete multiple tasks in the DevTools.</span></span>  <span data-ttu-id="aa0ab-106">Les API peuvent être inclues dans vos scripts.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-106">APIs are available to include in your scripts.</span></span> <span data-ttu-id="aa0ab-107">Les méthodes de commodité sont uniquement disponibles pour une utilisation dans l’outil **Console,** telles que les `debug()` méthodes et les `monitorEvents()` méthodes.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-107">Convenience methods are only available for use in the **Console** tool, such as the `debug()` and `monitorEvents()` methods.</span></span>  <span data-ttu-id="aa0ab-108">Pour plus d’informations sur la mise en place de la **console,** accédez à Commencer à [journalisation des messages dans la console.][DevtoolsConsoleConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="aa0ab-108">For more information on getting started with the **Console**, navigate to [Get started with logging messages to the Console][DevtoolsConsoleConsoleLog].</span></span>  <span data-ttu-id="aa0ab-109">Pour plus d’informations sur les méthodes pratiques de la **console,** accédez à référence de [l’API des utilitaires de console.][DevtoolConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="aa0ab-109">For more information on the convenience methods in the **Console**, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="aa0ab-110">assert</span><span class="sxs-lookup"><span data-stu-id="aa0ab-110">assert</span></span>  

<span data-ttu-id="aa0ab-111">Cette méthode écrit une [erreur dans](#error) la **console** lorsqu’elle est évaluée `expression` à `false` .</span><span class="sxs-lookup"><span data-stu-id="aa0ab-111">This method writes an [error](#error) to the **Console** when `expression` evaluates to `false`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-112">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-112">JavaScript syntax</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="aa0ab-113">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-113">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-114">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-114">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-115">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-115">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const x = 5;
      const y = 3;
      const reason = 'x is expected to be less than y';
      console.assert(x < y, {x, y, reason});
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-116">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-116">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Résultat de l’exemple console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         <span data-ttu-id="aa0ab-118">Résultat de `console.assert()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-118">The result of the `console.assert()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a><span data-ttu-id="aa0ab-119">clear</span><span class="sxs-lookup"><span data-stu-id="aa0ab-119">clear</span></span>  

<span data-ttu-id="aa0ab-120">Cette méthode permet d’effacer la **console.**</span><span class="sxs-lookup"><span data-stu-id="aa0ab-120">This method clears the **Console**.</span></span>  

<span data-ttu-id="aa0ab-121">Si [conserver le journal][DevtoolsConsoleReferenceFilter] est désactivé, la méthode [Clear](#clear) est désactivée.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-121">If [Preserve Log][DevtoolsConsoleReferenceFilter] is turned on, the [clear](#clear) method is turned off.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-122">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-122">JavaScript syntax</span></span>  

```javascript
console.clear()
```

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-123">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-123">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-124">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-124">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-125">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-125">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a><span data-ttu-id="aa0ab-126">Voir également</span><span class="sxs-lookup"><span data-stu-id="aa0ab-126">See also</span></span>  

*   [<span data-ttu-id="aa0ab-127">Effacer la console</span><span class="sxs-lookup"><span data-stu-id="aa0ab-127">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="aa0ab-128">count</span><span class="sxs-lookup"><span data-stu-id="aa0ab-128">count</span></span>  

<span data-ttu-id="aa0ab-129">Cette méthode écrit le nombre de fois que la méthode [count](#count) a été invoquée sur la même ligne et avec la même `label` .</span><span class="sxs-lookup"><span data-stu-id="aa0ab-129">This method writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="aa0ab-130">Utilisez la [méthode countReset](#countreset) pour réinitialiser le nombre.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-130">Use the [countReset](#countreset) method to reset the count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-131">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-131">JavaScript syntax</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="aa0ab-132">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-133">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-133">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-134">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.count();
      console.count('coffee');
      console.count();
      console.count();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-135">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-135">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Résultat de l’exemple console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         <span data-ttu-id="aa0ab-137">Résultat de `console.count()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-137">The result of the `console.count()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="aa0ab-138">countReset</span><span class="sxs-lookup"><span data-stu-id="aa0ab-138">countReset</span></span>  

<span data-ttu-id="aa0ab-139">Cette méthode réinitialise un nombre.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-139">This method resets a count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-140">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-140">JavaScript syntax</span></span>  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-141">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-141">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-142">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-142">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.countReset();
      console.countReset('coffee');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-143">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-143">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a><span data-ttu-id="aa0ab-144">déboguer</span><span class="sxs-lookup"><span data-stu-id="aa0ab-144">debug</span></span>  

<span data-ttu-id="aa0ab-145">Cette méthode est identique à la méthode [log,](#log) à l’exception d’un niveau de journal différent.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-145">This method is identical to the [log](#log) method, except different log level.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-146">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-146">JavaScript syntax</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="aa0ab-147">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-147">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-148">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-148">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-149">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-149">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-150">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-150">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Résultat de l’exemple console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         <span data-ttu-id="aa0ab-152">Résultat de `console.debug()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-152">The result of the `console.debug()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a><span data-ttu-id="aa0ab-153">dir</span><span class="sxs-lookup"><span data-stu-id="aa0ab-153">dir</span></span>  

<span data-ttu-id="aa0ab-154">Cette méthode imprime une représentation JSON de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-154">This method prints a JSON representation of the specified object.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-155">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-155">JavaScript syntax</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="aa0ab-156">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-156">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-157">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-157">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-158">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-159">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-159">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Résultat de l’exemple console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         <span data-ttu-id="aa0ab-161">Résultat de `console.dir()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-161">The result of the `console.dir()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="aa0ab-162">dirxml</span><span class="sxs-lookup"><span data-stu-id="aa0ab-162">dirxml</span></span>  

<span data-ttu-id="aa0ab-163">Cette méthode imprime une représentation XML des descendants de `node` .</span><span class="sxs-lookup"><span data-stu-id="aa0ab-163">This method prints an XML representation of the descendants of `node`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-164">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-164">JavaScript syntax</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="aa0ab-165">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-165">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-166">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-166">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-167">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-167">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-168">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-168">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Résultat de l’exemple console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
         <span data-ttu-id="aa0ab-170">Résultat de `console.dirxml()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-170">The result of the `console.dirxml()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a><span data-ttu-id="aa0ab-171">erreur</span><span class="sxs-lookup"><span data-stu-id="aa0ab-171">error</span></span>  

<span data-ttu-id="aa0ab-172">Cette méthode imprime la console, la formate comme une erreur `object` et inclut une trace de pile. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="aa0ab-172">This method prints the `object` to the **Console**, formats it as an error, and includes a stack trace.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-173">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-173">JavaScript syntax</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="aa0ab-174">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-175">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-175">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-176">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-177">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-177">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Résultat de l’exemple console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         <span data-ttu-id="aa0ab-179">Résultat de `console.error()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-179">The result of the `console.error()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a><span data-ttu-id="aa0ab-180">groupe</span><span class="sxs-lookup"><span data-stu-id="aa0ab-180">group</span></span>  

<span data-ttu-id="aa0ab-181">Cette méthode groupe visuellement les messages jusqu’à ce que la [méthode groupEnd](#groupend) soit utilisée.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-181">This method visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="aa0ab-182">Utilisez la [méthode groupCollapsed](#groupcollapsed) pour réduire le groupe lorsqu’il se connecte initialement à la **console.**</span><span class="sxs-lookup"><span data-stu-id="aa0ab-182">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it initially logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-183">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-183">JavaScript syntax</span></span>  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-184">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-184">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-185">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const label = 'Adolescent Irradiated Espionage Tortoises';
      console.group(label);
      console.info('Leo');
      console.info('Mike');
      console.info('Don');
      console.info('Raph');
      console.groupEnd(label);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-186">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-186">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Résultat de l’exemple console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         <span data-ttu-id="aa0ab-188">Résultat de `console.group()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-188">The result of the `console.group()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="aa0ab-189">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="aa0ab-189">groupCollapsed</span></span>  

<span data-ttu-id="aa0ab-190">Cette méthode est identique à la méthode [log,](#log) sauf que le groupe est initialement réduire lorsqu’il se connecte à la **console.**</span><span class="sxs-lookup"><span data-stu-id="aa0ab-190">This method is identical to the [log](#log) method, except the group is initially collapsed when it logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-191">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-191">JavaScript syntax</span></span>  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a><span data-ttu-id="aa0ab-192">groupEnd</span><span class="sxs-lookup"><span data-stu-id="aa0ab-192">groupEnd</span></span>  

<span data-ttu-id="aa0ab-193">Cette méthode arrête de grouper visuellement les messages.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-193">This method stops visually grouping messages.</span></span>  <span data-ttu-id="aa0ab-194">Accédez à la [méthode de](#group) groupe.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-194">Navigate to the [group](#group) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-195">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-195">JavaScript syntax</span></span>  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a><span data-ttu-id="aa0ab-196">informations</span><span class="sxs-lookup"><span data-stu-id="aa0ab-196">info</span></span>  

<span data-ttu-id="aa0ab-197">Cette méthode est identique à la [méthode log.](#log)</span><span class="sxs-lookup"><span data-stu-id="aa0ab-197">This method is identical to the [log](#log) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-198">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-198">JavaScript syntax</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="aa0ab-199">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-199">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-200">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-200">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-201">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-202">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-202">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Résultat de l’exemple console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         <span data-ttu-id="aa0ab-204">Résultat de `console.info()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-204">The result of the `console.info()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a><span data-ttu-id="aa0ab-205">log</span><span class="sxs-lookup"><span data-stu-id="aa0ab-205">log</span></span>  

<span data-ttu-id="aa0ab-206">Cette méthode imprime un message dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="aa0ab-206">This method prints a message to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-207">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-207">JavaScript syntax</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="aa0ab-208">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-208">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-209">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-209">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-210">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-211">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-211">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Résultat de l’exemple console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         <span data-ttu-id="aa0ab-213">Résultat de `console.log()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-213">The result of the `console.log()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="aa0ab-214">table</span><span class="sxs-lookup"><span data-stu-id="aa0ab-214">table</span></span>  

<span data-ttu-id="aa0ab-215">Cette méthode enregistre un tableau d’objets en tant que tableau.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-215">This method logs an array of objects as a table.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-216">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-216">JavaScript syntax</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="aa0ab-217">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-217">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-218">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-218">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-219">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-219">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.table([
          {
              first: 'René',
              last: 'Magritte',
          },
          {
              first: 'Chaim',
              last: 'Soutine',
              birthday: '18930113',
          },
          {
              first: 'Henri',
              last: 'Matisse',
          }
      ]);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-220">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-220">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Résultat de l’exemple console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         <span data-ttu-id="aa0ab-222">Résultat de `console.table()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-222">The result of the `console.table()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a><span data-ttu-id="aa0ab-223">time</span><span class="sxs-lookup"><span data-stu-id="aa0ab-223">time</span></span>  

<span data-ttu-id="aa0ab-224">Cette méthode démarre un nouveau timer.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-224">This method starts a new timer.</span></span>  <span data-ttu-id="aa0ab-225">Utilisez la [méthode timeEnd](#timeend) pour arrêter le timer et imprimer le temps écoulé sur la **console.**</span><span class="sxs-lookup"><span data-stu-id="aa0ab-225">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-226">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-226">JavaScript syntax</span></span>  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-227">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-227">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-228">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.time();
      for (var i = 0; i < 100000; i++) {
          let square = i ** 2;
      }
      console.timeEnd();
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-229">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-229">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Résultat de l’exemple console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         <span data-ttu-id="aa0ab-231">Résultat de `console.time()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-231">The result of the `console.time()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="aa0ab-232">timeEnd</span><span class="sxs-lookup"><span data-stu-id="aa0ab-232">timeEnd</span></span>  

<span data-ttu-id="aa0ab-233">Cette méthode arrête un timer.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-233">This method stops a timer.</span></span>  <span data-ttu-id="aa0ab-234">Pour plus d’informations, accédez à la [méthode d’heure.](#time)</span><span class="sxs-lookup"><span data-stu-id="aa0ab-234">For more information, navigate to the [time](#time) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-235">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-235">JavaScript syntax</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="aa0ab-236">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-236">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

---  

## <a name="trace"></a><span data-ttu-id="aa0ab-237">trace</span><span class="sxs-lookup"><span data-stu-id="aa0ab-237">trace</span></span>  

<span data-ttu-id="aa0ab-238">Cette méthode imprime une trace de pile sur la **console.**</span><span class="sxs-lookup"><span data-stu-id="aa0ab-238">This method prints a stack trace to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-239">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-239">JavaScript syntax</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="aa0ab-240">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-240">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-241">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-241">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-242">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-242">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const first = () => { second(); };
      const second = () => { third(); };
      const third = () => { fourth(); };
      const fourth = () => { console.trace(); };
      first();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-243">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-243">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Résultat de l’exemple console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         <span data-ttu-id="aa0ab-245">Résultat de `console.trace()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-245">The result of the `console.trace()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a><span data-ttu-id="aa0ab-246">warn</span><span class="sxs-lookup"><span data-stu-id="aa0ab-246">warn</span></span>  

<span data-ttu-id="aa0ab-247">Cette méthode imprime un avertissement sur la **console.**</span><span class="sxs-lookup"><span data-stu-id="aa0ab-247">This method prints a warning to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa0ab-248">Syntaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-248">JavaScript syntax</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="aa0ab-249">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa0ab-249">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

### <a name="javascript-example"></a><span data-ttu-id="aa0ab-250">Exemple JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa0ab-250">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa0ab-251">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa0ab-252">Sortie</span><span class="sxs-lookup"><span data-stu-id="aa0ab-252">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Résultat de l’exemple console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
         <span data-ttu-id="aa0ab-254">Résultat de `console.warn()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa0ab-254">The result of the `console.warn()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="aa0ab-255">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="aa0ab-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Logs in the Console tool | Documents Microsoft"  
[DevtoolConsoleUtilities]: ./utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Effacer la console - Référence de la console | Documents Microsoft"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtrer par niveau de journal – Référence de la console | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Persist messages across page loads - Console reference | Documents Microsoft"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Présentation de Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="aa0ab-262">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa0ab-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aa0ab-263">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="aa0ab-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="aa0ab-265">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa0ab-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
