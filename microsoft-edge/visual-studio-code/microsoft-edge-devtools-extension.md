---
description: Comment utiliser des éléments pour Microsoft Edge (Chromium) à partir de Visual Studio Code
title: Éléments pour Microsoft Edge (Chromium) de Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, vs code, visual studio code, éléments
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398454"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a>Microsoft Edge DevTools pour l’extension Visual Studio Code de recherche  

Utiliser <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->cette extension à accéder dans Microsoft Edge DevTools à [l’intérieur Microsoft Visual Studio Code][VisualstudioCode].  Vous avez accès aux outils **éléments** **et** réseau dans Microsoft Edge DevTools.  Vous pouvez lancer ou attacher une instance de Microsoft Edge.  Une fois connecté, vous pouvez afficher la structure HTML d’runtime, modifier la disposition, résoudre les problèmes de style et inspecter le trafic réseau.  

## <a name="elements-tool"></a>Outil Éléments  

Par défaut, l’extension lance une instance de navigateur dans une fenêtre unique et vous offre la fonctionnalité **Elements** de Microsoft Edge DevTools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools pour Visual Studio Code’exécution avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools pour Visual Studio Code’exécution avec une fenêtre de navigateur complète  
:::image-end:::  

Dans les paramètres d’extension, vous pouvez activer davantage de fonctionnalités telles que le **mode sans** tête et le **réseau.**  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Activation (ou désactivation) du mode sans tête et inspection du réseau dans les paramètres d’extension" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Activation du mode sans tête \(ou désactivation\) et inspection du réseau dans les paramètres d’extension  
:::image-end:::  

## <a name="headless-mode"></a>Mode sans tête  

En mode sans en-tête, cette extension ne lance pas une instance de navigateur complète pour le débogage.  Il exécute une instance en arrière-plan.  Vous de devez peut-être rester à l’intérieur de l’éditeur et interagir avec le navigateur incorporé.  Une icône de navigateur supplémentaire n’est pas affichée dans la barre des tâches.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools pour les Visual Studio Code’exécution sans en-tête" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools pour les Visual Studio Code’exécution avec un navigateur sans en-tête  
:::image-end:::  

> [!NOTE]
> Sur macOS, vous devez activer le mode sans tête comme mode préféré.  L’utilisation du mode sans en-tête doit résoudre un problème dans lequel, si la fenêtre n’est pas visible, la fenêtre du navigateur signale qu’elle `Not Active` l’est.  

## <a name="network-tool"></a>Outil réseau  

Si vous souhaitez également inspecter le trafic réseau de votre application, ouvrez les paramètres et allumez **l’onglet** Réseau.  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspection du réseau dans Microsoft Edge DevTools pour les Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Inspection du réseau dans Microsoft Edge DevTools pour les Visual Studio Code  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a>Lancement Microsoft Edge à partir de l’extension  

Accédez à Microsoft Edge outils dans la **barre d’activité.**  À côté de **l’Microsoft Edge Outils** : Cibles, il existe un signe plus qui ouvre le navigateur de votre application.  Si vous choisissez l’option **about:blank,** vous devez accéder à votre application web dans le navigateur pour qu’elle apparaisse dans le panneau **Éléments** dans Visual Studio Code.  

## <a name="launching-microsoft-edge-from-the-debug-view"></a>Lancement Microsoft Edge à partir de la vue Débogage  

Si vous avez l’habitude d’utiliser la vue Débogage dans Visual Studio Code, accédez à Microsoft Edge devTools à partir de celui-ci.  

1.  Dans Visual Studio Code, accédez à l’affichage Débogage 
    *   Sélectionnez `Ctrl` + `Shift` + `D` sur Windows/Linux \( `Command` + `Shift` + `D` sur macOS\).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Si vous n’avez aucune configuration dans Visual Studio Code, effectuer l’une des actions suivantes.  
>     *   Sélectionnez `F5` .  
>     *   Choisissez le **bouton Lire** \(vert\).  
> 1.  Dans ladown, choisissez **Edge** dans la dropdown.  
> 1.  Un fichier qui contient la configuration suivante doit `launch.json` être affiché.  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> Une fois que vous avez chargé la configuration correcte, terminez l’action suivante.  

1.  Pour lancer l’outil **Éléments** à Visual Studio Code, effectuer l’une des actions suivantes. 
    *   Sélectionnez `F5` .  
    *   Choisissez le **bouton Lire** \(vert\).  
         
Vous pouvez maintenant faire les actions suivantes.  

*   Accédez à une capture vidéo de votre navigateur.  
*   Inspectez le DOM et le style des composants sur votre page.  

## <a name="attaching-to-microsoft-edge"></a>Attachement à un Microsoft Edge  

Pour ouvrir un navigateur et attacher l’instance à Visual Studio Code, complétez les étapes suivantes. 

1.  Pour ouvrir une instance de Microsoft Edge \(Chromium\), copiez et exécutez la commande suivante.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  Après le lancement de l’instance, copiez et collez l’extrait de code suivant dans votre `launch.json` fichier.  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.  
1.  Pour lancer l’outil **Éléments** à Visual Studio Code, effectuer l’une des actions suivantes. 
    *   Sélectionnez `F5` .  
    *   Choisissez le **bouton Lire** \(vert\).  
         
Vous pouvez maintenant faire les actions suivantes.  

*   Accédez à une capture vidéo de votre navigateur.  
*   Inspectez le DOM et le style des composants sur votre page.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a>Contacter l’équipe Microsoft Edge devTools pour Visual Studio Code extension  

Envoyez vos commentaires en [classant un problème][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] par rapport [au GitHub de][GithubMicrosoftVscodeEdgeDevtools] l’extension.  

Si vous souhaitez vous aider à effectuer <!--the Microsoft Edge DevTools for Visual Studio Code -->Cette extension est préférable, vos contributions sont les bienvenues.  Recherchez tout ce dont vous avez besoin pour commencer [dans le GitHub de][GithubMicrosoftVscodeEdgeDevtools] l’extension.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nouveau problème : microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils pour Visual Studio Code"  
