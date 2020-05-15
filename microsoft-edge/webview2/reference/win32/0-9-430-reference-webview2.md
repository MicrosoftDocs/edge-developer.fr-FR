---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Applications WebView 2 de Microsoft Edge 2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8baa7b1f571d62fad21a30441f47835bff3da96a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653556"
---
# <span data-ttu-id="1455c-104">0.9.430-référence (WebView2)</span><span class="sxs-lookup"><span data-stu-id="1455c-104">0.9.430 - Reference (WebView2)</span></span>  

> [!NOTE]
> <span data-ttu-id="1455c-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="1455c-105">This reference may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="1455c-106">Reportez-vous à [référence](../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="1455c-106">Please refer to [Reference](../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="1455c-107">Le contrôle Microsoft Edge WebView2 vous permet d’héberger le contenu Web de votre application à l’aide de [Microsoft Edge \ (chrome \)](https://www.microsoftedgeinsider.com) en tant que moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="1455c-107">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="1455c-108">Pour plus d’informations, voir [vue d’ensemble de Microsoft Edge WebView2](../../index.md)) et [mise en route d’WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="1455c-108">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="1455c-109">[ICoreWebView2](0-9-430/ICoreWebView2.md) est l’endroit idéal pour commencer à apprendre les détails de l’API.</span><span class="sxs-lookup"><span data-stu-id="1455c-109">[ICoreWebView2](0-9-430/ICoreWebView2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="1455c-110">Globales</span><span class="sxs-lookup"><span data-stu-id="1455c-110">Globals</span></span>  

*   [<span data-ttu-id="1455c-111">Globales</span><span class="sxs-lookup"><span data-stu-id="1455c-111">Globals</span></span>](0-9-430/webview2-idl.md)  

## <span data-ttu-id="1455c-112">Implément</span><span class="sxs-lookup"><span data-stu-id="1455c-112">Interfaces</span></span>  
*   [<span data-ttu-id="1455c-113">ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="1455c-113">ICoreWebView2</span></span>](0-9-430/ICoreWebView2.md)
*   [<span data-ttu-id="1455c-114">ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="1455c-114">ICoreWebView2Deferral</span></span>](0-9-430/ICoreWebView2Deferral.md)
*   [<span data-ttu-id="1455c-115">ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="1455c-115">ICoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-430/ICoreWebView2DevToolsProtocolEventReceiver.md)
*   [<span data-ttu-id="1455c-116">ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="1455c-116">ICoreWebView2Environment</span></span>](0-9-430/ICoreWebView2Environment.md)
*   [<span data-ttu-id="1455c-117">ICoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="1455c-117">ICoreWebView2Host</span></span>](0-9-430/ICoreWebView2Host.md)
*   [<span data-ttu-id="1455c-118">ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="1455c-118">ICoreWebView2HttpHeadersCollectionIterator</span></span>](0-9-430/ICoreWebView2HttpHeadersCollectionIterator.md)
*   [<span data-ttu-id="1455c-119">ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="1455c-119">ICoreWebView2HttpRequestHeaders</span></span>](0-9-430/ICoreWebView2HttpRequestHeaders.md)
*   [<span data-ttu-id="1455c-120">ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="1455c-120">ICoreWebView2HttpResponseHeaders</span></span>](0-9-430/ICoreWebView2HttpResponseHeaders.md)
*   [<span data-ttu-id="1455c-121">ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="1455c-121">ICoreWebView2Settings</span></span>](0-9-430/ICoreWebView2Settings.md)
*   [<span data-ttu-id="1455c-122">ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="1455c-122">ICoreWebView2WebResourceRequest</span></span>](0-9-430/ICoreWebView2WebResourceRequest.md)
*   [<span data-ttu-id="1455c-123">ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1455c-123">ICoreWebView2WebResourceResponse</span></span>](0-9-430/ICoreWebView2WebResourceResponse.md)

### <span data-ttu-id="1455c-124">Interfaces d’argument d’événement</span><span class="sxs-lookup"><span data-stu-id="1455c-124">Event argument interfaces</span></span>

*   [<span data-ttu-id="1455c-125">ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-125">ICoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-430/ICoreWebView2AcceleratorKeyPressedEventArgs.md)
*   [<span data-ttu-id="1455c-126">ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-126">ICoreWebView2ContentLoadingEventArgs</span></span>](0-9-430/ICoreWebView2ContentLoadingEventArgs.md)
*   [<span data-ttu-id="1455c-127">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-127">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [<span data-ttu-id="1455c-128">ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-128">ICoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-430/ICoreWebView2MoveFocusRequestedEventArgs.md)
*   [<span data-ttu-id="1455c-129">ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-129">ICoreWebView2NavigationCompletedEventArgs</span></span>](0-9-430/ICoreWebView2NavigationCompletedEventArgs.md)
*   [<span data-ttu-id="1455c-130">ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-130">ICoreWebView2NavigationStartingEventArgs</span></span>](0-9-430/ICoreWebView2NavigationStartingEventArgs.md)
*   [<span data-ttu-id="1455c-131">ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-131">ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span>](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventArgs.md)
*   [<span data-ttu-id="1455c-132">ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-132">ICoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-430/ICoreWebView2NewWindowRequestedEventArgs.md)
*   [<span data-ttu-id="1455c-133">ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-133">ICoreWebView2PermissionRequestedEventArgs</span></span>](0-9-430/ICoreWebView2PermissionRequestedEventArgs.md)
*   [<span data-ttu-id="1455c-134">ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-134">ICoreWebView2ProcessFailedEventArgs</span></span>](0-9-430/ICoreWebView2ProcessFailedEventArgs.md)
*   [<span data-ttu-id="1455c-135">ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-135">ICoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-430/ICoreWebView2ScriptDialogOpeningEventArgs.md)
*   [<span data-ttu-id="1455c-136">ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-136">ICoreWebView2SourceChangedEventArgs</span></span>](0-9-430/ICoreWebView2SourceChangedEventArgs.md)
*   [<span data-ttu-id="1455c-137">ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-137">ICoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-430/ICoreWebView2WebMessageReceivedEventArgs.md)
*   [<span data-ttu-id="1455c-138">ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1455c-138">ICoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-430/ICoreWebView2WebResourceRequestedEventArgs.md)

### <span data-ttu-id="1455c-139">Interfaces de délégué</span><span class="sxs-lookup"><span data-stu-id="1455c-139">Delegate interfaces</span></span>

*   [<span data-ttu-id="1455c-140">ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-140">ICoreWebView2AcceleratorKeyPressedEventHandler</span></span>](0-9-430/ICoreWebView2AcceleratorKeyPressedEventHandler.md)
*   [<span data-ttu-id="1455c-141">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-141">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-9-430/ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [<span data-ttu-id="1455c-142">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-142">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-9-430/ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [<span data-ttu-id="1455c-143">ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-143">ICoreWebView2CapturePreviewCompletedHandler</span></span>](0-9-430/ICoreWebView2CapturePreviewCompletedHandler.md)
*   [<span data-ttu-id="1455c-144">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-144">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-9-430/ICoreWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [<span data-ttu-id="1455c-145">ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-145">ICoreWebView2ContentLoadingEventHandler</span></span>](0-9-430/ICoreWebView2ContentLoadingEventHandler.md)
*   [<span data-ttu-id="1455c-146">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-146">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span>](0-9-430/ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler.md)
*   [<span data-ttu-id="1455c-147">ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-147">ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span>](0-9-430/ICoreWebView2CreateCoreWebView2HostCompletedHandler.md)
*   [<span data-ttu-id="1455c-148">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-148">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [<span data-ttu-id="1455c-149">ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-149">ICoreWebView2DocumentTitleChangedEventHandler</span></span>](0-9-430/ICoreWebView2DocumentTitleChangedEventHandler.md)
*   [<span data-ttu-id="1455c-150">ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-150">ICoreWebView2ExecuteScriptCompletedHandler</span></span>](0-9-430/ICoreWebView2ExecuteScriptCompletedHandler.md)
*   [<span data-ttu-id="1455c-151">ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-151">ICoreWebView2FocusChangedEventHandler</span></span>](0-9-430/ICoreWebView2FocusChangedEventHandler.md)
*   [<span data-ttu-id="1455c-152">ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-152">ICoreWebView2HistoryChangedEventHandler</span></span>](0-9-430/ICoreWebView2HistoryChangedEventHandler.md)
*   [<span data-ttu-id="1455c-153">ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-153">ICoreWebView2MoveFocusRequestedEventHandler</span></span>](0-9-430/ICoreWebView2MoveFocusRequestedEventHandler.md)
*   [<span data-ttu-id="1455c-154">ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-154">ICoreWebView2NavigationCompletedEventHandler</span></span>](0-9-430/ICoreWebView2NavigationCompletedEventHandler.md)
*   [<span data-ttu-id="1455c-155">ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-155">ICoreWebView2NavigationStartingEventHandler</span></span>](0-9-430/ICoreWebView2NavigationStartingEventHandler.md)
*   [<span data-ttu-id="1455c-156">ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-156">ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span>](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventHandler.md)
*   [<span data-ttu-id="1455c-157">ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-157">ICoreWebView2NewWindowRequestedEventHandler</span></span>](0-9-430/ICoreWebView2NewWindowRequestedEventHandler.md)
*   [<span data-ttu-id="1455c-158">ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-158">ICoreWebView2PermissionRequestedEventHandler</span></span>](0-9-430/ICoreWebView2PermissionRequestedEventHandler.md)
*   [<span data-ttu-id="1455c-159">ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-159">ICoreWebView2ProcessFailedEventHandler</span></span>](0-9-430/ICoreWebView2ProcessFailedEventHandler.md)
*   [<span data-ttu-id="1455c-160">ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-160">ICoreWebView2ScriptDialogOpeningEventHandler</span></span>](0-9-430/ICoreWebView2ScriptDialogOpeningEventHandler.md)
*   [<span data-ttu-id="1455c-161">ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-161">ICoreWebView2SourceChangedEventHandler</span></span>](0-9-430/ICoreWebView2SourceChangedEventHandler.md)
*   [<span data-ttu-id="1455c-162">ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-162">ICoreWebView2WebMessageReceivedEventHandler</span></span>](0-9-430/ICoreWebView2WebMessageReceivedEventHandler.md)
*   [<span data-ttu-id="1455c-163">ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-163">ICoreWebView2WebResourceRequestedEventHandler</span></span>](0-9-430/ICoreWebView2WebResourceRequestedEventHandler.md)
*   [<span data-ttu-id="1455c-164">ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-164">ICoreWebView2WindowCloseRequestedEventHandler</span></span>](0-9-430/ICoreWebView2WindowCloseRequestedEventHandler.md)
*   [<span data-ttu-id="1455c-165">ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1455c-165">ICoreWebView2ZoomFactorChangedEventHandler</span></span>](0-9-430/ICoreWebView2ZoomFactorChangedEventHandler.md)
