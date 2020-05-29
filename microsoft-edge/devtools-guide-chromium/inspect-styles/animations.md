---
title: Inspecter des animations
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566210"
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

> ##### Figure1  
> Inspecteur d’animation  
> ![inspecteur d’animation][ImageAnimationInspector]  

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
        
        > ##### Figure 2  
        > Animations via le menu principal  
        > ![Animations via le menu principal][ImageAnimationsViaMainMenu]  
        
*   Ouvrir le **menu de commandes**  
    1.  Entrez `Drawer: Show Animations`.  

L’inspecteur d’animation s’ouvre en tant qu’onglet en regard du tiroir de la console.  Dans la mesure où l’inspecteur d’animation est l’onglet tiroir, vous pouvez utiliser l’inspecteur d’animation de n’importe quel panneau DevTools.  

> ##### Figure3  
> Inspecteur d’animation vide  
> ![Inspecteur d’animation vide][ImageEmptyAnimationInspector]  

L’inspecteur d’animation est groupé en quatre sections principales \ (ou volets \).  Ce guide fait référence à chaque volet comme suit:  

| | Volet | Description |  
| --- |:--- |:--- |  
| 1 | **Contrôles** | Vous pouvez alors effacer tous les groupes d’animations actuellement capturées ou changer la vitesse du groupe d’animation actuellement sélectionné. |  
| deuxième | **Présentation** | Sélectionnez un groupe d’animations pour l’inspecter et le modifier dans le volet **Détails** . |  
| 3D | **Chronologie** | Interrompez et démarrez une animation à partir de cet emplacement, ou accédez à un point spécifique de l’animation. |  
| n°4 | **Détails** | Inspecter et modifier le groupe d’animations actuellement sélectionné. |  

> ##### Figure 4  
> Inspecteur d’animation annoté  
> ![Inspecteur d’animation annoté][ImageAnnotatedAnimationInspector]  

Pour capturer une animation, il vous suffit d’effectuer l’interaction déclenchant l’animation lorsque l’inspecteur d’animation est ouvert.  Si une animation est déclenchée lors du chargement de la page, rechargez la page avec l’inspecteur d’animation ouvert pour détecter l’animation.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Inspecter des animations   

Après avoir capturé une animation, plusieurs méthodes s’offrent à vous pour les relire:  

*   Placez le pointeur de la souris sur la miniature dans le volet **vue d’ensemble** pour en afficher un aperçu.  
*   Sélectionnez le groupe animation dans le volet **vue d’ensemble** \ (pour qu’il s’affiche dans le volet d' **informations** ), puis appuyez sur l’icône **réexécuter** l' ![ icône de lecture ][ImageReplayButtonIcon] .  L’animation est relues dans la fenêtre d’affichage.  Cliquez sur l’icône de vitesse de l' **animation vitesse d'** animation ![ ][ImageAnimationSpeedButtonsIcon] pour modifier la vitesse d’aperçu du groupe d’animation actuellement sélectionné.  Vous pouvez utiliser la barre verticale rouge pour modifier votre position actuelle.  
*   Cliquez et faites glisser la barre verticale rouge pour faire défiler l’animation d’affichage.  

### Afficher les détails d’une animation  

Une fois le groupe d’animations capturé, cliquez dessus dans le volet **vue d’ensemble** pour afficher les détails.  Dans le volet d' **informations** , chaque animation individuelle est affectée à une ligne.  

> ##### Figure 5  
> Détails sur le groupe d’animations  
> ![Détails sur le groupe d’animations][ImageAnimationGroupDetails]  

Placez le pointeur sur une animation pour la mettre en surbrillance dans la fenêtre d’affichage.  Cliquez sur l’animation pour la sélectionner dans le panneau **éléments** .  

> ##### Figure 6  
> Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage  
> ![Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage][ImageHoverOverAnimationHighlightViewport]  

La section la plus à gauche d’une animation est la définition.  La section à droite, plus ternie représente des itérations.  Par exemple, dans la [figure 7](#figure-7), les sections deux et trois représentent des itérations de la section One.  

> ##### Figure 7  
> Diagramme d’itérations d’animation  
> ![Diagramme d’itérations d’animation][ImageDiagramAnimationIterations]  

Si deux éléments ont la même animation appliquée, l’inspecteur d’animation affecte la même couleur aux éléments.  La couleur est aléatoire et n’a aucune précision.  Par exemple, dans [figure 8](#figure-8) les deux éléments `div.cwccw.earlier` et `div.cwccw.later` ont la même animation \ ( `spinrightleft` \) appliquée, comme les `div.ccwcw.earlier` éléments et `div.ccwcw.later` .  

> ##### Figure8  
> Animations à code couleur  
> ![Animations à code couleur][ImageColorCodedAnimations]  

## Modifier des animations   

Il existe trois façons de modifier une animation à l’aide de l’inspecteur d’animation:  

*   Durée de l’animation.  
*   Minutage des images clés.  
*   Délai de début  

Pour cette section, supposez que la [figure 9](#figure-9) représente l’animation d’origine:  

> ##### Figure9  
> Animation d’origine avant modification  
> ![Animation d’origine avant modification][ImageOriginalAnimationBeforeModification]  

Pour modifier la durée d’une animation, cliquez sur le premier ou le dernier cercle et faites-le glisser.  

> ##### Figure10  
> Durée modifiée  
> ![Durée modifiée][ImageModifiedDuration]  

Si l’animation définit des règles d’images clés, celles-ci sont représentées sous forme de cercles intérieurs blancs.  Cliquez sur l’un des éléments suivants pour modifier le minutage de l’image clé.  

> ##### Figure11  
> Image clé modifiée  
> ![Image clé modifiée][ImageModifiedKeyframe]  

Pour ajouter un délai à une animation, cliquez dessus et faites-la glisser n’importe où, à l’exception des cercles.  

> ##### Figure12  
> Retard modifié  
> ![Retard modifié][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Figure 1: inspecteur d’animation"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Figure 2: animations via le menu principal"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Figure 3: inspecteur d’animation vide"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Figure 4: inspecteur d’animation annoté"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Figure 5: détails sur le groupe d’animations"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Figure 6: survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage"  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Figure 7: diagramme d’itérations d’animation"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Figure 8: animations à code couleur"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Figure 9: animation d’origine avant modification"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Figure 10: durée de modification"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Figure 11: image clé modifiée"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Figure 12: délai modifié"  

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
