---
description: Ouvrez l’onglet «Affichage», puis sélectionnez «émuler les médias CSS» > «imprimer».
title: Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d4e8e06d60461ac4cdcab8686a18a0698d52f6e3
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125117"
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

# <span data-ttu-id="ef5b3-104">Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)</span><span class="sxs-lookup"><span data-stu-id="ef5b3-104">Force Microsoft Edge DevTools into Print Preview mode (CSS Print Media Type)</span></span>  

<span data-ttu-id="ef5b3-105">La [requête imprimer][MDNUsingMediaQueries] sur le média détermine l’apparence de votre page avant son impression.</span><span class="sxs-lookup"><span data-stu-id="ef5b3-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="ef5b3-106">Pour forcer votre page en mode aperçu avant impression:</span><span class="sxs-lookup"><span data-stu-id="ef5b3-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="ef5b3-107">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="ef5b3-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="ef5b3-109">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="ef5b3-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef5b3-110">Tapez `rendering` , sélectionnez **afficher le rendu**, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ef5b3-110">Type `rendering`, choose **Show Rendering**, and then select `Enter`.</span></span>  
1.  <span data-ttu-id="ef5b3-111">Sous **émuler le média CSS** , sélectionnez **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="ef5b3-111">Under **Emulate CSS media** choose **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Menu de commandes" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="ef5b3-113">Mode aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="ef5b3-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ef5b3-114">À partir de cet emplacement, vous pouvez afficher et modifier votre CSS, comme n’importe quelle autre page Web.</span><span class="sxs-lookup"><span data-stu-id="ef5b3-114">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="ef5b3-115">Voir [commencer à afficher et modifier des feuilles CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="ef5b3-115">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <span data-ttu-id="ef5b3-116">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ef5b3-116">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevToolsCSSGetStarted]: ./index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> <span data-ttu-id="ef5b3-120">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ef5b3-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ef5b3-121">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="ef5b3-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="ef5b3-123">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ef5b3-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
