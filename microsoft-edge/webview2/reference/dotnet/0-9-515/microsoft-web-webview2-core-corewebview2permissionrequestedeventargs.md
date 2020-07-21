---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2bfa4559824c9bb397648249ead8fa8cb60c281c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884630"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

