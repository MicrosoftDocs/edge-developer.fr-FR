---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 3862576134d1179fb24b2ce865f705b2bf1db8a6
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757605"
---
# Comprendre les versions de kit de développement logiciel WebView2  

WebView2 dépend de Microsoft Edge pour fonctionner. Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.  La version minimale est répercutée dans la version du package du SDK.  Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure. La version du navigateur est également spécifiée dans les [notes de publication][Webview2Releasenotes]de WebView2.  Pour plus d’informations sur les dernières versions du navigateur, voir [canaux de navigateur][DeployedgeChannels].  

> [!NOTE]
> WebView2 est actuellement en version preview.  Même si l’équipe WebView de Microsoft Edge s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les SDK, il n’est pas garanti que certaines versions plus récentes du navigateur ne prennent pas en charge les versions antérieures du SDK.  Si des modifications sont apportées entre les versions de navigateur et les kits de développement logiciel (SDK), l’équipe WebView Microsoft Edge spécifie les modifications apportées aux [notes de publication][Webview2Releasenotes].  

À l’avenir, le modèle de distribution pour les applications WebView2 changera. Pour plus d’informations, consultez [WebView2 Runtime][Webview2IndexEdgeRuntime].  
 
## Package de publication et version préliminaire  

Dans Preview, le package de publication contient les éléments suivants.  

*   [API C/C++ Win32][Webview2ReferenceWin3209538]: les API du SDK qui doivent rester identiques à la disponibilité. 

Dans Preview, le package de la version préliminaire contient les éléments suivants.  

*   API .NET: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]et [Core][Webview2ReferenceDotnet09538]
*   API expérimentales.  Pour plus d’informations, consultez la section [API Experimantal](#experimental-apis) .  

### API expérimentales  

L’équipe WebView teste des API qui représentent de nouvelles fonctionnalités intitulées API expérimentales.  Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).  Certaines API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.  Vous devez vous attendre à ce que toutes les API expérimentales soient modifiées avant leur publication.  Évaluez les API expérimentales et partagez des commentaires à l’aide de la [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Évitez d’utiliser les API expérimentales dans les applications de production.  

### Feuille de route  

Lorsque WebView2 atteint un état disponible général stable, le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.  Le package de la version préliminaire contient des API expérimentales susceptibles d’être modifiées en fonction des commentaires du développeur et des informations partagées.  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2-distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
