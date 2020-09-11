---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011830"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

En-têtes de requête HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Contains](#contains) | Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.
[GetHeader](#getheader) | Obtient la valeur d’en-tête correspondant au nom.
[GetHeaders](#getheaders) | Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.
[GetIterator](#getiterator) | Obtient un itérateur sur la collection d’en-têtes de requête.
[RemoveHeader](#removeheader) | Supprime l’en-tête qui correspond au nom.
[SetHeader](#setheader) | Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.

Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting. Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.

## Ses

#### Contains 

Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.

> public bool [Contains](#contains)(String name)

#### GetHeader 

Obtient la valeur d’en-tête correspondant au nom.

> chaîne publique [GetHeader](#getheader)(nom de chaîne)

#### GetHeaders 

Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.

> public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(String name)

#### GetIterator 

Obtient un itérateur sur la collection d’en-têtes de requête.

> public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()

#### RemoveHeader 

Supprime l’en-tête qui correspond au nom.

> public void [RemoveHeader](#removeheader)(String name)

#### SetHeader 

Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.

> public void [setHeader](#setheader)(nom de chaîne, valeur chaîne)

