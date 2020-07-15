---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 5e6e2d955dd0d52a093eea116a01961e1ee58c76
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877769"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

