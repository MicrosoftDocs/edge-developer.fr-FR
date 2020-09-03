---
description: Si vous êtes en train de taper les mêmes expressions JavaScript dans la console à plusieurs reprises, essayez plutôt d’utiliser des expressions dynamiques.
title: Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6b66c44b77cd50bc0c1575e5eceb7c8d1a01b709
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993113"
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





# Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques   

  

Si vous vous intentez de taper la même expression JavaScript dans la console à plusieurs reprises, il peut être plus facile de créer une **expression dynamique**.  Dans les **expressions dynamiques** , vous tapez une expression une seule fois, puis épinglez celle-ci en haut de votre console.  La valeur de l’expression est mise à jour en temps réel.  

## Créer une expression dynamique   

1.  [Ouvrez la console][DevToolsConsoleReferenceOpenConsole].  
1.  Cliquez sur **créer une expression dynamique** \ ( ![ créer une expression dynamique ][ImageCreateLiveExpressionIcon] \).  La zone de texte **expression dynamique** s’affiche.  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Taper document. activeElement dans la zone de texte expression dynamique" lightbox="../media/console-create-live-expression.msft.png":::
       Saisie `document.activeElement` de texte dans la zone de texte **expression dynamique**  
    :::image-end:::  
    
1.  Tapez `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) pour enregistrer l’expression ou cliquez en dehors de la zone de texte **expression dynamique** .  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Ouvrez la console-référence de la console | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
