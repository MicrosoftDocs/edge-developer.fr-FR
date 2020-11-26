---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 54d62de00a89a3c433fd77e9ec20945adbfc19c3
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191609"
---
# Comprendre les versions de kit de développement logiciel WebView2  

Les nouvelles versions du kit de développement logiciel (SDK) WebView2 sont fournies à la même cadence générale que le navigateur Microsoft Edge \ (chrome \), qui est approximativement toutes les six semaines.  

## Package de mise à jour et version préliminaire  

Le package NuGet WebView2 contient à la fois une version de package et une version préliminaire.  

Le **package de publication** est en transfert compatible et contient les composants suivants.  

*   [API C/C++ Win32][ReferenceWin32]
*   API .NET:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]et [Core][DotnetMicrosoftWebWebview2CoreNamespace].  
    
Les API du SDK sont entièrement prises en charge.  

Le **package** de mise à jour est un sur-ensemble du package de publication doté d' [API expérimentales](#experimental-apis).  

### Feuille de route  

Le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.  Le package de mise à jour contient des API expérimentales susceptibles d’être modifiées en fonction de vos commentaires.  

## API expérimentales  

L’équipe WebView cherche des commentaires sur les API expérimentales qui pourront être incluses dans les versions ultérieures.  Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).  Pour vous aider à évaluer les API expérimentales et à partager vos commentaires, accédez au [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Il est possible de présenter, de modifier et de supprimer des API expérimentales du SDK au kit de développement logiciel (SDK).  Évitez d’utiliser les API expérimentales dans les applications de production.  

> [!NOTE]
> Les API expérimentales peuvent ne pas être disponibles dans votre version installée de WebView2 Runtime.  

## Correspondance des versions du runtime WebView2  
Les applications WebView2 requièrent que les utilisateurs installent un [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].  L’exécution de WebView2 est automatiquement mise à jour vers la dernière version disponible.  Dans certains cas, il est possible que les utilisateurs puissent arrêter les mises à jour automatiques d’WebView2 Runtime, ce qui risque de provoquer des problèmes de compatibilité avec les applications.  

Si les mises à jour de l’application WebView2 sont arrêtées, vérifiez que vous comprenez la version minimale du [Runtime WebView2][MicrosoftDeveloperEdgeWebview2] requis par votre application.  Prenez en compte les deux éléments suivants:  

1.  La version minimale requise du kit de développement logiciel (SDK), dans les [notes de publication][Webview2Releasenotes] de WebView2, sous **version d’WebView2 Runtime minimum**.  Par exemple, pour la version SDK version [1.0.622.22][Webview2Releasenotes1062222], vous devez installer le [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] ou un [canal Microsoft Edge non stable][MicrosoftedgeinsiderDownload] dont le numéro de version est `86.0.616.0` ou version ultérieure.  La version minimale requise par le SDK est modifiée uniquement en cas de changement de rupture dans la plateforme Web.  
1.  La version minimale requise du package NuGet requis pour prendre en charge les interfaces et les API que vous utilisez dans votre application.  Les nouvelles interfaces et API sont ajoutées périodiquement à WebView2.  Les API et interfaces intégrées dans un kit de développement logiciel (SDK) nécessitent différentes versions du runtime WebView2, car les API et l’interface sont ajoutées au kit de développement logiciel à différents moments.  La version du runtime WebView2 requise correspond au numéro de la build, le troisième numéro, de la version du SDK dans laquelle l’API a été introduite pour la première fois.  Par exemple, une nouvelle API ou interface ajoutée dans SDK version [1.0.622.22][Webview2Releasenotes1062222] nécessite la version du runtime WebView2:  `86.0.622.0`  une API ou une interface ajoutée à une version ultérieure du SDK nécessite le runtime WebView2 portant le même numéro de version que le kit de développement logiciel (SDK).  Pour vous aider à déterminer si la version Runtime WebView2 prend en charge une interface ou une API, naviguez pour [déterminer la configuration requise pour le runtime WebView2](#determine-webview2-runtime-requirement).  
    
> [!IMPORTANT]
> Lorsque vous développez des [applications WebView2 persistantes][Webview2ConceptsDistributionEvergreenDistributionMode], testez régulièrement votre application par rapport aux dernières versions des navigateurs Microsoft Edge WebView2 Runtime et non stables.  Dans la mesure où la plateforme Web est en perpétuelle évolution, il est préférable de procéder au test régulier pour vous assurer que votre application fonctionne comme prévu.  

### Déterminer la configuration requise pour WebView2 Runtime  

En fonction du SDK que vous utilisez, prenez en compte les éléments suivants:  

*   **Win32 C/C++**.  Lors de l’utilisation `QueryInterface` pour obtenir une nouvelle interface, vérifiez la valeur de retour de `E_NOINTERFACE` .  La valeur peut indiquer que le runtime WebView2 est une version antérieure et ne prend pas en charge cette interface.  Pour obtenir un exemple de fonctionnement, accédez à la [ligne 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.Net et WinUI**.  Recherchez une `No such interface supported` exception lors de l’utilisation des méthodes, propriétés et événements qui ont été ajoutés aux SDK plus récents.  L’exception peut se produire lorsque le runtime WebView2 est une version antérieure et ne prend pas en charge les API.  
    
Si une API n’est pas disponible, envisagez de supprimer la fonctionnalité associée ou Informez vos utilisateurs qu’une mise à jour du runtime WebView2 est requise.  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  
[Webview2Releasenotes1062222]: ../releasenotes.md#1062222 "1.0.622.22-notes de publication pour WebView2 SDK | Documents Microsoft"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espace de noms Microsoft. Web. WebView2. Core | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft. Web. WebView2. WPF | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft. Web. WebView2. WinForms | Documents Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Référence C++ Win32 WebView2 | Documents Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Développeur Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Ligne 622-AppWindow. cpp-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  
