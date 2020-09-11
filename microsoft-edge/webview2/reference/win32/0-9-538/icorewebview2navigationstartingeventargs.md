---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 8bf2cf37ef76256987a52fd5491e5c995244dd65
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011299"
---
# 0.9.579-interface ICoreWebView2NavigationStartingEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NavigationStarting.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Cancel](#get_cancel) | L’hôte est susceptible de définir cet indicateur pour annuler la navigation.
[get_IsRedirected](#get_isredirected) | True lors de la redirection de la navigation.
[get_IsUserInitiated](#get_isuserinitiated) | True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.
[get_NavigationId](#get_navigationid) | ID de la navigation.
[get_RequestHeaders](#get_requestheaders) | En-têtes de requête HTTP pour la navigation.
[get_Uri](#get_uri) | URI de la navigation demandée.
[put_Cancel](#put_cancel) | Définissez la propriété Cancel.

## Ses

#### get_Cancel 

L’hôte est susceptible de définir cet indicateur pour annuler la navigation.

> valeur publique HRESULT [get_Cancel](#get_cancel)(bool * Cancel)

S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact. Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond. Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.

#### get_IsRedirected 

True lors de la redirection de la navigation.

> valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool * IsRedirected)

#### get_IsUserInitiated 

True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.

> valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### get_NavigationId 

ID de la navigation.

> navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT

#### get_RequestHeaders 

En-têtes de requête HTTP pour la navigation.

> [get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * * requestHeaders)

Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.

#### get_Uri 

URI de la navigation demandée.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### put_Cancel 

Définissez la propriété Cancel.

> [put_Cancel](#put_cancel)par le biais du public HRESULT

