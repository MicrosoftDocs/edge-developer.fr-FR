---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 5cc3ca23dcababc35a73b44a81c54439d0dbe1a3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884308"
---
# 0.9.430-interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateCoreWebView2Environment.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.

> [appel](#invoke)HRESULT public (résultat HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) * created_environment)

