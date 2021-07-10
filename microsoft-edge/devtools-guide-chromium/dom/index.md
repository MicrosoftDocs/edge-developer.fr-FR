---
description: Découvrez comment afficher les nœuds, rechercher des nœuds, modifier des nœuds, référencer des nœuds dans la console, rompre sur les modifications de nœuds, etc.
title: Commencer à afficher et modifier le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 8340c4d4d7eacdb6ad4155c1c9699db150522f16
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643433"
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
# <a name="get-started-with-viewing-and-changing-the-dom"></a>Commencer à afficher et modifier le DOM  

Complétez ces didacticiels interactifs [](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) pour découvrir les principes de base de l’affichage et de la modification du modèle objet de document \(DOM\) d’une page à l’aide Microsoft Edge DevTools.  

Ce didacticiel part du principe que vous connaissez la différence entre le DOM et le code HTML. Accédez à [l’annexe : HTML par rapport au DOM](#appendix-html-versus-the-dom) pour obtenir une explication.  

## <a name="open-dom-examples"></a>Exemples d’ouverture de DOM  

1.  Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.  
    
    [Exemples DOM][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a>Afficher les nodes DOM  

L’arborescence DOM du panneau Éléments est l’endroit où vous pouvez faire toutes les activités liées au DOM dans DevTools.  

### <a name="inspect-a-node"></a>Inspecter un nœud  

Lorsque vous êtes intéressé par un nœud DOM particulier, **Inspect** est un moyen rapide d’ouvrir DevTools et d’examiner ce nœud.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Inspect a Node**, right-choose **Contrôleo** and choose **Inspect**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecter un nœud" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Inspecter un nœud  
    :::image-end:::  
    
    1.  **L’outil Elements** de DevTools s’ouvre.  `<li>Michelangelo</li>` est mis en surbrillant dans **l’arborescence DOM.**  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Mettre en surbrillon le nœud" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Mettre en `Michelangelo` surbrillade le nœud  
        :::image-end:::  
        
        1.  Choisissez **l’icône Inspect** \( Inspect \) dans le ![ coin supérieur gauche de ](../media/inspect-icon.msft.png) DevTools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Icône Inspecter" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Icône **Inspecter**  
            :::image-end:::  
            
1.  Sous **Inspecter un nœud,** choisissez le **texte Tokyo.**  À présent, `<li>Tokyo</li>` est mis en surbrillant dans l’arborescence DOM.  

L’inspection d’un nœud constitue également la première étape de l’affichage et de la modification des styles d’un nœud.  Accédez à [Prise en main avec l’affichage et la modification du CSS.][DevToolsCssGetStarted]  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a>Naviguer dans l’arborescence DOM avec un clavier  

Une fois que vous avez sélectionné un nœud dans l’arborescence DOM, vous pouvez naviguer dans l’arborescence DOM avec votre clavier.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.  `<li>Ringo</li>` est sélectionné dans l’arborescence DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspecter le nœud Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Inspecter le `Ringo` nœud  
    :::image-end:::  
    
    1.  Sélectionnez la `Up` touche de direction 2 fois.  `<ul>`  est sélectionnée.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspecter le nœud ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Inspecter le `ul` nœud  
        :::image-end:::  
        
    1.  Sélectionnez la `Left` touche de direction.  La `<ul>` liste est réduire.  
    1.  Sélectionnez de `Left` nouveau la touche de direction.  Le parent du `<ul>` nœud est sélectionné.  Dans ce cas, il s’agit `<div>` de l’ID `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Sélectionnez la touche de direction 2 fois de sorte que vous avez re-sélectionné la liste `Down` `<ul>` que vous venons de réduire.  Il doit se présenter comme suit: `<ul>... </ul>`  
    1.  Sélectionnez la `Right` touche de direction.  La liste se développe.  

### <a name="scroll-into-view"></a>Faire défiler vers l’avant  

Lorsque vous affichez l’arborescence DOM, vous pouvez être intéressé par un nœud DOM qui ne se trouve pas actuellement dans laport d’affichage.  Par exemple, supposons que vous avez fait défiler vers le bas de la page et que le nœud en haut de la page vous `<h1>` intéresse.  **Le défilement vers l’affichage** vous permet de repositionner rapidement la vue afin de pouvoir passer en revue le nœud.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.  
1.  Faites défiler vers le bas de la page Exemples DOM.  
1.  Le `<li>Magritte</li>` nœud doit toujours être sélectionné dans votre arborescence DOM.  Si ce n’est pas le cas, revenir [à Scroll into view](#scroll-into-view) et recommencer.  
1.  Pointez sur `<li>Magritte</li>` le nœud, ouvrez le menu contextuel \(clic droit\), puis choisissez Faire **défiler l’affichage.**  Votre port d’affichage défile vers le haut afin de passer en revue le nœud **Magritte.**  Accédez à [l’Annexe : options manquantes](#appendix-missing-options) si vous n’êtes pas en mesure de passer en revue l’option **Défilement vers l’affichage.**
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Faire défiler vers l’avant" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Faire défiler vers l’avant**  
    :::image-end:::  

### <a name="search-for-nodes"></a>Rechercher des nodes  

Vous pouvez effectuer une recherche dans l’arborescence DOM par chaîne, sélecteur CSS ou sélecteur XPath.  

1.  Concentrez votre curseur sur **l’outil Éléments.**  
1.  Sélectionnez `Control` + `F` \(Windows, Linux\) ou `Command` + `F` \(macOS\).  La barre de recherche s’ouvre en bas de l’arborescence DOM.  
1.  Tapez `The Moon is a Harsh Mistress`.  La dernière phrase est mise en évidence dans l’arborescence DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Mettre la requête en surbrill valeur dans la barre de recherche" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Mettre la requête en surbrill valeur dans la barre de recherche  
    :::image-end:::  
    
Comme mentionné ci-dessus, la barre de recherche prend également en charge les sélecteurs CSS et XPath.  

## <a name="edit-the-dom"></a>Modifier le DOM  

Vous pouvez modifier le DOM à la volée et examiner l’impact des modifications sur la page.  

### <a name="edit-content"></a>Modifier le contenu  

Pour modifier le contenu d’un nœud, double-cliquez sur le contenu dans l’arborescence DOM.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.  
    1.  Dans l’arborescence DOM, double-cliquez `Michelle` sur .  En d’autres termes, double-cliquez sur le texte entre `<li>` et `</li>` .  Le texte est mis en surbrillant pour indiquer qu’il est sélectionné.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Modifier le texte" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Modifier le texte  
        :::image-end:::  
        
    1.  Supprimer `Michelle` , `Leela` tapez , puis `Enter` sélectionnez pour confirmer la modification.  Le texte du DOM change de **Michelle** en **Leela**.  

### <a name="edit-attributes"></a>Modifier les attributs  

Pour modifier les attributs, double-cliquez sur le nom ou la valeur de l’attribut.  Suivez les instructions pour apprendre à ajouter des attributs à un nœud.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Edit Attributes**, right-choose **Contrôle** and choose **Inspect**.  
1.  Double-cliquez `<li>` sur .  Le texte est mis en surbrillade pour indiquer que le nœud est sélectionné.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Modifier le nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Modifier le nœud  
    :::image-end:::  
    
1.  Sélectionnez `Right` la touche de direction, ajoutez un espace, `style="background-color:gold"` tapez, puis sélectionnez `Enter` .  La couleur d’arrière-plan du nœud est or.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Ajouter un attribut de style au nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Ajouter un `style` attribut au nœud  
    :::image-end:::  
    
### <a name="edit-node-type"></a>Modifier le type de nœud  

Pour modifier le type d’un nœud, double-cliquez sur le type, puis tapez le nouveau type.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Edit Node Type**, right-chooseEve and choose **Inspect**. ****  
    1.  Double-cliquez `<li>` sur .  Le texte `li` est mis en surbrillant.  
    1.  `li`Supprimer, `button` tapez, puis sélectionnez `Enter` .  Le `<li>` nœud est changé en `<button>` nœud.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Changer le type de nœud en bouton" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Modifier le type de nœud par `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a>Réordez les nodes DOM  

Faites glisser les nodes pour les réorder.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Reorder DOM Nodes**, right-choose **Contrôle and** choose **Inspect**.  
    
    > [!NOTE]
    > Il s’agit du dernier élément de la liste.  
    
    1.  Dans l’arborescence DOM, faites `<li>Elvis Presley</li>` glisser vers le haut de la liste.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Faire glisser le nœud vers le haut de la liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Faire glisser le nœud vers le haut de la liste  
        :::image-end:::  
        
### <a name="force-state"></a>État de force  

Vous pouvez forcer les nodes à rester dans les états, y compris `:active` , , `:hover` et `:focus` `:visited` `:focus-within` .  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Sous **l’état Force,** **pointez sur la souris de l’en-dessous.**  La couleur d’arrière-plan devient orange.  
    1.  Pointez **sur le Bouton de l’enfant,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
    1.  Pointez `<li class="demo--hover">The Lord of the Flies</li>` dessus, ouvrez le menu contextuel \(clic droit\), puis choisissez **Force State**  >  **:hover**.  Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.  La couleur d’arrière-plan reste orange même si vous ne pointez pas réellement sur le nœud.  

### <a name="hide-a-node"></a>Masquer un nœud  

Sélectionnez `H` pour masquer un nœud.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Sous **Masquer un nœud,** choisissez avec le droit de la main **Les étoiles ma destination** et sélectionnez **Inspecter.**  
    1.  Sélectionnez la `H` clé.  Le nœud est masqué.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Apparence du nœud dans l’arborescence DOM une fois masqué" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Apparence du nœud dans l’arborescence DOM une fois masqué  
        :::image-end:::  
        
    1.  Sélectionnez `H` de nouveau la clé.  Le nœud est de nouveau affiché.  

### <a name="delete-a-node"></a>Supprimer un nœud  

Sélectionnez `Delete` pour supprimer un nœud.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.  
    1.  Sélectionnez la `Delete` clé.  Le nœud est supprimé.  
    1.  Sélectionnez `Control` + `Z` \(Windows, Linux\) ou `Command` + `Z` \(macOS\).  La dernière action est annulée et le nœud réapparaît.  

## <a name="access-nodes-in-the-console"></a>Accès aux nodes dans la console  

DevTools fournit quelques raccourcis pour accéder aux nodes DOM à partir de la console ou obtenir des références JavaScript à chacun d’eux.  

### <a name="reference-the-currently-selected-node-with-0"></a>Référencer le nœud actuellement sélectionné avec 0 $  

Lorsque vous examinez un nœud, le texte à côté du nœud signifie que vous pouvez faire référence à ce nœud dans la `== $0` console avec la variable `$0` .  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.  
    1.  Sélectionnez `Escape` la clé pour ouvrir le caisse de la console.  
    1.  Tapez `$0` et sélectionnez la `Enter` clé.  Le résultat de l’expression indique `$0` que le résultat est `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Résultat de la première expression $0 dans la console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Résultat de la première `$0` expression dans la **console**  
        :::image-end:::  
        
    1.  Pointez sur le résultat.  Le nœud est mis en surbrillade dans laport d’affichage.  
    1.  Choisissez `<li>Dune</li>` dans l’arborescence DOM, tapez `$0` de nouveau dans la console, puis sélectionnez à `Enter` nouveau.  À présent, `$0` évalue à `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Résultat de la deuxième expression $0 dans la console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Résultat de la deuxième `$0` expression dans la **console**  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a>Store en tant que variable globale  

Si vous devez faire référence à un nœud plusieurs fois, stockez-le en tant que variable globale.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Sous **Store en tant que variable globale,** pointez sur la grande **veille,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
    1.  Pointez `<li>The Big Sleep</li>` dessus dans l’arborescence DOM, ouvrez le menu contextuel \(clic droit\), puis choisissez Store en tant que variable **globale.**  Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.  
    1.  Tapez `temp1` dans la console, puis sélectionnez `Enter` .  Le résultat de l’expression indique que la variable est évaluée au nœud.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Résultat de l’expression temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Résultat de `temp1` l’expression  
        :::image-end:::  
        
### <a name="copy-js-path"></a>Copier le chemin d’accès JS  

Copiez le chemin d’accès JavaScript sur un nœud lorsque vous devez le référencer dans un test automatisé.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Sous **Copier le chemin d’accès JS,** pointez sur le contrôle **ContrôleZov,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
    1.  Pointez `<li>The Brothers Karamazov</li>` dessus dans l’arborescence DOM, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier**le  >  **chemin d’accès JS**.  Une expression résolue en nœud a `document.querySelector()` été copiée dans le Presse-papiers.  
    1.  Sélectionnez `Control` + `V` \(Windows, Linux\) ou `Command` + `V` \(macOS\) pour coller l’expression dans la console.  
    1.  Sélectionnez `Enter` pour évaluer l’expression.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Résultat de l’expression Copier le chemin d’accès JS" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Résultat de l’expression **Copier le chemin d’accès JS**  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a>Pause sur les modifications DOM  

DevTools vous permet de suspendre le code JavaScript d’une page lorsque javaScript modifie le DOM.  

### <a name="break-on-attribute-modifications"></a>Pause sur les modifications d’attribut  

Utilisez des points d’arrêt de modification d’attribut lorsque vous souhaitez suspendre le JavaScript qui entraîne la modification de n’importe quel attribut d’un nœud.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Break on attribute modifications**, right-choose **Saueruterut** and choose **Inspect**.  
    1.  Dans l’arborescence DOM, pointez sur , ouvrez le menu contextuel `<li id="target">Sauerkraut</li>` \(clic droit\), puis choisissez **Break On**  >  **Attribute Modifications**.  Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Pause sur les modifications d’attribut" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Pause sur les modifications d’attribut**  
        :::image-end:::  
        
    1.  À l’étape suivante, il vous sera demandé de choisir un bouton qui interrompt le code de la page.  Une fois la page suspendue, vous ne pouvez plus la faire défiler.  Vous devez choisir **Resume Script** \( Resume Script \) pour que la page défile ![ à ](../media/resume-script-icon.msft.png) nouveau.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Où reprendre l’exécution du script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Où reprendre l’exécution du script  
        :::image-end:::  
        
    1.  Sélectionnez le **bouton Définir l’arrière-plan** ci-dessus.  Cela définit `style` l’attribut du nœud sur `background-color:thistle` .  DevTools suspend la page et met en évidence le code à l’origine de la modification de l’attribut.  
    1.  Choose **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \), as mentioned earlier.  
    
### <a name="break-on-node-removal"></a>Rupture lors de la suppression du nœud  

Si vous souhaitez suspendre lorsqu’un nœud particulier est supprimé, utilisez des points d’arrêt de suppression de nœud.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Break on Node Removal**, right-choose **Contrôlemancer** and choose **Inspect**.  
    1.  Dans l’arborescence DOM, pointez sur , ouvrez le menu contextuel `<li id="target">Neuromancer</li>` \(clic droit\), puis choisissez **Pause sur**la suppression  >  **du nœud.**  Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.  
    1.  Sélectionnez le **bouton Supprimer** ci-dessus.  DevTools suspend la page et met en évidence le code qui a provoqué la suppression du nœud.  
    1.  Choose **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).  
    
### <a name="break-on-subtree-modifications"></a>Pause sur les modifications de sous-arbre  

Après avoir placé un point d’arrêt de modification de sous-arbre sur un nœud, DevTools interrompt la page lorsque l’un des descendants du nœud est ajouté ou supprimé.  

1.  [Ouvrez des exemples DOM.](#open-dom-examples)  
1.  Under **Break on Subtree Modifications**, right-choose A Fire Upon The **Deep** and choose **Inspect**.  
    1.  Dans l’arborescence DOM, pointez sur , qui est le nœud ci-dessus, ouvrez le menu contextuel `<ul id="target">` `<li>A Fire Upon the Deep</li>` \(clic droit\), puis choisissez **Break On**  >  **Subtree Modifications**.  Si l’option n’est pas affichée, accédez à Annexe [: Options manquantes.](#appendix-missing-options)  
    1.  Choose **Add Child**.  Le code s’interrompt car un nœud a `<li>` été ajouté à la liste.  
    1.  Choose **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).  
    
## <a name="next-steps"></a>Étapes suivantes  

Cela couvre la plupart des fonctionnalités DOM dans DevTools.  Vous pouvez découvrir le reste des fonctionnalités en pointant sur les nodes dans l’arborescence DOM, en ouvrant le menu contextuel \(clic droit\) et en testant les autres options qui n’ont pas été couvertes dans ce didacticiel.  Accédez aux [raccourcis clavier du panneau][DevToolsShortcutsElements]Éléments.  

Consultez la [Microsoft Edge d’accueil de DevTools][MicrosoftEdgeDevTools] pour découvrir tout ce que vous pouvez faire avec DevTools.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a>Annexe : HTML par rapport au DOM  

La section suivante explique rapidement la différence entre le code HTML et le DOM.  

:::row:::
   :::column span="":::
      Lorsque vous utilisez un navigateur web pour demander une page, le serveur renvoie du code HTML comme l’extrait de code suivant  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      Le navigateur pare le code HTML et crée une arborescence d’objets comme la liste suivante.  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

Cette arborescence d’objets, ou de nodes, représentant le contenu de la page est appelée DOM.  

:::row:::
   :::column span="":::
      Pour l’instant, il ressemble au code HTML, mais supposons que le script référencé en bas du code HTML exécute l’extrait de code suivant.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Ce code supprime le `h1` nœud et ajoute un autre nœud au `p` DOM.  Le DOM complet affiche maintenant la liste suivante.  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

Le code HTML de la page est désormais différent du DOM.  En d’autres termes, html représente le contenu de la page initiale et le DOM représente le contenu de la page actuelle.  Lorsque JavaScript ajoute, supprime ou modifie des nodes, le DOM devient différent du code HTML.  

Accédez [à Introduction au DOM][MDNIntroductionToDOM] pour en savoir plus.  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a>Annexe : Options manquantes  

De nombreuses instructions de ce didacticiel vous indiquent de pointer sur un nœud dans l’arborescence DOM, d’ouvrir le menu contextuel \(clic droit\), puis de choisir une option dans le menu contextuel qui s’ouvre.  Si l’option spécifiée dans le menu contextuel n’est pas affichée, essayez de pointer à l’extérieur du texte du nœud et d’ouvrir le menu contextuel \(clic droit\).  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Où choisir si toutes les options ne sont pas affichées" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Où choisir si toutes les options ne sont pas affichées  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge outils de développement \(Chromium\) | Documents Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Prise en main Avec l’affichage et la modification des | Documents Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Raccourcis clavier de l’outil Éléments : Microsoft Edge raccourcis clavier DevTools | Documents Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Example | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Présentation de la | DOM MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/dom/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
