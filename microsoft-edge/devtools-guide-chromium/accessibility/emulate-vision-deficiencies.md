---
title: Émuler les déficiences de la vision dans Microsoft Edge DevTools (cécité des couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758084"
---
# Émuler les déficiences de la vision

Dans le monde entier, environ 8% des hommes et 0,5% des femmes présentent un déficience de la vision de la [couleur][ColorblindawarenessMain] qui est souvent appelée «cécité en couleur».  [Microsoft Edge devtools][MicrosoftEdgeDevTools] vous permet d’émuler différentes déficiences connues et de fournir un aperçu de votre produit pour vous permettre de le consulter.  

| Déficience de la couleur | Détails |  
|:--- |:--- |  
| Vision floue |  |   
| Protanopia | L’impossibilité de percevoir des lumières rouges. |  
| Deuteranopia | L’impossibilité de percevoir une lumière verte. |  
| Tritanopia | L’impossibilité de percevoir une lumière bleue. |  
| Achromatopsia | L’impossibilité de percevoir une couleur, à l’exception des nuances de gris. |  

## Accéder aux outils de rendu  

Pour tester votre produit Web actuel à des fins de coloration, ouvrez les [outils de rendu][RenderingTools].  

1.  Ouvrir les outils de rendu en sélectionnant l' `...` élément de menu dans la barre d’outils  
1.  Sélectionner `More tools`  
1.  Sélectionner `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Ouverture des outils de rendu" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Ouverture des **outils de rendu**  
    :::image-end:::  

Le menu de **rendu** s’affiche dans la partie inférieure du devtools.  

1.  Faites défiler vers le bas jusqu’à l' `Emulate Vision deficiencies` élément de menu, puis sélectionnez l’une des options proposées.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menu émuler les déficiences de la vision des outils de rendu" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Menu **émuler les déficiences** de la vision des outils de **rendu**  
    :::image-end:::  
    
1.  Choisir une des options  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Options de menu émuler la vision carences" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Options de menu **émuler la vision carences**  
    :::image-end:::  
    
1.  La page actuelle s’affiche dans une simulation de la façon dont elle peut s’afficher à l’utilisateur présentant le déficience choisie.  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Documentation des outils de développement Microsoft Edge dans l’émulation de vision floue" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Affichage à l’aide d’une émulation de **vision floue**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Documentation des outils de développement Microsoft Edge dans l’émulation de vision achromatopsia" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Affichage à l’aide de l’émulation de **vision achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Utiliser le menu de commandes  

Vous pouvez également accéder aux différentes émulations sans utiliser les différents menus du menu de **commandes**.  

1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Tapez `emulate` , sélectionnez ce que vous voulez simuler et appuyez sur `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Différentes options d’émulation disponibles dans le menu de commandes" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Différentes options d’émulation disponibles dans le **menu de commandes**  
    :::image-end:::  
    
> [!IMPORTANT]
> Les outils d’émulation sont des approximations de la façon dont une personne avec chaque déficience risque de voir votre produit.  Chaque personne est différente, par conséquent, les déficiences de vision varient en fonction du niveau de gravité d’une personne à l’autre.  Pour mieux répondre aux besoins de vos utilisateurs, évitez les combinaisons de couleurs susceptibles de résoudre le problème.  Les outils d’émulation ne retrouvent pas une évaluation complète de l’accessibilité de votre produit, mais il est recommandé de commencer par une bonne étape pour éviter les défauts les plus importants.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Organisme de sensibilisation couleur aveugle"  
[AmfcbMain]: https://www.amfcb.org "L’American Foundation pour les aveugles en couleur (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Outils de rendu Microsoft Edge (chrome)"  
