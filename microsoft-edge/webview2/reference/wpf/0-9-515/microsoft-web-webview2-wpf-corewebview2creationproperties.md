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
ms.openlocfilehash: d2c3b3ee179dec217418241031142549d170e440
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653249"
---
# Classe Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties 

Espace de noms: Microsoft. Web. WebView2. WPF \
Assembly: Microsoft. Web. WebView2. WPF. dll

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

Cette classe est un ensemble de paramètres les plus courants utilisés pour créer un CoreWebView2Environment.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[BrowserExecutableFolder](#browserexecutablefolder) | Obtient ou définit la valeur à transmettre en tant que paramètre browserExecutableFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.
[Langue](#language) | Obtient ou définit la valeur à utiliser pour la propriété Language du paramètre CoreWebView2EnvironmentOptions transmis à CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.
[UserDataFolder](#userdatafolder) | Obtient ou définit la valeur à transmettre en tant que paramètre userDataFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.
[CoreWebView2CreationProperties](#corewebview2creationproperties) | Crée une nouvelle instance de CoreWebView2CreationProperties avec les données par défaut pour toutes les propriétés.

Son objectif principal est d’affecter [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) afin de personnaliser l’environnement utilisé par un [WebView2](microsoft-web-webview2-wpf-webview2.md) lors de l’initialisation implicite. C’est également un utilitaire d’intégration WPF agréable qui permet d’utiliser les paramètres d’environnement couramment utilisés afin d’être des propriétés de dépendance et de créer et d’utiliser des balises.

Cette classe n’est pas conçue pour contenir toutes les options de personnalisation de l’environnement possibles. Si vous avez besoin d’un contrôle total sur l’environnement utilisé par un contrôle WebView2, vous devez initialiser le contrôle de manière explicite en créant votre propre environnement avec CoreWebView2Environment. CreateAsync et en le passant à [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*avant* de définir la propriété [WebView2. source](microsoft-web-webview2-wpf-webview2.md) sur tout. Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe [WebView2](microsoft-web-webview2-wpf-webview2.md) .

## Ses

#### BrowserExecutableFolder 

Obtient ou définit la valeur à transmettre en tant que paramètre browserExecutableFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.

> [BrowserExecutableFolder](#browserexecutablefolder) de chaîne publique

#### Langue 

Obtient ou définit la valeur à utiliser pour la propriété Language du paramètre CoreWebView2EnvironmentOptions transmis à CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.

> [langage](#language) de chaîne publique

#### UserDataFolder 

Obtient ou définit la valeur à transmettre en tant que paramètre userDataFolder de CoreWebView2Environment. CreateAsync lors de la création d’un environnement avec cette instance.

> [UserDataFolder](#userdatafolder) de chaîne publique

#### CoreWebView2CreationProperties 

Crée une nouvelle instance de CoreWebView2CreationProperties avec les données par défaut pour toutes les propriétés.

> public [CoreWebView2CreationProperties](#corewebview2creationproperties)()

