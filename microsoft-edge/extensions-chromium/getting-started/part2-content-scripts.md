---
description: Insérer dynamiquement une image INSERT sous la balise Corps de page à l’aide de scripts de contenu
title: 'Didacticiel de création d’extension: partie2'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement web, html, css, javascript, développeur, extensions
ms.openlocfilehash: 48af14c33a368a3449acb88b4dfb875ad5398e7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397915"
---
# <a name="create-an-extension-tutorial-part-2"></a>Didacticiel de création d’extension: partie2  
  
[Source de package d’extension terminée pour ce partie][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a>Vue d'ensemble  

Ce didacticiel couvre les technologies d’extension suivantes.
*   Injection de bibliothèques JavaScript dans une extension  
*   Exposition des ressources d’extension aux onglets du navigateur  
*   Inclure des pages de contenu dans les onglets de navigateur existants  
*   Que les pages de contenu écoutent les messages des fenêtres publicitaires et répondent  

Vous allez apprendre à mettre à jour votre menu déroulant pour remplacer votre image de démarrage statique par un titre et un bouton HTML standard.  Ce bouton, lorsqu’il est sélectionné, transmet cette image d’étoiles, qui est incorporée dans l’extension, à la page de contenu.  Cette image est insérée dans l’onglet du navigateur actif. Pour plus d’informations, suivez les étapes ci-dessous.

1.  Supprimer l’image de la fenêtre pop-up et la remplacer par un bouton  

Tout d’abord, mettez à jour votre fichier avec une marque simple qui affiche `popup.html` un titre et un bouton.  Vous allez programmer ce bouton prochainement, mais pour l’instant, incluez simplement une référence à un fichier JavaScript `popup.js` vide.  Voici le code HTML de mise à jour.  

```html
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            body {
                width: 500px;
            }
            button {
                background-color: #336dab;
                border: none;
                color: white;
                padding: 15px 32px;
                text-align: center;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <h1>Show the NASA picture of the day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

Après la mise à jour et l’ouverture de l’extension, une fenêtre pop-up s’ouvre avec un bouton d’affichage.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html après avoir sélectionné l’icône Extension":::
   popup.html après avoir sélectionné l’icône Extension
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  Stratégie de mise à jour pour afficher l’image en haut de l’onglet du navigateur  

Une fois le bouton ajouté, la tâche suivante consiste à faire monter le fichier image en haut de la `images/stars.jpeg` page d’onglet active.  

N’oubliez pas que chaque page d’onglet s’exécute dans son propre thread. En outre, l’extension utilise un thread différent.  Tout d’abord, créez un script de contenu qui est injecté dans la page d’onglets.  Ensuite, envoyez un message à partir de votre fenêtre pop-up vers ce script de contenu en cours d’exécution sur la page d’onglet. Le script de contenu reçoit le message, qui décrit l’image à afficher.  

3. Créer le javaScript de fenêtre pop-up pour envoyer un message  

Tout d’abord, créez et ajoutez du code pour envoyer un message à votre script de contenu non encore créé que vous devez créer et injecter momentanément dans l’onglet `popup/popup.js` de votre navigateur.  Pour ce faire, le code suivant ajoute un événement à votre bouton `onclick` d’affichage de fenêtre pop-up.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

Dans `onclick` l’événement, recherchez l’onglet du navigateur actuel.  Ensuite, utilisez `chrome.tabs.sendmessage` l’API d’extension pour envoyer un message à cet onglet.  

Dans ce message, vous devez inclure l’URL de l’image que vous souhaitez afficher. Envoyez également un ID unique à affecter à l’image insérée.  Vous pouvez choisir de laisser javaScript générer l’insertion de contenu, mais pour des raisons qui deviennent apparentes ultérieurement, générez cet ID unique ici et passez-le au script de contenu non encore `popup.js` créé.  

L’extrait de code suivant décrit le code mis à jour dans `popup/popup.js` .  Passez également l’ID de l’onglet actuel, qui est utilisé plus loin dans cet article.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
    sendMessageId.onclick = function() {
        chrome.tabs.query({ active: true, currentWindow: true }, function(tabs) {
            chrome.tabs.sendMessage(
                tabs[0].id,
                {
                    url: chrome.extension.getURL("images/stars.jpeg"),
                    imageDivId: `${guidGenerator()}`,
                    tabId: tabs[0].id
                },
                function(response) {
                    window.close();
                }
            );
            function guidGenerator() {
                const S4 = function () {
                    return (((1 + Math.random()) * 0x10000) | 0).toString(16).substring(1);
                };
                return (S4() + S4() + "-" + S4() + "-" + S4() + "-" + S4() + "-" + S4() + S4() + S4());
            }
        });
    };
}
```  

4. Rendre votre fichier star.jpeg disponible à partir de n’importe quel onglet de navigateur  

Vous vous demandez probablement pourquoi, lorsque vous passez le must `images/stars.jpeg` you use the chrome Extension API `chrome.extension.getURL` instead of just passing in the relative URL without the extra prefix like in the previous section.  Par ailleurs, ce préfixe supplémentaire, renvoyé par `getUrl` l’image attachée, ressemble à ce qui suit.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

La raison est que vous injectez l’image à l’aide de `src` l’attribut de l’élément dans la page de `img` contenu.  La page de contenu s’exécute sur un thread unique qui n’est pas le même que le thread exécutant l’extension.  Vous devez exposer le fichier image statique en tant que bien web pour qu’il fonctionne correctement.  

Ajoutez une autre entrée dans le `manifest.json` fichier pour déclarer que l’image est disponible pour tous les onglets du navigateur.  Cette entrée est la suivante :\(vous devez la voir dans le fichier complet ci-dessous lorsque vous ajoutez la déclaration de script de contenu `manifest.json` à venir\).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Vous avez écrit le code dans votre fichier pour envoyer un message à la page de contenu incorporée sur la page active de l’onglet actif, mais vous n’avez pas créé et injecté cette `popup.js` page de contenu.  Faites-le maintenant.  

5.  Mettre à jour votre manifest.jspour l’accès au contenu et au web  

Mise à jour `manifest.json` qui inclut `content-scripts` le et se présente comme `web_accessible_resources` suit.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    },
    "content_scripts": [
        {
            "matches": [
              "<all_urls>"
            ],
            "js": ["lib/jquery.min.js","content-scripts/content.js"]
        }
    ],
    "web_accessible_resources": [
        "images/*.jpeg"
    ]
}
```  

La section que vous avez ajoutée est `content_scripts` .  L’attribut est définie sur , ce qui signifie que tous les fichiers sont injectés dans toutes les pages d’onglets du navigateur `matches` lorsque chaque onglet est `<all_urls>` `content_scripts` chargé.  Les types de fichiers autorisés qui peuvent être injectés sont JavaScript et CSS.  Vous avez également ajouté `libjquery.min.js` .  Vous pouvez l’inclure à partir du téléchargement mentionné en haut de la section.  

6. Ajouter jQuery et comprendre le thread associé  

Dans les scripts de contenu que vous injectez, envisagez d’utiliser jQuery \( `$` \).  Vous avez ajouté une version minifiée de jQuery et l’avez mise dans votre package d’extension en tant que `lib\jquery.min.js` .  Ces scripts de contenu s’exécutent dans des bacs à sable individuels, ce qui signifie que jQuery injecté dans la `popup.js` page n’est pas partagé avec le contenu.  

N’oubliez pas que même si javaScript est en cours d’exécution sur l’onglet du navigateur sur la page web chargée, tout contenu injecté n’y a pas accès.  Ce javaScript injecté a simplement accès au DOM réel chargé dans cet onglet de navigateur.  

7. Ajouter l’listener de message de script de contenu  

Voici ce fichier qui est injecté dans chaque page d’onglets de navigateur `content-scripts\content.js` en fonction de votre `manifest.json` `content-scripts` section.  

```javascript
chrome.runtime.onMessage.addListener(function(request, sender, sendResponse) {
    $("body").prepend(
        `<img  src="${request.url}" id="${request.imageDivId}"
               class="slide-image" /> `
    );
    $("head").prepend(
        `<style>
          .slide-image {
              height: auto;
              width: 100vw;
          }
        </style>`
    );
    $(`#${request.imageDivId}`).click(function() {
        $(`#${request.imageDivId}`).remove(`#${request.imageDivId}`);
    });
    sendResponse({ fromcontent: "This message is from content.js" });
});
```  

Notez que tout ce que fait JavaScript ci-dessus consiste à inscrire un à `listener` l’aide de la méthode `chrome.runtime.onMessage.addListener` d’API d’extension.  Ce listener attend les messages comme celui que vous avez envoyé à partir de la décrit précédemment avec la méthode `popup.js` `chrome.tabs.sendMessage` API d’extension.  

Le premier paramètre de la méthode est une fonction dont le premier paramètre, request, est les détails du `addListener` message transmis.  N’oubliez pas que lorsque vous avez utilisé la méthode, les attributs du premier paramètre sont `popup.js` `sendMessage` et `url` `imageDivId` .  

Lorsqu’un événement est géré par l’écoute, la fonction qui est le premier paramètre est exécuté.  Le premier paramètre de cette fonction est un objet qui possède des attributs attribués par `sendMessage` .  Cette fonction traite simplement les trois lignes de script jQuery.  

*   La première ligne de script insère dynamiquement dans l’en-tête DOM une section que vous devez affecter en tant que **\<style\>** `slide-image` classe à votre `img` élément.  
*   La deuxième ligne de script permet d’additioner un élément juste en dessous de l’onglet de votre navigateur avec la classe affectée, ainsi que l’ID de cet élément `img` `body` `slide-image` `imageDivId` image.  
*   La troisième ligne de script ajoute un événement qui couvre la totalité de l’image, ce qui permet à l’utilisateur de sélectionner n’importe où sur l’image et cette image est supprimée de la page \(avec son écoute `click` d’événements\).  

8. Ajouter des fonctionnalités pour supprimer l’image affichée lorsqu’elle est sélectionnée  

Maintenant, lorsque vous accédez à une page et sélectionnez votre icône **Extension,** le menu déroulant s’affiche comme suit.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html après avoir sélectionné l’icône Extension":::
   popup.html après avoir sélectionné l’icône Extension
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

Lorsque vous sélectionnez le `Display` bouton, vous obtenez ce qui se trouve ci-dessous.  Si vous sélectionnez n’importe où sur l’image, cet élément d’image est supprimé et les pages de tabulation se resserrent à ce qui était `stars.jpeg` affiché à l’origine.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Image s’affichant dans le navigateur":::
   Image s’affichant dans le navigateur
:::image-end:::

Vous avez créé une extension qui envoie avec succès un message à partir de la fenêtre pop-up de l’icône d’extension et insère dynamiquement JavaScript en cours d’exécution en tant que contenu sous l’onglet du navigateur.  Le contenu injecté définit l’élément image pour afficher vos étoiles statiques jpeg.  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Source du package d’extension | Documents Microsoft"  
