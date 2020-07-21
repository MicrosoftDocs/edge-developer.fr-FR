---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 321d18a726ac19db92018cb27d31867029991cf0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886219"
---
# 0.9.430-interface ICoreWebView2HttpResponseHeaders 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

En-têtes de réponse HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Ajoute la ligne d’en-tête avec le nom et la valeur.
[Contains](#contains) | Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.
[GetHeader](#getheader) | Obtient la première valeur d’en-tête dans la collection qui correspond au nom.
[GetHeaders](#getheaders) | Obtient les valeurs d’en-tête correspondant au nom.
[GetIterator](#getiterator) | Obtient un itérateur sur la collection d’en-têtes de réponse entières.

Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.

## Ses

#### AppendHeader 

Ajoute la ligne d’en-tête avec le nom et la valeur.

> public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)

#### Contains 

Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.

> le HRESULT public [contient](#contains)(nom LPCWSTR, bool * Contains)

#### GetHeader 

Obtient la première valeur d’en-tête dans la collection qui correspond au nom.

> public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr * value)

#### GetHeaders 

Obtient les valeurs d’en-tête correspondant au nom.

> public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * itérateur)

#### GetIterator 

Obtient un itérateur sur la collection d’en-têtes de réponse entières.

> public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * itérateur)

