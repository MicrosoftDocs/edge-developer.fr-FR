---
description: Forcez Microsoft Edge DevTools en mode Aperçu du jeu de couleurs.
title: Forcer Microsoft Edge DevTools en mode Aperçu du jeu de couleurs (CSS Préfère le jeu de couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1cdc9601e9e6fea1f6921c6cc40a1ed8232a0da8
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519148"
---
# <a name="dark-or-light-color-scheme-simulation"></a>Simulation de jeu de couleurs foncées ou claires  

Les systèmes d'exploitation peuvent afficher n'importe quelle application dans des couleurs plus foncées ou plus claires.  Le fait de disposer d'un produit web avec un thème clair dans un système d'exploitation en mode sombre constitue un problème d'accessibilité pour certains utilisateurs.  Sur le web, vous pouvez utiliser la requête multimédia CSS [prefers-color-scheme][MDNPrefersColorScheme] pour détecter si les utilisateurs préfèrent afficher votre produit dans un schéma de couleurs plus sombre ou plus claire.  Utilisez [Microsoft Edge DevTools pour][DevtoolsIndex] simuler un changement de mode sombre en mode clair sans avoir à modifier l'intégralité du système d'exploitation.  

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
    > Il suffit de taper ou de ne pas révéler l'outil qui vous permet de le faire, car il existe également un moyen de choisir un thème `dark` `light` pour [DevTools.][DevtoolsCustomizeDarkTheme]  Si vous vous demandez ce qu'il faut choisir, assurez-vous que vous choisissez un élément de **menu** de rendu, et non un **élément de** menu Apparence.  

1.  Après avoir choisi un jeu de couleurs, actualisez le document actuel pour afficher le mode simulé.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Mode lumineux simulé à l'intérieur de Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Mode lumineux simulé à l'intérieur de Microsoft Edge DevTools  
    :::image-end:::  
    
    Affichez et modifiez votre CSS comme n'importe quelle autre page web.  Pour plus d'informations, [accédez à La mise en place de l'affichage et de la modification de CSS.][DevtoolsCssIndex]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Activer le thème foncé dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsCssIndex]: ../css/index.md "Mise en place de l'affichage et de la modification des | Documents Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
