---
description: Extensions mise en route partie 2
title: Insérer dynamiquement une image de la NASA sous la balise du corps de la page à l’aide de scripts de contenu
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: fd2276c069116a7f69f06ae50f201e284b60f3ea
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016728"
---
# Insérer dynamiquement une image de la NASA sous la balise du corps de la page à l’aide de scripts de contenu  

<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart2]  
-->  

## Présentation  

Dans la partie 2, vous apprendrez à mettre à jour votre menu contextuel de manière à ne pas afficher l’image de l’extension statique que vous aviez auparavant, mais pour remplacer cette image par un titre et un bouton HTML standard.  Lorsque cette option est sélectionnée, ce bouton transmet à la page de contenu l’image d’étoiles, qui est incorporée dans l’extension.  Cette image est insérée dans l’onglet du navigateur actif.  

*   Technologies d’extension abordées dans ce guide  
    *   Injection de bibliothèques JavaScript dans l’extension  
    *   Exposition des ressources d’extension aux onglets du navigateur  
    *   Insertion de pages de contenu dans les onglets d’un navigateur existants  
    *   Pour que les pages de contenu écoutent les messages des fenêtres contextuelles et répondent  

## Supprimer l’image de la fenêtre contextuelle et la remplacer par un bouton  

Tout d’abord, vous devez mettre à jour votre `popup.html` fichier à l’aide d’un balisage direct qui affiche un titre et un bouton.  Vous programmerez ce bouton sous peu, mais pour l’instant, incluez simplement une référence à un fichier JavaScript vide `popup.js` .  Voici le code HTML de mise à jour.  

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
        <h1>Show the NASA Picture of the Day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

Après avoir effectué la mise à jour de votre extension et sélectionné l’icône de lancement de l’extension, vous disposez des fenêtres contextuelles suivantes avec un bouton d’affichage.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   Affichage popup.html après l’utilisation de l’icône d’extension
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## Stratégie mise à jour pour afficher une image en haut de l’onglet de navigateur  

Après avoir ajouté le bouton, la tâche suivante consiste à ce qu’il affiche le `images/stars.jpeg` fichier image en haut de la page d’onglets actif.  

N’oubliez pas que chaque page d’onglet possède un propre thread unique et l’extension possède un thread distinct.  Par conséquent, vous devez d’abord créer un script de contenu et injecter ce script de contenu dans la page d’onglets.  Lorsque vous procédez ainsi, vous devez envoyer un message à partir de votre fenêtre contextuelle vers le script de contenu en cours d’exécution sur la page d’onglet indiquant que le script de contenu doit apparaître et comment l’afficher.  

## Création d’une fenêtre contextuelle permettant d’envoyer un message  

Tout d’abord, créez `popup/popup.js` et ajoutez du code pour envoyer un message à votre script de contenu qui n’est pas encore créé et à insérer dans votre onglet de navigateur.  Pour ce faire, le code suivant ajoute un `onclick` événement à votre bouton d’affichage de fenêtre contextuelle.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

Dans l' `onclick` événement, ce que vous devez faire est l’onglet de navigateur actuel (s’il n’en existe qu’un).  Ensuite, une fois que vous avez trouvé cet onglet, utilisez l' `chrome.tabs.sendmessage` API d’extension pour envoyer un message à cet onglet.  

Dans ce message, vous devez inclure l’URL de l’image que vous voulez afficher, et vous voulez envoyer un ID unique qui doit être attribué à cette image insérée.  Il est possible que vous souhaitiez que le JavaScript d’insertion de contenu génère cela, mais pour des raisons qui deviennent évidentes par la suite, génère cet ID unique ici `popup.js` et le transmet au script de contenu non encore créé.  

Voici votre fichier mis à jour `popup/popup.js` .  Par ailleurs, il n’est pas possible d’utiliser l’ID de tabulation actuel dont vous devez avoir besoin dans une section ultérieure.  

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

## Rendre vos étoiles. jpeg disponibles à partir de n’importe quel onglet de navigateur  

Vous vous demandez probablement pourquoi, lorsque vous passez l', `images/stars.jpeg` vous devez utiliser l' `chrome.extension.getURL` API d’extension chrome au lieu de simplement transmettre l’URL relative sans le préfixe supplémentaire comme dans la section précédente.  Par le biais du processus, le préfixe supplémentaire renvoyé par `getUrl` l’image associée ressemble à ceci.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

C’est la raison pour laquelle vous injectez l’image en utilisant l' `src` attribut de l' `img` élément dans la page de contenu.  La page de contenu s’exécute sur un thread unique qui n’est pas le même que le thread exécutant l’extension.  Vous devez exposer le fichier image statique en tant que ressource Web pour qu’il fonctionne correctement.  

Pour ce faire, vous devez ajouter une autre entrée dans le `manifest.json` fichier.  Vous devez déclarer que l’image est accessible à partir de n’importe quel onglet de navigateur.  Cette entrée est la suivante: \ (vous devriez la voir dans le `manifest.json` fichier complet ci-dessous lorsque vous ajoutez la déclaration de script de contenu à paraître).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Vous avez à présent rédigé le code dans votre `popup.js` fichier pour envoyer un message à la page de contenu qui est incorporée sur la page d’onglet actif actuelle, mais vous n’avez pas créé et injecté cette page de contenu.  Faites-le maintenant.  

## Mise à jour de votre manifest.jspour l’accès au contenu et au Web  

Les mises à jour `manifest.json` incluant les `content-scripts` et `web_accessible_resources` sont les suivantes.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day.",
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

La section ajoutée est `content_scripts` .  L’attribut `matches` défini pour `<all_urls>` signifie que tous les fichiers mentionnés dans la section **content_scripts** sont injectés dans toutes les pages d’onglets du navigateur lorsque chacun d’eux est chargé.  Les types de fichiers autorisés qui peuvent être injectés sont JavaScript et CSS.  Ajoutée `libjquery.min.js` .  Vous pouvez inclure le fichier à partir du téléchargement mentionné en haut de la section.  

## Ajout de jQuery et présentation du thread associé  

Dans les scripts de contenu que vous injectez, planifiez à l’aide de jQuery \ ( `$` \).  Vous avez ajouté une version minified de jQuery et la place dans votre package d’extension `lib\jquery.min.js` .  Ces scripts s’exécutent dans un sandbox unique de tris, ce qui signifie que le jQuery injecté dans la `popup.js` page n’est pas partagé avec le contenu.  

Gardez à l’esprit que, même si le JavaScript est en cours d’exécution sur la page Web chargée, tout contenu injecté n’y a pas accès.  Ce code JavaScript injecté a uniquement accès au DOM réel chargé dans cet onglet de navigateur.  

## Ajout de l’écouteur de messages de script de contenu  

Ce fichier est alors `content-scripts\content.js` injecté dans chaque page d’onglet de navigateur en fonction de votre `manifest.json` `content-scripts` section.  

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

Notez que toutes les informations ci-dessus sont inscrites à `listener` l’aide de la `chrome.runtime.onMessage.addListener` méthode API d’extension.  Cet écouteur attend des messages comme celui que vous avez envoyé à partir de la `popup.js` description précédente avec la `chrome.tabs.sendMessage` méthode API d’extension.  

Le premier paramètre de la `addListener` méthode est une fonction dont le premier paramètre, request, est le détail du message transmis.  Rappelez-vous que, `popup.js` lorsque vous avez utilisé la `sendMessage` méthode, les attributs du premier paramètre sont `url` et `imageDivId` .  

Quand un événement est traité par l’écouteur, la fonction qui est le premier paramètre est exécutée.  Le premier paramètre de cette fonction est un objet qui comporte des attributs comme attribués par `sendMessage` .  Cette fonction traite simplement les trois lignes de script jQuery.  

*   La première insère dynamiquement dans l’en-tête DOM une **\<style\>** section que vous devez assigner en tant que `slide-image` classe à votre `img` élément.  
*   Le second, ajoute un `img` élément situé juste en dessous `body` de l’onglet de votre navigateur, à laquelle la classe est affectée, ainsi que `slide-image` l' `imageDivId` ID de cet élément image.  
*   Le troisième ajoute un `click` événement qui couvre la totalité de l’image, ce qui permet à l’utilisateur de sélectionner n’importe quel endroit de l’image, et cette image est supprimée de la page \ (en tant qu’écouteur d’événements).  

## Ajout de fonctionnalités pour supprimer l’image affichée en cas de sélection  

À présent, lorsque vous naviguez vers n’importe quelle page et sélectionnez l’icône de votre **extension** , le menu contextuel s’affiche comme suit.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   Affichage popup.html après l’utilisation de l’icône d’extension
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

Lorsque vous sélectionnez le `Display` bouton, les informations suivantes s’afficheront.  Si vous sélectionnez n’importe où sur l' `stars.jpeg` image, l’élément d’image est supprimé et les pages d’onglets sont réduites à celles affichées à l’origine.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Image de l’affichage dans le navigateur":::
   Image de l’affichage dans le navigateur
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

Vous avez à présent créé une extension permettant d’envoyer un message à partir de l’icône de l’extension à la fenêtre contextuelle insérée dynamiquement en tant que contenu dans l’onglet du navigateur.  Ce contenu injecté définit l’élément image pour afficher votre JPEG d’étoiles statiques.  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Source du package d’extension terminée pour cette partie | Documents Microsoft"  
