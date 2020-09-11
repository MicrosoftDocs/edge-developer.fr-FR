---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: d1e30c17239eb1b609eb3f2c63e48a3a59616131
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011026"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Il s’agit de l’environnement WebView2.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.
[CompareBrowserVersions](#comparebrowserversions) | Comparez les versions du navigateur correctement pour déterminer la version la plus récente, la plus ancienne ou la plus récente.
[CreateAsync](#createasync) | Crée un environnement WebView2 persistant à l’aide de la version latérale installée.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Créer de manière asynchrone un nouveau WebView.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Créer un CoreWebView2PointerInfo vide.
[CreateWebResourceResponse](#createwebresourceresponse) | Créer un objet de réponse aux ressources Web.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.
[GetProviderForHwnd](#getproviderforhwnd) | Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.

Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement. Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.

## Ses

#### BrowserVersionString 

Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.

> [BrowserVersionString](#browserversionstring) de chaîne publique

Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString. Les noms de canaux sont «bêta», «dev» et «Canaries».

#### NewBrowserVersionAvailable 

L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.

> événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)

Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView. Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté. S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.

Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur. Vous pouvez également demander à l’utilisateur de redémarrer l’application.

#### CompareBrowserVersions 

Comparez les versions du navigateur correctement pour déterminer la version la plus récente, la plus ancienne ou la plus récente.

> public static int [CompareBrowserVersions](#comparebrowserversions)(chaîne version1, chaîne version2)

Renvoie-1, 0 ou 1 selon que la propriété version1 est inférieure ou égale ou supérieure à version2, respectivement.

##### Parameters
* `version1` Une des chaînes de version à comparer. 

* `version2` Autre chaîne de version à comparer.

#### CreateAsync 

Crée un environnement WebView2 persistant à l’aide de la version latérale installée.

> tâches asynchrones publiques< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions options)

##### Parameters
* `browserExecutableFolder` Le chemin d’accès relatif au dossier qui contient le bord incorporé. 

* `userDataFolder` userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2. 

* `options` Options permettant de créer un environnement WebView2.

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

> public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)

Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine. Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne. Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.

#### GetAvailableBrowserVersionString 

Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.

> [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)de chaîne statique publique (chaîne browserExecutableFolder)

##### Parameters
* `browserExecutableFolder` Le chemin d’accès relatif au dossier qui contient le bord incorporé.

#### GetProviderForHwnd 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.

> [GetProviderForHwnd](#getproviderforhwnd)d’objet public (IntPtr hwnd)

