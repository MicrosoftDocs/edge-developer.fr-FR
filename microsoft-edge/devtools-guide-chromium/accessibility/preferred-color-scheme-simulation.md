---
description: Forcez Microsoft Edge DevTools en mode Aperçu du jeu de couleurs.
title: Forcer Microsoft Edge DevTools en mode Aperçu du jeu de couleurs (CSS Prefers Color Scheme)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: dc2911ce7a7fcbeef7763099541822b5cd6cf053
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597065"
---
# <a name="dark-or-light-color-scheme-simulation"></a>Simulation de jeu de couleurs foncées ou claires  

De nombreux systèmes d’exploitation ont un moyen d’afficher n’importe quelle application dans des couleurs plus foncées ou plus claires.  Le fait de disposer d’un produit web avec un thème clair dans un système d’exploitation en mode sombre constitue un problème d’accessibilité pour certains utilisateurs.  

Pour une page web, vous pouvez utiliser la requête multimédia CSS [prefers-color-scheme][MDNPrefersColorScheme] pour détecter si l’utilisateur préfère afficher votre produit dans un schéma de couleurs plus sombre ou plus clair.  Ensuite, pour tester le résultat, utilisez [Microsoft Edge DevTools][DevtoolsIndex] pour simuler un changement de mode sombre en mode clair, sans avoir à modifier le paramètre pour l’ensemble de votre système d’exploitation.  

**Pour émuler un thème foncé ou clair :**

1.  Ouvrez **le menu Commande.**  
    1.  Sélectionnez `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\).  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Menu **Commande**  
        :::image-end:::  
        
1.  Type `emulate color` , choose either Emulate **CSS prefers-color-scheme: dark** or Emulate **CSS prefers-color-scheme: light** and then select `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Option de modèle de couleurs du menu Commande" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Option de modèle de **couleurs** du menu Commande  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Il suffit de taper ou de ne pas révéler l’outil qui vous permet de le faire, car il existe également un moyen de choisir un thème pour `dark` `light` [DevTools.][DevtoolsCustomizeDarkTheme]  Si vous vous demandez ce qu’il faut choisir, assurez-vous que vous choisissez un élément de **menu** de rendu, et non un **élément de** menu Apparence.  

1.  Après avoir choisi un jeu de couleurs, actualisez le document actuel pour afficher le mode simulé.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Mode lumière simulé à l’intérieur Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Mode lumière simulé à l’intérieur Microsoft Edge DevTools  
    :::image-end:::  
    
    Affichez et modifiez votre CSS comme n’importe quelle autre page web.  Pour plus d’informations, [accédez à Commencer à afficher et modifier les CSS.][DevtoolsCssIndex]  


## <a name="see-also"></a>Articles associés

* [Vérifier les problèmes de contraste avec le thème foncé et le thème clair](test-dark-mode.md)


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Activer le thème foncé dans Microsoft Edge devTools | Documents Microsoft"
[DevtoolsCssIndex]: ../css/index.md "Commencer à afficher et modifier les | Documents Microsoft"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
