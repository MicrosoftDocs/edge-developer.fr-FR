---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 059bbeb34f372af0cef944e484599c0b50543cc9
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844424"
---
# Comprendre les versions de kit de développement logiciel WebView2  

WebView2 dépend de Microsoft Edge pour fonctionner.  Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.  La version minimale est répercutée dans la version du package du SDK.  Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure.  La version du navigateur est également spécifiée dans les [notes de publication][Releasenotes]de WebView2.  Pour plus d’informations sur les dernières versions du navigateur, voir [canaux de navigateur][DeployedgeChannels].  

> [!NOTE]
> WebView2 est actuellement en version preview.  Même si l’équipe WebView s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les SDK, il n’est pas garanti dans la mesure où les versions plus récentes du navigateur risquent de ne pas prendre en charge des versions antérieures du SDK.  Si des modifications sont apportées entre les versions de navigateur et les kits de développement logiciel (SDK), l’équipe WebView spécifie les modifications apportées aux [notes de publication][Releasenotes].  

À l’avenir, l’équipe WebView planifie le changement du modèle de distribution pour les applications WebView2.  Pour plus d’informations, reportez-vous à la section [mode de distribution persistant][DistributionEvergreenMode].  
 
## Package de publication et version préliminaire  

Dans Preview, le package de publication contient les éléments suivants.  

*   [API C/C++ Win32][ReferenceWin3209538]: les API du SDK qui doivent rester identiques à la disponibilité. 

Dans Preview, la version préliminaire du package contient les composants suivants.  

*   API .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]et [Core][ReferenceDotnet09538]
*   API expérimentales.  Pour plus d’informations, consultez la section [API expérimentales](#experimental-apis) .  

### API expérimentales  

L’équipe WebView teste des API qui représentent de nouvelles fonctionnalités intitulées API expérimentales.  Les API expérimentales sont marquées comme `experimental` dans le kit de développement logiciel (SDK).  Certaines API expérimentales pourront être fournies sous la forme d’API entièrement stables dans le package de publication.  Vous devez vous attendre à ce que toutes les API expérimentales soient modifiées avant leur publication.  Évaluez les API expérimentales et partagez des commentaires à l’aide de la [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Évitez d’utiliser les API expérimentales dans les applications de production.  

### Feuille de route  

Lorsque WebView2 atteint un état disponible général stable, le package de publication contient toutes les API Win32 C/C++ et .NET stables et prises en charge.  Le package de la version préliminaire contient des API expérimentales susceptibles d’être modifiées en fonction des commentaires du développeur et des informations partagées.  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
