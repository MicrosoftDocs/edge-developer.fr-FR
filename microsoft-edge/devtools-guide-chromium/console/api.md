---
title: Référence sur les API de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 19545759ede4252f2e7ba21329d482f4eb96f0c6
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708476"
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

# Référence sur les API de la console  

Utilisez les méthodes de l’API de console pour écrire des messages dans la console à partir de votre JavaScript.  Pour consulter une présentation interactive de la rubrique, voir [utiliser la journalisation des messages dans la console][DevtoolsConsoleLog].  Pour les méthodes de commodité comme celles `debug()` `monitorEvents()` disponibles uniquement dans le volet de la **console** , voir référence sur l' [API des utilitaires][DevtoolConsoleUtilities]de la console.  

---  

## évalué  

```javascript
console.assert(expression, object)
```

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Écrit une [erreur](#error) sur la console lorsque `expression` prend la valeur `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Résultat de l’exemple console. Assert ()." lightbox="../media/console-demo-assert-button.msft.png":::
   Figure 1: résultat de l' `console.assert()` exemple  
:::image-end:::  

---  

## supprime  

```javascript
console.clear()
```

Efface la console.  

```javascript
console.clear();  
```  

Si l’option [conserver le journal][DevtoolsConsoleReferenceLevel] est activée, la méthode [Clear](#clear) est désactivée.  

### Voir également  

*   [Effacement de la console][DevtoolsConsoleReferenceClear]  

---  

## tronçon  

```javascript
console.count([label])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Écrit le nombre de fois où la méthode de [comptage](#count) a été appelée à la même ligne et la même `label` .  Utilisez la méthode [countReset](#countreset) pour réinitialiser le compte.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Résultat de l’exemple console. Count ()" lightbox="../media/console-demo-count-button.msft.png":::
   Figure 2: résultat de l' `console.count()` exemple  
:::image-end:::  

---  

## countReset  

```javascript
console.countReset([label])
```  

Réinitialise le nombre.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## déboguer  

```javascript
console.debug(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Verbose`

Identique au [Journal](#log) sauf dans le niveau de journal différent.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Résultat de l’exemple console. Debug ()" lightbox="../media/console-demo-debug-button.msft.png":::
   Figure 3: résultat de l' `console.debug()` exemple  
:::image-end:::  

---  

## dir  

```javascript
console.dir(object)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime une représentation JSON de l’objet spécifié.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Résultat de l’exemple console. dir ()" lightbox="../media/console-demo-dir-button.msft.png":::
   Figure 4: résultat de l' `console.dir()` exemple  
:::image-end:::  

---  

## dirxml  

```javascript
console.dirxml(node)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime une représentation XML des descendants de `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Résultat de l’exemple console. DirXML ()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Figure 5: résultat de l' `console.dirxml()` exemple  
:::image-end:::  

---  

## erreur  

```javascript
console.error(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Error`  

Imprime la `object` dans la console, la convertit en tant qu’erreur et inclut une trace de pile.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Résultat de l’exemple console. Error ()" lightbox="../media/console-demo-error-button.msft.png":::
   Figure 6: résultat de l' `console.error()` exemple  
:::image-end:::  

---  

## groupe  

```javascript
console.group(label)
```  

Rassemble les messages visuellement ensemble jusqu’à ce que la méthode [groupEnd](#groupend) soit utilisée.  Utilisez la méthode [groupCollapsed](#groupcollapsed) pour réduire le groupe lors de son enregistrement initial dans la console.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Résultat de l’exemple console. Group ()." lightbox="../media/console-demo-group-button.msft.png":::
   Figure 7: résultat de l' `console.group()` exemple  
:::image-end:::  

---  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Identique à la méthode [log](#log) , sauf que le groupe est réduit au départ lorsqu’il est connecté à la console.  

---  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Arrête le regroupement visuel des messages.  Voir la méthode de [groupe](#group) .  

---  

## des informations  

```javascript
console.info(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Identique à la méthode [log](#log) .  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Résultat de l’exemple console.info ()" lightbox="../media/console-demo-info-button.msft.png":::
   Figure 8: résultat de l' `console.info()` exemple  
:::image-end:::  

---  

## Journal  

```javascript
console.log(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Affiche un message sur la console.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Résultat de l’exemple console. log ()" lightbox="../media/console-demo-log-button.msft.png":::
   Figure 9: résultat de l' `console.log()` exemple  
:::image-end:::  

---  

## tabulaire  

```javascript
console.table(array)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Enregistre un tableau d’objets sous forme de table.  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Résultat de l’exemple console. table ()" lightbox="../media/console-demo-table-button.msft.png":::
   Figure 10: résultat de l' `console.table()` exemple  
:::image-end:::  

---  

## time  

```javascript
console.time([label])
```  

Démarre un nouveau minuteur.  Utilisez la méthode [timeEnd](#timeend) pour arrêter le minuteur et imprimer le temps écoulé vers la console.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Résultat de l’exemple console. Time ()." lightbox="../media/console-demo-time-button.msft.png":::
   Figure 11: résultat de l' `console.time()` exemple  
:::image-end:::  

---  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Arrête une minuterie.  Voir la méthode [Time](#time) .  

---  

## repérer  

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

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Résultat de l’exemple console. trace ()" lightbox="../media/console-demo-trace-button.msft.png":::
   Figure 12: résultat de l' `console.trace()` exemple  
:::image-end:::  

---  

## informé  

```javascript
console.warn(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Warning`  

Affiche un avertissement sur la console.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Résultat de l’exemple console. Warn ()." lightbox="../media/console-demo-warn-button.msft.png":::
   Figure 13: résultat de l' `console.warn()` exemple  
:::image-end:::  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Commencer à utiliser la journalisation des messages dans la console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "XXXXXX xxxxxxx xxx xxxxxxxxx"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Effacement de la console-référence de la console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Faire persister les messages sur les chargements de page-référence de la console"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrer par niveau du journal-référence de la console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
