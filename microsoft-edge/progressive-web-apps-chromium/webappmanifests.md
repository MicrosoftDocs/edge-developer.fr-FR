---
title: Utiliser le manifeste d’application web pour intégrer votre application Web progressive au système d’exploitation
description: Découvrez comment utiliser le manifeste d’application web pour intégrer votre application Web progressive à votre système d’exploitation.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399098"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a><span data-ttu-id="c4d74-104">Utiliser le manifeste d’application web pour intégrer votre application web progressive au système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c4d74-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="c4d74-105">Un manifeste d’application web d’un site web régit l’apparence et le comportement de votre application web progressive \(PWA\) lorsqu’elle est installée sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="c4d74-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="c4d74-106">Au niveau le plus élémentaire, le manifeste fournit des détails sur le nom de votre application, les icônes à utiliser pour représenter votre application dans les menus système et le thème colore le système d’exploitation \(OS\) utilise dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="c4d74-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="c4d74-107">Le manifeste vous permet également de déverrouiller des fonctionnalités puissantes qui permettent à votre application de se comporter comme d’autres applications natives sur le système.</span><span class="sxs-lookup"><span data-stu-id="c4d74-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a><span data-ttu-id="c4d74-108">Utiliser des raccourcis pour fournir un accès rapide aux fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c4d74-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="c4d74-109">La plupart des systèmes d’exploitation fournissent un accès rapide aux fonctionnalités clés de l’application à l’aide de raccourcis dans le menu contextique connecté à l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="c4d74-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="c4d74-110">Pour utiliser des raccourcis dans votre PWA, incluez `shortcuts` la propriété dans votre manifeste d’application web.</span><span class="sxs-lookup"><span data-stu-id="c4d74-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="c4d74-111">L’extrait de code suivant montre comment définir un raccourci dans le manifeste de votre application web.</span><span class="sxs-lookup"><span data-stu-id="c4d74-111">The following code snippet displays how to define a shortcut in your web app manifest.</span></span>  

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

<span data-ttu-id="c4d74-112">Lorsqu’il est ajouté à un manifeste d’application web complet, l’ajout de l’extrait de code précédent active deux raccourcis dans le menu contextique sur l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="c4d74-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="c4d74-113">Le premier est nommé `Play Later` et possède une icône personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c4d74-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="c4d74-114">Le second est nommé `Subscriptions` et n’a pas d’icône, car `icons` la propriété est facultative.</span><span class="sxs-lookup"><span data-stu-id="c4d74-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="c4d74-115">La propriété est également facultative et peut être utilisée pour fournir des informations supplémentaires à `description` des fins d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="c4d74-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <a name="identify-your-app-as-a-share-target"></a><span data-ttu-id="c4d74-116">Identifier votre application en tant que cible de partage</span><span class="sxs-lookup"><span data-stu-id="c4d74-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="c4d74-117">De nombreux systèmes d’exploitation permettent aux utilisateurs de partager rapidement des liens et des fichiers avec des applications natives.</span><span class="sxs-lookup"><span data-stu-id="c4d74-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="c4d74-118">Les applications web progressives peuvent également participer à cette fonctionnalité, à l’aide du `share_target` membre du manifeste d’application web.</span><span class="sxs-lookup"><span data-stu-id="c4d74-118">Progressive Web Apps can participate in this feature as well, using the `share_target` member of the Web App Manifest.</span></span>  <span data-ttu-id="c4d74-119">À `share_target` l’aide de , vous définissez la page \(similaire à un formulaire\) et les paramètres que vous prévoyez `"action"` d’y passer.</span><span class="sxs-lookup"><span data-stu-id="c4d74-119">Using `share_target`, you define the `"action"` page \(similar to a form\) and the parameters you expect to be passed into it.</span></span>  <span data-ttu-id="c4d74-120">L’extrait de code suivant affiche un exemple `share_target` d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c4d74-120">The following code snippet displays an example of how to use `share_target`.</span></span>

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

<span data-ttu-id="c4d74-121">Lorsqu’il est ajouté au manifeste de l’application Web, il s’agit de la `"/share.html"` page d’action d’un partage.</span><span class="sxs-lookup"><span data-stu-id="c4d74-121">When added to the Web App Manifest, this establishes `"/share.html"` as the action page for a share.</span></span> <span data-ttu-id="c4d74-122">En outre, il définit trois paramètres qui seraient transmis à cette page d’action : `"title"` `"text"` , et `"url"` .</span><span class="sxs-lookup"><span data-stu-id="c4d74-122">Additionally, it defines three parameters that would be passed to that action page:`"title"`, `"text"`, and `"url"`.</span></span>  <span data-ttu-id="c4d74-123">Ces paramètres sont stockés dans les propriétés et les propriétés `"name"` `"description"` de `"link"` [l’objet ShareData.][GitHubWicgWebShareDomSharedata]</span><span class="sxs-lookup"><span data-stu-id="c4d74-123">These parameters will be stored in the `"name"`, `"description"`, and `"link"` properties of the [ShareData][GitHubWicgWebShareDomSharedata] object.</span></span>  <span data-ttu-id="c4d74-124">Par défaut, la page d’action reçoit les paramètres dans le cadre d’une requête GET, mais vous pouvez spécifier la demande et `method` l’encodage \(en tant que \), comme vous le feriez sur un `enctype` formulaire web.</span><span class="sxs-lookup"><span data-stu-id="c4d74-124">By default, the action page receives the parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4d74-125">Voir également</span><span class="sxs-lookup"><span data-stu-id="c4d74-125">See also</span></span>  

<span data-ttu-id="c4d74-126">Pour en savoir plus sur les manifestes d’application web, accédez à la liste suivante des rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="c4d74-126">To learn more about Web App Manifests, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="c4d74-127">Manifestes d’application web</span><span class="sxs-lookup"><span data-stu-id="c4d74-127">Web App Manifests</span></span>][MDNWebAppManifests]  
*   [<span data-ttu-id="c4d74-128">Cible de partage web</span><span class="sxs-lookup"><span data-stu-id="c4d74-128">Web Share Target</span></span>][GitHubWicgWebShareTarget]
*   [<span data-ttu-id="c4d74-129">Partage web</span><span class="sxs-lookup"><span data-stu-id="c4d74-129">Web Share</span></span>][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestes d’application web | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Web Share Target API | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Dictionnaire ShareData - Api de partage web | WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Web Share API | WICG"
