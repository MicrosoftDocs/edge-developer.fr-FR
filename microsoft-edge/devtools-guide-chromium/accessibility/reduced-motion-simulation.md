---
description: Simulez un mouvement réduit à l’aide des outils de développement.
title: Simuler un mouvement réduit à l’aide des outils de développement (CSS préfère le mouvement réduit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 29cdbd7492665e819315910b3f743d444470cc12
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397866"
---
# <a name="reduced-motion-simulation"></a>Simulation de mouvement réduit  

L’animation dans les produits web peut être un problème d’accessibilité.  Les systèmes d’exploitation traitent le problème en incluant une option pour désactiver les animations afin d’éviter toute confusion chez l’utilisateur et d’éventuels problèmes liés à l’état, tels que le déclenchement de crises.  Sur le web, vous pouvez utiliser la requête multimédia CSS à mouvement réduit pour détecter si les [utilisateurs][MDNPrefersReducedMotion] préfèrent ne pas exécuter ou afficher d’animations.  Dans votre produit, vous pouvez encapsuler votre code d’animation dans un test afin d’éviter que des animations ne s’affichent pour les utilisateurs concernés.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

À [l’Microsoft Edge DevTools,][DevtoolsIndex]vous pouvez simuler ce paramètre de mouvement réduit sans avoir à modifier votre système d’exploitation.  

1.  Ouvrez **le menu Commande.**  
    1.  Sélectionnez `Control` + `Shift` + `P` sur Windows/Linux `Command` + `Shift` + `P` ou sur macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Menu **Commande**  
        :::image-end:::  
        
1.  Tapez `reduced` , pour activer et désactiver la simulation.  Choisissez l’option et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de mouvement réduit préféré à partir du menu Commande" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activer ou désactiver le paramètre de mouvement **réduit préféré** à partir du **menu Commande**  
    :::image-end:::  
    
1.  Actualisez la page actuelle pour tester si vos animations sont désactivées ou visibles.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
