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
# <a name="create-an-extension-tutorial-part-2"></a><span data-ttu-id="2d675-104">Didacticiel de création d’extension: partie2</span><span class="sxs-lookup"><span data-stu-id="2d675-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="2d675-105">Source de package d’extension terminée pour ce partie</span><span class="sxs-lookup"><span data-stu-id="2d675-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a><span data-ttu-id="2d675-106">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="2d675-106">Overview</span></span>  

<span data-ttu-id="2d675-107">Ce didacticiel couvre les technologies d’extension suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d675-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="2d675-108">Injection de bibliothèques JavaScript dans une extension</span><span class="sxs-lookup"><span data-stu-id="2d675-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="2d675-109">Exposition des ressources d’extension aux onglets du navigateur</span><span class="sxs-lookup"><span data-stu-id="2d675-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="2d675-110">Inclure des pages de contenu dans les onglets de navigateur existants</span><span class="sxs-lookup"><span data-stu-id="2d675-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="2d675-111">Que les pages de contenu écoutent les messages des fenêtres publicitaires et répondent</span><span class="sxs-lookup"><span data-stu-id="2d675-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="2d675-112">Vous allez apprendre à mettre à jour votre menu déroulant pour remplacer votre image de démarrage statique par un titre et un bouton HTML standard.</span><span class="sxs-lookup"><span data-stu-id="2d675-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="2d675-113">Ce bouton, lorsqu’il est sélectionné, transmet cette image d’étoiles, qui est incorporée dans l’extension, à la page de contenu.</span><span class="sxs-lookup"><span data-stu-id="2d675-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="2d675-114">Cette image est insérée dans l’onglet du navigateur actif. Pour plus d’informations, suivez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2d675-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="2d675-115">Supprimer l’image de la fenêtre pop-up et la remplacer par un bouton</span><span class="sxs-lookup"><span data-stu-id="2d675-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="2d675-116">Tout d’abord, mettez à jour votre fichier avec une marque simple qui affiche `popup.html` un titre et un bouton.</span><span class="sxs-lookup"><span data-stu-id="2d675-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="2d675-117">Vous allez programmer ce bouton prochainement, mais pour l’instant, incluez simplement une référence à un fichier JavaScript `popup.js` vide.</span><span class="sxs-lookup"><span data-stu-id="2d675-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="2d675-118">Voici le code HTML de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2d675-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="2d675-119">Après la mise à jour et l’ouverture de l’extension, une fenêtre pop-up s’ouvre avec un bouton d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2d675-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html après avoir sélectionné l’icône Extension":::
   <span data-ttu-id="2d675-121">popup.html après avoir sélectionné l’icône Extension</span><span class="sxs-lookup"><span data-stu-id="2d675-121">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="2d675-122">Stratégie de mise à jour pour afficher l’image en haut de l’onglet du navigateur</span><span class="sxs-lookup"><span data-stu-id="2d675-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="2d675-123">Une fois le bouton ajouté, la tâche suivante consiste à faire monter le fichier image en haut de la `images/stars.jpeg` page d’onglet active.</span><span class="sxs-lookup"><span data-stu-id="2d675-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="2d675-124">N’oubliez pas que chaque page d’onglet s’exécute dans son propre thread.</span><span class="sxs-lookup"><span data-stu-id="2d675-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="2d675-125">En outre, l’extension utilise un thread différent.</span><span class="sxs-lookup"><span data-stu-id="2d675-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="2d675-126">Tout d’abord, créez un script de contenu qui est injecté dans la page d’onglets.</span><span class="sxs-lookup"><span data-stu-id="2d675-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="2d675-127">Ensuite, envoyez un message à partir de votre fenêtre pop-up vers ce script de contenu en cours d’exécution sur la page d’onglet.</span><span class="sxs-lookup"><span data-stu-id="2d675-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="2d675-128">Le script de contenu reçoit le message, qui décrit l’image à afficher.</span><span class="sxs-lookup"><span data-stu-id="2d675-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="2d675-129">Créer le javaScript de fenêtre pop-up pour envoyer un message</span><span class="sxs-lookup"><span data-stu-id="2d675-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="2d675-130">Tout d’abord, créez et ajoutez du code pour envoyer un message à votre script de contenu non encore créé que vous devez créer et injecter momentanément dans l’onglet `popup/popup.js` de votre navigateur.  Pour ce faire, le code suivant ajoute un événement à votre bouton `onclick` d’affichage de fenêtre pop-up.</span><span class="sxs-lookup"><span data-stu-id="2d675-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="2d675-131">Dans `onclick` l’événement, recherchez l’onglet du navigateur actuel.  Ensuite, utilisez `chrome.tabs.sendmessage` l’API d’extension pour envoyer un message à cet onglet.</span><span class="sxs-lookup"><span data-stu-id="2d675-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="2d675-132">Dans ce message, vous devez inclure l’URL de l’image que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="2d675-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="2d675-133">Envoyez également un ID unique à affecter à l’image insérée.</span><span class="sxs-lookup"><span data-stu-id="2d675-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="2d675-134">Vous pouvez choisir de laisser javaScript générer l’insertion de contenu, mais pour des raisons qui deviennent apparentes ultérieurement, générez cet ID unique ici et passez-le au script de contenu non encore `popup.js` créé.</span><span class="sxs-lookup"><span data-stu-id="2d675-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="2d675-135">L’extrait de code suivant décrit le code mis à jour dans `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="2d675-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="2d675-136">Passez également l’ID de l’onglet actuel, qui est utilisé plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2d675-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

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

4. <span data-ttu-id="2d675-137">Rendre votre fichier star.jpeg disponible à partir de n’importe quel onglet de navigateur</span><span class="sxs-lookup"><span data-stu-id="2d675-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="2d675-138">Vous vous demandez probablement pourquoi, lorsque vous passez le must `images/stars.jpeg` you use the chrome Extension API `chrome.extension.getURL` instead of just passing in the relative URL without the extra prefix like in the previous section.</span><span class="sxs-lookup"><span data-stu-id="2d675-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="2d675-139">Par ailleurs, ce préfixe supplémentaire, renvoyé par `getUrl` l’image attachée, ressemble à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="2d675-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="2d675-140">La raison est que vous injectez l’image à l’aide de `src` l’attribut de l’élément dans la page de `img` contenu.</span><span class="sxs-lookup"><span data-stu-id="2d675-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="2d675-141">La page de contenu s’exécute sur un thread unique qui n’est pas le même que le thread exécutant l’extension.</span><span class="sxs-lookup"><span data-stu-id="2d675-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="2d675-142">Vous devez exposer le fichier image statique en tant que bien web pour qu’il fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="2d675-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="2d675-143">Ajoutez une autre entrée dans le `manifest.json` fichier pour déclarer que l’image est disponible pour tous les onglets du navigateur.</span><span class="sxs-lookup"><span data-stu-id="2d675-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="2d675-144">Cette entrée est la suivante :\(vous devez la voir dans le fichier complet ci-dessous lorsque vous ajoutez la déclaration de script de contenu `manifest.json` à venir\).</span><span class="sxs-lookup"><span data-stu-id="2d675-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="2d675-145">Vous avez écrit le code dans votre fichier pour envoyer un message à la page de contenu incorporée sur la page active de l’onglet actif, mais vous n’avez pas créé et injecté cette `popup.js` page de contenu.</span><span class="sxs-lookup"><span data-stu-id="2d675-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="2d675-146">Faites-le maintenant.</span><span class="sxs-lookup"><span data-stu-id="2d675-146">Do that now.</span></span>  

5.  <span data-ttu-id="2d675-147">Mettre à jour votre manifest.jspour l’accès au contenu et au web</span><span class="sxs-lookup"><span data-stu-id="2d675-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="2d675-148">Mise à jour `manifest.json` qui inclut `content-scripts` le et se présente comme `web_accessible_resources` suit.</span><span class="sxs-lookup"><span data-stu-id="2d675-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="2d675-149">La section que vous avez ajoutée est `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="2d675-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="2d675-150">L’attribut est définie sur , ce qui signifie que tous les fichiers sont injectés dans toutes les pages d’onglets du navigateur `matches` lorsque chaque onglet est `<all_urls>` `content_scripts` chargé.</span><span class="sxs-lookup"><span data-stu-id="2d675-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="2d675-151">Les types de fichiers autorisés qui peuvent être injectés sont JavaScript et CSS.</span><span class="sxs-lookup"><span data-stu-id="2d675-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="2d675-152">Vous avez également ajouté `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2d675-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="2d675-153">Vous pouvez l’inclure à partir du téléchargement mentionné en haut de la section.</span><span class="sxs-lookup"><span data-stu-id="2d675-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="2d675-154">Ajouter jQuery et comprendre le thread associé</span><span class="sxs-lookup"><span data-stu-id="2d675-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="2d675-155">Dans les scripts de contenu que vous injectez, envisagez d’utiliser jQuery \( `$` \).</span><span class="sxs-lookup"><span data-stu-id="2d675-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="2d675-156">Vous avez ajouté une version minifiée de jQuery et l’avez mise dans votre package d’extension en tant que `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2d675-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="2d675-157">Ces scripts de contenu s’exécutent dans des bacs à sable individuels, ce qui signifie que jQuery injecté dans la `popup.js` page n’est pas partagé avec le contenu.</span><span class="sxs-lookup"><span data-stu-id="2d675-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="2d675-158">N’oubliez pas que même si javaScript est en cours d’exécution sur l’onglet du navigateur sur la page web chargée, tout contenu injecté n’y a pas accès.</span><span class="sxs-lookup"><span data-stu-id="2d675-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="2d675-159">Ce javaScript injecté a simplement accès au DOM réel chargé dans cet onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="2d675-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="2d675-160">Ajouter l’listener de message de script de contenu</span><span class="sxs-lookup"><span data-stu-id="2d675-160">Add the content script message listener</span></span>  

<span data-ttu-id="2d675-161">Voici ce fichier qui est injecté dans chaque page d’onglets de navigateur `content-scripts\content.js` en fonction de votre `manifest.json` `content-scripts` section.</span><span class="sxs-lookup"><span data-stu-id="2d675-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="2d675-162">Notez que tout ce que fait JavaScript ci-dessus consiste à inscrire un à `listener` l’aide de la méthode `chrome.runtime.onMessage.addListener` d’API d’extension.</span><span class="sxs-lookup"><span data-stu-id="2d675-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="2d675-163">Ce listener attend les messages comme celui que vous avez envoyé à partir de la décrit précédemment avec la méthode `popup.js` `chrome.tabs.sendMessage` API d’extension.</span><span class="sxs-lookup"><span data-stu-id="2d675-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="2d675-164">Le premier paramètre de la méthode est une fonction dont le premier paramètre, request, est les détails du `addListener` message transmis.</span><span class="sxs-lookup"><span data-stu-id="2d675-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="2d675-165">N’oubliez pas que lorsque vous avez utilisé la méthode, les attributs du premier paramètre sont `popup.js` `sendMessage` et `url` `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="2d675-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="2d675-166">Lorsqu’un événement est géré par l’écoute, la fonction qui est le premier paramètre est exécuté.</span><span class="sxs-lookup"><span data-stu-id="2d675-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="2d675-167">Le premier paramètre de cette fonction est un objet qui possède des attributs attribués par `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="2d675-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="2d675-168">Cette fonction traite simplement les trois lignes de script jQuery.</span><span class="sxs-lookup"><span data-stu-id="2d675-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="2d675-169">La première ligne de script insère dynamiquement dans l’en-tête DOM une section que vous devez affecter en tant que **\<style\>** `slide-image` classe à votre `img` élément.</span><span class="sxs-lookup"><span data-stu-id="2d675-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="2d675-170">La deuxième ligne de script permet d’additioner un élément juste en dessous de l’onglet de votre navigateur avec la classe affectée, ainsi que l’ID de cet élément `img` `body` `slide-image` `imageDivId` image.</span><span class="sxs-lookup"><span data-stu-id="2d675-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="2d675-171">La troisième ligne de script ajoute un événement qui couvre la totalité de l’image, ce qui permet à l’utilisateur de sélectionner n’importe où sur l’image et cette image est supprimée de la page \(avec son écoute `click` d’événements\).</span><span class="sxs-lookup"><span data-stu-id="2d675-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="2d675-172">Ajouter des fonctionnalités pour supprimer l’image affichée lorsqu’elle est sélectionnée</span><span class="sxs-lookup"><span data-stu-id="2d675-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="2d675-173">Maintenant, lorsque vous accédez à une page et sélectionnez votre icône **Extension,** le menu déroulant s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="2d675-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html après avoir sélectionné l’icône Extension":::
   <span data-ttu-id="2d675-175">popup.html après avoir sélectionné l’icône Extension</span><span class="sxs-lookup"><span data-stu-id="2d675-175">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="2d675-176">Lorsque vous sélectionnez le `Display` bouton, vous obtenez ce qui se trouve ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2d675-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="2d675-177">Si vous sélectionnez n’importe où sur l’image, cet élément d’image est supprimé et les pages de tabulation se resserrent à ce qui était `stars.jpeg` affiché à l’origine.</span><span class="sxs-lookup"><span data-stu-id="2d675-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Image s’affichant dans le navigateur":::
   <span data-ttu-id="2d675-179">Image s’affichant dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="2d675-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="2d675-180">Vous avez créé une extension qui envoie avec succès un message à partir de la fenêtre pop-up de l’icône d’extension et insère dynamiquement JavaScript en cours d’exécution en tant que contenu sous l’onglet du navigateur.  Le contenu injecté définit l’élément image pour afficher vos étoiles statiques jpeg.</span><span class="sxs-lookup"><span data-stu-id="2d675-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Source du package d’extension | Documents Microsoft"  
