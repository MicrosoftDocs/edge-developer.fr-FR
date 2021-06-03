---
description: Activez « Marquer les scripts de contenu en tant que code de bibliothèque » à partir Paramètres > Framework Library Code.
title: Marquer les scripts de contenu en tant que code de bibliothèque
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e3c2e89e8635b568d0beea8df8720bbb28beb711
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564027"
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
# <a name="mark-content-scripts-as-library-code"></a>Marquer les scripts de contenu en tant que code de bibliothèque  

Lorsque vous utilisez l’outil **Sources** pour passer du [code][DevToolsJavascriptStepThroughCode]pas à pas, vous suspendez parfois le code que vous ne connaissez pas.  Vous avez probablement suspendu le code pour l’une des extensions Microsoft Edge que vous avez installées.  Pour ne pas suspendre le code d’extension, effectuer les actions suivantes.  

1.  Dans DevTools, dans le coin supérieur droit, choisissez**l’icône d’engrenage**( Paramètres ).  La page **Settings** (Paramètres) s’affiche.  
1.  Below **Paramètres**, choose **Ignore List**.  La section Code de la bibliothèque **d’Paramètres** **s’affiche.**  
1.  Activer la case à cocher **Marquer les scripts de contenu** en tant que code bibliothèque.  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Activer la case à cocher Marquer les scripts de contenu en tant que code bibliothèque" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Activer la case **à cocher Marquer les scripts de contenu** en tant que code bibliothèque  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Étape 4 : Pas à pas dans le code : commencer à déboguer JavaScript dans Microsoft Edge devTools | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
