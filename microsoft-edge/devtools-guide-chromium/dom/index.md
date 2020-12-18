---
description: Pour afficher des nœuds, recherchez des nœuds, modifiez des nœuds, des nœuds de référence dans la console, Rompez les changements de nœud, etc.
title: Découvrir comment afficher et modifier le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5b12b984aed7e35ce11dd45e8bc33f5d5fd454f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231103"
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

# Découvrir comment afficher et modifier le DOM  

Pour découvrir les notions de base de l’affichage et de la modification du DOM d’une page, suivez les didacticiels interactifs de Microsoft DevTools.  

Ce didacticiel part du principe que vous connaissez la différence entre le DOM et le code HTML.  Accédez à l' [annexe: HTML et au DOM](#appendix-html-versus-the-dom) pour obtenir une explication.  

## Exemples d’ouverture de DOM  

1.  Maintenez la touche Windows enfoncée `Control` `Command` et sélectionnez les **exemples DOM** à ouvrir dans un nouvel onglet.  
    
    [Exemples DOM][GlitchDomExamples]  
    
## Afficher les nœuds DOM  

L’arborescence DOM du panneau éléments vous permet d’effectuer toutes les activités liées au DOM dans DevTools.  

### Inspecter un nœud  

Lorsque vous êtes intéressé par un nœud DOM particulier, **Inspect** est un moyen rapide d’ouvrir devtools et d’examiner ce nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **inspecter un nœud**, cliquez avec le bouton droit sur **Michelangelo** , puis sélectionnez **inspecter**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecter un nœud" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Inspecter un nœud  
    :::image-end:::  
    
    1.  Le panneau **éléments** de devtools s’ouvre.  `<li>Michelangelo</li>` est mise en évidence dans l' **arborescence DOM**.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Mise en surbrillance du nœud Michelangelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Mettre en surbrillance le `Michelangelo` nœud  
        :::image-end:::  
        
        1.  **** ![ ][ImageInspectIcon] Dans le coin supérieur gauche de devtools, cliquez sur l’icône d’examen.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Icône Inspect" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Icône **Inspect**  
            :::image-end:::  
            
1.  Sous **inspecter un nœud**, cliquez sur le texte de **Tokyo** .  Est désormais `<li>Tokyo</li>` mis en surbrillance dans l’arborescence DOM.  

L’examen d’un nœud est également la première étape de l’affichage et de la modification des styles d’un nœud.  Naviguez jusqu’à la section [découvrir comment afficher et modifier des feuilles CSS][DevToolsCssGetStarted].  

### Parcourir l’arborescence DOM à l’aide d’un clavier  

Une fois que vous avez sélectionné un nœud dans l’arborescence DOM, vous pouvez parcourir l’arborescence DOM à l’aide de votre clavier.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **naviguez dans l’arborescence DOM à l’aide d’un clavier**, cliquez avec le bouton droit sur **Ringo** , puis sélectionnez **inspecter**.  `<li>Ringo</li>` est sélectionnée dans l’arborescence DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspectez le nœud Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Inspecter le `Ringo` nœud  
    :::image-end:::  
    
    1.  Appuyez sur la `Up` touche de direction 2 fois.  `<ul>`  est sélectionnée.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Examen du nœud UL" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Inspecter le `ul` nœud  
        :::image-end:::  
        
    1.  Appuyez sur la `Left` touche de direction.  La `<ul>` liste est réduite.  
    1.  Appuyez de `Left` nouveau sur la touche de direction.  Le parent du `<ul>` nœud est sélectionné.  Dans le cas présent, il s’agit de l' `<div>` ID with `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Appuyez `Down` deux fois sur la touche de direction pour que vous ayez sélectionné de nouveau la `<ul>` liste que vous venez de réduire.  Il doit se présenter comme suit: `<ul>... </ul>`  
    1.  Appuyez sur la `Right` touche de direction.  La liste est développée.  

### Faire défiler l’affichage  

Lors de l’affichage de l’arborescence DOM, il se peut que vous vous trouviez intéressé par un nœud DOM qui n’est pas disponible dans la fenêtre d’affichage.  Par exemple, supposons que vous faites défiler vers le bas de la page et que vous soyez intéressé par le `<h1>` nœud en haut de la page.  **Faire défiler dans l’affichage** vous permet de repositionner rapidement la fenêtre d’affichage pour pouvoir passer en revue le nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **défilement dans l’affichage**, cliquez avec le bouton droit sur **Magritte** , puis sélectionnez **inspecter**.  
1.  Faites défiler vers le bas de la page des exemples DOM.  
1.  Le `<li>Magritte</li>` nœud doit toujours être sélectionné dans votre arborescence DOM.  Si ce n’est pas le cas, revenez à la [fenêtre de défilement pour faire défiler](#scroll-into-view) le document.  
1.  Pointez sur le `<li>Magritte</li>` nœud, ouvrez le menu contextuel, puis sélectionnez **défilement dans l’affichage**.  Votre fenêtre d’affichage défile vers le haut pour que vous puissiez consulter le nœud **Magritte** .  Naviguez jusqu’à [l’annexe: options manquantes](#appendix-missing-options) si vous n’êtes pas en mesure de passer en revue l’option **défilement dans l’affichage** .
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Faire défiler l’affichage" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Faire défiler l’affichage**  
    :::image-end:::  

### Rechercher des nœuds  

Vous pouvez effectuer une recherche dans l’arborescence DOM par chaîne, sélecteur CSS ou sélecteur XPath.  

1.  Pointez votre curseur sur le panneau **éléments** .  
1.  Sélectionnez `Control` + `F` \ (Windows, Linux \) ou `Command` + `F` \ (MacOS \).  La barre de recherche s’ouvre en bas de l’arborescence DOM.  
1.  Entrez `The Moon is a Harsh Mistress`.  Dernière phrase mise en évidence dans l’arborescence DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Mettre en surbrillance la requête dans la barre de recherche" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Mettre en surbrillance la requête dans la barre de recherche  
    :::image-end:::  
    
Comme mentionné précédemment, la barre de recherche prend également en charge les sélecteurs de CSS et de XPath.  

## Modifier le DOM  

Vous pouvez modifier le DOM à la volée et passer en revue la façon dont les modifications affectent la page.  

### Modifier du contenu  

Pour modifier le contenu d’un nœud, double-cliquez sur le contenu de l’arborescence DOM.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **modifier le contenu**, cliquez avec le bouton droit sur **Michelle** , puis sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, double-cliquez `Michelle` .  En d’autres termes, double-cliquez sur le texte entre `<li>` et `</li>` .  Le texte est mis en surbrillance pour indiquer qu’il est sélectionné.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Modifier le texte" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Modifier le texte  
        :::image-end:::  
        
    1.  Supprimez `Michelle` , tapez `Leela` , puis sélectionnez `Enter` pour confirmer la modification.  Le texte du DOM passe de **Michelle** à **Leela**.  

### Modifier les attributs  

Pour modifier les attributs, double-cliquez sur le nom ou la valeur de l’attribut.  Suivez les instructions pour savoir comment ajouter des attributs à un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **modifier les attributs**, cliquez avec le bouton droit sur **Howard** , puis sélectionnez **inspecter**.  
1.  Double-cliquez sur `<li>` .  Le texte est mis en surbrillance pour indiquer que le nœud est sélectionné.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Modifier le nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Modifier le nœud  
    :::image-end:::  
    
1.  Appuyez sur la `Right` touche de direction, ajoutez un espace, tapez `style="background-color:gold"` , puis sélectionnez `Enter` .  La couleur d’arrière-plan du nœud devient or.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Ajouter un attribut de style au nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Ajouter un `style` attribut au nœud  
    :::image-end:::  
    
### Modifier le type de nœud  

Pour modifier le type d’un nœud, double-cliquez sur le type et tapez le nouveau type.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **modifier le type de nœud**, cliquez avec le bouton droit sur **Hank** , puis sélectionnez **inspecter**.  
    1.  Double-cliquez sur `<li>` .  Le texte `li` est mis en surbrillance.  
    1.  Supprimez `li` , tapez `button` , puis sélectionnez `Enter` .  Le `<li>` nœud devient un `<button>` nœud.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Changer le type de nœud en bouton" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Changer le type de nœud en `button`  
        :::image-end:::  
        
### Réorganiser les nœuds DOM  

Faites glisser les nœuds pour les réorganiser.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **Réorganiser les nœuds DOM**, cliquez avec le bouton droit sur **Elvis Presley** , puis sélectionnez **inspecter**.  
    
    > [!NOTE]
    > Il s’agit du dernier élément de la liste.  
    
    1.  Dans l’arborescence DOM, faites glisser `<li>Elvis Presley</li>` vers le haut de la liste.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Faites glisser le nœud vers le haut de la liste." lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Faites glisser le nœud vers le haut de la liste.  
        :::image-end:::  
        
### État de la force  

Vous pouvez imposer aux nœuds de rester dans des États, y compris,,, `:active` `:hover` `:focus` `:visited` et `:focus-within` .  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Dans **État**de l’état de force, pointez sur **le Seigneur du brusque**.  La couleur d’arrière-plan devient orange.  
    1.  Cliquez avec le bouton droit sur **la Seigneur du brusque** , puis sélectionnez **inspecter**.  
    1.  Cliquez avec le bouton droit `<li class="demo--hover">The Lord of the Flies</li>` de la souris et sélectionnez **forcer l’État**  >  **: hover**.  Accédez à [l’annexe: options manquantes](#appendix-missing-options) si l’option n’est pas affichée.  La couleur d’arrière-plan reste orange même si vous n’êtes pas en train de pointer sur le nœud.  

### Masquer un nœud  

Sélectionnez `H` pour masquer un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **masquer un nœud**, cliquez avec le bouton droit sur **les étoiles ma destination** et sélectionnez **inspecter**.  
    1.  Appuyez sur la `H` touche.  Le nœud est masqué.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Aspect du nœud dans l’arborescence DOM après son masquage" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Aspect du nœud dans l’arborescence DOM après son masquage  
        :::image-end:::  
        
    1.  Appuyez de `H` nouveau sur la touche.  Le nœud s’affiche à nouveau.  

### Supprimer un nœud  

Sélectionnez `Delete` pour supprimer un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **supprimer un nœud**, cliquez avec le bouton droit sur **Fondation** , puis sélectionnez **inspecter**.  
    1.  Appuyez sur la `Delete` touche.  Le nœud est supprimé.  
    1.  Sélectionnez `Control` + `Z` \ (Windows, Linux \) ou `Command` + `Z` \ (MacOS \).  La dernière action est déstablie et le nœud réapparaît.  

## Accéder aux nœuds de la console  

DevTools fournit plusieurs raccourcis pour accéder aux nœuds DOM à partir de la console ou pour obtenir des références JavaScript à chacun d’eux.  

### Faire référence au nœud actuellement sélectionné avec $0  

Lorsque vous examinez un nœud, le `== $0` texte en regard du nœud signifie que vous pouvez référencer ce nœud dans la console avec la variable `$0` .  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **faire référence au nœud actuellement sélectionné avec $0**, cliquez avec le bouton droit **de la main sur la gauche de l’obscurité** et sélectionnez **inspecter**.  
    1.  Appuyez sur la `Escape` touche pour ouvrir le tiroir de la console.  
    1.  Tapez `$0` , puis appuyez sur la `Enter` touche.  Le résultat de l’expression indique `$0` `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Résultat de la première expression $0 dans la console." lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Résultat de la première `$0` expression de la **console** .  
        :::image-end:::  
        
    1.  Positionnez le pointeur sur le résultat.  Le nœud est mis en surbrillance dans la fenêtre d’affichage.  
    1.  Cliquez `<li>Dune</li>` dans l’arborescence DOM, retapez `$0` la console, puis sélectionnez `Enter` à nouveau.  `$0`Évalue désormais `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Résultat de la deuxième expression $0 dans la console." lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Résultat de la deuxième `$0` expression de la **console** .  
        :::image-end:::  
        
### Store en tant que variable globale  

Si vous devez vous référer à un nœud à plusieurs reprises, stockez-le en tant que variable globale.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **stocker comme variable globale**, cliquez avec le bouton droit sur **la grande** mise en veille et sélectionnez **inspecter**.  
    1.  Cliquez avec le bouton droit `<li>The Big Sleep</li>` dans l’arborescence DOM et sélectionnez **stocker comme variable globale**.  Accédez à [l’annexe: options manquantes](#appendix-missing-options) si l’option n’est pas affichée.  
    1.  Entrez `temp1` dans la console et sélectionnez `Enter` .  Le résultat de l’expression indique que la variable est évaluée au nœud.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Résultat de l’expression temp1." lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Le résultat de l' `temp1` expression.  
        :::image-end:::  
        
### Copier le chemin d’accès JS  

Copiez le chemin d’accès JavaScript vers un nœud lorsque vous devez le référencer dans un test automatisé.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **copier le chemin d’accès js**, cliquez avec le bouton droit sur **le Karamazov de frères** et sélectionnez **inspecter**.  
    1.  `<li>The Brothers Karamazov</li>`Dans l’arborescence DOM, cliquez avec le bouton droit, puis sélectionnez **copier**le  >  **chemin d’accès js**.  Une `document.querySelector()` expression qui est résolue en nœud est copiée dans le presse-papiers.  
    1.  Sélectionnez `Control` + `V` \ (Windows, Linux \) ou `Command` + `V` \ (MacOS \) pour coller l’expression dans la console.  
    1.  `Enter`Pour évaluer l’expression.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Résultat de l’expression de chemin d’accès JS de copie" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Résultat de l’expression de **chemin d’accès js de copie**  
        :::image-end:::  
        
## Arrêt sur les modifications DOM  

DevTools vous permet de suspendre le JavaScript d’une page lorsque JavaScript modifie le DOM.  

### Annuler les modifications apportées aux attributs  

Utilisez des points d’arrêt de modification d’attribut lorsque vous souhaitez suspendre le JavaScript qui entraîne la modification des attributs d’un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Dans la section **arrêter la modification des attributs**, cliquez avec le bouton droit sur **sauerkraut** , puis sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Sauerkraut</li>` puis choisissez **arrêt sur**la  >  **modification des attributs**.  Accédez à [l’annexe: options manquantes](#appendix-missing-options) si l’option n’est pas affichée.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Annuler les modifications apportées aux attributs" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Annuler les modifications apportées aux attributs**  
        :::image-end:::  
        
    1.  Dans la prochaine étape, vous allez être invité à cliquer sur un bouton qui met en pause le code de la page.  Après l’interruption de la page, vous ne pouvez plus faire défiler la page.  Pour faire en **** sorte que ![ ][ImageResumeScriptIcon] la page puisse être défiler de nouveau, vous devez choisir l’un de ces scripts.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Où reprendre l’exécution du script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Où reprendre l’exécution du script  
        :::image-end:::  
        
    1.  Cliquez sur le bouton **définir l’arrière-plan** ci-dessus.  L' `style` attribut du nœud est alors défini sur `background-color:thistle` .  DevTools interrompt la page et met en surbrillance le code à l’origine du changement d’attribut.  
    1.  Sélectionnez **curriculum vitae** ( ![ script de reprise ][ImageResumeScriptIcon] \), comme mentionné précédemment.  
    
### Arrêt lors de la suppression du nœud  

Si vous souhaitez suspendre la suppression d’un nœud particulier, utilisez des points d’arrêt de suppression de nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **arrêt du nœud lors de la suppression du nœud**, cliquez avec le bouton droit sur **Neuromancer** , puis sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Neuromancer</li>` puis sélectionnez **interrompre lors de**la  >  **suppression du nœud**.  Accédez à [l’annexe: options manquantes](#appendix-missing-options) si l’option n’est pas affichée.  
    1.  Cliquez sur le bouton **supprimer** .  DevTools interrompt la page et met en surbrillance le code ayant entraîné la suppression du nœud.  
    1.  Sélectionnez **curriculum vitae** ( ![ script de reprise ][ImageResumeScriptIcon] \).  
    
### Modification de la sous-arborescence  

Après avoir placé un point d’arrêt de modification de sous-arborescence sur un nœud, DevTools interrompt la page lorsque l’un des descendants du nœud est ajouté ou supprimé.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **modifications de**la sous-arborescence, cliquez avec le bouton droit sur **un incendie en profondeur** et sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, cliquez avec le bouton droit `<ul id="target">` , qui correspond au nœud ci-dessus `<li>A Fire Upon the Deep</li>` , puis choisissez l’élément **saut de sous**-  >  **arborescence modifié**.  Accédez à [l’annexe: options manquantes](#appendix-missing-options) si l’option n’est pas affichée.  
    1.  Choisissez **Ajouter un enfant**.  Le code s’interrompt, car un `<li>` nœud a été ajouté à la liste.  
    1.  Sélectionnez **curriculum vitae** ( ![ script de reprise ][ImageResumeScriptIcon] \).  
    
## Étapes suivantes  

Ce qui couvre la plupart des fonctionnalités relatives au DOM dans DevTools.  Vous pouvez découvrir les autres options disponibles en cliquant avec le bouton droit sur les nœuds de l’arborescence DOM et en expérimentant les autres options qui n’ont pas été traitées dans ce didacticiel.  Accédez aux [raccourcis clavier du panneau d’éléments][DevToolsShortcutsElements].  

Consultez la [page d’accueil de Microsoft Edge devtools][MicrosoftEdgeDevTools] pour découvrir tout ce que vous pouvez faire avec devtools.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## Annexe: HTML et DOM  

La section suivante décrit rapidement la différence entre le code HTML et le DOM.  

:::row:::
   :::column span="":::
      Lorsque vous utilisez un navigateur Web pour demander une page, le serveur retourne du code HTML, comme dans l’extrait de code suivant.  

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
      Le navigateur analyse le code HTML et crée une arborescence d’objets, comme la liste suivante.  
      
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

Ce type d’arborescence d’objets ou de nœuds, qui représente le contenu de la page, est appelé le DOM.  

:::row:::
   :::column span="":::
      Dans le cas présent, le code HTML ressemble à ceci, mais supposez que le script référencé en bas du code HTML exécute l’extrait de code suivant.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Ce code supprime le `h1` nœud et ajoute un autre `p` nœud au DOM.  Le DOM complet affiche désormais la liste suivante.  
      
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

Le code HTML de la page est désormais différent du DOM.  En d’autres termes, HTML représente le contenu de page initial et le DOM représente le contenu de la page active.  Lorsque JavaScript ajoute, supprime ou modifie des nœuds, le DOM devient différent du code HTML.  

Accédez à [Présentation du DOM][MDNIntroductionToDOM] pour en savoir plus.  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and choose **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## Annexe: options manquantes  

La plupart des instructions de ce didacticiel vous demandent de cliquer avec le bouton droit sur un nœud dans l’arborescence DOM, puis de sélectionner une option dans le menu contextuel qui s’affiche.  Si l’option spécifiée dans le menu contextuel n’est pas affichée, cliquez avec le bouton droit en dehors du texte du nœud.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Où choisir si toutes les options ne sont pas affichées" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Où choisir si toutes les options ne sont pas affichées  
:::image-end:::  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge \ (chrome \) | Documents Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-panel-keyboard-shortcuts "Raccourcis clavier du panneau d’éléments-raccourcis clavier de Microsoft Edge DevTools | Documents Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemple de modèle DOM Microsoft Edge (chrome) DevTools Problème"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/dom/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
