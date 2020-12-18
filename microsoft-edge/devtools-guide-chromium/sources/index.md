---
description: Afficher et modifier des fichiers, créer des extraits de code, déboguer JavaScript et configurer des espaces de travail dans le panneau sources de Microsoft Edge DevTools.
title: Vue d’ensemble du volet Sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b90f927670146c004a335256ace28203219442eb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232944"
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

# Vue d’ensemble du volet Sources  

Utilisez le volet **sources** de Microsoft Edge DevTools pour effectuer ces actions.  

*   [Afficher les fichiers](#display-files).  
*   [Modifier les feuilles CSS et JavaScript](#edit-css-and-javascript).  
*   [Créez et enregistrez des **extraits** de code JavaScript](#create-save-and-run-snippets), que vous pouvez exécuter sur n’importe quelle page Web.  **Les extraits de code** sont similaires aux bookmarklets.  
*   [Déboguer JavaScript](#debug-javascript).  
*   [Configurer un espace de travail](#set-up-a-workspace)de telle sorte que les modifications que vous apportez dans DevTools soient enregistrées dans le code de votre système de fichiers.  
    
## Afficher des fichiers  

Utilisez le volet **page** pour afficher toutes les ressources que la page a chargées.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Le volet des pages" lightbox="../media/sources-page-pane.msft.png":::
   Le volet des **pages**  
:::image-end:::  

Organisation du volet des **pages** :  
*   Le niveau supérieur, tel que `top` dans l’illustration précédente, représente un [cadre HTML][W3CHtml4Frames].  Recherchez `top` sur chaque page visitée.  `top` représente le cadre du document principal.  
*   Le second niveau, tel que `docs.microsoft.com` dans l’illustration précédente, représente une [origine][HtmlstandardOrigin].  
*   Le troisième niveau, le quatrième niveau ainsi de suite, représentent les répertoires et les ressources qui ont été chargés depuis cette origine.  Par exemple, dans l’illustration précédente, le chemin d’accès complet à la ressource `devtools-guide-chromium` est `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Pour afficher le contenu dans le volet **éditeur** , sélectionnez un fichier dans le volet de la **page** .  Vous pouvez afficher n’importe quel type de fichier.  Pour les images, un aperçu de l’image est affiché.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Afficher le contenu de a4d10f71.index-docs.js dans le volet éditeur" lightbox="../media/sources-editor-pane.msft.png":::
   Afficher le contenu de `a4d10f71.index-docs.js` dans le volet **éditeur**  
:::image-end:::  

## Modifier CSS et JavaScript  

Utilisez le volet **éditeur** pour modifier les feuilles CSS et JavaScript.  DevTools met à jour la page pour exécuter votre nouveau code.  Par exemple, si vous modifiez un fichier CSS en ajoutant la règle de style ci-dessous:

```css
.metadata.page-metadata {
    color: red;
}
```

Cette modification doit prendre effet immédiatement.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Modification de CSS dans le volet éditeur pour modifier la couleur du texte du sous-titre en rouge" lightbox="../media/edit-css.msft.png":::
   Modification de CSS dans le volet **éditeur** pour modifier la couleur du texte du sous-titre en rouge  
:::image-end:::  

Les modifications apportées aux feuilles CSS sont immédiatement appliquées, sans enregistrement.  Pour que les modifications JavaScript soient appliquées, sélectionnez `Control`+`S` \ (Windows, Linux \) ou `Command`+`S` \ (MacOS \).  DevTools ne ré-exécute pas de script, les seules modifications JavaScript qui prennent effet sont celles que vous effectuez dans les fonctions.  Par exemple, dans l’illustration suivante, vous remarquerez que `console.log('A')`n’exécute pas, alors que `console.log('B')` exécute.  Si DevTools ré-exécute le script entier après avoir apporté la modification, le texte `A` aurait été enregistré dans la **console**.  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Modification de JavaScript dans le volet éditeur" lightbox="../media/edit-js.msft.png":::
   Modification de JavaScript dans le volet **éditeur**  
:::image-end:::  

DevTools efface vos modifications CSS et JavaScript lorsque vous rechargez la page.  Accédez à [configurer un espace de travail](#set-up-a-workspace) pour découvrir comment enregistrer les modifications apportées à votre système de fichiers.  

## Création, enregistrement et exécution d’extraits de code  

Les extraits de code sont des scripts que vous pouvez exécuter sur n’importe quelle page.  Imaginez que vous entrez le code suivant à plusieurs reprises dans la **console**pour insérer la bibliothèque jQuery dans une page, de sorte que vous puissiez exécuter des commandes jQuery à partir de la **console**.  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Au lieu de cela, vous pouvez enregistrer ce code dans un **extrait de code** et l’exécuter en quelques clics sur le bouton, chaque fois que vous en avez besoin.  DevTools enregistre **l’extrait de code** dans votre système de fichiers.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Un extrait de code qui insère la bibliothèque jQuery dans une page" lightbox="../media/snippet.msft.png":::
   **Un extrait de code** qui insère la bibliothèque jQuery dans une page  
:::image-end:::  

Pour exécuter un **extrait de code** :

*   Ouvrez le fichier à l’aide du volet **extrait de code** , puis sélectionnez **exécuter** \ (![le bouton d’exécution][ImageRunIcon]\).  
*   Ouvrez le [menu de commandes][DevtoolsGuideChromiumCommandMenuIndex], supprimez le `>` caractère, tapez `!` le nom de votre **extrait**de texte, puis sélectionnez `Enter` .  
    
Pour plus d’informations, accédez à [exécuter des extraits de code à partir de n’importe quelle page][DevtoolsGuideChromiumJavascriptSnippets] .

## Déboguer JavaScript  

Au lieu d’utiliser `console.log()` pour induire l’endroit où votre code JavaScript rencontre un problème, envisagez plutôt d’utiliser les outils de débogage de Microsoft Edge DevTools.  L’idée générale consiste à définir un point d’arrêt, qui est un point d’arrêt intentionnel dans votre code, et à parcourir le runtime de votre code, une ligne à la fois.  Lorsque vous parcourez le code, vous pouvez afficher et modifier les valeurs de toutes les propriétés et variables actuellement définies, exécuter JavaScript dans la **console**, etc.

Pour les informations de base sur le débogage dans DevTools, accédez à la section [commencer le débogage de JavaScript][DevtoolsGuideChromiumJavascriptIndex].

:::image type="complex" source="../media/debugging.msft.png" alt-text="Déboguer JavaScript" lightbox="../media/debugging.msft.png":::
   Déboguer JavaScript  
:::image-end:::  

## Configurer un espace de travail  

Par défaut, lorsque vous modifiez un fichier dans l’outil **sources** , les modifications correspondantes sont perdues lorsque vous rechargez la page.  Les **espaces de travail** vous permettent d’enregistrer les modifications que vous apportez dans Devtools à votre système de fichiers.  Fondamentalement, DevTools peut être utilisé en tant qu’éditeur de code.

Accédez à [modifier les fichiers avec des espaces de travail][DevtoolsGuideChromiumWorkspacesIndex] pour commencer.

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Exécution d’extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Modifier des fichiers avec des espaces de travail | Documents Microsoft"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origine | HTML standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Images | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/sources) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
