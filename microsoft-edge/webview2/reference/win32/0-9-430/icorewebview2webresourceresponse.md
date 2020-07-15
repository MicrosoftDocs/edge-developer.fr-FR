---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: c0c33bab95f8d2c7908864b1869bc9a186216ef9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877545"
---
# 0.9.430-interface ICoreWebView2WebResourceResponse 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

Réponse HTTP utilisée avec l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Contenu de réponse HTTP en tant que flux.
[put_Content](#put_content) | Définissez la propriété Content.
[get_Headers](#get_headers) | En-têtes de réponse HTTP ignorés.
[get_StatusCode](#get_statuscode) | Code d’état de réponse HTTP.
[put_StatusCode](#put_statuscode) | Définissez la propriété StatusCode.
[get_ReasonPhrase](#get_reasonphrase) | Expression de raison de réponse HTTP.
[put_ReasonPhrase](#put_reasonphrase) | Définissez la propriété ReasonPhrase.

## Ses

#### get_Content 

Contenu de réponse HTTP en tant que flux.

> accès public HRESULT [get_Content](#get_content)(IStream * * content)

Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse. Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur. Null signifie qu’il n’y a pas de données de contenu. La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)

#### put_Content 

Définissez la propriété Content.

> [put_Content](#put_content)par le biais du contenu public HRESULT

#### get_Headers 

En-têtes de réponse HTTP ignorés.

> [get_Headersles](#get_headers)HRESULT publiques[(en](ICoreWebView2HttpResponseHeaders.md) -têtes * *)

#### get_StatusCode 

Code d’état de réponse HTTP.

> valeur publique HRESULT [get_StatusCode](#get_statuscode)

#### put_StatusCode 

Définissez la propriété StatusCode.

> [put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)

#### get_ReasonPhrase 

Expression de raison de réponse HTTP.

> valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * ReasonPhrase)

#### put_ReasonPhrase 

Définissez la propriété ReasonPhrase.

> [put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)

