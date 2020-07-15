---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 8bc625d12cc3b3ebe06970fd282dd8f60bcabd22
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878399"
---
# 0.8.355-interface IWebView2NavigationStartingEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NavigationStarting.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | URI de la navigation demandée.
[get_IsUserInitiated](#get_isuserinitiated) | True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.
[get_IsRedirected](#get_isredirected) | True lors de la redirection de la navigation.
[get_RequestHeaders](#get_requestheaders) | En-têtes de requête HTTP pour la navigation.
[get_Cancel](#get_cancel) | L’hôte est susceptible de définir cet indicateur pour annuler la navigation.
[put_Cancel](#put_cancel) | Définissez la propriété Cancel.

## Ses

#### get_Uri 

URI de la navigation demandée.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### get_IsUserInitiated 

True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.

> valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### get_IsRedirected 

True lors de la redirection de la navigation.

> valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool * IsRedirected)

#### get_RequestHeaders 

En-têtes de requête HTTP pour la navigation.

> [get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) * * requestHeaders)

Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.

#### get_Cancel 

L’hôte est susceptible de définir cet indicateur pour annuler la navigation.

> valeur publique HRESULT [get_Cancel](#get_cancel)(bool * Cancel)

S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact. Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond. Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.

#### put_Cancel 

Définissez la propriété Cancel.

> [put_Cancel](#put_cancel)par le biais du public HRESULT

