---
title: Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 39a7967a7dd1d0b34eb802d2879e04a64afd0dd0
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982234"
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





# <span data-ttu-id="de57f-103">Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques</span><span class="sxs-lookup"><span data-stu-id="de57f-103">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="de57f-104">Si vous vous intentez de taper la même expression JavaScript dans la console à plusieurs reprises, il peut être plus facile de créer une **expression dynamique**.</span><span class="sxs-lookup"><span data-stu-id="de57f-104">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="de57f-105">Dans les **expressions dynamiques** , vous tapez une expression une seule fois, puis épinglez celle-ci en haut de votre console.</span><span class="sxs-lookup"><span data-stu-id="de57f-105">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="de57f-106">La valeur de l’expression est mise à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="de57f-106">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="de57f-107">Créer une expression dynamique</span><span class="sxs-lookup"><span data-stu-id="de57f-107">Create a Live Expression</span></span>   

1.  <span data-ttu-id="de57f-108">[Ouvrez la console][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="de57f-108">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="de57f-109">Cliquez sur **créer une expression dynamique** \ ( ![ créer une expression dynamique ][ImageCreateLiveExpressionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="de57f-109">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="de57f-110">La zone de texte **expression dynamique** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="de57f-110">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Taper document. activeElement dans la zone de texte expression dynamique" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="de57f-112">Saisie `document.activeElement` de texte dans la zone de texte **expression dynamique**</span><span class="sxs-lookup"><span data-stu-id="de57f-112">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="de57f-113">Tapez `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) pour enregistrer l’expression ou cliquez en dehors de la zone de texte **expression dynamique** .</span><span class="sxs-lookup"><span data-stu-id="de57f-113">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Ouvrez la console-référence de la console | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="de57f-115">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="de57f-115">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="de57f-116">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="de57f-116">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="de57f-118">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="de57f-118">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
