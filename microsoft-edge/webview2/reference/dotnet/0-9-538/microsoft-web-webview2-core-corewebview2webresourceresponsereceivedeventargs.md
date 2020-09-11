---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
ms.openlocfilehash: a8c988fdfee72ed22e74886b440819d7a9d6fe24
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010509"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

