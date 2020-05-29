---
title: Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601746"
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





# <span data-ttu-id="8a4fa-103">Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8a4fa-103">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="8a4fa-104">Le menu de commandes fournit un moyen rapide de naviguer dans l’interface utilisateur de Microsoft Edge DevTools et d’accomplir des tâches courantes, telles que la [désactivation de JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="8a4fa-104">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="8a4fa-105">Il est possible que vous connaissiez une fonctionnalité semblable dans le code Visual Studio appelé [palette de commandes][VisualStudioCodeUICommandPalette], qui était l’original du menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="8a4fa-105">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

> ##### <span data-ttu-id="8a4fa-106">Figure1</span><span class="sxs-lookup"><span data-stu-id="8a4fa-106">Figure 1</span></span>  
> <span data-ttu-id="8a4fa-107">Utiliser le menu de commande pour désactiver JavaScript</span><span class="sxs-lookup"><span data-stu-id="8a4fa-107">Using the Command Menu to disable JavaScript</span></span>  
> ![Utiliser le menu de commande pour désactiver JavaScript][ImageDisableJS]  

## <span data-ttu-id="8a4fa-109">Ouvrir le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="8a4fa-109">Open the Command Menu</span></span>   

<span data-ttu-id="8a4fa-110">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="8a4fa-110">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="8a4fa-111">Vous avez le choix entre les commandes **personnaliser et contrôler devtools** `...` , puis sélectionner **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="8a4fa-111">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

> ##### <span data-ttu-id="8a4fa-112">Figure 2</span><span class="sxs-lookup"><span data-stu-id="8a4fa-112">Figure 2</span></span>  
> <span data-ttu-id="8a4fa-113">Commande exécuter</span><span class="sxs-lookup"><span data-stu-id="8a4fa-113">Run Command</span></span>  
> ![Commande exécuter][ImageRunCommand]  

## <span data-ttu-id="8a4fa-115">Afficher les autres actions disponibles</span><span class="sxs-lookup"><span data-stu-id="8a4fa-115">See other available actions</span></span>   

<span data-ttu-id="8a4fa-116">Si vous utilisez le flux de travail décrit dans [ouvrir le menu de commandes](#open-the-command-menu), le menu de commandes s’ouvre avec un `>` caractère en gras dans la zone de texte du menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="8a4fa-116">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character prepended to the Command Menu text box.</span></span>  

> ##### <span data-ttu-id="8a4fa-117">Figure3</span><span class="sxs-lookup"><span data-stu-id="8a4fa-117">Figure 3</span></span>  
> <span data-ttu-id="8a4fa-118">Le caractère de commande</span><span class="sxs-lookup"><span data-stu-id="8a4fa-118">The command character</span></span>  
> ![Le caractère de commande][ImageCommandCharacter]  

<span data-ttu-id="8a4fa-120">Supprimez le `>` caractère et tapez `?` pour afficher d’autres actions disponibles dans le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="8a4fa-120">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

> ##### <span data-ttu-id="8a4fa-121">Figure 4</span><span class="sxs-lookup"><span data-stu-id="8a4fa-121">Figure 4</span></span>  
> <span data-ttu-id="8a4fa-122">Autres actions disponibles</span><span class="sxs-lookup"><span data-stu-id="8a4fa-122">Other available actions</span></span>  
> ![Autres actions disponibles][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Figure 1: utilisation du menu de commandes pour désactiver JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Figure 2: commande exécuter"  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Figure 3: caractère de commande"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Figure 4: autres actions disponibles"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Désactiver JavaScript avec Microsoft Edge DevTools"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Palette de commandes-interface utilisateur de code Visual Studio"  

> [!NOTE]
> <span data-ttu-id="8a4fa-130">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a4fa-130">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8a4fa-131">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="8a4fa-131">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="8a4fa-133">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a4fa-133">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
