---
description: Découvrez comment déboguer des contrôles WebView2.
title: Commencer le débogage des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 4f94fe880f66f8aeb387d2db4a8bfaab20699466
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230697"
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

Visual Studio fournit différents outils de débogage pour le Web et le code natif dans les applications WebView2.  Dans la section Visual Studio, le focus principal est le débogage de contrôles WebView, mais les autres méthodes de débogage dans Visual Studio sont disponibles comme d’habitude.  Le processus suivant permet de déboguer du code Web et du code natif dans des applications Win32 ou des compléments Office uniquement.  

> [!IMPORTANT]
> Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.  Sélectionnez `Ctrl` + `Shift` + `I` ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter la situation.  

Avant de commencer, assurez-vous que les conditions suivantes sont remplies.  

*   Pour déboguer les scripts, l’application doit être lancée à partir de Visual Studio.  
*   Vous ne pouvez pas attacher de débogueur à un processus WebView2 en cours d’exécution.  
*   Installez Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure.  
    
Installez et configurez les outils de débogage de script dans Visual Studio.  

1.  Procédez comme suit pour installer le composant **Diagnostics JavaScript** dans le **développement de bureau avec C++**.  
    
    1.  Dans la barre de l’Explorateur Windows, tapez `Visual Studio Installer` .  
    1.  Sélectionnez **programme d’installation de Visual Studio** pour l’ouvrir.  
    1.  Dans le programme d’installation de Visual Studio, sur la version installée, sélectionnez le bouton **plus** , puis sélectionnez **modifier**.  
    1.  Dans Visual Studio, sous **charges de travail**, choisissez le paramètre **développement de bureau en C++** .  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Écran modification de la charge de travail dans Visual Studio" lightbox="./media/workloads.png":::
            Écran modification de la charge de travail dans Visual Studio
        :::image-end:::  
        
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
    
## [VisualStudioCode](#tab/visualstudiocode)  

Utilisez le code Microsoft Visual Studio pour déboguer les scripts qui s’exécutent dans les contrôles WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

Dans le code Visual Studio, effectuez les actions suivantes pour déboguer votre code. 

1.  Un fichier est requis pour votre projet `launch.json` .  Si votre projet ne comporte pas de `launch.json` fichier, copiez l’extrait de code suivant et créez un `launch.json` fichier.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
    
1.  Pour définir un point d’arrêt dans votre code source, pointez sur la ligne, puis sélectionnez `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Le point d’arrêt est défini dans le code Visual Studio" lightbox="./media/breakpointvs.png":::
       Le point d’arrêt est défini dans le code Visual Studio  
    :::image-end:::
    
    > [!NOTE]
    > Dans la mesure où le code Visual Studio n’effectue pas le mappage source, assurez-vous de définir des points d’arrêt dans le même fichier que WebView2.  Dans le cas contraire, le code Visual Studio n’interrompt pas le code en cours d’exécution au point d’arrêt.  
    
1.  Exécutez le code.  
    1.  Dans l’onglet **exécuter** , choisissez la configuration de lancement dans le menu déroulant.  
    1.  Pour démarrer le débogage de votre application, sélectionnez Démarrer le débogage, qui est le triangle vert en regard de la liste déroulante de configuration de lancement.  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Onglet exécuter de code Visual Studio" lightbox="./media/runvs.png":::
           Onglet exécuter de code Visual Studio  
        :::image-end:::  
        
1.  Ouvrez la **console de débogage** pour afficher les erreurs et la sortie de débogage.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Console de débogage de code Visual Studio" lightbox="./media/resultsvs.png":::
       Console de débogage de code Visual Studio  
    :::image-end:::  
    
**Paramètres avancés**:  

*   Débogage WebView ciblé. 
    
    Dans certaines applications WebView2, vous pouvez utiliser plusieurs contrôles WebView2. Pour sélectionner le contrôle WebView2 à déboguer dans cette situation, vous pouvez utiliser le débogage de WebView2 ciblé 
    
    Ouvrez `launch.json` et effectuez les actions suivantes pour utiliser le débogage d’affichage WebView ciblé.  
    
    1.  Vérifiez que le `useWebview` paramètre est défini sur `true` .  
    1.  Ajoutez le `urlFilter` paramètre.  Lorsque le contrôle WebView2 navigue vers une URL, la `urlFilter` valeur de paramètre est utilisée pour comparer les chaînes qui s’affichent dans l’URL.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Lors du débogage de votre application, il est possible que vous deviez parcourir le code du début du processus de rendu. Si vous voulez afficher des pages Web sur des sites et que vous n’avez pas accès au code source, vous pouvez utiliser l' `?=value`  option, car les pages Web ignorent les paramètres non reconnus.   
    
    > [!IMPORTANT]
    > Une fois la première correspondance trouvée dans l’URL, le débogueur s’arrête.  Vous ne pouvez pas déboguer deux contrôles WebView2 en même temps, car le port CDP est partagé par tous les contrôles WebView2 et utilise un numéro de port unique.  
    
*   Déboguer des processus en cours d’exécution  
    
    Il est possible que vous deviez joindre le débogueur pour exécuter les processus WebView2. Pour ce faire, dans `launch.json` , mettez à jour le `request` paramètre en `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    Votre contrôle WebView2 doit ouvrir le port CDP pour permettre le débogage du contrôle WebView2.  Votre code doit être créé pour s’assurer qu’un seul contrôle WebView2 est ouvert par un port CDP (chrome Developer Protocol) avant de démarrer le débogueur.  
    
*   Options de suivi de débogage  
    
    Ajoutez le `trace` paramètre à launch.jsactivé pour activer le suivi de débogage.  
    
    1.  Ajouter un `trace` paramètre.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Enregistrez la sortie de débogage dans un fichier journal." lightbox="./media/tracelog.png":::
                 Enregistrer la sortie de débogage dans un fichier journal  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Sortie détaillée" lightbox="./media/verbose.png":::
                 Sortie du débogage de code Visual Studio avec l’affichage suivi détaillé activé  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Déboguer des compléments Office.
    
    Si vous déboguez des compléments Office, ouvrez le code source du complément dans une instance distincte du code Visual Studio.  Ouvrez launch.jsdans votre application WebView2, puis ajoutez l’extrait de code suivant pour joindre le débogueur au complément Office.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Résoudre les problèmes du débogueur  
    
    Vous pouvez rencontrer les situations suivantes lors de l’utilisation du débogueur.  
    
    *   Le débogueur ne s’arrête pas au point d’arrêt et vous avez une sortie de débogage.  Pour résoudre ce problème, vérifiez que le fichier contenant le point d’arrêt est le même que celui utilisé par le contrôle WebView2.  Le débogueur n’effectue pas le mappage de chemin d’accès source.  
    *   Vous ne pouvez pas attacher de processus en cours d’exécution et vous obtenez une erreur de temporisation.  Pour résoudre ce problème, vérifiez que le contrôle WebView2 a ouvert le port CDP.  Vérifiez que votre  `additionalBrowserArguments`  valeur dans le Registre est correcte ou que les options sont correctes.  Pour plus d’informations, consultez [additionalBrowserArguments pour dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] et [additionalBrowserArguments pour Win32][Webview2ReferenceWin32Webview2IdlParameters].  
    
* * *  

## Voir également  

*   Pour commencer à utiliser WebView2, voir [guides de mise en route de WebView2][Webview2MainGettingStarted].  
*   Pour obtenir un exemple complet de fonctionnalités WebView2, consultez la référentiel Samples [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.
*   Pour plus d’informations sur les API WebView2, voir informations de référence sur les [API][Webview2ApiReference].
*   Pour plus d’informations sur WebView2, voir [ressources WebView2][Webview2MainNextSteps].
    
## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriété CoreWebView2EnvironmentOptions. AdditionalBrowserArguments (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment-global | Documents Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
