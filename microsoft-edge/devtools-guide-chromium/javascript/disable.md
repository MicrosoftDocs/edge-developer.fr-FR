---
description: Ouvrez le menu de commandes et exécutez la commande «désactiver JavaScript».
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: de756e04c91768c49eed50debce97ae91fdaa3bd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992798"
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

# <span data-ttu-id="0fe02-104">Désactiver JavaScript avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0fe02-104">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="0fe02-105">Suivez les étapes ci-dessous pour voir l’apparence et le comportement d’une page Web lorsque JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0fe02-105">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="0fe02-106">[Ouvrez Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="0fe02-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="0fe02-107">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="0fe02-107">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menu de commandes" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="0fe02-109">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="0fe02-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0fe02-110">Commencez `javascript` à taper, sélectionnez **Désactiver JavaScript**, puis appuyez sur `Enter` la touche pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="0fe02-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="0fe02-111">JavaScript est désormais désactivé.</span><span class="sxs-lookup"><span data-stu-id="0fe02-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Sélectionnez Désactiver JavaScript dans le menu de commandes." lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="0fe02-113">Sélectionnez **Désactiver JavaScript** dans le **menu de commandes** .</span><span class="sxs-lookup"><span data-stu-id="0fe02-113">Select **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0fe02-114">L’icône d’avertissement jaune en regard de **sources** vous rappelle que JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0fe02-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icône d’avertissement en regard de sources" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="0fe02-116">Icône d’avertissement en regard de **sources**</span><span class="sxs-lookup"><span data-stu-id="0fe02-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0fe02-117">JavaScript reste désactivé dans l’onglet tant que vous avez DevTools ouvert.</span><span class="sxs-lookup"><span data-stu-id="0fe02-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="0fe02-118">Vous pouvez vouloir recharger la page pour voir si et comment la page dépend de JavaScript lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="0fe02-118">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="0fe02-119">Pour réactiver JavaScript, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="0fe02-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="0fe02-120">Ouvrez à nouveau le **menu de commandes** et exécutez la `Enable JavaScript` commande.</span><span class="sxs-lookup"><span data-stu-id="0fe02-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="0fe02-121">Fermez DevTools.</span><span class="sxs-lookup"><span data-stu-id="0fe02-121">Close DevTools.</span></span>  

## <span data-ttu-id="0fe02-122">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0fe02-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="0fe02-124">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0fe02-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0fe02-125">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="0fe02-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="0fe02-127">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0fe02-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
