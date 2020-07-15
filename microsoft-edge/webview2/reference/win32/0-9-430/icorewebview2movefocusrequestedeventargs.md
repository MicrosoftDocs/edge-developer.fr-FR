---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: fe0c0fae0ec33cbc5ba50ca163b3f4fc8baa61b9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880954"
---
# 0.9.430-interface ICoreWebView2MoveFocusRequestedEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement MoveFocusRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Reason](#get_reason) | La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.
[get_Handled](#get_handled) | Indiquez si l’événement a été géré par l’application.
[put_Handled](#put_handled) | Définissez la propriété Handled.

## Ses

#### get_Reason 

La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.

> valeur publique HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON * value)

#### get_Handled 

Indiquez si l’événement a été géré par l’application.

> valeur publique HRESULT [get_Handled](#get_handled)(bool * value)

Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE. Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée. L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre. S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.

#### put_Handled 

Définissez la propriété Handled.

> [put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)

