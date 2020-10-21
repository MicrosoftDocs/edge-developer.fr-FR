---
description: Utilisez l’API de console pour écrire des messages dans la console.
title: Référence sur les API de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 38fb3ee2345530775423ac3ec8e53e0d8de76eaf
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125285"
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

# <span data-ttu-id="d579d-104">Référence sur les API de la console</span><span class="sxs-lookup"><span data-stu-id="d579d-104">Console API Reference</span></span>  

<span data-ttu-id="d579d-105">Utilisez les méthodes de l’API de console pour écrire des messages dans la console à partir de votre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d579d-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="d579d-106">Pour une présentation interactive de la rubrique, accédez à [la section commencer à enregistrer les messages dans la console][DevtoolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="d579d-106">For an interactive introduction to the topic, navigate to [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="d579d-107">Pour les méthodes de commodité comme celles `debug()` `monitorEvents()` disponibles uniquement dans le volet de la **console** , accédez à la référence sur l' [API des utilitaires][DevtoolConsoleUtilities]de la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <span data-ttu-id="d579d-108">évalué</span><span class="sxs-lookup"><span data-stu-id="d579d-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="d579d-109">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="d579d-110">Écrit une [erreur](#error) sur la console lorsque `expression` prend la valeur `false` .</span><span class="sxs-lookup"><span data-stu-id="d579d-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="d579d-112">Figure 1: résultat de l' `console.assert()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-113">supprime</span><span class="sxs-lookup"><span data-stu-id="d579d-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="d579d-114">Efface la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="d579d-115">Si l’option [conserver le journal][DevtoolsConsoleReferenceLevel] est activée, la méthode [Clear](#clear) est désactivée.</span><span class="sxs-lookup"><span data-stu-id="d579d-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <span data-ttu-id="d579d-116">Voir également</span><span class="sxs-lookup"><span data-stu-id="d579d-116">See also</span></span>  

*   [<span data-ttu-id="d579d-117">Effacement de la console</span><span class="sxs-lookup"><span data-stu-id="d579d-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <span data-ttu-id="d579d-118">tronçon</span><span class="sxs-lookup"><span data-stu-id="d579d-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="d579d-119">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-120">Écrit le nombre de fois où la méthode de [comptage](#count) a été appelée à la même ligne et la même `label` .</span><span class="sxs-lookup"><span data-stu-id="d579d-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="d579d-121">Utilisez la méthode [countReset](#countreset) pour réinitialiser le compte.</span><span class="sxs-lookup"><span data-stu-id="d579d-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="d579d-123">Figure 2: résultat de l' `console.count()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-124">countReset</span><span class="sxs-lookup"><span data-stu-id="d579d-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="d579d-125">Réinitialise le nombre.</span><span class="sxs-lookup"><span data-stu-id="d579d-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <span data-ttu-id="d579d-126">déboguer</span><span class="sxs-lookup"><span data-stu-id="d579d-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="d579d-127">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="d579d-128">Identique au [Journal](#log) sauf dans le niveau de journal différent.</span><span class="sxs-lookup"><span data-stu-id="d579d-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="d579d-130">Figure 3: résultat de l' `console.debug()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-131">dir</span><span class="sxs-lookup"><span data-stu-id="d579d-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="d579d-132">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-133">Imprime une représentation JSON de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="d579d-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="d579d-135">Figure 4: résultat de l' `console.dir()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="d579d-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="d579d-137">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-138">Imprime une représentation XML des descendants de `node` .</span><span class="sxs-lookup"><span data-stu-id="d579d-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="d579d-140">Figure 5: résultat de l' `console.dirxml()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-141">erreur</span><span class="sxs-lookup"><span data-stu-id="d579d-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="d579d-142">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="d579d-143">Imprime la `object` dans la console, la convertit en tant qu’erreur et inclut une trace de pile.</span><span class="sxs-lookup"><span data-stu-id="d579d-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="d579d-145">Figure 6: résultat de l' `console.error()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-146">groupe</span><span class="sxs-lookup"><span data-stu-id="d579d-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="d579d-147">Rassemble les messages visuellement ensemble jusqu’à ce que la méthode [groupEnd](#groupend) soit utilisée.</span><span class="sxs-lookup"><span data-stu-id="d579d-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="d579d-148">Utilisez la méthode [groupCollapsed](#groupcollapsed) pour réduire le groupe lors de son enregistrement initial dans la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-group-button.msft.png":::
   <span data-ttu-id="d579d-150">Figure 7: résultat de l' `console.group()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="d579d-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="d579d-152">Identique à la méthode [log](#log) , sauf que le groupe est réduit au départ lorsqu’il est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <span data-ttu-id="d579d-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="d579d-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="d579d-154">Arrête le regroupement visuel des messages.</span><span class="sxs-lookup"><span data-stu-id="d579d-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="d579d-155">Voir la méthode de [groupe](#group) .</span><span class="sxs-lookup"><span data-stu-id="d579d-155">See the [group](#group) method.</span></span>  

---  

## <span data-ttu-id="d579d-156">des informations</span><span class="sxs-lookup"><span data-stu-id="d579d-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="d579d-157">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-158">Identique à la méthode [log](#log) .</span><span class="sxs-lookup"><span data-stu-id="d579d-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="d579d-160">Figure 8: résultat de l' `console.info()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-161">Journal</span><span class="sxs-lookup"><span data-stu-id="d579d-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="d579d-162">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-163">Affiche un message sur la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="d579d-165">Figure 9: résultat de l' `console.log()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-166">tabulaire</span><span class="sxs-lookup"><span data-stu-id="d579d-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="d579d-167">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-168">Enregistre un tableau d’objets sous forme de table.</span><span class="sxs-lookup"><span data-stu-id="d579d-168">Logs an array of objects as a table.</span></span>  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-table-button.msft.png":::
   <span data-ttu-id="d579d-170">Figure 10: résultat de l' `console.table()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-171">time</span><span class="sxs-lookup"><span data-stu-id="d579d-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="d579d-172">Démarre un nouveau minuteur.</span><span class="sxs-lookup"><span data-stu-id="d579d-172">Starts a new timer.</span></span>  <span data-ttu-id="d579d-173">Utilisez la méthode [timeEnd](#timeend) pour arrêter le minuteur et imprimer le temps écoulé vers la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="d579d-175">Figure 11: résultat de l' `console.time()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-176">timeEnd</span><span class="sxs-lookup"><span data-stu-id="d579d-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="d579d-177">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-178">Arrête une minuterie.</span><span class="sxs-lookup"><span data-stu-id="d579d-178">Stops a timer.</span></span>  <span data-ttu-id="d579d-179">Voir la méthode [Time](#time) .</span><span class="sxs-lookup"><span data-stu-id="d579d-179">See the [time](#time) method.</span></span>  

---  

## <span data-ttu-id="d579d-180">repérer</span><span class="sxs-lookup"><span data-stu-id="d579d-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="d579d-181">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="d579d-182">Imprime une trace de pile sur la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="d579d-184">Figure 12: résultat de l' `console.trace()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="d579d-185">informé</span><span class="sxs-lookup"><span data-stu-id="d579d-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="d579d-186">[Niveau du journal][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="d579d-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="d579d-187">Affiche un avertissement sur la console.</span><span class="sxs-lookup"><span data-stu-id="d579d-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="d579d-189">Figure 13: résultat de l' `console.warn()` exemple</span><span class="sxs-lookup"><span data-stu-id="d579d-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

## <span data-ttu-id="d579d-190">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="d579d-190">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Commencer à utiliser la journalisation des messages dans la console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "XXXXXX xxxxxxx xxx xxxxxxxxx"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Effacement de la console-référence de la console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Faire persister les messages sur les chargements de page-référence de la console"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrer par niveau du journal-référence de la console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

> [!NOTE]
> <span data-ttu-id="d579d-197">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d579d-197">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d579d-198">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="d579d-198">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="d579d-200">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d579d-200">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
