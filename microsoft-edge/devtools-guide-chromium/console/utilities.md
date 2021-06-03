---
description: Référence des commandes pratiques disponibles dans la console Microsoft Edge DevTools.
title: Référence de l’API des utilitaires de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 436f2807c5fab1723ca6cc93fddc68d9ecf12db7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564531"
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
# <a name="console-utilities-api-reference"></a>Référence de l’API des utilitaires de console  

L’API Des utilitaires de console contient une collection de commandes pratiques pour effectuer les tâches courantes suivantes.  

*   Choisir et inspecter les éléments DOM  
*   Afficher les données dans un format lisible  
*   Arrêter et démarrer le profileur  
*   Surveiller les événements DOM  
    
> [!WARNING]
> Les commandes suivantes fonctionnent uniquement dans la Microsoft Edge **console**DevTools.  Les commandes ne fonctionnent pas si elles sont exécutés à partir de vos scripts.  

Pour plus d’informations sur les méthodes et les autres méthodes, accédez à Référence de `console.log()` `console.error()` `console.*` [l’API console.][DevToolsConsoleApi]  

## <a name="recently-evaluated-expression"></a>Expression récemment évaluée  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
$_
```  

Cette commande renvoie la valeur de la dernière expression évaluée.  

### <a name="console-example"></a>Exemple de console  

Dans la figure suivante, une expression simple \( `2 + 2` \) est évaluée.  La `$_` propriété est ensuite évaluée, qui contient la même valeur.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ est la dernière expression évaluée" lightbox="../media/console-arithmatic.msft.png":::
   `$_` est la dernière expression évaluée  
:::image-end:::  

Dans la figure suivante, l’expression évaluée contient initialement un tableau de noms.  L’évaluation de la longueur du tableau, la valeur stockée dans devient la `$_.length` `$_` dernière expression évaluée, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ change lorsque de nouvelles commandes sont évaluées" lightbox="../media/console-array-length.msft.png":::
   `$_` modifications lors de l’évaluation de nouvelles commandes ;  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a>Élément ou objet JavaScript récemment choisi  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
$0
```  

Cette commande renvoie l’élément ou l’objet JavaScript le plus récemment choisi.  `$1` renvoie le deuxième dernier choix, et ainsi de suite.  Les commandes , , et les commandes fonctionnent comme une référence historique aux cinq derniers éléments `$0` `$1` `$2` `$3` `$4` DOM inspectés **** **** dans l’outil Elements ou aux cinq derniers objets de tas JavaScript choisis dans l’outil Mémoire.  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a>Exemple de console  

Dans la figure suivante, un `img` élément est choisi dans l’outil **Elements.**  Dans le caisse **de** la console, `$0` a été évalué et affiche le même élément.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="La valeur $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   La liste  `$0`  
:::image-end:::  

Dans la figure suivante, l’image affiche un autre élément choisi dans la même page web.  L’élément qui vient d’être choisi fait référence au nouvel élément, alors `$0` qu’il renvoie `$1` l’élément précédemment choisi.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="La valeur $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   La liste  `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a>Sélecteur de requête  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
$(selector, [startNode])
```  

Cette commande renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.  Cette méthode est un alias de la [méthode document.querySelector().][MdnDocsWebApiDocumentQueryselector]  

### <a name="console-example"></a>Exemple de console  

Dans la figure suivante, une référence au premier `<img>` élément de la page web est renvoyée.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   La liste  `$('img')`  
:::image-end:::  

Pour rechercher le premier élément dans le DOM ou pour le rechercher et l’afficher sur la page web, complétez les actions suivantes.  

1.  Pointez sur le résultat renvoyé.  
1.  Ouvrez le menu contextuel \(cliquez avec le bouton droit\).  
1.  Choisissez **Révéler dans le panneau Éléments.**  

Dans la figure suivante, une référence à l’élément actuellement choisi est renvoyée et la `src` propriété est affichée.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="Le $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   La liste  `$('img').src`  
:::image-end:::  

Cette méthode prend également en charge un deuxième paramètre, qui spécifie un élément ou un nœud à partir duquel `startNode` rechercher des éléments.  La valeur par défaut du paramètre est `document` .  

Dans la figure suivante, le premier élément une fois l’élément trouvé et la `img` `title--image` propriété de `src` `img` l’élément est renvoyée.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   La liste  `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Si vous utilisez une bibliothèque telle que jQuery qui utilise , la fonctionnalité est écrasée et correspond à l’implémentation de `$` `$` cette bibliothèque.  

---  

## <a name="query-selector-all"></a>Sélecteur de requête tout  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
$$(selector, [startNode])
```  

Cette commande renvoie un tableau d’éléments qui correspondent au sélecteur CSS spécifié.  Cette méthode équivaut à l’exécution de la [méthode document.querySelectorAll().][MdnDocsWebApiDocumentQueryselectorall]  

### <a name="console-example"></a>Exemple de console  

Dans l’exemple de code et la figure suivants, utilisez cette procédure pour créer un tableau de tous les éléments de la page web actuelle et afficher la valeur de la propriété `$$()` `<img>` pour chaque `src` élément.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Utilisation de $$() pour choisir toutes les images de la page web et afficher les sources" lightbox="../media/console-element-selector-image-all.msft.png":::
   Utilisation `$$()` pour choisir toutes les images de la page web et afficher les sources  
:::image-end:::  

Cette méthode prend également en charge un deuxième paramètre, qui spécifie un élément ou un nœud à partir duquel `startNode` rechercher des éléments.  La valeur par défaut du paramètre est `document` .  

Dans l’exemple de code et la figure suivants, une version modifiée de l’exemple de code et de la figure précédents utilise pour créer un tableau de tous les éléments qui apparaissent dans la page web actuelle après le nœud `$$()` `<img>` choisi.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Using $$() to choose all images that appear after the specified <div> element in the webpage and display the sources" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Utilisation `$$()` pour choisir toutes les images qui apparaissent après l’élément spécifié dans la page web et afficher les `<div>` sources  
:::image-end:::  

> [!NOTE]
> Sélectionnez `Shift` + `Enter` dans la **console** pour démarrer une nouvelle ligne sans l’exécution du script.  

---  

## <a name="xpath"></a>XPath  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
$x(path, [startNode])
```  

Cette commande renvoie un tableau d’éléments DOM qui correspondent à l’expression XPath spécifiée.  

### <a name="console-example"></a>Exemple de console  

Dans l’exemple de code et la figure suivants, tous les éléments `<p>` de la page web sont renvoyés.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Utilisation d’un sélecteur XPath" lightbox="../media/console-array-xpath.msft.png":::
   Utilisation d’un sélecteur XPath  
:::image-end:::  

Dans l’exemple de code et la figure suivants, tous les éléments `<p>` qui contiennent des `<a>` éléments sont renvoyés.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Utilisation d’un sélecteur XPath plus compliqué" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Utilisation d’un sélecteur XPath plus compliqué  
:::image-end:::  

Comme pour les autres commandes de sélecteur, possède un deuxième paramètre facultatif, qui spécifie un élément ou un nœud à partir duquel rechercher `$x(path)` `startNode` des éléments.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Utilisation d’un sélecteur XPath avec startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Utilisation d’un sélecteur XPath avec `startNode`  
:::image-end:::  

---  

## <a name="clear"></a>clear  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
clear()
```  

Cette commnad permet d’effacer la console de l’historique.  

### <a name="console-example"></a>Exemple de console  

```console
clear()
```  

## <a name="copy"></a>copy  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
copy(object)
```  

Cette méthode copie une représentation sous la chaîne de l’objet spécifié dans le Presse-papiers.  

### <a name="console-example"></a>Exemple de console  

```console
copy($0)
```  

---  

## <a name="debug"></a>déboguer  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
debug(method)
```  

>[!NOTE]
> Le [Chromium problème #1050237][CR1050237] suivi d’un bogue avec la `debug()` fonction.  Si vous rencontrez le problème, essayez plutôt d’utiliser des [points d’arrêt.][DevtoolsJavascriptBreakpoints]  

Lorsque vous demandez la méthode spécifiée, le déboqueur appelle et s’interrompt à l’intérieur de la méthode sur **l’outil Sources.**  Il vous permet d’aller pas à pas et de déboguer le code.  

### <a name="console-example"></a>Exemple de console  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Rupture à l’intérieur d’une méthode avec débogage()" lightbox="../media/console-debug-text.msft.png":::
   Rupture à l’intérieur d’une méthode avec `debug()`  
:::image-end:::  

Permet `undebug(method)` d’arrêter de rompre la méthode ou d’utiliser l’interface utilisateur pour désactiver tous les points d’arrêt.  

Pour plus d’informations sur les points d’arrêt, accédez à Comment suspendre votre code avec des points [d’arrêt Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].  

---  

## <a name="dir"></a>dir  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
dir(object)
```  

Cette commande affiche une liste de toutes les propriétés de l’objet spécifié.  Cette méthode est un alias de la [méthode console.dir().][MdnDocsWebApiConsoleDir]  

Évaluez `document.head` dans la console **pour** afficher le code HTML entre les `<head>` `</head>` balises et les balises.  

### <a name="console-example"></a>Exemple de console  

Dans l’exemple de code et la figure suivants, une liste de style objet s’affiche après l’utilisation `console.dir()` dans la **console**.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Journalisation de document.head avec la méthode dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Journalisation `document.head` avec `dir()` la méthode  
:::image-end:::  

Pour plus d’informations, [accédez à console.dir()][DevToolsConsoleApiConsoleDirObject] dans l’API console.  

---  

## <a name="dirxml"></a>dirxml  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
dirxml(object)
```  

Cette commande imprime une représentation XML de l’objet spécifié, tel qu’il est affiché dans **l’outil Elements.**  Cette méthode est équivalente à la [méthode console.dirxml().][MdnDocsWebApiConsoleDirxml]  

---  

## <a name="inspect"></a>inspect  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
inspect(object/method)
```  

Cette commande s’ouvre et choisit l’élément ou l’objet spécifié dans le **** panneau approprié : l’outil **Elements** pour les éléments DOM ou l’outil Mémoire pour les objets de tas JavaScript.  

### <a name="console-example"></a>Exemple de console  

Dans l’exemple de code et la figure `document.body` suivants, l’élément s’ouvre dans **l’outil Elements.**  

### <a name="console-example"></a>Exemple de console  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspection d’un élément avec inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Inspection d’un élément avec `inspect()`  
:::image-end:::  

Lors de la transmission d’une méthode à inspecter, la méthode ouvre la page web dans l’outil **Sources** que vous pouvez inspecter.  

---  

## <a name="geteventlisteners"></a>getEventListeners  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
getEventListeners(object)
```  

Cette commande renvoie les écouteurs d’événements enregistrés sur l’objet spécifié.  La valeur de retour est un objet qui contient un tableau pour chaque type d’événement inscrit \(par exemple `click` ou `keydown` \).  Les membres de chaque tableau sont des objets qui décrivent l’écoute enregistrée pour chaque type.  

### <a name="console-example"></a>Exemple de console  

Dans l’extrait de code et la figure suivantes, tous les écouteurs d’événements enregistrés sur `document` l’objet sont répertoriés.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Sortie de l’utilisation de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Résultat de l’utilisation `getEventListeners(document)`  
:::image-end:::  

Si plusieurs listener sont inscrits sur l’objet spécifié, le tableau contient un membre pour chaque listener.  Dans la figure suivante, deux écouteurs d’événements sont enregistrés sur `document` l’élément pour `click` l’événement.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Plusieurs écouteurs" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Plusieurs écouteurs  
:::image-end:::  

Vous pouvez développer chacun des objets suivants pour explorer les propriétés.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vue étendue de l’objet d’écoute" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Vue étendue de l’objet d’écoute  
:::image-end:::  

---  

## <a name="keys"></a>clés  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
keys(object)
```  

Cette commande renvoie un tableau contenant les noms des propriétés appartenant à l’objet spécifié.  Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .  

### <a name="console-example"></a>Exemple de console  

Par exemple, supposons que votre application a défini l’objet suivant.  

```console
var player1 = {"name": "Ted", "level": 42}
```  

Dans les exemples de code et la figure suivants, le résultat suppose qu’il a été défini dans l’espace de noms global \(par souci de simplicité\) avant que vous tapiez et dans `player1` `keys(player1)` la `values(player1)` console.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Commandes keys() et values()" lightbox="../media/console-keys-values.msft.png":::
   Commandes `keys()` Et `values()`  
:::image-end:::  

---  

## <a name="monitor"></a>moniteur  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
monitor(method)
```  

Cette commande enregistre un message dans la console qui indique le nom de la méthode ainsi que les arguments transmis à la méthode dans le cadre d’une demande.  

### <a name="console-example"></a>Exemple de console  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Méthode monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   Méthode `monitor()`  
:::image-end:::  

À utiliser `unmonitor(method)` pour mettre fin à l’analyse.  

---  

## <a name="monitorevents"></a>monitorEvents  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
monitorEvents(object[, events])
```  

Lorsqu’un des événements spécifiés se produit sur l’objet spécifié, l’objet d’événement est consigné dans la console.  Vous pouvez spécifier un seul événement à surveiller, un tableau d’événements ou l’un des types d’événements génériques qui sont mappés à une collection prédéfinie d’événements.  

### <a name="console-example"></a>Exemple de console  

Examinez l’exemple de code et la figure suivants.  

L’exemple suivant surveille tous les événements de resize sur l’objet fenêtre.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Événements de resize de fenêtre d’analyse" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Événements de resize de fenêtre d’analyse  
:::image-end:::  

L’extrait de code suivant définit un tableau pour surveiller les événements et les événements `resize` `scroll` sur l’objet fenêtre.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Vous pouvez également spécifier l’un des types d’événements disponibles, les chaînes qui m’indiquent des jeux d’événements prédéfinés.  Le tableau suivant affiche les types d’événements disponibles et les mappages d’événements associés.  

| Type d’événement | Événements mappés correspondants |  
|:--- |:--- |  
| `mouse` | « click », « dblclick », « mousedown », « mousemove », « mouseout », « mouseover », « mouseup », « mousewheel » |  
| `key` | «keydown», «keypress», «keyup», «textInput» |  
| `touch` | « touchcancel », « touchend », « touchmove », « touchstart » |  
| `control` | «flou», «modifier», «focus», «réinitialiser», «resize», «scroll», «select», «submit», «zoom» |  

Dans l’exemple de code suivant, le type d’événement correspondant aux événements sur un champ de texte d’entrée est actuellement `key` `key` choisi dans **l’outil Éléments.**  

```console
monitorEvents($0, "key");
```  

Dans la figure suivante, l’exemple de sortie après la saisie d’un caractère dans le champ de texte s’affiche.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Surveillance des événements clés" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Surveillance des événements clés  
:::image-end:::  

---  

## <a name="profile"></a>profile  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
profile([name])
```  

Cette commande démarre une session de profilage de l’UC JavaScript avec un nom facultatif.  La [méthode profileEnd()](#profileend) termine le profil et affiche les résultats dans l’outil Mémoire. ****  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Exemple de console  

1.  Exécutez la `profile()` méthode pour démarrer le profilage.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Exécutez [la méthode profileEnd()](#profileend) pour arrêter le profilage et afficher les résultats dans l’outil Mémoire. ****  

Les profils peuvent également être imbrmbrés.  Dans la figure et les exemples de code suivants, le résultat est le même quel que soit l’ordre.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Plusieurs profils d’UC peuvent fonctionner en même temps et vous n’êtes pas obligé de fermer chacun d’eux dans l’ordre de création.  

---  

## <a name="profileend"></a>profileEnd  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
profileEnd([name])
```  

Cette commande termine une session de profilage de l’UC JavaScript et affiche les résultats dans **l’outil** Mémoire.  Vous devez être en cours d’exécution [de la méthode profile().](#profile)  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Exemple de console  

1.  Exécutez [la méthode profile()](#profile) pour démarrer le profilage.  
1.  Exécutez la `profileEnd()` méthode pour arrêter le profilage et afficher les résultats dans l’outil Mémoire. ****  
    
    ```console
    profileEnd("My profile")
    ```  

Les profils peuvent également être imbrmbrés.  Dans l’exemple de code et la figure suivants, le résultat est le même quelle que soit la commande.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Le résultat s’affiche sous la mesure d’une capture instantanée de tas dans **l’outil Mémoire.**  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Profils groupés" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Profils groupés  
:::image-end:::  

> [!NOTE]
> Plusieurs profils d’UC peuvent fonctionner en même temps et vous n’êtes pas obligé de fermer chacun d’eux dans l’ordre de création.  

---  

## <a name="queryobjects"></a>queryObjects  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
queryObjects(Constructor)
```  

Cette commande renvoie un tableau d’objets créés avec le constructeur spécifié.  L’étendue `queryObjects()` est le contexte d’runtime actuellement choisi dans la **console.**  

### <a name="console-example"></a>Exemple de console  

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Renvoie tout `Promises` .  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      Renvoie tous les éléments HTML.  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      Renvoie tous les objets qui ont été ins instantiés à l’aide `new functionName()` de .  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>table  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
table(data[, columns])
```  

Cette commande enregistre les données d’objet avec une mise en forme de tableau basée sur l’objet de données avec des en-tête de colonne facultatifs.  

### <a name="console-example"></a>Exemple de console  

Dans l’exemple de code et la figure suivants, une liste de noms utilisant un tableau dans la console s’affiche.  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Résultat de la méthode table()" lightbox="../media/console-table-display.msft.png":::
   Résultat de la `table()` méthode  
:::image-end:::  

---  

## <a name="undebug"></a>undebug  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
undebug(method)
```  

Cette commande arrête le débogage de la méthode spécifiée. Ainsi, lorsque la méthode est demandée, le débogger n’est plus appelé.  

### <a name="console-example"></a>Exemple de console  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a>unmonitor  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
unmonitor(method)
```  

Cette commande arrête la surveillance de la méthode spécifiée.  Cette méthode est utilisée de concert avec la [méthode monitor().](#monitor)  

### <a name="console-example"></a>Exemple de console  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a>unmonitorEvents  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
unmonitorEvents(object[, events])
```  

Cette commande arrête la surveillance des événements pour l’objet et les événements spécifiés.  

### <a name="console-example"></a>Exemple de console  

Par exemple, l’extrait de code suivant arrête toute surveillance des événements sur l’objet fenêtre.  

```console
unmonitorEvents(window);
```  

Vous pouvez également arrêter de manière sélective la surveillance d’événements spécifiques sur un objet.  Par exemple, le code suivant démarre la surveillance de tous les événements sur l’élément actuellement choisi, puis arrête la surveillance des événements \(peut-être pour réduire le bruit dans la `mouse` `mousemove` sortie de la console\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a>values  

### <a name="console-syntax"></a>Syntaxe de la console  

```console
values(object)
```  

Cette commande renvoie un tableau contenant les valeurs de toutes les propriétés appartenant à l’objet spécifié.  

### <a name="console-example"></a>Exemple de console  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir - Console API reference | Documents Microsoft"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Comment suspendre votre code avec des points d’arrêt Microsoft Edge devTools | Documents Microsoft"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Accélérer le runtime JavaScript | Documents Microsoft"  

[CR1050237]: https://crbug.com/1050237 "Problème 1050237 : débogage(fonction) ne fonctionne pas | Chromium bogues"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/utilities) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
