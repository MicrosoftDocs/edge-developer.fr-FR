---
description: Découvrez comment afficher et modifier localStorage à l’aide du volet stockage local et de la console.
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c68f11b8ba2c10a0792f10acf5c5ededf2ad8e8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231187"
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

1.  Sélectionnez l’onglet **application** pour ouvrir l’outil de l' **application** .  Le volet **manifeste** est affiché par défaut.  
    
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
    
1.  Choisissez une ligne du tableau pour afficher la valeur de la visionneuse sous le tableau.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Afficher la valeur de la clé de eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Afficher la valeur de la `eventLogQueue_Online` clé  
    :::image-end:::  
    
## Créer une paire clé-valeur localStorage  

1.  [Affichez les paires clé-valeur localStorage d’un domaine](#view-localstorage-keys-and-values).  
1.  Double-cliquez sur la partie vide de la table.  DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur  
    :::image-end:::  
    
## Modifier les clés ou valeurs de localStorage  

1.  [Affichez les paires clé-valeur localStorage d’un domaine](#view-localstorage-keys-and-values).  
1.  Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Modifier une clé de localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Modifier une `localStorage` clé  
    :::image-end:::  
    
## Supprimer des paires clé-valeur localStorage  

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Choisissez la paire clé-valeur que vous voulez supprimer.  DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.  
1.  Sélectionnez la `Delete` clé ou cliquez sur **supprimer** la sélection ![ ][ImageDeleteIcon] .  
    
## Supprimer toutes les `localStorage` paires clé-valeur pour un domaine  

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Sélectionnez **Effacer tout** ( ![ Effacer tout ][ImageClearIcon] ).  
    
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
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
