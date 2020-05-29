---
title: XXXXXX xxxxxxx xxx xxxxxxxxx
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601795"
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

Dans la [figure 1](#figure-1), une expression simple \ ( `2 + 2` \) est évaluée.  La `$_` propriété est alors évaluée, qui contient la même valeur.  

> ##### Figure1  
> `$_` est la dernière expression évaluée  
> ![$ _ est l’expression la plus récemment évaluée.][ImageRecentExpression]  

Dans la [figure 2](#figure-2), l’expression évaluée contient initialement un tableau de noms.  Si vous évaluez la `$_.length` longueur de l’argument matrice, la valeur stockée dans `$_` les modifications devient la dernière expression évaluée `4` .  

> ##### Figure 2  
> `$_` change lorsque de nouvelles commandes sont évaluées  
> ![$ _ change lorsque de nouvelles commandes sont évaluées][ImageChangedRecentExpression]  

## Élément récemment sélectionné ou objet JavaScript  

```console
$0
```  

Retourne l’élément le plus récemment sélectionné ou l’objet JavaScript.  `$1` renvoie le second dernier sélectionné, et ainsi de suite.  Les `$0` commandes,,, `$1` `$2` `$3` et `$4` permettent de faire une référence historique aux cinq derniers éléments DOM examinés dans le panneau **éléments** ou les cinq derniers objets du tas JavaScript sélectionnés dans le panneau **mémoire** .  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

Dans [figure 3](#figure-3), un `img` élément est sélectionné dans le panneau **éléments** .  Le tiroir **Console** de la console `$0` a été évalué et affiche le même élément.  

> ##### Figure3  
> La liste  `$0`  
> ![$0][ImageElement0]  

Dans la [figure 4](#figure-4), l’image montre un élément différent sélectionné dans la même page.  L' `$0` élément désormais fait référence à l’élément que vous venez de sélectionner, tandis qu’il `$1` renvoie le précédent.  

> ##### Figure 4  
> La liste  `$1`  
> ![$1][ImageElement1]  

## Sélecteur de requête  

```console
$(selector, [startNode])
```  

Renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.  Cette méthode est un alias de la méthode [document. querySelector ()][MDNDocumentQuerySelector] .  

Dans la [figure 5](#figure-5), une référence au premier `<img>` élément du document est renvoyée.  

> ##### Figure 5  
> La liste  `$('img')`  
> ![$ ('Img')][ImageElementImg]  

Cliquez avec le bouton droit sur le résultat retourné et sélectionnez **Reveal dans le panneau d’éléments** pour le Rechercher dans le DOM ou **faites défiler l’écran** pour l’afficher sur la page.  

Dans la [figure 6](#figure-6), une référence à l’élément actuellement sélectionné est renvoyée et la propriété SRC est affichée.  

> ##### Figure 6  
> La liste  `$('img').src`  
> ![$ ('Img'). SRC][ImageElementImgSource]  

Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.  La valeur par défaut de ce paramètre est `document` .  

Dans la [figure 7](#figure-7), le premier `img` élément est trouvé après `title--image` et affiche le `src` résultat correct.  

> ##### Figure 7  
> $ ('Img', document. querySelector ('title--image')). SRC  
> ![$ ('Img', document. querySelector ('title--image')). SRC][ImageElementImgNodeSource]  

> [!NOTE]
> Si vous utilisez une bibliothèque telle que jQuery qui utilise `$` , cette fonctionnalité est écrasée et `$` correspond à l’implémentation de cette bibliothèque.  

## Sélecteur de requête  

```console
$$(selector, [startNode])
```  

Retourne un tableau d’éléments qui correspondent au sélecteur CSS spécifié.  Cette méthode équivaut à appeler la méthode [document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .  

Dans la [figure 8](#figure-8), utilisez `$$()` pour créer un tableau de tous les `<img>` éléments du document actuel et afficher la valeur de la `src` propriété de chaque élément.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### Figure8  
> Utiliser `$$()` pour sélectionner toutes les images du document et afficher les sources  
> ![Utilisation de $ $ () pour sélectionner toutes les images du document et afficher les sources][ImageArrayElementImgSource]  

Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.  La valeur par défaut de ce paramètre est `document` .  

Dans la [figure 9](#figure-9), une version modifiée de la [figure 8](#figure-8) utilise `$$()` pour créer un tableau de tous les `<img>` éléments qui s’affichent dans le document actuel après le nœud sélectionné.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### Figure9  
> Utiliser `$$()` pour sélectionner toutes les images qui apparaissent après l' `<div>` élément spécifié dans le document et afficher les sources  
> ![Utilisation de $ $ () pour sélectionner toutes les images qui s’affichent après l’élément <div> spécifié dans le document et afficher les sources][ImageArrayElementImgNodeSource]  

> [!NOTE]
> Appuyez sur `Shift` + `Enter` la console pour commencer une nouvelle ligne sans exécuter le script.  

## Suivante  

```console
$x(path, [startNode])
```  

Renvoie un tableau d’éléments DOM qui correspondent à l’expression XPath spécifiée.  

Dans la [figure 10](#figure-10), tous les `<p>` éléments de la page sont renvoyés.  

```console
$x("//p")
```  

> ##### Figure10  
> Utilisation d’un sélecteur XPath  
> ![Utilisation d’un sélecteur XPath][ImageArrayXpath]  

Dans la [figure 11](#figure-11), tous les `<p>` éléments contenant des `<a>` éléments sont renvoyés.  

```console
$x("//p[a]")
```  

> ##### Figure11  
> Utilisation d’un sélecteur XPath plus complexe  
> ![Utilisation d’un sélecteur XPath plus complexe][ImageArrayXpathChild]  

À l’instar des autres commandes de sélecteur, `$x(path)` possède un deuxième paramètre facultatif, `startNode` qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.  

> ##### Figure12  
> Utilisation d’un sélecteur XPath avec `startNode`  
> ![Utilisation d’un sélecteur XPath avec startNode][ImageArrayXpathNode]  

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
> Le [#1050237 problème de chrome][MonorailIssue1050237] effectue le suivi d’un bogue avec la `debug()` fonction.  Si vous rencontrez ce problème, essayez plutôt d' [utiliser des points d’arrêt][DevtoolsJavascriptBreakpoints] .  

Lorsque vous demandez la méthode spécifiée, le débogueur est appelé et s’interrompt à l’intérieur de la méthode sur le panneau **sources** pour vous permettre de parcourir le code et de le déboguer.  

```console
debug("debug");
```  

> ##### Figure13  
> Casser dans une méthode avec `debug()`  
> ![Casser au sein d’une méthode à l’aide du débogage ()][ImageDebugMethod]  

Utilisez `undebug(method)` cette commande pour arrêter l’interruption de la méthode, ou utilisez l’interface utilisateur pour désactiver tous les points d’arrêt.  

Pour plus d’informations sur les points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Affiche une liste de styles d’objet de toutes les propriétés de l’objet spécifié.  Cette méthode est un alias de la méthode [console. dir ()][MDNConsoleDir] .  

Évaluez `document.head` la console pour afficher le code HTML entre `<head>` les `</head>` balises et.  Dans la [figure 14](#figure-14), une liste de styles d’objet s’affiche après utilisation `console.dir()` dans la console.  

```console
document.head;
dir(document.head);
```  

> ##### Figure14  
> Journalisation `document.head` avec la `dir()` méthode  
> ![Journalisation du document. Head avec la méthode dir ()][ImageLogObject]  

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

Dans la [figure 15](#figure-15), l' `document.body` écran s’ouvre dans le panneau **éléments** .  

```console
inspect(document.body);
```  

> ##### Figure15  
> Examen d’un élément avec `inspect()`  
> ![Inspecter un élément avec Inspect ()][ImageInspectElement]  

Lorsque vous passez une méthode à inspecter, la méthode ouvre le document dans le panneau **sources** et vous pouvez le consulter.  

## getEventListeners  

```console
getEventListeners(object)
```  

Renvoie les écouteurs d’événements enregistrés sur l’objet spécifié.  La valeur de retour est un objet qui contient un tableau pour chaque type d’événement inscrit \ (tel que `click` ou `keydown` \).  Les membres de chaque tableau sont des objets qui décrivent l’écouteur inscrit pour chaque type.  Dans la [figure 16](#figure-16), tous les détecteurs d’événements enregistrés sur l’objet document apparaissent.  

```console
getEventListeners(document);
```  

> ##### Figure16  
> Résultat de l’utilisation de `getEventListeners(document)`  
> ![Sortie de l’utilisation de getEventListeners (document)][ImageGetListeners]  

S’il existe plusieurs écouteurs enregistrés sur l’objet spécifié, le tableau contient un membre pour chaque écouteur.  Dans la [figure 16](#figure-16), deux écouteurs d’événements sont inscrits dans l’élément document pour l' `click` événement.  

> ##### Figure17  
> Écouteurs multiples  
> ![Écouteurs multiples][ImageMultipleListeners]  

Vous pouvez également développer chacun des objets suivants pour découvrir les propriétés.  

> ##### Figure 18  
> Affichage développé de l’objet Listener  
> ![Affichage développé de l’objet Listener][ImageListenersExpanded]  

## clés  

```console
keys(object)
```  

Retourne une matrice contenant les noms des propriétés appartenant à l’objet spécifié.  Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .  

Par exemple, supposons que votre application définisse l’objet suivant.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

Dans la [figure 19](#figure-19), le résultat suppose qu’il `player1` a été défini dans l’espace de noms global \ (pour la simplicité \) avant de taper `keys(player1)` et `values(player1)` dans la console.  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### Figure 19  
> `keys()`Commandes et `values()`  
> ![Commandes Keys () et values ()][ImageConsoleKeysValues]  

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

> ##### Figure 20  
> La `monitor()` méthode  
> ![Méthode Monitor ()][ImageConsoleMonitorSum]  

Utiliser `unmonitor(method)` pour cesser de surveiller.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Quand l’un des événements spécifiés se produit sur l’objet spécifié, l’objet Event est enregistré dans la console.  Vous pouvez spécifier un événement unique à surveiller, un tableau d’événements ou l’un des types d’événements génériques mappés à une collection prédéfinie d’événements.  Voir [figure 21](#figure-21).  

Le code suivant analyse tous les événements de redimensionnement sur l’objet Window.  

```console
monitorEvents(window, "resize");
```  

> ##### Figure 21  
> Surveiller les événements de redimensionnement d’une fenêtre  
> ![Surveiller les événements de redimensionnement d’une fenêtre][ImageMonitorResize]  

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

Dans la [figure 22](#figure-22), le `key` type d’événement correspondant aux `key` événements dans un champ de texte de saisie est actuellement sélectionné dans le panneau **éléments** .  

```console
monitorEvents($0, "key");
```  

Dans la [figure 22](#figure-22) , l’exemple de sortie après avoir tapé un caractère dans le champ de texte est affiché.  

> ##### Figure 22  
> Surveiller les événements de touche  
> ![Surveiller les événements de touche][ImageMonitorKey]  

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

Les profils risquent également d’être imbriqués.  Dans la [figure 23](#figure-23) , le résultat est le même quel que soit l’ordre.  

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

Les profils risquent également d’être imbriqués.  Dans la [figure 23](#figure-23) , le résultat est le même quel que soit l’ordre.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Le résultat s’affiche sous la forme d’un instantané de tas dans le panneau **mémoire** .  

> ##### Figure 23  
> Profils groupés  
> ![Profils groupés][ImageGroupedProfiles]  

> [!NOTE]
> Les profils d’UC multiples peuvent fonctionner en même temps et vous n’avez pas besoin de les clôturer dans l’ordre de création.  

## tabulaire  

```console
table(data[, columns])
```  

Enregistre les données d’objet avec une mise en forme de tableau en fonction de l’objet de données avec des en-têtes de colonnes facultatifs.  Dans la [figure 24](#figure-24), une liste de noms utilisant une table dans la console s’affiche.  

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

> ##### Figure 24  
> La `table()` méthode  
> ![Méthode table ()][ImageConsoleTable]  

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

Arrête l’analyse de la méthode spécifiée.  Ce mode est utilisé en concert avec la méthode [Monitor ()](#monitor) .  

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

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Figure 1: $ _ est l’expression la plus récemment évaluée"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Figure 2: $ _ change lorsque de nouvelles commandes sont évaluées"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Figure 3: $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Figure 4: $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Figure 5: $ ('img')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Figure 6: $ ('img'). SRC"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Figure 7: $ ('img', document. querySelector ('title--image')). SRC"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Figure 8: utilisation de $ $ () pour sélectionner toutes les images du document et afficher les sources"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Figure 9: utilisation de $ $ () pour sélectionner toutes les images qui s’affichent après l’élément <div> spécifié dans le document et afficher les sources"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Figure 10: utilisation d’un sélecteur XPath"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Figure 11: utilisation d’un sélecteur XPath plus complexe"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Figure 12: utilisation d’un sélecteur XPath avec startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Figure 13: rupture au sein d’une méthode à l’aide du débogage ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Figure 14: enregistrement du document. Body avec la méthode dir ()"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Figure 15: examen d’un élément avec Inspect ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Figure 16: sortie de l’utilisation de getEventListeners (document)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Figure 17: écouteurs multiples"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Figure 18: vue développée de l’objet Listener"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Figure 19: commandes Keys () et values ()"  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Figure 20: méthode Monitor ()"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Figure 21: surveiller les événements de redimensionnement d’une fenêtre"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Figure 22: surveiller les événements de touche"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Figure 23: profils groupés"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Figure 24: méthode table ()"  

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
