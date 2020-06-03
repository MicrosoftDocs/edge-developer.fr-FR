---
title: Remplacement de la chaîne de l’agent utilisateur à partir de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 376e1550d0dc31f3b47b6badd6970076a8c13f91
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607306"
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





# <span data-ttu-id="c9dd5-103">Remplacement de la chaîne de l’agent utilisateur à partir de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c9dd5-103">Override The User Agent String From Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c9dd5-104">Pour remplacer la chaîne de l' [agent utilisateur][MDNUserAgent] à partir de Microsoft Edge devtools:</span><span class="sxs-lookup"><span data-stu-id="c9dd5-104">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="c9dd5-105">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="c9dd5-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="c9dd5-106">Figure1</span><span class="sxs-lookup"><span data-stu-id="c9dd5-106">Figure 1</span></span>  
    > <span data-ttu-id="c9dd5-107">Menu de commandes</span><span class="sxs-lookup"><span data-stu-id="c9dd5-107">The Command Menu</span></span>  
    > ![Menu de commandes][ImageCommandMenu]  
    
1.  <span data-ttu-id="c9dd5-109">Tapez `network conditions` , sélectionnez **afficher les conditions du réseau**, puis appuyez `Enter` sur l’onglet **conditions réseau** pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="c9dd5-109">Type `network conditions`, select **Show Network conditions**, and press `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="c9dd5-110">Dans la section **agent utilisateur** , désactivez la case à cocher **sélectionner automatiquement** .</span><span class="sxs-lookup"><span data-stu-id="c9dd5-110">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="c9dd5-111">Figure 2</span><span class="sxs-lookup"><span data-stu-id="c9dd5-111">Figure 2</span></span>  
    > <span data-ttu-id="c9dd5-112">Désactiver l' **option sélectionner automatiquement**</span><span class="sxs-lookup"><span data-stu-id="c9dd5-112">Disabling **Select automatically**</span></span>  
    > ![Désactiver l’option sélectionner automatiquement][ImageUserAgentDisableSelectAutomatically]  
    
1.  <span data-ttu-id="c9dd5-114">Sélectionnez une chaîne d’agent utilisateur dans la liste ou entrez votre propre chaîne personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c9dd5-114">Select a user agent string from the list, or enter your own custom string.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Figure 1: menu de commandes"  
[ImageUserAgentDisableSelectAutomatically]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png "Figure 2: désactiver l’option sélectionner automatiquement"  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  

> [!NOTE]
> <span data-ttu-id="c9dd5-118">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9dd5-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c9dd5-119">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="c9dd5-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="c9dd5-121">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9dd5-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  