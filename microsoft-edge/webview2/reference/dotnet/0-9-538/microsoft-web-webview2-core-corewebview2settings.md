---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Settings
ms.openlocfilehash: 7ce831c3259aaede687a5f5bdf3e2a78fc9700a3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010837"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Settings 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

Par défaut, la valeur est TRUE.

#### AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.

> public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)

Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload). Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.

#### AreDevToolsEnabled 

AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.

> public bool [AreDevToolsEnabled](#aredevtoolsenabled)

C’est vrai par défaut.

#### AreHostObjectsAllowed 

La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.

> public bool [AreHostObjectsAllowed](#arehostobjectsallowed)

Par défaut, la valeur est TRUE.

#### IsBuiltInErrorPageEnabled 

La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.

> public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)

Par défaut, la valeur est TRUE. Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.

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

Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations). La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations). Si elle est définie sur false, la communication n’est pas autorisée. PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur. C’est vrai par défaut.

#### IsZoomControlEnabled 

La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.

> public bool [IsZoomControlEnabled](#iszoomcontrolenabled)

Par défaut, la valeur est TRUE. Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.

