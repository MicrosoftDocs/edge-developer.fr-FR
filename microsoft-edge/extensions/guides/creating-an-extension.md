---
description: Découvrir comment créer une extension Microsoft Edge
title: Créer une extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683650"
---
# Création d’une extension Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Ce guide décrit la création d’une extension pour Microsoft Edge.  Cet exemple d’extension vous permet de manipuler des feuilles de style CSS spécifiques pour [docs.Microsoft.com][MicrosoftDocs] , notamment pour vous guider dans la création d’un fichier manifeste, l’interface utilisateur et les scripts d’arrière-plan et de contenu.  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.microsoft.com Body a changé en bleu":::
   Docs.microsoft.com Body a changé en bleu
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

Ce didacticiel suppose que vous disposez d’une compréhension de base de l’extension d’un navigateur et de son fonctionnement.  Pour plus d’informations sur les blocs de construction des extensions, voir [anatomie d’une extension][MDNAnatomyExtension].  

Téléchargez le code de l' [exemple complet sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Création du fichier manifeste  

Pour commencer, créez un répertoire pour votre extension et nommez-le `color-changer` .  

Dans le `color-changer` dossier, créez un fichier nommé `manifest.json` .  Le `manifest.json` fichier est requis pour toutes les extensions et fournit des informations importantes pour l’extension, de l’extension aux autorisations.  

> [!NOTE] 
> Ce guide vous guide à travers toutes les clés de manifeste que vous devez utiliser dans ce guide, mais pour obtenir la liste de toutes les clés de manifeste prises en charge et recommandées, voir [clés de manifeste prises en charge][ExtensionsApisupportManifestKeys].  

À l’intérieur `manifest.json` , ajoutez le code suivant.  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### Définitions des clés de manifeste  

| Clé | Détails |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | Nom de l’extension.  |  
| [auteur][MDNManifestjsonAuthor] | Auteur de l’extension.  |  
| [version][MDNManifestjsonVersion] | Numéro de version de l’extension.  |  
| [description][MDNManifestjsonDescription] | Description de l’extension affichée dans la section à propos du menu extension dans Microsoft Edge.  |  
| [attribué][MDNManifestjsonPermissions] | Tableau de chaînes demandant des autorisations pour l’extension.  Pour votre extension, vous demandez des autorisations pour afficher les sites Web visités \ («onglets» \) et mettre à jour le contenu des URL correspondantes « `*://docs.microsoft.com/*` ».  |  
| [browser_action][MDNManifestjsonBrowserAction] | Contient les informations relatives à une icône. L’icône est placée sur la barre d’outils Microsoft Edge, à droite de la barre d’adresse.  |  

#### définitions de clés de browser_action  

| Clé | Détails |  
|:--- |:--- |  
| `default_icon` | Icône utilisée dans la barre d’outils.  |  
| `default_title` | Texte qui s’affiche lorsqu’un utilisateur pointe sur l’icône dans la barre d’outils.  |  
| `default_popup` | Chemin d’accès au fichier HTML de la fenêtre contextuelle.  |  

À présent que vous avez créé le fichier manifeste, vous avez besoin d’une interface utilisateur pour l’extension.  

## Création de la fenêtre contextuelle  

Pour votre extension, créez une fenêtre contextuelle pour l’interface utilisateur, comme ci-dessous.  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Interface contextuelle de l’extension":::
   Interface contextuelle de l’extension
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

Créez un fichier nommé `popup.html` à la racine de votre `color-changer` dossier.  Collez le code suivant `popup.html` .  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

Dans `popup.html` , vous créez un titre, un paragraphe et trois boutons \ (AliceBlue, Cornsilk et Reset \).  

À présent, créez un dossier nommé `css` et dans créer un fichier nommé `styles.css` .  Ajoutez les styles ci-dessous.  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

Ce code CSS donne à notre extension quelques styles de base.  N’hésitez pas à ajouter des styles pour personnaliser votre extension.  

Ensuite, vous devez créer le fichier JavaScript qui interagit avec la fenêtre contextuelle.  Créez un `js` dossier et un fichier nommé `popup.js` à l’intérieur de celui-ci.  Mettez à jour `popup.js` avec le code suivant.  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

Dans `popup.js` , l’API [Tab][MDNApiTabs] vous permet d’interagir avec les onglets du navigateur et d’injecter du texte et des styles dans le contenu de la page.  À l’aide de la méthode [Tabs. insertCSS ()][MDNApiTabsInsertcss] , vous injectez la feuille de style CSS spécifiée dans la page qui remplace l’en-tête de [docs.Microsoft.com][MicrosoftDocs] par une autre couleur lorsque l’utilisateur clique sur le bouton spécifié.  

À présent que vous disposez de la fonctionnalité contextuelle de base, ajoutez des icônes à l’extension.  

## Ajout d’icônes  

Les icônes servent à représenter l’extension dans la barre d’outils du navigateur, dans le menu extensions et dans d’autres emplacements.  Téléchargez les [icônes de votre extension sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages]. Pour plus d’informations sur les icônes d’extension dans Microsoft Edge, voir le [Guide de conception][ExtensionsGuidesDesignIcons].  

Après avoir téléchargé les icônes de l’extension, enregistrez les icônes dans un `images` dossier `color-changer` .  

L’icône qui s’affiche dans la barre d’outils est définie à l' `default_icon` intérieur de la clé de [browser_action][MDNManifestjsonBrowserAction] , que vous avez déjà ajoutée à votre fichier de manifeste dans une section antérieure.  

La `icons` clé définit les icônes qui doivent être utilisées dans les menus paramètres d’extensions.  Vous trouverez ci-dessous une sélection de plusieurs icônes de tailles différentes pour indiquer les différentes résolutions d’écran.  Le nom des icônes, et les haut-parleurs `25` `48` en pixels des icônes.  

Dans le fichier [Manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , incluez une clé de niveau supérieur pour `icons` .  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### Définitions des clés de manifeste  

| Clé | Détails |  
|:--- |:--- |  
| [icônes][MDNManifestjsonIcons] | Icônes de votre extension avec paires clé-valeur de taille d’image `px` et chemin d’image par rapport au répertoire racine de l’extension. |  

> [!NOTE]
> Utilisez les icônes `inactive##.png` situées dans le dossier images, plus loin dans ce guide.  

## Test de l’extension  

À présent que vous avez ajouté l’interface utilisateur et les icônes créées, testez votre extension.  Suivez les étapes permettant d' [Ajouter une extension][ExtensionsGuidesAddingRemovingExtensionsAdding] à Microsoft Edge.  Ensuite, revenez à ce guide.  

Une fois votre extension ajoutée, accédez à la page de [docs.Microsoft.com][MicrosoftDocs] .  La fenêtre contextuelle suivante doit apparaître après avoir cliqué sur l’action du navigateur.  La couleur du corps du [docs.Microsoft.com][MicrosoftDocs] doit également changer de couleur.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Docs.microsoft.com en-tête modifié comme AliceBlue":::
         Docs.microsoft.com en-tête modifié comme AliceBlue :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Docs.microsoft.com en-tête modifié comme Cornsilk":::
         Docs.microsoft.com en-tête modifié comme Cornsilk :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

Si vous rencontrez des erreurs ou des fonctionnalités qui ne fonctionnent pas, voir le guide des [extensions de débogage][ExtensionsGuidesDebuggingExtensions] ou télécharger l' [exemple complet sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Ajouter du contenu et des scripts d’arrière-plan  

Accédez à l’étape suivante et ajoutez de la logique pour désactiver l’extension du travail sur les pages en dehors du domaine [docs.Microsoft.com][MicrosoftDocs] .  

Vous devez d’abord créer un [script de contenu][MDNContentScripts].  Ensuite, vous devez créer des scripts de contenu qui s’exécutent dans le contexte d’une page Web particulière, qui peuvent accéder au contenu d’une page Web et peuvent communiquer avec des scripts en arrière-plan.  Dans votre `js` annuaire, créez un fichier nommé `content.js` et ajoutez le code suivant.  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

Ce script obtient l’URL de la page active `document.location.href` et vérifie si la page actuelle est sur le domaine [docs.Microsoft.com][MicrosoftDocs] .  Si la page n’est pas sur le domaine [docs.Microsoft.com][MicrosoftDocs] \ (par exemple [https://www.bing.com/][|::ref1::|] , \), les chemins d’accès aux icônes inactifs \ (icônes grisées \) sont envoyés au script en arrière-plan à l’aide de [Runtime. SendMessage ()][MDNApiRuntimeSendmessage].  

Vous devez mettre à jour le fichier [Manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] pour inclure la `content_scripts` clé suivante.  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### Définitions des clés de manifeste  

| Clé | Détails |  
|:--- |:---- |  
| [content_scripts][MDNManifestjsonContentScripts] | Contient les informations relatives aux scripts de contenu chargés par le navigateur. |  

#### définitions de clés de content_scripts  

| Clé | Détails |  
|:--- |:---- |  
| `matches` \ (obligatoire \) | Modèle d’URL à faire correspondre avant de charger le script de contenu. |  
| `js` | Le script qui doit être chargé sur les URL correspondants. |  
| `run_at` | Spécifie l’emplacement d’insertion des fichiers JavaScript de la `js` clé. |  

Ensuite, vous devez créer un [script en arrière-plan][MDNAnatomyExtensionBackgroundScripts].  Les scripts en arrière-plan s’exécutent en arrière-plan du navigateur, s’exécutent indépendamment de la durée de vie d’une fenêtre de navigateur ou de page Web, et sont en mesure de communiquer avec des scripts de contenu.  

`js`Créez un fichier nommé `background.js` et ajoutez le code suivant à l’intérieur de votre dossier.  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

La méthode [Runtime. onMessage][MDNApiRuntimeOnmessage] écoute pour [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] à partir du script de contenu.  Si le domaine de la page n’est pas [docs.Microsoft.com][MicrosoftDocs], la méthode [browserAction. seticon ()][MDNApiBrowseractionSeticon] définit les chemins d’icône vers les images inactives.  

Le script désactive également l’action du navigateur ([browserAction. Disable][MDApiBrowseractionDisable]\), de sorte que les utilisateurs ne puissent pas cliquer sur l’action du navigateur en dehors d’une page de [docs.Microsoft.com][MicrosoftDocs] .  

Vous devez ajouter le script en arrière-plan au fichier [Manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] .  Ajoutez la `background` clé suivante à votre manifeste.  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### Définitions des clés de manifeste  

| Clé | Détails|  
|:--- |:--- |  
| [arrière-plan][MDNManifestjsonBackground] | Contient les scripts en arrière-plan. |  

#### définitions des touches d’arrière-plan  

| Clé | Détails |  
|:--- |:--- |  
| `scripts` | Le chemin d’accès à un fichier JavaScript. |  
| `persistent` (obligatoire) | Ce doit être défini sur `true` ou `false` .  S' `true` il est défini sur, le script en arrière-plan est chargé et reste persistant pour la section de navigation entière.  S' `false` il est défini sur, le script en arrière-plan est chargé avec un délai et reste persistant pour la session de navigation. |  

Rechargez votre extension et testez à nouveau.  Pour recharger votre extension: cliquez sur le **...** pour obtenir les paramètres et plus d’informations dans Microsoft Edge, cliquez sur **Extensions**, cliquez sur votre extension \ (**changer de couleur**\), puis cliquez sur **recharger l’extension**.  

À présent, ouvrez un nouvel onglet ou actualisez un onglet existant qui n’est pas une page de [docs.Microsoft.com][MicrosoftDocs] .  L’icône inactif doit apparaître et ne pas pouvoir cliquer sur l’action du navigateur.  

Félicitations!  Vous avez créé une extension pour Microsoft Edge!  Affichez l' [exemple complet sur GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  Poursuivez votre lecture pour en savoir plus sur les extensions.  

## Écrire une extension plus complexe  

Vous souhaitez écrire une extension plus complexe?  Jetez un coup d’œil à l’extension Beastify sur MDN dans l’article, [votre deuxième extension][MDNYourSecondWebextension].  Le modèle d’extension pour Microsoft Edge est légèrement différent du modèle d’extension pour Firefox, l’extension Beastify créée dans [votre deuxième extension][MDNYourSecondWebextension] a été adaptée à la fonction dans Microsoft Edge.  Consultez-le sur [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].  

Lorsque vous parcourez l’article sur MDN, [votre deuxième extension][MDNYourSecondWebextension], gardez à l’esprit les sections suivantes.  

### API  

Pour obtenir la liste des API d’extensions prises en charge dans Microsoft Edge, consultez la page [API prises en charge][ExtensionsAPIsupportApis] .  

### Tailles des icônes  

Les tailles d’icône de poste par défaut pour Microsoft Edge sont `20px` ,, `25px` `30px` , et `40px` .  Les autres tailles prises en charge sont `19px` , `35px` et `38px` .  Pour plus d’informations sur les tailles d’icône et les meilleures pratiques, voir le Guide de [conception][ExtensionsGuidesDesign] .  

### JavaScript  

Le modèle d’extension pour Microsoft Edge ne prend pas en charge les promesses JavaScript.  Au lieu de cela, utilisez des rappels.  Pour consulter d’autres exemples d’utilisation des rappels dans une extension, voir les démonstrations [impression rapide][GithubMicrosoftEdgeExtensionsDemosQuickPrint] et [échange de texte][GithubMicrosoftEdgeExtensionsDemosTextSwap] .  

Passez en revue l’exemple d' [impression rapide][GithubMicrosoftEdgeExtensionsDemosQuickPrint] dans la vidéo suivante.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### Manifest. JSON  

*   La `author` clé est requise dans Microsoft Edge.  
*   La `activeTab` clé n’est pas prise en charge dans Microsoft Edge  

Pour plus d’informations sur les [extensions de navigateur][MDNBrowserExtensions], voir [documents Web MDN][MDNWebDocs].  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Ajout d’une extension: ajout, déplacement et suppression d’extensions pour Microsoft Edge | Documents Microsoft"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Extensions de débogage | Documents Microsoft"  
[ExtensionsGuidesDesign]: ./design.md "Recommandations en matière de conception pour les extensions Microsoft Edge | Documents Microsoft"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Icônes-recommandations en matière de conception pour les extensions Microsoft Edge | Documents Microsoft"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md "API prises en charge Documents Microsoft"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Clés de manifeste prises en charge | Documents Microsoft"  

[MicrosoftDocs]: https://docs.microsoft.com "Documents Microsoft"  

[MDNWebDocs]: https://developer.mozilla.org "Documents Web MDN"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Extensions de navigateur | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomie d’une extension | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Scripts en arrière-plan-anatomie d’une extension | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "browserAction. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. onMessage-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. sendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "onglets-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenu | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "auteur-manifeste. JSON | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "arrière-plan-manifeste. JSON | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest. JSON | MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Description-manifeste. JSON | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "icônes-manifeste. JSON | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "nom-manifeste. JSON | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "autorisations-manifeste. JSON | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "version-manifeste. JSON | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Votre deuxième extension | MDN"  

[Bing]: https://www.bing.com "Maps"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Changer de couleur-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Images-changement de couleur-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest. JSON-Color changer-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Impression rapide-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Échange de texte-MicrosoftEdge/MicrosoftEdge-extensions-démonstrations | GitHub"  
