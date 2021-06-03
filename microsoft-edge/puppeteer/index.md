---
description: Utiliser Le lanceur d’enfants pour automatiser et tester dans Microsoft Edge
title: Marionnettiste
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft Edge, développement web, développeur, outils, automatisation, test
ms.openlocfilehash: 89a4dad3319f8e61f27487973509a8ee5ac23b6a
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480166"
---
# <a name="puppeteer-overview"></a><span data-ttu-id="017c5-104">Vue d’ensemble de Puppeteer</span><span class="sxs-lookup"><span data-stu-id="017c5-104">Puppeteer overview</span></span>  

<span data-ttu-id="017c5-105">[Le lanceur est][|::ref1::|Main] une bibliothèque [de][NodejsMain] nœuds qui fournit une API de haut niveau pour contrôler Microsoft Edge \(Chromium\) à l’aide du protocole [DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="017c5-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="017c5-106">Le lanceur lance les [navigateurs sans tête][WikiHeadlessBrowser] par défaut.</span><span class="sxs-lookup"><span data-stu-id="017c5-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="017c5-107">Les navigateurs sans en-tête n’affichant pas d’interface utilisateur, vous devez utiliser la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="017c5-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="017c5-108">Vous pouvez également configurer Le lanceur pour qu’il exécute l’intégralité des Microsoft Edge \(sans en-tête\).</span><span class="sxs-lookup"><span data-stu-id="017c5-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="017c5-109">Par défaut, lorsque vous installez Le lanceur d’événements, le programme d’installation télécharge une version récente de [Chromium][ChromiumHome], le navigateur open source sur Microsoft Edge est également [créé.][MicrosoftBlogsWindowsExperience20181206]</span><span class="sxs-lookup"><span data-stu-id="017c5-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="017c5-110">Si vous avez Microsoft Edge \(Chromium\) installé, vous pouvez utiliser le cœur [de l’élément.][PuppeteerApivscore]</span><span class="sxs-lookup"><span data-stu-id="017c5-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="017c5-111">est une version légère de L’Explorateur qui lance une installation de navigateur existante, comme Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="017c5-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="017c5-112">Pour télécharger Microsoft Edge \(Chromium\), accédez à [Télécharger Microsoft Edge canaux Insider.][MicrosoftedgeinsiderDownload]</span><span class="sxs-lookup"><span data-stu-id="017c5-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <a name="installing-puppeteer-core"></a><span data-ttu-id="017c5-113">Installation de la clé d’installation</span><span class="sxs-lookup"><span data-stu-id="017c5-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="017c5-114">Vous pouvez `puppeteer-core` l’ajouter à votre site web ou à votre application avec l’une des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="017c5-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a><span data-ttu-id="017c5-115">Lancer Microsoft Edge avec un cœur de lanceur</span><span class="sxs-lookup"><span data-stu-id="017c5-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="017c5-116">s’appuie sur Node v8.9.0 ou une ultérieure.</span><span class="sxs-lookup"><span data-stu-id="017c5-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="017c5-117">L’exemple ci-dessous utilise ce qui est uniquement pris en charge dans `async` / `await` Node v7.6.0 ou une ultérieure.</span><span class="sxs-lookup"><span data-stu-id="017c5-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="017c5-118">Exécutez-la à partir de la ligne de commande pour vous assurer que vous `node -v` avez une version compatible de Node.js.</span><span class="sxs-lookup"><span data-stu-id="017c5-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="017c5-119">doivent être familiers aux utilisateurs d’autres frameworks de test de navigateur tels [que WebDriver][WebdriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="017c5-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="017c5-120">Vous créez une instance du navigateur, ouvrez une page, puis manipulez-la avec l’API Duser.</span><span class="sxs-lookup"><span data-stu-id="017c5-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="017c5-121">Dans l’exemple de code suivant, lance Microsoft Edge \(Chromium\), navigue vers et enregistre une `puppeteer-core` `https://www.microsoftedgeinsider.com` capture d’écran sous le nom `example.png` .</span><span class="sxs-lookup"><span data-stu-id="017c5-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="017c5-122">Copiez l’extrait de code suivant et enregistrez-le sous `example.js` .</span><span class="sxs-lookup"><span data-stu-id="017c5-122">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="017c5-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="017c5-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="017c5-124">Par exemple, sur macOS, la Microsoft Edge `executablePath` Canary doit être définie sur `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="017c5-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="017c5-125">Pour rechercher le chemin d’accès exécutable sur cette page, accédez au chemin d’accès exécutable et copiez-le ou installez le package de chemins d’accès edge avec l’une des `executablePath` `edge://version` commandes suivantes. \*\*\*\* [][npmEdgePaths]</span><span class="sxs-lookup"><span data-stu-id="017c5-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="017c5-126">L’exemple de code [ci-dessous][npmEdgePaths] utilise le package de chemins d’accès edge pour rechercher par programmation le chemin d’accès à votre installation de Microsoft Edge \(Chromium\) sur votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="017c5-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="017c5-127">Enfin, définissez `executablePath: EDGE_PATH` dans `example.js` .</span><span class="sxs-lookup"><span data-stu-id="017c5-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="017c5-128">Cliquez sur Enregistrer pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="017c5-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="017c5-129">Microsoft Edge \(EdgeHTML\) ne fonctionne pas avec `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="017c5-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="017c5-130">Vous devez installer les canaux [Microsoft Edge Insider pour][MicrosoftedgeinsiderDownload] continuer à suivre cet exemple.</span><span class="sxs-lookup"><span data-stu-id="017c5-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="017c5-131">Exécutez maintenant `example.js` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="017c5-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="017c5-132">lance Microsoft Edge, navigue vers et enregistre une `https://www.microsoftedgeinsider.com` capture d’écran de la page web.</span><span class="sxs-lookup"><span data-stu-id="017c5-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="017c5-133">Personnalisez la taille de la capture [d’écran avec page.setViewport()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="017c5-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Fichier example.png produit par example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="017c5-135">Le `example.png` fichier produit par</span><span class="sxs-lookup"><span data-stu-id="017c5-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="017c5-136">Il s’agit simplement d’un exemple simple des scénarios d’automatisation et de test activés par Leeer et `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="017c5-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="017c5-137">Pour plus d’informations sur Le jeu d’enfants et son fonctionnement, accédez [à Ce dernier.][|::ref2::|Main]</span><span class="sxs-lookup"><span data-stu-id="017c5-137">For more information about Puppeteer and how it works, navigate to [Puppeteer][|::ref2::|Main].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="017c5-138">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="017c5-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="017c5-139">L’équipe Microsoft Edge développeur est enthousiaste à l’écoute de vos commentaires sur l’utilisation de L’éditeur de logiciels, `puppeteer-core` et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="017c5-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="017c5-140">Utilisez **l’icône** Envoyer des commentaires dans Microsoft Edge devTools ou @EdgeDevTools [tweet][TwitterIntentTweetEdgedevtools] pour faire savoir à l’équipe Microsoft Edge ce que vous en pensez.</span><span class="sxs-lookup"><span data-stu-id="017c5-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="017c5-142">Icône **Envoyer des commentaires** dans le Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="017c5-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]  
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

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Documents Microsoft"  

<!--  [ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visionneuse de protocole Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge : améliorer le web grâce à des outils de collaboration open source | Blog sur l’expérience Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Projets Chromium de projet"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Chemins d'| npm"  

[PuppeteerMain]: https://pptr.dev "Resaisie"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "plus de personnes que d’autres | Resaisie"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Resaisie"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools - Publier un tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
