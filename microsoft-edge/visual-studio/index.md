---
description: Microsoft Edge (chrome) et Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, vs, Visual Studio, débogueur
ms.openlocfilehash: 3fc2e2c3dc21689d8c378ccbe33e4dff813ea12f
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986191"
---
# Visual Studio

Microsoft [Visual Studio](https://visualstudio.microsoft.com/vs/) est un environnement de développement intégré (IDE) que vous pouvez utiliser pour modifier, déboguer, générer et publier vos applications Web. Il s’agit d’un programme riche en fonctionnalités qui peut être utilisé pour de nombreux aspects du développement Web. Au-dessus et au-dessus de l’éditeur et du débogueur standard proposés par la plupart des environnements d’interface de développement, Visual Studio inclut des compilateurs, des outils d’exécution de code, des concepteurs graphiques et de nombreuses autres fonctionnalités pour faciliter votre processus de développement. Accédez à [cette page](https://visualstudio.microsoft.com/downloads/) pour télécharger Visual Studio si vous ne l’utilisez pas encore.

Pour l’instant, Visual Studio 2019 prend en charge le débogage JavaScript dans Microsoft Edge pour votre infrastructure ASP\.NET et les applications principales ASP\.NET. Suivez les étapes ci-dessous pour déboguer Microsoft Edge à partir de Visual Studio.

## Lancer Microsoft Edge
Visual Studio crée votre application principale ASP\.NET et ASP\.NET, démarre votre serveur Web, lance Microsoft Edge et connecte le débogueur Visual Studio en un clic. Cela vous permet de déboguer JavaScript en cours d’exécution dans Microsoft Edge directement à partir de votre IDE.

### Créer une application Web de base ASP.NET

Ouvrez Visual Studio 2019 et sélectionnez **créer un projet**. Dans l’écran suivant, sélectionnez **ASP\.NET Web Core application** et cliquez sur **suivant**.

> ##### Figure1  
> Créer une nouvelle application Web principale ASP.NET ![ créer une nouvelle application Web noyau ASP.net](./media/create-new-project.png)  

Indiquez le **nom** d’un projet pour votre nouveau projet, puis cliquez sur **créer**. Dans le cadre de cet exemple, sélectionnez **React.js** comme modèle qui vous montre comment intégrer React.js à une application principale ASP.net et cliquez sur **créer**.

### Lancer Microsoft Edge à partir de Visual Studio

Une fois votre projet créé, ouvrez **ClientApp/SRC/composants/Counter.js**. À présent, demandez à Visual Studio de déboguer JavaScript en sélectionnant le menu déroulant en regard du bouton de **lecture** vert et d' **IIS Express**. 

> ##### Figure 2  
> La liste déroulante en regard du bouton de **lecture** **vert et de** 
> ![ la liste déroulante en regard du bouton de lecture vert et d’IIS Express](./media/vs-dropdown.png)  

Sélectionnez **débogage de script** , puis cliquez sur **activé**.

> ##### Figure3  
> Activer le débogage de script dans Visual Studio ![ activer le débogage de script dans Visual Studio](./media/enable-script-debugging.png)  

Dans la même liste déroulante, sélectionnez **navigateur Web** , puis cliquez sur le canal d’aperçu de Microsoft Edge que Visual Studio doit lancer: Microsoft Edge Canaries, dev ou beta. Si ce n’est déjà fait, accédez à [cette page](https://www.microsoftedgeinsider.com/download) pour installer les canaux Microsoft Edge preview.

> ##### Figure 4  
> Sélectionnez la version d’évaluation du canal Microsoft Edge que vous souhaitez que Visual Studio démarre ![ sélectionnez le canal de version d’évaluation de Microsoft Edge que Visual Studio doit lancer.](./media/set-web-browser.png)  

> [!NOTE]
> Si vous sélectionnez Microsoft Edge (EdgeHTML), Visual Studio lancera cette opération au lieu de Microsoft Edge (chrome). [Installez les canaux d’aperçu de Microsoft Edge](https://www.microsoftedgeinsider.com/download) et sélectionnez-les ou assurez-vous que la version de Microsoft Edge installée sur votre ordinateur est Microsoft Edge (chrome) et non Microsoft Edge (EdgeHTML).

Maintenant que Visual Studio est configuré correctement, cliquez sur le bouton de **lecture** vert. Visual Studio va générer votre application, démarrer le serveur Web, lancer Microsoft Edge et accéder à l’application `https://localhost:44362/` ou au port spécifié dans **launchSettings.jsactivé**.

> ##### Figure 5  
> Microsoft Edge lancé depuis Visual Studio ![ Microsoft Edge lancé depuis Visual Studio](./media/edge-launch.png)  

### Déboguer JavaScript en cours d’exécution dans Microsoft Edge

Revenez à Visual Studio. Dans **Counter.js**, définissez un point d’arrêt sur la ligne 13 en cliquant dans la reliure en regard de la ligne.

> ##### Figure 6
> Pour définir un point d’arrêt dans Visual Studio, cliquez sur la reliure en regard de la ligne 13 dans **Counter.js** 
> ![ définir un point d’arrêt dans Visual Studio en cliquant sur la reliure en regard de la ligne 13 dans Counter.js](./media/set-breakpoint.png)  

Revenez à l’instance de Microsoft Edge lancée par Visual Studio. Cliquez sur le **compteur** dans le NavMenu à gauche de la page. Cliquez à présent sur **incrément**.

> ##### Figure 7
> La page de compteur de notre application Web principale ASP.NET ![ la page de compteur de notre application Web principale ASP.net](./media/edge-counter.png)  

Le débogueur JavaScript dans Visual Studio va appuyer sur le point d’arrêt défini dans **Counter.js**. Visual Studio a interrompu l’exécution du JavaScript en cours d’exécution dans Microsoft Edge et vous pouvez parcourir les lignes de script en ligne.

> ##### Figure8
> Visual Studio suspend JavaScript en cours d’exécution dans Microsoft Edge ![ Visual Studio suspendre JavaScript en cours d’exécution dans Microsoft Edge](./media/hit-breakpoint.png)  

Cet exemple ne s’agissait que d’une simple démonstration des fonctionnalités disponibles dans Visual Studio. Pour plus d’informations sur les opérations que vous pouvez effectuer dans Visual Studio 2019, consultez la [documentation](https://docs.microsoft.com/visualstudio/windows/?view=vs-2019)correspondante.

## Joindre à Microsoft Edge
Dans le flux de travail précédent, Visual Studio lance Microsoft Edge. Avec ce flux de travail, vous serez en mesure de joindre Visual Studio Debugger à une instance déjà en cours d’exécution de Microsoft Edge. 

Tout d’abord, assurez-vous qu’il n’y a aucune instance en cours d’exécution de Microsoft Edge. À présent, à partir de votre terminal, exécutez la commande suivante:

```console
start msedge –remote-debugging-port=9222
```

Dans Visual Studio, ouvrez le menu **Déboguer** , puis sélectionnez **attacher au processus** ou appuyez sur `Ctrl`  +  `Alt`  +  `P` .

> ##### Figure9
> Sélectionner **joindre au processus** dans Visual Studio, ![ sélection * * joindre au processus * * dans Visual Studio](./media/attach-to-process.png)  

Dans la boîte de dialogue **joindre au processus** , définissez **type de connexion** sur **chrome devtools protocole WebSocket (aucune authentification)**. Dans la zone de texte de la **cible de connexion** , entrez `http://localhost:9222/` et appuyez sur `Enter` . Vous devriez voir la liste des onglets ouverts que vous avez dans Microsoft Edge dans la boîte de dialogue **joindre au processus** .

> ##### Figure10
> Configuration de la boîte de dialogue **joindre au processus** dans Visual Studio ![ configuration de la boîte de dialogue joindre au processus dans Visual Studio](./media/attach-to-process-dialog.png)  

Cliquez sur **Sélectionner...** et vérifiez **JavaScript (Microsoft Edge-chrome)**. Vous pouvez ajouter des onglets, accéder à de nouveaux onglets, puis fermer les onglets et voir les modifications reflétées dans la boîte de dialogue **joindre au processus** en cliquant sur le bouton **Actualiser** . Sélectionnez l’onglet que vous voulez déboguer, puis cliquez sur **joindre**.

Le débogueur Visual Studio est désormais attaché à Microsoft Edge. Vous pouvez interrompre l’exécution d’JavaScript, définir des points d’arrêt et afficher `console.log()` directement des instructions dans la fenêtre sortie de débogage de Visual Studio.

## Contacter l’équipe Microsoft Visual Studio  

Nous sommes impatients d’apprendre à utiliser JavaScript dans Visual Studio.  Envoyez-nous vos commentaires en cliquant sur l’icône de **Commentaires** dans Visual Studio ou en utilisant un tweeter [ @VisualStudio and @EdgeDevTools](https://twitter.com/intent/tweet?text= @VisualStudio + @EdgeDevTools).  

> ##### Figure11
> Icône **Commentaires** dans Visual Studio, dans Visual Studio ![](./media/feedback-icon.png)  
