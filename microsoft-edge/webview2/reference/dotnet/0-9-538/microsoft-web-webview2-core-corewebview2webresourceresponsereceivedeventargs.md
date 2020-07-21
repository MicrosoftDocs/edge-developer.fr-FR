---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
ms.openlocfilehash: 44fc4f47aa10a7e409ac584cb75b750048056e47
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886511"
---
# <span data-ttu-id="43ca2-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="43ca2-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseReceivedEventArgs class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="43ca2-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="43ca2-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="43ca2-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="43ca2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="43ca2-107">Arguments d’événement pour l’événement WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="43ca2-107">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="43ca2-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="43ca2-108">Summary</span></span>

 <span data-ttu-id="43ca2-109">Ses</span><span class="sxs-lookup"><span data-stu-id="43ca2-109">Members</span></span>                        | <span data-ttu-id="43ca2-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="43ca2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="43ca2-111">Requête</span><span class="sxs-lookup"><span data-stu-id="43ca2-111">Request</span></span>](#request) | <span data-ttu-id="43ca2-112">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="43ca2-112">Web resource request object.</span></span>
[<span data-ttu-id="43ca2-113">Réponse</span><span class="sxs-lookup"><span data-stu-id="43ca2-113">Response</span></span>](#response) | <span data-ttu-id="43ca2-114">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="43ca2-114">Web resource response object.</span></span>
[<span data-ttu-id="43ca2-115">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="43ca2-115">PopulateResponseContentAsync</span></span>](#populateresponsecontentasync) | <span data-ttu-id="43ca2-116">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="43ca2-116">Async method to request the Content stream of the response.</span></span>

## <span data-ttu-id="43ca2-117">Ses</span><span class="sxs-lookup"><span data-stu-id="43ca2-117">Members</span></span>

#### <span data-ttu-id="43ca2-118">Requête</span><span class="sxs-lookup"><span data-stu-id="43ca2-118">Request</span></span> 

<span data-ttu-id="43ca2-119">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="43ca2-119">Web resource request object.</span></span>

> <span data-ttu-id="43ca2-120">[demande](#request) publique HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="43ca2-120">public HttpRequestMessage [Request](#request)</span></span>

<span data-ttu-id="43ca2-121">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="43ca2-121">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="43ca2-122">Réponse</span><span class="sxs-lookup"><span data-stu-id="43ca2-122">Response</span></span> 

<span data-ttu-id="43ca2-123">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="43ca2-123">Web resource response object.</span></span>

> <span data-ttu-id="43ca2-124">[réponse](#response) HttpResponseMessage publique</span><span class="sxs-lookup"><span data-stu-id="43ca2-124">public HttpResponseMessage [Response](#response)</span></span>

<span data-ttu-id="43ca2-125">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="43ca2-125">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="43ca2-126">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="43ca2-126">PopulateResponseContentAsync</span></span> 

<span data-ttu-id="43ca2-127">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="43ca2-127">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="43ca2-128">[PopulateResponseContentAsync](#populateresponsecontentasync)de tâches asynchrones publiques ()</span><span class="sxs-lookup"><span data-stu-id="43ca2-128">public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span></span>

