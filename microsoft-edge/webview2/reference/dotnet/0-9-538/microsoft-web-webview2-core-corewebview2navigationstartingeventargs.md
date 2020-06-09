---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 58ca180e73c3e4644e466e13c4059f32102f1896
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698599"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

Espace de noms: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

