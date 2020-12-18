---
description: Découvrez comment lier de manière statique la bibliothèque de chargeur WebView2.
title: Liaison statique de la bibliothèque de chargeur WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230928"
---
# Liaison statique de la bibliothèque de chargeur WebView2  

Vous pouvez distribuer votre application à l’aide d’un seul fichier exécutable au lieu d’un package de nombreux fichiers. Pour créer un fichier exécutable unique ou pour réduire la taille de votre package, vous devez lier de manière statique les fichiers WebView2Loader. Le kit de développement logiciel (SDK) WebView2 contient un fichier d’en-tête, `WebView2Loader.dll` et le `IDL` fichier. `WebView2Loader.dll` est un petit composant qui aide les applications à localiser le runtime WebView2 ou les canaux non stables de Microsoft Edge sur l’appareil.  

Pour les applications qui ne souhaitent pas expédier `WebView2Loader.dll` , procédez comme suit.  

1.  Ouvrez le `.vcxproj` fichier de projet de votre application dans un éditeur de texte, tel que le code Visual Studio.  
    
    > [!NOTE]
    > `.vcproj`Il peut s’agir d’un fichier caché, ce qui signifie qu’il n’est pas affiché dans Visual Studio.  Utilisez la ligne de commande pour rechercher des fichiers cachés.  
    
1.  Recherchez la section dans le code où vous incluez les fichiers cibles de package NuGet WebView2.  L’emplacement dans le code est surligné dans l’illustration suivante.  

    :::image type="complex" source="./media/inserthere.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/inserthere.png":::
       Fragment de code de fichiers de projet   
    :::image-end:::  
  
1.  Copiez l’extrait de code suivant et collez-le là où il `Microsoft.Web.WebView2.targets` est inclus.  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Extrait de code inséré" lightbox="./media/staticlib.png":::
       Extrait de code inséré  
    :::image-end:::  
    
1.  Modifiez les dépendances supplémentaires de la configuration de build de votre application.  Pour commencer, recherchez toutes les `<AdditionalDependencies>` balises. Pour chacun d’entre eux, ajoutez `version.lib` en tant que dépendance supplémentaire à chaque nouvelle configuration de build du `.vcxproj` fichier.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Ajouter version. lib à ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       Ajout `version.lib` à `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > L’équipe WebView2 vise à automatiser l’ajout de la dépendance supplémentaire dans les versions ultérieures.  
    
1. Compilez et exécutez l’application.

### Contacter l’équipe WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### Voir également  

*   Pour commencer à utiliser WebView2, accédez à [WebView2 guides de mise en route][Webview2MainGettingStarted].  
*   Pour obtenir un exemple complet de fonctionnalités WebView2, accédez à [WebView2Samples][GithubMicrosoftedgeWebview2samples] dans github.
*   Pour plus d’informations sur les API WebView2, accédez à la [référence d’API][Webview2ApiReference].
*   Pour plus d’informations sur WebView2, accédez à [ressources WebView2][Webview2MainNextSteps].

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
