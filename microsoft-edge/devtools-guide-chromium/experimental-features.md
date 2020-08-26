---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: 4c2541615700f2c637f293ee6a3fbacd9ccbc43a
ms.sourcegitcommit: 5ed791ed5423a3a4b03e8a1c7927f026307a6673
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2020
ms.locfileid: "10960717"
---
# Fonctionnalités expérimentales  

Vous pouvez utiliser les fonctionnalités expérimentales qui sont toujours en cours de développement dans Microsoft Edge DevTools pour tester et [transmettre des commentaires](#providing-feedback-on-experimental-features) avant chaque sortie.  

Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.  

## Activer les fonctionnalités expérimentales  

Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.  

1.  [Ouvrez devtools][DevtoolsOpen].  
     *   Sélectionnez `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  
1.  Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .  
    *   Sélectionnez `Shift` + `?` .  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  
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
| [Activer la console réseau](#enable-network-console) | 85 ou version ultérieure |  
| [Activer la visionneuse de commandes sources](#enable-source-order-viewer) | 86 ou version ultérieure |  

### Activer l’onglet Paramètres de raccourcis clavier personnalisés  

Propose une nouvelle page de **raccourcis** dans les [paramètres de devtools][DevToolsCustomizeSettings] qui permet d’associer des [raccourcis clavier][DevToolsShortcuts] dans devtools au [code Microsoft Visual Studio][VisualstudioCode].  

Une fois que vous avez activé l’expérience, rouvrez les [paramètres de devtools][DevToolsCustomizeSettings] à l’aide de la sélection `Shift` + `?` .  Accédez à la page nouveau **raccourcis** .  Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.  Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code Visual Studio.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="./media/experiments-keyboard-shortcut.png":::
   Faire correspondre les raccourcis clavier du DevTools au code Visual Studio  
:::image-end:::  

Par exemple, dans Windows, le raccourci clavier pour suspendre ou continuer à exécuter un script dans le [code Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] est `F5` .  Avec la valeur prédéfinie **devtools (par défaut)** , le même raccourci dans devtools est `F8` .  Le raccourci est également associé au **code Visual Studio** prédéfini `F5` .  

### Activer les nouvelles fonctionnalités de débogage de grille CSS  

Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.  Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.png":::
   Fonctionnalité de débogage de grille CSS  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer la prise en charge du déplacement des onglets entre les panneaux  

En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.  De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.  Lorsque vous sélectionnez l’expérience, vous pouvez déplacer des outils entre les volets supérieur et inférieur en pointant sur l’onglet, en ouvrant le menu contextuel \ (clic droit sur \), puis en **haut** ou **en bas**.   Cette expérience vous permet de personnaliser la disposition de votre DevTools.  Pour afficher ou masquer le panneau inférieur, sélectionnez `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.png":::
   Déplacement d’un onglet entre les panneaux  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer webhint  

[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.  L’expérience [webhint][WebhintMain] a pour résultat le devtools de commentaires webhint dans le volet [problèmes][DevtoolsIssues] .  Vous pouvez sélectionner le problème pour voir la documentation relative à la résolution du problème ainsi qu’une liste des ressources affectées sur votre site Web.  Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.png":::
   Commentaires de webhint dans le volet **problèmes**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer la console réseau  

**Network console** est le titre d’une expérience visant à faire des requêtes réseau synthétiques sur http.  Vous pouvez utiliser l’expérience de la **console réseau** pour envoyer des demandes d’API Web.  

Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.  Pour utiliser la console réseau:  

1.  Ouvrez le volet **réseau** .  
1.  Recherchez la demande réseau que vous souhaitez modifier et renvoyer.  
1.  Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier, puis relire**.  
1.  Lorsque la **console réseau** s’ouvre, modifiez les informations de requête réseau.  
1.  Sélectionnez **Envoyer**.  

:::image type="complex" source="./media/network-network-console.png" alt-text="Console réseau dans le tiroir de la console" lightbox="./media/network-network-console.png":::
   **Console réseau** dans le tiroir de la **console**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### Activer la visionneuse de commandes sources  

La **visionneuse de commandes source** est le titre d’une expérience permettant d’afficher l’ordre des éléments dans la source de la page.  Vous pouvez utiliser l’expérience de la **visionneuse de commandes sources** pour détecter des problèmes d’accessibilité dans vos pages, car l’ordre de l’affichage à l’écran risque de différer de l’ordre de la source, ce qui déconcerte les utilisateurs de lecteurs d’écran.  

Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.  Pour utiliser la visionneuse de commandes source:  

1.  Ouvrir le volet des **éléments** .  
1.  Ouvrez le volet **accessibilité** dans le panneau du tiroir.  
1.  Dans la section **visionneuse de commandes sources** , activez la case à cocher **afficher l’ordre source** .  
1.  Mettez en surbrillance un élément HTML pour afficher une superposition de l’ordre dans la source de la page.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet accessibilité" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Visionneuse de commandes source** dans le volet **accessibilité**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Fonctionnalités expérimentales antérieures  

*   la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.  

## Fourniture de commentaires sur les fonctionnalités expérimentales  

Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.  

*   Envoyez vos commentaires à l’aide de l’icône **Envoyer des commentaires** dans le devtools  
*   Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Icône Envoyer des commentaires dans le Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   Icône **Envoyer des commentaires** dans le Microsoft Edge devtools  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Code Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio pour Windows | Code Microsoft Visual Studio"  

[WebhintMain]: https://webhint.io "Astuce" 
