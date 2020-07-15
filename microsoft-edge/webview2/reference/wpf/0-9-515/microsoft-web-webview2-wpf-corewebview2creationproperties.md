---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 72c85df7d2d58d74cf27e04eb7128fdfa14ca2d9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880254"
---
# Classe Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties 

Espace de noms: Microsoft. Web. WebView2. WPF \
Assemblage: Microsoft.Web.WebView2.Wpf.dll

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

