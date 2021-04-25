---
description: Ouvrez le menu Commande et exécutez la commande « Désactiver JavaScript ».
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 665181b14e6fa5e86950a27822d52395f49f5b92
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519351"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a><span data-ttu-id="44e24-104">Désactiver JavaScript avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="44e24-104">Disable JavaScript with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="44e24-105">Pour examiner le rendu de votre page web lorsqu'un navigateur ne prend pas en charge JavaScript, éteinez temporairement JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44e24-105">To review how your webpage renders when a browser doesn't have JavaScript support, temporarily turn off JavaScript.</span></span>

<span data-ttu-id="44e24-106">Effectuer les actions suivantes pour examiner la façon dont une page web s'affiche et se comporte lorsque vous éteinez JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44e24-106">Complete the following actions to examine how a webpage displays and behaves when you turn off JavaScript.</span></span>  

1.  <span data-ttu-id="44e24-107">[Ouvrez Microsoft Edge DevTools.][DevToolsOpen]</span><span class="sxs-lookup"><span data-stu-id="44e24-107">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="44e24-108">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="44e24-108">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menu Commande" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="44e24-110">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="44e24-110">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="44e24-111">Commencez à `javascript` taper, choisissez **Désactiver JavaScript,** puis `Enter` sélectionnez pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="44e24-111">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="44e24-112">JavaScript est désormais désactivé.</span><span class="sxs-lookup"><span data-stu-id="44e24-112">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Choose Disable JavaScript in the Command Menu" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="44e24-114">Choose **Disable JavaScript** in the **Command Menu**</span><span class="sxs-lookup"><span data-stu-id="44e24-114">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="44e24-115">L'icône d'avertissement jaune en de côté **des sources** vous rappelle que JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="44e24-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icône d'avertissement en de côté des sources" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="44e24-117">Icône d'avertissement en de côté des **sources**</span><span class="sxs-lookup"><span data-stu-id="44e24-117">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="44e24-118">JavaScript reste désactivé dans l'onglet tant que DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="44e24-118">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="44e24-119">Vous souhaitez peut-être actualiser la page pour examiner si et comment la page web dépend de JavaScript lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="44e24-119">You may want to refresh the page to review if and how the webpage depends on JavaScript while loading.</span></span>  

<span data-ttu-id="44e24-120">Pour ré-activer JavaScript, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="44e24-120">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="44e24-121">Ouvrez **de nouveau le menu Commande** et exécutez la `Enable JavaScript` commande.</span><span class="sxs-lookup"><span data-stu-id="44e24-121">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="44e24-122">Fermez DevTools.</span><span class="sxs-lookup"><span data-stu-id="44e24-122">Close DevTools.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="44e24-123">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="44e24-123">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="44e24-125">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44e24-125">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="44e24-126">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="44e24-126">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="44e24-128">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44e24-128">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
