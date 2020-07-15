---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: ede6cef20a1a0f5fcd0780376b5ddec07bf05d26
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878798"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement PermissionRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.
[PermissionKind](#permissionkind) | Type de l’autorisation demandée.
[État](#state) | État d’une demande d’autorisation, c.-à-d.
[URI](#uri) | Origine du contenu Web qui demande l’autorisation.
[GetDeferral](#getdeferral) | GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.

## Ses

#### IsUserInitiated 

True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.

> public bool [IsUserInitiated](#isuserinitiated)

Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.

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

