---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698736"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures 

> [!NOTE]
> Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).

Espace de noms: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Height](#height) | Hauteur de la fenêtre.
[Vers la gauche](#left) | Position gauche de la fenêtre.
[MenuBar](#menubar) | Si vous souhaitez afficher la barre de menus.
[Barres](#scrollbars) | Si les barres de défilement s’affichent ou non.
[Statut](#status) | Si vous souhaitez ou non ajouter une barre d’État.
[ToolBar](#toolbar) | Affichage de la barre d’outils du navigateur.
[Top](#top) | La position supérieure de la fenêtre.
[Largeur](#width) | La largeur de la fenêtre.
[HasPosition](#hasposition) | A spécifié les valeurs Left et Top.
[HasSize](#hassize) | A spécifié des valeurs de hauteur et de largeur.

## Ses

#### Height 

Hauteur de la fenêtre.

> [hauteur](#height) publique uint

#### Vers la gauche 

Position gauche de la fenêtre.

> public uint vers la [gauche](#left)

Va échouer si HasPosition est faux.

#### MenuBar 

Si vous souhaitez afficher la barre de menus.

> Barre de [menus](#menubar) publique ent

#### Barres 

Si les barres de défilement s’affichent ou non.

> Barres de [défilement](#scrollbars) public ent

#### Statut 

Si vous souhaitez ou non ajouter une barre d’État.

> [État](#status) d’ent public

#### ToolBar 

Affichage de la barre d’outils du navigateur.

> [barre d’outils](#toolbar) public ent

#### Top 

La position supérieure de la fenêtre.

> public uint [Top](#top)

Va échouer si HasPosition est faux.

#### Largeur 

La largeur de la fenêtre.

> [largeur](#width) publique uint

#### HasPosition 

A spécifié les valeurs Left et Top.

> public ent [HasPosition](#hasposition)()

#### HasSize 

A spécifié des valeurs de hauteur et de largeur.

> public ent [HasSize](#hassize)()

