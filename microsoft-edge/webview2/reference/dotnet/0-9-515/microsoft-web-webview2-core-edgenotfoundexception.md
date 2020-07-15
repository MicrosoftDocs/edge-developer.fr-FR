---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: db4a903ca430541fa9edec9d953bf28531f7c0a4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879603"
---
# 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

```
class Microsoft.Web.WebView2.Core.EdgeNotFoundException
  : public Exception
```

Exception levée lorsqu’une installation Edge est manquante.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[EdgeNotFoundException](#edgenotfoundexception) | Initialise une nouvelle instance de la classe EdgeNotFoundException.
[EdgeNotFoundException](#edgenotfoundexception) | Initialise une nouvelle instance de la classe EdgeNotFoundException avec une référence à l’exception interne qui est la cause de l’exception.
[EdgeNotFoundException](#edgenotfoundexception) | Initialise une nouvelle instance de la classe EdgeNotFoundException avec un message d’erreur spécifié.
[EdgeNotFoundException](#edgenotfoundexception) | Initialise une nouvelle instance de la classe EdgeNotFoundException avec un message d’erreur spécifié et une référence à l’exception interne qui est la cause de l’exception.

## Ses

#### EdgeNotFoundException 

Initialise une nouvelle instance de la classe EdgeNotFoundException.

> public [EdgeNotFoundException](#edgenotfoundexception)()

#### EdgeNotFoundException 

Initialise une nouvelle instance de la classe EdgeNotFoundException avec une référence à l’exception interne qui est la cause de l’exception.

> public [EdgeNotFoundException](#edgenotfoundexception)(exception interne)

##### Parameters
* `inner` Exception qui est la cause de l’exception actuelle.

#### EdgeNotFoundException 

Initialise une nouvelle instance de la classe EdgeNotFoundException avec un message d’erreur spécifié.

> [EdgeNotFoundException](#edgenotfoundexception)public (message chaîne)

##### Parameters
* `message` Message d’erreur qui explique la raison de l’exception.

#### EdgeNotFoundException 

Initialise une nouvelle instance de la classe EdgeNotFoundException avec un message d’erreur spécifié et une référence à l’exception interne qui est la cause de l’exception.

> [EdgeNotFoundException](#edgenotfoundexception)public (message de chaîne, exception interne)

##### Parameters
* `message` Message d’erreur qui explique la raison de l’exception. 

* `inner` Exception qui est la cause de l’exception actuelle.

