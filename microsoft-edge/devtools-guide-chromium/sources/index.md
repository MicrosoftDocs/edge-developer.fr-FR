---
description: Utilisez l’outil Sources pour afficher, modifier et déboguer JavaScript renvoyé par le serveur, et pour inspecter les ressources qui font la page web actuelle.  Pour utiliser l’outil Sources comme environnement de développement, ajoutez des fichiers sources à un espace de travail.
title: Vue d’ensemble de l’outil Sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d3ef49bf986d8827216bd0bc183e45806aa0a2c3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564713"
---
# <a name="sources-tool-overview"></a>Vue d’ensemble de l’outil Sources  

Utilisez **l’outil Sources** pour afficher, modifier et déboguer le code JavaScript frontal et inspecter les ressources qui font la page web actuelle.  **L’outil Sources** possède trois volets :  

| Volet | Actions |  
|:--- |:--- |  
| **Volet navigateur** | Naviguez parmi les ressources renvoyées à partir du serveur pour construire la page web actuelle.  Sélectionnez des fichiers, des images et d’autres ressources et affichez leurs chemins d’accès.  Vous pouvez également configurer un espace de travail local pour enregistrer les modifications directement dans les fichiers sources.  |  
| **Volet** Éditeur | Afficher les fichiers JavaScript, HTML, CSS et autres qui sont renvoyés à partir du serveur.  A apporter des modifications expérimentales à JavaScript ou CSS.  Vos modifications sont conservées jusqu’à ce que vous actualisiez la page ou après l’actualisation de la page si vous enregistrez dans un fichier local avec espaces de travail.  Lorsque vous utilisez des espaces de travail ou des substitutions, vous pouvez également modifier des fichiers HTML.  |  
| **Volet Débogger** | Utilisez le débogger JavaScript pour définir des points d’arrêt, suspendre l’exécution de JavaScript et passer pas à pas le code, y compris les modifications que vous avez faites, tout en regardant les expressions JavaScript que vous spécifiez.  Observez et modifiez manuellement les valeurs des variables qui sont dans l’étendue de la ligne de code actuelle.  |  

La figure suivante montre le volet **Navigateur** mis en surbrillon avec une **** zone rouge dans le coin supérieur **** gauche de DevTools, le volet Éditeur mis en surbrillon dans le coin supérieur droit et le volet Débogueur mis en évidence en bas.  À l’extrême gauche se trouve la partie principale de la fenêtre du navigateur, affichant la page web rendue grisée, car le débogger est suspendu sur un point d’arrêt :

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Volets de l’outil Sources, en disposition étroite" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   Volets de l’outil Sources, en disposition étroite  
:::image-end:::  

Lorsque DevTools est **** large, le volet Débogueur est placé à droite et inclut **Scope** et **Watch**:  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Parcourir, afficher, modifier et déboguer JavaScript renvoyé par le serveur" lightbox="../media/sources-panes-wide-layout.msft.png":::
   Parcourir, afficher, modifier et déboguer JavaScript renvoyé par le serveur  
:::image-end:::  

Pour optimiser la taille de l’outil Sources, désédockez DevTools dans une fenêtre distincte et déplacez éventuellement la fenêtre DevTools vers un moniteur distinct.  Voir [Modifier Microsoft Edge placement de DevTools (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].

Pour charger la page web de démonstration de débogage ci-dessus, voir l’approche de base de l’utilisation [d’un déboguer,](#the-basic-approach-to-using-a-debugger)ci-dessous.

## <a name="using-the-navigator-pane-to-select-files"></a>Utilisation du volet Navigateur pour sélectionner des fichiers

Utilisez le **volet Navigateur** \(sur la gauche\) pour naviguer parmi les ressources renvoyées par le serveur pour construire la page web actuelle.  Sélectionnez des fichiers, des images et d’autres ressources et affichez leurs chemins d’accès.  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="Volet Navigateur" lightbox="../media/navigator-pane.msft.png":::
   Volet **Navigateur**
:::image-end:::  

Pour accéder aux onglets masqués du volet Navigateur, sélectionnez ![ Autres onglets ](../media/more-tabs-icon.msft.png) \(**Autres onglets**\).

Les sous-sections suivantes couvrent le volet Navigateur :  

*   [Utilisation de l’onglet Page pour explorer les ressources qui construisent la page web actuelle](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)  
*   [Utilisation de l’onglet Système de fichiers pour définir un espace de travail local](#using-the-filesystem-tab-to-define-a-local-workspace)  
*   [Utilisation de l’onglet Remplacements pour remplacer les fichiers serveur avec des fichiers locaux](#using-the-overrides-tab-to-override-server-files-with-local-files)  
*   [Utilisation de l’onglet Scripts de contenu pour Microsoft Edge extensions](#using-the-content-scripts-tab-for-microsoft-edge-extensions)  
*   [Utilisation de l’onglet Extraits de code pour exécuter des extraits de code JavaScript sur n’importe quelle page](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)  
*   [Utilisation du menu Commande pour ouvrir des fichiers](#using-the-command-menu-to-open-files)  
    
### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a>Utilisation de l’onglet Page pour explorer les ressources qui construisent la page web actuelle

Utilisez **l’onglet Page** du volet **Navigateur** pour explorer le système de fichiers renvoyé par le serveur pour construire la page web actuelle.  Sélectionnez un fichier JavaScript pour l’afficher, le modifier et le déboguer.  **L’onglet Page** répertorie toutes les ressources que la page a chargées.

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="Onglet Page dans le volet Navigateur de l’outil Sources" lightbox="../media/sources-page-tab.msft.png":::
   Onglet **Page** dans le volet **Navigateur** de l’outil **Sources**
:::image-end:::  

Pour afficher un fichier dans **le** volet Éditeur, sélectionnez un fichier dans l’onglet **Page.**  Pour une image, un aperçu de l’image s’affiche.  
Pour afficher l’URL ou le chemin d’accès d’une ressource, pointez sur la ressource.  
Pour charger un fichier dans un nouvel onglet du navigateur ou pour afficher d’autres actions, cliquez avec le bouton droit sur le nom du fichier.  

#### <a name="icons-in-the-page-tab"></a>Icônes dans l’onglet Page

**L’onglet Page** utilise les icônes suivantes :  

*   **L’icône** de fenêtre, ainsi que l’étiquette, représente le cadre de `top` document principal, qui est un [cadre HTML][W3CHtml4Frames].  
*   **L’icône cloud** représente une [origine][WhatwgHtmlSpecMulitpageOriginHtmlOrigin].  
*   **L’icône** de dossier représente un répertoire.  
*   **L’icône** de page représente une ressource.  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a>Grouper des fichiers par dossier ou en tant que liste plate

**L’onglet Page** affiche les fichiers ou les ressources regroupés par serveur et répertoire, ou sous la direction d’une liste plate.

Pour modifier le regroupement des ressources :

1.  À côté des onglets du volet Navigateur \(sur la gauche\), sélectionnez le bouton **...** \( Autres**options**\).  Un menu s’affiche.  
1.  Sélectionnez ou effacer **l’option Grouper par** dossier.  
    
### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a>Utilisation de l’onglet Système de fichiers pour définir un espace de travail local

Utilisez **l’onglet Système** de fichiers du volet **Navigateur** pour ajouter des fichiers à un espace de travail, afin que les modifications apportées dans DevTools sont enregistrées dans votre système de fichiers local.  
Un fichier qui se trouve dans un espace de travail est indiqué par un point vert à côté du nom de fichier, dans DevTools.  

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="Onglet Système de fichiers, pour un espace de travail" lightbox="../media/sources-filesystem-tab.msft.png":::
   Onglet **Système de** fichiers, pour un espace de travail
:::image-end:::  

Par défaut, lorsque vous modifiez un fichier dans l’outil **Sources,** vos modifications sont ignorées lorsque vous actualisez la page web.  **L’outil Sources** fonctionne avec une copie des ressources frontales renvoyées par le serveur web.  Lorsque vous modifiez ces fichiers frontaux renvoyés par le serveur, les modifications ne sont pas persistantes, car vous n’avez pas modifié les fichiers sources.  Vous devez également appliquer vos modifications dans votre code source réel, puis les déployer à nouveau sur le serveur.  
En revanche, lorsque vous utilisez un espace de travail, les modifications que vous a faites à votre code frontal sont conservées lorsque vous actualisez la page web.  Avec un espace de travail, lorsque vous modifiez le code frontal renvoyé par le serveur, l’outil Sources applique également vos modifications à votre code source local.  Ensuite, pour que les autres utilisateurs voient vos modifications, vous devez uniquement redéployer vos fichiers sources modifiés sur le serveur.  
Les espaces de travail fonctionnent bien lorsque le code JavaScript renvoyé par le serveur est identique à votre code source JavaScript local.  Les espaces de travail ne fonctionnent pas aussi bien lorsque votre flux de travail implique des transformations sur votre code source, telles que la minification ou la compilation [de TypeScript.][TypescriptlangMain]  

Pour plus d’informations, voir le didacticiel [Modifier les fichiers avec les espaces de travail.][DevtoolsGuideChromiumWorkspacesIndex]

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a>Utilisation de l’onglet Remplacements pour remplacer les fichiers serveur avec des fichiers locaux

Utilisez **l’onglet Remplacements** du volet **Navigateur** pour remplacer les ressources de page \(telles que les images\) avec les fichiers d’un dossier local.  
Les éléments de cet onglet remplacent ce que le serveur envoie au navigateur, même après que le serveur a envoyé les biens.  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="Onglet Remplacements du volet Navigateur" lightbox="../media/overrides-tab.msft.png":::
   Onglet **Remplacements** du volet **Navigateur**
:::image-end:::  

La **fonctionnalité Overrides** est similaire à Workspaces.  Utilisez les substitutions lorsque vous souhaitez expérimenter les modifications apportées à une page web et que vous devez conserver les modifications après avoir actualisé la page web, mais que vous ne vous souciez pas de ma mappage de vos modifications au code source de la page web.  

Un fichier qui remplace un fichier qui est renvoyé par le serveur est indiqué par un point violet à côté du nom de fichier, dans DevTools.

#### <a name="see-also"></a>Voir également

*   [Remplacer les ressources de page web avec des copies locales à l’Microsoft Edge DevTools][DevtoolsJavascriptOverrides]  
*   [Ma mappant le code prétraité au code source][DevToolsJavaScriptSourceMaps]  
    
### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a>Utilisation de l’onglet Scripts de contenu pour Microsoft Edge extensions

Utilisez **l’onglet Scripts** de contenu du volet **Navigateur** pour afficher les scripts de contenu qui ont été chargés par une extension Microsoft Edge que vous avez installée.  

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="Onglet Scripts de contenu du volet Navigateur" lightbox="../media/content-scripts-tab.msft.png":::
   Onglet **Scripts de contenu** du volet **Navigateur**
:::image-end:::  

Lorsque le débompeur entre dans du code que vous ne connaissez pas, vous pouvez marquer ce code comme du code de bibliothèque, afin d’éviter d’entrer pas à pas dans ce code.  Voir [Marquer les scripts de contenu en tant que code de bibliothèque.][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]

#### <a name="see-also"></a>Voir également

*   [Scripts de contenu][MdnAddOnsWebextensionsContentScripts]  
*   [Didacticiel de création d’extension: partie2][ExtensionsChromiumGetstartPart2ContentScripts]  
    
### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a>Utilisation de l’onglet Extraits de code pour exécuter des extraits de code JavaScript sur n’importe quelle page web

Utilisez **l’onglet** Extraits de code du volet **Navigateur** pour créer et enregistrer des extraits de code JavaScript, afin que vous pouvez facilement exécuter ces extraits de code sur n’importe quelle page web.

:::image type="complex" source="../media/snippet.msft.png" alt-text="Extrait de code qui insère la bibliothèque jQuery dans une page web" lightbox="../media/snippet.msft.png":::
   Extrait de code qui insère la bibliothèque jQuery dans une page web  
:::image-end:::  

Par exemple, supposons que vous entrez fréquemment le code suivant dans la **console**, pour insérer la bibliothèque jQuery dans une page afin que vous pouvez exécuter des commandes jQuery à partir de la **console**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Au lieu de cela, vous **** pouvez enregistrer ce code dans un extrait de code, puis l’exécuter facilement quand vous le souhaitez.  Lorsque vous sélectionnez `Ctrl` + `S` \(Windows/Linux\) ou `Command` + `S` \(macOS\), DevTools **** enregistre l’extrait de code dans votre système de fichiers.  

Il existe plusieurs façons d’exécuter un extrait de code :  

*   Dans le **volet Navigateur,** sélectionnez l’onglet Extraits de code, puis sélectionnez le fichier d’extraits de code pour l’ouvrir. ****  Ensuite, en bas du volet Éditeur, **sélectionnez Exécuter** \( ![ Le bouton Exécuter ](../media/run-snippet-icon.msft.png) \).  
*   Lorsque DevTools a le focus, sélectionnez `Ctrl` + `P` \(Windows/Linux\) ou `Command` + `P` [][DevToolsCommandMenuIndex]\(macOS\) `!` pour ouvrir le menu commande, puis tapez .  
    
Les extraits de code sont similaires aux bookmarklets.

#### <a name="see-also"></a>Voir également

*   [Exécuter des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptSnippets]  
    
### <a name="using-the-command-menu-to-open-files"></a>Utilisation du menu Commande pour ouvrir des fichiers

Pour ouvrir un fichier, en plus d’utiliser le volet **Navigateur** dans l’outil **Sources,** vous pouvez utiliser le menu Commande de n’importe où dans DevTools.

*   N’importe où dans DevTools, sélectionnez `Ctrl` + `P` sur Windows/Linux `Command` + `P` ou sur macOS.  Le menu Commande s’affiche et répertorie toutes les ressources présentes dans les onglets du volet **Navigateur** de l’outil **Sources.**  
*   Ou, à côté des onglets du volet **Navigateur** dans l’outil **Sources,** sélectionnez le bouton **...** \( Autres**options**\), puis sélectionnez Ouvrir **un fichier**.  

Pour afficher et sélectionner dans une liste de tous les fichiers .js, tapez `.js` .

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Ouverture d’un fichier à l’aide du menu Commande" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   Ouverture d’un fichier à l’aide du menu Commande
:::image-end:::

Si vous `?` tapez, le menu Commande affiche plusieurs commandes, notamment **...  Ouvrir le fichier**.  Si vous choisissez `Backspace` d’effacer le menu Commande, une liste de fichiers s’affiche.

Pour plus d’informations, voir Exécuter des commandes Microsoft Edge menu de commande [DevTools.][DevToolsCommandMenuIndex]

## <a name="using-the-editor-pane-to-view-or-edit-files"></a>Utilisation du volet Éditeur pour afficher ou modifier des fichiers

Utilisez **le** volet Éditeur pour afficher les fichiers frontaux renvoyés à partir du serveur afin de composer la page web actuelle, y compris les fichiers JavaScript, HTML, CSS et image.  Lorsque vous modifiez les fichiers **** frontaux dans le volet Éditeur, DevTools met à jour la page web pour exécuter le code modifié.  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="Volet Éditeur de l’outil Sources" lightbox="../media/editor-pane.msft.png":::
   Volet **Éditeur** de l’outil **Sources**  
:::image-end:::

Le **volet Éditeur** a le niveau de prise en charge suivant pour différents types de fichiers :  

| Type de fichier | Actions prises en charge |  
|:--- |:--- |  
| JavaScript | Afficher, modifier et déboguer.  |  
| CSS | Afficher et modifier.  |  
| HTML | Afficher et modifier.  |  
| Images | Afficher.  |  

Par défaut, les modifications sont ignorées lorsque vous actualisez la page web.  Pour plus d’informations sur la façon d’enregistrer les modifications apportées à votre système de fichiers, voir Utilisation de l’onglet Système de fichiers pour définir un espace de travail [local,](#using-the-filesystem-tab-to-define-a-local-workspace)ci-dessus.

Les sous-sections suivantes couvrent le volet Éditeur :  

*   [Modification d’un fichier JavaScript](#editing-a-javascript-file)  
*   [Reformatage d’un fichier JavaScript minifié avec une impression assez grande](#reformatting-a-minified-javascript-file-with-pretty-print)  
*   [Mappage du code minifié à votre code source pour afficher du code lisible](#mapping-minified-code-to-your-source-code-to-show-readable-code)  
*   [Transformations du code source au code frontal compilé](#transformations-from-source-code-to-compiled-front-end-code)  
*   [Modification d’un fichier CSS](#editing-a-css-file)  
*   [Modification d’un fichier HTML](#editing-an-html-file)  
*   [Accès à un numéro de ligne ou à une fonction](#going-to-a-line-number-or-function)  
*   [Affichage des fichiers sources lors de l’utilisation d’un autre outil](#displaying-source-files-when-using-a-different-tool)  
    
### <a name="editing-a-javascript-file"></a>Modification d’un fichier JavaScript

Pour modifier un fichier JavaScript dans DevTools, utilisez le volet Éditeur, dans l’outil **Sources.** ****

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Modification de JavaScript dans le volet éditeur" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   Modification de JavaScript dans le volet **éditeur**  
:::image-end:::

Pour charger un fichier dans le volet Éditeur, utilisez l’onglet **Page** dans le volet **Navigateur** \(sur la gauche\).  Vous pouvez également utiliser le **menu**DevTools, comme suit : dans le coin supérieur droit de DevTools, sélectionnez Personnaliser et contrôler **DevTools** \( \), puis `...` **ouvrez le fichier**.

#### <a name="save-and-undo"></a>Enregistrer et annuler

Pour que les modifications JavaScript soient appliquées, sélectionnez `Ctrl`+`S` \ (Windows, Linux \) ou `Command`+`S` \ (MacOS \).  

Si vous modifiez un fichier, un astérisque s’affiche à côté du nom de fichier.  

*   Pour enregistrer les modifications, sélectionnez `Ctrl` + `S` sur Windows/Linux `Command` + `S` ou sur macOS.  
*   Pour annuler une modification, sélectionnez `Ctrl` + `Z` sur Windows/Linux `Command` + `Z` ou sur macOS.  
    
Par défaut, vos modifications sont ignorées lorsque vous actualisez la page web.  Pour plus d’informations sur l’enregistrer dans votre système de fichiers local, voir Modifier des fichiers [avec Workspaces][DevtoolsGuideChromiumWorkspacesIndex].

#### <a name="find-and-replace"></a>Rechercher et remplacer

Pour rechercher du texte dans **** le fichier actuel, sélectionnez le volet Éditeur pour lui donner le focus, puis sélectionnez `Ctrl` + `F` sur Windows/Linux ou `Command` + `F` sur macOS.  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Rechercher et remplacer, dans le volet Éditeur de l’outil Sources" lightbox="../media/find-replace.msft.png":::
   **Rechercher** et **remplacer**, dans le volet **Éditeur** de l’outil **Sources**
:::image-end:::

Pour rechercher et remplacer du texte, sélectionnez le bouton Remplacer **\(** **A-\>B**\) à gauche de la **boîte** de texte Rechercher.  Le **bouton Remplacer** \(**A-\>B**\) s’affiche lors de l’affichage d’un fichier modifiable.

#### <a name="showing-the-changes-you-made"></a>Affichage des modifications que vous avez apportées

Pour passer en revue les modifications apportées **** à un fichier, cliquez avec le bouton droit dans le volet Éditeur, puis sélectionnez **Modifications locales.**

Le **caisse** s’ouvre en bas de DevTools, affichant vos modifications dans l’onglet **Modifications.**

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Affichage des modifications locales, sous l’onglet Modifications du caisse" lightbox="../media/local-modifications.msft.png":::
   Affichage **des modifications locales,** sous **l’onglet Modifications** du **caisse**
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a>Les modifications à l’intérieur d’une fonction prennent effet

DevTools ne ré-exécute pas de script, de sorte que les seules modifications JavaScript qui prennent effet sont les modifications que vous a faites au sein des fonctions.  Par exemple, dans la figure suivante, nous avons ajouté le code suivant au code JavaScript renvoyé par le serveur :  
*   Nous avons ajouté l’instruction `console.log('A')` en dehors de n’importe quelle fonction.  
*   Nous avons ajouté l’instruction `console.log('B')` à l’intérieur d’une `onClick` fonction.  
Nous avons ensuite enregistré les modifications, entré des numéros dans le formulaire, puis sélectionné le bouton du formulaire pour envoyer le formulaire.  

Après l’envoi du formulaire, qui est au niveau `console.log('A')` de l’étendue globale, ne s’exécute pas, mais, à l’intérieur d’une fonction, s’exécute, en sortie dans `console.log('B')` la console `onClick` `B` :

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript de portée globale n’est pas ré-exécuté" lightbox="../media/edit-js.msft.png":::
   JavaScript de portée globale n’est pas ré-exécuté  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a>Reformatage d’un fichier JavaScript minifié avec une impression assez grande

Pour utiliser pretty-print pour reformater un fichier **** afin de le rendre lisible, sélectionnez le bouton d’impression Pretty \( Format \), qui est affiché sous forme d’accolades, en bas du volet ![ ](../media/format-icon.msft.png) Éditeur.  Ou, si un **bouton Assez** imprimé apparaît en haut du volet Éditeur, vous pouvez sélectionner ce bouton.

:::image type="complex" source="../media/minified.msft.png" alt-text="Bouton d’impression Pretty" lightbox="../media/minified.msft.png":::
   Bouton **d’impression** Pretty  
:::image-end:::  

Le fichier reformaté apparaît dans un nouvel onglet, avec le nom `:formatted` du fichier.  Le code reformaté est en lecture seule.  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Un fichier JavaScript assez imprimé (reformaté)" lightbox="../media/pretty-printed.msft.png":::
   Un fichier JavaScript assez imprimé \(reformatted\)  
:::image-end:::  

Pour faire défiler le fichier reformaté jusqu’au code que vous sélectionnez dans le fichier minifié :  

1.  Si l’onglet de fichier reformaté est ouvert, fermez-le.  
1.  Sélectionnez du code dans le fichier minifié dans le volet Éditeur.
1.  Sélectionnez **le bouton Imprimer.**  
     
Le code formaté apparaît dans un nouvel onglet, en faisant défiler jusqu’au code que vous avez sélectionné.

Pour plus d’informations, [voir Reformater un fichier JavaScript minifié avec une impression assez grande.][DevToolsJavaScriptReferenceReformat]  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a>Mappage du code minifié à votre code source pour afficher du code lisible

Les cartes sources provenant de préprocesseurs entraînent le chargement par DevTools de vos fichiers sources JavaScript d’origine en plus de vos fichiers JavaScript transformés et minifiés qui sont renvoyés par le serveur.  Vous affichez ensuite vos fichiers sources d’origine pendant que vous définissez des points d’arrêt et vous avancez pas à pas dans le code.  Pendant ce temps, Microsoft Edge exécute réellement votre code minifié.  

Dans **** le volet Éditeur, si vous cliquez avec le bouton droit sur un fichier JavaScript, puis sélectionnez Ajouter un plan **source,** une boîte de message apparaît, avec une zone de texte **URL** de carte source et un bouton **Ajouter.**

L’approche de mappage de source permet de garder votre code frontal lisible et décomscriptible même après la combinaison, la minification ou la compilation de celui-ci.
Pour plus d’informations, voir [Ma cartographier le code prétraité au code source.][DevToolsJavaScriptSourceMaps]

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a>Transformations du code source au code frontal compilé

Si vous utilisez une infrastructure qui transforme vos fichiers JavaScript, tels que React, votre javaScript source local peut être différent du JavaScript frontal renvoyé par le serveur.  Les espaces de travail ne sont pas pris en charge dans ce scénario, mais le mappage de code source est pris en charge dans ce scénario.  

Dans un environnement de développement, votre serveur peut inclure vos cartes sources et vos fichiers d’origine `.ts` `.jsx` ou de React.  **L’outil Sources** affiche ces fichiers, mais ne vous permet pas de modifier ces fichiers.  Lorsque vous définissez des points d’arrêt et utilisez le débogueur, DevTools affiche vos fichiers d’origine, mais pas à pas dans la version minifiée de vos `.ts` `.jsx` fichiers JavaScript.

Dans ce scénario, l’outil **Sources** est utile pour inspecter et passer pas à pas le JavaScript frontal transformé renvoyé à partir du serveur.  Utilisez le débogger pour définir des expressions Watch et utilisez la console pour entrer des expressions JavaScript afin de manipuler des données dans l’étendue.

### <a name="editing-a-css-file"></a>Modification d’un fichier CSS

Il existe deux façons de modifier CSS dans DevTools :  

*   Dans **l’outil Elements,** vous travaillez avec un paramètre CSS à la fois, via des contrôles d’interface utilisateur.  Cette approche est recommandée dans la plupart des cas.  Pour plus d’informations, voir [Modifier les styles de police CSS][DevToolsInspectStylesEditFonts]et les paramètres dans le volet Styles.  
*   Dans **l’outil Sources,** vous utilisez un éditeur de texte.  
    
L’outil Sources prend en charge la modification directe d’un fichier CSS.  Par exemple, si vous modifiez le fichier CSS à partir du didacticiel Modifier les fichiers avec des [espaces][DevtoolsGuideChromiumWorkspacesIndex] de travail pour qu’il corresponde à la règle de style ci-dessous, l’élément dans le coin supérieur gauche de la page web rendue se transforme en `H1` vert :

```css
h1 {
  color: green;
}  
```  

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Modifier CSS dans le volet Éditeur pour changer la couleur du texte du titre H1 en vert" lightbox="../media/edit-css.msft.png":::
   Modifier CSS dans **le** volet Éditeur pour changer la couleur du texte du titre en `H1` vert  
:::image-end:::  

Les modifications CSS prennent effet immédiatement ; vous n’avez pas besoin d’enregistrer manuellement les modifications.

#### <a name="see-also"></a>Voir également  

*   [Modifier les styles et paramètres de police CSS dans le volet Styles][DevToolsInspectStylesEditFonts]  
*   [DevTools pour les débutants : Mise en place de CSS][DevToolsBeginnersCss] - didacticiel  
    
### <a name="editing-an-html-file"></a>Modification d’un fichier HTML

Il existe deux façons de modifier le code HTML dans DevTools :  

*   Dans **l’outil Elements,** vous travaillez avec un élément HTML à la fois, via des contrôles d’interface utilisateur.  
*   Dans **l’outil Sources,** vous utilisez un éditeur de texte.  
    
:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="Éditeur HTML de l’outil Sources" lightbox="../media/sources-html-editor.msft.png":::
   Éditeur HTML de l’outil **Sources**
:::image-end:::  

Contrairement à un fichier JavaScript ou CSS, un fichier HTML renvoyé par le serveur web ne peut pas être modifié directement dans l’outil Sources.  Pour modifier un fichier HTML à l’aide de l’Éditeur de l’outil Sources, le fichier HTML doit se trouver dans un espace de travail ou sous l’onglet **Remplacements.**  Consultez les sous-sections de l’article actuel :  

*   [Utilisation de l’onglet Système de fichiers pour définir un espace de travail local](#using-the-filesystem-tab-to-define-a-local-workspace)  
*   [Utilisation de l’onglet Remplacements pour remplacer les fichiers serveur par des fichiers locaux](#using-the-overrides-tab-to-override-server-files-with-local-files)  
   
Pour enregistrer les modifications, sélectionnez `Ctrl` + `S` sur Windows/Linux `Command` + `S` ou sur macOS.  Un fichier modifié est marqué par un astérisque.  
Pour trouver du texte, sélectionnez `Ctrl` + `F` sur Windows/Linux `Command` + `F` ou sur macOS.  
Pour annuler une modification, sélectionnez `Ctrl` + `Z` sur Windows/Linux `Command` + `Z` ou sur macOS.  
Pour afficher d’autres commandes lors de la modification d’un fichier HTML, dans le volet Éditeur, cliquez avec le bouton droit sur le fichier HTML.  
Vous pouvez également modifier le code HTML à l’aide d’un éditeur HTML, plutôt que de DevTools.  Par exemple, l’article [DevTools for beginners: Get started with HTML and the DOM][DevToolsBeginnersHtml] uses a website that enables HTML editing within the webpage.  

### <a name="going-to-a-line-number-or-function"></a>Accès à un numéro de ligne ou à une fonction

Pour aller à un numéro de ligne ou un symbole \(par exemple, un nom de fonction\) dans le fichier qui est ouvert dans le volet Éditeur, vous pouvez utiliser le menu Commande, plutôt que de faire défiler le fichier.

1.  Dans le **volet Navigateur,** sélectionnez les ellipses \( `...` \) \(**Autres options**\), puis **sélectionnez Ouvrir le fichier**.  Le menu Commande s’affiche.  
1.  Tapez l’un des caractères suivants :  
     
| Caractère | Nom de la commande | Objectif |  
|:--- |:--- |:--- |  
| \: | **Aller à la ligne** | Aller à un numéro de ligne.  |  
| \@ | **Go to symbol** | Go to a function.  Lorsque vous tapez, le menu Commande répertorie les fonctions qui se trouvent dans le fichier JavaScript qui est `@` ouvert dans le volet Éditeur.  |  
   
Pour plus d’informations, voir Exécuter des commandes Microsoft Edge menu de commande [DevTools.][DevToolsCommandMenuIndex]

### <a name="displaying-source-files-when-using-a-different-tool"></a>Affichage des fichiers sources lors de l’utilisation d’un autre outil

L’endroit principal pour afficher les fichiers sources dans DevTools se trouve dans **l’outil Sources.**  Mais parfois, vous devez accéder à d’autres outils, tels que **des** éléments ou une **console,** lors de l’affichage ou de la modification de vos fichiers sources.  Utilisez **l’outil Sources rapides** dans le [caisse.][DevtoolsCustomizeIndexDrawer]  

1.  Sélectionnez un outil autre que l’outil **Sources,** tel que **l’outil Éléments.**  
1.  Sélectionnez `Ctrl` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).  Le menu Commande s’ouvre.  
1.  `Quick Source`Tapez, puis sélectionnez **Afficher la source rapide.**  En bas de la fenêtre DevTools, le Panneau s’affiche, avec le **panneau Source** rapide sélectionné.  Le **panneau Source rapide** contient le dernier fichier que vous avez modifié dans l’outil **Sources,** dans une version compacte de l’éditeur de code DevTools.  
1.  Sélectionnez `Ctrl` + `P` \(Windows, Linux\) ou `Command` + `P` \(macOS\) **** pour ouvrir la boîte de dialogue Ouvrir un fichier.  
    
## <a name="using-the-debugger-pane-to-debug-javascript-code"></a>Utilisation du volet Déboguer le code JavaScript à l’aide du volet Déboguer

Utilisez le débogger JavaScript pour passer pas à pas le code JavaScript renvoyé par le serveur.  
Le débogger **inclut** le volet Débogger, ainsi que les points d’arrêt que vous définissez sur les lignes de code dans le **volet** Éditeur.

Avec le débogger, vous suivez le code pas à pas, tout en regardant les expressions JavaScript que vous spécifiez.  Observez et modifiez manuellement les valeurs des variables et indiquez automatiquement les variables qui sont dans l’étendue de l’instruction actuelle.

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="Volet Débogger de l’outil Sources  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   Volet **Débogger** de l’outil **Sources**  
:::image-end:::  

Le déboguer prend en charge les actions de débogage standard, telles que :  

*   Définition de points d’arrêt, pour suspendre le code.  
*   Code pas à pas.  
*   Affichage et modification de propriétés et de variables.  
*   En regardant les valeurs des expressions JavaScript.  
*   Affichage de la pile d’appels\ (séquence d’appels de fonction jusqu’à présent\).  
    
Le débogueur dans DevTools est conçu pour ressembler au débogueur dans [Visual Studio Code][VisualStudioCodeDocsEditorDebugging] et au débogueur dans Visual Studio [.][VisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]

Les sous-sections suivantes couvrent le débogage :  

*   [L’approche de base de l’utilisation d’un débogger](#the-basic-approach-to-using-a-debugger)  
*   [Avantages des contrôles Watch et Scope du débogger sur console.log](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)  
*   [Déboguer à Visual Studio Code directement](#debug-from-visual-studio-code-directly)  
*   [Articles sur le débogage](#articles-about-debugging)  
    
### <a name="the-basic-approach-to-using-a-debugger"></a>L’approche de base de l’utilisation d’un débogger

Pour résoudre les problèmes de code JavaScript, vous pouvez insérer des `console.log()` instructions dans le volet Éditeur. ****  Une autre approche plus puissante consiste à utiliser le débogueur de Microsoft Edge DevTools.  L’utilisation d’un débogger peut être plus simple que , une fois que vous êtes familiarisé avec `console.log()` l’approche du débogger.

Pour utiliser un débogger sur une page web, vous définissez généralement un point d’arrêt, puis vous envoyez un formulaire à partir de la page web, comme suit :

1.  Ouvrez la page web dans un nouvel onglet du navigateur.  Par exemple, ouvrez cette page web de formulaire dans un nouvel onglet : [Demo: Prise en main Debugging JavaScript with Microsoft Edge (Chromium) DevTools][GlitchMicrosoftEdgeChromiumDevtoolsDebugJsGetStarted].  
1.  Sélectionnez `F12` pour ouvrir la fenêtre **DevTools,** puis sélectionnez l’onglet **Sources.**  
1.  Dans le **volet Navigateur** \(sur la gauche\), sélectionnez l’onglet **Page,** puis sélectionnez le fichier JavaScript, tel que `get-started.js` .  
1.  Dans le **volet Éditeur,** sélectionnez un numéro de ligne près d’une ligne suspecte de code, pour définir un point d’arrêt sur cette ligne.  Dans la figure ci-dessous, un point d’arrêt est définie sur la `var sum = addend1 + addend2;` ligne.  
1.  Dans la page web, entrez des valeurs et envoyez le formulaire.  Par exemple, entrez des numéros, tels que et, puis sélectionnez le bouton Ajouter `5` `1` le numéro **1 et le numéro 2**.  
    
    Le débogger exécute le code JavaScript, puis s’interrompt au niveau du point d’arrêt.  Le débogger est désormais en mode Suspendu, afin que vous pouvez inspecter les valeurs des propriétés qui sont dans l’étendue et passer pas à pas du code.  
    
    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Entrée du mode suspendu du débogger" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        Entrée du mode suspendu du débogger  
    :::image-end:::  
    
    Dans la figure ci-dessus, nous avons ajouté les expressions de l’observation et nous avons ajouté deux `sum` `typeof sum` lignes au-delà du point d’arrêt.  
    
1.  Examinez les **** valeurs du volet Étendue, qui indiquent toutes les variables ou propriétés qui sont dans l’étendue du point d’arrêt actuel, ainsi que leurs valeurs.  Vous pouvez également ajouter des expressions dans **le volet** d’observation.  Ces expressions sont les mêmes que celles que vous écririez dans une `console.log` instruction pour déboguer votre code.  Pour exécuter des commandes JavaScript pour manipuler des données dans le contexte actuel, utilisez la **console.**  Pour ouvrir la console, sélectionnez `Esc` .  
1.  Pas à pas dans le code à **** l’aide des contrôles en haut du volet Débogger, tels que **l’étape** \( `F9` \).
    
#### <a name="see-also"></a>Voir également

*   [Commencer à déboguer JavaScript][DevtoolsGuideChromiumJavascriptIndex] - didacticiel utilisant une page web simple existante qui contient quelques contrôles de formulaire.
    
### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a>Avantages des contrôles Watch et Scope over console\.log du déboyeur  

Ces trois approches sont équivalentes :

*   Ajout temporaire des instructions et `console.log(sum)` `console.log(typeof sum)` dans le code, où se trouve `sum` l’étendue.  
*   Émission des instructions et dans le volet Console des `sum` `console.log(typeof sum)` DevTools, **** lorsque le débogueur est suspendu là où se trouve `sum` l’étendue.  
*   Définition des expressions **watch** `sum` et dans le volet `typeof sum` **Débogger.**  
    
Lorsque la variable est dans l’étendue et que sa valeur est automatiquement affichée dans la section Étendue du volet Débogger, elle est également superposée dans le volet Éditeur où elle est `sum` `sum` **** **** `sum` calculée.  Par exemple, vous n’aurez probablement pas besoin de définir une expression watch pour `sum` .

Le débogger offre un affichage et un environnement plus riches et plus flexibles qu’une `console.log` instruction.  Par exemple, dans le débogger, lorsque vous avancez dans le code, vous pouvez afficher et modifier les valeurs de toutes les propriétés et variables actuellement définies.  Vous pouvez également émettre des instructions JavaScript dans la **console,** par exemple pour modifier des valeurs dans un tableau qui est dans l’étendue.  \(Pour afficher la console, sélectionnez **Échap**.\)

Les points d’arrêt et les expressions d’observation sont conservés lorsque vous actualisez la page web.

### <a name="debug-from-visual-studio-code-directly"></a>Déboguer à Visual Studio Code directement

Pour utiliser le débogueur plus complet de Visual Studio Code au lieu du débogueur DevTools, utilisez l’extension **Microsoft Edge Tools for VS Code** for Visual Studio Code.

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="L’extension Microsoft Edge Outils de VS Code pour Visual Studio Code" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   Les **outils Microsoft Edge d’VS Code** pour Visual Studio Code  
:::image-end:::  

Cette extension permet **** d’accéder aux éléments et aux outils réseau de Microsoft Edge DevTools, à partir de Microsoft Visual Studio Code. ****  

Pour plus d’informations, [voir Visual Studio Code vue][VisualStudioCodeIndex] d’ensemble et la page GitHub Lisez-moi, Microsoft Edge [Outils][GithubMicrosoftVscodeEdgeDevtools]de développement pour Visual Studio Code .

### <a name="articles-about-debugging"></a>Articles sur le débogage

Les articles suivants couvrent le volet **Débogger** et les points d’arrêt :

*   Prise en compte du [débogage de JavaScript dans Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - Didacticiel \(avec captures d’écran\), à l’aide d’un projet simple existant.  
*   Utilisez les fonctionnalités [du][DevToolsJavaScriptReference] débogger : comment utiliser le débogger pour définir des points d’arrêt, passer du code à pas, afficher et modifier des valeurs de variables, observer des expressions JavaScript et afficher la pile d’appels.  
*   [Suspendez votre code avec des points d’arrêt :][DevToolsJavaScriptBreakpoints] comment définir des points d’arrêt de base et spécialisés dans le débogger.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools pour les débutants : mise en place de CSS | Documents Microsoft"  
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools pour les débutants : mise en place du code HTML et du dom | Documents Microsoft"  
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de commande DevTools de Microsoft Edge | Microsoft Docs"   
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Caisse : personnaliser Microsoft Edge devTools | Documents Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Modifier Microsoft Edge placement de DevTools (Undock, Dock to bottom, Dock to left) | Documents Microsoft"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Commencer à déboguer JavaScript dans Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Exécutez des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Modifier des fichiers à l'| Documents Microsoft"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles | Documents Microsoft"  
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Suspendez votre code avec des points d’arrêt | Documents Microsoft"  
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Marquer les scripts de contenu en tant qu'| Documents Microsoft"  
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Remplacer les ressources de page web avec des copies locales à l’aide Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Utiliser les fonctionnalités de débogger | Documents Microsoft"  
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Reformater un fichier JavaScript minifié avec une impression assez grande : utilisez les fonctionnalités de débogger | Documents Microsoft"  
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Ma cartographier le code prétraité sur le code source | Documents Microsoft"  
[VisualStudioCodeIndex]: ../../visual-studio-code/index.md "Visual Studio Code vue d’ensemble | Documents Microsoft"  
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Créer un didacticiel d’extension partie 2 | Documents Microsoft"  

[VisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: /visualstudio/debugger/navigating-through-code-with-the-debugger "Naviguer dans le code avec le Visual Studio débogger | Documents Microsoft"  

[VisualStudioCodeDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Débogage | Visual Studio Code"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft Edge Outils de développement Visual Studio Code | GitHub"  

[GlitchMicrosoftEdgeChromiumDevtoolsDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Démonstration : débogage Prise en main JavaScript avec Microsoft Edge (Chromium) DevTools | Documents Microsoft"  

[WhatwgHtmlSpecMulitpageOriginHtmlOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origine | HTML Standard"  

[MdnAddOnsWebextensionsContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenu | MDN"  

[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Images | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/sources) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

<!--todo: needs an accessibility review to replace "view", "see", and "look" with "display", exception is "see also" headings -->  

<!--todo: need a consistency review to replace all UI interactions with "choose" and all keyboard interactions with "select" -->  
