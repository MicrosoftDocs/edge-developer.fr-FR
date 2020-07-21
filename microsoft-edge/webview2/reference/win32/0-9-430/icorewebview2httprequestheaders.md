---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 04a8bf376ad7649021c4ab1555c3090cce5b52fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885610"
---
# 0.9.430-interface ICoreWebView2HttpRequestHeaders 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

En-têtes de requête HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[GetHeader](#getheader) | Obtient la valeur d’en-tête correspondant au nom.
[GetHeaders](#getheaders) | Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.
[Contains](#contains) | Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.
[SetHeader](#setheader) | Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.
[RemoveHeader](#removeheader) | Supprime l’en-tête qui correspond au nom.
[GetIterator](#getiterator) | Obtient un itérateur sur la collection d’en-têtes de requête.

Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting. Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.

## Ses

#### GetHeader 

Obtient la valeur d’en-tête correspondant au nom.

> public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr * value)

#### GetHeaders 

Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.

> public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * itérateur)

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

> public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * itérateur)

