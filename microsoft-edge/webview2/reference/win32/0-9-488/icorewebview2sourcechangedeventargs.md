---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9ea8f860d637c5d9e49e68917d167380c0418b87
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877370"
---
# 0.9.515-interface ICoreWebView2SourceChangedEventArgs 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

