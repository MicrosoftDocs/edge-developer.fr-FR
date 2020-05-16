---
title: Utiliser le manifeste Web App pour intégrer votre application Web progressive au système d’exploitation
description: Découvrez comment utiliser le manifeste Web App pour intégrer votre application Web progressive dans votre système d’exploitation.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications Web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659292"
---
# <span data-ttu-id="4bb93-104">Utiliser le manifeste Web App pour intégrer votre application Web progressive au système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4bb93-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="4bb93-105">Un manifeste de l’application Web d’un site Web détermine le fonctionnement et le comportement de votre application Web multifonction de votre application sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="4bb93-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="4bb93-106">Au niveau le plus simple, le manifeste fournit des détails sur le nom de votre application, des icônes à utiliser pour représenter votre application dans les menus système et des couleurs de thème utilisées dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="4bb93-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="4bb93-107">Le manifeste vous permet également de déverrouiller des fonctionnalités puissantes qui permettent à votre application de se comporter comme d’autres applications natives sur le système.</span><span class="sxs-lookup"><span data-stu-id="4bb93-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <span data-ttu-id="4bb93-108">Utiliser des raccourcis pour fournir un accès rapide aux fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="4bb93-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="4bb93-109">La plupart des systèmes d’exploitation fournissent un accès rapide aux fonctionnalités d’application principales à l’aide de raccourcis dans le menu contextuel associé à l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="4bb93-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="4bb93-110">Pour utiliser des raccourcis dans votre fichier Project Web App, incluez la `shortcuts` propriété dans le manifeste de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="4bb93-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="4bb93-111">L’extrait de code suivant montre comment définir un raccourci dans le manifeste de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="4bb93-111">The following code snippet shows how to define a shortcut in your web app manifest.</span></span>  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

<span data-ttu-id="4bb93-112">Lors de l’ajout d’un manifeste d’application Web complet, l’ajout de l’extrait de code précédent permet d’activer deux raccourcis dans le menu contextuel de l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="4bb93-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="4bb93-113">Le premier est nommé `Play Later` et possède une icône personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4bb93-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="4bb93-114">Le second est nommé `Subscriptions` et ne comporte pas d’icône, car la `icons` propriété est facultative.</span><span class="sxs-lookup"><span data-stu-id="4bb93-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="4bb93-115">La `description` propriété est également facultative et peut être utilisée pour fournir des informations supplémentaires à des fins d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="4bb93-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <span data-ttu-id="4bb93-116">Identifier votre application en tant que cible de partage</span><span class="sxs-lookup"><span data-stu-id="4bb93-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="4bb93-117">De nombreux systèmes d’exploitation permettent aux utilisateurs de partager rapidement des liens et des fichiers avec des applications natives.</span><span class="sxs-lookup"><span data-stu-id="4bb93-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="4bb93-118">Les applications Web progressives peuvent également participer à cette fonction par le biais du `share_target` manifeste de l’application Web.</span><span class="sxs-lookup"><span data-stu-id="4bb93-118">Progressive Web Apps can participate in this feature as well, via the `share_target` member of the Web App Manifest.</span></span> <span data-ttu-id="4bb93-119">À l’aide de share_target, vous définissez la page «action» (similaire à un formulaire) et les paramètres que vous vous attendez à y transmettre.</span><span class="sxs-lookup"><span data-stu-id="4bb93-119">Using share_target, you define the "action" page (similar to a form) and the parameters you expect to be passed into it.</span></span> <span data-ttu-id="4bb93-120">L’extrait de code suivant montre un exemple de l’utilisation de `share_target` .</span><span class="sxs-lookup"><span data-stu-id="4bb93-120">The following code snippet shows an example of how to use `share_target`.</span></span>

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

<span data-ttu-id="4bb93-121">Lors de l’ajout du manifeste de l’application Web, cette action établit «/share.html» en tant que page d’action du partage.</span><span class="sxs-lookup"><span data-stu-id="4bb93-121">When added to the Web App Manifest, this establishes "/share.html" as the action page for a share.</span></span> <span data-ttu-id="4bb93-122">Par ailleurs, il définit trois paramètres qui seraient transmis à cette page d’action: «Title», «Text» et «URL».</span><span class="sxs-lookup"><span data-stu-id="4bb93-122">Additionally, it defines three parameters that would be passed to that action page: "title", "text", and "url".</span></span> <span data-ttu-id="4bb93-123">Ces paramètres sont stockés dans les propriétés «Name», «description» et «Link» de l’objet [ShareData](https://wicg.github.io/web-share#dom-sharedata) .</span><span class="sxs-lookup"><span data-stu-id="4bb93-123">These parameters will be stored in the [ShareData](https://wicg.github.io/web-share#dom-sharedata) object’s "name", "description", and "link" properties.</span></span> <span data-ttu-id="4bb93-124">Par défaut, la page d’action reçoit ces paramètres dans le cadre d’une demande GET, mais vous pouvez spécifier la requête `method` et le codage \ (en tant que `enctype` \), comme vous le feriez sur un formulaire Web.</span><span class="sxs-lookup"><span data-stu-id="4bb93-124">By default, the action page receives these parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <span data-ttu-id="4bb93-125">Voir également</span><span class="sxs-lookup"><span data-stu-id="4bb93-125">See also</span></span>  

<span data-ttu-id="4bb93-126">Pour en savoir plus sur les manifestes de l’application Web, consultez la liste suivante de rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="4bb93-126">To learn more about Web App Manifests, see the following list of related topics.</span></span>  

* [<span data-ttu-id="4bb93-127">Manifestes de l’application Web</span><span class="sxs-lookup"><span data-stu-id="4bb93-127">Web App Manifests</span></span>][MDNWebAppManifests]  
* [<span data-ttu-id="4bb93-128">Cible de partage Web</span><span class="sxs-lookup"><span data-stu-id="4bb93-128">Web Share Target</span></span>][WICGShareTarget]
* [<span data-ttu-id="4bb93-129">Partager sur le Web</span><span class="sxs-lookup"><span data-stu-id="4bb93-129">Web Share</span></span>][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestes de l’application Web | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "API cible de partage Web | WICG"
[WICGShare]: https://w3c.github.io/web-share/ "API de partage Web | WICG"
