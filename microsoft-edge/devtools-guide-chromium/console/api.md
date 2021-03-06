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

# <a name="console-api-reference"></a>Référence de l’API de console  

Utilisez les méthodes de l’API console pour écrire des messages dans la console à partir de votre JavaScript.  Pour une présentation interactive de la rubrique, accédez à La mise en place [de la journalisation des messages dans la console.][DevtoolsConsoleLog]  Pour les méthodes pratiques telles que ou qui sont disponibles uniquement à partir du volet console, accédez à Référence de `debug()` `monitorEvents()` l’API des [utilitaires de console.][DevtoolConsoleUtilities] ****  

---  

## <a name="assert"></a>assert  

```javascript
console.assert(expression, object)
```

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Écrit une [erreur dans](#error) la console `expression` lorsqu’elle est évaluée à `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Résultat de l’exemple console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   Figure 1 : Résultat de `console.assert()` l’exemple  
:::image-end:::  

---  

## <a name="clear"></a>clear  

```javascript
console.clear()
```

Cette commande permet d’effacer la console.  

```javascript
console.clear();  
```  

Si [preserve Log][DevtoolsConsoleReferenceLevel] est activé, la méthode [Clear](#clear) est désactivée.  

### <a name="see-also"></a>Voir également  

*   [Effacer la console][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

```javascript
console.count([label])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Écrit le nombre de fois que la méthode [count](#count) a été invoquée sur la même ligne et avec la même `label` .  Utilisez la [méthode countReset](#countreset) pour réinitialiser le nombre.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Résultat de l’exemple console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   Figure 2 : Résultat de `console.count()` l’exemple  
:::image-end:::  

---  

## <a name="countreset"></a>countReset  

```javascript
console.countReset([label])
```  

Réinitialise un nombre.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a>déboguer  

```javascript
console.debug(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Verbose`

Identique au [journal à l’exception](#log) d’un niveau de journal différent.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Résultat de l’exemple console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   Figure 3 : Résultat de `console.debug()` l’exemple  
:::image-end:::  

---  

## <a name="dir"></a>dir  

```javascript
console.dir(object)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime une représentation JSON de l’objet spécifié.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Résultat de l’exemple console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   Figure 4 : Résultat de `console.dir()` l’exemple  
:::image-end:::  

---  

## <a name="dirxml"></a>dirxml  

```javascript
console.dirxml(node)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime une représentation XML des descendants de `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Résultat de l’exemple console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Figure 5 : Résultat de `console.dirxml()` l’exemple  
:::image-end:::  

---  

## <a name="error"></a>erreur  

```javascript
console.error(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Error`  

Imprime la console, la formate comme une erreur `object` et inclut une trace de pile.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Résultat de l’exemple console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   Figure 6 : Résultat de `console.error()` l’exemple  
:::image-end:::  

---  

## <a name="group"></a>groupe  

```javascript
console.group(label)
```  

Groupe visuellement les messages jusqu’à ce que la [méthode groupEnd](#groupend) soit utilisée.  Utilisez la [méthode groupCollapsed pour](#groupcollapsed) réduire le groupe lorsqu’il est initialement connecté à la console.  

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
   Figure 7 : Résultat de `console.group()` l’exemple  
:::image-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Identique à la [méthode de journal,](#log) sauf que le groupe est initialement réduire lorsqu’il est connecté à la console.  

---  

## <a name="groupend"></a>groupEnd  

```javascript
console.groupEnd(label)
```  

Arrête de grouper visuellement les messages.  Accédez à la [méthode de](#group) groupe.  

---  

## <a name="info"></a>des informations  

```javascript
console.info(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Identique à la [méthode de](#log) journal.  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Résultat de l’exemple console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   Figure 8 : Résultat de `console.info()` l’exemple  
:::image-end:::  

---  

## <a name="log"></a>log  

```javascript
console.log(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime un message dans la console.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Résultat de l’exemple console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   Figure 9 : Résultat de `console.log()` l’exemple  
:::image-end:::  

---  

## <a name="table"></a>table  

```javascript
console.table(array)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Enregistre un tableau d’objets en tant que tableau.  

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
   Figure 10 : Résultat de `console.table()` l’exemple  
:::image-end:::  

---  

## <a name="time"></a>time  

```javascript
console.time([label])
```  

Démarre un nouveau timer.  Utilisez la [méthode timeEnd](#timeend) pour arrêter le timer et imprimer le temps écoulé sur la console.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Résultat de l’exemple console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   Figure 11 : Résultat de `console.time()` l’exemple  
:::image-end:::  

---  

## <a name="timeend"></a>timeEnd  

```javascript
console.timeEnd([label])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Arrête un timer.  Accédez à la [méthode d’heure.](#time)  

---  

## <a name="trace"></a>trace  

```javascript
console.trace()
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime une trace de pile sur la console.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Résultat de l’exemple console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   Figure 12 : Résultat de `console.trace()` l’exemple  
:::image-end:::  

---  

## <a name="warn"></a>warn  

```javascript
console.warn(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Warning`  

Imprime un avertissement sur la console.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Résultat de l’exemple console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   Figure 13 : Résultat de `console.warn()` l’exemple  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Mise en place de la journalisation des messages dans la console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Référence de l’API des utilitaires de console"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Effacer la console - Référence de console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Persist messages across page loads - Console Reference"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrer par niveau de journal - Référence de la console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (Chromium)"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
