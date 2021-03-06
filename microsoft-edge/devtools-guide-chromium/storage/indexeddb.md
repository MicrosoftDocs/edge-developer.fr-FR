---
description: Découvrez comment afficher et modifier les données IndexedDB avec le panneau Application et les extraits de code.
title: Afficher et modifier les données IndexedDB avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6062cb6b574b2295441bc98616f600cbf00cee8e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398977"
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

# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a>Afficher et modifier les données IndexedDB avec Microsoft Edge DevTools  

Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour afficher et modifier les [données IndexedDB.][MDNIndexedDBAPI]  Il part du principe que vous êtes familiarisé avec DevTools.  Il suppose également que vous êtes familiarisé avec IndexedDB.  Si ce n’est pas le cas, [accédez à Utilisation d’IndexedDB][MDNUsingIndexedDB].  

## <a name="view-indexeddb-data"></a>Afficher les données IndexedDB  

1.  Choisissez **l’onglet Application** pour ouvrir **l’outil Application.**  Le **volet Manifeste** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Volet **** manifeste  
    :::image-end:::  
    
1.  Développez le menu **IndexedDB** pour passer en revue les bases de données disponibles.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Menu IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Menu **IndexedDB**  
    :::image-end:::  
    
    *   \( Icône de base de données \) représente une base de données, où est le nom de la base de données et l’origine qui ![ accède à la base de ][ImageDatabaseIcon] `notes - https://mdn.github.io` `notes` `https://mdn.github.io` données.  
    *   \( ![ Icône du magasin d’objets ][ImageObjectStoreIcon] \) est un magasin `notes` d’objets.  
    *   **title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitation connue**  Les bases de données tierces ne sont pas visibles.  Par exemple, si vous utilisez une fonction pour incorporer une valeur sur votre page et que votre réseau de distribution de données utilise IndexedDB, les données IndexedDB de votre réseau de distribution ne sont pas `<iframe>` visibles.  Accédez au [problème #943770][ChromiumIssue943770].  
    
1.  Choisissez une base de données pour passer en revue l’origine et le numéro de version.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="La base de données de notes" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       La base **de données de notes**  
    :::image-end:::  
    
1.  Choisissez un magasin d’objets pour passer en revue les paires clé-valeur.  
    
    > [!NOTE]
    > Les données IndexedDB ne sont pas mises à jour en temps réel.  Accédez à [Actualiser les données IndexedDB.](#refresh-indexeddb-data)  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Magasin d’objets notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       Magasin **d’objets notes**  
    :::image-end:::  
    
    *   **Le nombre** total d’entrées est le nombre total de paires clé-valeur dans le magasin d’objets.  
    *   **La valeur du générateur de clé** est la clé disponible suivante.  Le champ s’affiche uniquement lorsque vous utilisez [des générateurs de clés.][MDNBasicConceptsKeyGenerator]  
    
1.  Choisissez une cellule dans la **colonne Valeur** pour développer la valeur.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Afficher une valeur IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Afficher une **valeur IndexedDB**  
    :::image-end:::  
    
1.  Choisissez un index, tel **** que le **titre** ou le corps de la figure suivante, pour trier le magasin d’objets en fonction des valeurs de cet index.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Trier un magasin d’objets par index" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Trier un magasin d’objets par index  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a>Actualiser les données IndexedDB  

Les valeurs IndexedDB dans **l’outil Application** ne sont pas mises à jour en temps réel.  Choisissez **Actualiser** \( Actualiser \) lors de l’affichage d’un magasin d’objets pour actualiser les données, ou affichez une base de données et sélectionnez Actualiser la base de données ![ pour actualiser toutes les ][ImageRefreshIcon] données. ****  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Afficher une base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Afficher une base de données  
:::image-end:::  

## <a name="edit-indexeddb-data"></a>Modifier les données IndexedDB  

Les clés et valeurs IndexedDB ne sont pas modifiables à partir de **l’outil Application.**  Étant donné que DevTools a accès au contexte de page, vous pouvez exécuter du code JavaScript dans DevTools pour modifier les données IndexedDB.  

### <a name="edit-indexeddb-data-with-snippets"></a>Modifier les données IndexedDB avec des extraits de code  

[Les extraits de][DevtoolsJavascriptSnippets] code sont un moyen de stocker et d’exécuter des blocs de code JavaScript dans DevTools.  Lorsque vous exécutez un extrait de code, le résultat est enregistré dans la **console.**  Vous pouvez utiliser un extrait de code pour exécuter du code JavaScript afin de modifier une base de données IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Utiliser un extrait de code pour interagir avec IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Utiliser un extrait de code pour interagir avec IndexedDB  
:::image-end:::  

## <a name="delete-indexeddb-data"></a>Supprimer des données IndexedDB  

### <a name="delete-an-indexeddb-key-value-pair"></a>Supprimer une paire clé-valeur IndexedDB  

1.  [Afficher un magasin d’objets IndexedDB.](#view-indexeddb-data)  
1.  Choisissez la paire clé-valeur à supprimer.  DevTools le met en sur évidence pour indiquer qu’il est sélectionné.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Choisir une paire clé-valeur pour la supprimer" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Choisir une paire clé-valeur pour la supprimer  
    :::image-end:::  
    
1.  Sélectionnez `Delete` la clé ou choisissez Supprimer **sélectionné** \( Supprimer ![ sélectionné ][ImageDeleteIcon] \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Apparence du magasin d’objets après la suppression de la paire clé-valeur" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Apparence du magasin d’objets après la suppression de la paire clé-valeur  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a>Supprimer toutes les paires clé-valeur dans un magasin d’objets  

1.  [Afficher un magasin d’objets IndexedDB.](#view-indexeddb-data)  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Afficher un magasin d’objets" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Afficher un magasin d’objets  
    :::image-end:::  
    
1.  Choose **Clear object store** \( Clear object store ![ ][ImageClearIcon] \).  
    
### <a name="delete-an-indexeddb-database"></a>Supprimer une base de données IndexedDB  

1.  [Affichez la base de données IndexedDB](#view-indexeddb-data) à supprimer.  
1.  Choisissez **Supprimer la base de données.**  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Bouton Supprimer la base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Bouton **Supprimer la base de** données  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a>Supprimer tout le stockage IndexedDB  

1.  Ouvrez **le volet Effacer le** stockage.  
1.  Assurez-vous que la case à cocher **IndexedDB** est activée.  
1.  Choisissez **Effacer les données de site.**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Volet de stockage Effacer" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       Volet **de stockage** Effacer  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools : afficher les bases de données iframe IndexedDB - chromium - Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Générateur de clés : concepts de base | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB API | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utilisation de la base de données IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Utilisation d’un index : utilisation de la base de données IndexedDB | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
