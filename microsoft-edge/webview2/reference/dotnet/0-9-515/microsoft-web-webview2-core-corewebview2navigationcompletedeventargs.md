---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 3a15232a7fe2ddf230d0463069052c55f7abc843
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879134"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement NavigationCompleted.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Propriétés IsSuccess](#issuccess) | True lorsque la navigation est réussie.
[NavigationId](#navigationid) | ID de la navigation.
[WebErrorStatus](#weberrorstatus) | Code d’erreur en cas d’échec de la navigation.

## Ses

#### Propriétés IsSuccess 

True lorsque la navigation est réussie.

> public bool [Propriétés IsSuccess](#issuccess)

Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.

#### NavigationId 

ID de la navigation.

> public ulong [NavigationId](#navigationid)

#### WebErrorStatus 

Code d’erreur en cas d’échec de la navigation.

> public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)

