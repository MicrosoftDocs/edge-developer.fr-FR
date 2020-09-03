---
description: Examinez et modifiez des animations avec l’inspecteur d’animation Microsoft Edge DevTools.
title: Inspecter des animations
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a74a401edf5331f2dd3c1bf574110241f616d9f6
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992826"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Inspecter des animations   



Examinez et modifiez des animations avec l’inspecteur d’animation Microsoft Edge DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspecteur d’animation" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   inspecteur d’animation  
:::image-end:::  

### Résumé  

*   Capturez des animations en ouvrant l’inspecteur d’animation.  L’inspecteur d’animation détecte et trie automatiquement les animations au sein de groupes.  
*   Examinez les animations en ralentissant chacune d’elles, en reproduisant chacune d’elles ou en consultant le code source.  
*   Modifiez des animations en modifiant le minutage, le délai, la durée ou les décalages d’images clés.  

## Présentation   

L’inspecteur d’animation Microsoft Edge DevTools possède deux objectifs principaux.  

*   Examen des animations.  Vous voulez ralentir, relire ou inspecter le code source d’un groupe d’animations.  
*   Modification des animations.  Vous souhaitez modifier les décalements minutage, délai, durée et image clé d’un groupe d’animations.  La modification Bézier et la modification des images clés ne sont actuellement pas prises en charge.  

L’inspecteur d’animation prend en charge des animations CSS, des transitions CSS et des animations Web.  `requestAnimationFrame` les animations ne sont actuellement pas prises en charge.  

### Qu’est-ce qu’un groupe d’animations?  

Un groupe d’animations est un groupe d’animations qui peut être lié les uns aux autres.  Pour l’instant, le Web n’ayant pas de véritable concept d’animation de groupe, les concepteurs de trajectoire et les développeurs doivent donc composer et temps des animations individuelles pour que les animations s’affichent comme un effet visuel cohérent.  L’inspecteur d’animation prédit quelles animations sont liées en fonction de l’heure de début (sauf retards, etc.).  L’inspecteur d’animation regroupe également les animations côte à côte.  
En d’autres termes, un ensemble d’animations déclenchées dans le même bloc de script est regroupé.  S’il s’agit d’une animation asynchrone, elle est placée dans un groupe séparé.  

## Prise en main  

Il existe deux façons d’ouvrir l’inspecteur d’animation:  

*   Ouvrir le menu **personnaliser et contrôler devtools**  
    1.  Accédez au sous-menu **plus d’outils** .  
    1.  Sélectionnez **animations**:  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animations utilisant le menu principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Animations** utilisant le menu principal  
    :::image-end:::  
        
*   Ouvrir le **menu de commandes**  
    1.  Entrez `Drawer: Show Animations`.  

L’inspecteur d’animation s’ouvre en tant qu’onglet en regard du tiroir de la console.  Dans la mesure où l’inspecteur d’animation est l’onglet tiroir, vous pouvez utiliser l’inspecteur d’animation de n’importe quel panneau DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspecteur d’animation vide" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Inspecteur d’animation vide  
:::image-end:::  

L’inspecteur d’animation est groupé en quatre sections principales \ (ou volets \).  Ce guide fait référence à chaque volet comme suit:  

| | Volet | Description |  
| --- |:--- |:--- |  
| 1 | **Contrôles** | Vous pouvez alors effacer tous les groupes d’animations actuellement capturées ou changer la vitesse du groupe d’animation actuellement sélectionné. |  
| deuxième | **Présentation** | Sélectionnez un groupe d’animations pour l’inspecter et le modifier dans le volet **Détails** . |  
| 3D | **Chronologie** | Interrompez et démarrez une animation à partir de cet emplacement, ou accédez à un point spécifique de l’animation. |  
| n°4 | **Détails** | Inspecter et modifier le groupe d’animations actuellement sélectionné. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspecteur d’animation annoté" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Inspecteur d’animation annoté  
:::image-end:::  

Pour capturer une animation, il vous suffit d’effectuer l’interaction déclenchant l’animation lorsque l’inspecteur d’animation est ouvert.  Si une animation est déclenchée lors du chargement de la page, rechargez la page avec l’inspecteur d’animation ouvert pour détecter l’animation.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Inspecter des animations   

Après avoir capturé une animation, plusieurs méthodes s’offrent à vous pour les relire:  

*   Placez le pointeur de la souris sur la miniature dans le volet **vue d’ensemble** pour en afficher un aperçu.  
*   Sélectionnez le groupe animation dans le volet **vue d’ensemble** \ (pour qu’il s’affiche dans le volet d' **informations** ), puis appuyez sur l’icône **relire** ![ ][ImageReplayButtonIcon] .  L’animation est relues dans la fenêtre d’affichage.  Cliquez sur l’icône **Vitesse d’animation** \ (icônes de ![ Vitesse ][ImageAnimationSpeedButtonsIcon] d’animation \) pour modifier la vitesse d’aperçu du groupe d’animation actuellement sélectionné.  Vous pouvez utiliser la barre verticale rouge pour modifier votre position actuelle.  
*   Cliquez et faites glisser la barre verticale rouge pour faire défiler l’animation d’affichage.  
    
### Afficher les détails d’une animation  

Une fois le groupe d’animations capturé, cliquez dessus dans le volet **vue d’ensemble** pour afficher les détails.  Dans le volet d' **informations** , chaque animation individuelle est affectée à une ligne.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Détails sur le groupe d’animations" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Détails sur le groupe d’animations  
:::image-end:::  

Placez le pointeur sur une animation pour la mettre en surbrillance dans la fenêtre d’affichage.  Cliquez sur l’animation pour la sélectionner dans le panneau **éléments** .  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage  
:::image-end:::  

La section la plus à gauche d’une animation est la définition.  La section à droite, plus ternie représente des itérations.  Par exemple, dans l’illustration suivante, les sections deux et trois représentent des itérations de la section One.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramme d’itérations d’animation" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Diagramme d’itérations d’animation  
:::image-end:::  

Si deux éléments ont la même animation appliquée, l’inspecteur d’animation affecte la même couleur aux éléments.  La couleur est aléatoire et n’a aucune précision.  Par exemple, dans l’illustration suivante, les deux éléments `div.cwccw.earlier` et `div.cwccw.later` ont la même animation \ ( `spinrightleft` \) appliquée, comme les `div.ccwcw.earlier` éléments et `div.ccwcw.later` .  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animations à code couleur" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Animations à code couleur  
:::image-end:::  

## Modifier des animations   

Il existe trois façons de modifier une animation à l’aide de l’inspecteur d’animation.  

*   Durée de l’animation.  
*   Minutage des images clés.  
*   Délai de début  
    
Dans l’illustration suivante, l’animation d’origine est représentée.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animation d’origine avant modification" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Animation d’origine avant modification  
:::image-end:::  

Pour modifier la durée d’une animation, cliquez sur le premier ou le dernier cercle et faites-le glisser.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Durée modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Durée modifiée  
:::image-end:::  

Si l’animation définit des règles d’images clés, celles-ci sont représentées sous forme de cercles intérieurs blancs.  Cliquez sur l’un des éléments suivants pour modifier le minutage de l’image clé.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Image clé modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Image clé modifiée  
:::image-end:::  

Pour ajouter un délai à une animation, cliquez dessus et faites-la glisser n’importe où, à l’exception des cercles.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retard modifié" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Retard modifié  
:::image-end:::  

<!--  
  


-->  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
