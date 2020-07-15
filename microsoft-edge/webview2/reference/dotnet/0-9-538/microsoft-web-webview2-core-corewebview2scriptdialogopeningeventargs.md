---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: cbff39e9393026f51471bdfb3189600e2d7bf109
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879694"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement ScriptDialogOpening.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[DefaultText](#defaulttext) | Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.
[Types](#kind) | Type de boîte de dialogue JavaScript.
[Message](#message) | Message de la boîte de dialogue.
[ResultText](#resulttext) | Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.
[URI](#uri) | URI de la page qui a demandé la boîte de dialogue.
[Accept (Accepter)](#accept) | L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.
[GetDeferral](#getdeferral) | GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.

## Ses

#### DefaultText 

Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.

> [DefaultText](#defaulttext) de chaîne publique

Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.

#### Types 

Type de boîte de dialogue JavaScript.

> [type](#kind) CoreWebView2ScriptDialogKind public

Accepter, confirmer, demander ou beforeunload.

#### Message 

Message de la boîte de dialogue.

> [message](#message) de chaîne publique

JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.

#### ResultText 

Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.

> [ResultText](#resulttext) de chaîne publique

Ceci est ignoré pour les types de boîte de dialogue autres que invite. Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.

#### URI 

URI de la page qui a demandé la boîte de dialogue.

> [URI](#uri) de chaîne publique

#### Accept (Accepter) 

L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.

> public void [Accept](#accept)()

À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé. Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.

#### GetDeferral 

GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.

> public CoreWebView2Deferral [GetDeferral](#getdeferral)()

Vous pouvez l’utiliser pour remplir l’événement ultérieurement.

