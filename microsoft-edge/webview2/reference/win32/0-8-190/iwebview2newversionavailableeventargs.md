---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 4271cc1002de70db2803a5bd6d4be73748bf5bbb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885869"
---
# 0.8.355-interface IWebView2NewVersionAvailableEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NewVersionAvailable.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.

## Ses

#### get_NewVersion 

Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.

> valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR * NewVersion)

