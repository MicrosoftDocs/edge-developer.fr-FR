---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: d1cf39fe71c4b00f10a14da8a65428eb24daa71f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011934"
---
# interface ICoreWebView2NewWindowRequestedEventArgs 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NewWindowRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Détermine si NewWindowRequestedEvent est géré par Host.
[get_IsUserInitiated](#get_isuserinitiated) | IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.
[get_NewWindow](#get_newwindow) | Obtient la nouvelle fenêtre.
[get_Uri](#get_uri) | URI cible du NewWindowRequest.
[get_WindowFeatures](#get_windowfeatures) | Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.
[GetDeferral](#getdeferral) | Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.
[put_Handled](#put_handled) | Détermine si le NewWindowRequestedEvent est géré par Host.
[put_NewWindow](#put_newwindow) | Définit un WebView comme résultat du NewWindowRequest.

L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)

## Ses

#### get_Handled 

Détermine si NewWindowRequestedEvent est géré par Host.

> [get_Handled](#get_handled)par le biais du public HRESULT

#### get_IsUserInitiated 

IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.

> valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Le bloqueur de fenêtres contextuelles Edge est désactivé pour WebView de sorte que l’application puisse utiliser cet indicateur pour bloquer les fenêtres contextuelles non-utilisateur.

#### get_NewWindow 

Obtient la nouvelle fenêtre.

> [get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](icorewebview2.md) * * NewWindow)

#### get_Uri 

URI cible du NewWindowRequest.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### get_WindowFeatures 

Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.

> [get_WindowFeatures](#get_windowfeatures)par le biais du public HRESULT ([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) * * WindowFeatures)

Ces fonctionnalités peuvent être envisagées pour le positionnement et le dimensionnement des nouvelles fenêtres WebView.

#### GetDeferral 

Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.

> public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Report)

Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement. Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.

#### put_Handled 

Détermine si le NewWindowRequestedEvent est géré par Host.

> [put_Handleds](#put_handled)HRESULT publiques (bool géré)

S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte. Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée. La valeur par défaut est false.

#### put_NewWindow 

Définit un WebView comme résultat du NewWindowRequest.

> [put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) * NewWindow)

Le WebView cible ne doit pas être parcouru. Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.

