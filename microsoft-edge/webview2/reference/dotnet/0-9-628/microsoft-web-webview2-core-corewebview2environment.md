---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: c6b1f1c62da5aa5ef64693575abb9cb46ac13851
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011898"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Il s’agit de l’environnement WebView2.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | NewBrowserVersionAvailable se déclenche quand une nouvelle version du navigateur Edge est installée et disponible pour une utilisation via WebView2.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Créer de manière asynchrone un nouveau WebView.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Créer un CoreWebView2PointerInfo vide.
[CreateWebResourceResponse](#createwebresourceresponse) | Créer un objet de réponse aux ressources Web.
[GetProviderForHwnd](#getproviderforhwnd) | Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.

Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement. Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer. 

Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement. Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.

## Ses

#### BrowserVersionString 

Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.

> [BrowserVersionString](#browserversionstring) de chaîne publique

Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString. Les noms de canaux sont «bêta», «dev» et «Canaries».

#### NewBrowserVersionAvailable 

NewBrowserVersionAvailable se déclenche quand une nouvelle version du navigateur Edge est installée et disponible pour une utilisation via WebView2.

> événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)

Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView. Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté. S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.

Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur. Vous pouvez également demander à l’utilisateur de redémarrer l’application.

#### CreateCoreWebView2CompositionControllerAsync 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.

> tâche asynchrone publique< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr FenêtreParent)

FenêtreParent est le HWND dans lequel l’application relie l’arborescence d’éléments visuels du WebView. Il s’agira du HWND que l’application recevra les entrées de pointeur/souris destinées au WebView (et devront utiliser SendMouseInput/SendPointerInput pour transférer). Si l’application déplace l’arborescence d’éléments visuels WebView vers une autre fenêtre, elle doit définir CoreWebView2CompositionController. FenêtreParent pour mettre à jour le nouveau HWND parent de l’arborescence d’éléments visuels.

Définissez la propriété RootVisualTarget sur la CoreWebView2CompositionController créée pour fournir un élément visuel permettant d’héberger l’arborescence visuelle du navigateur.

Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application. Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.

#### CreateCoreWebView2ControllerAsync 

Créer de manière asynchrone un nouveau WebView.

> tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)

FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée. Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView. Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.

Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application. Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.

#### CreateCoreWebView2PointerInfo 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Créer un CoreWebView2PointerInfo vide.

> public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()

La CoreWebView2PointerInfo renvoyée doit être remplie avec toutes les informations pertinentes avant d’appeler SendPointerInput.

#### CreateWebResourceResponse 

Créer un objet de réponse aux ressources Web.

> public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)

Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine. Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne. Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.

#### GetProviderForHwnd 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.

> [GetProviderForHwnd](#getproviderforhwnd)d’objet public (IntPtr hwnd)

