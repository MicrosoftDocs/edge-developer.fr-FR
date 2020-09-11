---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011847"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Réponse HTTP utilisée avec l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Contenu](#content) | Contenu de réponse HTTP en tant que flux.
[En-têtes](#headers) | En-têtes de réponse HTTP ignorés.
[ReasonPhrase](#reasonphrase) | Expression de raison de réponse HTTP.
[StatusCode](#statuscode) | Code d’état de réponse HTTP.

## Ses

#### Contenu 

Contenu de réponse HTTP en tant que flux.

> [contenu](#content) de flux public

Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse. Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur. Null signifie qu’il n’y a pas de données de contenu. La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées).

#### En-têtes 

En-têtes de réponse HTTP ignorés.

> [en-têtes](#headers) [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) publics

#### ReasonPhrase 

Expression de raison de réponse HTTP.

> [ReasonPhrase](#reasonphrase) de chaîne publique

#### StatusCode 

Code d’état de réponse HTTP.

> [statusCode](#statuscode) ent public

