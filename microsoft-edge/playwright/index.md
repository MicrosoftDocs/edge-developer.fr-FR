---
description: Utiliser Playwright pour automatiser et effectuer des tests dans Microsoft Edge
title: Dramaturge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, développeur, outils, Automation, test, Playwright, nœud, JavaScript, NPM
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231082"
---
# <span data-ttu-id="92079-104">Dramaturge</span><span class="sxs-lookup"><span data-stu-id="92079-104">Playwright</span></span>  

<span data-ttu-id="92079-105">[Playwright][|::ref1::|Main] est une bibliothèque [Node.js][NodejsMain] permettant d’automatiser le [chrome][ChromiumHome], le [Firefox][FirefoxMain]et la [WebKit][|::ref2::|Main] d’une API unique.</span><span class="sxs-lookup"><span data-stu-id="92079-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="92079-106">Playwright est conçu pour permettre l’automatisation Web sur le Web, qui est toujours compatible avec le Green, la fiabilité et la rapidité.</span><span class="sxs-lookup"><span data-stu-id="92079-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="92079-107">[Dans la mesure où Microsoft Edge repose sur la plateforme Web de chrome Open-source][MicrosoftBlogsWindowsExperience20181206], Playwright est également capable d’automatiser Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92079-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="92079-108">Playwright lance les [navigateurs][WikiHeadlessBrowser] sans affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="92079-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="92079-109">Dans la plupart des navigateurs sans moniteur, vous devez utiliser la ligne de commande pour afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92079-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="92079-110">Vous pouvez également configurer Playwright pour qu’il fonctionne comme complet \ (non-headless \) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92079-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="92079-111">Par défaut, lorsque vous installez Playwright, le programme d’installation télécharge [chrome][ChromiumHome], [Firefox][FirefoxMain]et [WebKit][|::ref3::|Main].</span><span class="sxs-lookup"><span data-stu-id="92079-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="92079-112">Si Microsoft Edge \ (chrome \) est également installé, Playwright a simplement besoin d’une modification de code d’une ligne pour tester votre site Web ou votre application dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92079-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="92079-113">Pour télécharger Microsoft Edge \ (chrome \), accédez à [Télécharger Microsoft Edge][MicrosoftEdgeDownload].</span><span class="sxs-lookup"><span data-stu-id="92079-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="92079-114">Installation de Playwright</span><span class="sxs-lookup"><span data-stu-id="92079-114">Installing Playwright</span></span>  

<span data-ttu-id="92079-115">Installez [Playwright][|::ref4::|Main] pour tester votre site Web ou votre application à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="92079-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="92079-116">Lancer Microsoft Edge avec Playwright</span><span class="sxs-lookup"><span data-stu-id="92079-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="92079-117">[Playwright][|::ref5::|Main] nécessite Node.js version 10,17 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="92079-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="92079-118">Exécutez `node -v` la commande à partir de la ligne de commande pour vérifier que vous disposez d’une version compatible d' Node.js.</span><span class="sxs-lookup"><span data-stu-id="92079-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="92079-119">Les fichiers binaires du navigateur pour Chrome, Firefox et WebKit fonctionnent sur Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="92079-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="92079-120">Pour plus d’informations, accédez à la [Configuration système requise pour Playwright][PlaywrightSystemRequirements].</span><span class="sxs-lookup"><span data-stu-id="92079-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="92079-121">Playwright doit être familier aux utilisateurs d’autres infrastructures de test de [navigateur comme le][WebDriverChromiumMain] contrôleurs Web ou [Puppeteer][PuppeteerMain].</span><span class="sxs-lookup"><span data-stu-id="92079-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="92079-122">Vous pouvez créer une instance du navigateur, ouvrir une page, puis la manipuler avec l' [API Playwright][PlaywrightAPIReference].</span><span class="sxs-lookup"><span data-stu-id="92079-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="92079-123">Dans l’extrait de code suivant, Playwright lance Microsoft Edge \ (chrome \), accède à `https://www.microsoft.com/edge` et enregistre une capture d’écran sous `example.png` .</span><span class="sxs-lookup"><span data-stu-id="92079-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="92079-124">Copiez l’extrait de code suivant et enregistrez-le sous la forme `example.js` .</span><span class="sxs-lookup"><span data-stu-id="92079-124">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const { chromium } = require('playwright');

(async () => {
  const browser = await chromium.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoft.com/edge');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="92079-125">Changez `executablePath` de point pour qu’il pointe vers votre installation de Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="92079-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="92079-126">Par exemple, sur macOS, le `executablePath` Canaries pour Microsoft Edge doit être défini sur `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="92079-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="92079-127">Pour trouver le `executablePath` fichier, recherchez `edge://version` et copiez le **chemin d’exécution** sur cette page, ou installez le package [Edge-Path][npmEdgePaths] à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="92079-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="92079-128">L’extrait de code suivant utilise le paquet [Edge-Paths][npmEdgePaths] pour trouver par programmation le chemin d’accès à votre installation de Microsoft Edge \ (chrome \) sur votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92079-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="92079-129">Enfin, définissez `executablePath: EDGE_PATH` `example.js` .</span><span class="sxs-lookup"><span data-stu-id="92079-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="92079-130">Cliquez sur Enregistrer pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="92079-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="92079-131">Microsoft Edge \ (EdgeHTML \) ne fonctionne pas avec Playwright.</span><span class="sxs-lookup"><span data-stu-id="92079-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="92079-132">Pour continuer à suivre cet exemple, vous devez installer [Microsoft Edge \ (chrome \)][MicrosoftEdgeDownload] .</span><span class="sxs-lookup"><span data-stu-id="92079-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="92079-133">Exécuté `example.js` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="92079-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="92079-134">Playwright lance Microsoft Edge, accède à `https://www.microsoft.com/edge` et enregistre une capture d’écran de la page.</span><span class="sxs-lookup"><span data-stu-id="92079-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="92079-135">Vous pouvez personnaliser la taille de la page avec [page. setViewportSize ()][PlaywrightAPIPageSetViewport].</span><span class="sxs-lookup"><span data-stu-id="92079-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="Fichier example.png produit par example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="92079-137">Le `example.png` fichier obtenu par</span><span class="sxs-lookup"><span data-stu-id="92079-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="92079-138">C’est une simple démonstration des scénarios d’automatisation et de test activés par Playwright.</span><span class="sxs-lookup"><span data-stu-id="92079-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="92079-139">Pour effectuer des captures d’écran dans plusieurs navigateurs Web, modifiez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="92079-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="92079-140">Hexavalent</span><span class="sxs-lookup"><span data-stu-id="92079-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="92079-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="92079-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="92079-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="92079-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="92079-143">Pour plus d’informations sur Playwright, accédez au [site Web Playwright][|::ref6::|Main].</span><span class="sxs-lookup"><span data-stu-id="92079-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="92079-144">Regardez la  [Playwright référentiel Samples][PlaywrightRepo] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="92079-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="92079-145">Pour partager vos commentaires sur l’automatisation et le test de votre site Web ou de votre application avec Playwright, il est impossible de signaler [un problème][PlaywrightRepoNewIssue].</span><span class="sxs-lookup"><span data-stu-id="92079-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="92079-146">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="92079-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (chrome) | Documents Microsoft"  
[PuppeteerMain]: ../puppeteer/index.md "Puppeteer | Documents Microsoft"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: améliorez le Web grâce à une collaboration en ligne plus ouverte | Blog sur l’interface Microsoft"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Télécharger Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chrome | Projets de chrome"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "bords-tracés | NPM"  

[PlaywrightMain]: https://playwright.dev "Playwright"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Référence sur les API Playwright"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "page. setViewportSize (viewportSize) | Référence sur les API Playwright"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Configuration requise pour Playwright"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Playwright | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Nouveau problème dans Playwright référentiel Samples | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"  
