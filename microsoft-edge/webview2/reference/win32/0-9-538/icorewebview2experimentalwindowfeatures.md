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
ms.openlocfilehash: 576f54f2a7ecc2e1e99758719e80cc589c5bc791
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698756"
---
# interface ICoreWebView2ExperimentalWindowFeatures 

> [!NOTE]
> Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Height](#get_height) | Hauteur de la fenêtre.
[get_Left](#get_left) | Position gauche de la fenêtre. Va échouer si HasPosition est faux.
[get_MenuBar](#get_menubar) | Si vous souhaitez afficher la barre de menus.
[get_ScrollBars](#get_scrollbars) | Si les barres de défilement s’affichent ou non.
[get_Status](#get_status) | Si vous souhaitez ou non ajouter une barre d’État.
[get_Toolbar](#get_toolbar) | Affichage de la barre d’outils du navigateur.
[get_Top](#get_top) | La position supérieure de la fenêtre. Va échouer si HasPosition est faux.
[get_Width](#get_width) | La largeur de la fenêtre.
[HasPosition](#hasposition) | A spécifié les valeurs Left et Top.
[HasSize](#hassize) | A spécifié des valeurs de hauteur et de largeur.

Ces champs correspondent à la valeur «windowFeatures» transmise à Window. ouvrir comme spécifié dans[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)

## Ses

#### get_Height 

Hauteur de la fenêtre.

> valeur de HRESULT publique [get_Height](#get_height)(UInt32 * Height)

La valeur minimale est 100. Va échouer si HasSize est faux.

#### get_Left 

Position gauche de la fenêtre. Va échouer si HasPosition est faux.

> valeur publique HRESULT [get_Left](#get_left)(UInt32 * Left)

#### get_MenuBar 

Si vous souhaitez afficher la barre de menus.

> [get_MenuBars](#get_menubar)par valeur HRESULT publiques (bool * BarreMenus)

#### get_ScrollBars 

Si les barres de défilement s’affichent ou non.

> [get_ScrollBars](#get_scrollbars)par le biais du public HRESULT

#### get_Status 

Si vous souhaitez ou non ajouter une barre d’État.

> valeur publique HRESULT [get_Status](#get_status)(bool * Status)

#### get_Toolbar 

Affichage de la barre d’outils du navigateur.

> [get_Toolbars](#get_toolbar)par valeur de passe publiques (bool * Toolbar)

#### get_Top 

La position supérieure de la fenêtre. Va échouer si HasPosition est faux.

> valeur publique HRESULT [get_Top](#get_top)(UInt32 * Top)

#### get_Width 

La largeur de la fenêtre.

> [get_Width](#get_width)des valeurs HRESULT publiques (UInt32 * Width)

La valeur minimale est 100. Va échouer si HasSize est faux.

#### HasPosition 

A spécifié les valeurs Left et Top.

> public HRESULT [HasPosition](#hasposition)(bool * HasPosition)

#### HasSize 

A spécifié des valeurs de hauteur et de largeur.

> public HRESULT [HasSize](#hassize)(bool * HasSize)
