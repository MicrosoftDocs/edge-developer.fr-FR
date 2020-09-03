---
description: Ouvrez la console, créez une expression dynamique et attribuez à l’expression la valeur document. activeElement.
title: Effectuer le suivi de l’élément actif
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 9000b8ca1fa52daf5257f201c65dcabd78298ec7
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993204"
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

# <span data-ttu-id="8149f-104">Effectuer le suivi de l’élément actif</span><span class="sxs-lookup"><span data-stu-id="8149f-104">Track Which Element Has Focus</span></span>  

<span data-ttu-id="8149f-105">Imaginons que vous testiez l’accessibilité de la navigation au clavier d’une page.</span><span class="sxs-lookup"><span data-stu-id="8149f-105">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="8149f-106">Lorsque vous naviguez dans la page à l’aide de la `Tab` touche, l’appel de focus disparaît parfois, car l’élément qui a le focus est masqué.</span><span class="sxs-lookup"><span data-stu-id="8149f-106">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="8149f-107">Procédez comme suit pour effectuer le suivi de l’élément prioritaire dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="8149f-107">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="8149f-108">Ouvrez la **console**.</span><span class="sxs-lookup"><span data-stu-id="8149f-108">Open the **Console**.</span></span>  
1.  <span data-ttu-id="8149f-109">Cliquez sur **créer une expression dynamique** \ ( ![ créer une expression dynamique ][ImageCreateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="8149f-109">Click **Create Live Expression** \(![Create Live Expression][ImageCreateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Créer une expression dynamique" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="8149f-111">Créer une expression dynamique</span><span class="sxs-lookup"><span data-stu-id="8149f-111">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8149f-112">Entrez `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="8149f-112">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="8149f-113">Cliquez en dehors de l’interface utilisateur de l' **expression dynamique** pour l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="8149f-113">Click outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="8149f-114">La valeur que vous voyez ci-dessous `document.activeElement` est le résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="8149f-114">The value that you see below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="8149f-115">Dans la mesure où cette expression représente toujours l’élément prioritaire, vous disposez maintenant d’un moyen de toujours garder une trace de l’élément qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="8149f-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="8149f-116">Pointez sur le résultat pour mettre en surbrillance l’élément prioritaire dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8149f-116">Hover over the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="8149f-117">Cliquez avec le bouton droit sur le résultat et sélectionnez **Reveal dans le panneau éléments** pour afficher l’élément dans l’arborescence DOM sur le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="8149f-117">Right-click the result and select **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** panel.</span></span>  
*   <span data-ttu-id="8149f-118">Cliquez avec le bouton droit sur le résultat et sélectionnez **stocker comme variable globale** pour créer une référence variable au nœud que vous pouvez utiliser dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="8149f-118">Right-click the result and select **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <span data-ttu-id="8149f-119">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="8149f-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="8149f-120">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8149f-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8149f-121">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="8149f-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="8149f-123">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8149f-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
