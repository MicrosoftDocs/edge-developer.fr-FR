---
description: Les extraits sont des petits scripts que vous pouvez créer et exécuter dans l’outil sources de Microsoft Edge DevTools.  Vous pouvez accéder aux ressources et les exécuter à partir de n’importe quelle page.  Lorsque vous exécutez un snippet, il s’exécute à partir du contexte de la page Web actuellement ouverte.
title: Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3542243f7fa886865ced47d47991cd9b11001e2e
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145119"
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

# Exécuter des extraits de code JavaScript sur n’importe quelle page Web avec Microsoft Edge DevTools  

Si vous exécutez le même code dans la [console][DevtoolsConsoleIndex] de manière répétée, envisagez d’enregistrer le code en tant qu’extrait.  Les extraits sont des scripts que vous créez dans l’outil [sources][DevToolsSourcesTool] .  Les extraits de code ont accès au contexte JavaScript de la page Web, et vous pouvez exécuter des extraits de code sur une page Web.  Les paramètres de sécurité de la plupart des pages Web se bloquent lors du chargement d’autres scripts dans les extraits.  Pour cette raison, vous devez inclure tout votre code dans un fichier.  

Les extraits de vue sont une alternative aux [bookmarklets][WikiBookmarklet] à la différence que les extraits de la base ne s’exécutent que dans devtools et ne sont pas limités à la longueur autorisée d’une URL.  

L’utilisation d’extraits est un excellent moyen de changer quelques éléments dans une page Web tierce.  Les changements de code dans les extraits de code sont ajoutés à la page Web actuelle et s’exécutent dans le même contexte.  Pour plus d’informations sur la modification du code existant d’une page Web, voir [remplacement][DevtoolsJavascriptOverrides].  

:::row:::
   :::column span="":::
      Par exemple, dans la figure suivante, la page d’accueil DevTools sur la gauche et le code source de l’extrait de code à droite.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         Page Web avant d’exécuter l’extrait  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Code source de l’extrait de code de la page Web avant d’exécuter l’extrait de code.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

Dans l’illustration suivante, la page Web s’affiche après l’exécution de l’extrait de code.  Le **tiroir** de la console s’affiche pour afficher le `Hello, Snippets!` message indiquant que le Snippet enregistre les journaux et le contenu de la page Web s’en trouve entièrement modifié.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   La page Web après l’exécution de l’extrait  
:::image-end:::  

## Ouvrir le volet d’extraits  

Le volet d' **extraits** de liste répertorie vos extraits.  Lorsque vous voulez modifier un extrait de rapport, vous devez l’ouvrir à partir du volet **extraits** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Volet **snippets**  
:::image-end:::  

### Ouvrir le volet des fragments de fenêtre à l’aide d’une souris  

1.  Sélectionnez l’onglet **sources** pour ouvrir l’outil **sources** .  Le volet **page** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-page-pane.msft.png":::
       Outil **sources** avec le volet **pages** ouvert à gauche  
    :::image-end:::  
    
1.  Cliquez sur l’onglet **extraits** de vue pour ouvrir le volet d' **extraits** .  Il est possible que vous deviez sélectionner d' **autres onglets** \ ( ![ plus d’onglets ][ImageMoreTabsIcon] \) pour accéder à l’option d' **extraits** .  
    
### Ouvrir le volet d’extraits de fenêtre à l’aide du menu de commandes  

1.  Focalisez votre curseur à un endroit quelconque dans DevTools.  
1.  Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Tapez `Snippets` , choisissez **afficher les extraits**, puis sélectionnez `Enter` pour exécuter la commande.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-search-show-snippets.msft.png":::
       Commande **afficher les extraits**  
    :::image-end:::  
    
## Créer des extraits de  

### Créer un snippet via le volet sources  

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Sélectionnez **nouvel extrait**.  
1.  Entrez le nom de votre snippet, puis sélectionnez `Enter` Enregistrer.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nommer un snippet  
    :::image-end:::  
    
### Créer un snippet via le menu de commandes  

1.  Focalisez votre curseur à un endroit quelconque dans DevTools.  
1.  Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Tapez `Snippet` , choisissez **créer un nouvel extrait**, puis sélectionnez `Enter` pour exécuter la commande.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Commande de création d’un nouveau Snippet  
    :::image-end:::  
    
Pour renommer votre nouveau Snippet avec un nom personnalisé, accédez à [Renommer des extraits de nom](#rename-snippets).  

## Modifier des extraits de ce profil  

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Dans le volet **snippets** , sélectionnez le nom de l’extrait que vous voulez modifier.  Il s’ouvre dans l' **éditeur de code**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       **Éditeur de code**  
    :::image-end:::  
    
1.  Utilisez l' **éditeur de code** pour ajouter du JavaScript à votre snippet.  
1.  Lorsqu’un astérisque apparaît en regard du nom de votre snippet, cela signifie que vous avez du code non enregistré.  Sélectionnez `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) pour l’enregistrer.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Un astérisque en regard du nom de l’extrait de code indique le code non enregistré  
    :::image-end:::  
    
## Exécuter des Snippets  

### Exécuter un snippet à partir du panneau sources  

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Sélectionnez le nom de l’extrait que vous souhaitez exécuter.  L’extrait de code s’ouvre dans l' **éditeur de code**.  
1.  Sélectionnez **exécuter le fragment** de passe \ ( ![ exécuter l’extrait ][ImageRunSnippetIcon] \), ou sélectionnez `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \).  
    
### Exécuter un extrait de commande avec le menu de commandes  

1.  Focalisez votre curseur à un endroit quelconque dans DevTools.  
1.  Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Supprimez le `>` caractère et tapez le `!` caractère suivi du nom de l’extrait que vous voulez exécuter.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-search-run-command.msft.png":::
       Exécution d’un snippet à partir du **menu de commandes**  
    :::image-end:::  
    
1.  Activez `Enter` cette option pour exécuter l’extrait de.  

## Renommer des extraits de nom  

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Placez le curseur sur le nom de l’extrait, ouvrez le menu contextuel, puis cliquez sur **Renommer**.  
    
## Supprimer des extraits de  

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Placez le curseur sur le nom de l’extrait, ouvrez le menu contextuel, puis cliquez sur **supprimer**.  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevToolsSourcesTool]: ../sources.md "Présentation de l’outil sources | Documents Microsoft"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Remplacements | Documents Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc-notes | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
