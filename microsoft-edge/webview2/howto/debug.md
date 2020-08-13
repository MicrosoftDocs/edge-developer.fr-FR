---
description: Découvrez comment déboguer des contrôles WebView2.
title: Débogage de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 6b2cc65e5cb368c29efec2eb3638f0c1772000d9
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926476"
---
# Comment déboguer avec WebView2  

L’objectif du contrôle Microsoft Edge WebView2 combine les fonctionnalités de développement d’applications et les outils de développement d’applications Web et natives.  La page suivante décrit les différents outils à utiliser pour le développement de contrôles WebView2.  

## Outils Microsoft Edge Dev  

Utilisez les [outils de développement Microsoft Edge (chrome)][DevtoolsGuideChromiumMain] pour déboguer du contenu Web affiché dans les contrôles WebView2, de la même façon que Microsoft Edge.  Pour ouvrir le DevTools, positionnez le focus sur la fenêtre WebView, puis utilisez l’une des actions suivantes.  
*   Sélectionnez `F12` .  
*   Sélectionnez `Ctrl` + `Shift` + `I` .  
*   Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) > sélectionnez `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Outils Microsoft Edge Dev" lightbox="../media/f12.png":::
   Outils Microsoft Edge Dev  
:::image-end:::  

> [!NOTE]
> Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, le fait d’appuyer sur `F12` risque de déclencher le débogueur natif au lieu des outils de développement.  Appuyez sur `Ctrl` + `Shift` + `I` , ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter cette situation.  

> [!NOTE]
> Vous pouvez utiliser l' `--auto-open-devtools-for-tabs` argument de la ligne de commande pour ouvrir une nouvelle fenêtre devtools lorsque vous créez un WebView pour la première fois.  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## Visual Studio  

Utilisez le débogueur de script dans Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure pour déboguer votre script dans Visual Studio.  Vérifiez que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnostics JavaScript Visual Studio":::
   Diagnostics JavaScript Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Pour activer le débogage de script WebView2, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) dans votre projet > sélectionnez **Propriétés**.  

*   Dans **Propriétés de configuration**, sélectionnez **débogage**.  
*   Dans la propriété **type de débogueur** , sélectionnez **JavaScript (WebView2)** dans la liste des options. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Débogueur JavaScript Visual Studio":::
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

Vous pouvez utiliser du code Visual Studio pour déboguer des scripts qui s’exécutent dans des contrôles WebView2.  Pour plus d’informations, reportez-vous à la rubrique [applications WebView de Microsoft Edge (chrome)][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome) et débogueur de code et de code-débogueur pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
