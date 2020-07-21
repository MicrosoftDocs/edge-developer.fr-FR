---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/17/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 04c80d3319c74d3461666b6f35fadd0481b45207
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885533"
---
# <span data-ttu-id="ed360-104">Classe Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="ed360-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="ed360-105">Espace de noms: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="ed360-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="ed360-106">Assemblage: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="ed360-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="ed360-107">Cette classe est un ensemble de paramètres les plus courants utilisés pour créer un CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="ed360-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="ed360-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="ed360-108">Summary</span></span>

 <span data-ttu-id="ed360-109">Ses</span><span class="sxs-lookup"><span data-stu-id="ed360-109">Members</span></span>                        | <span data-ttu-id="ed360-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ed360-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ed360-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="ed360-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="ed360-112">Obtient ou définit la valeur à transmettre en tant que paramètre browserExecutableFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.</span><span class="sxs-lookup"><span data-stu-id="ed360-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="ed360-113">Langue</span><span class="sxs-lookup"><span data-stu-id="ed360-113">Language</span></span>](#language) | <span data-ttu-id="ed360-114">Obtient ou définit la valeur à utiliser pour la propriété Language du paramètre CoreWebView2EnvironmentOptions transmis à CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.</span><span class="sxs-lookup"><span data-stu-id="ed360-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="ed360-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="ed360-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="ed360-116">Obtient ou définit la valeur à transmettre en tant que paramètre userDataFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.</span><span class="sxs-lookup"><span data-stu-id="ed360-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="ed360-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="ed360-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="ed360-118">Crée une nouvelle instance de CoreWebView2CreationProperties avec les données par défaut pour toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="ed360-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="ed360-119">Son objectif principal est d’affecter [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) afin de personnaliser l’environnement utilisé par un [WebView2](microsoft-web-webview2-wpf-webview2.md) lors de l’initialisation implicite.</span><span class="sxs-lookup"><span data-stu-id="ed360-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="ed360-120">C’est également un utilitaire d’intégration WPF agréable qui permet d’utiliser les paramètres d’environnement couramment utilisés afin d’être des propriétés de dépendance et de créer et d’utiliser des balises.</span><span class="sxs-lookup"><span data-stu-id="ed360-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="ed360-121">Cette classe n’est pas conçue pour contenir toutes les options de personnalisation de l’environnement possibles.</span><span class="sxs-lookup"><span data-stu-id="ed360-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="ed360-122">Si vous avez besoin d’un contrôle total sur l’environnement utilisé par un contrôle WebView2, vous devez initialiser le contrôle de manière explicite en créant votre propre environnement avec CoreWebView2Environment. CreateAsync et en le passant à [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*avant* de définir la propriété [WebView2. source](microsoft-web-webview2-wpf-webview2.md) sur tout.</span><span class="sxs-lookup"><span data-stu-id="ed360-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="ed360-123">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe [WebView2](microsoft-web-webview2-wpf-webview2.md) .</span><span class="sxs-lookup"><span data-stu-id="ed360-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="ed360-124">Ses</span><span class="sxs-lookup"><span data-stu-id="ed360-124">Members</span></span>

#### <span data-ttu-id="ed360-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="ed360-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="ed360-126">Obtient ou définit la valeur à transmettre en tant que paramètre browserExecutableFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.</span><span class="sxs-lookup"><span data-stu-id="ed360-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="ed360-127">[BrowserExecutableFolder](#browserexecutablefolder) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="ed360-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="ed360-128">Langue</span><span class="sxs-lookup"><span data-stu-id="ed360-128">Language</span></span> 

<span data-ttu-id="ed360-129">Obtient ou définit la valeur à utiliser pour la propriété Language du paramètre CoreWebView2EnvironmentOptions transmis à CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.</span><span class="sxs-lookup"><span data-stu-id="ed360-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="ed360-130">[langage](#language) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="ed360-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="ed360-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="ed360-131">UserDataFolder</span></span> 

<span data-ttu-id="ed360-132">Obtient ou définit la valeur à transmettre en tant que paramètre userDataFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.</span><span class="sxs-lookup"><span data-stu-id="ed360-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="ed360-133">[UserDataFolder](#userdatafolder) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="ed360-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="ed360-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="ed360-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="ed360-135">Crée une nouvelle instance de CoreWebView2CreationProperties avec les données par défaut pour toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="ed360-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="ed360-136">public [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span><span class="sxs-lookup"><span data-stu-id="ed360-136">public [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

