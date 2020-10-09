---
description: Utilisez le volet média pour afficher des informations et déboguer les lecteurs multimédias par onglet de navigateur.
title: Afficher et déboguer les informations sur les lecteurs multimédias
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: dfcf17861c0296e347007bc3a1a02a2b80661e6f
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11105186"
---
# <span data-ttu-id="169aa-104">Afficher et déboguer les informations sur les lecteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="169aa-104">View and debug media players information</span></span>  

<span data-ttu-id="169aa-105">Utilisez le panneau **multimédia** dans Microsoft Edge devtools pour afficher des informations et déboguer les lecteurs multimédias par onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="169aa-105">Use the **Media** panel in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <span data-ttu-id="169aa-106">Ouvrir le panneau multimédia</span><span class="sxs-lookup"><span data-stu-id="169aa-106">Open the Media panel</span></span>  

<span data-ttu-id="169aa-107">Le panneau **média** est l’emplacement principal de devtools pour l’examen du lecteur multimédia d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="169aa-107">The **Media** panel is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="169aa-108">[Ouvrez devtools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="169aa-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="169aa-109">Pour ouvrir le panneau **média** , sélectionnez **personnaliser et contrôler devtools** `...`  >  **plus**de  >  **médias**.</span><span class="sxs-lookup"><span data-stu-id="169aa-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="169aa-111">Panneau **multimédia**</span><span class="sxs-lookup"><span data-stu-id="169aa-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="169aa-112">Afficher les informations des lecteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="169aa-112">View media players information</span></span>  

1.  <span data-ttu-id="169aa-113">Accédez à une page Web à l’aide d’un lecteur multimédia, tel que le page Web suivant.</span><span class="sxs-lookup"><span data-stu-id="169aa-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="169aa-114">Optimisation de la productivité grâce aux outils de développement Edge</span><span class="sxs-lookup"><span data-stu-id="169aa-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="169aa-115">Dans le menu des **joueurs** , un lecteur multimédia est affiché.</span><span class="sxs-lookup"><span data-stu-id="169aa-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="169aa-116">Sélectionnez le joueur.</span><span class="sxs-lookup"><span data-stu-id="169aa-116">Select the player.</span></span>  <span data-ttu-id="169aa-117">L’onglet **Propriétés** affiche les propriétés du lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="169aa-117">The **Properties** tab displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="169aa-119">Propriétés du média</span><span class="sxs-lookup"><span data-stu-id="169aa-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="169aa-120">Pour afficher tous les événements du lecteur multimédia, sélectionnez l’onglet **Events (événements** ).</span><span class="sxs-lookup"><span data-stu-id="169aa-120">To view all the media player events, choose the **Events** tab.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="169aa-122">Événements multimédias</span><span class="sxs-lookup"><span data-stu-id="169aa-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="169aa-123">Pour afficher les journaux du message du lecteur multimédia, sélectionnez l’onglet **messages** .  Vous pouvez filtrer les messages par niveau de journal ou chaîne.</span><span class="sxs-lookup"><span data-stu-id="169aa-123">To view the media player message logs, choose the **Messages** tab.  You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="169aa-125">Messages multimédias</span><span class="sxs-lookup"><span data-stu-id="169aa-125">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="169aa-126">Dans l’onglet **chronologie** , la lecture multimédia et l’état de la mémoire tampon sont affichés en temps réel.</span><span class="sxs-lookup"><span data-stu-id="169aa-126">On the **Timeline** tab, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="169aa-128">Barre de Planning multimédia</span><span class="sxs-lookup"><span data-stu-id="169aa-128">Media timeline</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="169aa-129">Débogage à distance</span><span class="sxs-lookup"><span data-stu-id="169aa-129">Remote debugging</span></span>  

<span data-ttu-id="169aa-130">Affichez les informations sur les lecteurs multimédias sur un appareil Android à partir de votre ordinateur Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="169aa-130">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="169aa-131">Pour configurer le débogage à distance, accédez à la rubrique mise [en route des appareils Android de débogage à distance][DevtoolsGuideChromiumRemoteDebuggingIndex].</span><span class="sxs-lookup"><span data-stu-id="169aa-131">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="169aa-132">Affichez les informations sur les lecteurs multimédias à distance.</span><span class="sxs-lookup"><span data-stu-id="169aa-132">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <span data-ttu-id="169aa-133">Masquer et afficher des lecteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="169aa-133">Hide and show media players</span></span>  

<span data-ttu-id="169aa-134">Vous pouvez parfois exécuter plusieurs lecteurs multimédias sur une page Web ou utiliser le même onglet de navigateur pour parcourir les différentes pages Web, chacune avec des lecteurs multimédias.</span><span class="sxs-lookup"><span data-stu-id="169aa-134">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="169aa-135">Il est possible que vous deviez masquer \ (ou afficher \) chaque lecteur multimédia pour faciliter le débogage.</span><span class="sxs-lookup"><span data-stu-id="169aa-135">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="169aa-136">Naviguez jusqu’à différentes pages Web vidéo à l’aide de l’onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="169aa-136">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="169aa-137">Pour masquer les lecteurs multimédias, effectuez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="169aa-137">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="169aa-138">Pour masquer un lecteur multimédia, pointez sur un lecteur multimédia, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et sélectionnez **masquer le joueur**.</span><span class="sxs-lookup"><span data-stu-id="169aa-138">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="169aa-139">Pour masquer tous les autres lecteurs multimédias, pointez sur un lecteur multimédia, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et sélectionnez **masquer tous les autres**.</span><span class="sxs-lookup"><span data-stu-id="169aa-139">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="169aa-141">Masquer des lecteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="169aa-141">Hide media players</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="169aa-142">Exporter des informations sur le lecteur multimédia</span><span class="sxs-lookup"><span data-stu-id="169aa-142">Export media player information</span></span>  

1.  <span data-ttu-id="169aa-143">Pour télécharger les informations du lecteur multimédia sous forme de fichier JSON, pointez sur un lecteur multimédia, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **enregistrer les informations du joueur**.</span><span class="sxs-lookup"><span data-stu-id="169aa-143">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="169aa-145">Exporter des informations sur le média</span><span class="sxs-lookup"><span data-stu-id="169aa-145">Export media information</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="169aa-146">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="169aa-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Ouvrir Microsoft Edge DevTools"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Commencer à utiliser le débogage à distance des appareils Android | Documents Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Optimisation de la productivité grâce aux outils de développement Edge | Bing Video"  

> [!NOTE]
> <span data-ttu-id="169aa-150">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="169aa-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="169aa-151">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="169aa-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="169aa-153">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="169aa-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

