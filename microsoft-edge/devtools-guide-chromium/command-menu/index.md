---
title: Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 09adaadd6f62710b219911f69fbe39ba8edfb61a
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982544"
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





# <span data-ttu-id="2c1ad-103">Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2c1ad-103">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="2c1ad-104">Le menu de commandes fournit un moyen rapide de naviguer dans l’interface utilisateur de Microsoft Edge DevTools et d’accomplir des tâches courantes, telles que la [désactivation de JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="2c1ad-104">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="2c1ad-105">Il est possible que vous connaissiez une fonctionnalité semblable dans le code Visual Studio appelé [palette de commandes][VisualStudioCodeUICommandPalette], qui était l’original du menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="2c1ad-105">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Utiliser le menu de commande pour désactiver JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="2c1ad-107">Utiliser le menu de commande pour désactiver JavaScript</span><span class="sxs-lookup"><span data-stu-id="2c1ad-107">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="2c1ad-108">Ouvrir le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="2c1ad-108">Open the Command Menu</span></span>   

<span data-ttu-id="2c1ad-109">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="2c1ad-109">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="2c1ad-110">Vous avez le choix entre les commandes **personnaliser et contrôler devtools** `...` , puis sélectionner **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="2c1ad-110">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Commande exécuter" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="2c1ad-112">Commande exécuter</span><span class="sxs-lookup"><span data-stu-id="2c1ad-112">Run Command</span></span>  
:::image-end:::  

## <span data-ttu-id="2c1ad-113">Afficher les autres actions disponibles</span><span class="sxs-lookup"><span data-stu-id="2c1ad-113">See other available actions</span></span>   

<span data-ttu-id="2c1ad-114">Si vous utilisez le flux de travail en mode plan dans [ouvrir le menu](#open-the-command-menu)de commandes, le menu de commandes s’ouvre avec un préfixe de `>` caractère dans la zone de texte menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="2c1ad-114">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Le caractère de commande" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="2c1ad-116">Le caractère de commande</span><span class="sxs-lookup"><span data-stu-id="2c1ad-116">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="2c1ad-117">Supprimez le `>` caractère et tapez `?` pour afficher d’autres actions disponibles dans le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="2c1ad-117">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Autres actions disponibles" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="2c1ad-119">Autres actions disponibles</span><span class="sxs-lookup"><span data-stu-id="2c1ad-119">Other available actions</span></span>  
:::image-end:::  

 



<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Désactiver JavaScript avec Microsoft Edge DevTools | Documents Microsoft"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Palette de commandes-interface utilisateur de code Visual Studio"  

> [!NOTE]
> <span data-ttu-id="2c1ad-122">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c1ad-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2c1ad-123">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="2c1ad-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="2c1ad-125">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c1ad-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
