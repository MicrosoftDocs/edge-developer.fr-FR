---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885792"
---
# 0.8.355-interface IWebView2ScriptDialogOpeningEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | URI de la page qui a demandé la boîte de dialogue.
[get_Kind](#get_kind) | Type de boîte de dialogue JavaScript.
[get_Message](#get_message) | Message de la boîte de dialogue.
[Accept (Accepter)](#accept) | L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer et inviter les boîtes de dialogue ou ne pas appeler cette méthode pour indiquer l’annulation.
[get_DefaultText](#get_defaulttext) | Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.
[get_ResultText](#get_resulttext) | Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.
[put_ResultText](#put_resulttext) | Définissez la propriété ResultText.
[GetDeferral](#getdeferral) | GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .

## Ses

#### get_Uri 

URI de la page qui a demandé la boîte de dialogue.

> valeur publique HRESULT [get_URI](#get_uri)(LPWSTR * URI)

#### get_Kind 

Type de boîte de dialogue JavaScript.

> [get_Kinds](#get_kind)par valeur public HRESULT (WEBVIEW2_SCRIPT_DIALOG_KIND * type)

#### get_Message 

Message de la boîte de dialogue.

> valeur publique HRESULT [get_Message](#get_message)(LPWSTR * message)

À partir de JavaScript il s’agit du premier paramètre passé à alerte, confirmation et invite.

#### Accept (Accepter) 

L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer et inviter les boîtes de dialogue ou ne pas appeler cette méthode pour indiquer l’annulation.

> [acceptation](#accept)publique HRESULT ()

À partir de JavaScript cela signifie que la fonction confirmer retourne la valeur true si Accept est appelé. Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.

#### get_DefaultText 

Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.

> valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.

#### get_ResultText 

Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.

> valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Ceci est ignoré pour les types de boîte de dialogue autres que invite. Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.

#### put_ResultText 

Définissez la propriété ResultText.

> [put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)

#### GetDeferral 

GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .

> public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * Report)

Vous pouvez l’utiliser pour remplir l’événement ultérieurement.

