---
description: En savoir plus sur les étapes suivantes pour WebView2
title: Feuille de route Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 7b67e4a6844ead0f845667a70df8657745ece938
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643419"
---
# <a name="microsoft-edge-webview2-roadmap"></a>Microsoft Edge Feuille de route WebView2  

> [!NOTE]
> Last Updated: July 2021  

Le contrôle WebView2 permet aux développeurs d’incorporer des technologies web dans leurs applications natives.  La page suivante décrit la feuille de route prospective pour WebView2.  

> [!NOTE]
> WebView2 est en cours de développement actif et la feuille de route continue d’évoluer en fonction des changements de marché et des commentaires des clients. Notez donc que les plans présentés ici ne sont pas exhaustifs et peuvent faire l’objet de modifications.  

Si vous avez des préoccupations ou des questions sur la feuille de route, faites part de vos commentaires dans le [repo de commentaires.][GithubMicrosoftedgeWebviewfeedbackMain]  

L’équipe WebView2 planifie les efforts majeurs suivants pour les futures mises à jour.  

* Aperçu UWP
* Aperçu MacOS
* Aperçu Xbox
* HoloLens Aperçu

## <a name="webview2-runtime-and-installer"></a>Runtime et programme d’installation WebView2  

[Un modèle de distribution persistant][ConceptDistributionEvergreenModel] vous permet de cibler ou d’installer le runtime WebView2 sur l’ordinateur de votre utilisateur.  Le runtime et le programme d’installation WebView2 persistants ont atteint la disponibilité générale \(GA\).  

## <a name="fixed-version"></a>Version fixe  

[Le modèle de distribution de version][ConceptsDistributionFixedVersionModel] fixe vous permet de mettre en package les Microsoft Edge binaires à l’intérieur de votre application native.  La version fixe a atteint la disponibilité générale \(GA\).  

## <a name="general-availability"></a>Disponibilité générale  

### <a name="win32-cc"></a>Win32 C/C++  

Le SDK Win32 C/C++ a atteint la ga.  

### <a name="net"></a>.NET  

Le SDK .NET a atteint la ga. 

### <a name="windows-ui-library-3"></a>Windows Bibliothèque d’interface utilisateur 3

Vous pouvez accéder aux contrôles WebView2 dans vos applications en utilisant [Windows UI Library 3 (WinUI3)][UwpToolkitsWinui3Index] avec le SDK Windows App. Il est actuellement en prévisualisation. Pour plus d’informations, accédez à la [feuille de route Windows SDK de l’application.][WindowsAppSDK|::ref1::|]

 
<!-- links -->  

[WindowsAppSDKRoadmap]: https://github.com/microsoft/WindowsAppSDK/blob/main/docs/roadmap.md "Feuille de route"
[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modèle de distribution persistant : distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modèle de distribution de version fixe : distribution d’applications à l’aide de WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI Library 3.0 Preview 1 (mai 2020) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Feuille de route de la bibliothèque d’interface utilisateur : microsoft/microsoft-ui-xaml | GitHub"  
