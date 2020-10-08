---
description: Découvrez comment lier de manière statique la bibliothèque de chargeur WebView2.
title: Liaison statique de la bibliothèque de chargeur WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: b7e0ec70cb00f318d4eb67254f37fcec79a5fcf6
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100302"
---
# Liaison statique de la bibliothèque de chargeur WebView2  

## Contexte  

Qu’est-ce que le WebView2Loader.dll?  

*   Le kit de développement logiciel (SDK) WebView2 contient un fichier d’en-tête, `WebView2Loader.dll.` et le `IDL` fichier. `WebView2Loader.dll` est un petit composant qui aide les applications à localiser le runtime WebView2 (ou canaux Microsoft Edge non stables) sur l’appareil.  

Pour les applications qui ont un seul Runtime et qui ne souhaitent pas expédier `WebView2Loader.dll` , procédez comme **Procedure** suit.  

## Procédure  

1.  Ouvrez le `.vcxproj` fichier de projet de votre application dans un éditeur de texte, tel que le code Visual Studio.  
    
    > [!NOTE]
    > `.vcproj`Il peut s’agir d’un fichier caché, ce qui signifie qu’il n’est pas affiché dans Visual Studio.  Pour rechercher un fichier masqué, utilisez la ligne de commande.  
    
1.  Recherchez la section dans le code où vous incluez les fichiers cibles de package NuGet WebView2.  L’emplacement dans le code est surligné dans l’illustration suivante.  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/inserthere.png"::: 
       Fragment de code de fichiers de projet  
    :::image-end:::  
    
1.  Copiez l’extrait de code suivant et collez-le partout où `Microsoft.Web.WebView2.targets` est inclus.  

    > [!NOTE]
    > Par exemple, incluez-le après le bloc de code suivant.  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/staticlib.png"::: 
       Extrait de code inséré  
    :::image-end:::  
    
1.  Modifiez les dépendances supplémentaires de la configuration de build de votre application.  Pour commencer, recherchez toutes les `<AdditionalDependencies>` balises.  
1.  Ajoutez `version.lib` comme dépendance supplémentaire à chaque configuration de build différente dans le `.vcxproj` fichier de votre application.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/versionlib.png"::: 
       Ajout `version.lib` à `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > L’équipe WebView2 vise à automatiser l’étape de dépendance supplémentaire dans les versions ultérieures.  
    
Compilez et déployez votre application.  Pris.  

## Voir également  

*   Pour commencer à utiliser WebView2, accédez à [WebView2 guides de mise en route][Webview2MainGettingStarted].  
*   Pour obtenir un exemple complet de fonctionnalités WebView2, accédez à [WebView2Samples][GithubMicrosoftedgeWebview2samples] dans github.
*   Pour plus d’informations sur les API WebView2, accédez à la [référence d’API][Webview2ApiReference].
*   Pour plus d’informations sur WebView2, accédez à [ressources WebView2][Webview2MainNextSteps].

## Contacter l’équipe WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions classe | Documents Microsoft"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-global | Documents Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
