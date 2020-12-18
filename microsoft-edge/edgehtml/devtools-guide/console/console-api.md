---
description: Utiliser l’API de console pour déboguer et profiler votre code par programmation
title: DevTools-console-API de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, API console
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46a74b80b504358ff7dbea40970528c8e2b228cf
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232928"
---
# API de la console

L' *API console* fournit un accès par programmation et en ligne de commande à la console devtools par le biais de l' `console` objet global, ce qui vous permet d’effectuer les opérations suivantes:

 - [Enregistrer les messages personnalisés](#logging-custom-messages) de votre code
 - [Inspecter des objets et des éléments](#inspecting-objects-and-elements) et enregistrer leurs informations
 - [Tester et mesurer votre code](#testing-and-measuring) en définissant des affirmations, minuteurs et compteurs
 - [Utiliser des instantanés du tas](#taking-heap-snapshots) pour évaluer la consommation de mémoire de votre code en cours d’exécution et identifier les fuites de mémoire
 - [Tracer votre callstacks](#tracing-callstacks) pour comprendre l’emplacement à partir duquel votre code est appelé 
 - [Organiser votre sortie journal](#organizing-log-output) pour rationaliser votre débogage

Voici les commandes et les paramètres de mise en forme actuellement pris en charge par Microsoft Edge. Ils fonctionnent de la même manière sur les navigateurs les plus importants.

## Journalisation des messages personnalisés

Votre code peut envoyer différents types de messages personnalisés à la console, à savoir:

Type de message  | &nbsp;   |
:------------------- | :------ |
[**erreur ()**](https://developer.mozilla.org/docs/Web/API/Console/error) et [ **exception ()**](https://developer.mozilla.org/docs/Web/API/Console/error)| Erreurs critiques et échecs
[**Warn ()**](https://developer.mozilla.org/docs/Web/API/Console/warn) | Erreurs possibles ou comportement inattendu 
[**info ()**](https://developer.mozilla.org/docs/Web/API/Console/info) | Informations utiles, mais non critiques
[**log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) et [ **debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log) | Débogage général (sans générer d’icône d’alerte système dans la console)

   
Vous pouvez les regrouper et les filtrer en même temps que les autres messages générés par Microsoft Edge à partir de la console. Toutes les méthodes de message personnalisées nécessitent un paramètre de chaîne (message) et des paramètres de substitution de format facultatif. Microsoft Edge prend en charge les options de mise en forme suivantes:

Paramètre format | &nbsp;
:------------------- | :--- |
**% b** | Binaire
**% c** | Style CSS intraligne (Voir l’exemple ci-dessous)
**% d**, **% i** | entier. 
**% f** | Flottant  
**% s** | Chaîne 
**% x** | Hexadécimal 
**% e** | Négatifs 

Par exemple, voici comment inclure les variables chaîne et entier dans votre message électronique:

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

Vous pouvez également ajouter un effet de surbrillance vert à un message électronique avec une feuille de style CSS inline ( `%c` ):

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Journal de console avec styles intralignes](../media/console_api_css.png)

## Inspecter des objets et des éléments

Les objets inspectables apparaissent dans la console dans une arborescence réduite avec des nœuds extensibles. La console détecte si vous envoyez un nœud DOM (par exemple, une balise div) ou un objet JavaScript (par exemple, un événement) et que vous les affichez automatiquement en tant que type détecté.

Vous pouvez également forcer une sortie spécifique:

Commande | &nbsp;
:------------------- | :--- |
[**dir ()**](https://developer.mozilla.org/docs/Web/API/Console/dir) | Affiche en tant qu’objet JavaScript inspectable
[**dirxml()**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | Affiche en tant que nœud DOM inspectable

Par exemple, essayez d’ouvrir la console et de comparer les sorties suivantes pour l' `<div id='main'>` élément sur cette page:

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Comparaison de la sortie «dir» par rapport à «DirXML»](../media/console_api_dir.png)

### Sélection d’un élément dans le panneau **éléments**

Vous pouvez sélectionner un élément à l’intérieur du contexte d’arborescence HTML de la page directement dans la console pour le débogage immédiat de la disposition et du style.

Commande | &nbsp;
:------------------- | :--- |
**Select ()** | Bascule vers le panneau **éléments** et positionne le focus sur l’élément spécifié.

Par exemple, si vous ouvrez la console sur cette page et tapez:

```javascript
console.select(document.querySelector("body"));
```

Le DevTools bascule vers le panneau **éléments** (s’il n’est pas déjà actif) et définit le focus dans l' [*arborescence html*](../elements.md#html-tree-view) pour l’élément spécifié.

![Exemple de la méthode «Select»](../media/console_api_select.png)

## Tests et mesures

### Test de votre code

Ajoutez des affirmations de test de l’API console à votre code pour le test unitaire et le débogage de votre code au fur et à mesure qu’il s’exécute dans le navigateur.

Commande | &nbsp;
:------------ | :-------------
[**assertion ()**](https://developer.mozilla.org/docs/Web/API/Console/assert) | Consigne un message d’erreur de console si l’expression fournie a pour résultat la *valeur faux*.

Outre l’expression logique fournie en tant qu’assertion testable, vous pouvez ajouter un message facultatif et des paramètres de mise en forme comme vous le feriez avec d’autres [messages de console personnalisés](#logging-custom-messages). Par exemple:

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Exemple de la méthode «assertion»](../media/console_api_assert.png)

### Comptage des exécutions dans votre code

Vous pouvez définir des compteurs dans votre code pour suivre le nombre de fois que le code environnant est exécuté. La définition de compteurs permet de garantir que votre code s’exécute comme prévu et vous aide à diagnostiquer les goulets d’étranglement de performances.

Commande | &nbsp;
:------------ | :-------------
[**Count ()**](https://developer.mozilla.org/docs/Web/API/Console/count) | Augmente et enregistre le nombre de fois que le nombre de fois *()* pour l’étiquette donnée a été exécuté.
[**countReset()**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | Rétablit le nombre à zéro pour l’étiquette de compteur fournie.

Par exemple, en exécutant les lignes suivantes dans la console:

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 . . . entraînera:
> Mon compteur: 1

### Chronométrage de votre code

Instrumentez votre code avec des minuteurs étiquetés pour mesurer le temps nécessaire à l’exécution d’une opération donnée.

Commande | &nbsp;
:------------ | :-------------
[**Time ()**](https://developer.mozilla.org/docs/Web/API/Console/time) | Démarre un minuteur avec l’étiquette fournie.
[**timeEnd()**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | Termine le minuteur avec l’étiquette spécifiée et indique le temps écoulé (en millisecondes).
[**timeStamp ()**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | Indique l’heure actuelle du système (en millisecondes).

Par exemple, essayez d’exécuter les lignes suivantes dans la console:

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### Captures d’instantanés de tas

Prenez des instantanés du tas pour évaluer la consommation de mémoire de votre code en cours d’exécution et identifier les fuites de mémoire.

Commande | &nbsp;
:------------ | :-------------
**takeHeapSnapshot()** | Capture les détails du tas JavaScript actuel et de ses objets attribués.

Le [testeur de mémoire](../memory.md#toolbar) devtools doit être en cours d’exécution pour pouvoir utiliser des instantanés de tas. Chaque photo apparaît sous la forme d’une vignette dans la [*synthèse de capture instantanée*](../memory.md#snapshot-summary) du panneau [**mémoire**](../memory.md) pour une inspection plus poussée.

## Suivi de callstacks

Le fait de comprendre l’objet de l’appel de votre code, le code en cours d’exécution et la durée nécessaire à l’exécution pour l’analyse de la lenteur ou du comportement inattendu. Une trace de pile indique le chemin d’exécution que votre code a pris pour y accéder, à partir de la demande de suivi via le chemin. 

Commande | &nbsp;
:------------ | :-------------
[**trace ()**](https://developer.mozilla.org/docs/Web/API/Console/trace) | Génère une trace de la pile des appels d’exécution du script actuelle.

Par exemple, en exécutant le code suivant dans la console:

```javascript
function a(){
  c();
}
function b(){
  c();
}
function c(){
  console.trace()
}
function d(){
  b();
}

a();
d();
```

. . . va générer les traces de pile suivantes:
> Console. trace () sur c (code eval: 8:3) à a (code eval: 2:3) sur le code d’évaluation (code d’évaluation: 14:1)
> 
> Console. trace () sur c (code d’erreur: 8:3) à l’adresse b (code d’évaluation: 5:3) sur le code d’erreur (code d’erreur 11:3).

## Organisation de la sortie Journal

Pour effacer toute la sortie de la console précédente, utilisez *console. Clear ()* (ou `CTRL + L` ). Cela n’efface pas la pile de l’historique de commandes de votre console (vous pouvez toujours l’utiliser avec les touches de direction vers le haut et vers le bas).

Commande | &nbsp;
:------------ | :-------------
[**Clear ()**](https://developer.mozilla.org/docs/Web/API/Console/clear) | Efface toutes les sorties précédentes de la console.

Si votre code génère un grand nombre de messages de console, vous pouvez les organiser visuellement en blocs imbriqués à l’aide des commandes suivantes:

 Commande | &nbsp;
:------------ | :-------------
[**groupe ()**](https://developer.mozilla.org/docs/Web/API/Console/group) | Commence un nouveau niveau d’imbrication pour la sortie de console avec l’étiquette spécifiée (optional).
[**groupCollapsed()**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | Commence un nouveau niveau d’imbrication pour la sortie de console avec l’étiquette spécifiée (optional), mais le contrôle de regroupement est réduit par défaut et doit être développé (en cliquant sur le contrôle Arrow) pour afficher la sortie enfant.
[**groupEnd()**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | Termine le groupe imbriqué pour l’étiquette spécifiée.

Par exemple, essayez d’entrer les commandes suivantes dans la console:

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

. . . Développez ensuite les contrôles de groupe *1* et *1,1* pour voir comment les commentaires du journal sont imbriqués:

![Regroupement de messages dans la console](../media/console_api_group.png)

Il est parfois plus facile de visualiser un objet ou un tableau JavaScript sous forme tabulaire qu’une liste plate. Pour cela, vous pouvez utiliser la commande *console. table ()* :

Commande | &nbsp;
:------------ | :-------------
[**table ()**](https://developer.mozilla.org/docs/Web/API/Console/table) | Génère le tableau ou l’objet fourni dans la console sous forme tabulaire.

Par exemple, le tableau d’objets suivant:

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

. . . sera restitué en tant que table dans la console:

![Afficher un tableau d’objets en tant que table dans la console](../media/console_api_table.png)
