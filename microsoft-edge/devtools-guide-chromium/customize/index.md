---
description: Liste des façons de personnaliser Microsoft Edge DevTools
title: Personnaliser Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/22/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5822fa087244fdfafdefe040709058411040ea45
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313022"
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

# Personnaliser Microsoft Edge DevTools  

Cette page répertorie les méthodes de personnalisation de Microsoft Edge DevTools.  

## Paramètres  

**Paramètres**  >  **Les préférences** contiennent de nombreuses options de personnalisation de DevTools.  

Pour ouvrir Paramètres, effectuer l’une des actions suivantes.  

*   Sélectionnez `F1` pendant que DevTools est en focus.  
*   Ouvrez **le menu principal,** puis choisissez **Paramètres.**  
    
:::image type="complex" source="../media/customize-settings-preferences.msft.png" alt-text="Paramètres" lightbox="../media/customize-settings-preferences.msft.png":::
   **Paramètres**  
:::image-end:::  

## Caisse  

Le **Panneau** est un second panneau dans lequel les outils de votre choix sont affichés.  

Pour ouvrir \(ou fermer\) le **caisse,** sélectionnez `Escape` .  

:::image type="complex" source="../media/customize-drawer-open.msft.png" alt-text="Le caisse" lightbox="../media/customize-drawer-open.msft.png":::
   Le **caisse**  
:::image-end:::  

Par défaut, certains outils s’ouvrent dans le panneau principal, tandis que d’autres apparaissent dans le **panneau**.  Choose **More** \( `...` \) to open a tool in the **Drawer**.  

:::image type="complex" source="../media/customize-drawer-open-more-tools.msft.png" alt-text="Bouton pour ouvrir le caisse" lightbox="../media/customize-drawer-open-more-tools.msft.png":::
   Bouton pour ouvrir le **caisse**  
:::image-end:::  

Vous pouvez déplacer les outils entre le panneau principal et le panneau.  

*   Pour déplacer un outil du panneau vers le panneau principal, pointez sur un outil, ouvrez le menu contextuel \(clic droit\) et choisissez Déplacer **vers le haut.**  
    
    :::image type="complex" source="../media/move-from-drawer.msft.png" alt-text="Déplacer l’outil du Panneau vers le panneau principal" lightbox="../media/move-from-drawer.msft.png":::
       Déplacer l’outil du **Panneau** vers le panneau principal  
    :::image-end:::  
    
*   Pour déplacer un outil du panneau principal vers le panneau, pointez sur un outil, ouvrez le menu contextuel \(clic droit\) et choisissez Déplacer **vers le bas.**  
    
    :::image type="complex" source="../media/move-to-drawer.msft.png" alt-text="Déplacer l’outil du panneau principal vers le panneau" lightbox="../media/move-to-drawer.msft.png":::
       Déplacer l’outil du panneau principal vers le **panneau**
    :::image-end:::  
    

## Réordesser les panneaux  

Choisissez et faites glisser un outil pour modifier l’ordre.  Votre ordre d’outils personnalisé est persistant dans les sessions DevTools.  

> [!NOTE]
> Par défaut, **l’outil** Réseau est généralement le quatrième à partir de la gauche.  Dans la figure suivante, le **panneau** Réseau est le premier à partir de la gauche.  

:::image type="complex" source="../media/customize-network-first-position.msft.png" alt-text="Ordre personnalisé des Devtools dans un panneau" lightbox="../media/customize-network-first-position.msft.png":::
   Ordre personnalisé des Devtools dans un panneau  
:::image-end:::  

## Modifier le placement de DevTools  

Voir [Microsoft Edge DevTools Placement][DevToolsPlacement].  

:::image type="complex" source="../media/customize-dev-tools-dock-side.msft.png" alt-text="DevTools non barraté" lightbox="../media/customize-dev-tools-dock-side.msft.png":::
   DevTools non barraté  
:::image-end:::  

## Thème foncé  

Voir [Activer le thème foncé.][DarkTheme]  

:::image type="complex" source="../media/customize-settings-appearance-theme.msft.png" alt-text="Thème foncé" lightbox="../media/customize-settings-appearance-theme.msft.png":::
   Thème foncé  
:::image-end:::  

## Expériences  

Pour activer les expériences DevTools, effectuer les actions suivantes.  

1.  Accédez `edge://flags/#enable-devtools-experiments` à .  
1.  Choose **Enable**.  
1.  Choose **Relaunch Now**, at the bottom of the page.  

La prochaine fois que vous ouvrirez DevTools, une nouvelle page nommée **Expériences** s’affiche dans [Paramètres.](#settings)  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreIcon]: ../media/more-icon.msft.png  

<!-- links -->  

[DevToolsPlacement]: ./placement.md "Modifier le placement de Microsoft Edge DevTools | Documents Microsoft"  
[DarkTheme]: ./dark-theme.md "Activer le thème foncé dans Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/customize/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
