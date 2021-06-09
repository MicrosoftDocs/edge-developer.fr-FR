---
description: Vue d’ensemble de l’interaction avec la page web actuelle dans le navigateur à l’aide de l’outil Console
title: Utiliser la console pour interagir avec le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 56ce6b1d8f1ad98eeb9c141c2e9b002e7679d7de
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597015"
---
# <a name="use-the-console-to-interact-with-the-dom"></a>Utiliser la console pour interagir avec le DOM

**L’outil Console** n’est pas uniquement utilisé pour la [journalisation des informations][DevtoolsConsoleConsoleLog] ou pour exécuter un [javaScript arbitraire.][DevtoolsConsoleConsoleJavascript]  Il s’agit également d’un excellent moyen d’interagir avec la page web dans le navigateur.  Considérez-la comme une version d’environnement de script de **l’outil Inspect.**  

## <a name="read-from-the-dom"></a>Lecture à partir du DOM

Pour référencer l’en-tête de la page web, effectuer les actions suivantes.  

1.  Ouvrez la **console.**
    *   Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  
1.  Tapez ou copiez-collez l’extrait de code suivant dans la **console.**  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Pour obtenir une référence à l’en-tête dans la console, utilisez document.querySelector" lightbox="../media/console-dom-get-reference.msft.png":::
    Pour obtenir une référence à l’en-tête dans la console, utilisez `document.querySelector`  
:::image-end:::  

Si vous sélectionnez ou déplacez le curseur de la souris sur le résultat `Shift` + `Tab` HTML, DevTools met en évidence l’en-tête pour vous.  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools met en évidence la section que vous choisissez dans la console" lightbox="../media/console-dom-highlight-element.msft.png":::
    DevTools met en évidence la section que vous choisissez dans la **console**  
:::image-end:::  

## <a name="manipulate-the-dom"></a>Manipuler le DOM

Vous pouvez également manipuler la page web.  Par exemple, si vous copiez et collez ou tapez ce qui suit dans la **console,** une bordure verte s’affiche autour de l’en-tête.

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Pour ajouter une bordure à un élément, utilisez la console" lightbox="../media/console-dom-add-border.msft.png":::
    Pour ajouter une bordure à un élément, utilisez la **console**  
:::image-end:::  

Selon la complexité de la page web, il peut être difficile de trouver l’élément à manipuler.  Toutefois, vous pouvez utiliser **l’outil Inspect** pour vous aider.  Dites que vous souhaitez manipuler la `Documentation` partie dans l’en-tête.

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Afficher l’élément que vous inspectez à l’écran" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    Afficher l’élément que vous inspectez à l’écran  
:::image-end:::  

Pour obtenir une référence directe à l’élément à manipuler, effectuer les actions suivantes.  

1.  Utilisez **l’outil Inspect** pour choisir l’élément.  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Pour choisir un élément, utilisez l’outil Inspect" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        Pour choisir un élément, utilisez **l’outil Inspect**  
    :::image-end:::  
    
1.  Choisissez-le et DevTools passe à **l’outil Elements.**  
1.  Choisissez le `...` menu en face de l’élément dans l’arborescence DOM.  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="L’élément choisi s’affiche dans l’arborescence DOM de l’outil Elements, choisissez le menu de dépassement pour obtenir d’autres fonctionnalités" lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        L’élément choisi s’affiche dans l’arborescence DOM de l’outil **Elements,** choisissez le menu de dépassement pour obtenir d’autres fonctionnalités  
    :::image-end:::  
    
1.  Ouvrez le menu contextuel et choisissez `Copy`  >  `Copy JS Path` .  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Copier le chemin d’accès JavaScript à partir d’un élément dans l’arborescence DOM de l’outil Elements" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        Copier le chemin d’accès JavaScript à partir d’un élément dans l’arborescence DOM de **l’outil Elements**  
    :::image-end:::  
    
1.  Revenir à la **console et** coller la commande.  
    
Pour modifier le texte du lien, `My Playground` ajoutez-le `.textContent = "My Playground"` à la commande que vous avez précédemment passée.  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Utiliser la console pour modifier le contenu d’un élément" lightbox="../media/console-dom-change-content.msft.png":::
    Utiliser la **console pour** modifier le contenu d’un élément  
:::image-end:::  

Utilisez toutes les manipulations DOM JavaScript que vous souhaitez faire dans la **console.**  Pour le rendre plus pratique, **la console** est livré avec quelques méthodes d’aide.  

## <a name="helpful-console-utility-methods"></a>Méthodes utilitaires de console utiles  

De nombreuses méthodes et raccourcis pratiques sont disponibles en tant [qu’utilitaires de console.][DevtoolsConsoleUtilities]  Certaines méthodes sont extrêmement puissantes et sont probablement des éléments que vous avez probablement écrits sous la mesure d’une série `console.log()` d’instructions dans le passé.

### <a name="the-power-to-the-"></a>L’alimentation à la $

La console dispose de puissances spéciales et vous vous en souvenez `$` peut-être à partir de jQuery. ****

*   `$_` stocke le résultat de la dernière commande.  Ainsi, si vous `2 + 2` tapez et sélectionnez, puis `Enter` `$_` tapez , la **console** vous `4` affiche.
*   `$0` est une pile des derniers éléments `$4` inspectés est toujours la plus `$0` nouvelle.  Ainsi, dans l’exemple précédent, vous avez simplement choisi l’élément dans l’outil **Inspect** et le type `$0.textContent = "My Playground"` pour obtenir le même effet.
*   `$x()` vous permet de choisir des éléments DOM à l’aide de XPATH.
*   `$()` et `$$()` sont des versions plus courtes de for et `document.querySelector()` `document.querySelectorAll()` .  
    
Par exemple, l’extrait de code suivant récupère tous les liens dans la page web \(comme c’est le cas pour \) et affiche les liens sous forme de tableau triable à copier-coller, par exemple, dans `$$('a')` `document.querySelectorAll('a')` Excel.

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Obtenir tous les liens dans la page web et afficher le résultat sous la mesure d’un tableau" lightbox="../media/console-dom-get-all-links.msft.png":::
    Obtenir tous les liens dans la page web et afficher le résultat sous la mesure d’un tableau  
:::image-end:::  

Toutefois, si vous ne souhaitez pas afficher les informations, mais que vous souhaitez les récupérer en tant que données.  Le `$$('a')` raccourci fournit les liens d’ancrage et toutes les propriétés de chacun d’eux.  Le problème est que vous souhaitez uniquement les liens et le texte associé.  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="Le raccourci $$ renvoie beaucoup trop d’informations" lightbox="../media/console-dom-too-much-link-information.msft.png":::
    Le `$$` raccourci renvoie beaucoup trop d’informations  
:::image-end:::  

Le `$$` raccourci présente une fonctionnalité supplémentaire intéressante.  Au lieu de renvoyer un `NodeList` pur comme , le raccourci vous donne toutes les `document.querySelectorAll()` `$$` `Array` méthodes.  Utilisez `map()` la méthode pour réduire les informations à ce dont vous avez besoin.  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

L’extrait de code renvoie un tableau de tous les liens en tant qu’objets avec `url` et `text` propriétés.  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Utiliser la carte sur $$ pour filtrer les informations au minimum" lightbox="../media/console-dom-filter-link-data.msft.png":::
    Utiliser la carte `$$` pour filtrer les informations jusqu’au minimum  
:::image-end:::  

Vous n’avez pas encore terminé, plusieurs liens sont des liens internes vers la page web ou ont du texte vide.  Utilisez la méthode de filtre pour vous débarrasser des liens internes.  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Obtenir les liens qui ne sont pas vides et qui sont externes" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    Obtenir les liens qui ne sont pas vides et qui sont externes  
:::image-end:::  

Comme affiché au début de la page web, vous pouvez également modifier ces éléments.  Par exemple, l’extrait de code suivant crée une bordure verte autour de tous les liens externes :

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Pour mettre en surbrillez tous les liens externes, ajoutez une bordure verte autour de chacun d’eux" lightbox="../media/console-dom-highlight-links.msft.png":::
    Pour mettre en surbrillez tous les liens externes, ajoutez une bordure verte autour de chacun d’eux  
:::image-end:::  

Au lieu d’écrire du JavaScript complexe pour filtrer les résultats, utilisez la puissance des sélecteurs CSS.  

Pour créer un tableau des images et des informations de toutes les images de la page web qui ne sont pas des images en ligne, effectuer `src` `alt` les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Tapez ou copiez-collez l’extrait de code suivant.  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Pour choisir des éléments, utilisez un sélecteur CSS complexe" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    Pour choisir des éléments, utilisez un sélecteur CSS complexe  
:::image-end:::  

Prêt pour un exemple encore plus complexe ?  Les pages web HTML générées à partir de markdown comme cet article ont des valeurs d’ID automatiques pour chaque titre afin de vous permettre d’établir un lien profond vers cette section.  Par exemple, une `# New features` modification apportée `<h1 id="new-features">New features</h1>` à .  

Pour lister tous les en-tête automatiques à copier et coller, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Tapez ou copiez-collez l’extrait de code suivant.  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

Le résultat est le texte qui contient le contenu de chaque titre suivi de l’URL complète qui pointe vers celui-ci.  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Obtenir tous les titres et les URL générées à partir de la page web" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    Obtenir tous les titres et les URL générées à partir de la page web  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a>Nettoyer avec effacer et copier

Lorsque vous développez **dans la console,** les choses peuvent être désordessée.  Vous trouverez peut-être frustrant d’essayer de choisir des résultats pendant que vous copiez et collez.  Les deux méthodes utilitaires suivantes vous aident.  

*   `copy()` copie ce que vous lui donnez dans le Presse-papiers.  La `copy()` méthode est particulièrement utile lorsque vous la mélangez `$_` avec celle qui copie le dernier résultat.
*   `clear()` clears the **Console**.

### <a name="read-and-monitor-events"></a>Lire et surveiller les événements

Deux autres méthodes utilitaires intéressantes de **console** traitent de la gestion des événements.

*   `getEventListeners(node)` répertorie tous les écouteurs d’événements d’un nœud.
*   `monitorEvents(node, events)` surveille et enregistre les événements qui se produisent sur un nœud.

Pour lister tous les auditeurs d’événements affectés au premier formulaire dans la page web, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Tapez ou copiez-collez l’extrait de code suivant.  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Obtenir tous les écouteurs d’événements pour le premier formulaire dans la page web" lightbox="../media/console-dom-get-form-events.msft.png":::
    Obtenir tous les écouteurs d’événements pour le premier formulaire dans la page web  
:::image-end:::  

Lorsque vous surveillez, vous recevez une notification dans la **console** chaque fois que des modifications sont apportées aux éléments spécifiés.  Vous définissez les événements que vous souhaitez écouter en tant que deuxième paramètre.  Il est important que vous définissiez les événements que vous souhaitez surveiller, sinon tout événement qui se produit sur l’élément est signalé.

Pour obtenir une notification dans la **console** chaque fois que vous faites défiler, resizez la fenêtre ou lorsque l’utilisateur tape du texte dans le formulaire de recherche, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Tapez ou copiez-collez l’extrait de code suivant.  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="La console affiche tous les événements de défilement qui se produisent sur la fenêtre" lightbox="../media/console-dom-monitor-events.msft.png":::
    **La console** affiche tous les événements de défilement qui se produisent sur la fenêtre  
:::image-end:::  

Pour enregistrer n’importe quelle action de touche sur l’élément actuellement choisi, concentrez-vous sur le formulaire de recherche dans l’en-tête et sélectionnez certaines touches.  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="La console affiche les événements de keyup qui se produisent sur le formulaire" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    **La console** affiche les `keyup` événements qui se produisent sur le formulaire  
:::image-end:::  

Pour l’arrêter, supprimez la surveillance que vous définissez à l’aide de l’extrait de code suivant.  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a>Réutilisation des scripts de manipulation DOM

Il peut s’avérer utile de manipuler le DOM à partir de la **console.**  Vous pouvez bientôt vous lancer dans les limitations de la **console** en tant que plateforme de développement.  La bonne nouvelle est que l’outil [Sources][DevtoolsSourcesIndex] dans DevTools offre un environnement de développement complet.  Dans **l’outil Sources,** vous pouvez effectuer les actions suivantes.  

*   Stockez vos scripts pour la **console en** tant [qu’extraits de code.][DevToolsJavascriptSnippets]  
*   Exécutez les scripts dans une page web à l’aide d’un raccourci clavier ou de l’éditeur.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console en tant qu’environnement JavaScript | Documents Microsoft"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Journaux dans l’outil Console | Documents Microsoft"  
[DevtoolsConsoleUtilities]: ./utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Exécutez des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsSourcesIndex]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
