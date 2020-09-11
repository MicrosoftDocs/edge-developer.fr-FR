---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: adeb4c0f223e8b38e3cefb93ae189a351d9828a5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010907"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement NewWindowRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Handled](#handled) | Si NewWindowRequestedEvent est géré par Host.
[IsUserInitiated](#isuserinitiated) | IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.
[NewWindow](#newwindow) | Obtient la nouvelle fenêtre.
[URI](#uri) | URI cible du NewWindowRequest.
[WindowFeatures](#windowfeatures) | Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.
[GetDeferral](#getdeferral) | Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)

## Ses

#### Handled 

Si NewWindowRequestedEvent est géré par Host.

> propriété booléenne [gérée](#handled)

S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte. Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée. La valeur par défaut est false.

#### IsUserInitiated 

IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.

> public bool [IsUserInitiated](#isuserinitiated)

#### NewWindow 

Obtient la nouvelle fenêtre.

> public CoreWebView2 [NewWindow](#newwindow)

#### URI 

URI cible du NewWindowRequest.

> [URI](#uri) de chaîne publique

Le WebView cible ne doit pas être parcouru. Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.

#### WindowFeatures 

Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.

> public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)

Ces fonctionnalités peuvent être envisagées pour le positionnement et le dimensionnement des nouvelles fenêtres WebView.

#### GetDeferral 

Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

> public CoreWebView2Deferral [GetDeferral](#getdeferral)()

Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête d’ouverture de fenêtre ultérieurement. Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.

