---
description: Ouvrez l’outil Conditions réseau, désactivez sélectionner automatiquement, puis choisissez dans la liste ou entrez une chaîne personnalisée.
title: Remplacer la chaîne de l’agent utilisateur Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 50d831847342c749cd36f203998351d53325a6f8
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564293"
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
# <a name="override-the-user-agent-string-from-microsoft-edge-devtools"></a><span data-ttu-id="2e81d-104">Remplacer la chaîne de l’agent utilisateur Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2e81d-104">Override the user agent string from Microsoft Edge DevTools</span></span>  

<span data-ttu-id="2e81d-105">Pour remplacer la chaîne [d’agent][MDNUserAgent] utilisateur à partir Microsoft Edge DevTools :</span><span class="sxs-lookup"><span data-stu-id="2e81d-105">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="2e81d-106">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="2e81d-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu Commande" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="2e81d-108">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="2e81d-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2e81d-109">Tapez `network conditions` , **sélectionnez Afficher les conditions réseau,** puis `Enter` sélectionnez ouvrir **l’outil Conditions réseau.**</span><span class="sxs-lookup"><span data-stu-id="2e81d-109">Type `network conditions`, choose **Show Network conditions**, and select `Enter` to open the **Network conditions** tool.</span></span>  
1.  <span data-ttu-id="2e81d-110">Dans la section **Agent utilisateur,** désactiver la case à cocher **Sélectionner** automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2e81d-110">In the **User agent** section, turn off the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Désactiver la sélection automatiquement" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="2e81d-112">Désactiver la **sélection automatiquement**</span><span class="sxs-lookup"><span data-stu-id="2e81d-112">Turn off **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2e81d-113">Choisissez une chaîne d’agent utilisateur dans la liste, ou entrez votre propre chaîne personnalisée.</span><span class="sxs-lookup"><span data-stu-id="2e81d-113">Choose a user agent string from the list, or enter your own custom string.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2e81d-114">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="2e81d-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  

> [!NOTE]
> <span data-ttu-id="2e81d-116">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2e81d-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2e81d-117">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2e81d-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2e81d-119">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2e81d-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
