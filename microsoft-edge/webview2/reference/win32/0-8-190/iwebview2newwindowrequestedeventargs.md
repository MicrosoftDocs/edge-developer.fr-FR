---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: cbcac385546c44e776ed48b8ae4d3ab754b614e0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885892"
---
# 0.8.355-interface IWebView2NewWindowRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NewWindowRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | URI cible du NewWindowRequest.
[put_NewWindow](#put_newwindow) | Définit un WebView comme résultat du NewWindowRequest.
[get_NewWindow](#get_newwindow) | Obtient la nouvelle fenêtre.
[put_Handled](#put_handled) | Détermine si le NewWindowRequestedEvent est géré par Host.
[get_Handled](#get_handled) | Détermine si NewWindowRequestedEvent est géré par Host.
[get_IsUserInitiated](#get_isuserinitiated) | IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.
[GetDeferral](#getdeferral) | Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.

L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () etc.)

## Ses

#### get_Uri 

URI cible du NewWindowRequest.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### put_NewWindow 

Définit un WebView comme résultat du NewWindowRequest.

> [put_NewWindow](#put_newwindow)par le biais du public HRESULT ([IWebView2WebView](IWebView2WebView.md) * NewWindow)

Le WebView cible ne doit pas être parcouru. Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.

#### get_NewWindow 

Obtient la nouvelle fenêtre.

> [get_NewWindow](#get_newwindow)publique HRESULT ([IWebView2WebView](IWebView2WebView.md) * * NewWindow)

#### put_Handled 

Détermine si le NewWindowRequestedEvent est géré par Host.

> [put_Handleds](#put_handled)HRESULT publiques (bool géré)

S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte. Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée. La valeur par défaut est false.

#### get_Handled 

Détermine si NewWindowRequestedEvent est géré par Host.

> [get_Handled](#get_handled)par le biais du public HRESULT

#### get_IsUserInitiated 

IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.

> valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### GetDeferral 

Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.

> public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * Report)

Vous pouvez utiliser l’objet [IWebView2Deferral](IWebView2Deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement. Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.

