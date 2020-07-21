---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: fc65d857f11a77a1d3629d40266f0453acadaa7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886310"
---
# 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

