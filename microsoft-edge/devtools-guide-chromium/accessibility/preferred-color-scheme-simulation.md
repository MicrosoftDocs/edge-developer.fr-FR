---
title: Forcez Microsoft Edge DevTools en mode d’aperçu du jeu de couleurs (CSS préfère le modèle de couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: a83284b676ad388114a4a0ddb7ebdf2203ebcb90
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758081"
---
# Simulation de jeu de couleurs sombre ou léger  

Les systèmes d’exploitation peuvent afficher n’importe quelle application en couleurs plus sombres ou plus claires.  Le fait de disposer d’un produit Web comportant un thème clair dans un système d’exploitation en mode foncé est un réseau qui peut être un problème d’accessibilité pour certains utilisateurs.  Sur le Web, vous pouvez utiliser la requête de médias CSS de [jeu de couleurs][MDNPrefersColorScheme] pour détecter si les utilisateurs préfèrent voir votre produit dans le cadre d’un jeu de couleurs plus sombre ou plus clair.  Utilisez [Microsoft Edge devtools][DevtoolsGuideChromiumMain] pour simuler une modification du mode sombre au mode clair sans avoir à modifier l’intégralité du système d’exploitation.  

1.  Ouvrir le **menu de commandes**.  
    1.  Appuyez `Control` + `Shift` + `P` sur Windows ou `Command` + `Shift` + `P` sur MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           **Menu de commandes**  
        :::image-end:::   
        
1.  Tapez `emulate color` , sélectionnez **émuler des feuilles de style CSS préféré-jeu de couleurs: Dark** ou **émuler des feuilles de style CSS préféré-couleur: clair** , puis appuyer `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Sélection des jeux de couleurs dans le menu de commandes" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Sélection des jeux de couleurs dans le menu de **commandes**  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Il suffit de taper `dark` ou de `light` ne pas afficher l’outil approprié, car il existe également un moyen de [choisir un thème pour devtools][DevtoolsGuideChromiumCustomizeDarkTheme].  Si vous vous demandez ce qu’il faut choisir, assurez-vous de sélectionner un élément de menu de **rendu** , et non un élément de menu **apparence** .  

1.  Après avoir sélectionné un modèle de couleurs, rechargez le document actuel pour afficher le mode simulé.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Mode Light simulé dans Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Mode Light simulé dans Microsoft Edge DevTools  
    :::image-end:::  
    
    Affichez et modifiez votre CSS comme n’importe quelle autre page Web.  Pour plus d’informations, voir [commencer à afficher et modifier des feuilles CSS][DevtoolsGuideChromiumCssIndex].  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) Microsoft | Documents Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Activer un thème foncé dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "préférence-jeu de couleurs | MDN"  
