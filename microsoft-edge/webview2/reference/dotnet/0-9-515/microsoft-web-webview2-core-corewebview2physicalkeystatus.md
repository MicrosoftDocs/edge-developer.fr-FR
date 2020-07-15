---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: da7069fb4dad164720bb697a250a216a0bd452ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881199"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus struct 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

