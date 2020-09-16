---
description: Extensions mise en route partie 2
title: Insérer dynamiquement une image de la NASA sous la balise du corps de la page à l’aide de scripts de contenu
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 586f0427241e5f01b63a22ce204484dc5e8cf154
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015757"
---
# <span data-ttu-id="0ecda-104">Insérer dynamiquement une image de la NASA sous la balise du corps de la page à l’aide de scripts de contenu</span><span class="sxs-lookup"><span data-stu-id="0ecda-104">Dynamically Insert NASA Picture Below The Page Body Tag Using Content Scripts</span></span>  

<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart2]  
-->  

## <span data-ttu-id="0ecda-105">Présentation</span><span class="sxs-lookup"><span data-stu-id="0ecda-105">Overview</span></span>  

<span data-ttu-id="0ecda-106">Dans la partie 2, vous apprendrez à mettre à jour votre menu contextuel de manière à ne pas afficher l’image de l’extension statique que vous aviez auparavant, mais pour remplacer cette image par un titre et un bouton HTML standard.</span><span class="sxs-lookup"><span data-stu-id="0ecda-106">In part 2, you learn to update your pop-up menu to not show the static stars image you had before, but to replace that image with a title and a standard HTML button.</span></span>  <span data-ttu-id="0ecda-107">Lorsque cette option est sélectionnée, ce bouton transmet à la page de contenu l’image d’étoiles, qui est incorporée dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="0ecda-107">That button, when selected, passes that stars image, which is embedded in the Extension, to the content page.</span></span>  <span data-ttu-id="0ecda-108">Cette image est insérée dans l’onglet du navigateur actif.</span><span class="sxs-lookup"><span data-stu-id="0ecda-108">That image, is inserted into the active browser tab.</span></span>  

*   <span data-ttu-id="0ecda-109">Technologies d’extension abordées dans ce guide</span><span class="sxs-lookup"><span data-stu-id="0ecda-109">Extension technologies covered in this guide</span></span>  
    *   <span data-ttu-id="0ecda-110">Injection de bibliothèques JavaScript dans l’extension</span><span class="sxs-lookup"><span data-stu-id="0ecda-110">Injecting JavaScript libraries into Extension</span></span>  
    *   <span data-ttu-id="0ecda-111">Exposition des ressources d’extension aux onglets du navigateur</span><span class="sxs-lookup"><span data-stu-id="0ecda-111">Exposing Extension assets to browser tabs</span></span>  
    *   <span data-ttu-id="0ecda-112">Insertion de pages de contenu dans les onglets d’un navigateur existants</span><span class="sxs-lookup"><span data-stu-id="0ecda-112">Including content pages in existing browser tabs</span></span>  
    *   <span data-ttu-id="0ecda-113">Pour que les pages de contenu écoutent les messages des fenêtres contextuelles et répondent</span><span class="sxs-lookup"><span data-stu-id="0ecda-113">Having content pages listen for messages from pop-ups and respond</span></span>  

## <span data-ttu-id="0ecda-114">Supprimer l’image de la fenêtre contextuelle et la remplacer par un bouton</span><span class="sxs-lookup"><span data-stu-id="0ecda-114">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="0ecda-115">Tout d’abord, vous devez mettre à jour votre `popup.html` fichier à l’aide d’un balisage direct qui affiche un titre et un bouton.</span><span class="sxs-lookup"><span data-stu-id="0ecda-115">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="0ecda-116">Vous programmez ce bouton sous peu, mais pour l’instant, incluez simplement une référence à un fichier JavaScript vide `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="0ecda-116">You program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="0ecda-117">Voici le code HTML de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0ecda-117">Here is update HTML.</span></span>  

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

<span data-ttu-id="0ecda-118">Après avoir effectué la mise à jour de votre extension et sélectionné l’icône de lancement de l’extension, vous disposez des fenêtres contextuelles suivantes avec un bouton d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0ecda-118">After updating your Extension and selecting the Extension launch icon, the have the following pop-up includes a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   <span data-ttu-id="0ecda-120">Affichage popup.html après l’utilisation de l’icône d’extension</span><span class="sxs-lookup"><span data-stu-id="0ecda-120">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## <span data-ttu-id="0ecda-121">Stratégie mise à jour pour afficher une image en haut de l’onglet de navigateur</span><span class="sxs-lookup"><span data-stu-id="0ecda-121">Updated strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="0ecda-122">Après avoir ajouté le bouton, la tâche suivante consiste à ce qu’il affiche le `images/stars.jpeg` fichier image en haut de la page d’onglets actif.</span><span class="sxs-lookup"><span data-stu-id="0ecda-122">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="0ecda-123">N’oubliez pas que chaque page d’onglet possède un propre thread unique et l’extension possède un thread distinct.</span><span class="sxs-lookup"><span data-stu-id="0ecda-123">Remember, each tab page has a unique own thread and the Extension has a separate thread.</span></span>  <span data-ttu-id="0ecda-124">Par conséquent, vous devez d’abord créer un script de contenu et injecter ce script de contenu dans la page d’onglets.</span><span class="sxs-lookup"><span data-stu-id="0ecda-124">So, you must first create a content script and inject that content script into the tab page.</span></span>  <span data-ttu-id="0ecda-125">Lorsque vous procédez ainsi, vous devez envoyer un message à partir de votre fenêtre contextuelle vers le script de contenu en cours d’exécution sur la page d’onglet indiquant que le script de contenu doit apparaître et comment l’afficher.</span><span class="sxs-lookup"><span data-stu-id="0ecda-125">Once you do that, you must send a message from your pop-up to that content script running on the tab page telling that content script what image to show, and how to show it.</span></span>  

## <span data-ttu-id="0ecda-126">Création d’une fenêtre contextuelle permettant d’envoyer un message</span><span class="sxs-lookup"><span data-stu-id="0ecda-126">Creating the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="0ecda-127">Tout d’abord, créez `popup/popup.js` et ajoutez du code pour envoyer un message à votre script de contenu qui n’est pas encore créé et à insérer dans votre onglet de navigateur.  Pour ce faire, le code suivant ajoute un `onclick` événement à votre bouton d’affichage de fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="0ecda-127">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="0ecda-128">Dans l' `onclick` événement, ce que vous devez faire est l’onglet de navigateur actuel (s’il n’en existe qu’un).</span><span class="sxs-lookup"><span data-stu-id="0ecda-128">In the `onclick` event, what you must do is find the current browser tab \(if there is only one open it is that one\).</span></span>  <span data-ttu-id="0ecda-129">Ensuite, une fois que vous avez trouvé cet onglet, utilisez l' `chrome.tabs.sendmessage` API d’extension pour envoyer un message à cet onglet.</span><span class="sxs-lookup"><span data-stu-id="0ecda-129">Then, once you find that tab, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="0ecda-130">Dans ce message, vous devez inclure l’URL de l’image que vous voulez afficher, et vous voulez envoyer un ID unique qui doit être attribué à cette image insérée.</span><span class="sxs-lookup"><span data-stu-id="0ecda-130">In that message you must include the URL to the image you want to display, and you want to send a unique ID that should be assigned to that inserted image.</span></span>  <span data-ttu-id="0ecda-131">Il est possible que vous souhaitiez que le JavaScript d’insertion de contenu génère cela, mais pour des raisons qui deviennent évidentes par la suite, génère cet ID unique ici `popup.js` et le transmet au script de contenu non encore créé.</span><span class="sxs-lookup"><span data-stu-id="0ecda-131">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="0ecda-132">Voici votre fichier mis à jour `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="0ecda-132">Here is your updated `popup/popup.js` file.</span></span>  <span data-ttu-id="0ecda-133">Par ailleurs, il n’est pas possible d’utiliser l’ID de tabulation actuel dont vous devez avoir besoin dans une section ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0ecda-133">Also, pass in the current tab ID which you should need in a later section but for now, is not be used.</span></span>  

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

## <span data-ttu-id="0ecda-134">Rendre vos étoiles. jpeg disponibles à partir de n’importe quel onglet de navigateur</span><span class="sxs-lookup"><span data-stu-id="0ecda-134">Making your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="0ecda-135">Vous vous demandez probablement pourquoi, lorsque vous passez l', `images/stars.jpeg` vous devez utiliser l' `chrome.extension.getURL` API d’extension chrome au lieu de simplement transmettre l’URL relative sans le préfixe supplémentaire comme dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="0ecda-135">You are probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="0ecda-136">Par le biais du processus, le préfixe supplémentaire renvoyé par `getUrl` l’image associée ressemble à ceci.</span><span class="sxs-lookup"><span data-stu-id="0ecda-136">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="0ecda-137">C’est la raison pour laquelle vous injectez l’image en utilisant l' `src` attribut de l' `img` élément dans la page de contenu.</span><span class="sxs-lookup"><span data-stu-id="0ecda-137">The reason is that you are injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="0ecda-138">La page de contenu s’exécute sur un thread unique qui n’est pas le même que le thread exécutant l’extension.</span><span class="sxs-lookup"><span data-stu-id="0ecda-138">The content page is running on a unique thread that is not the same as the thread running the Extension.</span></span>  <span data-ttu-id="0ecda-139">Vous devez exposer le fichier image statique en tant que ressource Web pour qu’il fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="0ecda-139">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="0ecda-140">Pour ce faire, vous devez ajouter une autre entrée dans le `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="0ecda-140">To do that, you must add another entry in the `manifest.json` file.</span></span>  <span data-ttu-id="0ecda-141">Vous devez déclarer que l’image est accessible à partir de n’importe quel onglet de navigateur.  Cette entrée est la suivante: \ (vous devriez la voir dans le `manifest.json` fichier complet ci-dessous lorsque vous ajoutez la déclaration de script de contenu à paraître).</span><span class="sxs-lookup"><span data-stu-id="0ecda-141">You must declare the image to be accessible from any browser tab.  That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="0ecda-142">Vous avez à présent rédigé le code dans votre `popup.js` fichier pour envoyer un message à la page de contenu qui est incorporée sur la page d’onglet actif actuelle, mais vous n’avez pas créé et injecté cette page de contenu.</span><span class="sxs-lookup"><span data-stu-id="0ecda-142">You have now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you have not created and injected that content page.</span></span>  <span data-ttu-id="0ecda-143">Faites-le maintenant.</span><span class="sxs-lookup"><span data-stu-id="0ecda-143">Do that now.</span></span>  

## <span data-ttu-id="0ecda-144">Mise à jour de votre manifest.jspour l’accès au contenu et au Web</span><span class="sxs-lookup"><span data-stu-id="0ecda-144">Updating your manifest.json for content and web access</span></span>  

<span data-ttu-id="0ecda-145">Les mises à jour `manifest.json` incluant les `content-scripts` et `web_accessible_resources` sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ecda-145">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="0ecda-146">La section ajoutée est `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="0ecda-146">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="0ecda-147">L’attribut `matches` défini pour `<all_urls>` signifie que tous les fichiers mentionnés dans la section **content_scripts** sont injectés dans toutes les pages d’onglets du navigateur lorsque chacun d’eux est chargé.</span><span class="sxs-lookup"><span data-stu-id="0ecda-147">The attribute `matches` set to `<all_urls>` means that all the files mention in the **content_scripts** section is injected into all browser tab pages when each are loaded.</span></span>  <span data-ttu-id="0ecda-148">Les types de fichiers autorisés qui peuvent être injectés sont JavaScript et CSS.</span><span class="sxs-lookup"><span data-stu-id="0ecda-148">The allowable types of files that are able to be injected here are javascript and css.</span></span>  <span data-ttu-id="0ecda-149">Ajoutée `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0ecda-149">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="0ecda-150">Vous pouvez inclure le fichier à partir du téléchargement mentionné en haut de la section.</span><span class="sxs-lookup"><span data-stu-id="0ecda-150">You are able to include that from the download mentioned at the top of the section.</span></span>  

## <span data-ttu-id="0ecda-151">Ajout de jQuery et présentation du thread associé</span><span class="sxs-lookup"><span data-stu-id="0ecda-151">Adding jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="0ecda-152">Dans les scripts de contenu que vous injectez, planifiez à l’aide de jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="0ecda-152">In the content scripts you are injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="0ecda-153">Vous avez ajouté une version minified de jQuery et la place dans votre package d’extension `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0ecda-153">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="0ecda-154">Ces scripts s’exécutent dans un sandbox unique de tris, ce qui signifie que le jQuery injecté dans la `popup.js` page n’est pas partagé avec le contenu.</span><span class="sxs-lookup"><span data-stu-id="0ecda-154">These content scripts run in an individual sandbox of sorts, which means that the jQuery injected into the `popup.js` page does not share with the content.</span></span>  

<span data-ttu-id="0ecda-155">Gardez à l’esprit que, même si le JavaScript est en cours d’exécution sur la page Web chargée, tout contenu injecté n’y a pas accès.</span><span class="sxs-lookup"><span data-stu-id="0ecda-155">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected does not have access to that.</span></span>  <span data-ttu-id="0ecda-156">Ce code JavaScript injecté a uniquement accès au DOM réel chargé dans cet onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="0ecda-156">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

## <span data-ttu-id="0ecda-157">Ajout de l’écouteur de messages de script de contenu</span><span class="sxs-lookup"><span data-stu-id="0ecda-157">Adding the content script message listener</span></span>  

<span data-ttu-id="0ecda-158">Ce fichier est alors `content-scripts\content.js` injecté dans chaque page d’onglet de navigateur en fonction de votre `manifest.json` `content-scripts` section.</span><span class="sxs-lookup"><span data-stu-id="0ecda-158">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="0ecda-159">Notez que toutes les informations ci-dessus sont inscrites à `listener` l’aide de la `chrome.runtime.onMessage.addListener` méthode API d’extension.</span><span class="sxs-lookup"><span data-stu-id="0ecda-159">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="0ecda-160">Cet écouteur attend des messages comme celui que vous avez envoyé à partir de la `popup.js` description précédente avec la `chrome.tabs.sendMessage` méthode API d’extension.</span><span class="sxs-lookup"><span data-stu-id="0ecda-160">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="0ecda-161">Le premier paramètre de la `addListener` méthode est une fonction dont le premier paramètre, request, est le détail du message transmis.</span><span class="sxs-lookup"><span data-stu-id="0ecda-161">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="0ecda-162">Rappelez-vous que, `popup.js` lorsque vous avez utilisé la `sendMessage` méthode, les attributs du premier paramètre sont `url` et `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="0ecda-162">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="0ecda-163">Quand un événement est traité par l’écouteur, la fonction qui est le premier paramètre est exécutée.</span><span class="sxs-lookup"><span data-stu-id="0ecda-163">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="0ecda-164">Le premier paramètre de cette fonction est un objet qui comporte des attributs comme attribués par `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="0ecda-164">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="0ecda-165">Cette fonction traite simplement les trois lignes de script jQuery.</span><span class="sxs-lookup"><span data-stu-id="0ecda-165">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="0ecda-166">La première insère dynamiquement dans l’en-tête DOM une **\<style\>** section que vous devez assigner en tant que `slide-image` classe à votre `img` élément.</span><span class="sxs-lookup"><span data-stu-id="0ecda-166">The first dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="0ecda-167">Le second, ajoute un `img` élément situé juste en dessous `body` de l’onglet de votre navigateur, à laquelle la classe est affectée, ainsi que `slide-image` l' `imageDivId` ID de cet élément image.</span><span class="sxs-lookup"><span data-stu-id="0ecda-167">The second, appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="0ecda-168">Le troisième ajoute un `click` événement qui couvre la totalité de l’image, ce qui permet à l’utilisateur de sélectionner n’importe quel endroit de l’image, et cette image est supprimée de la page \ (en tant qu’écouteur d’événements).</span><span class="sxs-lookup"><span data-stu-id="0ecda-168">The third adds a `click` event that covers the entire image allowing the user to select any place on the image and that image is be removed from the page \(along with it is event listener\).</span></span>  

## <span data-ttu-id="0ecda-169">Ajout de fonctionnalités pour supprimer l’image affichée en cas de sélection</span><span class="sxs-lookup"><span data-stu-id="0ecda-169">Adding functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="0ecda-170">À présent, lorsque vous naviguez vers n’importe quelle page et sélectionnez l’icône de votre **extension** , le menu contextuel s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="0ecda-170">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="Affichage popup.html après l’utilisation de l’icône d’extension":::
   <span data-ttu-id="0ecda-172">Affichage popup.html après l’utilisation de l’icône d’extension</span><span class="sxs-lookup"><span data-stu-id="0ecda-172">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="0ecda-173">Lorsque vous sélectionnez le `Display` bouton, les informations suivantes s’afficheront.</span><span class="sxs-lookup"><span data-stu-id="0ecda-173">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="0ecda-174">Si vous sélectionnez n’importe où sur l' `stars.jpeg` image, l’élément d’image est supprimé et les pages d’onglets sont réduites à celles affichées à l’origine.</span><span class="sxs-lookup"><span data-stu-id="0ecda-174">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Image de l’affichage dans le navigateur":::
   <span data-ttu-id="0ecda-176">Image de l’affichage dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="0ecda-176">The image showing in browser</span></span>
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

<span data-ttu-id="0ecda-177">Vous avez à présent créé une extension permettant d’envoyer un message à partir de l’icône de l’extension à la fenêtre contextuelle insérée dynamiquement en tant que contenu dans l’onglet du navigateur.  Ce contenu injecté définit l’élément image pour afficher votre JPEG d’étoiles statiques.</span><span class="sxs-lookup"><span data-stu-id="0ecda-177">You have now created an Extension that successfully sends a message from the Extension icon pop-up, to the dynamically inserted JavaScript running as content on the browser tab.  That injected content set the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Source du package d’extension terminée pour cette partie | Documents Microsoft"  