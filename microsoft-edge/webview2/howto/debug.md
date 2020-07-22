---
description: Découvrez comment déboguer des contrôles WebView2.
title: Débogage de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888580"
---
# Comment déboguer avec WebView2  

L’objectif du contrôle Microsoft Edge WebView2 combine les fonctionnalités de développement d’applications et les outils de développement d’applications Web et natives.  La page suivante décrit les différents outils à utiliser pour le développement de contrôles WebView2.  

## Outils Microsoft Edge Dev  

Utilisez les [outils de développement Microsoft Edge (chrome)][DevtoolsMain] pour déboguer le contenu Web affiché dans les contrôles WebView2, de la même façon que si vous utilisiez Microsoft Edge.  Pour ouvrir le DevTools, positionnez le focus sur la fenêtre WebView, puis utilisez l’une des actions suivantes.  

*   Sélectionnez `F12` .  
*   Sélectionnez `Ctrl` + `Shift` + `I` .  
*   Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) et sélectionnez `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Outils Microsoft Edge Dev" lightbox="../media/f12.png":::
   Outils Microsoft Edge Dev  
:::image-end:::  

> [!IMPORTANT]
> Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.  Utilisez `Ctrl` + `Shift` + `I` , ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter cette situation.  

## Visual Studio  

Vous pouvez utiliser Visual Studio pour développer le code de l’application et déboguer les scripts en même temps.  

Gardez les points suivants à l’esprit.  

*   Visual Studio ne prend en charge que les scripts de débogage lors du lancement de l’application à partir de Visual Studio.  \ (L’attachement d’un processus actif pour le débogage n’est pas pris en charge. \)  
*   Le scénario de débogage WebView ciblé n’est pas pris en charge.  

Utilisez le débogueur de script dans Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure pour déboguer votre script dans Visual Studio.  

Configurez le débogueur.  

*   Vérifiez que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.  
    
    1.  Accédez à **applications &** paramètres de fonctionnalités dans Windows.  Recherchez-le à l’aide de la barre des tâches Windows.  
    1.  Sélectionnez **modifier**.  
    1.  Vérifiez que les cases à cocher **Diagnostics JavaScript** et **développement de bureau dans C++** sont activées.  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Applications et fonctionnalités" lightbox="../media/appsandfeatures.png":::
           Applications et fonctionnalités  
        :::image-end:::  
        
*   Activez le débogage de script WebView2.  
    1.  Placez le pointeur de la souris sur votre projet, ouvrez le menu contextuel, puis cliquez sur **Propriétés**.  
    1.  Dans **Propriétés de configuration**, sélectionnez **débogage**.  
    1.  Dans la propriété **type de débogueur** , recherchez la liste des options dans la liste, puis sélectionnez **JavaScript (WebView2)**.  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Débogueur JavaScript Visual Studio" lightbox="../media/enbjs.png":::
           Débogueur JavaScript Visual Studio  
        :::image-end:::  
        
<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Vous êtes prêt à procéder au débogage.  

Pour déboguer, procédez comme suit.  

1.  Définir des points d’arrêt  
    *   Ouvrez le fichier de script et définissez le point d’arrêt à l’emplacement souhaité.  
        
        > [!NOTE]
        > L’adaptateur de débogage JS/TS n’effectue pas le mappage de chemin d’accès source.Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.  
        
1.  Exécuter du code  
    *   Sélectionnez votre arôme de build et votre environnement d’exécution appropriés, puis démarrez le débogueur Windows local.  
1.  Afficher la console de débogage  
    *   Votre application s’exécute et le débogueur se connecte après la création du premier webview2.Toute sortie de débogage en attente est affichée.  
        
        > [!NOTE]
        > Cette méthode de débogage est actuellement limitée aux applications Win32 et aux compléments Office.  
        
## VisualStudioCode  

Vous pouvez utiliser du code Visual Studio pour déboguer des scripts qui s’exécutent dans des contrôles WebView2.  Pour plus d’informations, reportez-vous à la rubrique [applications WebView de Microsoft Edge (chrome)][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Contacter l’équipe WebView de Microsoft Edge  

Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires.  Visitez le site de [Commentaires référentiel Samples][GithubMicrosoftedgeWebviewfeedback] pour envoyer des demandes de fonctionnalité ou des rapports de bogues.  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (chrome) applications WebView-débogueur de code VS pour Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
