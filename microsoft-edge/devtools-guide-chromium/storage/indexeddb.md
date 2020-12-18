---
description: Découvrez comment afficher et modifier des données IndexedDB à l’aide du volet de l’application et d’extraits.
title: Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 03e6d04050677a0ba153c6adc06dd795cc42115d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231201"
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

Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher et modifier des données [IndexedDB][MDNIndexedDBAPI] .  Il part du principe que vous êtes familiarisé avec DevTools.  Il suppose également que vous êtes familiarisé avec IndexedDB.  Si ce n’est pas le cas, accédez à [utiliser IndexedDB][MDNUsingIndexedDB].  

## Afficher les données de IndexedDB  

1.  Sélectionnez l’onglet **application** pour ouvrir l’outil de l' **application** .  Le volet **manifeste** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Volet **manifeste**  
    :::image-end:::  
    
1.  Développez le menu **IndexedDB** pour connaître les bases de données disponibles.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Menu de IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Menu de **IndexedDB**  
    :::image-end:::  
    
    *   \ ( ![ Icône de base de données ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` représente une base de données, où `notes` est le nom de la base de données et `https://mdn.github.io` est l’origine qui accède à la base de données.  
    *   \ ( ![ Icône de magasin d’objets ][ImageObjectStoreIcon] \) `notes` est un magasin d’objets.  
    *   le **titre** et le **corps** sont des [index][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitation connue**  Les bases de données tierces ne sont pas visibles.  Par exemple, si vous utilisez un `<iframe>` pour incorporer une publicité sur votre page, et si votre réseau publicitaire utilise IndexedDB, les données IndexedDB pour votre réseau publicitaire ne sont pas visibles.  Accédez à [#943770 problème][ChromiumIssue943770].  
    
1.  Choisissez une base de données pour vérifier l’origine et le numéro de version.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="La base de données Notes" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       La base de données **Notes**  
    :::image-end:::  
    
1.  Sélectionnez un magasin d’objets pour passer en revue les paires clé-valeur.  
    
    > [!NOTE]
    > Les données IndexedDB ne sont pas mises à jour en temps réel.  Accédez à [Actualiser les données de IndexedDB](#refresh-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Magasin d’objets notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       Magasin d’objets **Notes**  
    :::image-end:::  
    
    *   Nombre **total d’entrées** est le nombre total de paires clé-valeur dans le magasin d’objets.  
    *   **Valeur de générateur de clé** est la clé disponible suivante.  Le champ est affiché uniquement lors de l’utilisation de [générateurs de touches][MDNBasicConceptsKeyGenerator].  
    
1.  Choisissez une cellule dans la colonne **valeur** pour développer la valeur.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Afficher une valeur IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Afficher une valeur **IndexedDB**  
    :::image-end:::  
    
1.  Choisissez un index, tel que **titre** ou **corps** dans l’illustration suivante, pour trier la Banque d’objets en fonction des valeurs de cet index.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Trier un magasin d’objets par index" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Trier un magasin d’objets par index  
    :::image-end:::  
    
## Actualiser les données de IndexedDB  

Les valeurs IndexedDB dans l’outil d' **application** ne sont pas mises à jour en temps réel.  Sélectionnez **Actualiser** \ ( ![ Actualiser ][ImageReloadIcon] \) lors de l’affichage d’un magasin d’objets pour actualiser les données, ou affichez une base de données et sélectionnez **Actualiser la base de données** pour actualiser toutes les données.  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Affichage d’une base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Affichage d’une base de données  
:::image-end:::  

## Modifier les données de IndexedDB  

Les valeurs et les clés de IndexedDB ne sont pas modifiables à partir de l’outil de l' **application** .  Dans la mesure où DevTools a accès au contexte de page, vous pouvez exécuter du code JavaScript dans DevTools pour modifier les données IndexedDB.  

### Modification de données IndexedDB avec des extraits de niveau  

Les [extraits][DevtoolsJavascriptSnippets] de code permettent de stocker et d’exécuter des blocs de code JavaScript dans devtools.  Lorsque vous exécutez un snippet, le résultat est enregistré dans la **console**.  Vous pouvez utiliser un extrait de code pour exécuter du code JavaScript afin de modifier une base de données IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Utiliser un snippet pour interagir avec IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Utiliser un snippet pour interagir avec IndexedDB  
:::image-end:::  

## Supprimer des données de IndexedDB  

### Supprimer une paire clé-valeur IndexedDB  

1.  [Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).  
1.  Sélectionnez la paire clé-valeur que vous voulez supprimer.  DevTools le met en surbrillance pour indiquer qu’il est sélectionné.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Sélectionner une paire clé-valeur pour la supprimer" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Sélectionner une paire clé-valeur pour la supprimer  
    :::image-end:::  
    
1.  Appuyez sur la `Delete` touche ou sélectionnez **Supprimer la sélection** \ (supprimer la ![ sélection ][ImageDeleteIcon] ).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Aspect du magasin d’objets après la suppression de la paire clé-valeur" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Aspect du magasin d’objets après la suppression de la paire clé-valeur  
    :::image-end:::  
    
### Supprimer toutes les paires clé-valeur dans un magasin d’objets  

1.  [Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Afficher un magasin d’objets" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Afficher un magasin d’objets  
    :::image-end:::  
    
1.  Sélectionnez **effacer le magasin d’objets** \ ( ![ effacer le magasin d’objets ][ImageClearIcon] \).  
    
### Supprimer une base de données IndexedDB  

1.  [Affichez la base de données IndexedDB](#view-indexeddb-data) que vous voulez supprimer.  
1.  Cliquez sur **Supprimer la base de données**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Bouton supprimer la base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Bouton **Supprimer la base de données**  
    :::image-end:::  
    
### Supprimer tout le stockage IndexedDB  

1.  Ouvrir le volet de **stockage effacer** .  
1.  Vérifiez que la case à cocher **IndexedDB** est activée.  
1.  Sélectionnez **effacer les données du site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Vider le volet stockage" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       Vider le volet **stockage**  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Exécution d’extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: afficher les bases de données iframe IndexedDB-chrome-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Générateur de clés-Concepts de base | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utiliser IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Utilisation d’un index à l’aide d’IndexedDB | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
