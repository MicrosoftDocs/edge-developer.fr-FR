---
description: Modèles de version utilisés pour Microsoft Edge WebView2
title: Comprendre les versions du SDK WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: b292f59e264293a958eb619d04b751203cb517ac
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461177"
---
# <a name="understand-webview2-sdk-versions"></a>Comprendre les versions du SDK WebView2  

Les nouvelles versions du SDK WebView2 sont livrées à la même cadence générale que le navigateur Microsoft Edge \(Chromium\), soit environ toutes les six semaines.  

## <a name="release-and-prerelease-package"></a>Release and prerelease package  

Le package NuGet WebView2 contient à la fois une version et une version pré-version.  

Le **package de publication** est compatible avec le forward et contient les composants suivants.  

*   [API Win32 C/C++][ReferenceWin32]
*   API .NET :  [WPF,][DotnetMicrosoftWebWebview2WpfNamespace] [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]et [Core][DotnetMicrosoftWebWebview2CoreNamespace].  
    
Les API du SDK sont entièrement pris en charge.  

Le **package de version prédéfinie** est un sur-ensemble du package de publication avec des API [expérimentales.](#experimental-apis)  Évitez d’utiliser le SDK de pré-mise en production pour créer des applications de production.  

### <a name="roadmap"></a>Feuille de route  

Le package de publication contient toutes les API Win32 C/C++ et .NET stables et pris en charge.  Le package de version préreplique contient des API expérimentales qui peuvent faire l’objet de changements en fonction de vos commentaires.  

## <a name="experimental-apis"></a>API expérimentales  

L’équipe WebView recherche des commentaires sur les API expérimentales qui peuvent être incluses dans les prochaines publication.  Les API expérimentales sont marquées comme `experimental` dans le SDK.  Pour vous aider à évaluer les API expérimentales et à partager vos commentaires, accédez au repo de [commentaires WebView.][GithubMicrosoftedgeWebviewfeedback]  

> [!CAUTION]
> Les API expérimentales peuvent être introduites, modifiées et supprimées du SDK vers le SDK.  Évitez d’utiliser les API expérimentales dans les applications de production.  

> [!NOTE]
> Il se peut que les API expérimentales ne soient pas disponibles dans votre version installée de WebView2 Runtime.  

## <a name="matching-webview2-runtime-versions"></a>Correspondance des versions d’runtime de WebView2  
Les applications WebView2 nécessitent que les utilisateurs installent [un runtime WebView2.][MicrosoftDeveloperEdgeWebview2]  WebView2 Runtime est automatiquement mis à jour vers la dernière version disponible.  Dans certains scénarios, les utilisateurs peuvent vouloir arrêter les mises à jour automatiques du runtime WebView2, ce qui peut entraîner des problèmes de compatibilité des applications.  

Si les mises à jour WebView2 Runtime sont arrêtées, assurez-vous que vous comprenez la version minimale du [runtime WebView2][MicrosoftDeveloperEdgeWebview2] requise par votre application.  Prenez en compte les deux éléments suivants :  

1.  La version minimale requise du SDK pour charger correctement une instance webview2 se trouve dans les notes de publication [WebView2][Webview2Releasenotes] sous Version minimale de Microsoft Edge à **charger.**  La version minimale à charger requise par le SDK change uniquement lorsqu’une modification importante se produit sur la plateforme web.  Par exemple, pour la version [1.0.622.22][Webview2Releasenotes1062222]du SDK, vous devez installer [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] ou un canal [Microsoft Edge non stable][MicrosoftedgeinsiderDownload] avec un numéro de build ou une version plus `86.0.616.0` récente.   
1.  La version minimale requise du package NuGet requise pour prendre en charge les interfaces et les API de votre application se trouve dans les [notes][Webview2Releasenotes] de publication WebView2 sous **Compatibilité complète des API.**  De nouvelles interfaces et API sont régulièrement ajoutées à WebView2.  Les API et interfaces regroupées dans un SDK nécessitent différentes versions de WebView2 Runtime, car les API et l’interface sont ajoutées au SDK à différents moments.  La version WebView2 Runtime requise correspond au numéro de build, le troisième numéro, de la version du SDK dans qui l’API a été introduite pour la première fois.  Par exemple, une nouvelle API ou interface ajoutée dans la version [1.0.622.22][Webview2Releasenotes1062222] du SDK nécessite la version Runtime webView2 ou une version `86.0.622.0` plus récente.  Une API ou une interface ajoutée dans une version ultérieure du SDK nécessite un runtime WebView2 qui a le même numéro de version que le SDK.  Pour vous aider à déterminer si la version Runtime de WebView2 prend en charge une interface ou une API, accédez à Déterminer l’exigence [d’utilisation de WebView2.](#determine-webview2-runtime-requirement)  
    
> [!IMPORTANT]
> Lorsque vous développez des applications [WebView2][Webview2ConceptsDistributionEvergreenDistributionMode]persistantes, testez régulièrement votre application par rapport aux dernières versions du Runtime WebView2 et des canaux Microsoft Edge non stables.  Étant donné que la plateforme web évolue constamment, des tests réguliers sont le meilleur moyen de s’assurer que votre application se exécute comme prévu.  

### <a name="determine-webview2-runtime-requirement"></a>Déterminer l’exigence d’un runtime WebView2  

En fonction du SDK que vous utilisez, prenez en compte les éléments suivants :  

*   **Win32 C/C++**.  Lorsque vous utilisez `QueryInterface` pour obtenir une nouvelle interface, vérifiez la valeur de retour de `E_NOINTERFACE` .  La valeur peut indiquer que WebView2 Runtime est une version antérieure et ne prend pas en charge cette interface.  Pour obtenir un exemple de fonctionnement, accédez à [la ligne 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.NET et WinUI**.  Recherchez une exception lors de l’utilisation de méthodes, de propriétés et d’événements qui ont été ajoutés à des `No such interface supported` SDK plus récents.  L’exception peut se produire lorsque WebView2 Runtime est une version antérieure et ne prend pas en charge les API.  
    
Si une API n’est pas disponible, envisagez de supprimer la fonctionnalité associée ou informez vos utilisateurs qu’une mise à jour du runtime WebView2 est requise.  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Mode de distribution persistant : distribution des applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication du SDK WebView2 | Documents Microsoft"  
[Webview2Releasenotes1062222]: ../releasenotes.md#1062222 "1.0.622.22 - Notes de publication du SDK WebView2 | Documents Microsoft"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espace de noms Microsoft.Web.WebView2.Core | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft.Web.WebView2.Wpf | Documents Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft.Web.WebView2.WinForms | Documents Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Référence WebView2 Win32 C++ | Documents Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Développeur Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Ligne 622 - AppWindow.cpp - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  
