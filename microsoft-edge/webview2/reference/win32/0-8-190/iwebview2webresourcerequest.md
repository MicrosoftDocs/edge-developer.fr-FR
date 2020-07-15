---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 3c9736c8b5a3cfb0de994285f3a1f90d62666fd0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878147"
---
# 0.8.355-interface IWebView2WebResourceRequest 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

Une requête HTTP utilisée avec l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | URI de la requête.
[put_Uri](#put_uri) | Définissez la propriété Uri.
[get_Method](#get_method) | Méthode de requête HTTP.
[put_Method](#put_method) | Définissez la propriété Method.
[get_Content](#get_content) | Le corps du message de requête HTTP en tant que flux.
[put_Content](#put_content) | Définissez la propriété Content.
[get_Headers](#get_headers) | En-têtes de requête HTTP mutables.

## Ses

#### get_Uri 

URI de la requête.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### put_Uri 

Définissez la propriété Uri.

> [put_Uri](#put_uri)par le biais du public HRESULT

#### get_Method 

Méthode de requête HTTP.

> valeur publique HRESULT [get_Method](#get_method)(méthode LPWSTR *)

#### put_Method 

Définissez la propriété Method.

> [put_Method](#put_method)par le biais du public HRESULT (méthode LPCWSTR)

#### get_Content 

Le corps du message de requête HTTP en tant que flux.

> accès public HRESULT [get_Content](#get_content)(IStream * * content)

Les données publiées seraient là. Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé. Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur. Null signifie qu’il n’y a pas de données de contenu. La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)

#### put_Content 

Définissez la propriété Content.

> [put_Content](#put_content)par le biais du contenu public HRESULT

#### get_Headers 

En-têtes de requête HTTP mutables.

> [get_Headersles](#get_headers)HRESULT publiques[(en](IWebView2HttpRequestHeaders.md) -têtes * *)

