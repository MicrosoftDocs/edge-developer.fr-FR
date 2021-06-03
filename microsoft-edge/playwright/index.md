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
# Dramaturge  

[La bibliothèque][|::ref1::|Main] [d'Node.js][NodejsMain] permet d’automatiser [Chromium,][ChromiumHome] [Firefox][FirefoxMain]et [WebKit][|::ref2::|Main] avec une seule API.  Cette méthode est conçue pour permettre une automatisation web cross-browser toujours verte, capable, fiable et rapide.  Étant donné Microsoft Edge est créé sur la plateforme [web open source Chromium,][MicrosoftBlogsWindowsExperience20181206]La préélable est également en mesure d’automatiser les Microsoft Edge.  

Par défaut, [l’explorateur][WikiHeadlessBrowser] lance les navigateurs sans tête.  Les navigateurs sans en-tête n’affichant pas d’interface utilisateur, vous devez utiliser la ligne de commande.  Vous pouvez également configurer la configuration de l’accès de manière à ce qu’elle s’exécute Microsoft Edge \(non sans en-tête\).  

Par défaut, lorsque vous installez Le programme d’installation télécharge [Chromium,][ChromiumHome] [Firefox][FirefoxMain]et [WebKit.][|::ref3::|Main]  Si vous avez également installé Microsoft Edge \(Chromium\), Il vous suffit de modifier le code d’une ligne pour tester votre site web ou votre application dans Microsoft Edge.  Pour télécharger Microsoft Edge \(Chromium\), [accédez][MicrosoftEdgeDownload]à Télécharger Microsoft Edge .  

## Installation de l’installation  

Installez [l’Installation][|::ref4::|Main] pour tester votre site web ou votre application avec la commande suivante.  

```shell
npm i playwright
```  

## Lancer les Microsoft Edge avec l’err.  

> [!NOTE]
> [L'Node.js][|::ref5::|Main] la version 10.17 ou supérieure. Exécutez-la à partir de la ligne de commande pour vous assurer `node -v` que vous avez une version compatible de Node.js.  Les binaires du navigateur pour Chromium, Firefox et WebKit fonctionnent sur Windows, macOS et Linux. Pour plus d’informations, [accédez à la base de données requise.][PlaywrightSystemRequirements]  

L’explorateur doit être familier aux utilisateurs d’autres frameworks de test de navigateur tels [que WebDriver][WebDriverChromiumMain] [ou Browsereer][PuppeteerMain].  Vous créez une instance du navigateur, ouvrez une page, puis vous la manipulez avec [l’API De l’api de la manipulation.][PlaywrightAPIReference]  Dans l’extrait de code suivant, La lance Microsoft Edge \(Chromium\), navigue vers et enregistre une capture d’écran sous le nom `https://www.microsoft.com/edge` `example.png` .  

Copiez l’extrait de code suivant et enregistrez-le sous `example.js` .  

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

Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).  Par exemple, sur macOS, la Microsoft Edge `executablePath` Canary doit être définie sur `/Applications/Microsoft\ Edge\ Canary.app/` .  Pour rechercher le chemin d’accès exécutable sur cette page, accédez au chemin d’accès exécutable et copiez-le ou installez le package de chemins d’accès edge à l’aide `executablePath` `edge://version` de la commande suivante. **** [][npmEdgePaths]  

```shell
npm i edge-paths
```  

L’extrait de code suivant utilise le package [de][npmEdgePaths] chemins d’accès edge pour rechercher par programme le chemin d’accès à votre installation de Microsoft Edge \(Chromium\) sur votre système d’exploitation.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Enfin, définissez `executablePath: EDGE_PATH` dans `example.js` .  Cliquez sur Enregistrer pour enregistrer vos modifications.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) ne fonctionne pas avec l’attaque.  Vous devez installer [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] pour continuer à suivre cet exemple.  

Exécutez maintenant `example.js` à partir de la ligne de commande.  

```shell
node example.js
```  

Le lancement de Microsoft Edge, permet d’accéder à la page et d’enregistrer `https://www.microsoft.com/edge` une capture d’écran de la page.  Vous pouvez personnaliser la taille de page [avec page.setViewportSize()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="Le example.png produit par example.js" lightbox="../media/playwright-example.png":::
    Le `example.png` fichier produit par `example.js`  
:::image-end:::  

`example.js` n’est qu’une simple démonstration des scénarios d’automatisation et de test activés par l’utilisateur.  Pour prendre des captures d’écran dans plusieurs navigateurs web, modifiez le code suivant.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Pour plus d’informations sur la sous-programme, accédez au [site Web De l’auteur de l’événement.][|::ref6::|Main]  Consultez le [repo De l’GitHub.][PlaywrightRepo]  Pour partager vos commentaires sur l’automatisation et le test de votre site web ou de votre application avec l’Équipe de partage, [déposez un problème.][PlaywrightRepoNewIssue]  

## Contacter l’équipe DevTools MicrosoftEdge  

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
