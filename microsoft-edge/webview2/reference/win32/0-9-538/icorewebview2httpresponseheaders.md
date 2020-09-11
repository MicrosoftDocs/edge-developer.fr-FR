---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 6278f29f983503916e0015ab4bbac44f79ffe3d9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011306"
---
# 0.9.579-interface ICoreWebView2HttpResponseHeaders 

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

> public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * itérateur)

#### GetIterator 

Obtient un itérateur sur la collection d’en-têtes de réponse entières.

> public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * itérateur)

