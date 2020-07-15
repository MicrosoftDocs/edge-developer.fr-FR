---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 162d6dde904868ad6a4864b81c0ca76d50638c06
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878455"
---
# 0.8.355-interface IWebView2HttpRequestHeaders 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

En-têtes de requête HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[GetHeader](#getheader) | Obtient la valeur d’en-tête correspondant au nom.
[Contains](#contains) | Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.
[SetHeader](#setheader) | Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.
[RemoveHeader](#removeheader) | Supprime l’en-tête qui correspond au nom.
[GetIterator](#getiterator) | Obtient un itérateur sur la collection d’en-têtes de requête.

Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting. Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.

## Ses

#### GetHeader 

Obtient la valeur d’en-tête correspondant au nom.

> public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr * value)

#### Contains 

Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.

> le HRESULT public [contient](#contains)(nom LPCWSTR, bool * Contains)

#### SetHeader 

Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.

> public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)

#### RemoveHeader 

Supprime l’en-tête qui correspond au nom.

> public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)

#### GetIterator 

Obtient un itérateur sur la collection d’en-têtes de requête.

> public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) * * itérateur)

