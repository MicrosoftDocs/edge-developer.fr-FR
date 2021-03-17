---
description: Découvrez comment afficher et modifier localStorage avec le volet Stockage local et la console.
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 4eebf3108e7b1c6ecaecbfed445e8f3fe26215c4
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439674"
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

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a>Afficher et modifier le stockage local avec Microsoft Edge DevTools  

Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [localStorage.][MDNWindowsLocalStorage]  

## <a name="view-localstorage-keys-and-values"></a>Afficher les clés et les valeurs localStorage  

1.  Choisissez **l’onglet Application** pour ouvrir **l’outil Application.**  Le **volet** Manifeste s’affiche par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **** manifeste  
    :::image-end:::  
    
1.  Développez le menu **Stockage** local.  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Menu Stockage local" lightbox="../media/storage-application-local-storage.msft.png":::
       Menu **Stockage** local  
    :::image-end:::  
    
1.  Choisissez un domaine pour afficher les paires clé-valeur.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Paires clé-valeur localStorage pour le https://www.bing.com domaine" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       Paires `localStorage` clé-valeur pour le `https://www.bing.com` domaine  
    :::image-end:::  
    
1.  Choisissez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Afficher la valeur de la eventLogQueue_Online clé" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Afficher la valeur de la `eventLogQueue_Online` clé  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a>Créer une paire clé-valeur localStorage  

1.  [Afficher les paires clé-valeur localStorage d’un domaine.](#view-localstorage-keys-and-values)  
1.  Double-cliquez sur la partie vide du tableau.  DevTools crée une ligne et concentre votre curseur dans la **colonne** Clé.  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Partie vide du tableau à double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       Partie vide du tableau à double-cliquer pour créer une paire clé-valeur  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a>Modifier les clés ou valeurs localStorage  

1.  [Afficher les paires clé-valeur localStorage d’un domaine.](#view-localstorage-keys-and-values)  
1.  Double-cliquez sur une cellule **** dans la colonne **Clé** ou Valeur pour modifier cette clé ou cette valeur.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Modifier une clé localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Modifier une `localStorage` clé  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a>Supprimer les paires clé-valeur localStorage  

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine.](#view-localstorage-keys-and-values)  
1.  Choisissez la paire clé-valeur à supprimer.  DevTools le met en sur-soulignement en bleu pour indiquer qu’il est sélectionné.  
1.  Sélectionnez `Delete` la clé ou choisissez Supprimer **sélectionné** \( Supprimer ![ sélectionné ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a>Supprimer toutes `localStorage` les paires clé-valeur pour un domaine  

1.  [Afficher les `localStorage` paires clé-valeur d’un domaine.](#view-localstorage-keys-and-values)  
1.  Choose **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-localstorage-from-the-console"></a>Interagir avec localStorage à partir de la console  

Étant donné que vous pouvez exécuter JavaScript dans la **console**et que la **console** a accès aux contextes JavaScript de la page, il est possible d’interagir avec à partir de `localStorage` la **console.**  

1.  Utilisez le menu **Contexts JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux paires clé-valeur d’un domaine autre que la page qui `localStorage` s’affiche.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Modifier le contexte JavaScript de la console" lightbox="../media/storage-console-local-storage.msft.png":::
       Modifier le contexte JavaScript de la console  
    :::image-end:::  
    
1.  Exécutez vos expressions dans la console, comme vous le faites `localStorage` dans votre JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagir avec localStorage à partir de la console" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interagir avec `localStorage` à partir de la **console**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
