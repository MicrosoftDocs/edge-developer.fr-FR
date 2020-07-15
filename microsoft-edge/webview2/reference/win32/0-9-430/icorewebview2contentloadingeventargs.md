---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 95fa97268fb5695aebf5c1414752cf12cf1da57b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881143"
---
# 0.9.430-interface ICoreWebView2ContentLoadingEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

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

