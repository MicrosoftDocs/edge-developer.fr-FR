---
description: Découvrez comment afficher et modifier sessionStorage à l’Stockage de session et à la console.
title: Afficher et modifier les Stockage session avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6d686a6eb7bc6fca46d65c46fa9c5aee044ec052
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565063"
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
# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a>Afficher et modifier les Stockage session avec Microsoft Edge DevTools  

Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [sessionStorage.][MDNSessionStorage]  

## <a name="view-sessionstorage-keys-and-values"></a>Afficher les clés et les valeurs sessionStorage  

1.  Choisissez **l’onglet Application** pour ouvrir **l’outil Application.**  Le **panneau** manifeste est affiché par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **** manifeste  
    :::image-end:::  
    
1.  Développez **le menu Stockage** session.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Menu Session Stockage" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       **Menu Session Stockage**  
    :::image-end:::  
    
1.  Choisissez un domaine pour afficher les paires clé-valeur.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Paires clé-valeur sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Paires `sessionStorage` clé-valeur  
    :::image-end:::  
    
1.  Choisissez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Afficher la valeur de la touche x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Afficher la valeur de la `x-sid` clé  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a>Créer une paire clé-valeur sessionStorage  

1.  [Afficher les paires clé-valeur sessionStorage d’un domaine.](#view-sessionstorage-keys-and-values)  
1.  Double-cliquez sur la partie vide du tableau.  DevTools crée une ligne et concentre votre curseur dans la **colonne** Clé.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Partie vide du tableau à double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       Partie vide du tableau à double-cliquer pour créer une paire clé-valeur  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a>Modifier les clés ou valeurs sessionStorage  

1.  [Afficher les paires clé-valeur sessionStorage d’un domaine.](#view-sessionstorage-keys-and-values)  
1.  Double-cliquez sur une cellule **** dans la colonne **Clé** ou Valeur pour modifier cette clé ou cette valeur.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Modifier une clé sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Modifier une `sessionStorage` clé  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a>Supprimer des paires clé-valeur sessionStorage  

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine.](#view-sessionstorage-keys-and-values)  
1.  Choisissez la paire clé-valeur à supprimer.  DevTools le met en sur-soulignement en bleu pour indiquer qu’il est sélectionné.  
1.  Sélectionnez `Delete` la clé ou choisissez Supprimer **sélectionné** \( Supprimer ![ sélectionné ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a>Supprimer toutes les paires clé-valeur sessionStorage pour un domaine  

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine.](#view-sessionstorage-keys-and-values)  
1.  Choose **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-sessionstorage-from-the-console"></a>Interagir avec sessionStorage à partir de la console  

Étant donné que vous pouvez exécuter JavaScript dans la **console**et que la **console** a accès aux contextes JavaScript de la page, il est possible d’interagir avec à partir de `sessionStorage` la **console.**  

1.  Utilisez le menu **Contexts JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `sessionStorage` paires clé-valeur d’un domaine autre que la page sur lequel vous êtes.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Modifier le contexte JavaScript de la console" lightbox="../media/storage-console-domain-selection.msft.png":::
       Modifier le contexte JavaScript de la **console**  
    :::image-end:::  
    
1.  Exécutez `sessionStorage` vos expressions dans la **console,** de la même manière que votre JavaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagir avec sessionStorage à partir de la console" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interagir avec `sessionStorage` à partir de la **console**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
