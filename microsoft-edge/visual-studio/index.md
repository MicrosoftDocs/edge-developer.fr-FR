---
description: Microsoft Edge (Chromium) et Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, vs, visual studio, débogueur
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387273"
---
# <a name="visual-studio"></a>Visual Studio  

Microsoft [Visual Studio][MicrosoftVisualstudioVs] est un environnement de développement intégré \(IDE\).   Utilisez-le pour modifier, déboguer, créer et publier vos applications web.  Il s’agit d’un programme riche en fonctionnalités qui peut être utilisé pour de nombreux aspects de votre développement web.  Au-delà de l’éditeur et du débogger standard fournis par la plupart des ID, Visual Studio inclut les fonctionnalités suivantes pour faciliter votre processus de développement.  

*   compilateurs  
*   outils d’achèvement du code  
*   concepteurs graphiques  
*   beaucoup plus  
    
Si vous n’utilisez pas déjà Visual Studio, accédez à Télécharger [Visual Studio][MicrosoftVisualstudioDownloads] télécharger.  

Actuellement, Visual Studio 2019 prend en charge le débogage de JavaScript dans Microsoft Edge pour ASP.NET Framework et ASP.NET Core applications.  Pour utiliser les Visual Studio pour déboguer les Microsoft Edge.  

## <a name="launch-microsoft-edge"></a>Lancer Microsoft Edge  

Visual Studio le flux de travail suivant à l’aide d’un seul bouton.  

1.  Crée votre application ASP.NET et ASP.NET Core’application.  
1.  Démarre votre serveur web.  
1.  Lance Microsoft Edge.  
1.  Connecte le débo Visual Studio débooeur.  
    
Le flux de travail simplifié vous permet de déboguer JavaScript qui s’exécute Microsoft Edge directement à partir de votre IDE.  

### <a name="create-a-new-aspnet-core-web-app"></a>Créer une application ASP.NET Core web  

Ouvrez Visual Studio 2019 et choisissez **Créer un projet.**  Sur l’écran suivant, choisissez **ASP.NET Core’application Web**  >  **Suivante.**  

:::image type="complex" source="./media/create-new-project.png" alt-text="Créer une application ASP.NET Core Web" lightbox="./media/create-new-project.png":::
   Créer une application ASP.NET Core Web  
:::image-end:::  

Fournissez **un Project pour** votre nouveau projet et choisissez **Créer.**  Pour les besoins de l’exemple, ** choisissezReact.js** en tant que modèle, puis choisissez **Créer**.  Le **React.js** indique comment intégrer des React.js une application ASP.NET Core de messagerie.  

### <a name="launch-microsoft-edge-from-visual-studio"></a>Lancer le Microsoft Edge à partir Visual Studio  

Après avoir créé votre projet, ouvrez `ClientApp/src/components/Counter.js` .  Maintenant, pour utiliser Visual Studio pour déboguer JavaScript, choisissez la zone de description en haut du bouton **vert Lire** **et IIS Express**.  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="La zone de la zone de lecture en haut du bouton vert IIS Express" lightbox="./media/vs-dropdown.png":::
   La zone de la zone **** de lecture en haut du bouton **vert IIS Express**  
:::image-end:::  

Choose **Script Debugging**  >  **Enabled**.  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Activer le débogage de script dans Visual Studio" lightbox="./media/enable-script-debugging.png":::
   Activer le débogage de script dans Visual Studio  
:::image-end:::  

Dans la même dropdown, choisissez navigateur **web** > le canal d’aperçu de Microsoft Edge que vous souhaitez que Visual Studio lance, tel que Microsoft Edge Canary, Dev ou Beta.  Si vous n’utilisez pas déjà l’un Microsoft Edge de prévisualisation, accédez à Télécharger [Microsoft Edge canaux Insider pour][MicrosoftedgeinsiderDownload] en télécharger un.  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Choisissez le canal d’aperçu Microsoft Edge que vous souhaitez Visual Studio lancer" lightbox="./media/set-web-browser.png":::
   Choisissez le canal d’aperçu Microsoft Edge que vous souhaitez Visual Studio lancer  
:::image-end:::  

> [!NOTE]
> Si vous choisissez Microsoft Edge \(EdgeHTML\), Visual Studio la lance au lieu de Microsoft Edge \(Chromium\).  Installez l’un des canaux d’aperçu de [Microsoft Edge][MicrosoftedgeinsiderDownload] ou assurez-vous que la version de Microsoft Edge installée sur votre ordinateur est Microsoft Edge \(Chromium\) et non Microsoft Edge \(EdgeHTML\).  

Maintenant que Visual Studio est correctement configuré, choisissez le bouton **Vert** Lire.  Visual Studio votre application, démarrez le serveur web, lancez Microsoft Edge, puis accédez à ou à n’importe quel `https://localhost:44362/` port spécifié dans `launchSettings.json` .  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge lancement à partir de Visual Studio" lightbox="./media/edge-launch.png":::
   Microsoft Edge lancement à partir de Visual Studio  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a>Déboguer JavaScript en cours d’exécution Microsoft Edge  

Revenir à Visual Studio.  In `Counter.js` , to set a breakpoint on Line 13, choose the gutter next to the line.  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Choisissez la caniveau en face de la ligne 13 dans Counter.js pour définir un point d’arrêt dans Visual Studio" lightbox="./media/set-breakpoint.png":::
   Choisissez la caniveau en face de la ligne 13 `Counter.js` pour définir un point d’arrêt dans Visual Studio  
:::image-end:::  

Revenir à l’instance de Microsoft Edge que Visual Studio lancée.  Choisissez sur **Compteur** dans navMenu à gauche de la page web.  Maintenant, choisissez **Incrément .**  

:::image type="complex" source="./media/edge-counter.png" alt-text="Page Compteur dans notre application ASP.NET Core web" lightbox="./media/edge-counter.png":::
   Page Compteur dans notre application ASP.NET Core web  
:::image-end:::  

Le débogger JavaScript dans Visual Studio atteint le point d’arrêt que vous définissez dans `Counter.js` .  Visual Studio suspend désormais l’exécution du javaScript en cours d’exécution dans Microsoft Edge et vous pouvez exécuter le script ligne par ligne.  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio javaScript s’exécute en Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   Visual Studio javaScript s’exécute en Microsoft Edge  
:::image-end:::  

L’exemple n’était qu’une démonstration mineure des fonctionnalités disponibles dans Visual Studio.  Pour plus d’informations sur les fonctionnalités Visual Studio 2019, accédez [à Visual Studio documentation.][VisualStudioWindowsIndex]  

## <a name="attach-to-microsoft-edge"></a>Attacher à Microsoft Edge  

Auparavant, vous deviez lancer Microsoft Edge à partir Visual Studio.  À présent, vous pouvez attacher le débogger Visual Studio à une instance de Microsoft Edge.  

Tout d’abord, assurez-vous qu’il n’existe aucune instance de Microsoft Edge.  À présent, à partir de votre ligne de commande, exécutez la commande suivante.  

```console
start msedge –remote-debugging-port=9222
```  

À Visual Studio, ouvrez le menu **Débogage** et choisissez **Attacher au** processus ou sélectionnez `Ctrl` + `Alt` + `P` .  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Choose Attach to Process in Visual Studio" lightbox="./media/attach-to-process.png":::
   Choose **Attach to Process** in Visual Studio  
:::image-end:::  

À partir de **la boîte de dialogue Attacher** au processus, définissez le **type** de connexion sur websocket de protocole **Chrome devtools (aucune authentification).**  Dans la **boîte de texte Cible** de connexion, `http://localhost:9222/` tapez et sélectionnez `Enter` .  Examinez la liste des onglets ouverts que vous avez Microsoft Edge répertoriés dans la boîte de dialogue Attacher **au processus.**  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Configurer la boîte de dialogue Attacher au processus dans Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   Configurer la boîte **de dialogue Attacher au** processus dans Visual Studio  
:::image-end:::  

**Sélectionnez...** > case à cocher en regard de **JavaScript (Microsoft Edge – Chromium).**  Pour ajouter des onglets, accédez aux nouveaux onglets, fermez **** les onglets et affichez les modifications reflétées dans la boîte de dialogue Attacher au processus, sélectionnez **le bouton Actualiser.**  Choisissez l’onglet que vous souhaitez déboguer et choisissez **Attacher.**  

Le débo Visual Studio est maintenant attaché à Microsoft Edge.  Vous pouvez suspendre l’exécution de JavaScript, définir des points d’arrêt et réviser des instructions directement dans la fenêtre Sortie `console.log()` de débogage Visual Studio.  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a>Entrer en contact avec l’équipe Microsoft Visual Studio de recherche  

Les Microsoft Visual Studio et Microsoft Edge souhaitent en savoir plus sur la façon dont vous travaillez avec JavaScript dans Visual Studio.  Pour envoyer vos commentaires, sélectionnez l’icône Envoyer des commentaires Visual Studio ou tweetez-@VisualStudio [et @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools]. ****  

:::image type="complex" source="./media/feedback-icon.png" alt-text="Icône Envoyer des commentaires dans Visual Studio" lightbox="./media/feedback-icon.png":::
   Icône **Envoyer des commentaires** dans Visual Studio  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio documentation | Documents Microsoft"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Télécharger Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet vers @VisualStudio et @EdgeDevTools | Twitter"  
