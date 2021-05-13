---
description: Ouvrez la console, créez une expression dynamique et définissez l’expression sur document.activeElement.
title: Effectuer le suivi de l’élément actif
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e7d7bc9ebf8dd891bf7531d8dd283801a01fc3c1
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564594"
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
# <a name="track-which-element-has-focus"></a>Effectuer le suivi de l’élément actif  

Supposons que vous testiez l’accessibilité de la navigation au clavier d’une page.  Lorsque vous naviguez sur la page avec la touche, l’anneau de focus disparaît parfois car l’élément qui `Tab` a le focus est masqué.  

Effectuer les actions suivantes pour suivre l’élément focus dans DevTools.  

1.  Ouvrez la **console.**  
1.  Choose **Create Live Expression** \( Create Live Expression ![ ](../media/create-live-expression-icon.msft.png) \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Créer une expression live" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Créer une expression live  
    :::image-end:::  
    
1.  Tapez `document.activeElement`.  
1.  Choisissez en dehors de **l’interface** utilisateur Live Expression à enregistrer.  
    
La valeur affichée `document.activeElement` ci-dessous est le résultat de l’expression.  

Étant donné que cette expression représente toujours l’élément focus, vous avez désormais un moyen de toujours suivre l’élément qui a le focus.  

*   Pointez sur le résultat pour mettre en évidence l’élément focus dans la vue.  
*   Pointez sur le résultat, ouvrez le menu contextuel \(clic droit\), puis choisissez Révéler dans le panneau **Éléments** pour afficher l’élément dans l’arborescence DOM sur l’outil **Éléments.**  
*   Pointez sur le résultat, ouvrez le menu contextuel \(clic droit\), puis choisissez Store comme **variable** globale pour créer une référence de variable au nœud que vous pouvez utiliser dans la **console.**  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
