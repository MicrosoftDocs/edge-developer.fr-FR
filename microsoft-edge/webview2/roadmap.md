---
description: En savoir plus sur les nouveautés à venir pour WebView2
title: Introduction à la WebView 2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 52a2f6d9ef3447955554a5507c3eaab39e6b6a9e
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120367"
---
# Introduction à Microsoft Edge WebView2  

##### Dernière mise à jour: 2020 Oct  

Le contrôle WebView2 permet aux développeurs d’incorporer des technologies Web dans leurs applications natives.  La page suivante présente la procédure prospective pour WebView2.  

> [!NOTE]
> WebView2 est en cours de développement actif et la présentation continue à évoluer en fonction des variations du marché et des commentaires des clients. Veuillez noter que les plans décrits ici ne sont pas exhaustifs et peuvent faire l’objet de modifications.  

Si vous avez des inquiétudes ou des questions concernant la formule d’introduction, reportez-vous à la [référentiel Samples][GithubMicrosoftedgeWebviewfeedbackMain]de vos commentaires.  

L’équipe WebView2 planifie les efforts importants suivants pour les mises à jour ultérieures.  

:::row:::
   :::column span="1":::
      Programme d’installation d’WebView2 Runtime  
   :::column-end:::
   :::column span="2":::
      *   4e trimestre 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Version corrigée  
   :::column-end:::
   :::column span="2":::
      *   4e trimestre 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Disponibilité générale  
   :::column-end:::
   :::column span="2":::
      *   Win32 C/C++ \ (4e trim 2020 \)  
      *   .NET \ (4E TRIM 2020 \)  
      *   [WinUI 3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## Programme d’exécution et de WebView2  

Le [modèle de distribution persistant][ConceptDistributionEvergreenModel] vous permet de cibler ou de mettre en chaîne l’installation de WebView2 Runtime sur l’ordinateur de l’utilisateur.  Le programme d’exécution et de programme d’installation de WebView2 a atteint une disponibilité générale (GA).  

## Version corrigée  

Le [modèle de distribution de version fixe][ConceptsDistributionFixedVersionModel] vous permet d’empaqueter les fichiers binaires Microsoft Edge dans votre application native.  Ce service est actuellement disponible en préversion et destiné à la disponibilité du 4e trimestre 2020.  

## Disponibilité générale  

### Win32 C/C++  

Le kit de développement logiciel (SDK) Win32 C/C++ a atteint la disponibilité.  

### .NET  

Le kit de développement logiciel (SDK) .NET englobe le SDK C/C++ Win32.  Le kit de développement logiciel (SDK) .NET est censé se produire sous la version de Win32 C/C++ GA du 4e trimestre 2020.  

### WinUI 3.0  

Vous pouvez accéder à WebView2 dans vos applications UWP à l’aide de [Win interface 3,0][UwpToolkitsWinui3Index], actuellement en alpha.  Pour plus d’informations sur la façon de rester à jour, consultez la documentation de la [bibliothèque d’interface utilisateur Windows][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modèle de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modèle de distribution de version fixe: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Version d’évaluation de la bibliothèque d’interface utilisateur 3,0 Preview 1 (2020) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Plan de la bibliothèque d’interface utilisateur Windows-Microsoft/Microsoft-UI-XAML | GitHub"  
