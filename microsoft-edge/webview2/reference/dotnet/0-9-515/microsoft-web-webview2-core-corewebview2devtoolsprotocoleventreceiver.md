---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 1982c6926d2ed8805433efc4d46ff6f3cac691ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885057"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived) | S’abonner à un événement DevToolsProtocol.

Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.

## Ses

#### DevToolsProtocolEventReceived 

S’abonner à un événement DevToolsProtocol.

> événement public EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)

La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché. Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.

