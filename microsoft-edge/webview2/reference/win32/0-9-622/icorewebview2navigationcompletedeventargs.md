---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: b45920cfdab8a01d1288fbaf566748545b8a2c98
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011879"
---
# interface ICoreWebView2NavigationCompletedEventArgs 

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

Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false dans le cas d’autres scénarios tels que Window. Stop () appelé sur la page de navigation.

#### get_NavigationId 

ID de la navigation.

> [get_NavigationIds](#get_navigationid)par le biais du public HRESULT

#### get_WebErrorStatus 

Code d’erreur en cas d’échec de la navigation.

> [get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS * WebErrorStatus)

