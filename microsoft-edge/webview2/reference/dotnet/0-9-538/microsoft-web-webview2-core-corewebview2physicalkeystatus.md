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
ms.openlocfilehash: e0fb3f9ff7114b0c4f2a42893adabfd72e9616de
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698596"
---
# Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

Espace de noms: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[IsExtendedKey](#isextendedkey) | Indique s’il s’agit d’une touche étendue.
[IsKeyReleased](#iskeyreleased) | État de la transition.
[IsMenuKeyDown](#ismenukeydown) | Le code de contexte.
[RepeatCount](#repeatcount) | Nombre répété pour le message actuel.
[ScanCode](#scancode) | Le code de numérisation.
[WasKeyDown](#waskeydown) | État de la clé précédente.

Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .

## Ses

#### IsExtendedKey 

Indique s’il s’agit d’une touche étendue.

> public ent [IsExtendedKey](#isextendedkey)

#### IsKeyReleased 

État de la transition.

> public ent [IsKeyReleased](#iskeyreleased)

#### IsMenuKeyDown 

Le code de contexte.

> public ent [IsMenuKeyDown](#ismenukeydown)

#### RepeatCount 

Nombre répété pour le message actuel.

> public uint [repeatCount](#repeatcount)

#### ScanCode 

Le code de numérisation.

> public uint [ScanCode](#scancode)

#### WasKeyDown 

État de la clé précédente.

> public ent [WasKeyDown](#waskeydown)

