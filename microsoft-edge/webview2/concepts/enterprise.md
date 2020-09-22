---
description: Comprendre comment gérer les applications WebView2
title: Gestion des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge, entreprise, stratégie de groupe, gestion
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057860"
---
# Gestion des applications WebView2  

[WebView2][WebView2Landing] est un composant utilisé par les développeurs pour générer leurs applications, et les développeurs peuvent déployer un [Runtime WebView2 à mise à jour automatique persistant][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] sur un appareil utilisateur pour alimenter leurs applications.  Ce document explique comment les administrateurs informatiques pourront gérer les applications WebView2 et l’exécution.  Des commentaires de la part des administrateurs informatiques et des développeurs sont bienvenue sur le [WebView2 de commentaires référentiel Samples][GithubMicrosoftedgeWebviewfeddback].  

## Stratégies de groupe pour WebView2  

Les administrateurs informatiques pourront utiliser les objets de stratégie de groupe \ (GPO \) pour configurer les paramètres de stratégie pour WebView2.  Les stratégies suivantes ne s’appliquent pas à WebView2,  

*   Les [stratégies Microsoft Edge-Update][EdgeUpdatePolicies] sont disponibles pour les administrateurs informatiques qui peuvent gérer les aspects de l’installation et de la mise à jour du runtime WebView2.  Le navigateur Microsoft Edge et le runtime WebView2 sont mis à jour à l’aide du même mécanisme de mise à jour.  S’il s’agit d’une stratégie telle qu' `Update` elle est spécifique au canal, elle s’applique à la fois au navigateur et au runtime WebView2.  Par exemple, `UpdateSuppressed` permet aux administrateurs informatiques de définir l’heure de chaque jour pour supprimer la mise à jour automatique pour le navigateur et WebView2 Runtime.  Cela permet aux administrateurs informatiques de configurer leurs préférences et leurs proxys une seule fois pour le navigateur et WebView2 Runtime pour contrôler la bande passante ou le trafic de votre réseau ou à d’autres fins.  Les administrateurs informatiques pourront suivre le [Guide de Microsoft Edge][ConfigureMicrosoftEdge] pour configurer les stratégies Microsoft Edge-Update.  
*   [Microsoft Edge-les stratégies de navigateur][EdgeBrowserPolicies] ne s’appliquent pas aux applications WebView2.  Ce type d’application est conçu pour les applications et les navigateurs, et les administrateurs informatiques ne connaissent peut-être pas les applications qui utilisent WebView2.  L’application de stratégies de navigateur sur WebView2 pourrait avoir des effets inattendus.  Par exemple, les administrateurs informatiques peuvent bloquer JavaScript dans le navigateur et toutes les applications WebView2 en JavaScript sont endommagées.  
*   \ (Bientôt disponible \) politiques spécifiques à WebView2-WebView2 exposera un petit ensemble supplémentaire de stratégies de groupe dans les cas où la gestion de WebView2 est judicieuse.  Nous recommandons aux développeurs d’applications d’implémenter leurs propres stratégies de groupe pour gérer leur utilisation de WebView2, car il est plus simple pour les administrateurs informatiques de gérer l’application plutôt que d’WebView2 directement.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Comprendre le runtime et le programme d’installation WebView2 (Preview)-distribution d’applications à l’aide de WebView2 | Documents Microsoft"  

[WebView2Landing]: ../index.md "Introduction à Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge-stratégies de mise à jour | Documents Microsoft"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge-stratégies de navigateur | Documents Microsoft"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurer les paramètres de stratégie Microsoft Edge sur Windows | Documents Microsoft"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
