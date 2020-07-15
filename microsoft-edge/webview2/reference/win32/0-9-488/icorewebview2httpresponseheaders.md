---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 356f8bfc235e522ef5e976baf61f8c9017766a3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880534"
---
# 0.9.515-interface ICoreWebView2HttpResponseHeaders 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

