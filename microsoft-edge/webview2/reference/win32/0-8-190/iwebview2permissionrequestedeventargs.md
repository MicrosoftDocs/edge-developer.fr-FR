---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 92c08d199aa607dae9cc575955a1eb0bf016a9c0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878329"
---
# 0.8.355-interface IWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement PermissionRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Origine du contenu Web qui demande l’autorisation.
[get_PermissionType](#get_permissiontype) | Type de l’autorisation demandée.
[get_IsUserInitiated](#get_isuserinitiated) | True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.
[get_State](#get_state) | État d’une demande d’autorisation, c.-à-d.
[put_State](#put_state) | Définissez la propriété État.
[GetDeferral](#getdeferral) | GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .

## Ses

#### get_Uri 

Origine du contenu Web qui demande l’autorisation.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### get_PermissionType 

Type de l’autorisation demandée.

> valeur publique HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE * value)

#### get_IsUserInitiated 

True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.

> valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.

#### get_State 

État d’une demande d’autorisation, c.-à-d.

> valeur publique HRESULT [get_state](#get_state)(WEBVIEW2_PERMISSION_STATE * value)

l’octroi de la requête. La valeur par défaut est WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Définissez la propriété État.

> [put_State](#put_state)des valeurs HRESULT publiques (WEBVIEW2_PERMISSION_STATE valeur)

#### GetDeferral 

GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .

> public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * Report)

Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.

