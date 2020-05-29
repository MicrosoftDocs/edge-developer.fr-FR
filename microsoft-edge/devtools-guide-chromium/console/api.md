---
title: Référence sur les API de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: e54bae7c7c61584ccd39568f1bb54312cc2082c0
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601753"
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





# <span data-ttu-id="43ab2-103">Référence sur les API de la console</span><span class="sxs-lookup"><span data-stu-id="43ab2-103">Console API Reference</span></span>   

  

<span data-ttu-id="43ab2-104">Utilisez les méthodes de l’API de console pour écrire des messages dans la console à partir de votre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="43ab2-104">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="43ab2-105">Pour plus d’introduction au sujet interactif, voir [utiliser la journalisation des messages dans la console][DevtoolsConsoleLog] .</span><span class="sxs-lookup"><span data-stu-id="43ab2-105">See [Get Started With Logging Messages To The Console][DevtoolsConsoleLog] for an interactive introduction to the topic.</span></span>  <span data-ttu-id="43ab2-106">Pour plus d' [information] [DevtoolConsoleUtilities] sur les méthodes de commodité comme celles `debug()` `monitorEvents()` disponibles uniquement sur la console, voir référence sur l’API des utilitaires de la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-106">See [Console Utilities API Reference] [DevtoolConsoleUtilities] if you are looking for the convenience methods like `debug()` or `monitorEvents()` which are only available from the Console.</span></span>  

## <span data-ttu-id="43ab2-107">évalué</span><span class="sxs-lookup"><span data-stu-id="43ab2-107">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="43ab2-108">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-108">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="43ab2-109">Écrit une [erreur](#error) sur la console lorsque `expression` prend la valeur `false` .</span><span class="sxs-lookup"><span data-stu-id="43ab2-109">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### <span data-ttu-id="43ab2-110">Figure1</span><span class="sxs-lookup"><span data-stu-id="43ab2-110">Figure 1</span></span>  
> <span data-ttu-id="43ab2-111">Le résultat de l' `console.assert()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-111">The result of the `console.assert()` example</span></span>  
> ![Résultat de l’exemple console. Assert ().][ImageAssert]  

## <span data-ttu-id="43ab2-113">supprime</span><span class="sxs-lookup"><span data-stu-id="43ab2-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="43ab2-114">Efface la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="43ab2-115">Si l’option [conserver le journal][DevtoolsConsoleReferenceLevel] est activée, la méthode [Clear](#clear) est désactivée.</span><span class="sxs-lookup"><span data-stu-id="43ab2-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

<span data-ttu-id="43ab2-116">Voir aussi: [effacer la console][DevtoolsConsoleReferenceClear]</span><span class="sxs-lookup"><span data-stu-id="43ab2-116">See also: [Clear the Console][DevtoolsConsoleReferenceClear]</span></span>  

## <span data-ttu-id="43ab2-117">tronçon</span><span class="sxs-lookup"><span data-stu-id="43ab2-117">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="43ab2-118">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-118">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-119">Écrit le nombre de fois où la méthode de [comptage](#count) a été appelée à la même ligne et la même `label` .</span><span class="sxs-lookup"><span data-stu-id="43ab2-119">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="43ab2-120">Utilisez la méthode [countReset](#countreset) pour réinitialiser le compte.</span><span class="sxs-lookup"><span data-stu-id="43ab2-120">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### <span data-ttu-id="43ab2-121">Figure 2</span><span class="sxs-lookup"><span data-stu-id="43ab2-121">Figure 2</span></span>  
> <span data-ttu-id="43ab2-122">Le résultat de l' `console.count()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-122">The result of the `console.count()` example</span></span>  
> ![Résultat de l’exemple console. Count ()][ImageCount]  

## <span data-ttu-id="43ab2-124">countReset</span><span class="sxs-lookup"><span data-stu-id="43ab2-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="43ab2-125">Réinitialise le nombre.</span><span class="sxs-lookup"><span data-stu-id="43ab2-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

## <span data-ttu-id="43ab2-126">déboguer</span><span class="sxs-lookup"><span data-stu-id="43ab2-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="43ab2-127">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-128">Identique à la méthode [log](#log) .</span><span class="sxs-lookup"><span data-stu-id="43ab2-128">Identical to the [log](#log) method.</span></span>  

```javascript
console.debug('debug');  
```  

> ##### <span data-ttu-id="43ab2-129">Figure3</span><span class="sxs-lookup"><span data-stu-id="43ab2-129">Figure 3</span></span>  
> <span data-ttu-id="43ab2-130">Le résultat de l' `console.debug()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-130">The result of the `console.debug()` example</span></span>  
> ![Résultat de l’exemple console. Debug ()][ImageDebug]  

## <span data-ttu-id="43ab2-132">dir</span><span class="sxs-lookup"><span data-stu-id="43ab2-132">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="43ab2-133">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-133">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-134">Imprime une représentation JSON de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="43ab2-134">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

> ##### <span data-ttu-id="43ab2-135">Figure 4</span><span class="sxs-lookup"><span data-stu-id="43ab2-135">Figure 4</span></span>  
> <span data-ttu-id="43ab2-136">Le résultat de l' `console.dir()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-136">The result of the `console.dir()` example</span></span>  
> ![Résultat de l’exemple console. dir ()][ImageDir]  

## <span data-ttu-id="43ab2-138">dirxml</span><span class="sxs-lookup"><span data-stu-id="43ab2-138">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="43ab2-139">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-139">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-140">Imprime une représentation XML des descendants de `node` .</span><span class="sxs-lookup"><span data-stu-id="43ab2-140">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

> ##### <span data-ttu-id="43ab2-141">Figure 5</span><span class="sxs-lookup"><span data-stu-id="43ab2-141">Figure 5</span></span>  
> <span data-ttu-id="43ab2-142">Le résultat de l' `console.dirxml()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-142">The result of the `console.dirxml()` example</span></span>  
> ![Résultat de l’exemple console. DirXML ()][ImageDirXml]  

## <span data-ttu-id="43ab2-144">erreur</span><span class="sxs-lookup"><span data-stu-id="43ab2-144">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="43ab2-145">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-145">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="43ab2-146">Imprime la `object` dans la console, la convertit en tant qu’erreur et inclut une trace de pile.</span><span class="sxs-lookup"><span data-stu-id="43ab2-146">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### <span data-ttu-id="43ab2-147">Figure 6</span><span class="sxs-lookup"><span data-stu-id="43ab2-147">Figure 6</span></span>  
> <span data-ttu-id="43ab2-148">Le résultat de l' `console.error()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-148">The result of the `console.error()` example</span></span>  
> ![Résultat de l’exemple console. Error ()][ImageError]  

## <span data-ttu-id="43ab2-150">groupe</span><span class="sxs-lookup"><span data-stu-id="43ab2-150">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="43ab2-151">Rassemble les messages visuellement ensemble jusqu’à ce que la méthode [groupEnd](#groupend) soit utilisée.</span><span class="sxs-lookup"><span data-stu-id="43ab2-151">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="43ab2-152">Utilisez la méthode [groupCollapsed](#groupcollapsed) pour réduire le groupe lors de son enregistrement initial dans la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-152">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### <span data-ttu-id="43ab2-153">Figure 7</span><span class="sxs-lookup"><span data-stu-id="43ab2-153">Figure 7</span></span>  
> <span data-ttu-id="43ab2-154">Le résultat de l' `console.group()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-154">The result of the `console.group()` example</span></span>  
> ![Résultat de l’exemple console. Group ().][ImageGroup]  

## <span data-ttu-id="43ab2-156">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="43ab2-156">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="43ab2-157">Identique à la méthode [log](#log) , sauf que le groupe est réduit au départ lorsqu’il est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-157">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

## <span data-ttu-id="43ab2-158">groupEnd</span><span class="sxs-lookup"><span data-stu-id="43ab2-158">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="43ab2-159">Arrête le regroupement visuel des messages.</span><span class="sxs-lookup"><span data-stu-id="43ab2-159">Stops visually grouping messages.</span></span>  <span data-ttu-id="43ab2-160">Voir la méthode de [groupe](#group) .</span><span class="sxs-lookup"><span data-stu-id="43ab2-160">See the [group](#group) method.</span></span>  

## <span data-ttu-id="43ab2-161">des informations</span><span class="sxs-lookup"><span data-stu-id="43ab2-161">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="43ab2-162">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-163">Identique à la méthode [log](#log) .</span><span class="sxs-lookup"><span data-stu-id="43ab2-163">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

> ##### <span data-ttu-id="43ab2-164">Figure8</span><span class="sxs-lookup"><span data-stu-id="43ab2-164">Figure 8</span></span>  
> <span data-ttu-id="43ab2-165">Le résultat de l' `console.info()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-165">The result of the `console.info()` example</span></span>  
> ![Résultat de l’exemple console.info ()][ImageInfo]  

## <span data-ttu-id="43ab2-167">Journal</span><span class="sxs-lookup"><span data-stu-id="43ab2-167">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="43ab2-168">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-168">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-169">Affiche un message sur la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-169">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

> ##### <span data-ttu-id="43ab2-170">Figure9</span><span class="sxs-lookup"><span data-stu-id="43ab2-170">Figure 9</span></span>  
> <span data-ttu-id="43ab2-171">Le résultat de l' `console.log()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-171">The result of the `console.log()` example</span></span>  
> ![Résultat de l’exemple console. log ()][ImageLog]  

## <span data-ttu-id="43ab2-173">tabulaire</span><span class="sxs-lookup"><span data-stu-id="43ab2-173">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="43ab2-174">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-175">Enregistre un tableau d’objets sous forme de table.</span><span class="sxs-lookup"><span data-stu-id="43ab2-175">Logs an array of objects as a table.</span></span>  

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

> ##### <span data-ttu-id="43ab2-176">Figure10</span><span class="sxs-lookup"><span data-stu-id="43ab2-176">Figure 10</span></span>  
> <span data-ttu-id="43ab2-177">Le résultat de l' `console.table()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-177">The result of the `console.table()` example</span></span>  
> ![Résultat de l’exemple console. table ()][ImageTable]  

## <span data-ttu-id="43ab2-179">time</span><span class="sxs-lookup"><span data-stu-id="43ab2-179">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="43ab2-180">Démarre un nouveau minuteur.</span><span class="sxs-lookup"><span data-stu-id="43ab2-180">Starts a new timer.</span></span>  <span data-ttu-id="43ab2-181">Utilisez la méthode [timeEnd](#timeend) pour arrêter le minuteur et imprimer le temps écoulé vers la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-181">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### <span data-ttu-id="43ab2-182">Figure11</span><span class="sxs-lookup"><span data-stu-id="43ab2-182">Figure 11</span></span>  
> <span data-ttu-id="43ab2-183">Le résultat de l' `console.time()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-183">The result of the `console.time()` example</span></span>  
> ![Résultat de l’exemple console. Time ().][ImageTime]  

## <span data-ttu-id="43ab2-185">timeEnd</span><span class="sxs-lookup"><span data-stu-id="43ab2-185">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="43ab2-186">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-187">Arrête une minuterie.</span><span class="sxs-lookup"><span data-stu-id="43ab2-187">Stops a timer.</span></span>  <span data-ttu-id="43ab2-188">Voir la méthode [Time](#time) .</span><span class="sxs-lookup"><span data-stu-id="43ab2-188">See the [time](#time) method.</span></span>  

## <span data-ttu-id="43ab2-189">repérer</span><span class="sxs-lookup"><span data-stu-id="43ab2-189">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="43ab2-190">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-190">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="43ab2-191">Imprime une trace de pile sur la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-191">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### <span data-ttu-id="43ab2-192">Figure12</span><span class="sxs-lookup"><span data-stu-id="43ab2-192">Figure 12</span></span>  
> <span data-ttu-id="43ab2-193">Le résultat de l' `console.trace()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-193">The result of the `console.trace()` example</span></span>  
> ![Résultat de l’exemple console. trace ()][ImageTrace]  

## <span data-ttu-id="43ab2-195">informé</span><span class="sxs-lookup"><span data-stu-id="43ab2-195">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="43ab2-196">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="43ab2-196">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="43ab2-197">Affiche un avertissement sur la console.</span><span class="sxs-lookup"><span data-stu-id="43ab2-197">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

> ##### <span data-ttu-id="43ab2-198">Figure13</span><span class="sxs-lookup"><span data-stu-id="43ab2-198">Figure 13</span></span>  
> <span data-ttu-id="43ab2-199">Le résultat de l' `console.warn()` exemple</span><span class="sxs-lookup"><span data-stu-id="43ab2-199">The result of the `console.warn()` example</span></span>  
> ![Résultat de l’exemple console. Warn ().][ImageWarn]  

   

  

<!-- image links -->  

[ImageAssert]: /microsoft-edge/devtools-guide-chromium/media/console-demo-assert-button.msft.png "Figure 1: exemple de résultat de la console. Assert ()"  
[ImageCount]: /microsoft-edge/devtools-guide-chromium/media/console-demo-count-button.msft.png "Figure 2: exemple de la console. Count ()"  
[ImageDebug]: /microsoft-edge/devtools-guide-chromium/media/console-demo-debug-button.msft.png "Figure 3: Voici le résultat de l’exemple console. Debug ()."  
[ImageDir]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dir-button.msft.png "Figure 4: résultat de l’exemple console. dir ()"  
[ImageDirXml]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dirxml-button.msft.png "Figure 5: Voici le résultat de l’exemple console. DirXML ()"  
[ImageError]: /microsoft-edge/devtools-guide-chromium/media/console-demo-error-button.msft.png "Figure 6: exemple de valeur de la console. Error ()"  
[ImageGroup]: /microsoft-edge/devtools-guide-chromium/media/console-demo-group-button.msft.png "Figure 7: exemples de la console. Group ()"  
[ImageInfo]: /microsoft-edge/devtools-guide-chromium/media/console-demo-info-button.msft.png "Figure 8: résultat de l’exemple console.info ()"  
[ImageLog]: /microsoft-edge/devtools-guide-chromium/media/console-demo-log-button.msft.png "Figure 9: Voici le résultat de l’exemple console. log ()"  
[ImageTable]: /microsoft-edge/devtools-guide-chromium/media/console-demo-table-button.msft.png "Figure 10: Voici le résultat de l’exemple console. table ()"  
[ImageTime]: /microsoft-edge/devtools-guide-chromium/media/console-demo-time-button.msft.png "Figure 11: exemple du résultat de la console. Time ()"  
[ImageTrace]: /microsoft-edge/devtools-guide-chromium/media/console-demo-trace-button.msft.png "Figure 12: Voici le résultat de l’exemple console. trace ()."  
[ImageWarn]: /microsoft-edge/devtools-guide-chromium/media/console-demo-warn-button.msft.png "Figure 13: exemple de valeur de la console. Warn ()"  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Commencer à utiliser la journalisation des messages dans la console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "XXXXXX xxxxxxx xxx xxxxxxxxx"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Effacement de la console-référence de la console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Faire persister les messages sur les chargements de page-référence de la console"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrer par niveau du journal-référence de la console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

> [!NOTE]
> <span data-ttu-id="43ab2-220">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43ab2-220">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="43ab2-221">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="43ab2-221">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="43ab2-223">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43ab2-223">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
