---
description: Utilisez l'API console pour écrire des messages dans la console.
title: Référence de l’API de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 54b89e25501449a1e5119afa812a0535fbc6ffbb
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483253"
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

**L'outil** Console est utile lorsque vous terminez plusieurs tâches dans DevTools.  Les API peuvent être inclues dans vos scripts. Les méthodes de commodité sont uniquement disponibles pour une utilisation dans l'outil **Console,** telles que les `debug()` méthodes et les `monitorEvents()` méthodes.  Pour plus d'informations sur la mise en place de la **console,** accédez à Commencer à [journalisation des messages dans la console.][DevtoolsConsoleConsoleLog]  Pour plus d'informations sur les méthodes pratiques de la **console,** accédez à référence de [l'API des utilitaires de console.][DevtoolConsoleUtilities]  

---  

## <a name="assert"></a>assert  

Cette méthode écrit une [erreur dans](#error) la **console** `expression` lorsqu'elle est évaluée à `false` .  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.assert(expression, object)
```

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
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
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Résultat de l'exemple console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         Résultat de `console.assert()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a>clear  

Cette méthode permet d'effacer la **console.**  

Si [conserver le journal][DevtoolsConsoleReferenceFilter] est désactivé, la méthode [Clear](#clear) est désactivée.  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.clear()
```

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a>Voir également  

*   [Effacer la console][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

Cette méthode écrit le nombre de fois que la méthode [count](#count) a été invoquée sur la même ligne et avec la même `label` .  Utilisez la [méthode countReset](#countreset) pour réinitialiser le nombre.  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.count([label])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
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
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Résultat de l'exemple console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         Résultat de `console.count()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a>countReset  

Cette méthode réinitialise un nombre.  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
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
      Sortie
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a>déboguer  

Cette méthode est identique à la méthode [log,](#log) à l'exception d'un niveau de journal différent.  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.debug(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Verbose`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Résultat de l'exemple console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         Résultat de `console.debug()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a>dir  

Cette méthode imprime une représentation JSON de l'objet spécifié.  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.dir(object)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Résultat de l'exemple console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         Résultat de `console.dir()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a>dirxml  

Cette méthode imprime une représentation XML des descendants de `node` .  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.dirxml(node)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Résultat de l'exemple console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
         Résultat de `console.dirxml()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a>erreur  

Cette méthode imprime la console, la formate comme une erreur `object` et inclut une trace de pile. ****  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.error(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Résultat de l'exemple console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         Résultat de `console.error()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a>groupe  

Cette méthode groupe visuellement les messages jusqu'à ce que la [méthode groupEnd](#groupend) soit utilisée.  Utilisez la [méthode groupCollapsed](#groupcollapsed) pour réduire le groupe lorsqu'il se connecte initialement à la **console.**  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
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
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Résultat de l'exemple console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         Résultat de `console.group()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

Cette méthode est identique à la méthode [log,](#log) sauf que le groupe est initialement réduire lorsqu'il se connecte à la **console.**  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a>groupEnd  

Cette méthode arrête de grouper visuellement les messages.  Accédez à la [méthode de](#group) groupe.  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a>informations  

Cette méthode est identique à la [méthode log.](#log)  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.info(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Résultat de l'exemple console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         Résultat de `console.info()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a>log  

Cette méthode imprime un message dans la **console.**  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.log(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Résultat de l'exemple console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         Résultat de `console.log()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>table  

Cette méthode enregistre un tableau d'objets en tant que tableau.  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.table(array)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
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
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Résultat de l'exemple console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         Résultat de `console.table()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a>time  

Cette méthode démarre un nouveau timer.  Utilisez la [méthode timeEnd](#timeend) pour arrêter le timer et imprimer le temps écoulé sur la **console.**  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
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
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Résultat de l'exemple console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         Résultat de `console.time()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a>timeEnd  

Cette méthode arrête un timer.  Pour plus d'informations, accédez à la [méthode d'heure.](#time)  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.timeEnd([label])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

---  

## <a name="trace"></a>trace  

Cette méthode imprime une trace de pile sur la **console.**  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.trace()
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
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
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Résultat de l'exemple console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         Résultat de `console.trace()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a>warn  

Cette méthode imprime un avertissement sur la **console.**  

### <a name="javascript-syntax"></a>Syntaxe JavaScript  

```javascript
console.warn(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Warning`  

### <a name="javascript-example"></a>Exemple JavaScript  

:::row:::
   :::column span="1":::
      Entrée  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Sortie
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Résultat de l'exemple console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
         Résultat de `console.warn()` l'exemple  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Logs in the Console tool | Documents Microsoft"  
[DevtoolConsoleUtilities]: ./utilities.md "Référence de l'API des utilitaires de console | Documents Microsoft"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Effacer la console - Référence de la console | Documents Microsoft"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtrer par niveau de journal – Référence de la console | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Persist messages across page loads - Console reference | Documents Microsoft"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Présentation de Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
