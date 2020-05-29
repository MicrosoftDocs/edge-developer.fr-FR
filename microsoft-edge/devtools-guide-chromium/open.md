---
title: Ouvrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601886"
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
   limitations under the License. -->





# <span data-ttu-id="06f7c-103">Ouvrir Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="06f7c-103">Open Microsoft Edge DevTools</span></span>   



<span data-ttu-id="06f7c-104">Il existe de nombreuses façons d’ouvrir Microsoft Edge DevTools, car les utilisateurs différents ont besoin d’un accès rapide à différentes parties de l’interface utilisateur d’DevTools.</span><span class="sxs-lookup"><span data-stu-id="06f7c-104">There are many ways to open Microsoft Edge DevTools, because different users want fast access to different parts of the DevTools UI.</span></span>  

## <span data-ttu-id="06f7c-105">Ouvrir le panneau des éléments pour vérifier le DOM ou les feuilles CSS</span><span class="sxs-lookup"><span data-stu-id="06f7c-105">Open the Elements panel to inspect the DOM or CSS</span></span>   

<span data-ttu-id="06f7c-106">Lorsque vous voulez examiner les styles ou les attributs d’un nœud DOM, cliquez avec le bouton droit sur l’élément, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="06f7c-106">When you want to inspect the styles or attributes of a DOM node, right-click the element and select **Inspect**.</span></span>  

> ##### <span data-ttu-id="06f7c-107">Figure1</span><span class="sxs-lookup"><span data-stu-id="06f7c-107">Figure 1</span></span>  
> <span data-ttu-id="06f7c-108">Option **inspecter**</span><span class="sxs-lookup"><span data-stu-id="06f7c-108">The **Inspect** option</span></span>  
> ![Option inspecter][ImageInspectOption]  

<span data-ttu-id="06f7c-110">Ou appuyez sur `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Option` + `C` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="06f7c-110">Or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Option`+`C` \(macOS\).</span></span>  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <span data-ttu-id="06f7c-111">Ouvrir le panneau Console pour afficher les messages enregistrés ou exécuter JavaScript</span><span class="sxs-lookup"><span data-stu-id="06f7c-111">Open the Console panel to view logged messages or run JavaScript</span></span>   

<span data-ttu-id="06f7c-112">`Control` + `Shift` + `J` Pour accéder directement au panneau de la console, appuyez sur \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \). **Console**</span><span class="sxs-lookup"><span data-stu-id="06f7c-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to jump straight into the **Console** panel.</span></span>  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## <span data-ttu-id="06f7c-113">Ouvrir le dernier panneau ouvert</span><span class="sxs-lookup"><span data-stu-id="06f7c-113">Open the last panel you had open</span></span>   

<span data-ttu-id="06f7c-114">Appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="06f7c-114">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  

## <span data-ttu-id="06f7c-115">Ouvrez DevTools à partir du menu principal de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="06f7c-115">Open DevTools from the Microsoft Edge main menu</span></span>  

<span data-ttu-id="06f7c-116">Cliquez sur **paramètres, puis sur plus \ (Alt + F \)** `...` et sélectionnez **autres outils**de développement outils de  >  **développement**.</span><span class="sxs-lookup"><span data-stu-id="06f7c-116">Click **Settings and more \(Alt+F\)** `...` and then select **More Tools** > **Developer Tools**.</span></span>  

> ##### <span data-ttu-id="06f7c-117">Figure 2</span><span class="sxs-lookup"><span data-stu-id="06f7c-117">Figure 2</span></span>  
> <span data-ttu-id="06f7c-118">Ouverture de DevTools à partir du menu principal de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="06f7c-118">Opening DevTools from the Microsoft Edge main menu</span></span>  
> ![Ouverture de DevTools à partir du menu principal de Microsoft Edge][ImageOpenFromMain]  

## <span data-ttu-id="06f7c-120">Ouverture automatique DevTools sur chaque nouvel onglet</span><span class="sxs-lookup"><span data-stu-id="06f7c-120">Auto-open DevTools on every new tab</span></span>   

<span data-ttu-id="06f7c-121">Ouvrez Microsoft Edge à partir de la ligne de commande et transmettez l' `--auto-open-devtools-for-tabs` indicateur.</span><span class="sxs-lookup"><span data-stu-id="06f7c-121">Open Microsoft Edge from the command line and pass the `--auto-open-devtools-for-tabs` flag.</span></span>  

<span data-ttu-id="06f7c-122">Windows \ (CMD \):</span><span class="sxs-lookup"><span data-stu-id="06f7c-122">Windows \(CMD\):</span></span>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

<span data-ttu-id="06f7c-123">Windows \ (PowerShell \):</span><span class="sxs-lookup"><span data-stu-id="06f7c-123">Windows \(PowerShell\):</span></span>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

<span data-ttu-id="06f7c-124">MacOS</span><span class="sxs-lookup"><span data-stu-id="06f7c-124">macOS:</span></span>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Figure 1: option inspecter"  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Figure 2: ouverture de DevTools à partir du menu principal de Microsoft Edge"  

<!-- links -->  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> <span data-ttu-id="06f7c-127">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06f7c-127">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="06f7c-128">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/open) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="06f7c-128">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/open) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="06f7c-130">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06f7c-130">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
