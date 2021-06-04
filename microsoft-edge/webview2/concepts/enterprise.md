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
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057860"
---
# Gestion des applications WebView2  

[WebView2 est][WebView2Landing] un composant que les développeurs utilisent pour créer leurs applications, et les développeurs peuvent déployer une application [WebView2 Runtime en auto-mise][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] à jour sur l’appareil de l’utilisateur pour alimenter leurs applications.  Ce document explique comment les administrateurs informatiques peuvent gérer les applications WebView2 et Runtime.  Les commentaires des administrateurs informatiques et des développeurs sont les bienvenus sur le repo de commentaires [WebView2.][GithubMicrosoftedgeWebviewfeddback]  

##  <a name="group-policies-for-webview2"></a>Stratégies de groupe pour WebView2  

Les administrateurs informatiques peuvent utiliser des objets de stratégie de groupe \(GPO\) pour configurer les paramètres de stratégie pour WebView2.  L’ensemble de stratégies suivant est/ne s’applique pas à WebView2,  

*   [Microsoft Edge - Les][EdgeUpdatePolicies] stratégies de mise à jour sont disponibles pour que les administrateurs informatiques gèrent les aspects d’installation et de mise à jour du runtime WebView2.  Le navigateur Microsoft Edge web et WebView2 Runtime sont mis à jour à l’aide du même mécanisme de mise à jour.  Sauf si une stratégie, telle que , est spécifique au canal, elle s’applique à la fois au navigateur et `Update` au runtime WebView2.  Par exemple, permet aux administrateurs informatiques de définir une heure pendant chaque jour pour supprimer la mise à jour automatique pour le navigateur et `UpdateSuppressed` WebView2 Runtime.  Cela permet aux administrateurs informatiques de configurer les préférences et les proxies une fois pour le navigateur et WebView2 Runtime afin de contrôler leur bande passante/trafic réseau ou à d’autres fins.  Les administrateurs informatiques [peuvent suivre Microsoft Edge guide pour][ConfigureMicrosoftEdge] configurer Microsoft Edge - Mettre à jour les stratégies.  
*   [Microsoft Edge - Les stratégies de navigateur][EdgeBrowserPolicies] ne s’appliquent pas aux applications WebView2.  Cela est dû au fait que les applications et les navigateurs ont des cas d’utilisation différents et que les administrateurs informatiques ne connaissent peut-être pas les applications qui utilisent WebView2.  L’application de stratégies de navigateur sur WebView2 peut avoir des conséquences inattendues.  Par exemple, les administrateurs informatiques peuvent bloquer JavaScript dans le navigateur et toutes les applications WebView2 utilisant JavaScript sont rompues.  
*   \(Bientôt disponible\) Les stratégies spécifiques de WebView2 – WebView2 exposent un petit ensemble supplémentaire de stratégies de groupe dans les cas où la gestion de WebView2 est directement logique.  Nous recommandons aux développeurs d’applications d’implémenter leurs propres stratégies de groupe pour gérer leur utilisation de WebView2, car il est plus simple pour les administrateurs informatiques de gérer l’application plutôt que WebView2 directement.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Comprendre le runtime et le programme d’installation WebView2 (prévisualisation) : distribution des applications à l’aide de WebView2 | Documents Microsoft"  

[WebView2Landing]: ../index.md "Présentation des Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge - Mettre à jour les stratégies | Documents Microsoft"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge : stratégies de navigateur | Documents Microsoft"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurer les paramètres Microsoft Edge de stratégie sur Windows | Documents Microsoft"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
