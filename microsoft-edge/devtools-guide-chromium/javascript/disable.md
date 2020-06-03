---
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f3838b4e8eccf83aaa71be35ff477ec56cbe7455
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581809"
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





# <span data-ttu-id="bd887-103">Désactiver JavaScript avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bd887-103">Disable JavaScript With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="bd887-104">Pour afficher un aperçu d’une page Web lorsque JavaScript est désactivé:</span><span class="sxs-lookup"><span data-stu-id="bd887-104">To see how a web page looks and behaves when JavaScript is disabled:</span></span>  

1.  <span data-ttu-id="bd887-105">[Ouvrez Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="bd887-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="bd887-106">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="bd887-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="bd887-107">Figure1</span><span class="sxs-lookup"><span data-stu-id="bd887-107">Figure 1</span></span>  
    > <span data-ttu-id="bd887-108">Menu de commandes</span><span class="sxs-lookup"><span data-stu-id="bd887-108">The Command Menu</span></span>  
    > ![Menu de commandes][ImageCommandMenu]  
    
1.  <span data-ttu-id="bd887-110">Commencez `javascript` à taper, sélectionnez **Désactiver JavaScript**, puis appuyez sur `Enter` la touche pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="bd887-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="bd887-111">JavaScript est désormais désactivé.</span><span class="sxs-lookup"><span data-stu-id="bd887-111">JavaScript is now disabled.</span></span>  
    
    > ##### <span data-ttu-id="bd887-112">Figure 2</span><span class="sxs-lookup"><span data-stu-id="bd887-112">Figure 2</span></span>  
    > <span data-ttu-id="bd887-113">Sélection de l’option **Désactiver JavaScript** dans le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="bd887-113">Selecting **Disable JavaScript** in the Command Menu</span></span>  
    > ![Sélection de l’option désactiver JavaScript dans le menu de commandes][ImageDisableJS]  
    
    <span data-ttu-id="bd887-115">L’icône d’avertissement jaune en regard de **sources** vous rappelle que JavaScript est désactivé.</span><span class="sxs-lookup"><span data-stu-id="bd887-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    > ##### <span data-ttu-id="bd887-116">Figure3</span><span class="sxs-lookup"><span data-stu-id="bd887-116">Figure 3</span></span>  
    > <span data-ttu-id="bd887-117">Icône d’avertissement en regard de **sources**</span><span class="sxs-lookup"><span data-stu-id="bd887-117">The warning icon next to **Sources**</span></span>  
    > ![Icône d’avertissement en regard de sources][ImageDisableJSWarning]  

<span data-ttu-id="bd887-119">JavaScript reste désactivé dans cet onglet tant que vous avez DevTools ouvert.</span><span class="sxs-lookup"><span data-stu-id="bd887-119">JavaScript remains disabled in this tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="bd887-120">Vous pouvez vouloir recharger la page pour voir si et comment la page dépend de JavaScript lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="bd887-120">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="bd887-121">Pour réactiver JavaScript:</span><span class="sxs-lookup"><span data-stu-id="bd887-121">To re-enable JavaScript:</span></span>  

*   <span data-ttu-id="bd887-122">Ouvrez à nouveau le **menu de commandes** et exécutez la `Enable JavaScript` commande.</span><span class="sxs-lookup"><span data-stu-id="bd887-122">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="bd887-123">Fermez DevTools.</span><span class="sxs-lookup"><span data-stu-id="bd887-123">Close DevTools.</span></span>  

## <span data-ttu-id="bd887-124">Commentaires</span><span class="sxs-lookup"><span data-stu-id="bd887-124">Feedback</span></span>   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Figure 1: menu de commandes"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Figure 2: sélectionnez Désactiver JavaScript dans le menu de commandes"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Figure 3: icône d’avertissement en regard de sources"  

<!-- links -->  

[DevToolsOpen]: ../open.md "Ouvrir Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="bd887-129">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bd887-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bd887-130">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="bd887-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="bd887-132">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bd887-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  