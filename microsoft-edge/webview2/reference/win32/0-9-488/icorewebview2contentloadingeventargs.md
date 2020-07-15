---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a5dd8dc0b504faad7c02669ae464ca1ef75c88af
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880779"
---
# 0.9.515-interface ICoreWebView2ContentLoadingEventArgs 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

