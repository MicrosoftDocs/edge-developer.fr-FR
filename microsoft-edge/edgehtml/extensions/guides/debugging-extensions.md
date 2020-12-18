---
description: Avec les outils de développement F12, Découvrez comment déboguer le script en arrière-plan, les scripts de contenu et les pages d’extension d’une extension.
title: Extensions-débogage
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, JavaScript, développeur, débogage et débogage
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 17da1a2badd99dd57bb8b1e3de063fe045b34333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233416"
---
# Extensions de débogage  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide des outils de développement F12.

La vidéo suivante présente une extension Microsoft Edge de Microsoft, en passant par chaque scénario de débogage et en le fixant. Pour plus d’informations, consultez les instructions pas à pas ci-dessous.

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> Pour tirer parti du débogage par extension avec la fonction F12, vous devez d’abord activer les fonctionnalités de développement dans à propos de: indicateurs. Pour plus d’informations sur la façon de procéder [, voir Ajout et suppression d’extensions](./adding-and-removing-extensions.md) .


## Débogage de script en arrière-plan
Pour démarrer le débogage du script en arrière-plan de votre extension:

1. Cliquez sur **plus (...),** puis sur **Extensions** pour accéder au volet extension.  
 ![Bouton plus](./../media/morebutton.png)
2. Cliquez sur l’extension que vous souhaitez déboguer.
3. Cliquez sur le lien de la **page d’arrière-plan** pour afficher la touche F12 du processus en arrière-plan.  
 ![affichage extensions sélectionnés des options avec le lien inspecter](./../media/debug-inspect.png)
4. Sélectionnez l’onglet **débogueur** dans F12.
5. Naviguez jusqu’au script en arrière-plan de votre extension et sélectionnez-le.
6. Placez des points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.  
 ![Console F12 montrant le script en arrière-plan avec des points d’arrêt](./../media/debug-f12-background.png)
7. Sélectionnez l’onglet **console** et exécutez la commande « `location.reload()` ». Cette opération permet de réexécuter le script en arrière-plan, ce qui vous permet de parcourir votre code.  
 ![console avec emplacement. recharger entré](./../media/debug-f12-background-console.png)


## Débogage de script de contenu
Pour démarrer le débogage du script de contenu de votre extension:

1. Lancez la version F12 en accédant au bouton **autres (...)** et en sélectionnant **«F12 outils de développement»** ou en appuyant sur la touche F12 de votre clavier.
2. Recherchez et sélectionnez le script de contenu de votre extension. Les scripts de contenu pour les extensions actuellement en cours d’exécution seront représentés par un dossier différent pour chaque extension.

    > [!NOTE]
    > Seuls les scripts de contenu doivent s’afficher.

3. Placez des points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.  
 ![F12 avec le débogage de script de contenu](./../media/debug-content-f12.png)
4. Actualisez l’onglet du navigateur pour commencer à exécuter votre code.




## Débogage de page d’extension

Il existe deux méthodes qui peuvent être utilisées pour accéder au code source de la page de votre extension pour le débogage. Une méthode s’applique à un large éventail de pages tandis que l’autre fonctionne uniquement pour les pages contextuelles.

### Débogage de n’importe quelle page d’extension
La méthode suivante fonctionne pour toutes les pages d’extension, comme la page d’options et les fenêtres contextuelles:


1. Cliquez avec le bouton droit sur l’arrière-plan de votre page.
2. Sélectionnez **«afficher la source»**.

   ![débogage contextuelle avec F12-sélectionnez](./../media/debug-popup-select.png)

3. Lorsque F12 s’ouvre, placez les points d’arrêt dans le fichier que vous voulez déboguer.

   ![débogage contextuelle avec F12](./../media/debug-popup-f12.png)
4. Sélectionnez l’onglet **console** et exécutez la commande `location.reload()` . Cette opération permet de réexécuter le script de page, ce qui vous permet de parcourir votre code.  

   ![console avec emplacement. recharger entré](./../media/debug-f12-background-console.png)

### Débogage d’une page d’extension contextuelle
Bien que la méthode utilisée pour déboguer les pages d’extension s’applique également aux pages d’extension contextuelle, les étapes suivantes décrivent une autre méthode de débogage de votre fenêtre contextuelle:

1. Cliquez avec le bouton droit sur l’icône de votre extension.
2. Sélectionnez **«Inspect Popup»**.

   ![inspection de débogage contextuelle](./../media/debug-popup-inspect.png)
3. Suivez les étapes 3 et 4 ci-dessus pour placer des points d’arrêt et recharger la fenêtre contextuelle.
