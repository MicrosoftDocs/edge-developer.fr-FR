---
description: Inspectez et modifiez les animations à l’aide de l’inspecteur d’animation Microsoft Edge DevTools.
title: Inspecter les animations
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 742096f13179de2ad1a95dc9fa62d2bbf3d7c226
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397733"
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

# <a name="inspect-animations"></a>Inspecter les animations  

Inspectez et modifiez les animations à l’aide de l’inspecteur d’animation Microsoft Edge DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspecteur d’animation" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   inspecteur d’animation  
:::image-end:::  

### <a name="summary"></a>Résumé  

*   Capturez les animations en ouvrant l’Inspecteur d’animation.  L’Inspecteur d’animation détecte et trie automatiquement les animations en groupes.  
*   Inspectez les animations en ralentissant chacune d’elles, en relisant chacune d’elles ou en visualxant le code source.  
*   Modifiez les animations en modifiant le minutage, le délai, la durée ou les décalages d’images clés.  

## <a name="overview"></a>Vue d'ensemble  

L’inspecteur d’animation Microsoft Edge DevTools a deux objectifs principaux.  

*   Inspection des animations.  Vous souhaitez ralentir, relire ou inspecter le code source d’un groupe d’animations.  
*   Modification des animations.  Vous souhaitez modifier le minutage, le délai, la durée ou les décalages d’images clés d’un groupe d’animations.  La modification de Bézier et la modification d’images clés ne sont actuellement pas pris en charge.  

L’Inspecteur d’animation prend en charge les animations CSS, les transitions CSS et les animations web.  `requestAnimationFrame` les animations ne sont actuellement pas pris en charge.  

### <a name="what-is-an-animation-group"></a>Qu’est-ce qu’un groupe d’animations ?  

Un groupe d’animations est un groupe d’animations qui peuvent être liées les unes aux autres.  Pour l’instant, le web n’a pas de concept réel d’animation de groupe, de sorte que les concepteurs de mouvement et les développeurs doivent composer et timer des animations individuelles afin que les animations s’restituer comme un seul effet visuel cohérent.  L’Inspecteur d’animations prévoit les animations qui sont liées en fonction de l’heure de début \(à l’exclusion des retards, et ainsi de suite\).  L’Inspecteur d’animations groupe également les animations côte à côte.  
En d’autres termes, un ensemble d’animations qui sont toutes déclenchées dans le même bloc de scripts sont regroupées.  Si une animation est asynchrone, elle est placée dans un groupe distinct.  

## <a name="get-started"></a>Prise en main  

Il existe deux façons d’ouvrir l’Inspecteur d’animation :  

*   Ouvrir le menu Personnaliser et contrôler **DevTools**  
    1.  Accédez au **sous-menu Outils** Plus.  
    1.  Choisissez **Animations**:  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animations à l’aide du menu principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Animations à l’aide** du menu principal  
    :::image-end:::  
        
*   Ouvrir le **menu Commande**  
    1.  Entrez `Drawer: Show Animations`.  

L’Inspecteur d’animation s’ouvre à côté de **l’outil Console.**  Étant donné que l’Inspecteur d’animation est un outil DevTools, vous pouvez utiliser l’Inspecteur d’animation à partir de n’importe quel panneau DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspecteur d’animation vide" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Inspecteur d’animation vide  
:::image-end:::  

L’Inspecteur d’animation est regroupé en quatre sections principales \(ou volets\).  Ce guide fait référence à chaque volet comme suit :  

| Index | Volet | Description |  
|:--- |:--- |:--- |  
| 1 | **Contrôles** | À partir de là, vous pouvez effacer tous les groupes d’animations actuellement capturés ou modifier la vitesse du groupe d’animations actuellement sélectionné. |  
| 2 | **Vue d'ensemble** | Choisissez un groupe d’animations ici pour l’inspecter et le modifier dans le **volet d’informations.** |  
| 3 | **Chronologie** | Suspendez et démarrez une animation à partir d’ici, ou faites un saut vers un point spécifique de l’animation. |  
| 4 | **Détails** | Inspectez et modifiez le groupe d’animations actuellement sélectionné. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspecteur d’animation annotée" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Inspecteur d’animation annotée  
:::image-end:::  

Pour capturer une animation, il vous suffit d’effectuer l’interaction qui déclenche l’animation lorsque l’Inspecteur d’animation est ouvert.  Si une animation est déclenchée lors du chargement de la page, actualisez la page avec l’Inspecteur d’animation ouvert pour détecter l’animation.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a>Inspecter les animations  

Une fois que vous avez capturé une animation, vous pouvez la relire de plusieurs façons :  

*   Pointez sur la miniature dans **le** volet Vue d’ensemble pour en afficher un aperçu.  
*   Choisissez le groupe **** d’animations dans le volet Vue **** d’ensemble \(afin qu’il s’affiche dans le volet d’informations\) et choisissez l’icône de relecture **\(** icône de relecture ![ ][ImageReplayButtonIcon] \).  L’animation est relecture dans la vue.  Choisissez les **icônes de vitesse d’animation** \( icônes de vitesse d’animation \) pour modifier la vitesse d’aperçu du groupe d’animations ![ actuellement ][ImageAnimationSpeedButtonsIcon] sélectionné.  Vous pouvez utiliser la barre verticale rouge pour modifier votre position actuelle.  
*   Choisissez et faites glisser la barre verticale rouge pour nettoyer l’animation de la vue.  
    
### <a name="view-animation-details"></a>Afficher les détails de l’animation  

Après avoir capturé un groupe d’animations, choisissez-le dans le volet Vue d’ensemble pour afficher les détails. ****  Dans le **volet Détails,** chaque animation individuelle est affectée à une ligne.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Détails du groupe d’animations" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Détails du groupe d’animations  
:::image-end:::  

Pointez sur une animation pour la surligner dans la vue.  Choisissez l’animation pour la sélectionner dans **l’outil Éléments.**  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Pointer sur l’animation pour la surligner dans la vue" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Pointer sur l’animation pour la surligner dans la vue  
:::image-end:::  

La section la plus sombre et la plus à gauche d’une animation est la définition.  La section droite, plus fondue, représente des itérations.  Par exemple, dans la figure suivante, les sections 2 et 3 représentent les itérations de la première section.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramme des itérations d’animation" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Diagramme des itérations d’animation  
:::image-end:::  

Si deux éléments ont la même animation appliquée, l’Inspecteur d’animation affecte la même couleur aux éléments.  La couleur est aléatoire et n’a aucune signification.  Par exemple, dans la figure suivante, les deux éléments ont la même `div.cwccw.earlier` `div.cwccw.later` animation \( \) appliquée, tout comme les `spinrightleft` `div.ccwcw.earlier` éléments et les `div.ccwcw.later` éléments.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animations codées en couleur" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Animations codées en couleur  
:::image-end:::  

## <a name="modify-animations"></a>Modifier les animations  

Il existe trois façons de modifier une animation avec l’Inspecteur d’animation.  

*   Durée de l’animation.  
*   Minutage des images clés.  
*   Délai de début.  
    
Dans la figure suivante, l’animation d’origine est représentée.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animation d’origine avant modification" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Animation d’origine avant modification  
:::image-end:::  

Pour modifier la durée d’une animation, choisissez et faites glisser le premier ou le dernier cercle.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Durée modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Durée modifiée  
:::image-end:::  

Si l’animation définit des règles d’image clé, celles-ci sont représentées en tant que cercles internes blancs.  Choisissez et faites glisser l’une d’entre elles pour modifier le minutage de l’images clés.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Images clés modifiées" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Images clés modifiées  
:::image-end:::  

Pour ajouter un délai à une animation, choisissez-la et faites-la glisser n’importe où à l’exception des cercles.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retard modifié" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Retard modifié  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
