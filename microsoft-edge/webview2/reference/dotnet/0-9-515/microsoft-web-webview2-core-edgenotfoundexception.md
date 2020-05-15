---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 55ada31485ef061bb3649fb5e2a2811358913dd7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653340"
---
# Classe Microsoft. Web. WebView2. Core. EdgeNotFoundException 

Espace de noms: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

