---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ecf68bfc338d06fdd2d1a104126685ca105810b0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879379"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement AcceleratorKeyPressed.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Handled](#handled) | Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.
[KeyEventKind](#keyeventkind) | Type d’événement de touche qui a entraîné le déclenchement de l’événement.
[KeyEventLParam](#keyeventlparam) | Valeur LPARAM qui s’accompagne du message de la fenêtre.
[PhysicalKeyStatus](#physicalkeystatus) | Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.
[VirtualKey](#virtualkey) | Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.

## Ses

#### Handled 

Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.

> propriété booléenne [gérée](#handled)

Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur. Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.

#### KeyEventKind 

Type d’événement de touche qui a entraîné le déclenchement de l’événement.

> public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)

#### KeyEventLParam 

Valeur LPARAM qui s’accompagne du message de la fenêtre.

> public ent [KeyEventLParam](#keyeventlparam)

Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.

#### PhysicalKeyStatus 

Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.

> public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)

#### VirtualKey 

Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.

> public uint [VirtualKey](#virtualkey)

Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A». Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).

