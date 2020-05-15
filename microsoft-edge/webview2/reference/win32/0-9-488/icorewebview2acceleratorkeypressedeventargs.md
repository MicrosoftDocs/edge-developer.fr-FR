---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 10311cf26b66e824447461530f1ce0870ea01ceb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653371"
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

