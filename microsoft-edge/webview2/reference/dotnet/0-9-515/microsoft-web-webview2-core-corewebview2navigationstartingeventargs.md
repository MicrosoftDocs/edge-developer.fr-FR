---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ea3936ac1267fa085f62db843f5cac3fad2635b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879785"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

