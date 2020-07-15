---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: ef1ca9707bba15fdaf8f37a306b56fdfc2c34588
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878980"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs 

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

