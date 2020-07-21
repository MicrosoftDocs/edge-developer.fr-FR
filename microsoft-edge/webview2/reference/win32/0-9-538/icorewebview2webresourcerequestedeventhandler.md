---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 3cdafae6480a3bf6e3a5bf96f7e7fba1ae8cc77c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884518"
---
# interface ICoreWebView2WebResourceRequestedEventHandler 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

Se déclenche quand une requête d’URL (par le biais d’un réseau, un fichier, etc.) est effectuée dans le WebView pour un filtre de ressources Web correspondant à une URL spécifiée dans AddWebResourceRequestedFilter.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

L’hôte peut afficher et modifier la demande ou fournir une réponse sous la forme d’un modèle similaire à HTTP, auquel cas la requête est immédiatement terminée. Il est possible qu’elle ne contienne aucun en-tête de requête ajouté par la pile réseau, par exemple les en-têtes d’autorisation.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

> [appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) * sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) * args)

