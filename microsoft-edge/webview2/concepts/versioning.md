---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a47c7295e87cf4295f8cdf898b62aa3b550aa9a5
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120338"
---
# Comprendre les versions de kit de développement logiciel WebView2  

Pour développer une application WebView2, vous devez installer le [Runtime WebView2][MicrosoftDeveloperEdgeWebview2] ou un [canal Microsoft Edge non stable][MicrosoftedgeinsiderDownload].  La version minimale requise est incluse dans la version du package NuGet du SDK.  Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer le [Runtime WebView2][MicrosoftDeveloperEdgeWebview2] ou un [canal Microsoft Edge non stable][MicrosoftedgeinsiderDownload] avec un numéro de version 488 ou une version ultérieure.  La version minimale requise est également spécifiée dans les [notes de publication][Releasenotes]de WebView2.  Les nouvelles versions du kit de développement logiciel (SDK) WebView2 sont fournies à la même cadence générale que le navigateur Microsoft Edge \ (chrome \), qui est approximativement toutes les six semaines.  

> [!IMPORTANT]
> Lorsque vous développez des applications WebView2 persistantes, testez régulièrement votre application par rapport aux dernières versions des navigateurs Microsoft Edge WebView2 Runtime et non stables.  Dans la mesure où la plateforme Web est en perpétuelle évolution, il est préférable de procéder au test régulier pour vous assurer que votre application s’exécute comme prévu.  

## Package de mise à jour et version préliminaire  

Le package NuGet WebView2 contient à la fois une version de package et une version préliminaire.  

Le package de publication est en transfert compatible et contient les [API C/C++ Win32][ReferenceWin32].  Les API dans ce SDK sont entièrement prises en charge.  

Le package de mise à jour est un sur-ensemble du package de publication avec les composants supplémentaires indiqués ci-dessous.  

*   API .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]et [Core][DotnetMicrosoftWebWebview2CoreNamespace]  
*   API expérimentales: pour plus d’informations, accédez à la section [API expérimentales](#experimental-apis) .  

## API expérimentales  

L’équipe WebView teste les API d’expérimentation qui pourront être incluses dans les versions ultérieures.  Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).  Les API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.  Vous pouvez évaluer les API expérimentales et partager des commentaires à l’aide de l' [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Évitez d’utiliser les API expérimentales dans les applications de production.  

## Correspondance des versions du runtime WebView2  

Lors de l’écriture d’une application WebView2 à l’aide d’une version de kit de développement logiciel (SDK) spécifique, les utilisateurs de votre application peuvent l’exécuter avec plusieurs versions compatibles du runtime WebView2.  L’équipe WebView travaille sur une version d’WebView2 Runtime compatible qui contient des API non expérimentales des versions précédentes du runtime et des nouvelles API non expérimentales.  

En fonction du SDK que vous utilisez, prenez en compte les éléments suivants: 

*   **Win32 C/C++**.  Lors de l’utilisation `QueryInterface` pour obtenir une nouvelle interface, recherchez une valeur de retour de `E_NOINTERFACE` .  Cette valeur peut indiquer que le runtime WebView2 est une version antérieure et ne prend pas en charge cette interface.  
*   **.Net et WinUI**.  Recherchez une `No such interface supported` exception lors de l’utilisation des méthodes, propriétés et événements qui ont été ajoutés aux SDK plus récents.  Cette exception peut se produire lorsque le runtime WebView2 est une version antérieure et ne prend pas en charge ces API.  

Si une API n’est pas disponible, envisagez de supprimer la fonctionnalité associée ou Informez vos utilisateurs qu’ils ont besoin de mettre à jour leur version de WebView2 Runtime.  

Il est possible de présenter, de modifier et de supprimer des API expérimentales du SDK au kit de développement logiciel (SDK).  Les API expérimentales peuvent ne pas être disponibles dans votre version installée de WebView2 Runtime.  

## Feuille de route  

Le package de publication contient toutes les API Win32 C/C++ stables et prises en charge.  À l’avenir, le package de publication contient toutes les API .NET stables et prises en charge lorsqu’elles sont disponibles en général.  Le package de mise à jour contient des API expérimentales susceptibles d’être modifiées en fonction de vos commentaires et de vos informations de partage.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espace de noms Microsoft. Web. WebView2. Core | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft. Web. WebView2. WPF | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft. Web. WebView2. WinForms | Documents Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Référence C++ Win32 WebView2 | Documents Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Développeur Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  
