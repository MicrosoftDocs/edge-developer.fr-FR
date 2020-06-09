---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: c82c37d7127d69700f35fbf9e2a69f85159a7109
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698621"
---
# <span data-ttu-id="d45b3-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d45b3-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="d45b3-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d45b3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d45b3-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="d45b3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d45b3-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d45b3-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="d45b3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d45b3-108">Summary</span></span>

 <span data-ttu-id="d45b3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d45b3-109">Members</span></span>                        | <span data-ttu-id="d45b3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d45b3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d45b3-111">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="d45b3-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="d45b3-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="d45b3-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="d45b3-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="d45b3-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="d45b3-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d45b3-114">The ID of the navigation.</span></span>
[<span data-ttu-id="d45b3-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="d45b3-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="d45b3-116">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d45b3-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="d45b3-117">Ses</span><span class="sxs-lookup"><span data-stu-id="d45b3-117">Members</span></span>

#### <span data-ttu-id="d45b3-118">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="d45b3-118">IsSuccess</span></span> 

<span data-ttu-id="d45b3-119">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="d45b3-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="d45b3-120">public bool [Propriétés IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="d45b3-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="d45b3-121">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="d45b3-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="d45b3-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="d45b3-122">NavigationId</span></span> 

<span data-ttu-id="d45b3-123">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d45b3-123">The ID of the navigation.</span></span>

> <span data-ttu-id="d45b3-124">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="d45b3-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="d45b3-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="d45b3-125">WebErrorStatus</span></span> 

<span data-ttu-id="d45b3-126">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d45b3-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="d45b3-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="d45b3-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

