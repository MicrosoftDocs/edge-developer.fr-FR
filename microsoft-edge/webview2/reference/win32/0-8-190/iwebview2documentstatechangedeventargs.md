---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 342716da2cded9c903f1edd13fb3400c779a9b39
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653500"
---
# interface IWebView2DocumentStateChangedEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement DocumentStateChanged.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | True si la page vers laquelle vous naviguez est un nouveau document.
[get_IsErrorPage](#get_iserrorpage) | True si le contenu chargé est une page d’erreur.

## Ses

#### get_IsNewDocument 

True si la page vers laquelle vous naviguez est un nouveau document.

> valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool * IsNewDocument)

#### get_IsErrorPage 

True si le contenu chargé est une page d’erreur.

> valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool * IsErrorPage)

