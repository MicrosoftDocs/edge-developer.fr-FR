---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: 19fd59c5dd9f18a681c69250fdcddb22e2796565
ms.sourcegitcommit: f92bf0b50812b43228990b794611daa2144e431c
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2020
ms.locfileid: "10858051"
---
# Fonctionnalités expérimentales  

Vous pouvez utiliser les fonctionnalités expérimentales qui sont toujours en cours de développement dans Microsoft Edge DevTools pour tester et [transmettre des commentaires](#providing-feedback-on-experimental-features) avant chaque sortie.  

Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.  

## Activer les fonctionnalités expérimentales  

Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.  

1.  [Ouvrez devtools][DevtoolsOpen].  
     *   Appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  
1.  Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .  
    *   Appuyez sur `Shift` + `?` .  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  
1.  Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.png":::
       Liste des expériences dans les paramètres de DevTools  
    :::image-end:::  
    
1.  Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.  
1.  Fermez et rouvrez Microsoft Edge DevTools.  

> [!NOTE]
> Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.  Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.  

## Fonctionnalités expérimentales mises en évidence  

Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.  

| Fonctionnalités expérimentales | Version de Microsoft Edge |  
|:--- |:--- |  
| [Activer l’onglet Paramètres de raccourcis clavier personnalisés](#enable-custom-keyboard-shortcuts-settings-tab) | 84 ou version ultérieure |
| [Activer les nouvelles fonctionnalités de débogage de grille CSS](#enable-new-css-grid-debugging-features) | 85 ou version ultérieure |  
| [Activer la prise en charge du déplacement des onglets entre les panneaux](#enable-support-to-move-tabs-between-panels) | 85 ou version ultérieure |  
| [Activer webhint](#enable-webhint) | 85 ou version ultérieure |  

### Activer l’onglet Paramètres de raccourcis clavier personnalisés

Fournit une nouvelle page de **raccourcis** dans les [paramètres de devtools][DevToolsCustomizeSettings] qui permet d’associer des [raccourcis clavier][DevToolsShortcuts] dans le devtools au [code vs][VisualstudioCode].  

Une fois que vous avez activé cette expérience, ouvrez de nouveau [devtools paramètres][DevToolsCustomizeSettings] en appuyant sur `Shift` + `?` .  Accédez à la page nouveau **raccourcis** .  Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.  Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code VS.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code VS" lightbox="./media/experiments-keyboard-shortcut.png":::
   Faire correspondre les raccourcis clavier du DevTools au code VS
:::image-end:::  

Par exemple, dans Windows, le raccourci clavier pour suspendre ou continuer à exécuter un script en [code vs][VisualstudioCodeShortcutsKeyboardWindows] est `F5` .  Avec la valeur prédéfinie **devtools (par défaut)** , ce raccourci est le même dans devtools qu' `F8` avec le **code prédéfini Visual Studio** , ce raccourci est désormais également disponible `F5` .  

### Activer les nouvelles fonctionnalités de débogage de grille CSS  

Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.  Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.png":::
   Fonctionnalité de débogage de grille CSS  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer la prise en charge du déplacement des onglets entre les panneaux  

En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.  De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.  Lorsque cette expérience est sélectionnée, vous pouvez déplacer des outils entre les volets supérieur et inférieur en pointant sur l’onglet, en ouvrant le menu contextuel \ (clic droit sur \) et en sélectionnant **déplacer vers le haut** ou **déplacer vers le bas**.   Cette expérience vous permet de personnaliser la disposition de votre DevTools.  Pour afficher ou masquer le panneau inférieur, appuyez sur `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.png":::
   Déplacement d’un onglet entre les panneaux  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer webhint  

[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.  Cette expérience apporte le commentaire de webhint à DevTools dans le volet des [problèmes][DevtoolsIssues] .  Vous pouvez sélectionner le problème pour voir la documentation relative à la résolution du problème ainsi qu’une liste des ressources affectées sur votre site Web.  Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.png":::
   Commentaires de webhint dans le volet problèmes  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## Fonctionnalités expérimentales antérieures  

*   la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.  

## Fourniture de commentaires sur les fonctionnalités expérimentales  

Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.  

*   Envoyez vos commentaires à l’aide de l’icône de commentaires dans le DevTools  
*   Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   Icône de commentaires dans le Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio pour Windows | Code Visual Studio"  

[WebhintMain]: https://webhint.io "Astuce" 
