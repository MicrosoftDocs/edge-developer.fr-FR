---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 1b80b42bc26316d1fcc8ac74656f24cb0db75bae
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011868"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

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

> public CoreWebView2HttpRequestHeaders [requestHeaders](#requestheaders)

Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.

#### URI 

URI de la navigation demandée.

> [URI](#uri) de chaîne publique

