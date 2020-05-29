---
title: Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612087"
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





# Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools   

  

Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher et modifier des données [IndexedDB][MDNIndexedDBAPI] .  Il part du principe que vous êtes familiarisé avec DevTools.  Il suppose également que vous êtes familiarisé avec IndexedDB.  Si ce n’est pas le cas, voir [utilisation de IndexedDB][MDNUsingIndexedDB].  

## Afficher les données de IndexedDB   

1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** s’ouvre généralement par défaut.  
    
    > ##### Figure1  
    > Volet manifeste  
    > ![Volet manifeste][ImageManifest]  

1.  Développez le menu **IndexedDB** pour afficher les bases de données disponibles.  
    
    > ##### Figure 2  
    > Menu de **IndexedDB**  
    > ![Menu de IndexedDB][ImageIndexedDBMenu]  
    
    *   ![Icône de base de données ][ImageDatabaseIcon] `notes - https://mdn.github.io` représente une base de données, où `notes` est le nom de la base de données et `https://mdn.github.io` est l’origine qui accède à la base de données.  
    *   ![L’icône magasin ][ImageObjectStoreIcon] `notes` d’objets est un magasin d’objets.  
    *   le **titre** et le **corps** sont des [index][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitation connue**  Les bases de données tierces ne sont pas visibles.  Par exemple, si vous utilisez un `<iframe>` pour incorporer une publicité sur votre page, et si votre réseau publicitaire utilise IndexedDB, les données IndexedDB pour votre réseau publicitaire ne sont pas visibles.  Voir [#943770 de problèmes][ChromiumIssue943770].  
    
1.  Sélectionner une base de données pour afficher l’origine et le numéro de version.  
    
    > ##### Figure3  
    > La base de données **Notes**  
    > ![La base de données Notes][ImageIndexedDBDatabase]  
    
1.  Sélectionnez un magasin d’objets pour afficher les paires clé-valeur.  
    
    > [!NOTE]
    > Les données IndexedDB ne sont pas mises à jour en temps réel.  Voir [Actualiser les données de IndexedDB](#refresh-indexeddb-data).  
    
    > ##### Figure 4  
    > Magasin d’objets **Notes**  
    > ![Magasin d’objets notes][ImageIndexedDBObjectStore]  

    *   Nombre **total d’entrées** est le nombre total de paires clé-valeur dans le magasin d’objets.  
    *   **Valeur de générateur de clé** est la clé disponible suivante.  Ce champ est affiché uniquement lors de l’utilisation de [générateurs de touches][MDNBasicConceptsKeyGenerator].  

1.  Sélectionnez une cellule dans la colonne **valeur** pour développer cette valeur.  
    
    > ##### Figure 5  
    > Affichage d’une valeur IndexedDB  
    > ![Affichage d’une valeur IndexedDB][ImageIndexedBDValue]  
    
1.  Sélectionnez un index, tel que **titre** ou **corps** dans la [figure 6](#figure-6), pour trier le magasin d’objets en fonction des valeurs de cet index.  
   
    > ##### Figure 6  
    > Magasin d’objets trié par ordre alphabétique en fonction de la clé de **titre**  
    > ![Tri d’un magasin d’objets par index][ImageIndexedDBIndex]  

## Actualiser les données de IndexedDB   

Les valeurs IndexedDB dans le panneau d' **application** ne sont pas mises à jour en temps réel.  Sélectionnez **Actualiser** ![ ][ImageReloadIcon] l’actualisation lors de l’affichage d’un magasin d’objets pour actualiser les données, ou affichez une base de données et cliquez sur **Actualiser la base de données** pour actualiser toutes les données.  

> ##### Figure 7  
> Affichage d’une base de données  
> ![Affichage d’une base de données][ImageIndexedDBDatabase2]  

## Modifier les données de IndexedDB   

Les valeurs et les clés IndexedDB ne peuvent pas être modifiées dans le panneau de l' **application** .  Dans la mesure où DevTools a accès au contexte de page, vous pouvez exécuter du code JavaScript dans DevTools pour modifier les données IndexedDB.  

### Modification de données IndexedDB avec des extraits de niveau   

Les [extraits][DevtoolsJavascriptSnippets] de code permettent de stocker et d’exécuter des blocs de code JavaScript dans devtools.  Lorsque vous exécutez un snippet, le résultat est enregistré dans la **console**.  Vous pouvez utiliser un extrait de code pour exécuter du code JavaScript afin de modifier une base de données IndexedDB.  

> ##### Figure8  
> Utilisation d’un snippet pour interagir avec IndexedDB  
> ![Utilisation d’un snippet pour interagir avec IndexedDB][ImageIndexedDBSnippet]  

## Supprimer des données de IndexedDB   

### Supprimer une paire clé-valeur IndexedDB   

1.  [Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).  
1.  Sélectionnez la paire clé-valeur que vous voulez supprimer.  DevTools le met en surbrillance pour indiquer qu’il est sélectionné.  
    
    > ##### Figure9  
    > Sélection d’une paire clé-valeur pour la supprimer  
    > ![Sélection d’une paire clé-valeur pour la supprimer][ImageIndexedDBKeyValuePair]  

1.  Appuyez sur la `Delete` touche ou cliquez sur supprimer la suppression **sélectionnée** ![ ][ImageDeleteIcon] .  
    
    > ##### Figure10  
    > Aspect du magasin d’objets après la suppression de la paire clé-valeur  
    > ![Aspect du magasin d’objets après la suppression de la paire clé-valeur][ImageIndexedDBKeyValuePairDeleted]  

### Supprimer toutes les paires clé-valeur dans un magasin d’objets   

1.  [Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).  
    
    > ##### Figure11  
    > Affichage d’un magasin d’objets  
    > ![Affichage d’un magasin d’objets][ImageIndexedDBObjectStore]  

1.  Sélectionnez effacer le magasin d’objets du **magasin d’objets** ![ ][ImageClearIcon] .  

### Supprimer une base de données IndexedDB   

1.  [Affichez la base de données IndexedDB](#view-indexeddb-data) que vous voulez supprimer.  
1.  Sélectionnez **Supprimer la base de données**.  
    
    > ##### Figure12  
    > Bouton **Supprimer la base de données**  
    > ![Bouton supprimer la base de données][ImageIndexedDBDatabase]  

### Supprimer tout le stockage IndexedDB   

1.  Ouvrir le volet de **stockage effacer** .  

1.  Vérifiez que la case à cocher **IndexedDB** est activée.  

1.  Sélectionnez **effacer les données du site**.  
    
    > ##### Figure13  
    > Vider le volet **stockage** pour ![ Vider le volet stockage][ImageIndexedDBClearStorage]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Figure 1: volet manifeste"  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Figure 2: menu IndexedDB"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Figure 3: notes_db base de données"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Figure 4: magasin d’objets notes_os"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Figure 5: affichage d’une valeur IndexedDB"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Figure 6: tri d’un magasin d’objets par index"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Figure 7: affichage d’une base de données"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Figure 8: utilisation d’un snippet pour interagir avec IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Figure 9: sélection d’une paire clé-valeur pour la supprimer"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Figure 10: apparence du magasin d’objets après la suppression de la paire clé-valeur"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Figure 11: affichage d’un magasin d’objets"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Figure 12: bouton supprimer la base de données"  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Figure 13: volet de stockage clair"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: afficher les bases de données iframe IndexedDB-chrome-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Générateur de clés-Concepts de base | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utiliser IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Utilisation d’un index à l’aide d’IndexedDB | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
