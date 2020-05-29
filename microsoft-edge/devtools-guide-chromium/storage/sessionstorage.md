---
title: Afficher et modifier le stockage de session avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612080"
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





# Afficher et modifier le stockage de session avec Microsoft Edge DevTools   

  

Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des [`sessionStorage`][MDNSessionStorage] paires clé-valeur.  

## Afficher les clés et valeurs de sessionStorage   

1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** est affiché par défaut.  
    
    > ##### Figure1  
    > Volet manifeste  
    > ![Volet manifeste][ImageManifest]  

1.  Développez le menu stockage de la **session** .  
    
    > ##### Figure 2  
    > Menu de **stockage de session**  
    > ![Menu de stockage de session][ImageSessionStorageMenu]  

1.  Sélectionnez un domaine pour afficher les paires clé-valeur.  
    
    > ##### Figure3  
    > Paires clé-valeur sessionStorage  
    > ![Paires clé-valeur «sessionStorage»][ImageSessionStorage]  

1.  Sélectionnez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.  
    
    > ##### Figure 4  
    > Affichage de la valeur de la `x-sid` clé  
    > ![Affichage de la valeur de la clé x-sid][ImageSessionStorageViewer]  

## Créer une paire clé-valeur sessionStorage   

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).  
1.  Double-cliquez sur la partie vide de la table.  DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .  
    
    > ##### Figure 5  
    > Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur  
    > ![Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur][ImageSessionStorageCreate]  

## Modifier les clés ou valeurs de sessionStorage   

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).  
1.  Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.  
    
    > ##### Figure 6  
    > Modification d’une `sessionStorage` touche  
    > ![Modification d’une clé sessionStorage][ImageSessionStorageEdit]  

## Supprimer des paires clé-valeur sessionStorage   

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).  
1.  Sélectionnez la paire clé-valeur que vous voulez supprimer.  DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.  

1.  Appuyez sur la `Delete` touche ou cliquez sur supprimer la suppression **sélectionnée** ![ ][ImageDeleteIcon] .  

## Suppression de toutes les paires clé-valeur sessionStorage pour un domaine   

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).  

1.  Sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon] .  

## Interagir avec sessionStorage à partir de la console   

Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et puisque la **console** a accès aux contextes JavaScript de la page, il est possible d’interagir avec `sessionStorage` à partir de la **console**.  

1.  Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `sessionStorage` paires clé-valeur d’un domaine autre que celui de la page sur laquelle vous vous trouvez.  
    
    > ##### Figure 7  
    > Modification du contexte JavaScript de la **console**  
    > ![Modification du contexte JavaScript de la console][ImageJSContext]  

1.  Exécutez vos `sessionStorage` expressions dans la console, de la même manière que dans JavaScript.  
    
    > ##### Figure8  
    > Interaction `sessionStorage` à partir de la **console**  
    > ![Interaction avec sessionStorage à partir de la console][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Figure 2: menu de stockage de session"  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Figure 3: paires clé-valeur sessionStorage"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Figure 4: affichage de la valeur de la clé x-sid"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Figure 5: partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur"  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Figure 6: modification d’une clé de sessionStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Figure 7: modification du contexte JavaScript de la console"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Figure 8: interaction avec sessionStorage à partir de la console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
