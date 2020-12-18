---
description: Émuler les déficiences de la vision dans Microsoft Edge DevTools.
title: Émuler les déficiences de la vision dans Microsoft Edge DevTools (cécité des couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230823"
---
# Émuler les faiblesses de la vision

Pour mieux répondre aux besoins de vos utilisateurs grâce à la déficience de la [couleur][ColorblindawarenessMain] (en aveugle \), [Microsoft Edge devtools][DevtoolsIndex] vous permet de simuler des défauts de vision spécifiques.  L’outil **émuler les déficiences** de la vision simule les catégories suivantes.  

| Déficience de la vision couleur | Détails |  
|:--- |:--- |  
| Vision floue | L’utilisateur a des difficultés à se focaliser sur des détails précis. |   
| Protanopia | L’utilisateur ne peut percevoir aucun éclairage rouge. |  
| Deuteranopia | L’utilisateur ne peut percevoir aucun éclairage vert. |  
| Tritanopia | L’utilisateur ne peut pas percevoir de lumière bleue. |  
| Achromatopsia | L’utilisateur ne peut pas percevoir une couleur, ce qui réduit toute la couleur en nuance de gris. |  

## Accéder aux outils de rendu  

Pour simuler une déficience de vision pour votre produit Web, ouvrez les [outils de rendu][DevtoolsRenderingToolsIndex].  

1.  Pour ouvrir les outils de rendu, en choisissant l' `...` élément de menu dans la barre d’outils  
1.  Choisir `More tools`  
1.  Choisir `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Ouverture des outils de rendu" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Ouverture des **outils de rendu**  
    :::image-end:::  

Le menu **rendu** s’affiche dans le tiroir.  

1.  Faites défiler vers le bas jusqu’à l' `Emulate vision deficiencies` élément de menu, puis sélectionnez le menu déroulant pour afficher les options.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menu émuler les déficiences de la vision sur le tiroir de rendu" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Menu **émuler les déficiences** de la vision sur le tiroir de **rendu**  
    :::image-end:::  
    
1.  Choisissez une option.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Options de menu émuler la vision carences" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Options de menu **émuler la vision carences**  
    :::image-end:::  
    
1.  La fenêtre principale de Windows affiche la simulation de l’option choisie appliquée à la page active.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Affichage à l’aide de * * vision floue * * simulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Affichage avec simulation de **vision floue**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Affichage à l’aide de * * achromatopsia * * simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Affichage à l’aide de la simulation **achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Utiliser le menu de commandes  

Vous pouvez également utiliser le **menu de commandes** pour accéder aux différentes simulations.  

1.  Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Tapez `emulate` , sélectionnez ce que vous voulez simuler et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Différentes options de simulation disponibles dans le menu de commandes" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Différentes options de simulation disponibles dans le **menu de commandes**  
    :::image-end:::  
    
> [!IMPORTANT]
> Les outils d’déficience de la **vision** simulent des approximations de la façon dont une personne avec chaque déficience risque de voir votre produit.  Chaque personne est différente, par conséquent, les déficiences de vision varient en fonction du niveau de gravité d’une personne à l’autre.  Pour mieux répondre aux besoins de vos utilisateurs, évitez les combinaisons de couleurs susceptibles de résoudre le problème.  Les outils d’déficience de la **vision** ne constituent pas une évaluation complète de votre produit.  Au lieu de cela, les outils **émuler les déficiences** de la vision doivent vous offrir une bonne première étape pour éviter les problèmes.  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analyser les performances au moment de l’exécution | Documents Microsoft"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Organisme de sensibilisation couleur aveugle"  

[AmfcbMain]: https://www.amfcb.org "L’American Foundation pour les aveugles en couleur (AFCB)"  

