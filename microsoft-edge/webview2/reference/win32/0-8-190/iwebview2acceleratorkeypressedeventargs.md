---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 5d052488d23f3d016ba2fd71eb929d5aa2ebea6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877363"
---
# 0.8.355-interface IWebView2AcceleratorKeyPressedEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement AcceleratorKeyPressed.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_KeyEventType](#get_keyeventtype) | Type d’événement de touche qui a entraîné le déclenchement de l’événement.
[get_VirtualKey](#get_virtualkey) | Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.
[get_KeyEventLParam](#get_keyeventlparam) | Valeur LPARAM qui s’accompagne du message de la fenêtre.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.
[Poignée](#handle) | Les appels permettent au processus de navigateur de continuer.

## Ses

#### get_KeyEventType 

Type d’événement de touche qui a entraîné le déclenchement de l’événement.

> [get_KeyEventType](#get_keyeventtype)par le biais du public HRESULT (WEBVIEW2_KEY_EVENT_TYPE * KeyEventType)

Il s’agit de l’une des WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN ou WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.

#### get_VirtualKey 

Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.

> valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint * VirtualKey)

Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A». Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).

#### get_KeyEventLParam 

Valeur LPARAM qui s’accompagne du message de la fenêtre.

> valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * lParam)

Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.

#### get_PhysicalKeyStatus 

Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.

> [get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (WEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### Poignée 

Les appels permettent au processus de navigateur de continuer.

> [handle](#handle)HRESULT public (bool géré)

Le passage de la valeur TRUE empêchera le navigateur d’exécuter l’action par défaut pour cette touche accélérateur. Si le gestionnaire d’événements renvoie sans appeler [handle ()](#handle), il est équivalent au handle d’appel (false). Le [handle d’appel ()](#handle) après son appel ou le gestionnaire d’événements renvoyé ne fera rien.

