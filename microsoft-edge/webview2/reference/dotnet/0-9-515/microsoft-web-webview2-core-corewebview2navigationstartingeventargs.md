---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886373"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement NavigationStarting.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Annuler](#cancel) | L’hôte est susceptible de définir cet indicateur pour annuler la navigation.
[IsRedirected](#isredirected) | True lors de la redirection de la navigation.
[IsUserInitiated](#isuserinitiated) | True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.
[NavigationId](#navigationid) | ID de la navigation.
[RequestHeaders](#requestheaders) | En-têtes de requête HTTP pour la navigation.
[URI](#uri) | URI de la navigation demandée.

## Ses

#### Annuler 

L’hôte est susceptible de définir cet indicateur pour annuler la navigation.

> public bool [Annuler](#cancel)

S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact. Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond. Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.

#### IsRedirected 

True lors de la redirection de la navigation.

> public bool [IsRedirected](#isredirected)

#### IsUserInitiated 

True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.

> public bool [IsUserInitiated](#isuserinitiated)

#### NavigationId 

ID de la navigation.

> public ulong [NavigationId](#navigationid)

#### RequestHeaders 

En-têtes de requête HTTP pour la navigation.

> public HttpRequestHeaders [requestHeaders](#requestheaders)

Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.

#### URI 

URI de la navigation demandée.

> [URI](#uri) de chaîne publique

