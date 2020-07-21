---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
ms.openlocfilehash: 44fc4f47aa10a7e409ac584cb75b750048056e47
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886511"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement WebResourceResponseReceived.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Requête](#request) | Objet demande de ressources Web.
[Réponse](#response) | Objet de réponse aux ressources Web.
[PopulateResponseContentAsync](#populateresponsecontentasync) | Méthode Async pour demander le flux de contenu de la réponse.

## Ses

#### Requête 

Objet demande de ressources Web.

> [demande](#request) publique HttpRequestMessage

Toute modification apportée à cet objet sera ignorée.

#### Réponse 

Objet de réponse aux ressources Web.

> [réponse](#response) HttpResponseMessage publique

Toute modification apportée à cet objet sera ignorée.

#### PopulateResponseContentAsync 

Méthode Async pour demander le flux de contenu de la réponse.

> [PopulateResponseContentAsync](#populateresponsecontentasync)de tâches asynchrones publiques ()

