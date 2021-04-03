---
description: Navigation
title: Navigation | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: e87994d6205f81e01385a131e17091d0c8b001d5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470843"
---
# <a name="navigation-events"></a>Événements de navigation  

:::row:::
   :::column span="1":::
      Plateformes pris en charge :
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

Les événements de navigation s’exécutent lorsque des actions asynchrones spécifiques se produisent sur le contenu affiché dans une instance WebView2.  Par exemple, lorsqu’un utilisateur WebView2 navigue vers un nouveau site web, le contenu natif écoute la modification à l’aide de `NavigationStarting` l’événement.  Une fois l’action de navigation terminée, `NavigationCompleted` s’exécute.  Pour obtenir un bon exemple d’événements de navigation, accédez au guide de [mise en place de WebView2.][Webview2IndexGettingStarted]  

<!--todo:  Move the relevant information out of the getting started guide to better focus the content and leave the most concise elements in the getting started guide.  -->   

La séquence normale d’événements de navigation `NavigationStarting` est , , et puis `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .  Les événements suivants décrivent l’état de WebView2 pendant chaque navigation.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Événements de navigation Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
         Événements de navigation Microsoft Edge WebView2  
      :::image-end:::  
      
      > [!NOTE]
      > La figure représente les événements de navigation avec la même `NavigationId` propriété sur l’argument d’événement respectif.  
   :::column-end:::
   :::column span="2":::
      | Séquence | Nom de l’événement | Détails |  
      |:--- |:--- |:--- |  
      | 1 | `NavigationStarting`  |  WebView2 commence à naviguer et la navigation entraîne une demande réseau.  L’hôte peut désapprouver la demande pendant l’événement.  |  
      | 2 | `SourceChanged`  |  La source de WebView2 se transforme en une nouvelle URL.  L’événement peut être le résultat d’une action de navigation qui ne provoque pas de demande réseau telle qu’une navigation par fragment.  |  
      | 3 | `ContentLoading`  |  WebView commence à charger le contenu de la nouvelle page.  |  
      | 4 | `HistoryChanged`  |  La navigation entraîne la mise à jour de l’historique de WebView2.  |  
      | 5 | `NavigationCompleted`  |  WebView2 termine le chargement du contenu sur la nouvelle page.  |  
   :::column-end:::
:::row-end:::

Suivre les événements de navigation vers chaque nouveau document à l’aide de l’ID de navigation \( `NavigationId` événement\).  `NavigationId`L’événement WebView change chaque fois qu’une navigation réussie vers un nouveau document se termine.  

 Les événements de navigation avec différentes instances `NavigationId` d’événement peuvent se chevaucher.  Par exemple, lorsque vous démarrez un événement de navigation, vous devez attendre l’événement `NavigationStarting` associé.  Si vous démarrez ensuite une autre navigation, vous devez voir l’événement pour la première navigation suivi de l’événement pour le second, suivi de l’événement pour la première navigation, puis de tous les autres événements de navigation appropriés pour la `NavigationStarting` `NavigationStarting` deuxième `NavigationCompleted` navigation.  
 
 Dans les cas d’erreur, il peut y avoir ou non un événement selon que la navigation est continue `ContentLoading` à une page d’erreur.  
 
 Si une redirection HTTP se produit, il existe plusieurs événements dans une ligne, où les arguments d’événement ultérieurs ont la propriété définie, mais l’événement `NavigationStarting` `IsRedirect` reste le `NavigationId` même.  
 
 Les mêmes événements de navigation de document, tels que la navigation vers un fragment, n’entraînent pas l’événement et `NavigationStarting` n’incrémentent `NavigationId` pas l’événement.  

Pour surveiller ou annuler des événements de navigation à l’intérieur de sous-images dans une instance WebView2, utilisez les événements qui agissent comme les événements équivalents `FrameNavigationStarting` `FrameNavigationCompleted` sans trame.  

## <a name="see-also"></a>Voir également  

*   Pour commencer à utiliser WebView2, accédez aux guides de mise en page [WebView2.][Webview2IndexGettingStarted]  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au référentiel [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.  
*   Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]  
*   Pour plus d’informations sur WebView2, accédez à [Ressources WebView2.][Webview2IndexNextSteps]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Getting started - Introduction to Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
