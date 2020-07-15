---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: dd141e135275d815458ce66a93dfc9ef3e7b33a8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878861"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement MoveFocusRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Handled](#handled) | Indiquez si l’événement a été géré par l’application.
[Raison](#reason) | La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.

## Ses

#### Handled 

Indiquez si l’événement a été géré par l’application.

> propriété booléenne [gérée](#handled)

Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE. Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée. L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre. S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.

#### Raison 

La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.

> [raison](#reason) du CoreWebView2MoveFocusReason public

