---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: dfa6aedb10e60a2af15c7b098c479f8537d6c747
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011824"
---
# <span data-ttu-id="b1783-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b1783-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="b1783-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b1783-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b1783-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b1783-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b1783-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="b1783-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="b1783-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b1783-108">Summary</span></span>

 <span data-ttu-id="b1783-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b1783-109">Members</span></span>                        | <span data-ttu-id="b1783-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b1783-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b1783-111">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b1783-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="b1783-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="b1783-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="b1783-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="b1783-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="b1783-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b1783-114">The ID of the navigation.</span></span>
[<span data-ttu-id="b1783-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b1783-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="b1783-116">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b1783-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="b1783-117">Ses</span><span class="sxs-lookup"><span data-stu-id="b1783-117">Members</span></span>

#### <span data-ttu-id="b1783-118">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b1783-118">IsSuccess</span></span> 

<span data-ttu-id="b1783-119">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="b1783-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="b1783-120">public bool [Propriétés IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="b1783-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="b1783-121">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false dans le cas d’autres scénarios tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="b1783-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional scenarios such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="b1783-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="b1783-122">NavigationId</span></span> 

<span data-ttu-id="b1783-123">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b1783-123">The ID of the navigation.</span></span>

> <span data-ttu-id="b1783-124">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="b1783-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="b1783-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b1783-125">WebErrorStatus</span></span> 

<span data-ttu-id="b1783-126">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b1783-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="b1783-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="b1783-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

