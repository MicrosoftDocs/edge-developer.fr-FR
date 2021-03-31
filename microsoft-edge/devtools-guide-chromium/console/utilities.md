---
description: Référence des commandes pratiques disponibles dans la console Microsoft Edge DevTools.
title: Référence de l’API des utilitaires de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398825"
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

L’API des utilitaires de console contient une collection de commandes pratiques pour effectuer des tâches courantes : sélection et inspection des éléments DOM, affichage de données dans un format lisible, arrêt et démarrage du profileur et surveillance des événements DOM.  

> [!WARNING]
> Les commandes suivantes fonctionnent uniquement dans la console Microsoft Edge DevTools.  Les commandes ne fonctionnent pas si elles sont exécutés à partir de vos scripts.  

Pour le reste des méthodes et méthodes, accédez à Référence de `console.log()` `console.error()` `console.*` [l’API console.][DevToolsConsoleApi]  

## <a name="recently-evaluated-expression"></a>Expression récemment évaluée  

```console
$_
```  

Renvoie la valeur de l’expression la plus récemment évaluée.  

Dans la figure suivante, une expression simple \( `2 + 2` \) est évaluée.  La `$_` propriété est ensuite évaluée, qui contient la même valeur.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ est la dernière expression évaluée" lightbox="../media/console-arithmatic.msft.png":::
   Figure 1 :  `$_` est l’expression la plus récemment évaluée  
:::image-end:::  

Dans la figure suivante, l’expression évaluée contient initialement un tableau de noms.  Évaluation pour trouver la longueur du tableau, la valeur stockée dans les modifications pour devenir la dernière `$_.length` `$_` expression évaluée, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ change lorsque de nouvelles commandes sont évaluées" lightbox="../media/console-array-length.msft.png":::
   Figure 2 :  `$_` modifications lors de l’évaluation de nouvelles commandes  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a>Élément récemment choisi ou objet JavaScript  

```console
$0
```  

Renvoie l’élément ou l’objet JavaScript sélectionné le plus récemment.  `$1` renvoie la deuxième dernière sélection, et ainsi de suite.  Les commandes , , et les commandes fonctionnent comme une référence historique aux cinq derniers éléments DOM inspectés dans l’outil Elements ou aux cinq derniers objets de tas `$0` `$1` `$2` `$3` `$4` JavaScript sélectionnés **** **** dans l’outil Mémoire.  

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
   :::column-end:::
:::row-end:::  

Dans la figure suivante, un `img` élément est sélectionné dans l’outil **Elements.**  Dans le caisse **de** la console, `$0` a été évalué et affiche le même élément.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="La valeur $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Figure 3 : Le `$0`  
:::image-end:::  

Dans la figure suivante, l’image montre un autre élément sélectionné dans la même page.  L’élément sélectionné fait désormais référence à l’élément nouvellement sélectionné, tandis qu’il renvoie `$0` `$1` l’élément précédemment sélectionné.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="La valeur $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Figure 4 : Le `$1`  
:::image-end:::  

## <a name="query-selector"></a>Sélecteur de requêtes  

```console
$(selector, [startNode])
```  

Renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.  Cette méthode est un alias de la [méthode document.querySelector().][MDNDocumentQuerySelector]  

Dans la figure suivante, une référence au premier `<img>` élément du document est renvoyée.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   Figure 5 : Le `$('img')`  
:::image-end:::  

Pointez sur le résultat renvoyé, ouvrez le menu contextuel \(clic droit\), puis **** choisissez **Révéler** dans le panneau Éléments pour le trouver dans le DOM ou faites défiler vers l’affichage pour l’afficher sur la page.  

Dans la figure suivante, une référence à l’élément actuellement sélectionné est renvoyée et la propriété src est affichée.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="Le $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Figure 6 : Le `$('img').src`  
:::image-end:::  

Cette méthode prend également en charge un deuxième paramètre, startNode, qui spécifie un « élément » ou un nœud à partir duquel rechercher des éléments.  La valeur par défaut du paramètre est `document` .  

Dans la figure suivante, le premier élément est trouvé après l’élément et l’affichage correct `img` `title--image` est `src` renvoyé.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Figure 7 : Le `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Si vous utilisez une bibliothèque telle que jQuery qui utilise , la fonctionnalité est écrasée et correspond à l’implémentation de `$` `$` cette bibliothèque.  

## <a name="query-selector-all"></a>Sélecteur de requêtes tous  

```console
$$(selector, [startNode])
```  

Renvoie un tableau d’éléments qui correspondent au sélecteur CSS spécifié.  Cette méthode équivaut à l’exécution de la [méthode document.querySelectorAll().][MDNDocumentQuerySelectorAll]  

Dans l’exemple de code et la figure suivants, utilisez pour créer un tableau de tous les éléments du document actuel et afficher la valeur de la propriété `$$()` `<img>` pour chaque `src` élément.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Utilisation de $$() pour sélectionner toutes les images du document et afficher les sources" lightbox="../media/console-element-selector-image-all.msft.png":::
   Figure 8 : Utilisation `$$()` pour sélectionner toutes les images du document et afficher les sources  
:::image-end:::  

Cette méthode prend également en charge un deuxième paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel rechercher des éléments.  La valeur par défaut du paramètre est `document` .  

Dans l’exemple de code et la figure suivants, une version modifiée de l’exemple de code et de la figure précédents utilise pour créer un tableau de tous les éléments qui apparaissent dans le document actuel après le nœud `$$()` `<img>` sélectionné.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Using $$() to select all images that appear after the specified <div> element in the document and display the sources" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Figure 9 : Utilisation pour sélectionner toutes les images qui apparaissent après l’élément spécifié dans le document et afficher `$$()` `<div>` les sources  
:::image-end:::  

> [!NOTE]
> Sélectionnez `Shift` + `Enter` dans la console pour démarrer une nouvelle ligne sans l’exécution du script.  

## <a name="xpath"></a>XPath  

```console
$x(path, [startNode])
```  

Renvoie un tableau d’éléments DOM qui correspondent à l’expression XPath spécifiée.  

Dans l’exemple de code et la figure suivants, tous les éléments `<p>` de la page sont renvoyés.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Utilisation d’un sélecteur XPath" lightbox="../media/console-array-xpath.msft.png":::
   Figure 10 : Utilisation d’un sélecteur XPath  
:::image-end:::  

Dans l’exemple de code et la figure suivants, tous les éléments `<p>` qui contiennent des `<a>` éléments sont renvoyés.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Utilisation d’un sélecteur XPath plus compliqué" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Figure 11 : Utilisation d’un sélecteur XPath plus compliqué  
:::image-end:::  

Comme pour les autres commandes de sélecteur, possède un deuxième paramètre facultatif, qui spécifie un élément ou un nœud à partir duquel rechercher `$x(path)` `startNode` des éléments.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Utilisation d’un sélecteur XPath avec startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Figure 12 : Utilisation d’un sélecteur XPath avec `startNode`  
:::image-end:::  

## <a name="clear"></a>clear  

```console
clear()
```  

Cette commande permet d’effacer la console de l’historique.  

```console
clear()
```  

## <a name="copy"></a>copy  

```console
copy(object)
```  

La `copy(object)` méthode copie une représentation sous la chaîne de l’objet spécifié dans le Presse-papiers.  

```console
copy($0)
```  

## <a name="debug"></a>déboguer  

```console
debug(method)
```  

>[!NOTE]
> Le [problème Chromium #1050237][MonorailIssue1050237] suivi d’un bogue avec la `debug()` fonction.  Si vous rencontrez le problème, essayez plutôt [d’utiliser des points d’arrêt.][DevtoolsJavascriptBreakpoints]  

Lorsque vous demandez la méthode spécifiée, le déboguer est appelé et s’interrompt à l’intérieur de la méthode sur l’outil **Sources,** ce qui vous permet d’aller pas à pas dans le code et de le déboguer.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Rupture à l’intérieur d’une méthode avec débogage()" lightbox="../media/console-debug-text.msft.png":::
   Figure 13 : Rupture à l’intérieur d’une méthode avec `debug()`  
:::image-end:::  

Permet d’arrêter la rupture de la méthode ou d’utiliser `undebug(method)` l’interface utilisateur pour désactiver tous les points d’arrêt.  

Pour plus d’informations sur les points d’arrêt, accédez à [Suspendre votre code avec des points d’arrêt.][DevToolsJavascriptBreakpoints]  

## <a name="dir"></a>dir  

```console
dir(object)
```  

Affiche une liste de style objet de toutes les propriétés de l’objet spécifié.  Cette méthode est un alias de la [méthode console.dir().][MDNConsoleDir]  

Évaluez `document.head` dans la console pour afficher le code HTML entre les `<head>` `</head>` balises et les balises.  Dans l’exemple de code et la figure suivants, une liste de style objet s’affiche après l’utilisation `console.dir()` dans la console.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Journalisation de document.head avec la méthode dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Figure 14 : Journalisation `document.head` avec `dir()` méthode  
:::image-end:::  

Pour plus d’informations, accédez [`console.dir()`][DevToolsConsoleApiConsoleDirObject] à l’entrée dans l’API console.  

## <a name="dirxml"></a>dirxml  

```console
dirxml(object)
```  

Imprime une représentation XML de l’objet spécifié, tel qu’il est affiché dans **l’outil Elements.**  Cette méthode est équivalente à la [méthode console.dirxml().][MDNConsoleDirxml]  

## <a name="inspect"></a>inspect  

```console
inspect(object/method)
```  

Ouvre et sélectionne l’élément ou l’objet spécifié dans le panneau approprié **** : l’outil **Elements** pour les éléments DOM ou l’outil Mémoire pour les objets tas JavaScript.  

Dans l’exemple de code et la figure `document.body` suivants, l’élément s’ouvre dans **l’outil Elements.**  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspection d’un élément avec inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Figure 15 : Inspection d’un élément avec `inspect()`  
:::image-end:::  

Lors de la transmission d’une méthode à inspecter, la méthode ouvre le document dans l’outil **Sources** que vous pouvez inspecter.  

## <a name="geteventlisteners"></a>getEventListeners  

```console
getEventListeners(object)
```  

Renvoie les écouteurs d’événements enregistrés sur l’objet spécifié.  La valeur de retour est un objet qui contient un tableau pour chaque type d’événement enregistré \(par exemple `click` ou `keydown` \).  Les membres de chaque tableau sont des objets qui décrivent l’écoute enregistrée pour chaque type.  Dans l’exemple de code suivant, tous les écouteurs d’événements enregistrés sur l’objet document sont répertoriés.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Sortie de l’utilisation de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Figure 16 : Résultat de l’utilisation `getEventListeners(document)`  
:::image-end:::  

Si plusieurs listener sont inscrits sur l’objet spécifié, le tableau contient un membre pour chaque listener.  Dans la figure suivante, deux écouteurs d’événements sont enregistrés sur l’élément de document pour `click` l’événement.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Plusieurs écouteurs" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Figure 17 : Plusieurs écouteurs  
:::image-end:::  

Vous pouvez développer chacun des objets suivants pour explorer les propriétés.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vue étendue de l’objet d’écoute" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Figure 18 : Vue étendue de l’objet d’écoute  
:::image-end:::  

## <a name="keys"></a>clés  

```console
keys(object)
```  

Renvoie un tableau contenant les noms des propriétés appartenant à l’objet spécifié.  Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .  

Par exemple, supposons que votre application a défini l’objet suivant.  

```console
var player1 =   
```  

Dans les exemples de code et la figure suivants, le résultat suppose qu’il a été défini dans l’espace de noms global \(par souci de simplicité\) avant la saisie et dans `player1` `keys(player1)` la `values(player1)` console.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Commandes keys() et values()" lightbox="../media/console-keys-values.msft.png":::
   Figure 19 : Commandes `keys()` `values()` et commandes  
:::image-end:::  

## <a name="monitor"></a>moniteur  

```console
monitor(method)
```  

Enregistre un message dans la console qui indique le nom de la méthode ainsi que les arguments transmis à la méthode lors de son appel.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Méthode monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   Figure 20 : `monitor()` Méthode  
:::image-end:::  

À utiliser `unmonitor(method)` pour cesser la surveillance.  

## <a name="monitorevents"></a>monitorEvents  

```console
monitorEvents(object[, events])
```  

Lorsqu’un des événements spécifiés se produit sur l’objet spécifié, l’objet d’événement est consigné dans la console.  Vous pouvez spécifier un seul événement à surveiller, un tableau d’événements ou l’un des types d’événements génériques qui sont mappés à une collection prédéfinie d’événements.  Examinez l’exemple de code et la figure suivants.  

L’exemple suivant surveille tous les événements de resize sur l’objet fenêtre.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Événements de resize de fenêtre d’analyse" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Figure 21 : Événements de resize de fenêtre de surveillance  
:::image-end:::  

L’exemple suivant définit un tableau pour surveiller les événements et les `resize` `scroll` événements sur l’objet fenêtre.  

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

Dans l’exemple de code suivant, le type d’événement correspondant aux événements sur un champ de texte d’entrée est actuellement sélectionné `key` `key` dans **l’outil Éléments.**  

```console
monitorEvents($0, "key");
```  

Dans la figure suivante, l’exemple de sortie après avoir tapé un caractère dans le champ de texte s’affiche.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Surveillance des événements clés" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Figure 22 : Surveillance des événements clés  
:::image-end:::  

## <a name="profile"></a>profile  

```console
profile([name])
```  

Démarre une session de profilage du processeur JavaScript avec un nom facultatif.  La [méthode profileEnd()](#profileend) termine le profil et affiche les résultats dans l’outil Mémoire. ****  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Exécutez la `profile()` méthode pour démarrer le profilage.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Exécutez [la méthode profileEnd()](#profileend) pour arrêter le profilage et afficher les résultats dans l’outil Mémoire. ****  

Les profils peuvent également être imbrmbrés.  Dans les exemples de code suivants et la figure, le résultat est le même quelle que soit la commande.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Plusieurs profils d’UC peuvent fonctionner en même temps et vous n’êtes pas obligé de fermer chacun d’eux dans l’ordre de création.  

## <a name="profileend"></a>profileEnd  

```console
profileEnd([name])
```  

Termine une session de profilage du processeur JavaScript et affiche les résultats dans **l’outil** Mémoire.  Vous devez être en cours d’exécution [de la méthode profile().](#profile)  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Exécutez [la méthode profile()](#profile) pour démarrer le profilage.  
1.  Exécutez la `profileEnd()` méthode pour arrêter le profilage et afficher les résultats dans l’outil Mémoire. ****  
    
    ```console
    profileEnd("My profile")
    ```  

Les profils peuvent également être imbrmbrés.  Dans l’exemple de code suivant et la figure, le résultat est le même quelle que soit la commande.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Le résultat s’affiche sous la mesure d’une capture instantanée de tas dans **l’outil Mémoire.**  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Profils groupés" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Figure 23 : Profils groupés  
:::image-end:::  

> [!NOTE]
> Plusieurs profils d’UC peuvent fonctionner en même temps et vous n’êtes pas obligé de fermer chacun d’eux dans l’ordre de création.  

## <a name="queryobjects"></a>queryObjects  

```console
queryObjects(Constructor)
```  

Renvoyer un tableau d’objets créés avec le constructeur spécifié.  L’étendue `queryObjects()` est le contexte d’runtime actuellement sélectionné dans la console.

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

```console
table(data[, columns])
```  

Enregistre les données d’objet avec une mise en forme de tableau basée sur l’objet de données avec des en-tête de colonne facultatifs.  Dans l’exemple de code et la figure suivants, une liste de noms utilisant un tableau dans la console s’affiche.  

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
   Figure 24 : Résultat de la `table()` méthode  
:::image-end:::  

## <a name="undebug"></a>undebug  

```console
undebug(method)
```  

Arrête le débogage de la méthode spécifiée de sorte que lorsque la méthode est appelée, le déboguer n’est plus appelé.  

```console
undebug(getData);
```  

## <a name="unmonitor"></a>unmonitor  

```console
unmonitor(method)
```  

Arrête la surveillance de la méthode spécifiée.  Cette méthode est utilisée de concert avec la [méthode monitor().](#monitor)  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a>unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Arrête la surveillance des événements pour l’objet et les événements spécifiés.  Par exemple, l’exemple suivant arrête l’analyse des événements sur l’objet fenêtre.  

```console
unmonitorEvents(window);
```  

Vous pouvez également arrêter de manière sélective la surveillance d’événements spécifiques sur un objet.  Par exemple, le code suivant démarre la surveillance de tous les événements sur l’élément actuellement sélectionné, puis arrête la surveillance des événements \(peut-être pour réduire le bruit dans la `mouse` `mousemove` sortie de la console\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a>values  

```console
values(object)
```  

Renvoie un tableau contenant les valeurs de toutes les propriétés appartenant à l’objet spécifié.  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence de l’API de console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir - Référence de l’API console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Accélérer le runtime JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problème 1050237 : débogage(fonction) ne fonctionne pas | Monorail"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/utilities) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
