---
description: Ouvrez le menu Commande et exécutez la commande « Désactiver JavaScript ».
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2067944fa17c332dd15ffb3ef97afe02d35685ed
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398559"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a><span data-ttu-id="6bb36-104">Désactiver JavaScript avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6bb36-104">Disable JavaScript with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="6bb36-105">Effectuer les actions suivantes pour afficher l’apparence et le comportement d’une page web lorsque JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="6bb36-105">Complete the following actions to display how a webpage looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="6bb36-106">[Ouvrez Microsoft Edge DevTools.][DevToolsOpen]</span><span class="sxs-lookup"><span data-stu-id="6bb36-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="6bb36-107">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="6bb36-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menu Commande" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="6bb36-109">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="6bb36-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6bb36-110">Commencez à `javascript` taper, choisissez **Désactiver JavaScript,** puis `Enter` sélectionnez pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="6bb36-110">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="6bb36-111">JavaScript est désormais désactivé.</span><span class="sxs-lookup"><span data-stu-id="6bb36-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Choose Disable JavaScript in the Command Menu" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="6bb36-113">Choose **Disable JavaScript** in the **Command Menu**</span><span class="sxs-lookup"><span data-stu-id="6bb36-113">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="6bb36-114">L’icône d’avertissement jaune en de côté **des sources** vous rappelle que JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="6bb36-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icône d’avertissement en de côté des sources" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="6bb36-116">Icône d’avertissement en de côté des **sources**</span><span class="sxs-lookup"><span data-stu-id="6bb36-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6bb36-117">JavaScript reste désactivé dans l’onglet tant que DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6bb36-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="6bb36-118">Vous souhaitez peut-être actualiser la page pour examiner si et comment la page web dépend de JavaScript lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="6bb36-118">You may want to refresh the page to review if and how the webpage depends on JavaScript while loading.</span></span>  

<span data-ttu-id="6bb36-119">Pour ré-activer JavaScript, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6bb36-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="6bb36-120">Ouvrez **de nouveau le menu Commande** et exécutez la `Enable JavaScript` commande.</span><span class="sxs-lookup"><span data-stu-id="6bb36-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="6bb36-121">Fermez DevTools.</span><span class="sxs-lookup"><span data-stu-id="6bb36-121">Close DevTools.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6bb36-122">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6bb36-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="6bb36-124">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6bb36-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6bb36-125">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6bb36-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="6bb36-127">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6bb36-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
