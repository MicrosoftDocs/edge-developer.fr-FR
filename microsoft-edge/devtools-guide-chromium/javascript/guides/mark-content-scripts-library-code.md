---
description: Activez « Marquer les scripts de contenu en tant que code de bibliothèque » à partir Paramètres > Framework Library Code.
title: Marquer les scripts de contenu en tant que code de bibliothèque
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e3c2e89e8635b568d0beea8df8720bbb28beb711
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564027"
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
# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="82c1e-104">Marquer les scripts de contenu en tant que code de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82c1e-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="82c1e-105">Lorsque vous utilisez l’outil **Sources** pour passer du [code][DevToolsJavascriptStepThroughCode]pas à pas, vous suspendez parfois le code que vous ne connaissez pas.</span><span class="sxs-lookup"><span data-stu-id="82c1e-105">When you use the **Sources** tool to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you don't recognize.</span></span>  <span data-ttu-id="82c1e-106">Vous avez probablement suspendu le code pour l’une des extensions Microsoft Edge que vous avez installées.</span><span class="sxs-lookup"><span data-stu-id="82c1e-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="82c1e-107">Pour ne pas suspendre le code d’extension, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="82c1e-107">To not pause on extension code, complete the following actions.</span></span>  

1.  <span data-ttu-id="82c1e-108">Dans DevTools, dans le coin supérieur droit, choisissez**l’icône d’engrenage**( Paramètres ).</span><span class="sxs-lookup"><span data-stu-id="82c1e-108">In DevTools, in the upper right, choose the gear icon (**Settings**).</span></span>  <span data-ttu-id="82c1e-109">La page **Settings** (Paramètres) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="82c1e-109">The **Settings** page appears.</span></span>  
1.  <span data-ttu-id="82c1e-110">Below **Paramètres**, choose **Ignore List**.</span><span class="sxs-lookup"><span data-stu-id="82c1e-110">Below **Settings**, choose **Ignore List**.</span></span>  <span data-ttu-id="82c1e-111">La section Code de la bibliothèque **d’Paramètres** **s’affiche.**</span><span class="sxs-lookup"><span data-stu-id="82c1e-111">The **Framework Library Code** section of **Settings** appears.</span></span>  
1.  <span data-ttu-id="82c1e-112">Activer la case à cocher **Marquer les scripts de contenu** en tant que code bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="82c1e-112">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Activer la case à cocher Marquer les scripts de contenu en tant que code bibliothèque" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="82c1e-114">Activer la case **à cocher Marquer les scripts de contenu** en tant que code bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82c1e-114">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="82c1e-115">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="82c1e-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Étape 4 : Pas à pas dans le code : commencer à déboguer JavaScript dans Microsoft Edge devTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="82c1e-117">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82c1e-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="82c1e-118">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="82c1e-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="82c1e-120">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82c1e-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
