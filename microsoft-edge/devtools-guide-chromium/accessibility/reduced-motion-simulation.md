---
description: Simulez un mouvement réduit à l’aide des outils de développement.
title: Simuler un mouvement réduit à l’aide des outils de développement (CSS préfère le mouvement réduit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7244c2e80bbf9070214b6abd02583792c785953c
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597055"
---
# <a name="reduced-motion-simulation"></a>Simulation de mouvement réduit  

L’animation dans les produits web peut être un problème d’accessibilité.  Les systèmes d’exploitation traitent ce problème en incluant une option pour désactiver les animations afin d’éviter toute confusion chez l’utilisateur et d’éventuels problèmes de santé, tels que le déclenchement de crises.  

Sur une page web, [][MDNPrefersReducedMotion] vous pouvez utiliser la requête multimédia CSS à mouvement réduit par préférence pour détecter si l’utilisateur préfère afficher des animations.  Encapsulez ensuite votre code d’animation dans un test, pour exécuter des animations de manière conditionnable.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Ensuite, testez votre code, comme suit.

Pour simuler le paramètre de mouvement réduit du système d’exploitation, sans avoir à modifier le paramètre de votre système d’exploitation :

1.  Ouvrez **le menu Commande.**  
    1.  Sélectionnez `Control` + `Shift` + `P` sur Windows/Linux `Command` + `Shift` + `P` ou sur macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Menu **Commande**  
        :::image-end:::  
        
1.  Tapez `reduced` , pour activer et désactiver la simulation.  Choisissez l’option et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de mouvement réduit préféré à partir du menu Commande" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activer ou désactiver le paramètre de mouvement **réduit préféré** à partir du **menu Commande**  
    :::image-end:::  
    
1.  Actualisez la page web et vérifiez si vos animations s’exécutent.


## <a name="see-also"></a>Articles associés

* [Vérifiez que la page est utilisable](test-reduced-ui-motion.md) avec l’animation de l’interface utilisateur désactivée : une démonstration à l’aide d’une page de démonstration, avec des explications.

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
