---
title: Forcez Microsoft Edge DevTools en mode d’aperçu du jeu de couleurs (CSS préfère le modèle de couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 94c5369f0eb35059933be7f6202a4f64450629cd
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758077"
---
# Simulation de mouvement réduite  

Une animation dans des produits Web est susceptible de résoudre un problème d’accessibilité.  Les systèmes d’exploitation traitent le problème en incluant une option de désactivation des animations pour éviter toute confusion et risque de problèmes liés à la santé tels que les crises de déclenchement.  Sur le Web, vous pouvez utiliser la requête de média CSS [-Reduced-Motion][MDNPrefersReducedMotion] pour détecter si les utilisateurs préfèrent ne voir aucune animation.  Dans votre produit, vous pouvez encapsuler votre code d’animation dans un test pour éviter d’avoir des animations destinées aux utilisateurs concernés.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
  animation: none;
  }
}
```  

À l’aide de [Microsoft Edge devtools][DevtoolsGuideChromiumMain], vous pouvez simuler ce paramètre de mouvement réduit sans avoir à modifier votre système d’exploitation.  

1.  Ouvrir le **menu de commandes**.  
    1.  Appuyez `Control` + `Shift` + `P` sur Windows ou `Command` + `Shift` + `P` sur MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           **Menu de commandes**  
        :::image-end:::   
        
1.  Tapez `reduced` pour activer ou désactiver la simulation.  Sélectionnez l’option et appuyez sur `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de réduction du mouvement de votre choix dans le menu de commandes" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activer ou désactiver le paramètre de **réduction du mouvement** de votre choix dans le menu de **commandes**  
    :::image-end:::  
    
1.  Actualisez la page active pour tester si vos animations sont désactivées ou visibles.  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Figure 1: menu de commandes"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Figure 2: basculer la réduction de la vidéo à partir de la palette de commandes"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) Microsoft | Documents Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "préféré-réduction du mouvement | MDN"  