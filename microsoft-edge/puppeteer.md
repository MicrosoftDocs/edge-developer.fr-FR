---
description: Utiliser Puppeteer pour automatiser et effectuer des tests dans Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, développeur, outils, Automation, test
ms.openlocfilehash: ccca46426a006651a417a22e54c8b528834b5f81
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844011"
---
# <span data-ttu-id="0de05-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="0de05-104">Puppeteer</span></span>  

<span data-ttu-id="0de05-105">[Puppeteer][|::ref1::|Main] est une bibliothèque de [nœuds][NodejsMain] qui fournit une API de haut niveau pour contrôler Microsoft Edge \ (chrome \) sur le [protocole devtools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="0de05-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library which provides a high-level API to control Microsoft Edge \(Chromium\) over the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="0de05-106">Puppeteer exécute [headless][WikiHeadlessBrowser] par défaut, ce qui signifie que vous ne voyez pas d’interface utilisateur et que vous devez utiliser la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0de05-106">Puppeteer runs [headless][WikiHeadlessBrowser] by default, which means that you do not see a UI, and instead must use the command-line.</span></span>  <span data-ttu-id="0de05-107">Vous pouvez également configurer Puppeteer pour qu’il exécute le complet \ (non-headless \) Microsoft Edge ou chrome.</span><span class="sxs-lookup"><span data-stu-id="0de05-107">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge or Chromium as well.</span></span>  

<span data-ttu-id="0de05-108">Par défaut, lorsque vous installez Puppeteer, le programme d’installation télécharge une version récente de [chrome][ChromiumHome], le navigateur open source [sur lequel Microsoft Edge est également intégré][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="0de05-108">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="0de05-109">S’il est installé sur votre ordinateur, vous pouvez utiliser [Puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="0de05-109">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="0de05-110">est une version légère d’Puppeteer qui lance une installation de navigateur existante, telle que Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="0de05-110">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="0de05-111">Pour télécharger Microsoft Edge \ (chrome \), voir [Télécharger les canaux Microsoft Edge Insider][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="0de05-111">To download Microsoft Edge \(Chromium\), see [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>

## <span data-ttu-id="0de05-112">Installation de Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="0de05-112">Installing puppeteer-core</span></span>  

<span data-ttu-id="0de05-113">Vous pouvez `puppeteer-core` l’ajouter à votre site Web ou à votre application en utilisant l’une des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0de05-113">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="0de05-114">Lancer Microsoft Edge avec Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="0de05-114">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="0de05-115">repose sur le nœud v 8.9.0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0de05-115">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="0de05-116">L’exemple ci-dessous utilise `async` / `await` qui est uniquement pris en charge dans le nœud v 7.6.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0de05-116">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="0de05-117">Exécutez `node -v` la commande à partir de la ligne de commande pour vérifier que vous disposez d’une version compatible d' Node.js.</span><span class="sxs-lookup"><span data-stu-id="0de05-117">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="0de05-118">Familiarisez-vous aux utilisateurs d’autres infrastructures de test de navigateur comme le contrôleurs de [disque][WebDriverEdgehtmlMain]Web.</span><span class="sxs-lookup"><span data-stu-id="0de05-118">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="0de05-119">Vous pouvez créer une instance du navigateur, ouvrir une page, puis la manipuler avec l’API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="0de05-119">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="0de05-120">Dans l’exemple de code suivant, `puppeteer-core` lance Microsoft Edge \ (chrome \), accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran sous `example.png` .</span><span class="sxs-lookup"><span data-stu-id="0de05-120">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="0de05-121">Copiez l’exemple de code ci-dessous et enregistrez-le sous la forme `example.js` .</span><span class="sxs-lookup"><span data-stu-id="0de05-121">Copy the code sample below and save it as `example.js`.</span></span>  

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

<span data-ttu-id="0de05-122">Changez `executablePath` de point pour qu’il pointe vers votre installation de Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="0de05-122">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="0de05-123">Par exemple, sur macOS, le `executablePath` Canaries pour Microsoft Edge doit être défini sur `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="0de05-123">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="0de05-124">Pour trouver le `executablePath` fichier, recherchez `edge://version` et copiez le **chemin d’exécution** sur cette page, ou installez le package [Edge-Path][npmEdgePaths] avec l’une des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0de05-124">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="0de05-125">L’exemple de code ci-dessous utilise le package d' [itinéraires latéraux][npmEdgePaths] pour trouver par programmation le chemin d’accès à votre installation de Microsoft Edge \ (chrome \) sur votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0de05-125">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="0de05-126">Enfin, définissez `executablePath: EDGE_PATH` `example.js` .</span><span class="sxs-lookup"><span data-stu-id="0de05-126">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="0de05-127">Cliquez sur Enregistrer pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="0de05-127">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="0de05-128">Microsoft Edge \ (EdgeHTML \) ne fonctionne pas `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="0de05-128">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="0de05-129">Pour continuer à suivre cet exemple, vous devez installer les [canaux Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] .</span><span class="sxs-lookup"><span data-stu-id="0de05-129">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="0de05-130">Exécuté `example.js` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0de05-130">Now run `example.js` from the command-line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="0de05-131">lance Microsoft Edge, accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran 800px x 600px de la page.</span><span class="sxs-lookup"><span data-stu-id="0de05-131">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com` and saves an 800px x 600px screenshot of the page.</span></span>  <span data-ttu-id="0de05-132">Vous pouvez personnaliser la taille de la page avec [page. setViewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="0de05-132">You are able to customize the page size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Fichier example.png produit par example.js":::
   <span data-ttu-id="0de05-134">Figure 1: `example.png` fichier obtenu par</span><span class="sxs-lookup"><span data-stu-id="0de05-134">Figure 1:  The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

<span data-ttu-id="0de05-135">Voici un exemple simple de scénarios d’Automation et de test activés par Puppeteer et `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="0de05-135">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="0de05-136">Pour plus d’informations sur le fonctionnement de Puppeteer et son fonctionnement, voir [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="0de05-136">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="0de05-137">Envoyer des commentaires</span><span class="sxs-lookup"><span data-stu-id="0de05-137">Send Feedback</span></span>  

<span data-ttu-id="0de05-138">L’équipe de développement Edge est impatient d’entendre vos commentaires concernant l’utilisation de Puppeteer, `puppeteer-core` et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0de05-138">The Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="0de05-139">Utilisez l’icône d' **envoi de commentaires** dans le Microsoft Edge devtools ou Tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] pour faire savoir à l’équipe Microsoft Edge ce que vous en pensez.</span><span class="sxs-lookup"><span data-stu-id="0de05-139">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools":::
   <span data-ttu-id="0de05-141">Figure 2: icône de **Commentaires** dans le Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="0de05-141">Figure 2:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
> ##### Figure 2  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The Feedback icon in the Microsoft Edge DevTools](./devtools-guide-chromium/media/devtools-feedback.png)  
-->  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge: Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- image links -->  

<!-- links -->  

[WebdriverChromiumMain]: ./webdriver-chromium.md "Web Driver (chrome)"  
[WebdriverEdgehtmlMain]: ./webdriver.md "WebDriver (EdgeHTML)"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visionneuse de protocole chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: améliorer davantage le Web grâce à une collaboration plus ouverte sur le Web Blog sur l’interface Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[ChromiumHome]: https://www.chromium.org/Home "Chrome | Projets de chrome"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "NPM | Tracés latéraux"

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Puppeteer et Puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page. setViewport (fenêtre d’affichage) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-publiez un tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"  
