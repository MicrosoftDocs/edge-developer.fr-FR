---
description: Utiliser l’accès pour automatiser et tester dans Microsoft Edge
title: Dramaturge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft Edge, développement web, développeur, outils, automatisation, test, essai, nœud, javascript, npm
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231082"
---
# <span data-ttu-id="0e771-104">Dramaturge</span><span class="sxs-lookup"><span data-stu-id="0e771-104">Playwright</span></span>  

<span data-ttu-id="0e771-105">[La bibliothèque][|::ref1::|Main] [d'Node.js][NodejsMain] permet d’automatiser [Chromium,][ChromiumHome] [Firefox][FirefoxMain]et [WebKit][|::ref2::|Main] avec une seule API.</span><span class="sxs-lookup"><span data-stu-id="0e771-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="0e771-106">Cette méthode est conçue pour permettre une automatisation web cross-browser toujours verte, capable, fiable et rapide.</span><span class="sxs-lookup"><span data-stu-id="0e771-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="0e771-107">Étant donné Microsoft Edge est créé sur la plateforme [web open source Chromium,][MicrosoftBlogsWindowsExperience20181206]La préélable est également en mesure d’automatiser les Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0e771-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="0e771-108">Par défaut, [l’explorateur][WikiHeadlessBrowser] lance les navigateurs sans tête.</span><span class="sxs-lookup"><span data-stu-id="0e771-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="0e771-109">Les navigateurs sans en-tête n’affichant pas d’interface utilisateur, vous devez utiliser la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0e771-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="0e771-110">Vous pouvez également configurer la configuration de l’accès de manière à ce qu’elle s’exécute Microsoft Edge \(non sans en-tête\).</span><span class="sxs-lookup"><span data-stu-id="0e771-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="0e771-111">Par défaut, lorsque vous installez Le programme d’installation télécharge [Chromium,][ChromiumHome] [Firefox][FirefoxMain]et [WebKit.][|::ref3::|Main]</span><span class="sxs-lookup"><span data-stu-id="0e771-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="0e771-112">Si vous avez également installé Microsoft Edge \(Chromium\), Il vous suffit de modifier le code d’une ligne pour tester votre site web ou votre application dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0e771-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="0e771-113">Pour télécharger Microsoft Edge \(Chromium\), [accédez][MicrosoftEdgeDownload]à Télécharger Microsoft Edge .</span><span class="sxs-lookup"><span data-stu-id="0e771-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="0e771-114">Installation de l’installation</span><span class="sxs-lookup"><span data-stu-id="0e771-114">Installing Playwright</span></span>  

<span data-ttu-id="0e771-115">Installez [l’Installation][|::ref4::|Main] pour tester votre site web ou votre application avec la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="0e771-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="0e771-116">Lancer les Microsoft Edge avec l’err.</span><span class="sxs-lookup"><span data-stu-id="0e771-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="0e771-117">[L'Node.js][|::ref5::|Main] la version 10.17 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="0e771-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="0e771-118">Exécutez-la à partir de la ligne de commande pour vous assurer `node -v` que vous avez une version compatible de Node.js.</span><span class="sxs-lookup"><span data-stu-id="0e771-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="0e771-119">Les binaires du navigateur pour Chromium, Firefox et WebKit fonctionnent sur Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="0e771-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="0e771-120">Pour plus d’informations, [accédez à la base de données requise.][PlaywrightSystemRequirements]</span><span class="sxs-lookup"><span data-stu-id="0e771-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="0e771-121">L’explorateur doit être familier aux utilisateurs d’autres frameworks de test de navigateur tels [que WebDriver][WebDriverChromiumMain] [ou Browsereer][PuppeteerMain].</span><span class="sxs-lookup"><span data-stu-id="0e771-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="0e771-122">Vous créez une instance du navigateur, ouvrez une page, puis vous la manipulez avec [l’API De l’api de la manipulation.][PlaywrightAPIReference]</span><span class="sxs-lookup"><span data-stu-id="0e771-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="0e771-123">Dans l’extrait de code suivant, La lance Microsoft Edge \(Chromium\), navigue vers et enregistre une capture d’écran sous le nom `https://www.microsoft.com/edge` `example.png` .</span><span class="sxs-lookup"><span data-stu-id="0e771-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="0e771-124">Copiez l’extrait de code suivant et enregistrez-le sous `example.js` .</span><span class="sxs-lookup"><span data-stu-id="0e771-124">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="0e771-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="0e771-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="0e771-126">Par exemple, sur macOS, la Microsoft Edge `executablePath` Canary doit être définie sur `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="0e771-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="0e771-127">Pour rechercher le chemin d’accès exécutable sur cette page, accédez au chemin d’accès exécutable et copiez-le ou installez le package de chemins d’accès edge à l’aide `executablePath` `edge://version` de la commande suivante. \*\*\*\* [][npmEdgePaths]</span><span class="sxs-lookup"><span data-stu-id="0e771-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="0e771-128">L’extrait de code suivant utilise le package [de][npmEdgePaths] chemins d’accès edge pour rechercher par programme le chemin d’accès à votre installation de Microsoft Edge \(Chromium\) sur votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0e771-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="0e771-129">Enfin, définissez `executablePath: EDGE_PATH` dans `example.js` .</span><span class="sxs-lookup"><span data-stu-id="0e771-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="0e771-130">Cliquez sur Enregistrer pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="0e771-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="0e771-131">Microsoft Edge \(EdgeHTML\) ne fonctionne pas avec l’attaque.</span><span class="sxs-lookup"><span data-stu-id="0e771-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="0e771-132">Vous devez installer [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] pour continuer à suivre cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0e771-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="0e771-133">Exécutez maintenant `example.js` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0e771-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="0e771-134">Le lancement de Microsoft Edge, permet d’accéder à la page et d’enregistrer `https://www.microsoft.com/edge` une capture d’écran de la page.</span><span class="sxs-lookup"><span data-stu-id="0e771-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="0e771-135">Vous pouvez personnaliser la taille de page [avec page.setViewportSize()][PlaywrightAPIPageSetViewport].</span><span class="sxs-lookup"><span data-stu-id="0e771-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="Le example.png produit par example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="0e771-137">Le `example.png` fichier produit par</span><span class="sxs-lookup"><span data-stu-id="0e771-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="0e771-138">n’est qu’une simple démonstration des scénarios d’automatisation et de test activés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e771-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="0e771-139">Pour prendre des captures d’écran dans plusieurs navigateurs web, modifiez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="0e771-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="0e771-140">Chromium</span><span class="sxs-lookup"><span data-stu-id="0e771-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="0e771-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="0e771-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="0e771-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="0e771-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="0e771-143">Pour plus d’informations sur la sous-programme, accédez au [site Web De l’auteur de l’événement.][|::ref6::|Main]</span><span class="sxs-lookup"><span data-stu-id="0e771-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="0e771-144">Consultez le [repo De l’GitHub.][PlaywrightRepo]</span><span class="sxs-lookup"><span data-stu-id="0e771-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="0e771-145">Pour partager vos commentaires sur l’automatisation et le test de votre site web ou de votre application avec l’Équipe de partage, [déposez un problème.][PlaywrightRepoNewIssue]</span><span class="sxs-lookup"><span data-stu-id="0e771-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="0e771-146">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0e771-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Documents Microsoft"  
[PuppeteerMain]: ../puppeteer/index.md "| Documents Microsoft"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge : améliorer le web grâce à des outils de collaboration open source | Blog sur l’expérience Microsoft"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Télécharger Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Projets Chromium de projet"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "chemins d'| npm"  

[PlaywrightMain]: https://playwright.dev "Resserr"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Référence de l’API d’référence sur les référence"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "page.setViewportSize(viewportSize) | Référence de l’API d’référence sur les référence"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Conditions requises pour le système d’exploitation"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Les | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Nouveau problème dans les règles de | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
