---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: c13d0625669d6303c115c3d415d12278cfbe8320
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880499"
---
# 0.9.515-interface ICoreWebView2NavigationCompletedEventArgs 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NavigationCompleted.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_IsSuccess](#get_issuccess) | True lorsque la navigation est réussie.
[get_NavigationId](#get_navigationid) | ID de la navigation.
[get_WebErrorStatus](#get_weberrorstatus) | Code d’erreur en cas d’échec de la navigation.

## Ses

#### get_IsSuccess 

True lorsque la navigation est réussie.

> valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool * propriétés IsSuccess)

Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.

#### get_NavigationId 

ID de la navigation.

> navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT

#### get_WebErrorStatus 

Code d’erreur en cas d’échec de la navigation.

> [get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS * COREWEBVIEW2_WEB_ERROR_STATUS)

