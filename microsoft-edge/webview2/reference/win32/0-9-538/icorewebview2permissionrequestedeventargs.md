---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 4abb6fb058765a05ebb32fe97474348c4aebde12
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010032"
---
# 0.9.579-interface ICoreWebView2PermissionRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement PermissionRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_IsUserInitiated](#get_isuserinitiated) | True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.
[get_PermissionKind](#get_permissionkind) | Type de l’autorisation demandée.
[get_State](#get_state) | État d’une demande d’autorisation, c.-à-d.
[get_Uri](#get_uri) | Origine du contenu Web qui demande l’autorisation.
[GetDeferral](#getdeferral) | GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .
[put_State](#put_state) | Définissez la propriété État.

## Ses

#### get_IsUserInitiated 

True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.

> valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.

#### get_PermissionKind 

Type de l’autorisation demandée.

> valeur publique HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND * value)

#### get_State 

État d’une demande d’autorisation, c.-à-d.

> valeur publique HRESULT [get_state](#get_state)(COREWEBVIEW2_PERMISSION_STATE * value)

l’octroi de la requête. La valeur par défaut est COREWEBVIEW2_PERMISSION_STATE_DEFAULT.

#### get_Uri 

Origine du contenu Web qui demande l’autorisation.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### GetDeferral 

GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .

> public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Report)

Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.

#### put_State 

Définissez la propriété État.

> [put_State](#put_state)des valeurs HRESULT publiques (COREWEBVIEW2_PERMISSION_STATE valeur)

