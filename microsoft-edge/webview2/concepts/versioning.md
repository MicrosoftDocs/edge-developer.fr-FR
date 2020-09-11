---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 3ce1f0653a14d92571f1365cbfebc8bb2215ecbe
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010676"
---
# Comprendre les versions de kit de développement logiciel WebView2  

WebView2 dépend de Microsoft Edge pour fonctionner.  Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.  La version minimale est répercutée dans la version du package du SDK.  Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure.  La version du navigateur est également spécifiée dans les [notes de publication][Releasenotes]de WebView2.  Pour plus d’informations sur la dernière version du navigateur Microsoft Edge, voir [canaux du navigateur][DeployedgeChannels].  

> [!NOTE]
> WebView2 est actuellement en version preview.  Même si l’équipe WebView s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les kits de développement logiciel (SDK), il n’est pas garanti que les versions plus récentes du navigateur ne prennent pas en charge les versions antérieures du SDK.  Si des modifications sont apportées entre les versions de navigateur et les kits de développement logiciel (SDK), les modifications sont indiquées dans les [notes de publication][Releasenotes].  

À l’avenir, l’équipe WebView planifie le changement du modèle de distribution pour les applications WebView2.  Pour plus d’informations, accédez au [mode de distribution persistant][DistributionEvergreenMode].  

## Package de mise à jour et version préliminaire  

Dans Preview, le package de publication contient les éléments suivants.  

*   [API C/C++ Win32][ReferenceWin3209622]: les API du SDK qui doivent rester identiques à la disponibilité.  

Dans Preview, le package de mise à jour contient les composants suivants.  

*   API .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]et [Core][ReferenceDotnet09628]  
*   API expérimentales.  Pour plus d’informations, consultez la section [API expérimentales](#experimental-apis) .  

## API expérimentales  

L’équipe WebView teste les API expérimentales qui pourraient représenter de nouvelles fonctionnalités.  Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).  Les API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.  Vous devez vous attendre à ce que toutes les API expérimentales soient modifiées avant leur publication.  Évaluez les API expérimentales et partagez des commentaires à l’aide de la [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Évitez d’utiliser les API expérimentales dans les applications de production.  

## Correspondance des versions du runtime WebView2  

Lors de l’écriture d’une application WebView2 à l’aide d’une version de kit de développement logiciel (SDK) spécifique, les utilisateurs de votre application peuvent l’exécuter avec différentes versions compatibles du runtime WebView2.  À l’avenir, une nouvelle version du runtime WebView2 compatible plus récente contient toutes les API non expérimentales d’une ancienne version du runtime WebView2 compatible, ainsi que d’autres API non expérimentales.  

*   Les développeurs en **C/C++ Win32** , lors de l’utilisation `QueryInterface` pour obtenir une nouvelle interface, doivent vérifier la valeur de retour `E_NOINTERFACE` , qui peut indiquer que le runtime WebView2 est antérieur et ne prend pas en charge cette interface particulière.  
*   Les développeurs **.net et WinUI** doivent vérifier une `No such interface supported` exception lors de l’utilisation des méthodes, des propriétés et des événements ajoutés dans les SDK ultérieurs, qui peuvent se produire lorsque le runtime WebView2 est antérieur et ne prend pas en charge ces API spécifiques.  

Si une API n’est pas disponible, envisagez de désactiver la fonctionnalité associée, le cas échéant, ou d’informer l’utilisateur final qu’il doit mettre à jour sa version d’exécution WebView2.  

Il est possible de présenter, de modifier et de supprimer des API expérimentales du SDK au kit de développement logiciel (SDK).  Lorsque vous tentez d’utiliser une API expérimentale qui n’est pas disponible dans le runtime WebView2, vous pouvez observer le même comportement décrit précédemment.  

## Feuille de route  

Lorsque WebView2 atteint un état disponible général stable, le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.  Le package de mise à jour contient des API expérimentales susceptibles d’être modifiées en fonction de vos commentaires et de vos informations de partage.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ReferenceDotnet09628]: ../reference/dotnet/0-9-628-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWin3209622]: ../reference/win32/0-9-622-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
