---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011865"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement PermissionRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | True lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.
[PermissionKind](#permissionkind) | Type de l’autorisation demandée.
[État](#state) | État d’une demande d’autorisation, c.-à-d.
[URI](#uri) | Origine du contenu Web qui demande l’autorisation.
[GetDeferral](#getdeferral) | GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.

## Ses

#### IsUserInitiated 

True lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.

> public bool [IsUserInitiated](#isuserinitiated)

Le bloqueur de fenêtres contextuelles Edge est désactivé pour WebView de sorte que l’application puisse utiliser cet indicateur pour bloquer les fenêtres contextuelles non-utilisateur.

#### PermissionKind 

Type de l’autorisation demandée.

> public CoreWebView2PermissionKind [PermissionKind](#permissionkind)

#### État 

État d’une demande d’autorisation, c.-à-d.

> [État](#state) CoreWebView2PermissionState public

l’octroi de la requête.

La valeur par défaut est CoreWebView2PermissionState. default.

#### URI 

Origine du contenu Web qui demande l’autorisation.

> [URI](#uri) de chaîne publique

#### GetDeferral 

GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.

> public CoreWebView2Deferral [GetDeferral](#getdeferral)()

Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.

