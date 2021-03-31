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
# Dramaturge  

[Playwright][|::ref1::|Main] est une bibliothèque [Node.js][NodejsMain] permettant d’automatiser le [chrome][ChromiumHome], le [Firefox][FirefoxMain]et la [WebKit][|::ref2::|Main] d’une API unique.  Playwright est conçu pour permettre l’automatisation Web sur le Web, qui est toujours compatible avec le Green, la fiabilité et la rapidité.  [Dans la mesure où Microsoft Edge repose sur la plateforme Web de chrome Open-source][MicrosoftBlogsWindowsExperience20181206], Playwright est également capable d’automatiser Microsoft Edge.  

Playwright lance les [navigateurs][WikiHeadlessBrowser] sans affichage par défaut.  Dans la plupart des navigateurs sans moniteur, vous devez utiliser la ligne de commande pour afficher une interface utilisateur.  Vous pouvez également configurer Playwright pour qu’il fonctionne comme complet \(non-headless \) Microsoft Edge.  

Par défaut, lorsque vous installez Playwright, le programme d’installation télécharge [chrome][ChromiumHome], [Firefox][FirefoxMain]et [WebKit][|::ref3::|Main].  Si Microsoft Edge \(chrome \) est également installé, Playwright a simplement besoin d’une modification de code d’une ligne pour tester votre site Web ou votre application dans Microsoft Edge.  Pour télécharger Microsoft Edge \(chrome \), accédez à [Télécharger Microsoft Edge][MicrosoftEdgeDownload].  

## Installation de Playwright  

Installez [Playwright][|::ref4::|Main] pour tester votre site Web ou votre application à l’aide de la commande suivante.  

```shell
npm i playwright
```  

## Lancer Microsoft Edge avec Playwright  

> [!NOTE]
> [Playwright][|::ref5::|Main] nécessite Node.js version 10,17 ou ultérieure. Exécutez `node -v` la commande à partir de la ligne de commande pour vérifier que vous disposez d’une version compatible d' Node.js.  Les fichiers binaires du navigateur pour Chrome, Firefox et WebKit fonctionnent sur Windows, macOS et Linux. Pour plus d’informations, accédez à la [Configuration système requise pour Playwright][PlaywrightSystemRequirements].  

Playwright doit être familier aux utilisateurs d’autres infrastructures de test de [navigateur comme le][WebDriverChromiumMain] contrôleurs Web ou [Puppeteer][PuppeteerMain].  Vous pouvez créer une instance du navigateur, ouvrir une page, puis la manipuler avec l' [API Playwright][PlaywrightAPIReference].  Dans l’extrait de code suivant, Playwright lance Microsoft Edge \(chrome \), accède à `https://www.microsoft.com/edge` et enregistre une capture d’écran sous `example.png` .  

Copiez l’extrait de code suivant et enregistrez-le sous la forme `example.js` .  

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

Changez `executablePath` de point pour qu’il pointe vers votre installation de Microsoft Edge \(chrome \).  Par exemple, sur macOS, le `executablePath` Canaries pour Microsoft Edge doit être défini sur `/Applications/Microsoft\ Edge\ Canary.app/` .  Pour trouver le `executablePath` fichier, recherchez `edge://version` et copiez le **chemin d’exécution** sur cette page, ou installez le package [Edge-Path][npmEdgePaths] à l’aide de la commande suivante.  

```shell
npm i edge-paths
```  

L’extrait de code suivant utilise le paquet [Edge-Paths][npmEdgePaths] pour trouver par programmation le chemin d’accès à votre installation de Microsoft Edge \(chrome \) sur votre système d’exploitation.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Enfin, définissez `executablePath: EDGE_PATH` `example.js` .  Cliquez sur Enregistrer pour enregistrer vos modifications.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML \) ne fonctionne pas avec Playwright.  Pour continuer à suivre cet exemple, vous devez installer [Microsoft Edge \(chrome \)][MicrosoftEdgeDownload] .  

Exécuté `example.js` à partir de la ligne de commande.  

```shell
node example.js
```  

Playwright lance Microsoft Edge, accède à `https://www.microsoft.com/edge` et enregistre une capture d’écran de la page.  Vous pouvez personnaliser la taille de la page avec [page. setViewportSize ()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="Fichier example.png produit par example.js" lightbox="../media/playwright-example.png":::
    Le `example.png` fichier obtenu par `example.js`  
:::image-end:::  

`example.js` C’est une simple démonstration des scénarios d’automatisation et de test activés par Playwright.  Pour effectuer des captures d’écran dans plusieurs navigateurs Web, modifiez le code suivant.  

*   Hexavalent  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Pour plus d’informations sur Playwright, accédez au [site Web Playwright][|::ref6::|Main].  Regardez la  [Playwright référentiel Samples][PlaywrightRepo] sur GitHub.  Pour partager vos commentaires sur l’automatisation et le test de votre site Web ou de votre application avec Playwright, il est impossible de signaler [un problème][PlaywrightRepoNewIssue].  

## Contacter l’équipe DevTools MicrosoftEdge  

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
