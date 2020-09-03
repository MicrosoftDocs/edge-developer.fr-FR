---
description: Activez l’option marquer les scripts de contenu comme code de bibliothèque à partir des paramètres > code de la bibliothèque d’infrastructure.
title: Marquer des scripts de contenu comme du code de bibliothèque
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 517e0a4e944f32d41451a0a5d9d7baa91ff97212
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992791"
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

# Marquer des scripts de contenu comme du code de bibliothèque  

Lorsque vous utilisez le panneau **sources** de Microsoft Edge devtools pour parcourir le [code][DevToolsJavascriptStepThroughCode], vous pouvez parfois mettre en pause le code que vous ne connaissez pas.  Vous avez probablement suspendu le code de l’une des extensions Microsoft Edge que vous avez installées.  Suivez les étapes ci-dessous pour ne pas mettre en pause le code de l’extension.  

1.  Ouvrez DevTools, sélectionnez **personnaliser et contrôler devtools** \ ( `...` \), puis sélectionnez **paramètres**.  Vous pouvez également ouvrir les **paramètres** en sélectionnant `F1` .  

1.  Sélectionnez l’onglet Code de la **bibliothèque** qui ouvre la section Code de la **bibliothèque d’infrastructure** des **paramètres**.  
1.  Activez la case à cocher **marquer les scripts de contenu comme code de bibliothèque** .  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Activer la case à cocher marquer les scripts de contenu comme code de bibliothèque" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Activer la case à cocher **marquer les scripts de contenu comme code de bibliothèque**  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Étape 4: parcourir le code-mise en route avec le débogage JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
