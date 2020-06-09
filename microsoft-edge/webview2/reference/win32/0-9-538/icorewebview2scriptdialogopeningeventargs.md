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
ms.openlocfilehash: 94a008af5a66109add56cec7fd0969d4e20d8ca8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698743"
---
# interface ICoreWebView2ScriptDialogOpeningEventArgs 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement ScriptDialogOpening.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Accept (Accepter)](#accept) | L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.
[get_DefaultText](#get_defaulttext) | Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.
[get_Kind](#get_kind) | Type de boîte de dialogue JavaScript.
[get_Message](#get_message) | Message de la boîte de dialogue.
[get_ResultText](#get_resulttext) | Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.
[get_Uri](#get_uri) | URI de la page qui a demandé la boîte de dialogue.
[GetDeferral](#getdeferral) | GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .
[put_ResultText](#put_resulttext) | Définissez la propriété ResultText.

## Ses

#### Accept (Accepter) 

L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.

> [acceptation](#accept)publique HRESULT ()

À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé. Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.

#### get_DefaultText 

Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.

> valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.

#### get_Kind 

Type de boîte de dialogue JavaScript.

> [get_Kinds](#get_kind)par valeur public HRESULT (COREWEBVIEW2_SCRIPT_DIALOG_KIND * type)

Accepter, confirmer, demander ou beforeunload.

#### get_Message 

Message de la boîte de dialogue.

> valeur publique HRESULT [get_Message](#get_message)(LPWSTR * message)

JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.

#### get_ResultText 

Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.

> valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Ceci est ignoré pour les types de boîte de dialogue autres que invite. Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.

#### get_Uri 

URI de la page qui a demandé la boîte de dialogue.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### GetDeferral 

GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .

> public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Report)

Vous pouvez l’utiliser pour remplir l’événement ultérieurement.

#### put_ResultText 

Définissez la propriété ResultText.

> [put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)

