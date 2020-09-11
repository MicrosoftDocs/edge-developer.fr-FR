---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011894"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

En-têtes de réponse HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Ajoute la ligne d’en-tête avec le nom et la valeur.
[Contains](#contains) | Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.
[GetHeader](#getheader) | Obtient la première valeur d’en-tête dans la collection qui correspond au nom.
[GetHeaders](#getheaders) | Obtient les valeurs d’en-tête correspondant au nom.
[GetIterator](#getiterator) | Obtient un itérateur sur la collection d’en-têtes de réponse entières.

Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.

## Ses

#### AppendHeader 

Ajoute la ligne d’en-tête avec le nom et la valeur.

> public void [AppendHeader](#appendheader)(nom de chaîne, valeur chaîne)

#### Contains 

Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.

> public bool [Contains](#contains)(String name)

#### GetHeader 

Obtient la première valeur d’en-tête dans la collection qui correspond au nom.

> chaîne publique [GetHeader](#getheader)(nom de chaîne)

#### GetHeaders 

Obtient les valeurs d’en-tête correspondant au nom.

> public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(String name)

#### GetIterator 

Obtient un itérateur sur la collection d’en-têtes de réponse entières.

> public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()

