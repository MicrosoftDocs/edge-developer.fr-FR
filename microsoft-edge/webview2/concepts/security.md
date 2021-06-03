---
description: Comprendre comment développer des applications WebView2 sécurisées
title: Meilleures pratiques pour le développement d’applications WebView2 sécurisées
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, security
ms.openlocfilehash: d53417cc1ac98b44565692edbaec06216f7c110b
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119001"
---
# Meilleures pratiques pour le développement d’applications WebView2 sécurisées  

Le [contrôle WebView2 permet aux][Webview2Main] développeurs d’héberger du contenu web dans les applications natives. Lorsqu’il est utilisé correctement, l’hébergement de contenu web offre plusieurs avantages, tels que l’utilisation de l’interface utilisateur web, l’accès aux fonctionnalités de la plateforme web, le partage de code entre plateformes, etc.  Pour éviter les vulnérabilités qui peuvent survenir lors de l’hébergement de contenu web, veillez à concevoir votre application WebView2 pour surveiller étroitement les interactions entre le contenu web et l’application hôte.  

1.  Traitez tout le contenu web comme non sécurisé.  
    *   Validez les messages web et les paramètres d’objet hôte avant de les utiliser, car les messages et paramètres web peuvent être malformés \(involontairement ou malveillantment\) et provoquer un comportement inattendu de l’application.
    *   Vérifiez toujours l’origine du document en cours d’exécution dans WebView2 et évaluez la fiabilité du contenu.  
1.  Concevez des messages web spécifiques et des interactions d’objet hôte au lieu d’utiliser des proxies génériques.  
1.  Définissez les options suivantes pour restreindre la fonctionnalité de contenu web en modifiant [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] ou [CoreWebView2Settings (.NET).][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]  
    *   Définissez sur , si vous ne vous attendez pas à ce que `AreHostObjectsAllowed` le contenu web accède aux objets `false` hôtes.  
    *   Définissez sur , si vous ne vous attendez pas à ce que le `IsWebMessageEnabled` contenu web publie des messages web dans votre application `false` native.  
    *   Définissez sur , si vous ne vous attendez pas à ce que le contenu web exécute des `IsScriptEnabled` scripts \(par exemple, lorsque vous affichez du `false` contenu html statique\).  
    *   Définissez sur , si vous ne vous attendez pas à ce que le `AreDefaultScriptDialogsEnabled` `false` contenu web s’affiche `alert` ou les boîtes de `prompt` dialogue.  
1.  Dans les étapes suivantes, utilisez les événements et les événements pour mettre à jour les paramètres en `NavigationStarting` fonction de l’origine de la nouvelle `FrameNavigationStarting` page.  
    1.  Pour empêcher votre application de naviguer vers certaines pages, utilisez les événements pour vérifier, puis bloquer la navigation de page ou d’image.  
    1.  Lorsque vous naviguez vers une nouvelle page, vous devrez peut-être ajuster les valeurs des propriétés sur [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] ou [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] comme décrit précédemment.  
1.  Lorsque vous naviguez vers un nouveau document, utilisez l’événement pour supprimer les `ContentLoading` objets hôtes exposés à l’aide de `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Présentation des Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "interface ICoreWebView2Settings | Documents Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "Classe CoreWebView2Settings (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
