---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2dc5c437acadb06b5f8b12ae0dc54aec12412355
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883790"
---
# 0.9.515-interface ICoreWebView2ProcessFailedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement ProcessFailed.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_ProcessFailedKind](#get_processfailedkind) | Type d’échec du processus qui s’est produit.

## Ses

#### get_ProcessFailedKind 

Type d’échec du processus qui s’est produit.

> [get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (COREWEBVIEW2_PROCESS_FAILED_KIND * ProcessFailedKind)

