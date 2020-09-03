---
description: Découvrez comment afficher et modifier localStorage à l’aide du volet stockage local et de la console.
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: aa5365d1764ea0db537ea24464f9c76441f05322
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993554"
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





# Afficher et modifier le stockage local avec Microsoft Edge DevTools   



Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [localStorage][MDNWindowsLocalStorage] .  

## Afficher les clés et valeurs de localStorage   

1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** est affiché par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **manifeste**  
    :::image-end:::  
    
1.  Développez le menu **stockage local** .  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Menu stockage local" lightbox="../media/storage-application-local-storage.msft.png":::
       Menu **stockage local**  
    :::image-end:::  
    
1.  Sélectionnez un domaine pour afficher les paires clé-valeur.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Paires clé-valeur localStorage pour le https://www.bing.com domaine" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       `localStorage`Paires clé-valeur pour le `https://www.bing.com` domaine  
    :::image-end:::  
    
1.  Sélectionnez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Afficher la valeur de la clé de eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Afficher la valeur de la `eventLogQueue_Online` clé  
    :::image-end:::  
    
## Créer une paire clé-valeur localStorage   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Double-cliquez sur la partie vide de la table.  DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur  
    :::image-end:::  
    
## Modifier les clés ou valeurs de localStorage   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Modifier une clé de localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Modifier une `localStorage` clé  
    :::image-end:::  
    
## Supprimer des paires clé-valeur localStorage   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Sélectionnez la paire clé-valeur que vous voulez supprimer.  DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.  
1.  Appuyez sur la `Delete` touche ou cliquez sur **Supprimer la sélection** ![ ][ImageDeleteIcon] .  
    
## Supprimer toutes les `localStorage` paires clé-valeur pour un domaine   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Sélectionnez **Effacer tout** \ ( ![ Effacer tout ][ImageClearIcon] ).  
    
## Interagir avec localStorage à partir de la console   

Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et dans la mesure où la **console** a accès aux contextes JavaScript de la page, vous pouvez interagir avec celle-ci `localStorage` à partir de la **console**.  

1.  Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `localStorage` paires clé/valeur d’un domaine autre que la page qui s’affiche.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Changer le contexte JavaScript de la console" lightbox="../media/storage-console-local-storage.msft.png":::
       Changer le contexte JavaScript de la console  
    :::image-end:::  
    
1.  Exécutez vos `localStorage` expressions dans la console, de la même façon que dans votre code JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagir avec localStorage à partir de la console" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interagir avec `localStorage` à partir de la **console**  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
