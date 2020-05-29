---
title: Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 659120414597273b15657377c33c800e0c83b7cb
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601837"
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





# <span data-ttu-id="51781-103">Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)</span><span class="sxs-lookup"><span data-stu-id="51781-103">Force Microsoft Edge DevTools Into Print Preview Mode (CSS Print Media Type)</span></span>   



<span data-ttu-id="51781-104">La [requête imprimer][MDNUsingMediaQueries] sur le média détermine l’apparence de votre page avant son impression.</span><span class="sxs-lookup"><span data-stu-id="51781-104">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="51781-105">Pour forcer votre page en mode aperçu avant impression:</span><span class="sxs-lookup"><span data-stu-id="51781-105">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="51781-106">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="51781-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="51781-107">Figure1</span><span class="sxs-lookup"><span data-stu-id="51781-107">Figure 1</span></span>  
    > <span data-ttu-id="51781-108">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="51781-108">The **Command Menu**</span></span>  
    > ![Menu de commandes][ImageCommandMenu]  
    
1.  <span data-ttu-id="51781-110">Tapez `rendering` , sélectionnez **afficher le rendu**, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="51781-110">Type `rendering`, select **Show Rendering**, and then press `Enter`.</span></span>  
1.  <span data-ttu-id="51781-111">Sous **émuler le média CSS** , sélectionnez **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="51781-111">Under **Emulate CSS media** select **print**.</span></span>  
    
    > ##### <span data-ttu-id="51781-112">Figure 2</span><span class="sxs-lookup"><span data-stu-id="51781-112">Figure 2</span></span>  
    > <span data-ttu-id="51781-113">Mode aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="51781-113">Print preview mode</span></span>  
    > ![Mode aperçu avant impression][ImagePrintMode]  
    
<span data-ttu-id="51781-115">À partir de cet emplacement, vous pouvez afficher et modifier votre CSS, comme n’importe quelle autre page Web.</span><span class="sxs-lookup"><span data-stu-id="51781-115">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="51781-116">Voir [commencer à afficher et modifier des feuilles CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="51781-116">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

 



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Figure 1: menu de commandes"  
[ImagePrintMode]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png "Figure 2: mode aperçu avant impression"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> <span data-ttu-id="51781-122">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51781-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="51781-123">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="51781-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="51781-125">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51781-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
