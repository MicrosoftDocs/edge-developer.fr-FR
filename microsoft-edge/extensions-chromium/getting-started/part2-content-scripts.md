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
# <span data-ttu-id="064e5-104">Didacticiel Création de l’extension 2e partie</span><span class="sxs-lookup"><span data-stu-id="064e5-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="064e5-105">Source du package d’extension terminée pour cette partie</span><span class="sxs-lookup"><span data-stu-id="064e5-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <span data-ttu-id="064e5-106">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="064e5-106">Overview</span></span>  

<span data-ttu-id="064e5-107">Ce didacticiel traite des technologies d’extension suivantes.</span><span class="sxs-lookup"><span data-stu-id="064e5-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="064e5-108">Injection de bibliothèques JavaScript dans l’extension</span><span class="sxs-lookup"><span data-stu-id="064e5-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="064e5-109">Exposition des ressources d’extension aux onglets du navigateur</span><span class="sxs-lookup"><span data-stu-id="064e5-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="064e5-110">Insertion de pages de contenu dans les onglets d’un navigateur existants</span><span class="sxs-lookup"><span data-stu-id="064e5-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="064e5-111">Pour que les pages de contenu écoutent les messages des fenêtres contextuelles et répondent</span><span class="sxs-lookup"><span data-stu-id="064e5-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="064e5-112">Vous apprendrez à mettre à jour votre menu contextuel pour remplacer votre image de début statique par un titre et un bouton HTML standard.</span><span class="sxs-lookup"><span data-stu-id="064e5-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="064e5-113">Lorsque cette option est sélectionnée, ce bouton transmet à la page de contenu l’image d’étoiles, qui est incorporée dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="064e5-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="064e5-114">Cette image est insérée dans l’onglet du navigateur actif. Pour plus d’informations, suivez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="064e5-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="064e5-115">Supprimer l’image de la fenêtre contextuelle et la remplacer par un bouton</span><span class="sxs-lookup"><span data-stu-id="064e5-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="064e5-116">Tout d’abord, vous devez mettre à jour votre `popup.html` fichier à l’aide d’un balisage direct qui affiche un titre et un bouton.</span><span class="sxs-lookup"><span data-stu-id="064e5-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="064e5-117">Vous programmerez ce bouton sous peu, mais pour l’instant, incluez simplement une référence à un fichier JavaScript vide `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="064e5-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="064e5-118">Voici le code HTML de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="064e5-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="064e5-119">Après avoir mis à jour et ouvert l’extension, une fenêtre contextuelle s’ouvre avec un bouton d’affichage.</span><span class="sxs-lookup"><span data-stu-id="064e5-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   <span data-ttu-id="064e5-121">Affichage popup.html après l’utilisation de l’icône d’extension</span><span class="sxs-lookup"><span data-stu-id="064e5-121">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="064e5-122">Stratégie de mise à jour pour afficher une image en haut de l’onglet de navigateur</span><span class="sxs-lookup"><span data-stu-id="064e5-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="064e5-123">Après avoir ajouté le bouton, la tâche suivante consiste à ce qu’il affiche le `images/stars.jpeg` fichier image en haut de la page d’onglets actif.</span><span class="sxs-lookup"><span data-stu-id="064e5-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="064e5-124">N’oubliez pas que chaque page d’onglet s’exécute dans son propre thread.</span><span class="sxs-lookup"><span data-stu-id="064e5-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="064e5-125">Par ailleurs, l’extension utilise un thread différent.</span><span class="sxs-lookup"><span data-stu-id="064e5-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="064e5-126">Tout d’abord, créez un script de contenu injecté dans la page d’onglets.</span><span class="sxs-lookup"><span data-stu-id="064e5-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="064e5-127">Ensuite, envoyez un message à partir de votre fenêtre contextuelle au script de contenu en cours d’exécution sur la page d’onglets.</span><span class="sxs-lookup"><span data-stu-id="064e5-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="064e5-128">Le script de contenu reçoit le message qui décrit l’image qui doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="064e5-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="064e5-129">Créer une fenêtre contextuelle permettant d’envoyer un message</span><span class="sxs-lookup"><span data-stu-id="064e5-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="064e5-130">Tout d’abord, créez `popup/popup.js` et ajoutez du code pour envoyer un message à votre script de contenu qui n’est pas encore créé et à insérer dans votre onglet de navigateur.  Pour ce faire, le code suivant ajoute un `onclick` événement à votre bouton d’affichage de fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="064e5-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="064e5-131">Dans l' `onclick` événement, recherchez l’onglet de navigateur actuel.  Utilisez ensuite l' `chrome.tabs.sendmessage` API d’extension pour envoyer un message à cet onglet.</span><span class="sxs-lookup"><span data-stu-id="064e5-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="064e5-132">Dans ce message, vous devez inclure l’URL de l’image que vous voulez afficher.</span><span class="sxs-lookup"><span data-stu-id="064e5-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="064e5-133">Vous pouvez également envoyer un ID unique à affecter à l’image insérée.</span><span class="sxs-lookup"><span data-stu-id="064e5-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="064e5-134">Il est possible que vous souhaitiez que le JavaScript d’insertion de contenu génère cela, mais pour des raisons qui deviennent évidentes par la suite, génère cet ID unique ici `popup.js` et le transmet au script de contenu non encore créé.</span><span class="sxs-lookup"><span data-stu-id="064e5-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="064e5-135">L’extrait de code suivant décrit le code mis à jour dans `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="064e5-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="064e5-136">Par ailleurs, transmettez l’ID de la tabulation actuelle, qui est utilisé plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="064e5-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

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

4. <span data-ttu-id="064e5-137">Rendez vos étoiles. jpeg disponibles à partir de n’importe quel onglet de navigateur</span><span class="sxs-lookup"><span data-stu-id="064e5-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="064e5-138">Vous vous demandez probablement pourquoi, lorsque vous passez l', `images/stars.jpeg` vous devez utiliser l' `chrome.extension.getURL` API d’extension chrome au lieu de simplement transmettre l’URL relative sans le préfixe supplémentaire comme dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="064e5-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="064e5-139">Par le biais du processus, le préfixe supplémentaire renvoyé par `getUrl` l’image associée ressemble à ceci.</span><span class="sxs-lookup"><span data-stu-id="064e5-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="064e5-140">C’est la raison pour laquelle vous injectez l’image en utilisant l' `src` attribut de l' `img` élément dans la page de contenu.</span><span class="sxs-lookup"><span data-stu-id="064e5-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="064e5-141">La page de contenu s’exécute sur un thread unique qui n’est pas le même que le thread exécutant l’extension.</span><span class="sxs-lookup"><span data-stu-id="064e5-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="064e5-142">Vous devez exposer le fichier image statique en tant que ressource Web pour qu’il fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="064e5-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="064e5-143">Ajoutez une autre entrée dans le `manifest.json` fichier pour déclarer que l’image est disponible pour tous les onglets du navigateur.</span><span class="sxs-lookup"><span data-stu-id="064e5-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="064e5-144">Cette entrée est la suivante: \ (vous devriez la voir dans le `manifest.json` fichier complet ci-dessous lorsque vous ajoutez la déclaration de script de contenu à paraître).</span><span class="sxs-lookup"><span data-stu-id="064e5-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="064e5-145">Vous avez à présent rédigé le code dans votre `popup.js` fichier pour envoyer un message à la page de contenu qui est incorporée sur la page d’onglet actif actuelle, mais vous n’avez pas encore créé et injecté cette page de contenu.</span><span class="sxs-lookup"><span data-stu-id="064e5-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="064e5-146">Faites-le maintenant.</span><span class="sxs-lookup"><span data-stu-id="064e5-146">Do that now.</span></span>  

5.  <span data-ttu-id="064e5-147">Mettre à jour votre manifest.jspour le contenu et l’accès au Web</span><span class="sxs-lookup"><span data-stu-id="064e5-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="064e5-148">Les mises à jour `manifest.json` incluant les `content-scripts` et `web_accessible_resources` sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="064e5-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="064e5-149">La section ajoutée est `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="064e5-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="064e5-150">L' `matches` attribut est défini sur `<all_urls>` , ce qui signifie que tous les fichiers dans `content_scripts` sont injectés dans toutes les pages d’onglets du navigateur lorsque chaque onglet est chargé.</span><span class="sxs-lookup"><span data-stu-id="064e5-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="064e5-151">Les types de fichiers autorisés qui peuvent être injectés sont JavaScript et CSS.</span><span class="sxs-lookup"><span data-stu-id="064e5-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="064e5-152">Ajoutée `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="064e5-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="064e5-153">Vous pouvez inclure le fichier à partir du téléchargement mentionné en haut de la section.</span><span class="sxs-lookup"><span data-stu-id="064e5-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="064e5-154">Ajouter jQuery et présentation du thread associé</span><span class="sxs-lookup"><span data-stu-id="064e5-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="064e5-155">Dans les scripts de contenu que vous injectez, planifiez à l’aide de jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="064e5-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="064e5-156">Vous avez ajouté une version minified de jQuery et la place dans votre package d’extension `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="064e5-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="064e5-157">Ces scripts de contenu s’exécutent dans des sandbox individuels, ce qui signifie que la fonction jQuery injectée dans la `popup.js` page n’est pas partagée avec le contenu.</span><span class="sxs-lookup"><span data-stu-id="064e5-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="064e5-158">Gardez à l’esprit que, même si le JavaScript est en cours d’exécution sur la page Web chargée, tout contenu injecté n’y a pas accès.</span><span class="sxs-lookup"><span data-stu-id="064e5-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="064e5-159">Ce code JavaScript injecté a uniquement accès au DOM réel chargé dans cet onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="064e5-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="064e5-160">Ajouter l’écouteur de messages de script de contenu</span><span class="sxs-lookup"><span data-stu-id="064e5-160">Add the content script message listener</span></span>  

<span data-ttu-id="064e5-161">Ce fichier est alors `content-scripts\content.js` injecté dans chaque page d’onglet de navigateur en fonction de votre `manifest.json` `content-scripts` section.</span><span class="sxs-lookup"><span data-stu-id="064e5-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="064e5-162">Notez que toutes les informations ci-dessus sont inscrites à `listener` l’aide de la `chrome.runtime.onMessage.addListener` méthode API d’extension.</span><span class="sxs-lookup"><span data-stu-id="064e5-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="064e5-163">Cet écouteur attend des messages comme celui que vous avez envoyé à partir de la `popup.js` description précédente avec la `chrome.tabs.sendMessage` méthode API d’extension.</span><span class="sxs-lookup"><span data-stu-id="064e5-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="064e5-164">Le premier paramètre de la `addListener` méthode est une fonction dont le premier paramètre, request, est le détail du message transmis.</span><span class="sxs-lookup"><span data-stu-id="064e5-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="064e5-165">Rappelez-vous que, `popup.js` lorsque vous avez utilisé la `sendMessage` méthode, les attributs du premier paramètre sont `url` et `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="064e5-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="064e5-166">Quand un événement est traité par l’écouteur, la fonction qui est le premier paramètre est exécutée.</span><span class="sxs-lookup"><span data-stu-id="064e5-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="064e5-167">Le premier paramètre de cette fonction est un objet qui comporte des attributs comme attribués par `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="064e5-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="064e5-168">Cette fonction traite simplement les trois lignes de script jQuery.</span><span class="sxs-lookup"><span data-stu-id="064e5-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="064e5-169">La première ligne de script insère dynamiquement dans l’en-tête DOM une **\<style\>** section que vous devez assigner en tant que `slide-image` classe à votre `img` élément.</span><span class="sxs-lookup"><span data-stu-id="064e5-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="064e5-170">La deuxième ligne de script ajoute un `img` élément juste en dessous `body` de l’onglet de votre navigateur, à laquelle la `slide-image` classe est affectée et l' `imageDivId` ID de cet élément image.</span><span class="sxs-lookup"><span data-stu-id="064e5-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="064e5-171">La troisième ligne de script ajoute un `click` événement qui recouvre l’intégralité de l’image, ce qui permet à l’utilisateur de sélectionner n’importe où sur l’image et cette image est supprimée de la page \ (en tant qu’écouteur d’événements).</span><span class="sxs-lookup"><span data-stu-id="064e5-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="064e5-172">Ajouter une fonctionnalité pour supprimer l’image affichée lors de la sélection</span><span class="sxs-lookup"><span data-stu-id="064e5-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="064e5-173">À présent, lorsque vous naviguez vers n’importe quelle page et sélectionnez l’icône de votre **extension** , le menu contextuel s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="064e5-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   <span data-ttu-id="064e5-175">Affichage popup.html après l’utilisation de l’icône d’extension</span><span class="sxs-lookup"><span data-stu-id="064e5-175">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="064e5-176">Lorsque vous sélectionnez le `Display` bouton, les informations suivantes s’afficheront.</span><span class="sxs-lookup"><span data-stu-id="064e5-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="064e5-177">Si vous sélectionnez n’importe où sur l' `stars.jpeg` image, l’élément d’image est supprimé et les pages d’onglets sont réduites à celles affichées à l’origine.</span><span class="sxs-lookup"><span data-stu-id="064e5-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   <span data-ttu-id="064e5-179">Image de l’affichage dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="064e5-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="064e5-180">Vous avez créé une extension permettant d’envoyer un message à partir de l’icône de l’extension, et de l’insérer de manière dynamique en tant que contenu dans l’onglet du navigateur.  Le contenu injecté définit l’élément image pour afficher votre JPEG d’étoiles statiques.</span><span class="sxs-lookup"><span data-stu-id="064e5-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Source du package d’extension terminée | Documents Microsoft"  
