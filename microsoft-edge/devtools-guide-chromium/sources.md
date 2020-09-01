---
title: Vue d’ensemble du volet sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 469e4c3d8707379f5f41f072d31e2f7a5669651d
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984349"
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







# Présentation du panneau sources 



Utilisez le volet de **sources** de Microsoft Edge devtools pour effectuer les actions ci-dessous.  

*   [Afficher les fichiers](#view-files).  
*   [Modifiez les feuilles CSS et JavaScript](#edit-css-and-javascript).  
*   [Créez et enregistrez des **extraits** de code JavaScript](#create-save-and-run-snippets), que vous pouvez exécuter sur n’importe quelle page.  Les **extraits** sont similaires aux bookmarklets.  
*   [Déboguer JavaScript](#debug-javascript).  
*   [Configurez un espace de travail](#set-up-a-workspace)de telle sorte que les modifications que vous apportez dans devtools soient enregistrées dans le code de votre système de fichiers.  
    
## Afficher les fichiers 

Utilisez le volet **page** pour afficher toutes les ressources que la page a chargées.

:::image type="complex" source="./media/sources-page-pane.msft.png" alt-text="Volet pages" lightbox="./media/sources-page-pane.msft.png":::
   Volet **pages**  
:::image-end:::  

Organisation de la **page** :  
*   Le niveau supérieur, tel que `top` dans l’illustration précédente, représente un [cadre html][W3CHtml4Frames].  Recherchez `top` sur chaque page visitée.  `top` représente le cadre du document principal.  
*   Le second niveau, tel que `docs.microsoft.com` dans l’illustration précédente, représente une [origine][HtmlstandardOrigin].  
*   Le troisième niveau, le quatrième niveau, etc., représentent les répertoires et les ressources qui ont été chargés depuis cette origine.  Par exemple, dans l’illustration précédente, le chemin d’accès complet à la ressource `devtools-guide-chromium` est `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Cliquez sur un fichier dans le volet de **page** pour afficher le contenu dans le volet **éditeur** .  Il est possible que vous voyiez un type de fichier.  Pour les images, un aperçu de l’image s’affiche.  

:::image type="complex" source="./media/sources-editor-pane.msft.png" alt-text="Afficher le contenu de a4d10f71.index-docs.js dans le volet éditeur" lightbox="./media/sources-editor-pane.msft.png":::
   Afficher le contenu de `a4d10f71.index-docs.js` dans le volet **éditeur**  
:::image-end:::  

## Modifier CSS et JavaScript 

Utilisez le volet **éditeur** pour modifier les feuilles CSS et JavaScript.  DevTools met à jour la page pour exécuter votre nouveau code.  Par exemple, si vous modifiez un fichier CSS en ajoutant la règle de style ci-dessous:

```css
.metadata.page-metadata {
    color: red;
}
```

Vous devez voir que cette modification prend effet immédiatement.

:::image type="complex" source="./media/edit-css.msft.png" alt-text="Modification de CSS dans le volet éditeur pour changer la couleur du texte du sous-titre en rouge" lightbox="./media/edit-css.msft.png":::
   Modification de CSS dans le volet **éditeur** pour changer la couleur du texte du sous-titre en rouge  
:::image-end:::  

Les modifications apportées aux feuilles de style CSS sont immédiatement appliquées, sans enregistrement nécessaires.  Pour que les modifications JavaScript soient prises en compte, appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \).  DevTools ne réexécute pas de script, les seules modifications JavaScript qui prennent effet sont celles que vous effectuez dans les fonctions.  Par exemple, dans l’illustration suivante, vous remarquerez que le fonctionnement `console.log('A')` ne fonctionne pas `console.log('B')` .  Si DevTools réexécute le script entier après avoir apporté la modification, le texte `A` aurait été enregistré dans la **console**.  

:::image type="complex" source="./media/edit-js.msft.png" alt-text="Modification de JavaScript dans le volet éditeur" lightbox="./media/edit-js.msft.png":::
   Modification de JavaScript dans le volet **éditeur**  
:::image-end:::  

DevTools efface vos modifications CSS et JavaScript lorsque vous rechargez la page.  Pour savoir comment enregistrer les modifications apportées à votre système de fichiers, voir [configurer un espace de travail](#set-up-a-workspace) .  

## Création, enregistrement et exécution d’extraits de fichier 

Les extraits sont des scripts que vous pouvez exécuter sur n’importe quelle page.  Imaginez que vous entrez le code suivant à plusieurs reprises dans la **console**pour insérer la bibliothèque jQuery dans une page, de sorte que vous puissiez exécuter des commandes jQuery à partir de la **console**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Au lieu de cela, vous pouvez enregistrer ce code dans un **extrait** de code et l’exécuter en quelques clics sur le bouton, chaque fois que vous en avez besoin.  DevTools enregistre l' **extrait** de fichier dans votre système de fichiers.  

:::image type="complex" source="./media/snippet.msft.png" alt-text="Extrait de la bibliothèque jQuery insérée dans une page" lightbox="./media/snippet.msft.png":::
   **Extrait** de la bibliothèque jQuery insérée dans une page  
:::image-end:::  

Pour exécuter un **Snippet**:

*   Ouvrez le fichier à l’aide du volet **snippets** , puis cliquez sur **exécuter** \ ( ![ le bouton exécuter ][ImageRunIcon] \).  
*   Ouvrez le **[menu de commandes][DevtoolsGuideChromiumCommandMenuIndex]**, supprimez le `>` caractère, tapez `!` le nom de votre **extrait**de texte, puis appuyez sur `Enter` .  
    
Pour en savoir plus, voir [exécution d’extraits de code à partir de n’importe quelle page][DevtoolsGuideChromiumJavascriptSnippets] .

## Déboguer JavaScript 

Au lieu `console.log()` d’utiliser pour induire l’endroit où votre code JavaScript ne pose pas de problème, envisagez plutôt d’utiliser les outils de débogage de Microsoft Edge devtools.  L’idée générale consiste à définir un point d’arrêt, qui est un point d’arrêt intentionnel dans votre code, et à parcourir le runtime de votre code, une ligne à la fois.  Lorsque vous parcourez le code, vous pouvez afficher et modifier les valeurs de toutes les propriétés et variables actuellement définies, exécuter JavaScript dans la **console**, etc.

Pour plus d’informations sur les concepts de base du débogage dans DevTools, voir [prendre en main le débogage de code JavaScript][DevtoolsGuideChromiumJavascriptIndex] .

:::image type="complex" source="./media/debugging.msft.png" alt-text="Déboguer JavaScript" lightbox="./media/debugging.msft.png":::
   Déboguer JavaScript  
:::image-end:::  

## Configurer un espace de travail 

Par défaut, lorsque vous modifiez un fichier dans le panneau **sources** , les modifications correspondantes sont perdues lorsque vous rechargez la page.  Les **espaces de travail** vous permettent d’enregistrer les modifications que vous apportez dans devtools à votre système de fichiers.  Fondamentalement, DevTools peut être utilisé en tant qu’éditeur de code.

Pour commencer, voir [modifier des fichiers avec des espaces de travail][DevtoolsGuideChromiumWorkspacesIndex] .

<!--  
 


-->  

<!-- image links -->  

[ImageRunIcon]: ./media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ./command-menu/index.md "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: ./javascript/index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: ./javascript/snippets.md "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: ./workspaces/index.md "Modifier des fichiers avec des espaces de travail"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origine-norme HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Images | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/sources) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
