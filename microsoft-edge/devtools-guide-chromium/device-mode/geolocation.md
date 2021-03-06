---
description: Ouvrez l’outil Capteurs et sélectionnez les coordonnées dans la liste géolocalisation.
title: Remplacer la géolocalisation avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 8f6ad09b2f8db110f6743aae32e16cc9b1185400
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399000"
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

# <a name="override-geolocation-with-microsoft-edge-devtools"></a><span data-ttu-id="56e0c-104">Remplacer la géolocalisation avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="56e0c-104">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="56e0c-105">De nombreux sites web tirez parti de l’emplacement des utilisateurs afin de fournir une expérience plus pertinente aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="56e0c-105">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="56e0c-106">Par exemple, un site web météo peut afficher les prévisions locales dans la zone d’un utilisateur, une fois que l’utilisateur a accordé au site web l’autorisation d’accéder à l’emplacement de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="56e0c-106">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="56e0c-107">Si vous construisez une interface utilisateur qui change en fonction de l’emplacement de l’utilisateur, vous souhaitez probablement vous assurer que le site se comporte correctement à différents endroits dans le monde.</span><span class="sxs-lookup"><span data-stu-id="56e0c-107">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="56e0c-108">Pour remplacer votre géolocalisation dans Microsoft Edge DevTools, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="56e0c-108">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="56e0c-109">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="56e0c-109">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu Commande" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="56e0c-111">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="56e0c-111">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56e0c-112">Tapez `sensors` , choisissez Afficher les **capteurs,** puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="56e0c-112">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="56e0c-113">**L’outil** Capteurs s’ouvre en bas de votre fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="56e0c-113">The **Sensors** tool opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="56e0c-114">Dans la liste **Géolocalisation,** sélectionnez l’une des villes prédéfinies, comme , ou choisissez Emplacement personnalisé pour entrer des coordonnées personnalisées de longitude et de latitude, ou choisissez Emplacement indisponible pour afficher le comportement de votre site lorsque `Tokyo` l’emplacement de \*\*\*\* l’utilisateur n’est pas disponible. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="56e0c-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or choose **Custom location** to enter custom longitude and latitude coordinates, or choose **Location unavailable** to display how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Choisir Tokyo dans la liste géolocalisation" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="56e0c-116">Choisir `Tokyo` dans la liste **géolocalisation**</span><span class="sxs-lookup"><span data-stu-id="56e0c-116">Choose `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="56e0c-117">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="56e0c-117">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="56e0c-118">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56e0c-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="56e0c-119">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="56e0c-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="56e0c-121">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56e0c-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
