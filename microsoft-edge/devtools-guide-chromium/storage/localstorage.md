---
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612010"
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



Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des [`localStorage`][MDNWindowsLocalStorage] paires clé-valeur.  

## Afficher les clés et valeurs de localStorage   

1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** est affiché par défaut.  
    
    > ##### Figure1  
    > Volet manifeste  
    > ![Volet manifeste][ImageManifest]  

1.  Développez le menu **stockage local** .  
    
    > ##### Figure 2  
    > Le menu **stockage local** affiche deux domaines: `https://business.bing.com` et `https://www.bing.com`  
    > ![Menu stockage local][ImageLocalStorageMenu]  

1.  Sélectionnez un domaine pour afficher les paires clé-valeur.  
    
    > ##### Figure3  
    > `localStorage`Paires clé-valeur pour le `https://www.bing.com` domaine  
    > ![Paires clé-valeur localStorage pour le https://www.bing.com domaine][ImageLocalStorage]  

1.  Sélectionnez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.  
    
    > ##### Figure 4  
    > Affichage de la valeur de la `eventLogQueue_Online` clé  
    > ![Affichage de la valeur de la clé eventLogQueue_Online][ImageLocalStorageViewer]  

## Créer une `localStorage` paire clé-valeur   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Double-cliquez sur la partie vide de la table.  DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .  
    
    > ##### Figure 5  
    > Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur  
    > ![Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur][ImageLocalStorageCreate]  

## Modifier les `localStorage` clés ou les valeurs   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.  
    
    > ##### Figure 6  
    > Modification d’une `localStorage` touche  
    > ![Modification d’une clé localStorage][ImageLocalStorageEdit]  

## Supprimer `localStorage` des paires clé-valeur   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  
1.  Sélectionnez la paire clé-valeur que vous voulez supprimer.  DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.  

1.  Appuyez sur la `Delete` touche ou cliquez sur supprimer la suppression **sélectionnée** ![ ][ImageDeleteIcon] .  

## Supprimer toutes les `localStorage` paires clé-valeur pour un domaine   

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).  

1.  Sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon] .  

## Interagir avec `localStorage` à partir de la console   

Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et dans la mesure où la **console** a accès aux contextes JavaScript de la page, vous pouvez interagir avec celle-ci `localStorage` à partir de la **console**.  

1.  Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `localStorage` paires clé/valeur d’un domaine autre que la page qui s’affiche.  
    
    > ##### Figure 7  
    > Modification du contexte JavaScript de la **console**  
    > ![Modification du contexte JavaScript de la console][ImageJSContext]  

1.  Exécutez vos `localStorage` expressions dans la console, de la même façon que dans votre code JavaScript.  
    
    > ##### Figure8  
    > Interaction `localStorage` à partir de la **console**  
    > ![Interaction avec localStorage à partir de la console][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Figure 2: menu stockage local"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Figure 3: paires clé-valeur localStorage pour le https://www.bing.com domaine"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Figure 4: affichage de la valeur de la clé de eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Figure 5: partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Figure 6: modification d’une clé de localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Figure 7: modification du contexte JavaScript de la console"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Figure 8: interaction avec localStorage à partir de la console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

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
