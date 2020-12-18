---
description: Utiliser Puppeteer pour automatiser et effectuer des tests dans Microsoft Edge
title: Marionnettiste
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, développeur, outils, Automation, test
ms.openlocfilehash: 99d873a9b3988cb8a2827ecc9a69d574a196b037
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232830"
---
# <span data-ttu-id="9d1c7-104">Présentation de Puppeteer</span><span class="sxs-lookup"><span data-stu-id="9d1c7-104">Puppeteer overview</span></span>  

<span data-ttu-id="9d1c7-105">[Puppeteer][|::ref1::|Main] est une bibliothèque de [nœuds][NodejsMain] qui fournit une API de haut niveau pour contrôler Microsoft Edge \ (chrome \) à l’aide du [protocole devtools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="9d1c7-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="9d1c7-106">Puppeteer lance les [navigateurs][WikiHeadlessBrowser] sans affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="9d1c7-107">Dans la plupart des navigateurs sans moniteur, vous devez utiliser la ligne de commande pour afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="9d1c7-108">Vous pouvez également configurer Puppeteer pour qu’il fonctionne comme complet \ (non-headless \) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="9d1c7-109">Par défaut, lorsque vous installez Puppeteer, le programme d’installation télécharge une version récente de [chrome][ChromiumHome], le navigateur open source [sur lequel Microsoft Edge est également intégré][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="9d1c7-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="9d1c7-110">S’il est installé sur votre ordinateur, vous pouvez utiliser [Puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="9d1c7-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="9d1c7-111">est une version légère d’Puppeteer qui lance une installation de navigateur existante, telle que Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="9d1c7-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="9d1c7-112">Pour télécharger Microsoft Edge \ (chrome \), accédez à [Télécharger les canaux Microsoft Edge Insider][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="9d1c7-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <span data-ttu-id="9d1c7-113">Installation de Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="9d1c7-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="9d1c7-114">Vous pouvez `puppeteer-core` l’ajouter à votre site Web ou à votre application en utilisant l’une des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="9d1c7-115">Lancer Microsoft Edge avec Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="9d1c7-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="9d1c7-116">repose sur le nœud v 8.9.0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="9d1c7-117">L’exemple ci-dessous utilise `async` / `await` qui est uniquement pris en charge dans le nœud v 7.6.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="9d1c7-118">Exécutez `node -v` la commande à partir de la ligne de commande pour vérifier que vous disposez d’une version compatible d' Node.js.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="9d1c7-119">Familiarisez-vous aux utilisateurs d’autres infrastructures de test de navigateur comme le contrôleurs de [disque][WebdriverChromiumMain]Web.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="9d1c7-120">Vous pouvez créer une instance du navigateur, ouvrir une page, puis la manipuler avec l’API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="9d1c7-121">Dans l’exemple de code suivant, `puppeteer-core` lance Microsoft Edge \ (chrome \), accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran sous `example.png` .</span><span class="sxs-lookup"><span data-stu-id="9d1c7-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="9d1c7-122">Copiez l’extrait de code suivant et enregistrez-le sous la forme `example.js` .</span><span class="sxs-lookup"><span data-stu-id="9d1c7-122">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="9d1c7-123">Changez `executablePath` de point pour qu’il pointe vers votre installation de Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="9d1c7-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="9d1c7-124">Par exemple, sur macOS, le `executablePath` Canaries pour Microsoft Edge doit être défini sur `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="9d1c7-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="9d1c7-125">Pour trouver le `executablePath` fichier, recherchez `edge://version` et copiez le **chemin d’exécution** sur cette page, ou installez le package [Edge-Path][npmEdgePaths] avec l’une des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="9d1c7-126">L’exemple de code ci-dessous utilise le package d' [itinéraires latéraux][npmEdgePaths] pour trouver par programmation le chemin d’accès à votre installation de Microsoft Edge \ (chrome \) sur votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="9d1c7-127">Enfin, définissez `executablePath: EDGE_PATH` `example.js` .</span><span class="sxs-lookup"><span data-stu-id="9d1c7-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="9d1c7-128">Cliquez sur Enregistrer pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="9d1c7-129">Microsoft Edge \ (EdgeHTML \) ne fonctionne pas `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="9d1c7-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="9d1c7-130">Pour continuer à suivre cet exemple, vous devez installer les [canaux Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] .</span><span class="sxs-lookup"><span data-stu-id="9d1c7-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="9d1c7-131">À présent, exécutez `example.js` la commande à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="9d1c7-132">lance Microsoft Edge, accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran de la page Web.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="9d1c7-133">Personnalisez la taille de la capture d’écran avec [page. setViewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="9d1c7-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Fichier example.png produit par example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="9d1c7-135">Le `example.png` fichier obtenu par</span><span class="sxs-lookup"><span data-stu-id="9d1c7-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="9d1c7-136">Voici un exemple simple de scénarios d’Automation et de test activés par Puppeteer et `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="9d1c7-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="9d1c7-137">Pour plus d’informations sur le fonctionnement de Puppeteer et son fonctionnement, voir [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="9d1c7-137">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="9d1c7-138">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="9d1c7-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="9d1c7-139">L’équipe de développeurs Microsoft Edge a hâte d’entendre vos commentaires concernant l’utilisation de Puppeteer, `puppeteer-core` et de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="9d1c7-140">Utilisez l’icône d' **envoi de commentaires** dans le Microsoft Edge devtools ou Tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] pour faire savoir à l’équipe Microsoft Edge ce que vous en pensez.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="9d1c7-142">Icône **Envoyer des commentaires** dans Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9d1c7-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge:  Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (chrome) | Documents Microsoft"  
<!--  [WebdriverEdgehtmlMain]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visionneuse de protocole chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: améliorez le Web grâce à une collaboration en ligne plus ouverte | Blog sur l’interface Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[ChromiumHome]: https://www.chromium.org/Home "Chrome | Projets de chrome"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Tracés d’arête | NPM"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Puppeteer et Puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page. setViewport (fenêtre d’affichage) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-publiez un tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"  
