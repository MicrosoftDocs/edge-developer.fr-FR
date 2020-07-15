---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a3e8a958a70820bf32bd3a76acc9ee503f568438
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877755"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Il s’agit de l’environnement WebView2.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.
[CreateAsync](#createasync) | Crée un environnement WebView2 persistant à l’aide de la version latérale installée.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Créer de manière asynchrone un nouveau WebView.
[CreateWebResourceResponse](#createwebresourceresponse) | Créer un objet de réponse aux ressources Web.

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

#### CreateAsync 

Crée un environnement WebView2 persistant à l’aide de la version latérale installée.

> tâches asynchrones publiques< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions options)

##### Parameters
* `browserExecutableFolder` Le chemin d’accès relatif au dossier qui contient le bord incorporé. 

* `userDataFolder` userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2. 

* `options` Options permettant de créer un environnement WebView2.

#### CreateCoreWebView2ControllerAsync 

Créer de manière asynchrone un nouveau WebView.

> tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)

FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée. Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView. Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.

Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application. Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.

#### CreateWebResourceResponse 

Créer un objet de réponse aux ressources Web.

> public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)

Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine. Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne. Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.

