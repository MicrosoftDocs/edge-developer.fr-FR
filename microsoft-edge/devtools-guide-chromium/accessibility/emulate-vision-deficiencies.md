---
description: Émuler les défaillances visuelles dans Microsoft Edge DevTools.
title: Émuler les défaillances visuelles dans Microsoft Edge DevTools (daltonisme)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: eec3c95bac93e600acf1887c8d31cea2173c6aee
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397873"
---
# <a name="emulate-vision-deficiencies"></a>Émuler les faiblesses de la vision

Pour mieux répondre aux besoins de vos utilisateurs ayant des problèmes de [vision][ColorblindawarenessMain] des couleurs \(daltonisme\), [Microsoft Edge DevTools][DevtoolsIndex] vous permet de simuler des défaillances de vision de couleur spécifiques.  **L’outil Émuler les défauts de vision** simule les catégories suivantes.  

| Problèmes de vision des couleurs | Détails |  
|:--- |:--- |  
| Vision floue | L’utilisateur a des difficultés à se concentrer sur des détails précis. |  
| Protanopia | L’utilisateur ne peut pas percevoir de lumière rouge. |  
| Deuteranopia | L’utilisateur ne peut pas percevoir de lumière verte. |  
| Tritanopia | L’utilisateur ne parvient pas à percevoir la lumière bleue. |  
| Achromatopsia | L’utilisateur ne peut percevoir aucune couleur, ce qui réduit toutes les couleurs à une nuance de gris. |  

## <a name="navigate-to-the-rendering-tools"></a>Accéder aux outils de rendu  

Pour simuler une défaillance visuelle appliquée à votre produit web, ouvrez les [outils de rendu.][DevtoolsRenderingToolsIndex]  

1.  Pour ouvrir les outils de rendu, choisissez `...` l’élément de menu dans la barre d’outils  
1.  Choisir **d’autres outils**  
1.  Choisir le **rendu**  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Ouverture des outils de rendu" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Ouverture des **outils de rendu**  
    :::image-end:::  

Le menu **Rendu** s’affiche dans le bac.  

1.  Faites défiler vers le bas `Emulate vision deficiencies` jusqu’à l’élément de menu et choisissez le menu déroulant pour afficher les options.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menu Émuler les défaillances de la vision dans le caisse de rendu" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Le **menu Émuler les défaillances de** la vision dans le caisse **de** rendu  
    :::image-end:::  
    
1.  Choisissez une option.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Options du menu Émuler les défaillances de la vision" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       La **vision Émuler les faiblesses des** options de menu  
    :::image-end:::  
    
1.  La fenêtre principale affiche la simulation de l’option choisie appliquée à la page actuelle.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Afficher à l’aide de la simulation **Vision floue**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Afficher à **l’aide de la** simulation de vision floue  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Afficher à l’aide de la simulation **Achromatopsia**" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Afficher à l’aide de la simulation **Achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a>Utiliser le menu Commande  

Vous pouvez également utiliser le **menu Commande** pour accéder aux différentes simulations.  

1.  Sélectionnez `Control` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Menu **Commande**  
    :::image-end:::  
    
1.  Tapez `emulate` , choisissez ce que vous souhaitez simuler et `Enter` choisissez.  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Les différentes options de simulation disponibles dans le menu Commande" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Les différentes options de simulation disponibles dans le **menu Commande**  
    :::image-end:::  
    
> [!IMPORTANT]
> Les **outils Émuler les défauts** de vision simulent des approximations de la façon dont une personne atteinte de chaque défaillance peut voir votre produit.  Chaque personne est différente, par conséquent les défaillances visuelles varient en gravité d’une personne à l’autre.  Pour mieux répondre aux besoins de vos utilisateurs, évitez toute combinaison de couleurs qui peut être un problème.  Les **outils émuler les défaillances de vision** ne sont pas une évaluation complète de l’accessibilité de votre produit.  Au lieu de cela, les **outils émuler** les défaillances de la vision doivent vous donner une bonne première étape pour éviter les problèmes.  

<!-- links -->  

[DevToolsIndex]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analyser les performances d’exécution | Documents Microsoft"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "L’organisation De sensibilisation aux personnes non voyantes"  

[AmfcbMain]: https://www.amfcb.org "American Foundation for the Color Blind (AFCB)"  
