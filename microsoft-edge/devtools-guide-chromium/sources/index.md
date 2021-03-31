---
description: Afficher et modifier des fichiers, créer des extraits de code, déboguer JavaScript et configurer des espaces de travail dans le panneau Sources de Microsoft Edge DevTools.
title: Vue d’ensemble du volet Sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7ce7ae32b4bf91419512ec9e387cdf75549552a5
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439604"
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

# <a name="sources-panel-overview"></a>Vue d’ensemble du volet Sources  

Utilisez le volet **sources** de Microsoft Edge DevTools pour effectuer ces actions.  

*   [Afficher des fichiers](#display-files).  
*   [Modifier les feuilles CSS et JavaScript](#edit-css-and-javascript).  
*   [Créez et **enregistrez des extraits** de code JavaScript](#create-save-and-run-snippets)que vous pouvez exécuter sur n’importe quelle page web.  **Les extraits de code** sont similaires aux bookmarklets.  
*   [Déboguer JavaScript](#debug-javascript).  
*   [Configurer un espace de travail](#set-up-a-workspace)de telle sorte que les modifications que vous apportez dans DevTools soient enregistrées dans le code de votre système de fichiers.  
    
## <a name="display-files"></a>Afficher des fichiers  

Utiliser le panneau **Page** ; pour afficher toutes les ressources que la page a chargées.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Panneau Page" lightbox="../media/sources-page-pane.msft.png":::
   Panneau **Page**  
:::image-end:::  

Organisation du volet des **pages** :  
*   Le niveau supérieur, tel que `top` dans l’illustration précédente, représente un [cadre HTML][W3CHtml4Frames].  Recherchez `top` sur chaque page visitée.  `top` représente le cadre du document principal.  
*   Le second niveau, tel que `docs.microsoft.com` dans l’illustration précédente, représente une [origine][HtmlstandardOrigin].  
*   Le troisième niveau, le quatrième niveau ainsi de suite, représentent les répertoires et les ressources qui ont été chargés depuis cette origine.  Par exemple, dans l’illustration précédente, le chemin d’accès complet à la ressource `devtools-guide-chromium` est `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Choisissez un fichier dans le volet **Page** pour afficher le contenu dans **le** volet Éditeur.  Vous pouvez afficher n’importe quel type de fichier.  Pour les images, un aperçu de l’image est affiché.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Afficher le contenu des a4d10f71.index-docs.js dans le volet Éditeur" lightbox="../media/sources-editor-pane.msft.png":::
   Affichage du contenu du `a4d10f71.index-docs.js` panneau **Éditeur**  
:::image-end:::  

## <a name="edit-css-and-javascript"></a>Modifier CSS et JavaScript  

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

Les modifications apportées aux feuilles CSS sont immédiatement appliquées, sans enregistrement.  Pour que les modifications JavaScript soient appliquées, sélectionnez `Control`+`S` \(Windows, Linux \) ou `Command`+`S` \(MacOS \).  DevTools ne ré-exécute pas de script, les seules modifications JavaScript qui prennent effet sont celles que vous effectuez dans les fonctions.  Par exemple, dans l’illustration suivante, vous remarquerez que `console.log('A')`n’exécute pas, alors que `console.log('B')` exécute.  Si DevTools ré-exécute à nouveau l’intégralité du script après avoir fait la modification, le texte est enregistré `A` dans la **console**.  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Modification de JavaScript dans le volet éditeur" lightbox="../media/edit-js.msft.png":::
   Modification de JavaScript dans le panneau **Éditeur**  
:::image-end:::  

DevTools efface vos modifications CSS et JavaScript lorsque vous actualisez la page.  Accédez à [configurer un espace de travail](#set-up-a-workspace) pour découvrir comment enregistrer les modifications apportées à votre système de fichiers.  

## <a name="create-save-and-run-snippets"></a>Création, enregistrement et exécution d’extraits de code  

Les extraits de code sont des scripts que vous pouvez exécuter sur n’importe quelle page.  Imaginez que vous tapez à plusieurs reprises le code suivant dans la **console,** afin d’insérer la bibliothèque jQuery dans une page, afin que vous pouvez exécuter des commandes jQuery à partir de la **console**.  

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

*   Ouvrez le **** fichier à l’aide du panneau Extraits de code, puis choisissez **Exécuter** \( Le bouton ![ Exécuter ](../media/run-snippet-icon.msft.png) \).  
*   Ouvrez [le menu Commande,][DevtoolsGuideChromiumCommandMenuIndex]supprimez le caractère, tapez, tapez le nom de votre extrait `>` `!` de code, puis **** sélectionnez `Enter` .  
    
Pour plus d’informations, accédez à [exécuter des extraits de code à partir de n’importe quelle page][DevtoolsGuideChromiumJavascriptSnippets] .

## <a name="debug-javascript"></a>Déboguer JavaScript  

Au lieu d’utiliser `console.log()` pour induire l’endroit où votre code JavaScript rencontre un problème, envisagez plutôt d’utiliser les outils de débogage de Microsoft Edge DevTools.  L’idée générale consiste à définir un point d’arrêt, qui est un point d’arrêt intentionnel dans votre code, et à parcourir le runtime de votre code, une ligne à la fois.  Au fil du code, vous pouvez afficher et modifier les valeurs de toutes les propriétés et variables actuellement définies, exécuter JavaScript dans la **console,** etc.

Pour les informations de base sur le débogage dans DevTools, accédez à la section [commencer le débogage de JavaScript][DevtoolsGuideChromiumJavascriptIndex].

:::image type="complex" source="../media/debugging.msft.png" alt-text="Déboguer JavaScript" lightbox="../media/debugging.msft.png":::
   Déboguer JavaScript  
:::image-end:::  

## <a name="set-up-a-workspace"></a>Configurer un espace de travail  

Par défaut, lorsque vous modifiez un fichier dans l’outil **Sources,** ces modifications sont perdues lorsque vous actualisez la page.  Les **espaces de travail** vous permettent d’enregistrer les modifications que vous apportez dans Devtools à votre système de fichiers.  Fondamentalement, DevTools peut être utilisé en tant qu’éditeur de code.

Accédez à [modifier les fichiers avec des espaces de travail][DevtoolsGuideChromiumWorkspacesIndex] pour commencer.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de commande Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Commencer à déboguer JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Modifier des fichiers à l'| Documents Microsoft"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origine | HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Images | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/sources) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
