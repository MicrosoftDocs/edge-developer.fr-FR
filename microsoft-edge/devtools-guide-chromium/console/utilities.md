---
description: Référence aux commandes de commodité disponibles dans la console Microsoft Edge DevTools.
title: XXXXXX xxxxxxx xxx xxxxxxxxx
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2882d980e6da45072cab4b028ceb1838a9078064
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993106"
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

# XXXXXX xxxxxxx xxx xxxxxxxxx  

L’API des utilitaires de la console contient une collection de commandes pratiques permettant d’effectuer des tâches courantes: la sélection et l’examen des éléments DOM, l’affichage des données dans un format lisible, l’arrêt et le démarrage du profileur, et la surveillance des événements DOM.  

> [!WARNING]
> Les commandes suivantes fonctionnent uniquement dans la console Microsoft Edge DevTools.  Les commandes ne fonctionnent pas si celles-ci sont exécutées à partir de vos scripts.  

Vous recherchez `console.log()` , `console.error()` et le reste des `console.*` méthodes?  Voir [référence][DevToolsConsoleApi]sur l’API de la console.  

## Expression récemment évaluée  

```console
$_
```  

Renvoie la valeur de l’expression évaluée le plus récemment.  

Dans l’illustration suivante, une expression simple \ ( `2 + 2` \) est évaluée.  La `$_` propriété est alors évaluée, qui contient la même valeur.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ est l’expression la plus récemment évaluée." lightbox="../media/console-arithmatic.msft.png":::
   Figure 1:  `$_` l’expression la plus récente est évaluée  
:::image-end:::  

Dans l’illustration suivante, l’expression évaluée contient initialement un tableau de noms.  Si vous évaluez la `$_.length` longueur de l’argument matrice, la valeur stockée dans `$_` les modifications devient la dernière expression évaluée `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ change lorsque de nouvelles commandes sont évaluées" lightbox="../media/console-array-length.msft.png":::
   Figure 2:  `$_` modifications lors de l’évaluation de nouvelles commandes  
:::image-end:::  

## Élément récemment sélectionné ou objet JavaScript  

```console
$0
```  

Retourne l’élément le plus récemment sélectionné ou l’objet JavaScript.  `$1` renvoie le second dernier sélectionné, et ainsi de suite.  Les `$0` commandes,,, `$1` `$2` `$3` et `$4` permettent de faire une référence historique aux cinq derniers éléments DOM examinés dans le panneau **éléments** ou les cinq derniers objets du tas JavaScript sélectionnés dans le panneau **mémoire** .  

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

Dans l’illustration suivante, un `img` élément est sélectionné dans le panneau **éléments** .  Le tiroir **Console** de la console `$0` a été évalué et affiche le même élément.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="$0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Figure 3: le `$0`  
:::image-end:::  

Dans l’illustration suivante, l’image montre un élément différent sélectionné dans la même page.  L' `$0` élément désormais fait référence à l’élément que vous venez de sélectionner, tandis qu’il `$1` renvoie le précédent.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="$1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Figure 4: le `$1`  
:::image-end:::  

## Sélecteur de requête  

```console
$(selector, [startNode])
```  

Renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.  Cette méthode est un alias de la méthode [document. querySelector ()][MDNDocumentQuerySelector] .  

Dans l’illustration suivante, une référence au premier `<img>` élément du document est renvoyée.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ ('Img')" lightbox="../media/console-element-selector-image.msft.png":::
   Figure 5: le `$('img')`  
:::image-end:::  

Positionnez le pointeur sur le résultat retourné, ouvrez le menu contextuel (cliquez avec le bouton droit sur \), puis sélectionnez l’option **révéler dans le panneau d’éléments** pour le Rechercher dans le DOM ou **faire défiler pour** afficher la page.  

Dans l’illustration suivante, une référence à l’élément actuellement sélectionné est renvoyée et la propriété SRC est affichée.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$ ('Img'). SRC" lightbox="../media/console-element-selector-image-source.msft.png":::
   Figure 6: le `$('img').src`  
:::image-end:::  

Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.  La valeur par défaut du paramètre est `document` .  

Dans l’illustration suivante, le premier `img` élément est trouvé après `title--image` et affiche le `src` résultat correct.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ ('Img', document. querySelector ('title--image')). SRC" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Figure 7: le `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Si vous utilisez une bibliothèque telle que jQuery qui utilise `$` , la fonctionnalité est écrasée et `$` correspond à l’implémentation de cette bibliothèque.  

## Sélecteur de requête  

```console
$$(selector, [startNode])
```  

Retourne un tableau d’éléments qui correspondent au sélecteur CSS spécifié.  Cette méthode équivaut à appeler la méthode [document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .  

Dans l’exemple de code et la figure ci-dessous, utilisez `$$()` pour créer un tableau de tous les `<img>` éléments du document actuel et afficher la valeur de la `src` propriété de chaque élément.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Utilisation de $ $ () pour sélectionner toutes les images du document et afficher les sources" lightbox="../media/console-element-selector-image-all.msft.png":::
   Figure 8: utilisation `$$()` pour sélectionner toutes les images du document et afficher les sources  
:::image-end:::  

Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.  La valeur par défaut du paramètre est `document` .  

Dans l’exemple de code et la figure ci-dessous, une version modifiée de l’exemple de code précédent et de la figure utilise `$$()` pour créer un tableau de tous les `<img>` éléments qui s’affichent dans le document actif suite au nœud sélectionné.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Utilisation de $ $ () pour sélectionner toutes les images qui s’affichent après l’élément <div> spécifié dans le document et afficher les sources" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Figure 9: utilisation `$$()` pour sélectionner toutes les images qui apparaissent après l' `<div>` élément spécifié dans le document et afficher les sources  
:::image-end:::  

> [!NOTE]
> Appuyez sur `Shift` + `Enter` la console pour commencer une nouvelle ligne sans exécuter le script.  

## Suivante  

```console
$x(path, [startNode])
```  

Renvoie un tableau d’éléments DOM qui correspondent à l’expression XPath spécifiée.  

Dans l’exemple de code et la figure ci-dessous, tous les `<p>` éléments de la page sont renvoyés.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Utilisation d’un sélecteur XPath" lightbox="../media/console-array-xpath.msft.png":::
   Figure 10: utilisation d’un sélecteur XPath  
:::image-end:::  

Dans l’exemple de code et la figure ci-dessous, tous les `<p>` éléments qui contiennent des `<a>` éléments sont renvoyés.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Utilisation d’un sélecteur XPath plus complexe" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Figure 11: utilisation d’un sélecteur XPath plus complexe  
:::image-end:::  

À l’instar des autres commandes de sélecteur, `$x(path)` possède un deuxième paramètre facultatif, `startNode` qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Utilisation d’un sélecteur XPath avec startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Figure 12: utilisation d’un sélecteur XPath avec `startNode`  
:::image-end:::  

## supprime  

```console
clear()
```  

Efface la console de l’historique.  

```console
clear()
```  

## copy  

```console
copy(object)
```  

La `copy(object)` méthode copie une représentation de chaîne de l’objet spécifié dans le presse-papiers.  

```console
copy($0)
```  

## déboguer  

```console
debug(method)
```  

>[!NOTE]
> Le [#1050237 problème de chrome][MonorailIssue1050237] effectue le suivi d’un bogue avec la `debug()` fonction.  Si vous rencontrez un problème, essayez plutôt d' [utiliser des points d’arrêt][DevtoolsJavascriptBreakpoints] .  

Lorsque vous demandez la méthode spécifiée, le débogueur est appelé et s’interrompt à l’intérieur de la méthode sur le panneau **sources** pour vous permettre de parcourir le code et de le déboguer.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Casser au sein d’une méthode à l’aide du débogage ()" lightbox="../media/console-debug-text.msft.png":::
   Figure 13: rupture dans une méthode avec `debug()`  
:::image-end:::  

Utilisez `undebug(method)` cette commande pour arrêter l’interruption de la méthode, ou utilisez l’interface utilisateur pour désactiver tous les points d’arrêt.  

Pour plus d’informations sur les points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Affiche une liste de styles d’objet de toutes les propriétés de l’objet spécifié.  Cette méthode est un alias de la méthode [console. dir ()][MDNConsoleDir] .  

Évaluez `document.head` la console pour afficher le code HTML entre `<head>` les `</head>` balises et.  Dans l’exemple de code et la figure ci-dessous, une liste à l’aide de l’objet s’affiche après utilisation `console.dir()` de la console.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Journalisation du document. Head avec la méthode dir ()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Figure 14: journalisation `document.head` avec la `dir()` méthode  
:::image-end:::  

Pour plus d’informations, consultez l' [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrée dans l’API de la console.  

## dirxml  

```console
dirxml(object)
```  

Imprime une représentation XML de l’objet spécifié, comme indiqué dans l’onglet **éléments** .  Cette méthode est équivalente à la méthode [console. DirXML ()][MDNConsoleDirxml] .  

## recherche  

```console
inspect(object/method)
```  

Ouvre et sélectionne l’élément ou l’objet spécifié dans le panneau approprié: soit le panneau des **éléments** pour les éléments DOM, soit le panneau **mémoire** pour les objets du tas JavaScript.  

Dans l’exemple de code et la figure ci-après, l' `document.body` élément s’ouvre dans le panneau **éléments** .  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspecter un élément avec Inspect ()" lightbox="../media/console-inspect-document-body.msft.png":::
   Figure 15: examen d’un élément avec `inspect()`  
:::image-end:::  

Lorsque vous passez une méthode à inspecter, la méthode ouvre le document dans le panneau **sources** que vous pouvez inspecter.  

## getEventListeners  

```console
getEventListeners(object)
```  

Renvoie les écouteurs d’événements enregistrés sur l’objet spécifié.  La valeur de retour est un objet qui contient un tableau pour chaque type d’événement inscrit \ (tel que `click` ou `keydown` \).  Les membres de chaque tableau sont des objets qui décrivent l’écouteur inscrit pour chaque type.  Dans l’exemple de code suivant, tous les détecteurs d’événements enregistrés sur l’objet document apparaissent.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Sortie de l’utilisation de getEventListeners (document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Figure 16: résultat de l’utilisation de `getEventListeners(document)`  
:::image-end:::  

S’il existe plusieurs écouteurs enregistrés sur l’objet spécifié, le tableau contient un membre pour chaque écouteur.  Dans l’illustration suivante, deux écouteurs d’événements sont inscrits dans l’élément document pour l' `click` événement.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Écouteurs multiples" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Figure 17: écouteurs multiples  
:::image-end:::  

Vous pouvez également développer chacun des objets suivants pour découvrir les propriétés.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Affichage développé de l’objet Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Figure 18: vue développée de l’objet Listener  
:::image-end:::  

## clés  

```console
keys(object)
```  

Retourne une matrice contenant les noms des propriétés appartenant à l’objet spécifié.  Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .  

Par exemple, supposons que votre application définisse l’objet suivant.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

Dans les exemples de code et figures suivants, le résultat suppose qu’il `player1` a été défini dans l’espace de noms global \ (pour la simplicité \) avant de taper `keys(player1)` et `values(player1)` dans la console.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Commandes Keys () et values ()" lightbox="../media/console-keys-values.msft.png":::
   Figure 19: `keys()` commandes et `values()`  
:::image-end:::  

## moniteur  

```console
monitor(method)
```  

Consigne un message dans la console indiquant le nom de la méthode, ainsi que les arguments transmis à la méthode lors de son appel.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Méthode Monitor ()" lightbox="../media/console-function-monitor-sum.msft.png":::
   Figure 20: `monitor()` méthode  
:::image-end:::  

Utiliser `unmonitor(method)` pour cesser de surveiller.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Quand l’un des événements spécifiés se produit sur l’objet spécifié, l’objet Event est enregistré dans la console.  Vous pouvez spécifier un événement unique à surveiller, un tableau d’événements ou l’un des types d’événements génériques mappés à une collection prédéfinie d’événements.  Consultez l’exemple de code et la figure suivants.  

Le code suivant analyse tous les événements de redimensionnement sur l’objet Window.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Surveiller les événements de redimensionnement d’une fenêtre" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Figure 21: surveiller les événements de redimensionnement d’une fenêtre  
:::image-end:::  

Le code suivant définit un tableau pour contrôler les deux `resize` et les `scroll` événements sur l’objet Window.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Vous pouvez également spécifier l’un des types d’événements disponibles, qui mappent à des ensembles prédéfinis d’événements.  Le tableau ci-dessous répertorie les types d’événements disponibles et les mappages d’événements associés.  

| Type d’événement | Événements mappés correspondants |  
|:--- |:--- |  
| `mouse` | "Click", "DblClick", "MouseDown", "MouseMove", "mouseout", "MouseOver", "MouseUp", "MouseWheel" |  
| `key` | "KeyDown", "KeyPress", "KeyUp", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "Blur", "changement", "Focus", "Réinitialiser", "Redimensionner", "défilement", "sélectionner", "soumission", "zoom" |  

Dans l’exemple de code suivant, le `key` type d’événement correspondant aux `key` événements sur un champ de saisie de texte est actuellement sélectionné dans le panneau **éléments** .  

```console
monitorEvents($0, "key");
```  

Dans l’illustration suivante, la sortie de l’exemple après saisie d’un caractère dans le champ de texte s’affiche.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Surveiller les événements de touche" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Figure 22: surveiller les événements de touche  
:::image-end:::  

## profile  

```console
profile([name])
```  

Démarre une session de profil de l’UC JavaScript avec un nom facultatif.  La méthode [profileEnd ()](#profileend) termine le profil et affiche les résultats dans le panneau **mémoire** .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Exécutez la `profile()` méthode pour démarrer le profilage.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Exécutez la méthode [profileEnd ()](#profileend) pour arrêter le profilage et afficher les résultats dans le panneau **mémoire** .  

Les profils risquent également d’être imbriqués.  Dans les exemples de code suivants et figure le résultat est le même quel que soit l’ordre.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Les profils d’UC multiples peuvent fonctionner en même temps et vous n’avez pas besoin de les clôturer dans l’ordre de création.  

## profileEnd  

```console
profileEnd([name])
```  

Effectue une session de profilage de l’UC JavaScript et affiche les résultats dans le panneau **mémoire** .  Vous devez exécuter la méthode [Profile ()](#profile) .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Exécutez la méthode [Profile ()](#profile) pour démarrer le profilage.  
1.  Exécutez la `profileEnd()` méthode pour arrêter le profilage et afficher les résultats dans le panneau **mémoire** .  
    
    ```console
    profileEnd("My profile")
    ```  

Les profils risquent également d’être imbriqués.  Dans l’exemple de code suivant et la figure, le résultat est le même quel que soit l’ordre.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Le résultat s’affiche sous la forme d’un instantané de tas dans le panneau **mémoire** .  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Profils groupés" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Figure 23: profils groupés  
:::image-end:::  

> [!NOTE]
> Les profils d’UC multiples peuvent fonctionner en même temps et vous n’avez pas besoin de les clôturer dans l’ordre de création.  

## queryObjects  

```console
queryObjects(Constructor)
```  

Retourne un tableau d’objets créé avec le constructeur spécifié.  L’étendue de `queryObjects()` correspond au contexte d’exécution actuellement sélectionné dans la console.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Renvoie tous `Promises` .  
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
      
      Renvoie tous les objets qui ont été instanciés à l’aide de `new functionName()` .  
   :::column-end:::
:::row-end:::  

---  

## tabulaire  

```console
table(data[, columns])
```  

Enregistre les données d’objet avec une mise en forme de tableau en fonction de l’objet de données avec des en-têtes de colonnes facultatifs.  Dans l’exemple de code et la figure ci-dessous, une liste de noms utilisant une table dans la console s’affiche.  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Résultat de la méthode table ()." lightbox="../media/console-table-display.msft.png":::
   Figure 24: résultat de la `table()` méthode  
:::image-end:::  

## déboguer  

```console
undebug(method)
```  

Arrête le débogage de la méthode spécifiée de telle sorte que lorsque la méthode est appelée, le débogueur n’est plus appelé.  

```console
undebug(getData);
```  

## ne plus surveiller  

```console
unmonitor(method)
```  

Arrête l’analyse de la méthode spécifiée.  Cette méthode est utilisée en concert avec la méthode [Monitor ()](#monitor) .  

```console
unmonitor(getData);
```  

## unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Arrête de surveiller les événements relatifs aux objets et aux événements spécifiés.  Par exemple, la commande suivante arrête tout le suivi des événements sur l’objet Window.  

```console
unmonitorEvents(window);
```  

Vous pouvez également cesser de surveiller de manière sélective des événements spécifiques sur un objet.  Par exemple, le code suivant commence à surveiller tous les `mouse` événements de l’élément actuellement sélectionné, puis cesse de surveiller les `mousemove` événements (il peut s’avérer utile de réduire le bruit dans la sortie de la console).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## doubl  

```console
values(object)
```  

Renvoie une matrice contenant les valeurs de toutes les propriétés de l’objet spécifié.  

```console
values(object);
```  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence sur les API de la console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Rép."  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Accélérer le runtime JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problème 1050237: le débogage (fonction) ne fonctionne pas | Monorail"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/utilities) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
