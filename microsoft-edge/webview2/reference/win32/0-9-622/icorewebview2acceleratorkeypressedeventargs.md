---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: 7491756d5cc549f805f4f8003ac450cdc6c40b96
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011814"
---
# interface ICoreWebView2AcceleratorKeyPressedEventArgs 

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement AcceleratorKeyPressed.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.
[get_KeyEventKind](#get_keyeventkind) | Type d’événement de touche qui a entraîné le déclenchement de l’événement.
[get_KeyEventLParam](#get_keyeventlparam) | Valeur LPARAM qui s’accompagne du message de la fenêtre.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.
[get_VirtualKey](#get_virtualkey) | Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.
[put_Handled](#put_handled) | Définit la propriété Handled.

## Ses

#### get_Handled 

Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.

> [get_Handled](#get_handled)par le biais du public HRESULT

Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur. Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.

#### get_KeyEventKind 

Type d’événement de touche qui a entraîné le déclenchement de l’événement.

> [get_KeyEventKind](#get_keyeventkind)par le biais du public HRESULT (COREWEBVIEW2_KEY_EVENT_KIND * KeyEventKind)

#### get_KeyEventLParam 

Valeur LPARAM qui s’accompagne du message de la fenêtre.

> valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * lParam)

Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.

#### get_PhysicalKeyStatus 

Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.

> [get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (COREWEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### get_VirtualKey 

Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.

> valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint * VirtualKey)

Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A». Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).

#### put_Handled 

Définit la propriété Handled.

> [put_Handleds](#put_handled)HRESULT publiques (bool géré)

