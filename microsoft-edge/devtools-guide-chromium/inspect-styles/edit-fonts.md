---
description: Découvrez comment modifier les styles et paramètres de police CSS à l’aide du volet Styles dans Microsoft Edge DevTools.
title: Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
no-loc:
- Enable new font editor tool within the Styles pane
ms.openlocfilehash: 5d9074ca65f9cb98662a1bc181f70ead4c4232e1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439492"
---
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a>Modifier les styles et paramètres de police CSS dans le volet Styles  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

La typographie sur le web est une partie importante de l’expérience utilisateur.  Vous souhaitez vous assurer que vous respectez les directives de la marque d’entreprise et que votre contenu s’affiche comme prévu sur différents appareils.  Le texte doit être facile à lire à l’aide de la taille et de la hauteur de ligne.  Les utilisateurs peuvent re tailler des polices pour répondre à des besoins individuels.  Lorsque des polices spécifiques ne sont pas disponibles sur un appareil utilisateur, vous devez fournir des options de police de base.  

CSS offre une meilleure prise en charge de la typographie au cours des dernières années.  Des dizaines d’unités CSS différentes sont disponibles pour définir la taille du texte.  Vous disposez également de plusieurs propriétés CSS qui affectent la taille de police, l’espacement, la hauteur de ligne et d’autres fonctionnalités typographiques.  

Pour faciliter l’travail avec la typographie, un **éditeur** de polices visuel se trouve désormais dans le **volet Styles.**  Vous pouvez modifier vos paramètres de police et les modifications sont restituer immédiatement dans le navigateur.  Tout cela sans connaissances approfondies du CSS.  

Actuellement, **Enable new font editor tool within the Styles pane** la fonctionnalité est expérimentale et vous devez [l’activer pour Microsoft Edge outils de développement.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  

Toute CSS dans le volet **Styles,** définitions de police ou styles inline, affiche automatiquement une icône qui ouvre l’éditeur de **polices visuel.**  Pour ouvrir visual **Font Editor,** sélectionnez l’icône **Éditeur de** polices.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Icône du volet Styles pour modifier les paramètres de police" lightbox="../media/font-editor-icon.msft.png":::
         Icône du volet **Styles** pour modifier les paramètres de police  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles" lightbox="../media/font-editor-open.msft.png":::
         Éditeur **de polices** ouvert en haut du volet **Styles**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Tous les champs de l’éditeur **de police** visuel sont remplis à partir des valeurs du CSS dans le **volet Styles.**  Par exemple, la définition est définie sur dans le volet Styles, de sorte que le champ de texte de la hauteur de ligne s’affiche et que la zone de texte d’unité `line-height` `160%` **** `160` s’affiche. `%`  En outre, le curseur est automatiquement définie pour correspondre aux valeurs du champ de texte.  

**L’éditeur de** polices se compose de deux parties : le sélecteur de la famille de polices et l’éditeur de propriétés CSS.  

## <a name="the-font-family-selector"></a>Sélecteur de la famille de polices  

Le sélecteur de la famille de polices est la partie supérieure de l’éditeur **de polices visuel.**  Pour choisir les polices de la règle CSS, dans l’éditeur CSS, utilisez le sélecteur **de** la famille de polices.  Vous pouvez choisir des polices principales et de base pour chaque règle CSS.  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles avec le sélecteur de la famille de polices mis en évidence" lightbox="../media/font-editor-font-family.msft.png":::
   Éditeur **de polices** ouvert en haut du volet **Styles** avec le sélecteur **de** la famille de polices mis en évidence  
:::image-end:::  

Utilisez la **liste finale Famille** de polices pour choisir parmi une liste de polices.  Les polices sont organisées en quatre groupes.  

1.  Polices calculées, qui sont les polices disponibles dans la feuille de style dans le **volet Styles.**  
1.  Polices système, qui sont les polices disponibles sur le système d’exploitation actuel.  
1.  Familles de polices génériques, `serif` telles que ou `sans-serif` .  
1.  Valeurs globales, telles `inherit` `initial` que , et `unset` .  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles avec le sélecteur de la famille de polices mis en évidence" lightbox="../media/font-editor-font-family-list.msft.png":::
   Éditeur **de polices** ouvert en haut du volet **Styles** avec le sélecteur **de** la famille de polices mis en évidence  
:::image-end:::  

Une fois que vous avez choisi une police, un autre menu déroulant s’affiche pour que vous choisissiez des polices de fallback.  Vous pouvez choisir jusqu’à huit polices de fallback.  Pour supprimer une police, sélectionnez **l’icône Supprimer la famille de polices.**  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> Si vous choisissez une valeur globale pour la famille de polices, vous n’obtenez pas une autre dropdown, car il n’y a pas de retour pour elle dans CSS.  

## <a name="the-css-properties-editor"></a>Éditeur de propriétés CSS  

Vous pouvez modifier les propriétés de police CSS dans la partie inférieure de Visual **Font Editor**.  Vous pouvez modifier la taille de la police, la hauteur de ligne, le poids de la police et l’espacement des lettres à l’aide de l’un des contrôles d’interface utilisateur.  Vos modifications sont appliquées immédiatement dans le navigateur.  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Éditeur de polices ouvert en haut du volet Styles avec les propriétés CSS mises en surbrill" lightbox="../media/font-editor-css-properties.msft.png":::
   Éditeur **de polices** ouvert en haut du volet **Styles** avec les propriétés CSS mises en surbrill  
:::image-end:::  

Vous pouvez également convertir des unités CSS à l’aide de Visual **Font Editor**.  Par exemple, vous pouvez utiliser l’outil sur **** une règle CSS où le curseur de taille de police est initialement définie sur `16 pixels` .  Maintenant, utilisez la dropdown d’unité et choisissez la valeur `em` .  `1 em`L’affichage est égal à `16 pixels` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Modifier la taille de police à 16 pixels" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         Modifier la taille de la police en `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Ouvrir la dropdown d’unité pour la convertir en em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         Ouvrir la dropdown d’unités pour la convertir en `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

La dropdown d’unité fournit toutes les unités CSS numériques disponibles.  La taille de la police, la hauteur des lignes, l’importance de la police et l’espacement utilisent des unités différentes.  Lorsque les zones de texte sont sélectionnées, vous pouvez sélectionner les touches et les touches pour `arrow up` `arrow down` affiner vos paramètres.  Pour utiliser les curseurs avec un clavier, sélectionnez les `arrow left` touches et les `arrow down` touches.  

L’éditeur de propriétés CSS inclut également des mots clés prédéfincis.  Pour utiliser les mots clés prédéfins, sur le côté droit, sélectionnez `Toggle Input Type` l’icône.  L’interface utilisateur change et une liste liste des mots clés prédéfini s’affiche.  Pour revenir à l’interface utilisateur avec le curseur et d’autres contrôles d’interface utilisateur, choisissez de nouveau `Toggle Input Type` l’icône.  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Ouvrir l’interface de mot clé prédéfiny" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   Ouvrir l’interface de mot clé prédéfiny  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Activer les fonctions expérimentales – Fonctions expérimentales | Microsoft Docs"  
