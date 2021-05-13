---
description: Utilisez l’outil Multimédia pour afficher les informations et déboguer les joueurs multimédias par onglet de navigateur.
title: Afficher et déboguer les informations des joueurs multimédias
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0d2a60c31d5239a4b47102ae96a713b8bfcf46f3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564062"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="view-and-debug-media-players-information"></a><span data-ttu-id="129e5-104">Afficher et déboguer les informations des joueurs multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-104">View and debug media players information</span></span>  

<span data-ttu-id="129e5-105">Utilisez **l’outil Media** dans Microsoft Edge DevTools pour afficher les informations et déboguer les joueurs multimédias par onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="129e5-105">Use the **Media** tool in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <a name="open-the-media-tool"></a><span data-ttu-id="129e5-106">Ouvrir l’outil Multimédia</span><span class="sxs-lookup"><span data-stu-id="129e5-106">Open the Media tool</span></span>  

<span data-ttu-id="129e5-107">**L’outil** Media est l’endroit principal dans DevTools pour l’inspection du lecteur multimédia d’une page web.</span><span class="sxs-lookup"><span data-stu-id="129e5-107">The **Media** tool is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="129e5-108">[Ouvrez DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="129e5-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="129e5-109">Pour ouvrir le **panneau Média,** choisissez **Personnaliser et contrôler les outils DevTools** `...`  >  **More**  >  **Media**.</span><span class="sxs-lookup"><span data-stu-id="129e5-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="129e5-111">**Panneau** multimédia</span><span class="sxs-lookup"><span data-stu-id="129e5-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <a name="view-media-players-information"></a><span data-ttu-id="129e5-112">Afficher les informations des joueurs multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-112">View media players information</span></span>  

1.  <span data-ttu-id="129e5-113">Accédez à une page web avec un lecteur multimédia, tel que la page web suivante.</span><span class="sxs-lookup"><span data-stu-id="129e5-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="129e5-114">Optimisation de la productivité avec les outils de développement Edge</span><span class="sxs-lookup"><span data-stu-id="129e5-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="129e5-115">Sous le menu **Joueurs,** un lecteur multimédia s’affiche.</span><span class="sxs-lookup"><span data-stu-id="129e5-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="129e5-116">Choisissez le joueur.</span><span class="sxs-lookup"><span data-stu-id="129e5-116">Choose the player.</span></span>  <span data-ttu-id="129e5-117">Le **panneau Propriétés** affiche les propriétés du lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="129e5-117">The **Properties** panel displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propriétés multimédias" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="129e5-119">Propriétés multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="129e5-120">Pour afficher tous les événements du lecteur multimédia, choisissez le panneau **Événements.**</span><span class="sxs-lookup"><span data-stu-id="129e5-120">To view all the media player events, choose the **Events** panel.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Événements multimédias" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="129e5-122">Événements multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="129e5-123">Pour afficher les journaux des messages du lecteur multimédia, sélectionnez le **panneau Messages.**</span><span class="sxs-lookup"><span data-stu-id="129e5-123">To view the media player message logs, choose the **Messages** panel.</span></span>  <span data-ttu-id="129e5-124">Vous pouvez filtrer les messages par niveau de journal ou chaîne.</span><span class="sxs-lookup"><span data-stu-id="129e5-124">You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Messages multimédias" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="129e5-126">Messages multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-126">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="129e5-127">Dans le **panneau Chronologie,** l’état de la lecture multimédia et de la mémoire tampon est affiché en direct.</span><span class="sxs-lookup"><span data-stu-id="129e5-127">On the **Timeline** panel, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Chronologie des médias" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="129e5-129">Chronologie des médias</span><span class="sxs-lookup"><span data-stu-id="129e5-129">Media timeline</span></span>  
    :::image-end:::  
    
### <a name="remote-debugging"></a><span data-ttu-id="129e5-130">Débogage à distance</span><span class="sxs-lookup"><span data-stu-id="129e5-130">Remote debugging</span></span>  

<span data-ttu-id="129e5-131">Affichez les informations des joueurs multimédias sur un appareil Android à partir de Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="129e5-131">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="129e5-132">Pour configurer le débogage à distance, accédez à Commencer avec le [débogage à distance des appareils Android.][DevtoolsGuideChromiumRemoteDebuggingIndex]</span><span class="sxs-lookup"><span data-stu-id="129e5-132">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="129e5-133">Afficher les informations des joueurs multimédias à distance.</span><span class="sxs-lookup"><span data-stu-id="129e5-133">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a><span data-ttu-id="129e5-134">Masquer et afficher les joueurs multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-134">Hide and show media players</span></span>  

<span data-ttu-id="129e5-135">Parfois, vous exécutez plusieurs lecteur multimédia sur une page web ou utilisez le même onglet de navigateur pour parcourir différentes pages web, chacune avec des lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="129e5-135">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="129e5-136">Vous pouvez choisir de masquer \(ou afficher\) chaque lecteur multimédia pour une expérience de débogage plus facile.</span><span class="sxs-lookup"><span data-stu-id="129e5-136">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="129e5-137">Accédez à plusieurs pages web vidéo différentes à l’aide du même onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="129e5-137">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="129e5-138">Pour masquer les joueurs multimédias, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="129e5-138">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="129e5-139">Pour masquer un lecteur multimédia, pointez sur un lecteur multimédia, ouvrez le menu contextuel \(clic droit\), puis choisissez **Masquer le lecteur.**</span><span class="sxs-lookup"><span data-stu-id="129e5-139">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="129e5-140">Pour masquer tous les autres joueurs multimédias, pointez sur un lecteur multimédia, ouvrez le menu contextuel \(clic droit\), puis choisissez **Masquer tous les autres.**</span><span class="sxs-lookup"><span data-stu-id="129e5-140">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Masquer les joueurs multimédias" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="129e5-142">Masquer les joueurs multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-142">Hide media players</span></span>  
    :::image-end:::  
    
## <a name="export-media-player-information"></a><span data-ttu-id="129e5-143">Exporter les informations du lecteur multimédia</span><span class="sxs-lookup"><span data-stu-id="129e5-143">Export media player information</span></span>  

1.  <span data-ttu-id="129e5-144">Pour télécharger les informations du lecteur multimédia en tant que fichier JSON, pointez sur un lecteur multimédia, ouvrez le menu contextuel \(clic droit\), puis choisissez Enregistrer les informations **du lecteur.**</span><span class="sxs-lookup"><span data-stu-id="129e5-144">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exporter des informations multimédias" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="129e5-146">Exporter des informations multimédias</span><span class="sxs-lookup"><span data-stu-id="129e5-146">Export media information</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="129e5-147">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="129e5-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge (Chromium) DevTools | Documents Microsoft"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Optimisation de la productivité avec les outils de développement Edge | Bing Vidéo"  

> [!NOTE]
> <span data-ttu-id="129e5-151">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="129e5-151">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="129e5-152">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="129e5-152">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="129e5-154">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="129e5-154">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

