---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Settings
ms.openlocfilehash: 87b78956c29dac74bd023556a8c495222d248e9f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011857"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled) | La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.
[AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.
[AreDevToolsEnabled](#aredevtoolsenabled) | AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.
[AreHostObjectsAllowed](#arehostobjectsallowed) | La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.
[IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled) | La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.
[IsScriptEnabled](#isscriptenabled) | Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.
[IsStatusBarEnabled](#isstatusbarenabled) | IsStatusBarEnabled vérifie si la barre d’État s’affiche.
[IsWebMessageEnabled](#iswebmessageenabled) | La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.
[IsZoomControlEnabled](#iszoomcontrolenabled) | La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.

Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.

## Ses

#### AreDefaultContextMenusEnabled 

La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.

> public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)

C’est vrai par défaut.

#### AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.

> public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)

Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload). S’il est défini sur true, l’un peut également s’abonner à l’événement ScriptDialogOpening qui contiendra toutes les informations pour la boîte de dialogue et permettre à l’application hôte d’afficher sa propre interface utilisateur personnalisée. C’est vrai par défaut.

#### AreDevToolsEnabled 

AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.

> public bool [AreDevToolsEnabled](#aredevtoolsenabled)

C’est vrai par défaut.

#### AreHostObjectsAllowed 

La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.

> public bool [AreHostObjectsAllowed](#arehostobjectsallowed)

C’est vrai par défaut.

#### IsBuiltInErrorPageEnabled 

La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.

> public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)

C’est vrai par défaut. Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.

#### IsScriptEnabled 

Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.

> public bool [IsScriptEnabled](#isscriptenabled)

Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé. C’est vrai par défaut.

#### IsStatusBarEnabled 

IsStatusBarEnabled vérifie si la barre d’État s’affiche.

> public bool [IsStatusBarEnabled](#isstatusbarenabled)

La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations. C’est vrai par défaut.

#### IsWebMessageEnabled 

La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.

> public bool [IsWebMessageEnabled](#iswebmessageenabled)

Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations). La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et l’événement WebMessageReceived (voir la documentation WebMessageReceived pour plus d’informations). Si elle est définie sur false, la communication n’est pas autorisée. PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur. C’est vrai par défaut.

#### IsZoomControlEnabled 

La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.

> public bool [IsZoomControlEnabled](#iszoomcontrolenabled)

C’est vrai par défaut. Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.

