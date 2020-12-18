---
description: Simulez un mouvement réduit grâce aux outils de développement.
title: Simulez un mouvement réduit grâce aux outils de développement (CSS est le mouvement réduit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0e5243e01ca6c9344dceffb0bf004dadccc3d4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230788"
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

À l’aide de [Microsoft Edge devtools][DevtoolsIndex], vous pouvez simuler ce paramètre de mouvement réduit sans avoir à modifier votre système d’exploitation.  

1.  Ouvrir le **menu de commandes**.  
    1.  Sélectionnez `Control` + `Shift` + `P` Windows/Linux ou `Command` + `Shift` + `P` MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           **Menu de commandes**  
        :::image-end:::  
        
1.  Tapez `reduced` pour activer ou désactiver la simulation.  Sélectionnez l’option et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de réduction du mouvement de votre choix dans le menu de commandes" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activer ou désactiver le paramètre de **réduction du mouvement** de votre choix dans le menu de **commandes**  
    :::image-end:::  
    
1.  Actualisez la page active pour tester si vos animations sont désactivées ou visibles.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "préféré-réduction du mouvement | MDN"  
