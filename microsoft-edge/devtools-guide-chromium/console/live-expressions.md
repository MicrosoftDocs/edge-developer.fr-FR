---
description: Si vous vous trouvez en train de taper les mêmes expressions JavaScript dans la console à plusieurs reprises, essayez plutôt Expressions live.
title: Regardez les valeurs des expressions JavaScript en temps réel avec des expressions en direct
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: af920de1c395489dc09b83f3cc0f24814c4f5cbe
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439225"
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

# <a name="watch-javascript-expression-values-in-real-time-with-live-expressions"></a>Regardez les valeurs des expressions JavaScript en temps réel avec des expressions en direct  

Si vous vous trouvez en train de taper la même expression JavaScript dans la console à plusieurs reprises, vous trouverez peut-être plus facile de créer une **expression live.**  Avec **les expressions live,** vous tapez une expression une seule fois, puis vous l’épinglez en haut de votre console.  La valeur de l’expression est mise à jour en temps quasi réel.  

## <a name="create-a-live-expression"></a>Créer une expression live  

1.  [Ouvrez la console.][DevToolsConsoleReferenceOpenConsole]  
1.  Choose **Create Live Expression** \( Create Live Expression ![ ](../media/create-live-expression-icon.msft.png) \).  La **zone de texte Expression** en direct s’affiche.  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Saisie de document.activeElement dans la zone de texte Expression dynamique" lightbox="../media/console-create-live-expression.msft.png":::
       Saisie dans `document.activeElement` la zone de texte **Expression** live  
    :::image-end:::  
    
1.  Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) **** pour enregistrer l’expression, ou choisissez en dehors de la boîte de texte Live Expression.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Ouvrez la console - Console Reference | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
