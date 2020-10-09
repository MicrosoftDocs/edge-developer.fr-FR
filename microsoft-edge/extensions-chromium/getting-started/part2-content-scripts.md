---
description: Insérer dynamiquement une image de la NASA sous la balise du corps de la page à l’aide de scripts de contenu
title: Didacticiel Création de l’extension 2e partie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 755b70635c93d7331ef3ac985625ba7ac5689679
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104713"
---
# Didacticiel Création de l’extension 2e partie  
  
[Source du package d’extension terminée pour cette partie][ArchiveExtensionGettingStartedPart2]    

## Vue d'ensemble  

Ce didacticiel traite des technologies d’extension suivantes.
*   Injection de bibliothèques JavaScript dans l’extension  
*   Exposition des ressources d’extension aux onglets du navigateur  
*   Insertion de pages de contenu dans les onglets d’un navigateur existants  
*   Pour que les pages de contenu écoutent les messages des fenêtres contextuelles et répondent  

Vous apprendrez à mettre à jour votre menu contextuel pour remplacer votre image de début statique par un titre et un bouton HTML standard.  Lorsque cette option est sélectionnée, ce bouton transmet à la page de contenu l’image d’étoiles, qui est incorporée dans l’extension.  Cette image est insérée dans l’onglet du navigateur actif. Pour plus d’informations, suivez les étapes ci-dessous.

1.  Supprimer l’image de la fenêtre contextuelle et la remplacer par un bouton  

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
        <h1>Show the NASA picture of the day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

Après avoir mis à jour et ouvert l’extension, une fenêtre contextuelle s’ouvre avec un bouton d’affichage.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   Affichage popup.html après l’utilisation de l’icône d’extension
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  Stratégie de mise à jour pour afficher une image en haut de l’onglet de navigateur  

Après avoir ajouté le bouton, la tâche suivante consiste à ce qu’il affiche le `images/stars.jpeg` fichier image en haut de la page d’onglets actif.  

N’oubliez pas que chaque page d’onglet s’exécute dans son propre thread. Par ailleurs, l’extension utilise un thread différent.  Tout d’abord, créez un script de contenu injecté dans la page d’onglets.  Ensuite, envoyez un message à partir de votre fenêtre contextuelle au script de contenu en cours d’exécution sur la page d’onglets. Le script de contenu reçoit le message qui décrit l’image qui doit être affichée.  

3. Créer une fenêtre contextuelle permettant d’envoyer un message  

Tout d’abord, créez `popup/popup.js` et ajoutez du code pour envoyer un message à votre script de contenu qui n’est pas encore créé et à insérer dans votre onglet de navigateur.  Pour ce faire, le code suivant ajoute un `onclick` événement à votre bouton d’affichage de fenêtre contextuelle.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

Dans l' `onclick` événement, recherchez l’onglet de navigateur actuel.  Utilisez ensuite l' `chrome.tabs.sendmessage` API d’extension pour envoyer un message à cet onglet.  

Dans ce message, vous devez inclure l’URL de l’image que vous voulez afficher. Vous pouvez également envoyer un ID unique à affecter à l’image insérée.  Il est possible que vous souhaitiez que le JavaScript d’insertion de contenu génère cela, mais pour des raisons qui deviennent évidentes par la suite, génère cet ID unique ici `popup.js` et le transmet au script de contenu non encore créé.  

L’extrait de code suivant décrit le code mis à jour dans `popup/popup.js` .  Par ailleurs, transmettez l’ID de la tabulation actuelle, qui est utilisé plus loin dans cet article.  

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

4. Rendez vos étoiles. jpeg disponibles à partir de n’importe quel onglet de navigateur  

Vous vous demandez probablement pourquoi, lorsque vous passez l', `images/stars.jpeg` vous devez utiliser l' `chrome.extension.getURL` API d’extension chrome au lieu de simplement transmettre l’URL relative sans le préfixe supplémentaire comme dans la section précédente.  Par le biais du processus, le préfixe supplémentaire renvoyé par `getUrl` l’image associée ressemble à ceci.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

C’est la raison pour laquelle vous injectez l’image en utilisant l' `src` attribut de l' `img` élément dans la page de contenu.  La page de contenu s’exécute sur un thread unique qui n’est pas le même que le thread exécutant l’extension.  Vous devez exposer le fichier image statique en tant que ressource Web pour qu’il fonctionne correctement.  

Ajoutez une autre entrée dans le `manifest.json` fichier pour déclarer que l’image est disponible pour tous les onglets du navigateur.  Cette entrée est la suivante: \ (vous devriez la voir dans le `manifest.json` fichier complet ci-dessous lorsque vous ajoutez la déclaration de script de contenu à paraître).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Vous avez à présent rédigé le code dans votre `popup.js` fichier pour envoyer un message à la page de contenu qui est incorporée sur la page d’onglet actif actuelle, mais vous n’avez pas encore créé et injecté cette page de contenu.  Faites-le maintenant.  

5.  Mettre à jour votre manifest.jspour le contenu et l’accès au Web  

Les mises à jour `manifest.json` incluant les `content-scripts` et `web_accessible_resources` sont les suivantes.  

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

La section ajoutée est `content_scripts` .  L' `matches` attribut est défini sur `<all_urls>` , ce qui signifie que tous les fichiers dans `content_scripts` sont injectés dans toutes les pages d’onglets du navigateur lorsque chaque onglet est chargé.  Les types de fichiers autorisés qui peuvent être injectés sont JavaScript et CSS.  Ajoutée `libjquery.min.js` .  Vous pouvez inclure le fichier à partir du téléchargement mentionné en haut de la section.  

6. Ajouter jQuery et présentation du thread associé  

Dans les scripts de contenu que vous injectez, planifiez à l’aide de jQuery \ ( `$` \).  Vous avez ajouté une version minified de jQuery et la place dans votre package d’extension `lib\jquery.min.js` .  Ces scripts de contenu s’exécutent dans des sandbox individuels, ce qui signifie que la fonction jQuery injectée dans la `popup.js` page n’est pas partagée avec le contenu.  

Gardez à l’esprit que, même si le JavaScript est en cours d’exécution sur la page Web chargée, tout contenu injecté n’y a pas accès.  Ce code JavaScript injecté a uniquement accès au DOM réel chargé dans cet onglet de navigateur.  

7. Ajouter l’écouteur de messages de script de contenu  

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

*   La première ligne de script insère dynamiquement dans l’en-tête DOM une **\<style\>** section que vous devez assigner en tant que `slide-image` classe à votre `img` élément.  
*   La deuxième ligne de script ajoute un `img` élément juste en dessous `body` de l’onglet de votre navigateur, à laquelle la `slide-image` classe est affectée et l' `imageDivId` ID de cet élément image.  
*   La troisième ligne de script ajoute un `click` événement qui recouvre l’intégralité de l’image, ce qui permet à l’utilisateur de sélectionner n’importe où sur l’image et cette image est supprimée de la page \ (en tant qu’écouteur d’événements).  

8. Ajouter une fonctionnalité pour supprimer l’image affichée lors de la sélection  

À présent, lorsque vous naviguez vers n’importe quelle page et sélectionnez l’icône de votre **extension** , le menu contextuel s’affiche comme suit.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   Affichage popup.html après l’utilisation de l’icône d’extension
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

Lorsque vous sélectionnez le `Display` bouton, les informations suivantes s’afficheront.  Si vous sélectionnez n’importe où sur l' `stars.jpeg` image, l’élément d’image est supprimé et les pages d’onglets sont réduites à celles affichées à l’origine.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension"  
