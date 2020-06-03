---
title: Marquer des scripts de contenu comme du code de bibliothèque
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: fe34d8f2fb656283b1821441162b93d47d51d24e
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581788"
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





# <span data-ttu-id="591d1-103">Marquer des scripts de contenu comme du code de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="591d1-103">Mark Content Scripts as Library Code</span></span>   



<span data-ttu-id="591d1-104">Lorsque vous utilisez le panneau **sources** de Microsoft Edge devtools pour parcourir le [code][DevToolsJavascriptStepThroughCode], vous pouvez parfois mettre en pause le code que vous ne connaissez pas.</span><span class="sxs-lookup"><span data-stu-id="591d1-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="591d1-105">Vous avez probablement suspendu le code de l’une des extensions Microsoft Edge que vous avez installées.</span><span class="sxs-lookup"><span data-stu-id="591d1-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="591d1-106">Suivez les étapes ci-dessous pour ne pas mettre en pause le code de l’extension.</span><span class="sxs-lookup"><span data-stu-id="591d1-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="591d1-107">Ouvrez DevTools, sélectionnez **personnaliser et contrôler devtools** , `...` puis cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="591d1-107">Open DevTools, select **Customize and control DevTools** `...` and click **Settings**.</span></span>  <span data-ttu-id="591d1-108">Vous pouvez également ouvrir les **paramètres** en appuyant sur `F1` .</span><span class="sxs-lookup"><span data-stu-id="591d1-108">You may also open **Settings** by pressing `F1`.</span></span>  

1.  <span data-ttu-id="591d1-109">Sélectionnez l’onglet Code de la **bibliothèque** qui ouvre la section Code de la **bibliothèque d’infrastructure** des **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="591d1-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="591d1-110">Activez la case à cocher **marquer les scripts de contenu comme code de bibliothèque** .</span><span class="sxs-lookup"><span data-stu-id="591d1-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="591d1-111">Figure1</span><span class="sxs-lookup"><span data-stu-id="591d1-111">Figure 1</span></span>  
    > <span data-ttu-id="591d1-112">Activer la case à cocher **marquer les scripts de contenu comme code de bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="591d1-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    > ![Activer la case à cocher marquer les scripts de contenu comme code de bibliothèque][ImageMarkContentScriptsLibraryCode]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMarkContentScriptsLibraryCode]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png "Figure 1: activez la case à cocher marquer le contenu comme code de bibliothèque."  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Étape 4: parcourir le code-mise en route avec JavaScript dans Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="591d1-116">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="591d1-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="591d1-117">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools & phare \).</span><span class="sxs-lookup"><span data-stu-id="591d1-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="591d1-119">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="591d1-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  