---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: f40d0baa415ccc76747993c4070bb05eaf76fe56
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878609"
---
# 0.8.355-interface IWebView2Deferral 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2Deferral
  : public IUnknown
```

Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Complete](#complete) | Termine l’événement différé associé.

## Ses

#### Complete 

Termine l’événement différé associé.

> valeur publique HRESULT [achevée](#complete)()

Complète doit être appelé une seule fois pour chaque Report.

