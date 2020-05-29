---
title: Suivre l’élément sélectionné
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: a1bcb7e97357d1348b363ecd4842d1b6a78feb45
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581530"
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





# Suivre l’élément sélectionné   



Imaginons que vous testiez l’accessibilité de la navigation au clavier d’une page.  Lorsque vous naviguez dans la page à l’aide de la `Tab` touche, l’appel de focus disparaît parfois, car l’élément qui a le focus est masqué.  Pour effectuer le suivi de l’élément prioritaire dans DevTools:  

1.  Ouvrez la **console**.  
1.  Cliquez sur **créer** une expression dynamique ![ ][ImageCreateIcon] .  

    > ##### Figure1  
    > Création d’une **expression dynamique**  
    > ![Création d’une expression dynamique][ImageLiveExpression]  
    
1.  Entrez `document.activeElement`.
1.  Cliquez en dehors de l’interface utilisateur de l' **expression dynamique** pour l’enregistrer.

La valeur que vous voyez ci-dessous `document.activeElement` est le résultat de l’expression.  
Dans la mesure où cette expression représente toujours l’élément prioritaire, vous disposez maintenant d’un moyen de toujours garder une trace de l’élément qui a le focus.  

*   Pointez sur le résultat pour mettre en surbrillance l’élément prioritaire dans la fenêtre d’affichage.  
*   Cliquez avec le bouton droit sur le résultat et sélectionnez **Reveal dans le panneau éléments** pour afficher l’élément dans l’arborescence DOM sur le panneau **éléments** .  
*   Cliquez avec le bouton droit sur le résultat et sélectionnez **stocker comme variable globale** pour créer une référence variable au nœud que vous pouvez utiliser dans la **console**.  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCreateIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpression]: /microsoft-edge/devtools-guide-chromium/media/accessibility-console-create-live-expression-empty.msft.png "Figure 1: création d’une expression dynamique"  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
