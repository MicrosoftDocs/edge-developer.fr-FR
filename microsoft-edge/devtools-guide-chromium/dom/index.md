---
title: Découvrir comment afficher et modifier le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 4dee8b4e3ea927e72c0f98517f264b2c1d453013
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607446"
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

Ce didacticiel part du principe que vous connaissez la différence entre le DOM et le code HTML.  Pour obtenir une explication, voir [appendice: HTML et DOM](#appendix-html-versus-the-dom) .  

## Exemples d’ouverture de DOM  

1.  Maintenez `Control` la touche Windows enfoncée `Command` et cliquez sur les **exemples DOM** à ouvrir dans un nouvel onglet.  
    
    [Exemples DOM][GlitchDomExamples]  
    
## Afficher les nœuds DOM   

L’arborescence DOM du panneau éléments vous permet d’effectuer toutes les activités liées au DOM dans DevTools.  

### Inspecter un nœud   

Lorsque vous êtes intéressé par un nœud DOM particulier, **Inspect** est un moyen rapide d’ouvrir devtools et d’examiner ce nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **inspecter un nœud**, cliquez avec le bouton droit sur **Michelangelo** , puis sélectionnez **inspecter**.  
    
    > ##### Figure1  
    > Examen d’un nœud  
    > ![Examen d’un nœud][ImageInspectingNode]  
    
    1.  Le panneau **éléments** de devtools s’ouvre.  `<li>Michelangelo</li>` est mise en évidence dans l' **arborescence DOM**.  
        
        > ##### Figure 2  
        > Mise en surbrillance du nœud Michelangelo  
        > ![Mise en surbrillance du nœud Michelangelo][ImageHighlightingMichelangeloNode]  
        
        1.  Cliquez sur l’icône **Inspect** ![ Inspect ][ImageInspectIcon] située dans le coin supérieur gauche de devtools.  
            
            > ##### Figure3  
            > Icône Inspect  
            > ![Icône Inspect][ImageInspect]  
            
1.  Sous **inspecter un nœud**, cliquez sur le texte de **Tokyo** .  Est désormais `<li>Tokyo</li>` mis en surbrillance dans l’arborescence DOM.  

L’examen d’un nœud est également la première étape de l’affichage et de la modification des styles d’un nœud.  Voir [commencer à afficher et modifier des feuilles CSS][DevToolsCssGetStarted].  

### Parcourir l’arborescence DOM à l’aide d’un clavier   

Une fois que vous avez sélectionné un nœud dans l’arborescence DOM, vous pouvez parcourir l’arborescence DOM à l’aide de votre clavier.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **naviguez dans l’arborescence DOM à l’aide d’un clavier**, cliquez avec le bouton droit sur **Ringo** , puis sélectionnez **inspecter**.  `<li>Ringo</li>` est sélectionnée dans l’arborescence DOM.  
    
    > ##### Figure 4  
    > Examen du nœud Ringo  
    > ![Examen du nœud Ringo][ImageInspectingRingoNode]  
    
    1.  Appuyez sur la `Up` touche de direction 2 fois.  `<ul>`  est sélectionnée.  
        
        > ##### Figure 5  
        > Examen du nœud UL  
        > ![Examen du nœud UL][ImageInspectingUlNode]  
        
    1.  Appuyez sur la `Left` touche de direction.  La `<ul>` liste est réduite.  
    1.  Appuyez de `Left` nouveau sur la touche de direction.  Le parent du `<ul>` nœud est sélectionné.  Dans le cas présent, il s’agit de l' `<div>` ID with `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Appuyez `Down` deux fois sur la touche de direction pour que vous ayez sélectionné de nouveau la `<ul>` liste que vous venez de réduire.  Il doit se présenter comme suit: `<ul>... </ul>`  
    1.  Appuyez sur la `Right` touche de direction.  La liste est développée.  

### Faire défiler l’affichage   

Lors de l’affichage de l’arborescence DOM, il se peut que vous vous trouviez intéressé par un nœud DOM qui n’est pas disponible dans la fenêtre d’affichage.  Par exemple, supposons que vous faites défiler vers le bas de la page et que vous soyez intéressé par le `<h1>` nœud en haut de la page.  Le **défilement dans l’affichage** vous permet de repositionner rapidement la fenêtre d’affichage de manière à ce que vous puissiez voir le nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **défilement dans l’affichage**, cliquez avec le bouton droit sur **Magritte** , puis sélectionnez **inspecter**.  
1.  Faites défiler vers le bas de la page des exemples DOM.  
1.  Le `<li>Magritte</li>` nœud doit toujours être sélectionné dans votre arborescence DOM.  Si ce n’est pas le cas, revenez à la [fenêtre de défilement pour faire défiler](#scroll-into-view) le document.  
1.  Cliquez avec le bouton droit sur le `<li>Magritte</li>` nœud et sélectionnez **défilement dans l’affichage**.  Votre fenêtre d’affichage défile vers le haut pour que le nœud **Magritte** puisse s’afficher.  Voir [appendice: options manquantes](#appendix-missing-options) si vous n’êtes pas en mesure d’afficher l’option **défilement dans l’affichage** .
    
    > ##### Figure 6  
    > Faire défiler l’affichage  
    > ![Faire défiler l’affichage][ImageScrollView]  

### Rechercher des nœuds   

Vous pouvez effectuer une recherche dans l’arborescence DOM par chaîne, sélecteur CSS ou sélecteur XPath.  

1.  Pointez votre curseur sur le panneau **éléments** .  
1.  Appuyez sur `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \).  La barre de recherche s’ouvre en bas de l’arborescence DOM.  
1.  Entrez `The Moon is a Harsh Mistress`.  Dernière phrase mise en évidence dans l’arborescence DOM.  
    
    > ##### Figure 7  
    > Mise en surbrillance de la requête dans la barre de recherche  
    > ![Mise en surbrillance de la requête dans la barre de recherche][ImageHighlightingQuerySearchBar]  
    
Comme mentionné précédemment, la barre de recherche prend également en charge les sélecteurs de CSS et de XPath.  

## Modifier le DOM   

Vous pouvez modifier le DOM à la volée et constater l’incidence de ces modifications sur la page.  

### Modifier du contenu   

Pour modifier le contenu d’un nœud, double-cliquez sur le contenu de l’arborescence DOM.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **modifier le contenu**, cliquez avec le bouton droit sur **Michelle** , puis sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, double-cliquez `Michelle` .  En d’autres termes, double-cliquez sur le texte entre `<li>` et `</li>` .  Le texte est mis en surbrillance pour indiquer qu’il est sélectionné.  
        
        > ##### Figure8  
        > Modification du texte  
        > ![Modification du texte][ImageEditingText]  
        
    1.  Supprimez `Michelle` , tapez `Leela` , puis appuyez sur `Enter` pour confirmer la modification.  Le texte du DOM passe de **Michelle** à **Leela**.  

### Modifier les attributs   

Pour modifier les attributs, double-cliquez sur le nom ou la valeur de l’attribut.  Suivez les instructions pour savoir comment ajouter des attributs à un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **modifier les attributs**, cliquez avec le bouton droit sur **Howard** et sélectionnez **inspecter**.  

1.  Double-cliquez sur `<li>` .  Le texte est mis en surbrillance pour indiquer que le nœud est sélectionné.  
    
    > ##### Figure9  
    > Modification du nœud  
    > ![Modification du nœud][ImageEditingNode]  
    
1.  Appuyez sur la `Right` touche de direction, ajoutez un espace, tapez le texte `style="background-color:gold"` et appuyez sur `Enter` .  La couleur d’arrière-plan du nœud devient or.  
    
    > ##### Figure10  
    > Ajouter un attribut de style au nœud  
    > ![Ajouter un attribut de style au nœud][ImageAddingStyleAttributeNode]  
    
### Modifier le type de nœud   

Pour modifier le type d’un nœud, double-cliquez sur le type et tapez le nouveau type.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **modifier le type de nœud**, cliquez avec le bouton droit sur **Hank** , puis sélectionnez **inspecter**.  
    1.  Double-cliquez sur `<li>` .  Le texte `li` est mis en surbrillance.  
    1.  Suppr `li` , type `button` , puis appuyez sur `Enter` .  Le `<li>` nœud devient un `<button>` nœud.  
        
        > ##### Figure11  
        > Changer le type de nœud en Button  
        > ![Changer le type de nœud en Button][ImageChangingNodeButton]  
        
### Réorganiser les nœuds DOM   

Faites glisser les nœuds pour les réorganiser.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **Réorganiser les nœuds DOM**, cliquez avec le bouton droit sur **Elvis Presley** , puis sélectionnez **inspecter**.  
    
    > [!NOTE]
    > Il s’agit du dernier élément de la liste.  
    
    1.  Dans l’arborescence DOM, faites glisser `<li>Elvis Presley</li>` vers le haut de la liste.  
        
        > ##### Figure12  
        > Glissement du nœud vers le haut de la liste  
        > ![Glissement du nœud vers le haut de la liste][ImageDraggingNodeTopList]  
        
### État de la force   

Vous pouvez imposer aux nœuds de rester dans des États, y compris,,, `:active` `:hover` `:focus` `:visited` et `:focus-within` .  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Dans **État**de l’état de force, pointez sur **le Seigneur du brusque**.  La couleur d’arrière-plan devient orange.  
    1.  Cliquez avec le bouton droit sur **le Seigneur du brusque** et sélectionnez **inspecter**.  
    1.  Cliquez avec le bouton droit `<li class="demo--hover">The Lord of the Flies</li>` de la souris et sélectionnez **forcer l’État**  >  **: hover**.  Voir [annexe: options manquantes](#appendix-missing-options) si vous ne voyez pas cette option.  La couleur d’arrière-plan reste orange même si vous n’êtes pas en train de pointer sur le nœud.  

### Masquer un nœud   

Appuyez `H` pour masquer un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **masquer un nœud**, cliquez avec le bouton droit sur **l’étoile** et sélectionnez **inspecter**.  
    1.  Appuyez sur la `H` touche.  Le nœud est masqué.  
        
        > ##### Figure13  
        > Aspect du nœud dans l’arborescence DOM après son masquage  
        > ![Aspect du nœud dans l’arborescence DOM après son masquage][ImageNodeDomTreeAfterHidden]  
        
    1.  Appuyez de `H` nouveau sur la touche.  Le nœud s’affiche à nouveau.  

### Supprimer un nœud   

Appuyez `Delete` pour supprimer un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **supprimer un nœud**, cliquez avec le bouton droit sur **base** , puis sélectionnez **inspecter**.  
    1.  Appuyez sur la `Delete` touche.  Le nœud est supprimé.  
    1.  Appuyez sur `Control` + `Z` \ (Windows \) ou `Command` + `Z` \ (MacOS \).  La dernière action est déstablie et le nœud réapparaît.  

## Accéder aux nœuds de la console   

DevTools fournit plusieurs raccourcis pour accéder aux nœuds DOM à partir de la console ou pour obtenir des références JavaScript à chacun d’eux.  

### Faire référence au nœud actuellement sélectionné avec $0   

Lorsque vous examinez un nœud, le `== $0` texte en regard du nœud signifie que vous pouvez référencer ce nœud dans la console avec la variable `$0` .  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **faire référence au nœud actuellement sélectionné avec $0**, cliquez avec le bouton droit sur **la gauche de l’obscurité** et sélectionnez **inspecter**.  
    1.  Appuyez sur la `Escape` touche pour ouvrir le tiroir de la console.  
    1.  Tapez `$0` , puis appuyez sur la `Enter` touche.  Le résultat de l’expression indique `$0` `<li>The Left Hand of Darkness</li>` .  
        
        > ##### Figure14  
        > Résultat de la première `$0` expression de la console.  
        > ![Résultat de la première expression $0 dans la console.][ImageFirstConsole]  
        
    1.  Positionnez le pointeur sur le résultat.  Le nœud est mis en surbrillance dans la fenêtre d’affichage.  
    1.  Cliquez `<li>Dune</li>` dans l’arborescence DOM, tapez `$0` de nouveau la console, puis appuyez de `Enter` nouveau.  `$0`Évalue désormais `<li>Dune</li>` .  
        
        > ##### Figure15  
        > Résultat de la deuxième `$0` expression dans la console, ![ le résultat de la deuxième expression $0 de la console.][ImageSecondConsole]  
        
### Store en tant que variable globale   

Si vous devez vous référer à un nœud à plusieurs reprises, stockez-le en tant que variable globale.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **stocker comme variable globale**, cliquez avec le bouton droit sur **la grande** mise en veille et sélectionnez **inspecter**.  
    1.  Cliquez avec le bouton droit `<li>The Big Sleep</li>` dans l’arborescence DOM et sélectionnez **Store As global variable**.  Voir [annexe: options manquantes](#appendix-missing-options) si vous ne voyez pas cette option.  
    1.  Entrez `temp1` dans la console et appuyez sur `Enter` .  Le résultat de l’expression indique que la variable est évaluée au nœud.  
        
        > ##### Figure16  
        > Résultat de l’expression temp1.  
        > ![Résultat de l’expression temp1.][ImageResultTemp1]  
        
### Copier le chemin d’accès JS   

Copiez le chemin d’accès JavaScript vers un nœud lorsque vous devez le référencer dans un test automatisé.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **Copy js Path**, cliquez avec le bouton droit sur **l’Karamazov frères** et sélectionnez **inspecter**.  
    1.  `<li>The Brothers Karamazov</li>`Dans l’arborescence DOM, cliquez avec le bouton droit, puis sélectionnez **copier**le  >  **chemin d’accès js**.  Une `document.querySelector()` expression qui est résolue en nœud est copiée dans le presse-papiers.  
    1.  Appuyez sur `Control` + `V` \ (Windows \) ou `Command` + `V` \ (MacOS \) pour coller l’expression dans la console.  
    1.  Appuyez `Enter` pour évaluer l’expression.
        
        > ##### Figure17  
        > Résultat de l’expression de chemin d’accès JS de copie  
        > ![Résultat de l’expression de chemin d’accès JS de copie][ImageResultCopyJSPath]  
        
## Arrêt sur les modifications DOM   

DevTools vous permet de suspendre le JavaScript d’une page lorsque JavaScript modifie le DOM.  

### Annuler les modifications apportées aux attributs   

Utilisez des points d’arrêt de modification d’attribut lorsque vous souhaitez suspendre le JavaScript qui entraîne la modification des attributs d’un nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Dans la section **arrêter la modification des attributs**, cliquez avec le bouton droit sur **sauerkraut** , puis sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Sauerkraut</li>` puis sélectionnez **arrêter de**  >  **modifier les attributs**.  Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.
        
        > ##### Figure 18  
        > Annuler les modifications apportées aux attributs  
        > ![Annuler les modifications apportées aux attributs][ImageBreakAttributeModification]  
        
    1.  Dans la prochaine étape, vous allez être invité à cliquer sur un bouton qui met en pause le code de la page.  Après l’interruption de la page, vous ne pouvez plus faire défiler la page.  **Resume Script** ![ ][ImageResumeScriptIcon] Pour pouvoir faire défiler la page, vous devez cliquer sur curriculum vitae du script de reprise.
        
        > ##### Figure 19  
        > Où reprendre l’exécution du script  
        > ![Où reprendre l’exécution du script][ImageResumeScript]  
        
    1.  Cliquez sur le bouton **définir l’arrière-plan** ci-dessus.  L' `style` attribut du nœud est alors défini sur `background-color:thistle` .  DevTools interrompt la page et met en surbrillance le code à l’origine du changement d’attribut.  
    1.  Cliquez sur reprendre le script de reprise de **script** ![ ][ImageResumeScriptIcon] , comme mentionné plus haut.  
    
### Arrêt lors de la suppression du nœud   

Si vous souhaitez suspendre la suppression d’un nœud particulier, utilisez des points d’arrêt de suppression de nœud.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Sous **arrêt du nœud lors de la suppression du nœud**, cliquez avec le bouton droit sur **Neuromancer** , puis sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Neuromancer</li>` puis sélectionnez **arrêter lors de**la  >  **suppression du nœud**.  Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.  
    1.  Cliquez sur le bouton **supprimer** .  DevTools interrompt la page et met en surbrillance le code ayant entraîné la suppression du nœud.  
    1.  Cliquez sur reprendre le script de reprise de **script** ![ ][ImageResumeScriptIcon] .  
    
### Modification de la sous-arborescence   

Après avoir placé un point d’arrêt de modification de sous-arborescence sur un nœud, DevTools interrompt la page lorsque l’un des descendants du nœud est ajouté ou supprimé.  

1.  [Ouvrir des exemples DOM](#open-dom-examples).  
1.  Dans **modifications de**la sous-arborescence, cliquez avec le bouton droit sur **un feu sur le** côté et sélectionnez **inspecter**.  
    1.  Dans l’arborescence DOM, cliquez avec le bouton droit `<ul id="target">` , qui correspond au nœud ci-dessus `<li>A Fire Upon the Deep</li>` , puis sélectionnez l’option **arrêter**la modification de la sous-  >  **arborescence**.  Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.  
    1.  Cliquez sur **Ajouter un enfant**.  Le code s’interrompt, car un `<li>` nœud a été ajouté à la liste.  
    1.  Cliquez sur reprendre le script de reprise de **script** ![ ][ImageResumeScriptIcon] .  
    
## Étapes suivantes   

Ce qui couvre la plupart des fonctionnalités relatives au DOM dans DevTools.  Vous pouvez découvrir les autres options disponibles en cliquant avec le bouton droit sur les nœuds de l’arborescence DOM et en expérimentant les autres options qui n’ont pas été traitées dans ce didacticiel.  Voir aussi [raccourcis clavier du panneau éléments][DevToolsShortcutsElements].  

Consultez la [page d’accueil de Microsoft Edge devtools][MicrosoftEdgeDevTools] pour découvrir tout ce que vous pouvez faire avec devtools.  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## Annexe: HTML et DOM   

Cette section décrit rapidement la différence entre le code HTML et le DOM.  

Lorsque vous utilisez un navigateur Web pour demander une page, le serveur renvoie le code HTML comme suit:  

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

Le navigateur analyse le code HTML et crée une arborescence d’objets comme suit:  

```dom
html
  head
    title
  body
    h1
    p
    script
```  

Ce type d’arborescence d’objets ou de nœuds, qui représente le contenu de la page, est appelé le DOM.  Dans le cas présent, le code HTML ressemble à ceci, mais supposez que le script référencé en bas du code HTML exécute ce code:  

```javascript
const h1 = document.querySelector('h1');
h1.parentElement.removeChild(h1);
const p = document.createElement('p');
p.textContent = 'Wildcard!';
document.body.appendChild(p);
```  

Ce code supprime le `h1` nœud et ajoute un autre `p` nœud au DOM.  Le DOM complet se présente désormais comme suit:  

```dom
html
  head
    title
  body
    p
    script
    p
```  

Le code HTML de la page est désormais différent du DOM.  En d’autres termes, HTML représente le contenu de page initial et le DOM représente le contenu de la page active.  Lorsque JavaScript ajoute, supprime ou modifie des nœuds, le DOM devient différent du code HTML.  

Pour en savoir plus, voir [Présentation du DOM][MDNIntroductionToDOM] .  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > ![Scroll into view][ImageScrollView]  
    -->  

## Annexe: options manquantes   

La plupart des instructions de ce didacticiel vous demandent de cliquer avec le bouton droit sur un nœud dans l’arborescence DOM, puis de sélectionner une option dans le menu contextuel qui s’affiche.  Si vous ne voyez pas l’option spécifiée dans le menu contextuel, effectuez un clic droit en dehors du texte du nœud.  

> ##### Figure 20  
> Où cliquer pour afficher toutes les options  
> ![Où cliquer pour afficher toutes les options][ImageNotSeeingAllOptions]  

<!-- image links -->  

[ImageInspectIcon]: /microsoft-edge/devtools-guide-chromium/media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-icon.msft.png  

[ImageInspectingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-inspect.msft.png "Figure 1: examen d’un nœud"  
[ImageHighlightingMichelangeloNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png "Figure 2: mise en surbrillance du nœud Michelangelo"  
[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-select-element-page-inspect.msft.png "Figure 3: icône inspecter"  
[ImageInspectingRingoNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png "Figure 4: examen du nœud Ringo"  
[ImageInspectingUlNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png "Figure 5: examen du nœud UL"  
[ImageScrollView]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png "Figure 6: défilement dans l’affichage"  
[ImageHighlightingQuerySearchBar]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-search-nodes-highlight.msft.png "Figure 7: mise en surbrillance de la requête dans la barre de recherche"  
[ImageEditingText]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-content.msft.png "Figure 8: modification du texte"  
[ImageEditingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-highlighted.msft.png "Figure 9: modification du nœud"  
[ImageAddingStyleAttributeNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-inline-css.msft.png "Figure 10: ajouter un attribut de style au nœud"  
[ImageChangingNodeButton]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-node-type-button.msft.png "Figure 11: changer le type de nœud en bouton"  
[ImageDraggingNodeTopList]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-reorder-dom-nodes.msft.png "Figure 12: glissement du nœud vers le haut de la liste"  
[ImageNodeDomTreeAfterHidden]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-hide-a-node.msft.png "Figure 13: apparence du nœud dans l’arborescence DOM après son masquage"  
[ImageFirstConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png "Figure 14: résultat de la première expression $0 dans la console"  
[ImageSecondConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png "Figure 15: résultat de la deuxième expression $0 dans la console"  
[ImageResultTemp1]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png "Figure 16: résultat de l’expression Temp1"  
[ImageResultCopyJSPath]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png "Figure 17: résultat de l’expression de chemin d’accès JS de copie"  
[ImageBreakAttributeModification]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png "Figure 18: arrêt du changement d’attribut"  
[ImageResumeScript]: /microsoft-edge/devtools-guide-chromium/media/dom-break-attribute-modifications-sources-paused-on.msft.png "Figure 19: emplacement de reprise de l’exécution du script"  
[ImageNotSeeingAllOptions]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-right-click-right-side.msft.png "Figure 20: cliquez sur l’emplacement où cliquer pour afficher toutes les options"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge \ (chrome \)"  
[DevToolsCssGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  
[DevToolsShortcutsElements]: /microsoft-edge/devtools-guide-chromium/shortcuts#elements-panel-keyboard-shortcuts "Raccourcis clavier du panneau d’éléments-raccourcis clavier de Microsoft Edge DevTools"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemple de modèle DOM Microsoft Edge (chrome) DevTools Problème"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/dom/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
