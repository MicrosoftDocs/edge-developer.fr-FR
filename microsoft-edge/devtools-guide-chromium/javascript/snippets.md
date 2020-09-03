---
description: Les extraits sont des petits scripts que vous pouvez créer et exécuter dans le panneau sources de Microsoft Edge DevTools.  Vous pouvez y accéder et l’exécuter à partir de n’importe quelle page.  Lorsque vous exécutez un snippet, il s’exécute à partir du contexte de la page actuellement ouverte.
title: Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5f6284179aacb471116a2d732507b010c37ef235
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993386"
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





# Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools   



Si vous vous trouvez vous utilisez le même code dans la [console][DevtoolsConsoleIndex] à plusieurs reprises, envisagez plutôt d’enregistrer le code en tant qu’extrait.  Les extraits sont des scripts que vous créez dans le panneau [sources][DevToolsSourcesPanel] .  Ils ont accès au contexte JavaScript de la page et vous pouvez les exécuter sur n’importe quelle page.  Les extraits de vue sont une alternative aux [bookmarklets][WikiBookmarklet].  
Firefox DevTools possède une fonctionnalité semblable à celle des extraits de blocs- [Notes][MDNScratchpad].  

Par exemple, dans la figure suivante, la page d’accueil DevTools sur la gauche et le code source de l’extrait de code à droite.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aspect de la page avant d’exécuter l’extrait de page" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   Aspect de la page avant d’exécuter l’extrait de page  
:::image-end:::  

Code source de l’extrait de code de la figure précédente.  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

Dans l’illustration suivante, la page s’affiche après l’exécution de l’extrait de code.  Le **tiroir** de la console s’affiche pour afficher le `Hello, Snippets!` message indiquant que le Snippet enregistre les journaux et le contenu de la page est totalement modifié.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aspect de la page après avoir exécuté l’extrait" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Aspect de la page après avoir exécuté l’extrait  
:::image-end:::  

## Ouvrir le volet d’extraits   

Le volet d' **extraits** de liste répertorie vos extraits.  Lorsque vous voulez modifier un extrait de rapport, vous devez l’ouvrir à partir du volet **extraits** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Volet Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Volet **snippets**  
:::image-end:::  

### Ouvrir le volet des fragments de fenêtre à l’aide d’une souris   

1.  Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .  Le volet **page** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Panneau sources avec le volet page ouvert à gauche" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Panneau **sources** avec le volet **page** ouvert à gauche  
    :::image-end:::  
    
1.  Cliquez sur l’onglet **extraits** de vue pour ouvrir le volet d' **extraits** .  Vous devrez peut-être cliquer sur **autres onglets** \ ( ![ plus d’onglets ][ImageMoreTabsIcon] \) pour accéder à l’option **extraits** de vue.  
    
### Ouvrir le volet d’extraits de fenêtre à l’aide du menu de commandes   

1.  Focalisez votre curseur à l’intérieur du DevTools.  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Commencez `Snippets` à taper, sélectionnez **afficher les extraits**de texte, puis appuyez sur `Enter` pour exécuter la commande.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Commande Afficher les extraits" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Commande **afficher les extraits**  
    :::image-end:::  
    
## Créer des extraits de   

### Créer un snippet via le volet sources   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez sur **nouvel extrait**.  
1.  Entrez le nom de votre snippet, puis appuyez sur `Enter` Enregistrer.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nommer un snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nommer un snippet  
    :::image-end:::  
    
### Créer un snippet via le menu de commandes   

1.  Focalisez votre curseur à l’intérieur du DevTools.  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Commencez `Snippet` à taper, sélectionnez **créer un nouveau Snippet**, puis appuyez sur `Enter` pour exécuter la commande.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Commande de création d’un nouveau Snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Commande de création d’un nouveau Snippet  
    :::image-end:::  
    
Voir [Renommer des extraits de nom](#rename-snippets) si vous souhaitez attribuer un nom personnalisé à votre nouveau snippet.  

## Modifier des extraits de ce profil   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Dans le volet d' **extraits** de code, cliquez sur le nom de l’extrait que vous souhaitez modifier pour l’ouvrir dans l' **éditeur de code**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Éditeur de code" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       **Éditeur de code**  
    :::image-end:::  
    
1.  Utilisez l' **éditeur de code** pour ajouter du JavaScript à votre snippet.  
1.  Lorsqu’un astérisque apparaît en regard du nom de votre snippet, cela signifie que vous avez du code non enregistré. Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré.  
    :::image-end:::  
    
## Exécuter des Snippets   

### Exécuter un snippet à partir du panneau sources   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez sur le nom de l’extrait que vous souhaitez exécuter.  L’extrait de code s’ouvre dans l' **éditeur de code**.  
1.  Cliquez sur **exécuter le Snippet** \ (exécuter l’extrait de passe ![ ][ImageRunSnippetIcon] \) ou appuyez sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).  
    
### Exécuter un extrait de commande avec le menu de commandes   

1.  Focalisez votre curseur à l’intérieur du DevTools.  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Supprimez le `>` caractère et tapez le `!` caractère suivi du nom de l’extrait que vous voulez exécuter.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Exécution d’un snippet à partir du menu de commandes" lightbox="../media/javascript-search-run-command.msft.png":::
       Exécution d’un snippet à partir du **menu de commandes**  
    :::image-end:::  
    
1.  Appuyez `Enter` pour exécuter l’extrait de.  

## Renommer des extraits de nom   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **Renommer**.  
    
## Supprimer des extraits de   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **supprimer**.  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Présentation du panneau sources | Documents Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc-notes | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
