---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 903355ff04463ad86f1e25771f5f321f7d0df479
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879162"
---
# interface ICoreWebView2HttpRequestHeaders 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

En-têtes de requête HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Contains](#contains) | Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.
[GetHeader](#getheader) | Obtient la valeur d’en-tête correspondant au nom.
[GetHeaders](#getheaders) | Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.
[GetIterator](#getiterator) | Obtient un itérateur sur la collection d’en-têtes de requête.
[RemoveHeader](#removeheader) | Supprime l’en-tête qui correspond au nom.
[SetHeader](#setheader) | Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.

Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting. Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.

## Ses

#### Contains 

Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.

> le HRESULT public [contient](#contains)(nom LPCWSTR, bool * Contains)

#### GetHeader 

Obtient la valeur d’en-tête correspondant au nom.

> public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr * value)

#### GetHeaders 

Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.

> public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * itérateur)

#### GetIterator 

Obtient un itérateur sur la collection d’en-têtes de requête.

> public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * itérateur)

#### RemoveHeader 

Supprime l’en-tête qui correspond au nom.

> public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)

#### SetHeader 

Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.

> public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)

