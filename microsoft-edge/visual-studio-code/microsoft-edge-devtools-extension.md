---
description: Utiliser des éléments pour Microsoft Edge (chrome) à partir de code Visual Studio
title: Éléments de Microsoft Edge (chrome) issus du code Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, éléments
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135484"
---
# Extension de code Microsoft Edge DevTools pour Visual Studio  

Utiliser <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->pour accéder à cette extension dans Microsoft Edge DevTools dans le [code Visual Studio][VisualstudioCode].  Vous avez accès aux **éléments** et aux outils **réseau** dans Microsoft Edge devtools.  Vous pouvez lancer une instance de Microsoft Edge ou l’attacher à celle-ci.  Après vous être connecté, vous pouvez afficher la structure HTML d’exécution, modifier la disposition, résoudre les problèmes de style et inspecter le trafic réseau.  

## Outil éléments  

Par défaut, l’extension lance une instance de navigateur dans une fenêtre unique et vous donne les fonctionnalités d' **éléments** de Microsoft Edge devtools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools pour le code Visual Studio exécuté avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools pour le code Visual Studio exécuté avec une fenêtre de navigateur complète  
:::image-end:::  

Dans les paramètres de l’extension, vous pouvez activer davantage de fonctionnalités telles que le **mode** sans affichage et le **réseau**.  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Microsoft Edge DevTools pour le code Visual Studio exécuté avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Activation du mode sans affichage et de l’inspection du réseau dans les paramètres d’extension  
:::image-end:::  

## Mode headless  

En mode Headless, cette extension ne lance pas une instance de navigateur complète à déboguer.  Il exécute une instance en arrière-plan.  Il est possible que vous deviez rester à l’intérieur de l’éditeur et interagir avec le navigateur intégré.  Une icône de navigateur supplémentaire ne s’affiche pas dans la barre des tâches.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools pour le code Visual Studio exécuté avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools pour le code Visual Studio exécuté à l’aide d’un navigateur headless  
:::image-end:::  

> [!NOTE]
> Sur macOS, vous devez activer le mode headless comme mode préféré.  L’utilisation du mode headless doit résoudre un problème à l’endroit où, si la fenêtre n’est pas visible, la fenêtre du navigateur indique son état `Not Active` .  

## Outil réseau  

Si vous voulez également examiner le trafic réseau de votre application, vous pouvez ouvrir les paramètres et activer l’onglet **réseau** .  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Microsoft Edge DevTools pour le code Visual Studio exécuté avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Inspection du réseau dans Microsoft Edge DevTools pour le code Visual Studio  
:::image-end:::  

## Lancement de Microsoft Edge à partir de l’extension  

Accédez à outils Microsoft Edge dans la **barre d’activité**.  À côté de l’emplacement du message « **outils Microsoft Edge: cibles»,** il existe un signe plus qui ouvre le navigateur de votre application.  Si vous choisissez l’option **à propos** de, vous devez accéder à votre application Web dans le navigateur pour qu’elle apparaisse dans le panneau **éléments** du code Visual Studio.  

## Lancement de Microsoft Edge à partir de la vue de débogage  

Si vous avez l’habitude d’utiliser le mode débogage dans le code Visual Studio, accédez à DevTools Microsoft Edge.  

1.  Dans le code Visual Studio, accédez à la vue de débogage. 
    *   Sélectionnez `Ctrl` + `Shift` + `D` Windows/Linux \ ( `Command` + `Shift` + `D` sur MacOS \).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Si vous n’avez pas de configurations dans le code Visual Studio, effectuez l’une des actions suivantes.  
>     *   Sélectionnez `F5` .  
>     *   Cliquez sur le bouton **lire** \ (Green \).  
> 1.  Dans la liste déroulante, sélectionnez **Edge** dans la liste déroulante.  
> 1.  Un `launch.json` fichier doit être affiché pour contenir la configuration suivante.  
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
> Une fois la configuration correcte chargée, effectuez l’opération suivante.  

1.  Pour lancer l’outil **éléments** à partir du code Visual Studio, effectuez l’une des actions suivantes. 
    *   Sélectionnez `F5` .  
    *   Cliquez sur le bouton **lire** \ (Green \).  
         
À présent, vous pouvez effectuer les actions suivantes.  

*   Accédez à la vidéo de votre navigateur.  
*   Inspectez le DOM et le style des composants de votre page.  

## Joindre à Microsoft Edge  

Pour ouvrir un navigateur et joindre l’instance au code Visual Studio, procédez comme suit. 

1.  Pour ouvrir une instance de Microsoft Edge \ (chrome \), copiez et exécutez la commande suivante.  
    
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
    
1.  Dans le code Visual Studio, ouvrez le menu déroulant **débogueur** et sélectionnez **joindre à Microsoft Edge, puis ouvrez les outils de développement**.  
1.  Pour lancer l’outil **éléments** à partir du code Visual Studio, effectuez l’une des actions suivantes. 
    *   Sélectionnez `F5` .  
    *   Cliquez sur le bouton **lire** \ (Green \).  
         
À présent, vous pouvez effectuer les actions suivantes.  

*   Accédez à la vidéo de votre navigateur.  
*   Inspectez le DOM et le style des composants de votre page.  
    
## Contacter l’équipe de l’extension de code Microsoft Edge DevTools pour Visual Studio  

Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.  

Si vous voulez apporter des informations <!--the Microsoft Edge DevTools for Visual Studio Code -->C’est encore plus de plus de plaisirs.  Trouvez tout ce dont vous avez besoin pour commencer à utiliser le [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nouveau problème-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour le code VS"  
