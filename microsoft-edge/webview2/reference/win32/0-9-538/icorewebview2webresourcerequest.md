---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequest
ms.openlocfilehash: 4d339d6a066404b51bd8b362ad2c455fa8f26e1f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010200"
---
# 0.9.579-interface ICoreWebView2WebResourceRequest 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

Une requête HTTP utilisée avec l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Le corps du message de requête HTTP en tant que flux.
[get_Headers](#get_headers) | En-têtes de requête HTTP mutables.
[get_Method](#get_method) | Méthode de requête HTTP.
[get_Uri](#get_uri) | URI de la requête.
[put_Content](#put_content) | Définissez la propriété Content.
[put_Method](#put_method) | Définissez la propriété Method.
[put_Uri](#put_uri) | Définissez la propriété Uri.

## Ses

#### get_Content 

Le corps du message de requête HTTP en tant que flux.

> accès public HRESULT [get_Content](#get_content)(IStream * * content)

Les données publiées seraient là. Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé. Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur. Null signifie qu’il n’y a pas de données de contenu. La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)

#### get_Headers 

En-têtes de requête HTTP mutables.

> [get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httprequestheaders.md) -têtes * *)

#### get_Method 

Méthode de requête HTTP.

> valeur publique HRESULT [get_Method](#get_method)(méthode LPWSTR *)

#### get_Uri 

URI de la requête.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### put_Content 

Définissez la propriété Content.

> [put_Content](#put_content)par le biais du contenu public HRESULT

#### put_Method 

Définissez la propriété Method.

> [put_Method](#put_method)par le biais du public HRESULT (méthode LPCWSTR)

#### put_Uri 

Définissez la propriété Uri.

> [put_Uri](#put_uri)par le biais du public HRESULT

