---
description: Fonctionnalités ajoutées au DevTools Microsoft Edge (chrome) en mars 2019
title: Nouveautés de Microsoft Edge (chrome) DevTools en mars 2019
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/23/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0b592eddbd68b3bbd8ff0a9edf9a1253bd79677e
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182511"
---
# <span data-ttu-id="30708-104">Nouveautés de Microsoft Edge (chrome) DevTools</span><span class="sxs-lookup"><span data-stu-id="30708-104">What's new in the Microsoft Edge (Chromium) DevTools</span></span>

<span data-ttu-id="30708-105">Nous vous remercions d’avoir essayé une version d’évaluation du nouveau Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="30708-105">Thank you so much for trying out a preview of the new Microsoft Edge!</span></span> <span data-ttu-id="30708-106">Avec cette version, nous avons entrepris une équipe majeure dans la plateforme Web sous-jacente de Microsoft Edge en adoptant le projet open source de chrome.</span><span class="sxs-lookup"><span data-stu-id="30708-106">With this release, we've undertaken a major shift in the underlying web platform of Microsoft Edge by adopting the Chromium open source project.</span></span> <span data-ttu-id="30708-107">Avec cette modification, il est plus facile de créer et tester vos sites Web dans Microsoft Edge et de veiller à ce que les utilisateurs puissent continuer à travailler comme prévu, même si vos utilisateurs naviguent dans un autre navigateur de chrome, tel que Google Chrome, Vivaldi, Opera ou en 3D.</span><span class="sxs-lookup"><span data-stu-id="30708-107">With this change, it will be easier for you to build and test your web sites in Microsoft Edge and ensure they will still work as expected even if your users are browsing in a different Chromium-based browser, like Google Chrome, Vivaldi, Opera, or Brave.</span></span>

## <span data-ttu-id="30708-108">Le nouveau Microsoft Edge (chrome) DevTools</span><span class="sxs-lookup"><span data-stu-id="30708-108">The new Microsoft Edge (Chromium) DevTools</span></span>

<span data-ttu-id="30708-109">Si vous examinez Microsoft Edge et que vous développez essentiellement dans un navigateur en chrome, il est préférable de vous sentir à la maison.</span><span class="sxs-lookup"><span data-stu-id="30708-109">If you are checking out Microsoft Edge and you mainly develop in a Chromium-based browser, you should feel right at home.</span></span> <span data-ttu-id="30708-110">Les outils de développement Microsoft Edge (chrome) sont exactement comme les outils de développement que vous connaissez et utilisez déjà.</span><span class="sxs-lookup"><span data-stu-id="30708-110">The Microsoft Edge (Chromium) Developer Tools are exactly like the developer tools you already know and use!</span></span>

![DevTools Microsoft Edge (chrome)](./media/devtools.png)

<span data-ttu-id="30708-112">Si vous découvrez la nouvelle version de Microsoft Edge et que vous avez développé la version de Microsoft Edge (EdgeHTML), nous avons mis en place de nouveaux outils qui vous permettront de créer et tester plus facilement vos sites Web dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="30708-112">If you are checking out the new Microsoft Edge and you mainly developed in Microsoft Edge (EdgeHTML), we have got some great new tools that we hope will make it easier and faster for you to build and test your web sites in Microsoft Edge!</span></span> <span data-ttu-id="30708-113">Pour en savoir plus sur ces nouveaux outils, consultez [le Guide Microsoft Edge (chrome) devtools](../devtools-guide-chromium.md).</span><span class="sxs-lookup"><span data-stu-id="30708-113">To learn more about these new tools, check out [The Microsoft Edge (Chromium) DevTools Guide](../devtools-guide-chromium.md).</span></span>

## <span data-ttu-id="30708-114">Nouveaux thèmes sombres et clairs pour le DevTools</span><span class="sxs-lookup"><span data-stu-id="30708-114">New dark and light themes for the DevTools</span></span>

<span data-ttu-id="30708-115">Nous avons conçu de nouvelles thèmes sombres et clairs pour le DevTools que nous pensons que vous apprécierez!</span><span class="sxs-lookup"><span data-stu-id="30708-115">We've designed some new dark and light themes for the DevTools that we think you'll love!</span></span> <span data-ttu-id="30708-116">Par défaut, Microsoft Edge (chrome) DevTools utilise le thème sombre.</span><span class="sxs-lookup"><span data-stu-id="30708-116">By default, the Microsoft Edge (Chromium) DevTools will use the Dark theme.</span></span> <span data-ttu-id="30708-117">Pour modifier le thème de devtools, appuyez `Fn`  +  `F1` sur Windows ou Mac ou accédez à paramètres à l’aide du `...` bouton dans le coin supérieur droit de la devtools.</span><span class="sxs-lookup"><span data-stu-id="30708-117">To change the theme of the DevTools, press `Fn` + `F1` on Windows or Mac or navigate to Settings using the `...` button in the top right corner of the DevTools.</span></span>

![Menu principal de Microsoft Edge (chrome) DevTools](./media/devtools-main-menu.png)

<span data-ttu-id="30708-119">Dans les paramètres, vous pouvez modifier le thème du DevTools.</span><span class="sxs-lookup"><span data-stu-id="30708-119">From Settings, you can change the theme of the DevTools.</span></span> <span data-ttu-id="30708-120">Si vous avez aimé la façon dont le DevTools a été examiné dans votre navigateur de chrome, vous pouvez faire en sorte que le DevTools de Microsoft Edge (chrome) ressemble exactement à celui-ci en sélectionnant les thèmes **Dark (chrome)** ou **Light (chrome)** respectivement.</span><span class="sxs-lookup"><span data-stu-id="30708-120">If you liked the way the DevTools looked in your Chromium-based browser, you can make the Microsoft Edge (Chromium) DevTools look exactly like them by selecting the **Dark (Chromium)** or **Light (Chromium)** themes respectively.</span></span> 

## <span data-ttu-id="30708-121">Déboguer Microsoft Edge (chrome) à partir du code VS</span><span class="sxs-lookup"><span data-stu-id="30708-121">Debug Microsoft Edge (Chromium) from VS Code</span></span>

<span data-ttu-id="30708-122">Le [débogueur de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs vous permet désormais de déboguer Microsoft Edge (EdgeHTML) et Microsoft Edge (chrome) directement à partir du code vs.</span><span class="sxs-lookup"><span data-stu-id="30708-122">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can now debug both Microsoft Edge (EdgeHTML) and Microsoft Edge (Chromium) directly from VS Code!</span></span>

![Débogueur pour l’extension de code Edge VS](./media/vscode-debugger.png)

<span data-ttu-id="30708-124">Pour lancer Microsoft Edge (chrome) au lieu de Microsoft Edge (EdgeHTML) à partir du code VS, vous devez ajouter un `version` attribut à votre **launch.jsexistant sur** la configuration avec la version de Microsoft Edge (chrome) que vous voulez lancer ( `dev` , `beta` ou `canary` ).</span><span class="sxs-lookup"><span data-stu-id="30708-124">To launch Microsoft Edge (Chromium) instead of Microsoft Edge (EdgeHTML) from VS Code, you need to add a `version` attribute to your existing **launch.json** configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="30708-125">Voici un exemple \*\* delaunch.jsde\*\* configuration qui lancera la version Canaries de Microsoft Edge (chrome) sur [Bing.com](https://www.bing.com/):</span><span class="sxs-lookup"><span data-stu-id="30708-125">Here's a sample **launch.json** configuration that will launch the Canary version of Microsoft Edge (Chromium) to [bing.com](https://www.bing.com/):</span></span>

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

<span data-ttu-id="30708-126">Pour plus d’informations, consultez [la procédure de débogage de Microsoft Edge (chrome) à partir du code vs](../visual-studio-code/debugger-for-edge.md).</span><span class="sxs-lookup"><span data-stu-id="30708-126">For more information, check out [how to debug Microsoft Edge (Chromium) from VS Code](../visual-studio-code/debugger-for-edge.md).</span></span>

## <span data-ttu-id="30708-127">Mise à jour du protocole Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="30708-127">Edge DevTools Protocol update</span></span>

<span data-ttu-id="30708-128">Avec le Shift dans la plateforme Web sous-jacente de Microsoft Edge, le protocole Edge DevTools ne recevra plus aucune mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30708-128">With the shift in the underlying web platform of Microsoft Edge, the Edge DevTools Protocol will not be receiving any further updates.</span></span> <span data-ttu-id="30708-129">Le DevTools de Microsoft Edge (chrome) utilise le protocole DevTools chrome ou le protocole CDP.</span><span class="sxs-lookup"><span data-stu-id="30708-129">The Microsoft Edge (Chromium) DevTools will use the Chrome DevTools Protocol or CDP.</span></span> <span data-ttu-id="30708-130">Pour référencer la documentation sur les domaines et méthodes en CDP, consultez [la visionneuse CDP](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).</span><span class="sxs-lookup"><span data-stu-id="30708-130">To reference documentation on the domains and methods in CDP, please refer to [the CDP viewer](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).</span></span>

<span data-ttu-id="30708-131">Dans le nouveau Microsoft Edge, toutes les méthodes qui sont préfixées ne sont `ms` pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="30708-131">In the new Microsoft Edge, any methods that are prefixed with `ms` will not be supported.</span></span> <span data-ttu-id="30708-132">Pour en savoir plus sur l’utilisation de la technologie CDP dans Microsoft Edge (chrome), consultez la rubrique [protocole devtools (chrome)](../devtools-protocol-chromium.md).</span><span class="sxs-lookup"><span data-stu-id="30708-132">To learn more about how to use CDP in Microsoft Edge (Chromium), please refer to [DevTools Protocol (Chromium)](../devtools-protocol-chromium.md).</span></span>

## <span data-ttu-id="30708-133">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="30708-133">Known issues</span></span>

<span data-ttu-id="30708-134">De nombreux liens à partir de Microsoft Edge (chrome) DevTools vers du contenu hébergé sur des sites tiers ont été supprimés de manière temporaire.</span><span class="sxs-lookup"><span data-stu-id="30708-134">Many links from the Microsoft Edge (Chromium) DevTools to content hosted on third-party sites have been removed temporarily.</span></span> <span data-ttu-id="30708-135">Dès que nous aurons la possibilité de les remplacer, nous les ajouterons au DevTools.</span><span class="sxs-lookup"><span data-stu-id="30708-135">As soon as we can replace these links, we will add them back to the DevTools.</span></span>


<span data-ttu-id="30708-136">Lors du débogage du contenu Web sur un appareil Android à partir de Microsoft Edge (chrome), la version de l’DevTools qui s’ouvre lorsque vous cliquez sur le bouton **Inspect** de l’outil **périphériques distants** ne correspond pas à la version du navigateur sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="30708-136">When debugging web content on an Android device from Microsoft Edge (Chromium), the version of the DevTools that launches when you click the **Inspect** button from the **Remote devices** tool may not match the version of the browser on your Android device.</span></span> <span data-ttu-id="30708-137">Par conséquent, il est possible que vous voyiez de nouvelles fonctionnalités dans le DevTools qui ne fonctionnent pas sur le navigateur sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="30708-137">As a result, you may see new features in the DevTools that will not work against the browser on your Android device.</span></span> <span data-ttu-id="30708-138">S’il s’agit d’un problème que vous rencontrez, nous aimerions le lire [.](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="30708-138">If this is something you encounter, we'd love to hear about it so please [file feedback](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>

<span data-ttu-id="30708-139">Enfin, Visual Studio sur Windows et Mac ne prennent pas encore en charge Microsoft Edge (chrome).</span><span class="sxs-lookup"><span data-stu-id="30708-139">Finally, Visual Studio on Windows and Mac does not yet support Microsoft Edge (Chromium).</span></span> <span data-ttu-id="30708-140">Inscrivez-vous [ici](https://visualstudio.microsoft.com/vs/preview/) pour être le premier à savoir lorsque nous disposons d’une version d’évaluation de Visual Studio prenant en charge le débogage JavaScript au sein de Microsoft Edge (chrome) pour les projets ASP.net.</span><span class="sxs-lookup"><span data-stu-id="30708-140">Sign up [here](https://visualstudio.microsoft.com/vs/preview/) to be the first to know when we have a preview version of Visual Studio that supports JavaScript debugging inside Microsoft Edge (Chromium) for ASP.NET projects!</span></span>  
