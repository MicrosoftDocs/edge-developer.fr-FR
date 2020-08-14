---
description: Découvrez comment déboguer des contrôles WebView2.
title: Commencer le débogage des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: dcdeeadc2c25bcf50834176706b8d181f06f994a
ms.sourcegitcommit: 6c7ededf8677fd7add5e4060e92f9ec4cfdb6952
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2020
ms.locfileid: "10927901"
---
# Commencer le débogage des applications WebView2  

L’objectif du contrôle Microsoft Edge WebView2 est de combiner le meilleur des outils et des fonctionnalités de développement d’applications Web et natives.  Lorsque vous développez votre application WebView2, vous devez déboguer votre application.  Cet article présente les différents outils à utiliser pour déboguer votre code Web et votre code natif dans votre application WebView2.  

## [Outils Microsoft Edge Dev](#tab/devtools)  

Utilisez les [outils de développement Microsoft Edge (chrome)][DevtoolsGuideChromiumMain] pour déboguer le contenu Web affiché dans les contrôles WebView2, de la même façon que vous pouvez déboguer une autre page Web affichée dans Microsoft Edge.  Pour ouvrir le DevTools, positionnez le focus sur le contrôle WebView, puis utilisez l’une des actions suivantes.  

*   Sélectionnez `F12` .  
*   Sélectionnez `Ctrl` + `Shift` + `I` .  
*   Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) et sélectionnez `Inspect` .  

Pour plus d’informations, voir [vue d’ensemble de devtools][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="Débogage DevTools" lightbox="./media/f12.png":::
   Débogage DevTools  
:::image-end:::  

## [Visual Studio](#tab/visualstudio)  

Visual Studio fournit différents outils de débogage pour le Web et le code natif dans les applications WebView2.  Dans la section Visual Studio, le focus est essentiellement au débogage de contrôles WebView, mais les autres méthodes de débogage dans Visual Studio sont disponibles comme d’habitude.  Le processus suivant permet de déboguer du code Web et du code natif dans des applications Win32 ou des compléments Office uniquement.  

> [!IMPORTANT]
> Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.  Sélectionnez `Ctrl` + `Shift` + `I` ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter la situation.  

Avant de commencer, assurez-vous que les conditions suivantes sont remplies.  

*   Pour déboguer les scripts, l’application doit être lancée à partir de Visual Studio.  
*   Vous ne pouvez pas attacher de débogueur à un processus WebView2 en cours d’exécution.  
*   Installez Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure.  

Installez et configurez les outils de débogage de script dans Visual Studio.  

1.  Procédez comme suit pour installer le composant **Diagnostics JavaScript** dans le **développement de bureau avec C++**.  

    1. Dans la barre de l’Explorateur Windows, tapez `Visual Studio Installer` .  
    1. Sélectionnez **programme d’installation de Visual Studio** pour l’ouvrir.  
    1. Dans le programme d’installation de Visual Studio, sur la version installée, sélectionnez le bouton **plus** , puis sélectionnez **modifier**.  
    1. Dans Visual Studio, sous **charges de travail**, choisissez le paramètre **développement de bureau en C++** .  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Écran modification de la charge de travail dans Visual Studio" lightbox="./media/workloads.png":::
            Écran modification de la charge de travail dans Visual Studio :::image-end:::  
        
    1.  Choisissez **des composants individuels**.  
    1.  Dans la zone de recherche, entrez `JavaScript diagnostics` .  
    1.  Sélectionnez le paramètre **Diagnostics JavaScript** .  
    1.  Sélectionnez **modifier**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Onglet de modification de composants individuels dans Visual Studio" lightbox="./media/indivcomp.png":::
           Onglet de modification de composants individuels dans Visual Studio  
        :::image-end:::  
        
1.  Activez le débogage de script pour les applications WebView2.  
    1.  Dans votre projet WebView2, ouvrez le menu contextuel, puis cliquez sur **Propriétés**.  
    1.  Sous les **Propriétés de configuration**, sélectionnez **débogage**.  
    1.  Sous le **type de débogueur**, choisissez **JavaScript (WebView2)**.  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propriété de configuration du débogage de Visual Studio" lightbox="./media/enbjs.png":::
           Propriété de configuration du **débogage** de Visual Studio  
        :::image-end:::  
        
Effectuez les opérations suivantes pour déboguer votre application WebView2.  

1.  Pour définir un point d’arrêt dans votre code source, positionnez le curseur à gauche du numéro de ligne et choisissez de définir un point d’arrêt.  L’adaptateur de débogage JS/TS n’effectue pas le mappage de chemin d’accès source.  Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Ajouter un point d’arrêt dans Visual Studio" lightbox="./media/breakpoint.png"::: 
       Ajouter un point d’arrêt dans Visual Studio  
    :::image-end:::  
    
1.  Pour exécuter le débogueur, choisissez la taille en bits de la plateforme, puis sélectionnez le bouton de lecture de couleur verte en regard du **débogueur Windows local**.  L’application s’exécute et le débogueur se connecte au premier processus WebView2 créé.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Débogueur Windows de Visual Studio local" lightbox="./media/run.png"::: 
       **Débogueur Windows** de Visual Studio local  
    :::image-end:::  
    
1.  Dans la **console de débogage**, recherchez la sortie du débogueur.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Console de débogage de Visual Studio" lightbox="./media/console.png"::: 
       Console de **débogage** de Visual Studio  
    :::image-end:::  
    
* * *  

## Voir également  

*   Pour commencer à utiliser WebView2, voir [guides de mise en route de WebView2][Webview2MainGettingStarted].  
*   Pour obtenir un exemple complet de fonctionnalités WebView2, consultez la référentiel Samples [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.
*   Pour plus d’informations sur les API WebView2, voir informations de référence sur les [API][Webview2ApiReference].
*   Pour plus d’informations sur WebView2, voir [ressources WebView2][Webview2MainNextSteps].

## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome)"  

[Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions classe | Documents Microsoft"  
[Webview2ReferenceWin3209538Webview2IdlParameters]: ../reference/win32/0-9-538/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-global | Documents Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
