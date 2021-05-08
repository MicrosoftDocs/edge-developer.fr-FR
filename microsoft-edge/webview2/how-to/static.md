---
description: Découvrez comment lier statiquement la bibliothèque de chargeurs WebView2.
title: Comment lier statiquement la bibliothèque de chargeurs WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 8f48a4fde9e2960de6156fc14db8c84f87a49868
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535887"
---
# <a name="statically-link-the-webview2-loader-library"></a>Lier statiquement la bibliothèque de chargeurs WebView2  

Vous pouvez distribuer votre application avec un seul fichier exécutable, au lieu d’un package de nombreux fichiers. Pour créer un fichier exécutable unique ou pour réduire la taille de votre package, vous devez lier statiquement les fichiers WebView2Loader. Le SDK WebView2 contient un fichier d’en-tête `WebView2Loader.dll` et le `IDL` fichier. `WebView2Loader.dll` est un petit composant qui permet aux applications de localiser le Runtime WebView2 ou les canaux non stables de Microsoft Edge sur l’appareil.  

Pour les applications qui ne souhaitent pas d’expédition, `WebView2Loader.dll` complétez les étapes suivantes.  

1.  Ouvrez le fichier de projet de votre application dans un éditeur de texte, tel `.vcxproj` que Visual Studio Code.  
    
    > [!NOTE]
    > Le fichier de projet peut être masqué, ce qui signifie qu’il `.vcproj` ne s’affiche pas Visual Studio.  Utilisez la ligne de commande pour rechercher les fichiers masqués.  
    
1.  Recherchez la section dans le code où vous incluez les fichiers cibles du package NuGet WebView2.  L’emplacement dans le code est mis en évidence dans la figure suivante.  
    
    :::image type="complex" source="./media/insert-here.png" alt-text="Extrait de code Project Files" lightbox="./media/insert-here.png":::
       Extrait de code Project Files   
    :::image-end:::  
    
1.  Copiez l’extrait de code suivant et collez-le là où `Microsoft.Web.WebView2.targets` il est inclus.  
    
    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```  
    
    :::image type="complex" source="./media/static-lib.png" alt-text="Extrait de code inséré" lightbox="./media/static-lib.png":::
       Extrait de code inséré  
    :::image-end:::  
    
1.  Modifiez les dépendances supplémentaires de la configuration de build pour votre application.  Pour commencer, recherchez toutes les `<AdditionalDependencies>` balises. Pour chacun d’eux, `version.lib` ajoutez en tant que dépendance supplémentaire à chaque configuration de build différente dans le `.vcxproj` fichier.  
    
    :::image type="complex" source="./media/version-lib.png" alt-text="Ajout de version.lib à ItemDefinitionGroups" lightbox="./media/version-lib.png":::
       Ajout `version.lib` à `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > L’équipe WebView2 a pour objectif d’automatiser l’ajout de dépendances supplémentaires dans les prochaines publication.  
    
1.  Compilez et exécutez votre application.  
    
## <a name="getting-in-touch-with-the-webview2-team"></a>Entrer en contact avec l’équipe WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

## <a name="see-also"></a>Voir également  

*   To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez [à WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.
*   Pour plus d’informations sur les API WebView2, accédez à la référence [d’API.][Webview2ApiReference]
*   Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2MainNextSteps]
    
<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Référence de l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2MainGetStarted]: ../index.md#get-started "Get started - Introduction to Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Nouveautés - Déboguer JavaScript pour Visual Studio Code - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (Chromium) - Visual Studio Code - Déboguer pour Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
