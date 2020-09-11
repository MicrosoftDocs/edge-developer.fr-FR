---
description: Apprenez à développer des applications WebView2 sécurisées
title: Recommandations en matière de développement d’applications WebView2 sécurisées
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge, sécurité
ms.openlocfilehash: 774c812789bea4936611c41915e0c34f93205dba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010760"
---
# Recommandations en matière de développement d’applications WebView2 sécurisées  

Le [contrôle WebView2][Webview2Main] permet aux développeurs d’héberger du contenu Web dans les applications natives. En cas d’utilisation correcte, le contenu Web d’hébergement offre plusieurs avantages, comme l’utilisation de l’interface utilisateur Web, l’accès aux fonctionnalités de la plateforme Web, le partage de code multiplateforme, etc.  Pour éviter toute vulnérabilité pouvant découler de l’hébergement de contenu Web, veillez à concevoir votre application WebView2 pour surveiller étroitement les interactions entre le contenu Web et l’application hôte.  

1.  Considérer tout le contenu Web comme non sécurisé.  
    *   Validez les messages Web et les paramètres d’objet de l’hôte avant d’utiliser chacun d’eux, car les messages et les paramètres Web peuvent être incorrects (ou involontairement) et provoquer une inadvertance du comportement de l’application.
    *   Vérifiez toujours l’origine du document exécuté dans WebView2 et évaluez la fiabilité du contenu.  
1.  Concevez des messages Web et des interactions d’objets hôtes spécifiques au lieu d’utiliser des proxys génériques.  
1.  Définissez les options suivantes pour limiter les fonctionnalités de contenu Web en modifiant [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209622Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceWin3209628MicrosoftWebWebview2CoreCorewebview2settings].  
    *   Définissez `AreHostObjectsAllowed` la valeur sur `false` , si vous ne pensez pas que le contenu Web accède aux objets hôtes.  
    *   Définissez `IsWebMessageEnabled` la valeur sur `false` , si vous ne souhaitez pas que le contenu Web publie des messages Web dans votre application native.  
    *   Définissez `IsScriptEnabled` sur `false` , si vous ne pensez pas que le contenu Web doit exécuter des scripts (par exemple, lors de l’affichage d’un contenu HTML statique).  
    *   Définissez `AreDefaultScriptDialogsEnabled` sur `false` , si vous ne souhaitez pas que le contenu Web s’affiche ou ne s’affiche pas `alert` `prompt` .  
1.  Dans les étapes suivantes, utilisez les `NavigationStarting` `FrameNavigationStarting` événements et pour mettre à jour les paramètres en fonction de l’origine de la nouvelle page.  
    1.  Pour empêcher votre application de naviguer vers certaines pages, utilisez les événements pour vérifier et bloquer la navigation de la page ou du frame.  
    1.  Lorsque vous naviguez vers une nouvelle page, il est possible que vous deviez ajuster les valeurs de propriétés sur [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209622Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceWin3209628MicrosoftWebWebview2CoreCorewebview2settings] , comme décrit précédemment.  
1.  Lorsque vous naviguez vers un nouveau document, utilisez l' `ContentLoading` événement pour supprimer les objets hôtes exposés à l’aide de `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introduction à Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[Webview2ReferenceWin3209622Icorewebview2settings]: ../reference/win32/0-9-622/icorewebview2settings.md "interface ICoreWebView2Settings | Documents Microsoft"  

[Webview2ReferenceWin3209628MicrosoftWebWebview2CoreCorewebview2settings]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2settings.md "Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings | Documents Microsoft"  
