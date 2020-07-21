---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: e2e973e2ee1817decd24bbc1d0dc3daa9709795c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885078"
---
# <span data-ttu-id="6de1d-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6de1d-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="6de1d-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6de1d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6de1d-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6de1d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6de1d-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6de1d-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="6de1d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6de1d-108">Summary</span></span>

 <span data-ttu-id="6de1d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6de1d-109">Members</span></span>                        | <span data-ttu-id="6de1d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6de1d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6de1d-111">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6de1d-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="6de1d-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="6de1d-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="6de1d-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="6de1d-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="6de1d-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6de1d-114">The ID of the navigation.</span></span>
[<span data-ttu-id="6de1d-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6de1d-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="6de1d-116">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6de1d-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="6de1d-117">Ses</span><span class="sxs-lookup"><span data-stu-id="6de1d-117">Members</span></span>

#### <span data-ttu-id="6de1d-118">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6de1d-118">IsSuccess</span></span> 

<span data-ttu-id="6de1d-119">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="6de1d-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="6de1d-120">public bool [Propriétés IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="6de1d-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="6de1d-121">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="6de1d-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="6de1d-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="6de1d-122">NavigationId</span></span> 

<span data-ttu-id="6de1d-123">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6de1d-123">The ID of the navigation.</span></span>

> <span data-ttu-id="6de1d-124">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="6de1d-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="6de1d-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6de1d-125">WebErrorStatus</span></span> 

<span data-ttu-id="6de1d-126">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6de1d-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="6de1d-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="6de1d-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

