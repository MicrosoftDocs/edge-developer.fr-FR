---
description: Les extraits de code sont de petits scripts que vous pouvez écrire et exécuter dans l’outil Sources de Microsoft Edge DevTools.  Vous pouvez accéder aux ressources et les exécuter à partir de n’importe quelle page web.  Lorsque vous exécutez un extrait de code, il s’exécute à partir du contexte de la page web actuellement ouverte.
title: Exécuter des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 4a84e959f652320f40a501a26e9ba763c7348b33
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564111"
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
# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a>Exécuter des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools  

Si vous exécutez le même code dans la [console][DevtoolsConsoleIndex] à plusieurs reprises, envisagez plutôt d’enregistrer le code en tant qu’extrait de code.  Les extraits de code sont des scripts que vous avez écrits dans [l’outil Sources.][DevToolsSourcesTool]  Les extraits de code ont accès au contexte JavaScript de la page web et vous pouvez exécuter des extraits de code sur n’importe quelle page web.  Les paramètres de sécurité de la plupart des pages web bloquent le chargement d’autres scripts dans des extraits de code.  Pour cette raison, vous devez inclure tout votre code dans un seul fichier.  

Les extraits de code [][WikiBookmarklet] sont une alternative aux signets avec la différence que les extraits de code s’exécutent uniquement dans DevTools et ne sont pas limités à la longueur autorisée d’une URL.  

L’utilisation d’extraits de code est un excellent moyen de modifier quelques éléments dans une page web tierce.  Les modifications de code dans les extraits de code sont ajoutées à la page web actuelle et s’exécutent dans le même contexte.  Pour plus d’informations sur la modification du code existant d’une page web, accédez [à Remplacements.][DevtoolsJavascriptOverrides]  

:::row:::
   :::column span="":::
      Par exemple, la figure suivante montre la page d’accueil de DevTools à gauche et du code source d’extrait de code à droite.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Avant d’exécution de l’extrait de code" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         Page web avant l’exécution de l’extrait de code  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Code source de l’extrait de code à partir de la page web avant d’exécutez l’extrait de code.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

Dans la figure suivante, la page web apparaît après l’exécution de l’extrait de code.  Le **caisse de la** console s’affiche pour afficher le message journal de l’extrait de code et le contenu de la page web change `Hello, Snippets!` complètement.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Page web après l’exécution de l’extrait de code" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Page web après l’exécution de l’extrait de code  
:::image-end:::  

## <a name="open-the-snippets-tab"></a>Ouvrir l’onglet Extraits de code  

**L’onglet Extraits** de code, dans le volet **Navigateur** à gauche, répertorie vos extraits de code.  Lorsque vous souhaitez modifier un extrait de code, vous devez l’ouvrir à partir de l’onglet Extraits **de** code.  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Onglet Extraits de code" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Onglet **Extraits de** code  
:::image-end:::  

### <a name="open-the-snippets-tab-with-a-mouse"></a>Ouvrir l’onglet Extraits de code avec une souris  

1.  Sélectionnez **l’onglet Sources.**  **L’outil Sources** s’affiche.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Outil Sources avec l’onglet Page ouvert à gauche" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Outil **Sources** avec l’onglet **Page** ouvert à gauche  
    :::image-end:::  
    
1.  Dans le **volet Navigateur** (à gauche), sélectionnez l’onglet **Extraits de** code.  Pour accéder à **l’option** Extraits de code, vous devrez peut-être sélectionner **Plus d’onglets** \( ![ Autres onglets ](../media/more-tabs-icon.msft.png) \).  
    
### <a name="open-the-snippets-tab-with-the-command-menu"></a>Ouvrir l’onglet Extraits de code avec le menu Commande  

1.  Sélectionnez n’importe quoi dans DevTools, afin que DevTools ait le focus.  
1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le menu Commande.  
1.  Tapez `Snippets` , choisissez Afficher les **extraits**de code, puis `Enter` sélectionnez pour exécuter la commande.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Commande Afficher les extraits de code" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Commande **Afficher les extraits de** code  
    :::image-end:::  
    
## <a name="create-snippets"></a>Créer des extraits de code  

### <a name="create-a-snippet-through-the-sources-tool"></a>Créer un extrait de code via l’outil Sources  

1.  [Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)  
1.  Choose **New snippet**.  
1.  Entrez un nom pour votre extrait de code, puis sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nommer un extrait de code" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nommer un extrait de code  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a>Créer un extrait de code dans le menu Commande  

1.  Concentrez votre curseur quelque part dans DevTools.  
1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le menu Commande.  
1.  Tapez `Snippet` , choisissez Créer un extrait de **code,** puis `Enter` sélectionnez pour exécuter la commande.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Commande de création d’un extrait de code" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Commande de création d’un extrait de code  
    :::image-end:::  
    
Pour renommer votre nouvel extrait de code avec un nom personnalisé, accédez à Renommer les [extraits de code.](#rename-snippets)  

## <a name="edit-snippets"></a>Modifier les extraits de code  

1.  [Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)  
1.  Dans **l’onglet Extraits** de code, choisissez le nom de l’extrait de code à modifier.  Il s’ouvre dans **l’éditeur de code.**  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Éditeur de code" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       Éditeur **de code**  
    :::image-end:::  
    
1.  Utilisez **l’Éditeur de code** pour ajouter JavaScript à votre extrait de code.  
1.  Lorsqu’un astérisque apparaît à côté du nom de votre extrait de code, cela signifie que vous avez du code nonavé.  Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) à enregistrer.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un astérisque à côté du nom de l’extrait de code indique du code nonavé" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Un astérisque à côté du nom de l’extrait de code indique du code nonavé  
    :::image-end:::  
    
## <a name="run-snippets"></a>Exécuter des extraits de code  

### <a name="run-a-snippet-from-the-sources-tool"></a>Exécuter un extrait de code à partir de l’outil Sources  

1.  [Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)  
1.  Choisissez le nom de l’extrait de code à exécuter.  L’extrait de code s’ouvre dans **l’éditeur de code.**  
1.  Choose **Run snippet** \( ![ Run Snippet ](../media/run-snippet-icon.msft.png) \).
    
### <a name="run-a-snippet-with-the-command-menu"></a>Exécuter un extrait de code avec le menu Commande  

1.  Concentrez votre curseur quelque part dans DevTools.  
1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le menu Commande.  
1.  Supprimez le caractère et tapez le caractère suivi du nom de l’extrait de code à `>` `!` exécuter.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Exécution d’un extrait de code à partir du menu Commande" lightbox="../media/javascript-search-run-command.msft.png":::
       Exécution d’un extrait de code à partir du **menu Commande**  
    :::image-end:::  
    
1.  Sélectionnez `Enter` pour exécuter l’extrait de code.  

## <a name="rename-snippets"></a>Renommer les extraits de code  

1.  [Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)  
1.  Pointez sur le nom de l’extrait de code, ouvrez le menu contextuel \(clic droit\), puis choisissez **Renommer.**  
    
## <a name="delete-snippets"></a>Supprimer des extraits de code  

1.  [Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)  
1.  Pointez sur le nom de l’extrait de code, ouvrez le menu contextuel \(clic droit\), puis choisissez **Supprimer.**  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Vue d’ensemble de la console | Documents Microsoft"  
[DevToolsSourcesTool]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Remplace les | Documents Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
