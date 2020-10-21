---
description: Ouvrez la console, créez une expression dynamique et attribuez à l’expression la valeur document. activeElement.
title: Effectuer le suivi de l’élément actif
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a0d0861494db87e546443c0f3a1d4f531412300c
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125306"
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

# Effectuer le suivi de l’élément actif  

Imaginons que vous testiez l’accessibilité de la navigation au clavier d’une page.  Lorsque vous naviguez dans la page à l’aide de la `Tab` touche, l’appel de focus disparaît parfois, car l’élément qui a le focus est masqué.  

Procédez comme suit pour effectuer le suivi de l’élément prioritaire dans DevTools.  

1.  Ouvrez la **console**.  
1.  Sélectionnez **créer une expression dynamique** \ ( ![ créer une expression dynamique ][ImageCreateIcon] \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Créer une expression dynamique" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Créer une expression dynamique  
    :::image-end:::  
    
1.  Entrez `document.activeElement`.  
1.  Cliquez en dehors de l’interface utilisateur de l' **expression dynamique** pour l’enregistrer.  
    
La valeur que vous voyez ci-dessous `document.activeElement` est le résultat de l’expression.  

Dans la mesure où cette expression représente toujours l’élément prioritaire, vous disposez maintenant d’un moyen de toujours garder une trace de l’élément qui a le focus.  

*   Pointez sur le résultat pour mettre en surbrillance l’élément prioritaire dans la fenêtre d’affichage.  
*   Cliquez avec le bouton droit sur le résultat et sélectionnez **Reveal dans le panneau éléments** pour afficher l’élément dans l’arborescence DOM sur le panneau **éléments** .  
*   Cliquez avec le bouton droit sur le résultat et sélectionnez **stocker comme variable globale** pour créer une référence variable au nœud que vous pouvez utiliser dans la **console**.  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
