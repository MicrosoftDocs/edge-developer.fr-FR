---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2Deferral
ms.openlocfilehash: 533aefe8b14ae3cabfddd32cb588014067bfdd42
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010284"
---
# 0.9.579-interface ICoreWebView2Deferral 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
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

