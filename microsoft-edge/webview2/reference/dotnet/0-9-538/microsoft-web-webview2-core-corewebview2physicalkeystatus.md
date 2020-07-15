---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878770"
---
# Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

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

