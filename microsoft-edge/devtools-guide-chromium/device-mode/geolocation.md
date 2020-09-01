---
title: Remplacer le géolocalisation avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1bd6da8d0e4c170fa94fed995a26e77b119992f1
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981824"
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





# <span data-ttu-id="7c0ed-103">Remplacer le géolocalisation avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7c0ed-103">Override geolocation with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="7c0ed-104">De nombreux sites Web tirent parti de l’emplacement de l’utilisateur, afin de fournir une utilisation plus pertinente aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7c0ed-104">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="7c0ed-105">Par exemple, un site Web météo peut afficher la prévision locale dans la zone d’un utilisateur, une fois que l’utilisateur a accordé l’autorisation de site Web pour accéder à l’emplacement actuel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c0ed-105">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="7c0ed-106">Si vous créez une interface utilisateur qui change en fonction de l’emplacement de l’utilisateur, vous devez probablement vous assurer que le site se comporte correctement à différents emplacements du monde.</span><span class="sxs-lookup"><span data-stu-id="7c0ed-106">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="7c0ed-107">Pour ignorer votre géolocalisation dans Microsoft Edge DevTools, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c0ed-107">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="7c0ed-108">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="7c0ed-108">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="7c0ed-110">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="7c0ed-110">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7c0ed-111">Tapez `sensors` , sélectionnez **afficher les capteurs**, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7c0ed-111">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="7c0ed-112">L’onglet **capteurs** s’ouvre en bas de la fenêtre devtools.</span><span class="sxs-lookup"><span data-stu-id="7c0ed-112">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="7c0ed-113">Dans la liste de **géolocalisation** , sélectionnez l’une des villes prédéfinies, par exemple `Tokyo` , ou sélectionnez **emplacement personnalisé** pour entrer des coordonnées de longitude et de latitude personnalisées, ou sélectionnez **emplacement non disponible** pour voir l’apparence de votre site lorsque l’emplacement de l’utilisateur n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="7c0ed-113">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or select **Custom location** to enter custom longitude and latitude coordinates, or select **Location unavailable** to see how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Sélectionner Tokyo dans la liste de géolocalisation" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="7c0ed-115">Sélectionner `Tokyo` dans la liste de **géolocalisation**</span><span class="sxs-lookup"><span data-stu-id="7c0ed-115">Select `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
<!--  
## Feedback   

  
-->  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="7c0ed-116">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7c0ed-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7c0ed-117">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="7c0ed-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="7c0ed-119">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7c0ed-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
