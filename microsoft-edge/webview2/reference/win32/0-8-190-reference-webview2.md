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
ms.openlocfilehash: ba3103037db60674d1d3887ac43a8fce5be02bdd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653463"
---
# 0.8.190-référence (WebView2)  

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.8.355.  Reportez-vous à [référence](../../webview2-api-reference.md) pour la dernière référence d’API.

Le contrôle Microsoft Edge WebView2 vous permet d’héberger le contenu Web de votre application à l’aide de [Microsoft Edge \ (chrome \)](https://www.microsoftedgeinsider.com) en tant que moteur de rendu.  Pour plus d’informations, voir [vue d’ensemble de Microsoft Edge WebView2](../../index.md)) et [mise en route d’WebView2](../../gettingstarted/win32.md).  [IWebView2WebView](0-8-190/IWebView2WebView.md) est l’endroit idéal pour commencer à apprendre les détails de l’API.  

## Globales  

*   [Globales](0-8-190/webview2-idl.md)  

## Implément  
*   [IWebView2Deferral](0-8-190/IWebView2Deferral.md)
*   [IWebView2Environment](0-8-190/IWebView2Environment.md)
*   [IWebView2Environment2](0-8-190/IWebView2Environment2.md)
*   [IWebView2Environment3](0-8-190/IWebView2Environment3.md)
*   [IWebView2HttpHeadersCollectionIterator](0-8-190/IWebView2HttpHeadersCollectionIterator.md)
*   [IWebView2HttpRequestHeaders](0-8-190/IWebView2HttpRequestHeaders.md)
*   [IWebView2HttpResponseHeaders](0-8-190/IWebView2HttpResponseHeaders.md)
*   [IWebView2Settings](0-8-190/IWebView2Settings.md)
*   [IWebView2Settings2](0-8-190/IWebView2Settings2.md)
*   [IWebView2WebResourceRequest](0-8-190/IWebView2WebResourceRequest.md)
*   [IWebView2WebResourceRequestedEventArgs2](0-8-190/IWebView2WebResourceRequestedEventArgs2.md)
*   [IWebView2WebResourceResponse](0-8-190/IWebView2WebResourceResponse.md)
*   [IWebView2WebView](0-8-190/IWebView2WebView.md)
*   [IWebView2WebView2](0-8-190/IWebView2WebView2.md)
*   [IWebView2WebView3](0-8-190/IWebView2WebView3.md)
*   [IWebView2WebView4](0-8-190/IWebView2WebView4.md)
*   [IWebView2WebView5](0-8-190/IWebView2WebView5.md)

### Interfaces d’argument d’événement

*   [IWebView2AcceleratorKeyPressedEventArgs](0-8-190/IWebView2AcceleratorKeyPressedEventArgs.md)
*   [IWebView2DevToolsProtocolEventReceivedEventArgs](0-8-190/IWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [IWebView2DocumentStateChangedEventArgs](0-8-190/IWebView2DocumentStateChangedEventArgs.md)
*   [IWebView2MoveFocusRequestedEventArgs](0-8-190/IWebView2MoveFocusRequestedEventArgs.md)
*   [IWebView2NavigationCompletedEventArgs](0-8-190/IWebView2NavigationCompletedEventArgs.md)
*   [IWebView2NavigationStartingEventArgs](0-8-190/IWebView2NavigationStartingEventArgs.md)
*   [IWebView2NewVersionAvailableEventArgs](0-8-190/IWebView2NewVersionAvailableEventArgs.md)
*   [IWebView2NewWindowRequestedEventArgs](0-8-190/IWebView2NewWindowRequestedEventArgs.md)
*   [IWebView2PermissionRequestedEventArgs](0-8-190/IWebView2PermissionRequestedEventArgs.md)
*   [IWebView2ProcessFailedEventArgs](0-8-190/IWebView2ProcessFailedEventArgs.md)
*   [IWebView2ScriptDialogOpeningEventArgs](0-8-190/IWebView2ScriptDialogOpeningEventArgs.md)
*   [IWebView2WebMessageReceivedEventArgs](0-8-190/IWebView2WebMessageReceivedEventArgs.md)
*   [IWebView2WebResourceRequestedEventArgs](0-8-190/IWebView2WebResourceRequestedEventArgs.md)

### Interfaces de délégué

*   [IWebView2AcceleratorKeyPressedEventHandler](0-8-190/IWebView2AcceleratorKeyPressedEventHandler.md)
*   [IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-8-190/IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [IWebView2CallDevToolsProtocolMethodCompletedHandler](0-8-190/IWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [IWebView2CapturePreviewCompletedHandler](0-8-190/IWebView2CapturePreviewCompletedHandler.md)
*   [IWebView2ContainsFullScreenElementChangedEventHandler](0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [IWebView2CreateWebView2EnvironmentCompletedHandler](0-8-190/IWebView2CreateWebView2EnvironmentCompletedHandler.md)
*   [IWebView2CreateWebViewCompletedHandler](0-8-190/IWebView2CreateWebViewCompletedHandler.md)
*   [IWebView2DevToolsProtocolEventReceivedEventHandler](0-8-190/IWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [IWebView2DocumentStateChangedEventHandler](0-8-190/IWebView2DocumentStateChangedEventHandler.md)
*   [IWebView2DocumentTitleChangedEventHandler](0-8-190/IWebView2DocumentTitleChangedEventHandler.md)
*   [IWebView2ExecuteScriptCompletedHandler](0-8-190/IWebView2ExecuteScriptCompletedHandler.md)
*   [IWebView2FocusChangedEventHandler](0-8-190/IWebView2FocusChangedEventHandler.md)
*   [IWebView2MoveFocusRequestedEventHandler](0-8-190/IWebView2MoveFocusRequestedEventHandler.md)
*   [IWebView2NavigationCompletedEventHandler](0-8-190/IWebView2NavigationCompletedEventHandler.md)
*   [IWebView2NavigationStartingEventHandler](0-8-190/IWebView2NavigationStartingEventHandler.md)
*   [IWebView2NewVersionAvailableEventHandler](0-8-190/IWebView2NewVersionAvailableEventHandler.md)
*   [IWebView2NewWindowRequestedEventHandler](0-8-190/IWebView2NewWindowRequestedEventHandler.md)
*   [IWebView2PermissionRequestedEventHandler](0-8-190/IWebView2PermissionRequestedEventHandler.md)
*   [IWebView2ProcessFailedEventHandler](0-8-190/IWebView2ProcessFailedEventHandler.md)
*   [IWebView2ScriptDialogOpeningEventHandler](0-8-190/IWebView2ScriptDialogOpeningEventHandler.md)
*   [IWebView2WebMessageReceivedEventHandler](0-8-190/IWebView2WebMessageReceivedEventHandler.md)
*   [IWebView2WebResourceRequestedEventHandler](0-8-190/IWebView2WebResourceRequestedEventHandler.md)
*   [IWebView2ZoomFactorChangedEventHandler](0-8-190/IWebView2ZoomFactorChangedEventHandler.md)
