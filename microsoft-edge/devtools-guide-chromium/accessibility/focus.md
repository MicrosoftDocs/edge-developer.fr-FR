---
description: Ouvrez la console, créez une expression dynamique et définissez l’expression sur document.activeElement.
title: Effectuer le suivi de l’élément actif
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2c2040c690441fb33c802cf454dc7a1e3f33c494
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439169"
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

# <a name="track-which-element-has-focus"></a><span data-ttu-id="662a2-104">Effectuer le suivi de l’élément actif</span><span class="sxs-lookup"><span data-stu-id="662a2-104">Track which element has focus</span></span>  

<span data-ttu-id="662a2-105">Supposons que vous testiez l’accessibilité de la navigation au clavier d’une page.</span><span class="sxs-lookup"><span data-stu-id="662a2-105">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="662a2-106">Lorsque vous naviguez sur la page avec la touche, l’anneau de focus disparaît parfois car l’élément qui `Tab` a le focus est masqué.</span><span class="sxs-lookup"><span data-stu-id="662a2-106">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="662a2-107">Effectuer les actions suivantes pour suivre l’élément focus dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="662a2-107">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="662a2-108">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="662a2-108">Open the **Console**.</span></span>  
1.  <span data-ttu-id="662a2-109">Choose **Create Live Expression** \( Create Live Expression ![ ](../media/create-live-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="662a2-109">Choose **Create Live Expression** \(![Create Live Expression](../media/create-live-expression-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Créer une expression live" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="662a2-111">Créer une expression live</span><span class="sxs-lookup"><span data-stu-id="662a2-111">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="662a2-112">Entrez `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="662a2-112">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="662a2-113">Choisissez en dehors de **l’interface** utilisateur Live Expression à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="662a2-113">Choose outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="662a2-114">La valeur affichée `document.activeElement` ci-dessous est le résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="662a2-114">The value displayed below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="662a2-115">Étant donné que cette expression représente toujours l’élément focus, vous avez désormais un moyen de toujours suivre l’élément qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="662a2-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="662a2-116">Pointez sur le résultat pour mettre en évidence l’élément focus dans la vue.</span><span class="sxs-lookup"><span data-stu-id="662a2-116">Hover on the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="662a2-117">Pointez sur le résultat, ouvrez le menu contextuel \(clic droit\), puis choisissez Révéler dans le panneau **Éléments** pour afficher l’élément dans l’arborescence DOM sur l’outil **Éléments.**</span><span class="sxs-lookup"><span data-stu-id="662a2-117">Hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** tool.</span></span>  
*   <span data-ttu-id="662a2-118">Pointez sur le résultat, ouvrez le menu contextuel \(clic droit\), puis choisissez Store comme **variable** globale pour créer une référence de variable au nœud que vous pouvez utiliser dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="662a2-118">Hover on the result, open the contextual menu \(right-click\), and choose **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="662a2-119">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="662a2-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="662a2-120">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="662a2-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="662a2-121">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="662a2-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="662a2-123">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="662a2-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
