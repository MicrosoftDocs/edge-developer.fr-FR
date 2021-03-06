---
description: Ouvrez l’outil de rendu et sélectionnez Émuler le support CSS > imprimer.
title: Forcer Microsoft Edge DevTools en mode Aperçu avant impression (type de média d’impression CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0123b7abf475212304f654c04bc232e3e96f0bda
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399077"
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

# <a name="force-microsoft-edge-devtools-into-print-preview-mode"></a><span data-ttu-id="a1039-104">Forcer Microsoft Edge DevTools en mode Aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="a1039-104">Force Microsoft Edge DevTools into Print Preview mode</span></span>  

<span data-ttu-id="a1039-105">La [requête de média d’impression][MDNUsingMediaQueries] contrôle l’apparence de votre page lors de l’impression.</span><span class="sxs-lookup"><span data-stu-id="a1039-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="a1039-106">Pour forcer votre page en mode Aperçu avant impression :</span><span class="sxs-lookup"><span data-stu-id="a1039-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="a1039-107">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="a1039-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="a1039-109">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="a1039-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a1039-110">Tapez `rendering` , choisissez Afficher le **rendu,** puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a1039-110">Type `rendering`, choose **Show Rendering**, and then select `Enter`.</span></span>  
1.  <span data-ttu-id="a1039-111">Sous **Émuler le support CSS,** choisissez **Imprimer.**</span><span class="sxs-lookup"><span data-stu-id="a1039-111">Under **Emulate CSS media**, choose **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Mode Aperçu avant impression" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="a1039-113">Mode Aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="a1039-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="a1039-114">À partir de là, vous pouvez afficher et modifier votre CSS, comme n’importe quelle autre page web.</span><span class="sxs-lookup"><span data-stu-id="a1039-114">From here, you may display and change your CSS, like any other web page.</span></span>  <span data-ttu-id="a1039-115">Accédez à [la mise en place de l’affichage et de la modification de CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="a1039-115">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a1039-116">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a1039-116">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevToolsCSSGetStarted]: ./index.md "Commencer à afficher et modifier les | Documents Microsoft"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> <span data-ttu-id="a1039-120">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a1039-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a1039-121">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="a1039-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a1039-123">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a1039-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
