---
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 829902ddd76800bb8d36268cb07a61361aa1a159
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986114"
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

# <span data-ttu-id="60b45-103">Désactiver JavaScript avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="60b45-103">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="60b45-104">Suivez les étapes ci-dessous pour voir l’apparence et le comportement d’une page Web lorsque JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="60b45-104">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="60b45-105">[Ouvrez Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="60b45-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="60b45-106">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="60b45-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menu de commandes" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="60b45-108">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="60b45-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60b45-109">Commencez `javascript` à taper, sélectionnez **Désactiver JavaScript**, puis appuyez sur `Enter` la touche pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="60b45-109">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="60b45-110">JavaScript est désormais désactivé.</span><span class="sxs-lookup"><span data-stu-id="60b45-110">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Sélectionnez Désactiver JavaScript dans le menu de commandes." lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="60b45-112">Sélectionnez **Désactiver JavaScript** dans le **menu de commandes** .</span><span class="sxs-lookup"><span data-stu-id="60b45-112">Select **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="60b45-113">L’icône d’avertissement jaune en regard de **sources** vous rappelle que JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="60b45-113">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icône d’avertissement en regard de sources" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="60b45-115">Icône d’avertissement en regard de **sources**</span><span class="sxs-lookup"><span data-stu-id="60b45-115">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="60b45-116">JavaScript reste désactivé dans l’onglet tant que vous avez DevTools ouvert.</span><span class="sxs-lookup"><span data-stu-id="60b45-116">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="60b45-117">Vous pouvez vouloir recharger la page pour voir si et comment la page dépend de JavaScript lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="60b45-117">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="60b45-118">Pour réactiver JavaScript, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="60b45-118">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="60b45-119">Ouvrez à nouveau le **menu de commandes** et exécutez la `Enable JavaScript` commande.</span><span class="sxs-lookup"><span data-stu-id="60b45-119">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="60b45-120">Fermez DevTools.</span><span class="sxs-lookup"><span data-stu-id="60b45-120">Close DevTools.</span></span>  

## <span data-ttu-id="60b45-121">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="60b45-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="60b45-123">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60b45-123">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="60b45-124">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="60b45-124">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="60b45-126">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60b45-126">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
