---
description: Comprendre comment gérer les applications WebView2
title: Gestion des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, enterprise, group policy, manageability
ms.openlocfilehash: f32488a26f3e3c926517b0e40e6aac6a309e42b8
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627963"
---
# <a name="managing-webview2-applications"></a>Gestion des applications WebView2  

[WebView2 est][WebView2Landing] un composant que les développeurs utilisent pour créer leurs applications, et les développeurs peuvent déployer un [runtime WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] persistant à mise à jour autonome sur l’appareil de l’utilisateur pour alimenter leurs applications.  Ce document explique comment les administrateurs informatiques peuvent gérer les applications WebView2 et Runtime.  Les commentaires des administrateurs informatiques et des développeurs sont les bienvenus sur le repo de commentaires [WebView2.][GithubMicrosoftedgeWebviewfeddback]  

## <a name="group-policies-for-webview2"></a>Stratégies de groupe pour WebView2  

Les administrateurs informatiques peuvent utiliser des objets de stratégie de groupe \(GPO\) pour configurer les paramètres de stratégie pour WebView2.  L’ensemble de stratégies suivant est/ne s’applique pas à WebView2,  

*   [Microsoft Edge - Les][EdgeUpdatePolicies] stratégies de mise à jour sont disponibles pour que les administrateurs informatiques gèrent les aspects d’installation et de mise à jour du runtime WebView2.  Le navigateur Microsoft Edge web et WebView2 Runtime sont mis à jour à l’aide du même mécanisme de mise à jour.  Sauf si une stratégie, telle que , est spécifique au canal, elle s’applique à la fois au navigateur `Update` et au runtime WebView2.  Par exemple, permet aux administrateurs informatiques de définir une heure pendant chaque jour pour supprimer la mise à jour automatique pour le navigateur et `UpdateSuppressed` WebView2 Runtime.  Cela permet aux administrateurs informatiques de configurer les préférences et les proxies une fois pour le navigateur et WebView2 Runtime afin de contrôler leur bande passante/trafic réseau ou à d’autres fins.  Les administrateurs informatiques [peuvent suivre Microsoft Edge guide pour][ConfigureMicrosoftEdge] configurer Microsoft Edge - Mettre à jour les stratégies.  
*   [Microsoft Edge - Les stratégies de navigateur][EdgeBrowserPolicies] ne s’appliquent pas aux applications WebView2.  Cela est dû au fait que les applications et les navigateurs ont des cas d’utilisation différents et que les administrateurs informatiques ne connaissent peut-être pas les applications qui utilisent WebView2.  L’application de stratégies de navigateur sur WebView2 peut avoir des conséquences inattendues.  Par exemple, les administrateurs informatiques peuvent bloquer JavaScript dans le navigateur et toutes les applications WebView2 utilisant JavaScript sont rompues.  
*   [Les stratégies spécifiques à WebView2][WebView2Policies] sont disponibles pour que vous gériez WebView2 directement.  Toutefois, nous recommandons aux développeurs d’implémenter leurs propres stratégies de groupe pour gérer l’utilisation de WebView2, car il est plus facile pour les administrateurs de gérer l’application au lieu de gérer WebView2 directement.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Comprendre le runtime et le programme d’installation WebView2 (prévisualisation) : distribution des applications à l’aide de WebView2 | Documents Microsoft"  

[WebView2Landing]: ../index.md "Présentation des Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge - Mettre à jour les stratégies | Documents Microsoft"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge : stratégies de navigateur | Documents Microsoft"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurer les paramètres Microsoft Edge de stratégie sur Windows | Documents Microsoft"  
[WebView2Policies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge Documentation sur les stratégies WebView2 | Documents Microsoft" 

[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
