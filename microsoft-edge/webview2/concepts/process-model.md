---
description: Modèle de processus
title: Modèle de processus | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 95d0c53219114c47a781317ab4b2ee2028fc586f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535614"
---
# <a name="process-model"></a>Modèle de processus  

:::row:::
   :::column span="1":::
      Plateformes pris en charge :
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

WebView2 utilise le même modèle de processus que le Microsoft Edge navigateur.  Pour plus d’informations sur le modèle de processus de navigateur, accédez à Architecture du navigateur - À l’intérieur, regardez [le navigateur web moderne.][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]  

Un processus de navigateur est associé aux processus de rendu et à d’autres processus utilitaires, comme décrit dans cet article.  En outre, si WebView2 est spécifié, l’application hôte demandant des processus utilise WebView2.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processus 1" lightbox="../media/process-model-1.png":::
   Processus 1  
:::image-end:::    

Un processus de navigateur est associé à un seul dossier de données utilisateur.  Un processus de demande peut spécifier plusieurs dossiers de données utilisateur.  Un processus de demande qui spécifie plusieurs dossiers de données utilisateur est associé au même nombre de processus de navigateur.  
Par exemple, un processus de demande qui demande l’accès à deux dossiers de données utilisateur utilise deux processus de navigateur.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processus 2" lightbox="../media/process-model-2.png":::
   Processus 2  
:::image-end:::    

Un processus de navigateur est associé à plusieurs processus de rendu.  Une instance WebView 2 crée un processus de navigateur pour traiter les images.  Un processus de navigateur peut être associé à plusieurs images.  Un processus de navigateur peut être associé à différentes instances de WebView2.  Le nombre de processus de rendu varie en fonction des conditions suivantes.  

*   Utilisation de la fonctionnalité d’isolation de site web dans votre navigateur.  
*   Nombre d’origines déconnectées distinctes rendues dans les instances associées de WebView2.  
    
La fonctionnalité de navigateur d’isolation de site web est décrite dans le contenu précédent. 
<!--todo:  which previous content?  -->  

Représente `CoreWebView2Environment` un dossier de données utilisateur et un processus de navigateur.  Le processus ne correspond pas directement à un ensemble de processus, car différents processus de rendu sont utilisés par un contrôle WebView2 en fonction de l’isolation du site web, comme décrit `CoreWebView2` précédemment.  

Pour réagir aux incidents et se bloque dans le navigateur et les processus de rendu, utilisez `ProcessFailed` l’événement de `CoreWebView2` .  

Pour arrêter en toute sécurité les processus de navigateur et de rendu associés, utilisez `Close` la méthode de `CoreWebView2Controller` .  

Pour ouvrir la fenêtre Gestionnaire des tâches du navigateur à partir **de la fenêtre DevTools** d’une instance WebView2, terminez l’opération sur les actions suivantes.  

*   Sélectionnez `Shift` + `Escape` .  
*   Pointez sur la barre de titre de la fenêtre DevTools, ouvrez le menu contextuel \(clic droit\), puis choisissez `Browser task manager` .  
    
Tous les processus associés au processus de navigateur de votre WebView2 sont affichés, y compris les objectifs associés.  

## <a name="see-also"></a>Articles associés  

*   Pour Prise en main webview2, accédez aux guides de Prise en main [WebView2.][Webview2IndexGetStarted]  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au [repo WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.  
*   Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]  
*   Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2IndexNextSteps]  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Get started - Introduction to Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation Microsoft Edge WebView2 | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Architecture du navigateur : examiner le navigateur web moderne (partie 1)"  
