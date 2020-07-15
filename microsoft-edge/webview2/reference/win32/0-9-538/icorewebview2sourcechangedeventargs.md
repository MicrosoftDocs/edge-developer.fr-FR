---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 3e622a8fb5b8ed43e5a23eaab8bd0aa61ed7d193
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879400"
---
# interface ICoreWebView2SourceChangedEventArgs 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement SourceChanged.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | True si la page vers laquelle vous naviguez est un nouveau document.

## Ses

#### get_IsNewDocument 

True si la page vers laquelle vous naviguez est un nouveau document.

> valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool * IsNewDocument)

