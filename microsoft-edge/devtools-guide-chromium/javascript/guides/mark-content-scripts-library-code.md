---
description: Activez « Marquer les scripts de contenu en tant que code de bibliothèque » à partir de Paramètres > Framework Library Code.
title: Marquer les scripts de contenu en tant que code de bibliothèque
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ffc27cdd04ce28df888507fb2e1dc460d5bb4f21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398951"
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

# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="51b55-104">Marquer les scripts de contenu en tant que code de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51b55-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="51b55-105">Lorsque vous utilisez le **panneau Sources** de Microsoft Edge DevTools pour passer du [code][DevToolsJavascriptStepThroughCode]pas à pas, vous suspendez parfois le code que vous ne connaissez pas.</span><span class="sxs-lookup"><span data-stu-id="51b55-105">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="51b55-106">Vous avez probablement suspendu le code de l’une des extensions Microsoft Edge que vous avez installées.</span><span class="sxs-lookup"><span data-stu-id="51b55-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="51b55-107">Pour ne pas suspendre le code d’extension, effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="51b55-107">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="51b55-108">Ouvrez DevTools, choisissez Personnaliser et contrôler **DevTools** \( `...` \) > **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="51b55-108">Open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="51b55-109">Vous pouvez également ouvrir **Paramètres** en sélectionnant `F1` .</span><span class="sxs-lookup"><span data-stu-id="51b55-109">You may also open **Settings** by selecting `F1`.</span></span>  

1.  <span data-ttu-id="51b55-110">Choisissez le **panneau de code** bibliothèque qui ouvre la section **Code** de la bibliothèque d’infrastructure **des paramètres.**</span><span class="sxs-lookup"><span data-stu-id="51b55-110">Choose the **Library code** panel which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="51b55-111">Activer la case à cocher **Marquer les scripts de contenu** en tant que code bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="51b55-111">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Activer la case à cocher Marquer les scripts de contenu en tant que code bibliothèque" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="51b55-113">Activer la case **à cocher Marquer les scripts de contenu** en tant que code bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51b55-113">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="51b55-114">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="51b55-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Étape 4 : Pas à pas dans le code : commencer à déboguer JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="51b55-116">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51b55-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="51b55-117">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="51b55-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="51b55-119">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51b55-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
