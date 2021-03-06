---
description: Utilisez l’API console pour écrire des messages dans la console.
title: Référence de l’API de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f38a7403cf11fbec5f5833fc0b1ed10207b436de
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398048"
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

# <a name="console-api-reference"></a><span data-ttu-id="5143b-104">Référence de l’API de console</span><span class="sxs-lookup"><span data-stu-id="5143b-104">Console API reference</span></span>  

<span data-ttu-id="5143b-105">Utilisez les méthodes de l’API console pour écrire des messages dans la console à partir de votre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5143b-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="5143b-106">Pour une présentation interactive de la rubrique, accédez à La mise en place [de la journalisation des messages dans la console.][DevtoolsConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="5143b-106">For an interactive introduction to the topic, navigate to [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="5143b-107">Pour les méthodes pratiques telles que ou qui sont disponibles uniquement à partir du volet console, accédez à Référence de `debug()` `monitorEvents()` l’API des [utilitaires de console.][DevtoolConsoleUtilities] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5143b-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="5143b-108">assert</span><span class="sxs-lookup"><span data-stu-id="5143b-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="5143b-109">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="5143b-110">Écrit une [erreur dans](#error) la console `expression` lorsqu’elle est évaluée à `false` .</span><span class="sxs-lookup"><span data-stu-id="5143b-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Résultat de l’exemple console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="5143b-112">Figure 1 : Résultat de `console.assert()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="5143b-113">clear</span><span class="sxs-lookup"><span data-stu-id="5143b-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="5143b-114">Cette commande permet d’effacer la console.</span><span class="sxs-lookup"><span data-stu-id="5143b-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="5143b-115">Si [preserve Log][DevtoolsConsoleReferenceLevel] est activé, la méthode [Clear](#clear) est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5143b-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <a name="see-also"></a><span data-ttu-id="5143b-116">Voir également</span><span class="sxs-lookup"><span data-stu-id="5143b-116">See also</span></span>  

*   [<span data-ttu-id="5143b-117">Effacer la console</span><span class="sxs-lookup"><span data-stu-id="5143b-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="5143b-118">count</span><span class="sxs-lookup"><span data-stu-id="5143b-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="5143b-119">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-120">Écrit le nombre de fois que la méthode [count](#count) a été invoquée sur la même ligne et avec la même `label` .</span><span class="sxs-lookup"><span data-stu-id="5143b-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="5143b-121">Utilisez la [méthode countReset](#countreset) pour réinitialiser le nombre.</span><span class="sxs-lookup"><span data-stu-id="5143b-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Résultat de l’exemple console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="5143b-123">Figure 2 : Résultat de `console.count()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="5143b-124">countReset</span><span class="sxs-lookup"><span data-stu-id="5143b-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="5143b-125">Réinitialise un nombre.</span><span class="sxs-lookup"><span data-stu-id="5143b-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a><span data-ttu-id="5143b-126">déboguer</span><span class="sxs-lookup"><span data-stu-id="5143b-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="5143b-127">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="5143b-128">Identique au [journal à l’exception](#log) d’un niveau de journal différent.</span><span class="sxs-lookup"><span data-stu-id="5143b-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Résultat de l’exemple console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="5143b-130">Figure 3 : Résultat de `console.debug()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <a name="dir"></a><span data-ttu-id="5143b-131">dir</span><span class="sxs-lookup"><span data-stu-id="5143b-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="5143b-132">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-133">Imprime une représentation JSON de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="5143b-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Résultat de l’exemple console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="5143b-135">Figure 4 : Résultat de `console.dir()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="5143b-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="5143b-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="5143b-137">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-138">Imprime une représentation XML des descendants de `node` .</span><span class="sxs-lookup"><span data-stu-id="5143b-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Résultat de l’exemple console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="5143b-140">Figure 5 : Résultat de `console.dirxml()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <a name="error"></a><span data-ttu-id="5143b-141">erreur</span><span class="sxs-lookup"><span data-stu-id="5143b-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="5143b-142">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="5143b-143">Imprime la console, la formate comme une erreur `object` et inclut une trace de pile.</span><span class="sxs-lookup"><span data-stu-id="5143b-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Résultat de l’exemple console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="5143b-145">Figure 6 : Résultat de `console.error()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <a name="group"></a><span data-ttu-id="5143b-146">groupe</span><span class="sxs-lookup"><span data-stu-id="5143b-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="5143b-147">Groupe visuellement les messages jusqu’à ce que la [méthode groupEnd](#groupend) soit utilisée.</span><span class="sxs-lookup"><span data-stu-id="5143b-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="5143b-148">Utilisez la [méthode groupCollapsed pour](#groupcollapsed) réduire le groupe lorsqu’il est initialement connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="5143b-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Résultat de l’exemple console.group()" lightbox="../media/console-demo-group-button.msft.png":::
   <span data-ttu-id="5143b-150">Figure 7 : Résultat de `console.group()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="5143b-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="5143b-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="5143b-152">Identique à la [méthode de journal,](#log) sauf que le groupe est initialement réduire lorsqu’il est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="5143b-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <a name="groupend"></a><span data-ttu-id="5143b-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="5143b-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="5143b-154">Arrête de grouper visuellement les messages.</span><span class="sxs-lookup"><span data-stu-id="5143b-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="5143b-155">Accédez à la [méthode de](#group) groupe.</span><span class="sxs-lookup"><span data-stu-id="5143b-155">Navigate to the [group](#group) method.</span></span>  

---  

## <a name="info"></a><span data-ttu-id="5143b-156">des informations</span><span class="sxs-lookup"><span data-stu-id="5143b-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="5143b-157">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-158">Identique à la [méthode de](#log) journal.</span><span class="sxs-lookup"><span data-stu-id="5143b-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Résultat de l’exemple console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="5143b-160">Figure 8 : Résultat de `console.info()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <a name="log"></a><span data-ttu-id="5143b-161">log</span><span class="sxs-lookup"><span data-stu-id="5143b-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="5143b-162">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-163">Imprime un message dans la console.</span><span class="sxs-lookup"><span data-stu-id="5143b-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Résultat de l’exemple console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="5143b-165">Figure 9 : Résultat de `console.log()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <a name="table"></a><span data-ttu-id="5143b-166">table</span><span class="sxs-lookup"><span data-stu-id="5143b-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="5143b-167">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-168">Enregistre un tableau d’objets en tant que tableau.</span><span class="sxs-lookup"><span data-stu-id="5143b-168">Logs an array of objects as a table.</span></span>  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Résultat de l’exemple console.table()" lightbox="../media/console-demo-table-button.msft.png":::
   <span data-ttu-id="5143b-170">Figure 10 : Résultat de `console.table()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <a name="time"></a><span data-ttu-id="5143b-171">time</span><span class="sxs-lookup"><span data-stu-id="5143b-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="5143b-172">Démarre un nouveau timer.</span><span class="sxs-lookup"><span data-stu-id="5143b-172">Starts a new timer.</span></span>  <span data-ttu-id="5143b-173">Utilisez la [méthode timeEnd](#timeend) pour arrêter le timer et imprimer le temps écoulé sur la console.</span><span class="sxs-lookup"><span data-stu-id="5143b-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Résultat de l’exemple console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="5143b-175">Figure 11 : Résultat de `console.time()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="5143b-176">timeEnd</span><span class="sxs-lookup"><span data-stu-id="5143b-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="5143b-177">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-178">Arrête un timer.</span><span class="sxs-lookup"><span data-stu-id="5143b-178">Stops a timer.</span></span>  <span data-ttu-id="5143b-179">Accédez à la [méthode d’heure.](#time)</span><span class="sxs-lookup"><span data-stu-id="5143b-179">Navigate to the [time](#time) method.</span></span>  

---  

## <a name="trace"></a><span data-ttu-id="5143b-180">trace</span><span class="sxs-lookup"><span data-stu-id="5143b-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="5143b-181">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="5143b-182">Imprime une trace de pile sur la console.</span><span class="sxs-lookup"><span data-stu-id="5143b-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Résultat de l’exemple console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="5143b-184">Figure 12 : Résultat de `console.trace()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <a name="warn"></a><span data-ttu-id="5143b-185">warn</span><span class="sxs-lookup"><span data-stu-id="5143b-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="5143b-186">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="5143b-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="5143b-187">Imprime un avertissement sur la console.</span><span class="sxs-lookup"><span data-stu-id="5143b-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Résultat de l’exemple console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="5143b-189">Figure 13 : Résultat de `console.warn()` l’exemple</span><span class="sxs-lookup"><span data-stu-id="5143b-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5143b-190">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="5143b-190">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Mise en place de la journalisation des messages dans la console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Référence de l’API des utilitaires de console"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Effacer la console - Référence de console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Persist messages across page loads - Console Reference"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrer par niveau de journal - Référence de la console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (Chromium)"  

> [!NOTE]
> <span data-ttu-id="5143b-197">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5143b-197">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5143b-198">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5143b-198">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5143b-200">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5143b-200">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
