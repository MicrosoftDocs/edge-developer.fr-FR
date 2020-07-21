---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 7bccd93aeec2c5cfbc181ce5ab1cf58e29da48ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884294"
---
# 0.9.430-interface ICoreWebView2ContentLoadingEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement ContentLoading.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_IsErrorPage](#get_iserrorpage) | True si le contenu chargé est une page d’erreur.
[get_NavigationId](#get_navigationid) | ID de la navigation.

## Ses

#### get_IsErrorPage 

True si le contenu chargé est une page d’erreur.

> valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool * IsErrorPage)

#### get_NavigationId 

ID de la navigation.

> navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT

