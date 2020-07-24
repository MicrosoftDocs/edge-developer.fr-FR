---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895554"
---
# Événements de navigation  

L’ordre normal des événements de navigation est,,,, puis `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .  Les événements suivants décrivent l’état de WebView2 pendant chaque navigation.  

| Souche | Nom de l’événement | Détails |  
|:--- |:--- |:--- |  
| 1 | `NavigationStarting`  |  WebView2 commence à naviguer et aux résultats de navigation dans une requête réseau.  L’hôte est en mesure d’interdire la requête pendant l’événement.  |  
| deuxième | `SourceChanged`  |  La source de WebView2 passe à une nouvelle URL.  L’événement peut résulter d’une navigation qui n’entraîne pas de requête réseau telle qu’une navigation de type fragment.  |  
| 3D | `HistoryChanged`  |  L’historique des mises à jour de WebView2 est le résultat de la navigation.  |  
| n°4 | `ContentLoading`  |  WebView démarre le chargement du contenu de la nouvelle page.  |  
| n°5 | `NavigationCompleted`  |  WebView2 termine le chargement du contenu de la nouvelle page.  |  

Effectuer un suivi `navigations` vers chaque nouveau document à l’aide de l’ID de navigation \ ( `NavigationId` \).  Le `NavigationId` mode d’affichage du WebView change chaque fois qu’une navigation est réussie vers un nouveau document.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Événements de navigation Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   Événements de navigation Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> La figure précédente représente les événements de navigation ayant la même `NavigationId` propriété sur l’élément Arg correspondant.  

 `Navigations` les événements présentant différentes instances d' `NavigationId` événement risquent de se chevaucher.  Par exemple, lorsque vous démarrez une navigation, vous devez attendre l’événement associé `NavigationStarting` .  Si vous démarrez une autre navigation, vous devriez voir l' `NavigationStarting` événement pour la première navigation suivie de l' `NavigationStarting` événement pour la deuxième navigation, suivi de l' `NavigationCompleted` événement pour la première navigation, puis de tout le reste des événements de navigation appropriés pour la deuxième navigation.  
 
 Dans les cas d’erreur, il est possible qu’il n’y ait ou non un `ContentLoading` événement selon que la navigation se poursuit sur une page d’erreur.  
 
 Dans le cas d’une redirection HTTP, il existe plusieurs `NavigationStarting` événements dans une ligne, où les arguments d’événement suivants sont définis par la `IsRedirect` propriété, même si la propriété `NavigationId` reste la même.  
 
 Même document `navigations` , par exemple, la navigation jusqu’à un fragment, ne génèrent pas d' `NavigationStarting` événement et n’incrémentent pas le `NavigationId` .  

Pour surveiller ou annuler l' `navigations` intérieur de sous-trames dans le WebView, utilisez les `FrameNavigationStarting` événements et, `FrameNavigationCompleted` qui agissent de la même façon que les événements équivalents non liés aux images.  

<!-- links -->  
