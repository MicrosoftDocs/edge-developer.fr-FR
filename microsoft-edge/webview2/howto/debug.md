---
description: Découvrez comment déboguer des contrôles WebView2.
title: Commencer à déboguer des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: f895634d5e005bb07579d9a5f41c6a988cd78a33
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536464"
---
# <a name="get-started-debugging-webview2-apps"></a>Commencer à déboguer des applications WebView2  

L’objectif du Microsoft Edge WebView2 est de combiner le meilleur des fonctionnalités et outils de développement d’applications web et natives.  Lorsque vous développez votre application WebView2, vous devez la déboguer.  Cet article décrit les différents outils à utiliser pour déboguer votre code web et le code natif dans votre application WebView2.  

## [<a name="microsoft-edge-devtools"></a>Outils Microsoft Edge Dev](#tab/devtools)  

Utilisez les outils de développement [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] pour déboguer le contenu web affiché dans les contrôles WebView2, de la même façon que vous pouvez déboguer pour une autre page web affichée dans Microsoft Edge.  Pour ouvrir DevTools, définissez le focus sur le contrôle WebView, puis utilisez l’une des actions suivantes.  

*   Sélectionnez `F12` .  
*   Sélectionnez `Ctrl` + `Shift` + `I` .  
*   Ouvrez le menu contexto \(clic droit\) et choisissez `Inspect` .  
    
Pour plus d’informations, accédez à la vue [d’ensemble de DevTools.][DevtoolsGuideChromiumMain]  

:::image type="complex" source="./media/f12.png" alt-text="Débogage DevTools" lightbox="./media/f12.png":::
   Débogage DevTools  
:::image-end:::  

## [<a name="visual-studio"></a>Visual Studio](#tab/visualstudio)  

Visual Studio fournit différents outils de débogage pour le code web et natif dans les applications WebView2.  Dans la section Visual Studio, le principal objectif est le débogage des contrôles WebView, mais les autres méthodes de débogage dans Visual Studio sont disponibles comme d’habitude.  Utilisez le processus suivant pour déboguer le code web et le code natif dans les applications Win32 ou Office des applications uniquement.  

> [!IMPORTANT]
> Lorsque vous déboguer votre application dans Visual Studio avec le déboguer natif attaché, la sélection peut déclencher le déboguer natif au lieu des outils `F12` de développement.  Sélectionnez `Ctrl` + `Shift` + `I` ou utilisez le menu contexto \(clic droit\) pour éviter la situation.  

Avant de commencer, assurez-vous que les conditions suivantes sont remplies.  

*   Pour déboguer des scripts, l’application doit être lancée à partir de Visual Studio.  
*   Vous ne pouvez pas attacher un débompeur à un processus WebView2 en cours d’exécution.  
*   Installez Visual Studio version 2019 16.4 Preview 2 ou ultérieure.  
    
Installez et installez les outils de débogger de script dans Visual Studio.  

1.  Effectuer les actions suivantes pour installer le **composant de diagnostics JavaScript** dans le développement **de bureau avec C++**.  
    
    1.  Dans la Windows explorer, tapez `Visual Studio Installer` .  
    1.  Choisissez **Visual Studio Installer** pour l’ouvrir.  
    1.  Dans la Visual Studio Installer, sur la version installée, choisissez le bouton **Plus,** puis choisissez **Modifier**.  
    1.  Dans Visual Studio, sous **Charges de**travail, choisissez le paramètre **Développement de bureau en C++.**  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Écran Modification des charges de travail" lightbox="./media/workloads.png":::
            Visual Studio Écran Modification des charges de travail
        :::image-end:::  
        
    1.  Choisissez **des composants individuels.**  
    1.  Dans la zone de recherche, entrez `JavaScript diagnostics` .  
    1.  Choisissez le **paramètre de diagnostic JavaScript.**  
    1.  Choose **Modify**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio Modification de l’onglet Composants individuels" lightbox="./media/indivcomp.png":::
           Visual Studio Modification de l’onglet Composants individuels  
        :::image-end:::  
        
1.  Activez le débogage de script pour les applications WebView2.  
    1.  Dans votre projet WebView2, ouvrez le menu contexto \(clic droit\), puis choisissez **Propriétés.**  
    1.  Sous les **propriétés de configuration,** choisissez **Débogage.**  
    1.  Sous le **type de débogger,** choisissez **JavaScript (WebView2).**  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio Debugging Configuration, propriété" lightbox="./media/enbjs.png":::
           Visual Studio configuration **du débogage**  
        :::image-end:::  
        
Effectuer les actions suivantes pour déboguer votre application WebView2.  

1.  Pour définir un point d’arrêt dans votre code source, pointez sur la gauche du numéro de ligne et choisissez de définir un point d’arrêt.  L’adaptateur de débogage JS/TS n’effectue pas de mappage de chemin d’accès source.  Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio ajouter un point d’arrêt" lightbox="./media/breakpoint.png"::: 
       Visual Studio ajouter un point d’arrêt  
    :::image-end:::  
    
1.  Pour exécuter le débooeur, choisissez la taille de bits de la plateforme, puis choisissez le bouton de lecture vert en Windows **débogger**.  L’application s’exécute et le débogger se connecte au premier processus WebView2 créé.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio Débo Windows local" lightbox="./media/run.png"::: 
       Visual Studio Local **Windows Debugger**  
    :::image-end:::  
    
1.  Dans la **console de débogage,** recherchez la sortie du déboguer.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio Console de débogage" lightbox="./media/console.png"::: 
       Visual Studio console **de débogage**  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a>Visual Studio Code](#tab/visualstudiocode)  

Utilisez Microsoft Visual Studio code pour déboguer les scripts qui s’exécutent dans les contrôles WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

Dans Visual Studio Code, effectuer les actions suivantes pour déboguer votre code. 

1.  Votre projet doit avoir un `launch.json` fichier.  Si votre projet ne comprend pas de fichier, copiez l’extrait de code suivant `launch.json` et créez un `launch.json` fichier.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > Visual Studio Code mappage de chemin d’accès source nécessite désormais l’URL, votre application reçoit maintenant un paramètre de ligne de commande au démarrage.  Vous pouvez ignorer le paramètre en toute sécurité `url` si nécessaire.  
    
1.  Pour définir un point d’arrêt dans votre code source, pointez sur la ligne, puis sélectionnez `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Le point d’arrêt est Visual Studio Code" lightbox="./media/breakpointvs.png":::
       Le point d’arrêt est Visual Studio Code  
    :::image-end:::
    
1.  Exécutez le code.  
    1.  Sous **l’onglet** Exécuter, choisissez la configuration de lancement dans le menu déroulant.  
    1.  Pour commencer à déboguer votre application, sélectionnez Démarrer le débogage, qui est le triangle vert à côté de la zone de configuration de lancement.  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio Code Exécuter l’onglet" lightbox="./media/runvs.png":::
           Visual Studio Code Exécuter l’onglet  
        :::image-end:::  
        
1.  Ouvrez **la Console de débogage** pour afficher la sortie et les erreurs de débogage.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio Code Console de débogage" lightbox="./media/resultsvs.png":::
       Visual Studio Code Console de débogage  
    :::image-end:::  
    
**Advanced Paramètres**:  

*   Débogage Webview ciblé. 
    
    Dans certaines applications WebView2, vous pouvez utiliser plusieurs contrôles WebView2. Pour sélectionner le contrôle WebView2 à déboguer dans ce cas, vous pouvez utiliser le débogage webview2 ciblé 
    
    Ouvrez `launch.json` et terminez les actions suivantes pour utiliser le débogage Webview ciblé.  
    
    1.  Confirmez que `useWebview` le paramètre est paramétrable sur `true` .  
    1.  Ajoutez le `urlFilter` paramètre.  Lorsque le contrôle WebView2 navigue vers une URL, la valeur du paramètre est utilisée pour comparer les chaînes qui apparaissent `urlFilter` dans l’URL.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Lors du débogage de votre application, vous devrez peut-être passer du code au début du processus de rendu. Si vous rendez des pages web sur des sites et que vous n’avez pas accès au code source, vous pouvez utiliser cette option, car les pages web ignorent les `?=value`  paramètres non reconnus.   
    
    > [!IMPORTANT]
    > Une fois la première correspondance trouvée dans l’URL, le débogger s’arrête.  Vous ne pouvez pas déboguer deux contrôles WebView2 en même temps, car le port CDP est partagé par tous les contrôles WebView2 et utilise un numéro de port unique.  
    
*   Débogage des processus en cours d’exécution  
    
    Vous devrez peut-être attacher le débogger aux processus WebView2 en cours d’exécution. Pour ce faire, dans `launch.json` , mettez à jour le paramètre sur `request` `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    Votre contrôle WebView2 doit ouvrir le port CDP pour autoriser le débogage du contrôle WebView2.  Votre code doit être créé pour vous assurer qu’un seul contrôle WebView2 dispose d’un port CDP (Chrome Developer Protocol) ouvert, avant de démarrer le débogger.  
    
*   Options de suivi du débogage  
    
    Ajoutez `trace` le paramètre à launch.jsactivé pour activer le suivi du débogage.  
    
    1.  Ajouter un `trace` paramètre.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
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
                 Visual Studio Code Sortie de débogage avec suivi détaillée désactivé  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Déboguer Office des modules.  
    
    Si vous déboguer des Office, ouvrez le code source du Visual Studio Code.  Ouvrez launch.jsdans votre application WebView2 et ajoutez l’extrait de code suivant pour attacher le débogger au Office de messagerie.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Résolution des problèmes du débogger  
    
    Vous pouvez rencontrer les scénarios suivants lors de l’utilisation du débogger.  
    
    *   Le déboguer ne s’arrête pas au point d’arrêt et vous avez une sortie de débogage.  Pour résoudre le problème, confirmez que le fichier avec le point d’arrêt est le même fichier que celui utilisé par le contrôle WebView2.  Le débogger n’effectue pas de mappage de chemin d’accès source.  
    *   Vous ne pouvez pas vous attacher à un processus en cours d’exécution et vous obtenez une erreur de délai d’accès.  Pour résoudre le problème, confirmez que le contrôle WebView2 a ouvert le port CDP.   `additionalBrowserArguments` Assurez-vous que votre valeur dans le Registre est correcte ou que les options sont correctes.  Pour plus d’informations, accédez à [additionalBrowserArguments pour dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] et [additionalBrowserArguments pour Win32][Webview2ReferenceWin32Webview2IdlParameters].  
    
* * *  

## <a name="see-also"></a>Articles associés  

*   To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au repo [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.
*   Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][Webview2ApiReference]
*   Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2MainNextSteps]
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriété CoreWebView2EnvironmentOptions.AdditionalBrowserArguments (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment - Globals | Documents Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Référence de l’API WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en place : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
