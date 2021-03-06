---
description: Avec les outils de développement F12, découvrez comment déboguer le script d’arrière-plan, les scripts de contenu et les pages d’extension d’une extension.
title: Débogage | Extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, javascript, développeur, débogage, débogage
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399364"
---
# <a name="debugging-extensions"></a>Extensions de débogage  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide des outils de développement F12.  

La vidéo suivante montre une extension Microsoft Edge difficile, en parant chaque scénario de débogage et en le corrigeant tout au long du chemin.  Pour plus d’informations, voir les instructions détaillées ci-dessous.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> Pour tirer parti du débogage des extensions avec F12, vous devez d’abord activer les fonctionnalités de développement dans about:flags.  Voir [Ajout et suppression d’extensions](./adding-and-removing-extensions.md) pour plus d’informations sur la façon de le faire.  

## <a name="background-script-debugging"></a>Débogage de script en arrière-plan  

Pour commencer à déboguer le script en arrière-plan de votre extension :  

1.  Cliquez sur **Plus (...)** suivi **des extensions** pour aller dans le volet d’extensions.  
    
    ![Bouton plus](../media/morebutton.png)  
    
1.  Cliquez sur l’extension à déboguer.  
1.  Cliquez sur le lien de la page d’arrière-plan pour faire monter la F12 pour le processus en arrière-plan. ****  
    
    ![vue d’extension sélectionnée des options avec le lien Inspecter](../media/debug-inspect.png)  
    
1.  Sélectionnez **l’onglet Débogger** dans F12.  
1.  Accédez au script en arrière-plan de votre extension et sélectionnez-le.  
1.  Placez les points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.  
    
    ![Console f12 affichant un script en arrière-plan avec des points d’coupure](../media/debug-f12-background.png)  
    
1.  Sélectionnez **l’onglet Console** et exécutez la `location.reload()` commande.  Cela réexécute le script en arrière-plan, ce qui vous permet d’exécuter pas à pas votre code.  
    
    ![console avec location.reload entrée](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a>Débogage de script de contenu  

Pour commencer à déboguer le script de contenu de votre extension :  

1.  Lancez F12 en naviguant vers le bouton **Plus (...)** et en sélectionnant Outils de **développement F12** ou en appuyant `F12` sur votre clavier.  
1.  Accédez au script de contenu de votre extension et sélectionnez-le.  Les scripts de contenu pour les extensions en cours d’exécution sont représentés par un dossier différent pour chaque extension.  
    
    > [!NOTE]
    > Seuls les scripts de contenu en cours d’exécution s’affichent.  
    
1.  Placez les points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.  
    
    ![f12 avec le script de contenu déboyé](../media/debug-content-f12.png)  
    
1.  Actualisez l’onglet du navigateur pour commencer pas à pas dans votre code.  
    
## <a name="extension-page-debugging"></a>Débogage de page d’extension  

Deux méthodes peuvent être utilisées pour accéder au code source de votre page d’extension pour le débogage.  Une méthode s’applique à une variété de pages, tandis que l’autre fonctionne uniquement pour les pages popup.  

### <a name="debugging-any-extension-page"></a>Débogage d’une page d’extension  

La méthode suivante fonctionne pour toutes les pages d’extension, telles que la page d’options et les fenêtres popup :  

1.  Cliquez avec le bouton droit sur l’arrière-plan de votre page.  
1.  Sélectionnez **Afficher la source.**  
    
    ![Ouvrir le débogage de fenêtres popup avec f12](../media/debug-popup-select.png)  
    
1.  Une fois la F12 ouverte, placez les points d’arrêt dans le fichier que vous souhaitez déboguer.  
    
    ![débogage popup avec f12](../media/debug-popup-f12.png)  
    
1.  Sélectionnez **l’onglet Console** et exécutez la `location.reload()` commande.  Cela réexécute le script de page, ce qui vous permet d’exécuter pas à pas votre code.  
    
    ![console avec location.reload entrée](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a>Débogage d’une page d’extension popup  

Bien que la méthode de débogage des pages d’extension s’applique également aux pages d’extension de fenêtre popup, les étapes suivantes décrivent une autre façon de déboguer votre fenêtre popup :  

1.  Cliquez avec le bouton droit sur l’icône de votre extension.  
1.  Sélectionnez **Inspecter la fenêtre pop-up**.  
    
    ![inspection du débogage popup](../media/debug-popup-inspect.png)  
    
1.  Suivez les étapes 3 et 4 ci-dessus pour placer des points d’arrêt et recharger la fenêtre popup.  
    