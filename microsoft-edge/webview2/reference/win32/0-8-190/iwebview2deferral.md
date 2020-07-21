---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: a1c00c29a3e063cd995c9f0eb287d870fd1211dc
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886144"
---
# 0.8.355-interface IWebView2Deferral 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

