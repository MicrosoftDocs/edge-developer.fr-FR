---
description: Utiliser Le lanceur d’enfants pour automatiser et tester dans Microsoft Edge
title: Marionnettiste
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft Edge, développement web, développeur, outils, automatisation, test
ms.openlocfilehash: 068a2289b0e3bf8fffb49c771b83337abb79ea83
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398468"
---
# <a name="puppeteer-overview"></a>Vue d’ensemble de Puppeteer  

[Le lanceur est][|::ref1::|Main] une bibliothèque [de][NodejsMain] nœuds qui fournit une API de haut niveau pour contrôler Microsoft Edge \(Chromium\) à l’aide du protocole [DevTools][GithubChromedevtoolsProtocol].  Le lanceur lance les [navigateurs sans][WikiHeadlessBrowser] tête par défaut.  Les navigateurs sans en-tête n’affichant pas d’interface utilisateur, vous devez utiliser la ligne de commande.  Vous pouvez également configurer Le Lanceur pour qu’il exécute entièrement \(sans en-tête\) Microsoft Edge.  

Par défaut, lorsque vous installez Le lanceur d’événements, le programme d’installation télécharge une version récente de [Chromium][ChromiumHome], le navigateur open source sur qui Microsoft Edge est [également créé.][MicrosoftBlogsWindowsExperience20181206]  Si Microsoft Edge \(Chromium\) est installé, vous pouvez utiliser le logiciel [de pare-cœur.][PuppeteerApivscore]  `puppeteer-core` est une version légère de L’Explorateur qui lance une installation de navigateur existante, telle que Microsoft Edge \(Chromium\).  Pour télécharger Microsoft Edge \(Chromium\), accédez à Télécharger les canaux [Insider de Microsoft Edge.][MicrosoftedgeinsiderDownload]  

## <a name="installing-puppeteer-core"></a>Installation de la clé d’installation  

Vous pouvez `puppeteer-core` l’ajouter à votre site web ou à votre application avec l’une des commandes suivantes.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a>Lancer Microsoft Edge avec plus de cœur  

> [!NOTE]
> `puppeteer-core` s’appuie sur Node v8.9.0 ou une ultérieure.  L’exemple ci-dessous utilise ce qui est uniquement pris en charge dans `async` / `await` Node v7.6.0 ou une ultérieure.  Exécutez-la à partir de la ligne de commande pour vous assurer `node -v` que vous avez une version compatible de Node.js.  

`puppeteer-core` doivent être familiers aux utilisateurs d’autres frameworks de test de navigateur tels [que WebDriver][WebdriverChromiumMain].  Vous créez une instance du navigateur, ouvrez une page, puis manipulez-la avec l’API Dusier.  Dans l’exemple de code suivant, `puppeteer-core` lance Microsoft Edge \(Chromium\), navigue vers `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran sous le nom `example.png` .  

Copiez l’extrait de code suivant et enregistrez-le sous `example.js` .  

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

Modifiez `executablePath` pour pointer vers votre installation de Microsoft Edge \(Chromium\).  Par exemple, sur macOS, la `executablePath` canary pour Microsoft Edge doit être définie sur `/Applications/Microsoft\ Edge\ Canary.app/` .  Pour rechercher le chemin d’accès exécutable sur cette page, accédez au chemin d’accès exécutable et copiez-le ou installez le package de chemins d’accès edge avec l’une des `executablePath` `edge://version` commandes suivantes. **** [][npmEdgePaths]  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
L’exemple de code [ci-dessous][npmEdgePaths] utilise le package de chemins d’accès edge pour rechercher par programmation le chemin d’accès à votre installation de Microsoft Edge \(Chromium\) sur votre système d’exploitation.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Enfin, définissez `executablePath: EDGE_PATH` dans `example.js` .  Cliquez sur Enregistrer pour enregistrer vos modifications.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) ne fonctionne pas avec `puppeteer-core` .  Vous devez installer les [canaux Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] pour continuer à suivre cet exemple.  

Exécutez maintenant `example.js` à partir de la ligne de commande.  

```shell
node example.js
```  

`puppeteer-core` lance Microsoft Edge, navigue vers et enregistre une `https://www.microsoftedgeinsider.com` capture d’écran de la page web.  Personnalisez la taille de la capture [d’écran avec page.setViewport()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Fichier example.png produit par example.js" lightbox="./media/puppeteer-example.png":::
   Le `example.png` fichier produit par `example.js`  
:::image-end:::  

Il s’agit simplement d’un exemple simple des scénarios d’automatisation et de test activés par Leeer et `puppeteer-core` .  Pour plus d’informations sur Le jeu d’enfants et son fonctionnement, accédez [à Ce dernier.][|::ref2::|Main]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

L’équipe du développeur Microsoft Edge est enthousiaste à l’écoute de vos commentaires sur l’utilisation de Leeer `puppeteer-core` et de Microsoft Edge.  Utilisez **l’icône** Envoyer des commentaires dans microsoft Edge DevTools ou [@EdgeDevTools][TwitterIntentTweetEdgedevtools] pour faire savoir à l’équipe Microsoft Edge ce que vous en pensez.  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Icône **Envoyer des commentaires** dans Microsoft Edge DevTools  
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

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Documents Microsoft"  
<!--  [WebdriverEdgehtmlMain]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visionneuse de protocole Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge : améliorer le web grâce à des outils de collaboration open source | Blog sur l’expérience Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Projets Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Chemins d'| npm"  

[PuppeteerMain]: https://pptr.dev "Resaisie"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "plus de personnes que d’autres | Resaisie"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Resaisie"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools - Publier un tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
