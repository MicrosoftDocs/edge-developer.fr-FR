---
description: Utiliser Puppeteer pour automatiser et effectuer des tests dans Microsoft Edge
title: Marionnettiste
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, développeur, outils, Automation, test
ms.openlocfilehash: e92a863f28c96157b4c7692bd88ba6884cbf8f52
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192232"
---
# Marionnettiste  

[Puppeteer][|::ref1::|Main] est une bibliothèque de [nœuds][NodejsMain] qui fournit une API de haut niveau pour contrôler Microsoft Edge \ (chrome \) à l’aide du [protocole devtools][GithubChromedevtoolsProtocol].  Puppeteer lance les [navigateurs][WikiHeadlessBrowser] sans affichage par défaut.  Dans la plupart des navigateurs sans moniteur, vous devez utiliser la ligne de commande pour afficher une interface utilisateur.  Vous pouvez également configurer Puppeteer pour qu’il fonctionne comme complet \ (non-headless \) Microsoft Edge.  

Par défaut, lorsque vous installez Puppeteer, le programme d’installation télécharge une version récente de [chrome][ChromiumHome], le navigateur open source [sur lequel Microsoft Edge est également intégré][MicrosoftBlogsWindowsExperience20181206].  S’il est installé sur votre ordinateur, vous pouvez utiliser [Puppeteer-Core][PuppeteerApivscore].  `puppeteer-core` est une version légère d’Puppeteer qui lance une installation de navigateur existante, telle que Microsoft Edge \ (chrome \).  Pour télécharger Microsoft Edge \ (chrome \), accédez à [Télécharger les canaux Microsoft Edge Insider][MicrosoftedgeinsiderDownload].  

## Installation de Puppeteer-Core  

Vous pouvez `puppeteer-core` l’ajouter à votre site Web ou à votre application en utilisant l’une des commandes suivantes.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Lancer Microsoft Edge avec Puppeteer-Core  

> [!NOTE]
> `puppeteer-core` repose sur le nœud v 8.9.0 ou une version ultérieure.  L’exemple ci-dessous utilise `async` / `await` qui est uniquement pris en charge dans le nœud v 7.6.0 ou version ultérieure.  Exécutez `node -v` la commande à partir de la ligne de commande pour vérifier que vous disposez d’une version compatible d' Node.js.  

`puppeteer-core` Familiarisez-vous aux utilisateurs d’autres infrastructures de test de navigateur comme le contrôleurs de [disque][WebDriverEdgehtmlMain].  Vous pouvez créer une instance du navigateur, ouvrir une page, puis la manipuler avec l’API Puppeteer.  Dans l’exemple de code suivant, `puppeteer-core` lance Microsoft Edge \ (chrome \), accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran sous `example.png` .  

Copiez l’extrait de code suivant et enregistrez-le sous la forme `example.js` .  

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

Changez `executablePath` de point pour qu’il pointe vers votre installation de Microsoft Edge \ (chrome \).  Par exemple, sur macOS, le `executablePath` Canaries pour Microsoft Edge doit être défini sur `/Applications/Microsoft\ Edge\ Canary.app/` .  Pour trouver le `executablePath` fichier, recherchez `edge://version` et copiez le **chemin d’exécution** sur cette page, ou installez le package [Edge-Path][npmEdgePaths] avec l’une des commandes suivantes.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
L’exemple de code ci-dessous utilise le package d' [itinéraires latéraux][npmEdgePaths] pour trouver par programmation le chemin d’accès à votre installation de Microsoft Edge \ (chrome \) sur votre système d’exploitation.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Enfin, définissez `executablePath: EDGE_PATH` `example.js` .  Cliquez sur Enregistrer pour enregistrer vos modifications.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) ne fonctionne pas `puppeteer-core` .  Pour continuer à suivre cet exemple, vous devez installer les [canaux Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] .  

À présent, exécutez `example.js` la commande à partir de la ligne de commande.  

```shell
node example.js
```  

`puppeteer-core` lance Microsoft Edge, accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran de la page Web.  Personnalisez la taille de la capture d’écran avec [page. setViewport ()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Fichier example.png produit par example.js" lightbox="./media/puppeteer-example.png":::
   Le `example.png` fichier obtenu par `example.js`  
:::image-end:::  

L’exemple simple suivant utilise des scénarios d’Automation et de test activés par Puppeteer et `puppeteer-core` .  Pour plus d’informations sur le fonctionnement de Puppeteer et son fonctionnement, accédez à [Puppeteer][|::ref2::|Main].  

## Contacter l’équipe DevTools MicrosoftEdge  

L’équipe de développeurs Microsoft Edge a hâte d’entendre vos commentaires concernant l’utilisation de Puppeteer, `puppeteer-core` et de Microsoft Edge.  Utilisez l’icône d' **envoi de commentaires** dans le Microsoft Edge devtools ou Tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] pour faire savoir à l’équipe Microsoft Edge ce que vous en pensez.  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Icône **Envoyer des commentaires** dans Microsoft Edge devtools  
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

[WebdriverChromiumMain]: ./webdriver-chromium "WebDriver (chrome) | Documents Microsoft"  
[WebdriverEdgehtmlMain]: ./webdriver.md "Web Driver (EdgeHTML) | Documents Microsoft"  

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
