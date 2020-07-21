---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884861"
---
# 0.9.430-interface ICoreWebView2NewBrowserVersionAvailableEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NewBrowserVersionAvailable.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.

## Ses

#### get_NewVersion 

Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.

> valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR * NewVersion)

