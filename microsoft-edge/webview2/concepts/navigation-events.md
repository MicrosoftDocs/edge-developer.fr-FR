---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314796"
---
# Événements de navigation  

La séquence normale d’événements de navigation `NavigationStarting` est , , et puis `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .  Les événements suivants décrivent l’état de WebView2 pendant chaque navigation.  

| Séquence | Nom de l’événement | Détails |  
|:--- |:--- |:--- |  
| 1 | `NavigationStarting`  |  WebView2 commence à naviguer et la navigation entraîne une demande réseau.  L’hôte est en mesure d’interdiquer la demande pendant l’événement.  |  
| 2 | `SourceChanged`  |  La source de WebView2 se transforme en une nouvelle URL.  L’événement peut être le résultat d’une navigation qui ne provoque pas de demande réseau telle qu’une navigation par fragment.  |  
| 3 | `HistoryChanged`  |  Historique des mises à jour WebView2 suite à la navigation.  |  
| 4 | `ContentLoading`  |  WebView2 démarre le chargement du contenu pour la nouvelle page.  |  
| 5 | `NavigationCompleted`  |  WebView2 termine le chargement du contenu sur la nouvelle page.  |  

Suivez `navigations` chaque nouveau document à l’aide de l’ID de navigation \( `NavigationId` \).  Le `NavigationId` webview change chaque fois qu’une navigation vers un nouveau document réussit.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Événements de navigation Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   Événements de navigation Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> La figure précédente représente les événements de navigation avec la même `NavigationId` propriété sur l’rg d’événement respectif.  

 `Navigations` les événements avec différentes instances `NavigationId` d’événement peuvent se chevaucher.  Par exemple, lorsque vous démarrez une navigation, vous devez attendre l’événement `NavigationStarting` associé.  Si vous démarrez ensuite une autre navigation, vous devez voir l’événement pour la première navigation suivi de l’événement pour le second, suivi de l’événement pour la première navigation, puis de tous les autres événements de navigation appropriés pour la `NavigationStarting` `NavigationStarting` deuxième `NavigationCompleted` navigation.  
 
 Dans les cas d’erreur, il peut y avoir ou non un événement en fonction de la poursuite de la `ContentLoading` navigation vers une page d’erreur.  
 
 Dans le cas d’une redirection HTTP, il existe plusieurs événements d’une ligne, où lesrgs d’événements suivants ont la propriété définie, mais les `NavigationStarting` `IsRedirect` `NavigationId` événements restent identiques.  
 
 Le même document, tel que la navigation vers un fragment, n’entraîne pas l’événement et `navigations` `NavigationStarting` n’incrémente pas le `NavigationId` .  

Pour surveiller ou annuler à l’intérieur de sous-images du WebView, utilisez les événements qui agissent comme les événements équivalents `navigations` `FrameNavigationStarting` sans `FrameNavigationCompleted` trame.  

<!-- links -->  
