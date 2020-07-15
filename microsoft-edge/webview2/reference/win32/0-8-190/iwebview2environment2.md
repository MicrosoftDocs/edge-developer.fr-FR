---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: d127af61bfdc9bf692fa48489d7982bf2c6cad86
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878546"
---
# 0.8.355-interface IWebView2Environment2 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2Environment2
  : public IWebView2Environment
```

Fonctionnalités supplémentaires implémentées par l’objet Environment.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_BrowserVersionInfo](#get_browserversioninfo) | Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.

Pour plus d’informations, consultez l’interface [IWebView2Environment](IWebView2Environment.md) . Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2Environment](IWebView2Environment.md).

## Ses

#### get_BrowserVersionInfo 

Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.

> valeur publique HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR * VERSIONINFO)

Il correspond au format de l’API GetWebView2BrowserVersionInfo. Les noms de canaux sont «bêta», «dev» et «Canaries».

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

