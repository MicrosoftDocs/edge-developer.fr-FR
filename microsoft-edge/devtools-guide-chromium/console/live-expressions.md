---
description: Si vous vous trouvez en train de taper les mêmes expressions JavaScript dans la console à plusieurs reprises, essayez plutôt Expressions live.
title: Regardez les valeurs des expressions JavaScript en temps réel avec des expressions live
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 51b7aa5119775f43861a84c1055ac9149a626d8a
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483127"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a>Surveiller les modifications apportées dans JavaScript à l’aide d’expressions live  

**Les expressions live** sont un excellent moyen de surveiller les expressions JavaScript qui changent beaucoup.    Au lieu d’avoir de nombreux messages de console à lire et à parcourir, vous pouvez épingler vos expressions JavaScript spécifiques en haut de la **console.**  

## <a name="add-a-new-live-expression"></a>Ajouter une nouvelle expression live  

Pour commencer, sélectionnez le bouton Créer **une expression live** \(œil\) en regard de la **boîte** de texte Filtre.  Une fois que vous l’avez choisi, une boîte de texte s’affiche pour que vous y insérez votre nouvelle expression.  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Sélectionnez le bouton Nouvelle expression en direct pour ouvrir une boîte de texte pour taper une expression" lightbox="../media/console-live-expressions-new.msft.png":::
    Choisissez le `New live expression` bouton pour ouvrir une boîte de texte pour taper une expression  
:::image-end:::  

**Les expressions live** peuvent être n’importe quelle expression JavaScript valide.  Pour l’essayer, effectuer les actions suivantes.  

1.  Ouvrez la **boîte de texte Expression** live.  
1.  Tapez `document.activeElement`.  
1.  Pour enregistrer l’expression, effectuer l’une des actions suivantes.  
    *   Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\).  
    *   Choisissez en dehors de **la boîte de texte Expression** live.  
        
L’expression est maintenant en direct et s’affiche `body` en tant que résultat.  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="Expression dynamique pour document.activeElement affiche le corps en tant que résultat" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    Expression live pour `document.activeElement` afficher le corps en tant que résultat  
:::image-end:::  

Si vous naviguez dans la page web, la valeur change.  Par exemple, dans la figure suivante, vous ouvrez le menu de recherche dans la page web et l’expression s’affiche maintenant `button.nav-bar-button.focus-visible` en tant que valeur.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Pour modifier la valeur de l’expression live, interagissez avec différents éléments sur la page web" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    Pour modifier la valeur de **l’expression live,** interagissez avec différents éléments sur la page web  
:::image-end:::  

Pour modifier à nouveau la valeur, ouvrez et choisissez la zone de texte Rechercher sur la page web.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Accédez à un autre élément dans la page web pour mettre à jour l’expression live" lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    Accédez à un autre élément dans la page web pour mettre à jour **l’expression live**  
:::image-end:::  

## <a name="remove-live-expressions"></a>Supprimer des expressions live  

Une **expression dynamique** est disponible tant que vous la conservez active.  Pour vous débarrasser d’une **expression live,** choisissez la `x` suivante.  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Pour supprimer des expressions en direct, choisissez le x à côté de celui-ci" lightbox="../media/console-live-expressions-remove.msft.png":::
    Pour supprimer **des expressions live,** choisissez le `x` suivant  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a>Remplacer la journalisation de la console par des expressions en direct  

Vous pouvez créer autant d’expressions que vous le souhaitez et les faire persister entre les sessions de navigateur et les fenêtres.  **Les expressions live** sont un moyen de réduire le bruit dans votre flux de travail de débogage.  

Par exemple, vous souhaitez surveiller le mouvement de la souris dans la page web actuelle.  Accédez à [la démonstration de journalisation][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]du mouvement de la souris, ouvrez la **console**et déplacez votre souris pour afficher les journaux avec un grand nombre d’informations.  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="La console affiche beaucoup d’informations sur la position de la souris" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    **La console** affiche beaucoup d’informations sur la position de la souris  
:::image-end:::  

La grande quantité d’informations ralentit non seulement votre processus de débogage, mais facilite également l’accès aux modifications que vous souhaitez examiner.  À mesure **que la console** affiche davantage de messages et que vous déplacez votre souris, les valeurs que vous souhaitez consulter défilent hors de l’écran.  

Pour essayer **les expressions live en** tant qu’alternative, effectuer les actions suivantes.  

1.  Accédez au mouvement [de la souris sans la démonstration de journalisation.][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]  
1.  Créer **des expressions en direct** pour et `x` `y` .  
    
Lorsque vous utilisez **des expressions**live, vous obtenez toujours les informations sur la même partie de votre écran et conservez les journaux de la **console** pour les valeurs qui ne changent pas autant.

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Afficher la position x et y de la souris en tant qu’expressions live" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    Afficher la `x` position et la position de la souris en tant `y` **qu’expressions live**  
:::image-end:::  

**Les expressions live** s’exécutent exclusivement sur votre ordinateur et vous n’avez rien à modifier dans votre code pour l’afficher.  **Les expressions live** sont un excellent moyen de vous assurer que vous affichez uniquement les informations que vous souhaitez déboguer.  En outre, **les expressions live** vous aident à limiter le bruit sur les ordinateurs de vos utilisateurs.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Exemples de messages de console : utilisation du tableau | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Mouvement de la souris sans journalisation | GitHub"  
