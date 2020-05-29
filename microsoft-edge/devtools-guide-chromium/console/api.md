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





# Référence sur les API de la console   

  

Utilisez les méthodes de l’API de console pour écrire des messages dans la console à partir de votre JavaScript.  Pour plus d’introduction au sujet interactif, voir [utiliser la journalisation des messages dans la console][DevtoolsConsoleLog] .  Pour plus d' [information] [DevtoolConsoleUtilities] sur les méthodes de commodité comme celles `debug()` `monitorEvents()` disponibles uniquement sur la console, voir référence sur l’API des utilitaires de la console.  

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

> ##### Figure1  
> Le résultat de l' `console.assert()` exemple  
> ![Résultat de l’exemple console. Assert ().][ImageAssert]  

## supprime  

```javascript
console.clear()
```

Efface la console.  

```javascript
console.clear();  
```  

Si l’option [conserver le journal][DevtoolsConsoleReferenceLevel] est activée, la méthode [Clear](#clear) est désactivée.  

Voir aussi: [effacer la console][DevtoolsConsoleReferenceClear]  

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

> ##### Figure 2  
> Le résultat de l' `console.count()` exemple  
> ![Résultat de l’exemple console. Count ()][ImageCount]  

## countReset  

```javascript
console.countReset([label])
```  

Réinitialise le nombre.  

```javascript
console.countReset();
console.countReset('coffee');
```  

## déboguer  

```javascript
console.debug(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Identique à la méthode [log](#log) .  

```javascript
console.debug('debug');  
```  

> ##### Figure3  
> Le résultat de l' `console.debug()` exemple  
> ![Résultat de l’exemple console. Debug ()][ImageDebug]  

## dir  

```javascript
console.dir(object)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime une représentation JSON de l’objet spécifié.  

```javascript
console.dir(document.head);
```  

> ##### Figure 4  
> Le résultat de l' `console.dir()` exemple  
> ![Résultat de l’exemple console. dir ()][ImageDir]  

## dirxml  

```javascript
console.dirxml(node)
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Imprime une représentation XML des descendants de `node` .  

```javascript
console.dirxml(document);
```  

> ##### Figure 5  
> Le résultat de l' `console.dirxml()` exemple  
> ![Résultat de l’exemple console. DirXML ()][ImageDirXml]  

## erreur  

```javascript
console.error(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Error`  

Imprime la `object` dans la console, la convertit en tant qu’erreur et inclut une trace de pile.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### Figure 6  
> Le résultat de l' `console.error()` exemple  
> ![Résultat de l’exemple console. Error ()][ImageError]  

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

> ##### Figure 7  
> Le résultat de l' `console.group()` exemple  
> ![Résultat de l’exemple console. Group ().][ImageGroup]  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Identique à la méthode [log](#log) , sauf que le groupe est réduit au départ lorsqu’il est connecté à la console.  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Arrête le regroupement visuel des messages.  Voir la méthode de [groupe](#group) .  

## des informations  

```javascript
console.info(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Identique à la méthode [log](#log) .  

```javascript
console.info('info');
```  

> ##### Figure8  
> Le résultat de l' `console.info()` exemple  
> ![Résultat de l’exemple console.info ()][ImageInfo]  

## Journal  

```javascript
console.log(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Affiche un message sur la console.  

```javascript
console.log('log');
```  

> ##### Figure9  
> Le résultat de l' `console.log()` exemple  
> ![Résultat de l’exemple console. log ()][ImageLog]  

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

> ##### Figure10  
> Le résultat de l' `console.table()` exemple  
> ![Résultat de l’exemple console. table ()][ImageTable]  

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

> ##### Figure11  
> Le résultat de l' `console.time()` exemple  
> ![Résultat de l’exemple console. Time ().][ImageTime]  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Info`  

Arrête une minuterie.  Voir la méthode [Time](#time) .  

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

> ##### Figure12  
> Le résultat de l' `console.trace()` exemple  
> ![Résultat de l’exemple console. trace ()][ImageTrace]  

## informé  

```javascript
console.warn(object [, object, ...])
```  

[Niveau du journal][DevtoolsConsoleReferencePersist]: `Warning`  

Affiche un avertissement sur la console.  

```javascript
console.warn('warn');
```  

> ##### Figure13  
> Le résultat de l' `console.warn()` exemple  
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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/api) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
